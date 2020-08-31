---
title: Заметки о выпуске Azure PowerShell
description: Узнайте обо всех последних обновлениях модулей Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: ea8169e0aa04fb4cc27b715ef9dfde86f0e75e85
ms.sourcegitcommit: b94a3f00c147144b0ef7f8cf8d0f151e04674b89
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/25/2020
ms.locfileid: "88821963"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="a6e72-103">Заметки о выпуске Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="a6e72-103">Azure PowerShell release notes</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="a6e72-104">4.6.0 — август 2020 г.</span><span class="sxs-lookup"><span data-stu-id="a6e72-104">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a6e72-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e72-105">Az.Accounts</span></span>
* <span data-ttu-id="a6e72-106">Загружаются все общедоступные облачные среды, когда конечная точка обнаружения не возвращает AzureCloud по умолчанию или другие общедоступные среды [№ 12633]</span><span class="sxs-lookup"><span data-stu-id="a6e72-106">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="a6e72-107">В Get-AzSubscription предоставлен параметр SubscriptionPolicies [№ 12551].</span><span class="sxs-lookup"><span data-stu-id="a6e72-107">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a6e72-108">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a6e72-108">Az.Automation</span></span>
* <span data-ttu-id="a6e72-109">В Set-AzAutomationWebhook добавлен параметр -RunOn для определения группы гибридной рабочей роли.</span><span class="sxs-lookup"><span data-stu-id="a6e72-109">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e72-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e72-110">Az.Compute</span></span>
* <span data-ttu-id="a6e72-111">В New-AzVm, New-AzVmss, New-AzVMConfig, New-AzVmssConfig, Update-AzVM и Update-AzVmss добавлен параметр -EncryptionAtHost.</span><span class="sxs-lookup"><span data-stu-id="a6e72-111">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="a6e72-112">В возвращаемый объект Get-AzVM и Get-AzVmss добавлен параметр SecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="a6e72-112">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="a6e72-113">В Get-AzHostGroup добавлен необязательный параметр -InstanceView.</span><span class="sxs-lookup"><span data-stu-id="a6e72-113">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="a6e72-114">Добавлен новый командлет Invoke-AzVmPatchAssessment.</span><span class="sxs-lookup"><span data-stu-id="a6e72-114">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a6e72-115">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a6e72-115">Az.DataFactory</span></span>
* <span data-ttu-id="a6e72-116">В класс PSPipelineRun добавлены отсутствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a6e72-116">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a6e72-117">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a6e72-117">Az.HDInsight</span></span>
* <span data-ttu-id="a6e72-118">Включена поддержка создания кластера с функцией шифрования на узле.</span><span class="sxs-lookup"><span data-stu-id="a6e72-118">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a6e72-119">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a6e72-119">Az.KeyVault</span></span>
* <span data-ttu-id="a6e72-120">Добавлены предупреждающие сообщения для планирования отключения обратимого удаления.</span><span class="sxs-lookup"><span data-stu-id="a6e72-120">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="a6e72-121">Добавлены предупреждающие сообщения для планирования удаления атрибута SecretValueText.</span><span class="sxs-lookup"><span data-stu-id="a6e72-121">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="a6e72-122">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="a6e72-122">Az.Maintenance</span></span>
* <span data-ttu-id="a6e72-123">В New-AzMaintenanceConfiguration добавлены дополнительные поля, связанные с расписанием.</span><span class="sxs-lookup"><span data-stu-id="a6e72-123">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="a6e72-124">Добавлен новый командлет для Get-AzMaintenancePublicConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a6e72-124">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="a6e72-125">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-125">Az.ManagedServices</span></span>
* <span data-ttu-id="a6e72-126">Добавлены предупреждения о критических изменениях в командлетах назначения и определения управляемых служб.</span><span class="sxs-lookup"><span data-stu-id="a6e72-126">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a6e72-127">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a6e72-127">Az.Monitor</span></span>
* <span data-ttu-id="a6e72-128">Расширен набор параметров, заданный в Set-AzDiagnosticSetting, для разделения включения журналов и метрик [№ 12482].</span><span class="sxs-lookup"><span data-stu-id="a6e72-128">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="a6e72-129">Для Add-AzMetricAlertRuleV2 исправлена ошибка, возникающая при получении оповещения метрики из конвейера.</span><span class="sxs-lookup"><span data-stu-id="a6e72-129">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e72-130">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e72-130">Az.Resources</span></span>
* <span data-ttu-id="a6e72-131">Изменен ответ Get-AzPolicyAlias для включения сведений о том, изменяется ли этот псевдоним Политикой Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-131">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="a6e72-132">Создан новый командлет Set-AzRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="a6e72-132">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="a6e72-133">Добавлен командлет Get-AzDeploymentManagementGroupWhatIfResult для получения результатов выполнения What-If в шаблоне ARM в области группы управления.</span><span class="sxs-lookup"><span data-stu-id="a6e72-133">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="a6e72-134">Добавлен командлет Get-AzTenantWhatIfResult для получения результатов выполнения What-If в шаблоне ARM в области арендатора.</span><span class="sxs-lookup"><span data-stu-id="a6e72-134">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="a6e72-135">Переопределены параметры -WhatIf и -Confirm для New-AzManagementGroupDeployment и New-AzTenantDeployment для использования результатов выполнения What-If в шаблоне ARM.</span><span class="sxs-lookup"><span data-stu-id="a6e72-135">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="a6e72-136">Исправлено поведение параметров -WhatIf и -Confirm для новых командлетов развертывания, чтобы они соответствовали значению False.</span><span class="sxs-lookup"><span data-stu-id="a6e72-136">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="a6e72-137">Исправлена ошибка сериализации для -TemplateObject и TemplateParameterObject [№ 1528] [№ 6292].</span><span class="sxs-lookup"><span data-stu-id="a6e72-137">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="a6e72-138">Добавлен атрибут критического изменения в Get-AzResourceGroupDeploymentOperation для предстоящего изменения типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a6e72-138">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a6e72-139">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a6e72-139">Az.SignalR</span></span>
* <span data-ttu-id="a6e72-140">Исправлены ошибки файлов справки Restart-AzSignalR и Update-AzSignalR.</span><span class="sxs-lookup"><span data-stu-id="a6e72-140">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="a6e72-141">Добавлены командлеты Update-AzSignalRNetworkAcl, Set-AzSignalRUpstream.</span><span class="sxs-lookup"><span data-stu-id="a6e72-141">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a6e72-142">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6e72-142">Az.Storage</span></span>
* <span data-ttu-id="a6e72-143">Поддерживается ускорение запросов больших двоичных объектов:</span><span class="sxs-lookup"><span data-stu-id="a6e72-143">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="a6e72-144">Get-AzStorageBlobQueryResult;</span><span class="sxs-lookup"><span data-stu-id="a6e72-144">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="a6e72-145">New-AzStorageBlobQueryConfig.</span><span class="sxs-lookup"><span data-stu-id="a6e72-145">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="a6e72-146">Обновлен файл справки; дополнено описание и исправлена опечатка.</span><span class="sxs-lookup"><span data-stu-id="a6e72-146">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="a6e72-147">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a6e72-147">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="a6e72-148">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="a6e72-148">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="a6e72-149">Исправлена ошибка, из-за которой работа большого двоичного объекта завершается ошибкой, если связанный подкаталог не существует [№ 12592].</span><span class="sxs-lookup"><span data-stu-id="a6e72-149">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="a6e72-150">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a6e72-150">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="a6e72-151">Включена поддержка задания, получения и удаления политики репликации объекта в учетных записях хранения:</span><span class="sxs-lookup"><span data-stu-id="a6e72-151">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="a6e72-152">New-AzStorageObjectReplicationPolicyRule;</span><span class="sxs-lookup"><span data-stu-id="a6e72-152">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="a6e72-153">Set-AzStorageObjectReplicationPolicy;</span><span class="sxs-lookup"><span data-stu-id="a6e72-153">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="a6e72-154">Get-AzStorageObjectReplicationPolicy;</span><span class="sxs-lookup"><span data-stu-id="a6e72-154">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="a6e72-155">Remove-AzStorageObjectReplicationPolicy.</span><span class="sxs-lookup"><span data-stu-id="a6e72-155">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="a6e72-156">Включена поддержка включения и отключения канала изменений в службе BLOB-объектов учетной записи хранения:</span><span class="sxs-lookup"><span data-stu-id="a6e72-156">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="a6e72-157">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="a6e72-157">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="a6e72-158">4.5.0 — август 2020 г.</span><span class="sxs-lookup"><span data-stu-id="a6e72-158">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a6e72-159">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e72-159">Az.Accounts</span></span>
* <span data-ttu-id="a6e72-160">Командлет Connect-AzAccount теперь принимает параметр MaxContextPopulation (№ 9865).</span><span class="sxs-lookup"><span data-stu-id="a6e72-160">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="a6e72-161">Версия SubscriptionClient обновлена до 2019-06-01 и поддерживает отображение доменов арендаторов (№ 9838).</span><span class="sxs-lookup"><span data-stu-id="a6e72-161">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="a6e72-162">Добавлена поддержка домашнего арендатора и сведений managedBy арендатора для подписки.</span><span class="sxs-lookup"><span data-stu-id="a6e72-162">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="a6e72-163">Исправлено имя модуля и сведения о версии в данных телеметрии.</span><span class="sxs-lookup"><span data-stu-id="a6e72-163">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="a6e72-164">Исправлено поведение SqlDatabaseDnsSuffix и ServiceManagementUrl, когда конечная точка метаданных среды возвращает несовместимое значение.</span><span class="sxs-lookup"><span data-stu-id="a6e72-164">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="a6e72-165">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a6e72-165">Az.Aks</span></span>
* <span data-ttu-id="a6e72-166">Параметр ClientIdAndSecret замен на ServicePrincipalIdAndSecret и задан в виде псевдонима (№ 12381).</span><span class="sxs-lookup"><span data-stu-id="a6e72-166">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="a6e72-167">Командлеты Get-AzAks, New-AzAks, Remove-AzAks, Set-AzAks заменены на Get-AzAksCluster, New-AzAksCluster, Remove-AzAksCluster, Set-AzAksCluster. Исходные командлеты заданы в виде псевдонимов (№ 12373).</span><span class="sxs-lookup"><span data-stu-id="a6e72-167">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a6e72-168">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a6e72-168">Az.ApiManagement</span></span>
* <span data-ttu-id="a6e72-169">Добавлен новый командлет Add-AzApiManagementApiToGateway.</span><span class="sxs-lookup"><span data-stu-id="a6e72-169">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="a6e72-170">Добавлен новый командлет Get-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="a6e72-170">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="a6e72-171">Добавлен новый командлет Get-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a6e72-171">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="a6e72-172">Добавлен новый командлет Get-AzApiManagementGatewayKey.</span><span class="sxs-lookup"><span data-stu-id="a6e72-172">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="a6e72-173">Добавлен новый командлет New-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="a6e72-173">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="a6e72-174">Добавлен новый командлет New-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a6e72-174">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="a6e72-175">Добавлен новый командлет New-AzApiManagementResourceLocationObject.</span><span class="sxs-lookup"><span data-stu-id="a6e72-175">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="a6e72-176">Добавлен новый командлет Remove-AzApiManagementApiFromGateway.</span><span class="sxs-lookup"><span data-stu-id="a6e72-176">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="a6e72-177">Добавлен новый командлет Remove-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="a6e72-177">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="a6e72-178">Добавлен новый командлет Remove-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a6e72-178">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="a6e72-179">Добавлен новый командлет Update-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="a6e72-179">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="a6e72-180">Добавлен новый необязательный параметр [-GatewayId] в командлет Get-AzApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="a6e72-180">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a6e72-181">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-181">Az.CognitiveServices</span></span>
* <span data-ttu-id="a6e72-182">Задано явное использование действия "Отклонить" в качестве действия NetworkRules по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a6e72-182">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a6e72-183">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a6e72-183">Az.FrontDoor</span></span>
* <span data-ttu-id="a6e72-184">Исправлена проблема, связанная с возникновением исключения при попытке Enum.Parse привести значение NULL к значениям перечисления Enabled или Disabled (№ 12344).</span><span class="sxs-lookup"><span data-stu-id="a6e72-184">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a6e72-185">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a6e72-185">Az.HDInsight</span></span>
* <span data-ttu-id="a6e72-186">Добавлена поддержка создания кластера с функцией шифрования передаваемых данных.</span><span class="sxs-lookup"><span data-stu-id="a6e72-186">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="a6e72-187">Добавлен новый параметр EncryptionInTransit в командлет New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="a6e72-187">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="a6e72-188">Добавлен новый параметр EncryptionInTransit в командлет New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="a6e72-188">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="a6e72-189">Добавлена поддержка создания кластера с функцией приватного канала:</span><span class="sxs-lookup"><span data-stu-id="a6e72-189">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="a6e72-190">Добавлен новый параметр PublicNetworkAccessType и OutboundPublicNetworkAccessType в командлет New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="a6e72-190">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="a6e72-191">Добавлен новый параметр PublicNetworkAccessType и OutboundPublicNetworkAccessType в командлет New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="a6e72-191">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="a6e72-192">Реализовано возвращение сведений о виртуальной сети при вызове New-AzHDInsightCluster или Get-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="a6e72-192">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e72-193">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e72-193">Az.Network</span></span>
* <span data-ttu-id="a6e72-194">Включена поддержка параметра AddressPrefixType в Remove-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="a6e72-194">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="a6e72-195">Реализованы некритические изменения: функциональность PeerAddressType для частного пиринга в Remove-AzExpressRouteCircutPeeringConfig.</span><span class="sxs-lookup"><span data-stu-id="a6e72-195">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="a6e72-196">Код изменен для игнорирования регистра в параметрах AddressPrefixType и PeerAddressType.</span><span class="sxs-lookup"><span data-stu-id="a6e72-196">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="a6e72-197">Изменено сообщение с предупреждением для New-AzLoadBalancerFrontendIpConfig, New-AzPublicIpAddress и New-AzPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="a6e72-197">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a6e72-198">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a6e72-198">Az.OperationalInsights</span></span>
* <span data-ttu-id="a6e72-199">Добавлен параметр -ForceDelete для Remove-AzOperationalInsightsworkspace.</span><span class="sxs-lookup"><span data-stu-id="a6e72-199">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="a6e72-200">Добавлен новый командлет Get-AzOperationalInsightsDeletedWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a6e72-200">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="a6e72-201">Добавлен новый командлет Restore-AzOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a6e72-201">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a6e72-202">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-202">Az.RecoveryServices</span></span>
* <span data-ttu-id="a6e72-203">Улучшена работа с обнаружением контейнеров и элементов Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="a6e72-203">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e72-204">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e72-204">Az.Resources</span></span>
* <span data-ttu-id="a6e72-205">Добавлены свойства Condition, ConditionVersion и Description в New-AzRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="a6e72-205">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="a6e72-206">Это касается всех соответствующих изменений моделей данных.</span><span class="sxs-lookup"><span data-stu-id="a6e72-206">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e72-207">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e72-207">Az.Sql</span></span>
* <span data-ttu-id="a6e72-208">Исправлена ошибка, связанная с потенциальным игнорированием регистра имени сервера в New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="a6e72-208">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="a6e72-209">Исправлена ошибка, из-за которой возвращалось неправильное имя существующей базы данных в New-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="a6e72-209">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a6e72-210">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6e72-210">Az.Storage</span></span>
* <span data-ttu-id="a6e72-211">Добавлена поддержка создания маркера SAS контейнера и BLOB-объекта с новым разрешением x,t.</span><span class="sxs-lookup"><span data-stu-id="a6e72-211">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="a6e72-212">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="a6e72-212">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="a6e72-213">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="a6e72-213">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="a6e72-214">Добавлена поддержка создания маркера SAS учетной записи с новым разрешением x,t,f.</span><span class="sxs-lookup"><span data-stu-id="a6e72-214">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="a6e72-215">New-AzStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="a6e72-215">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="a6e72-216">Добавлена поддержка получения данных об использовании одной общей папки.</span><span class="sxs-lookup"><span data-stu-id="a6e72-216">Supported get single file share usage</span></span>
    - <span data-ttu-id="a6e72-217">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="a6e72-217">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="a6e72-218">4.4.0 — июль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="a6e72-218">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a6e72-219">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e72-219">Az.Accounts</span></span>
* <span data-ttu-id="a6e72-220">Добавлен новый командлет Invoke-AzRestMethod.</span><span class="sxs-lookup"><span data-stu-id="a6e72-220">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="a6e72-221">Устранена неполадка, из-за которой могли возникать ошибки с проверкой подлинности в сценариях с несколькими процессами, такими как выполнение нескольких командлетов Azure PowerShell с помощью Start-Job [№ 9448].</span><span class="sxs-lookup"><span data-stu-id="a6e72-221">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="a6e72-222">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a6e72-222">Az.Aks</span></span>
* <span data-ttu-id="a6e72-223">Исправлена ошибка, из-за которой Get-AzAks выводит не все кластеры [ №12296].</span><span class="sxs-lookup"><span data-stu-id="a6e72-223">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a6e72-224">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-224">Az.AnalysisServices</span></span>
* <span data-ttu-id="a6e72-225">Удалена ссылка на проект для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="a6e72-225">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a6e72-226">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a6e72-226">Az.Automation</span></span>
* <span data-ttu-id="a6e72-227">Исправлена ошибка, из-за которой строка с escape-символами не преобразовывалась в объект JSON.</span><span class="sxs-lookup"><span data-stu-id="a6e72-227">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e72-228">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e72-228">Az.Compute</span></span>
* <span data-ttu-id="a6e72-229">Добавлено предупреждение, которое отображается при использовании New-AzVmss, если версия образа не является последней.</span><span class="sxs-lookup"><span data-stu-id="a6e72-229">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a6e72-230">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a6e72-230">Az.DataFactory</span></span>
* <span data-ttu-id="a6e72-231">Добавлены глобальные параметры в Фабрику данных.</span><span class="sxs-lookup"><span data-stu-id="a6e72-231">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a6e72-232">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a6e72-232">Az.EventGrid</span></span>
* <span data-ttu-id="a6e72-233">Обновлен модуль для использования API версии 2020-06-01.</span><span class="sxs-lookup"><span data-stu-id="a6e72-233">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="a6e72-234">Добавлены новые возможности:</span><span class="sxs-lookup"><span data-stu-id="a6e72-234">Added new features:</span></span>
    - <span data-ttu-id="a6e72-235">сопоставление входных данных;</span><span class="sxs-lookup"><span data-stu-id="a6e72-235">Input mapping</span></span>
    - <span data-ttu-id="a6e72-236">схема доставки событий;</span><span class="sxs-lookup"><span data-stu-id="a6e72-236">Event Delivery Schema</span></span>
    - <span data-ttu-id="a6e72-237">Приватный канал</span><span class="sxs-lookup"><span data-stu-id="a6e72-237">Private Link</span></span>
    - <span data-ttu-id="a6e72-238">схема событий облака (версия 1.0);</span><span class="sxs-lookup"><span data-stu-id="a6e72-238">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="a6e72-239">раздел служебной шины как назначение;</span><span class="sxs-lookup"><span data-stu-id="a6e72-239">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="a6e72-240">функция Azure как назначение;</span><span class="sxs-lookup"><span data-stu-id="a6e72-240">Azure Function As Destination</span></span>
    - <span data-ttu-id="a6e72-241">пакетная обработка данных веб-перехватчика;</span><span class="sxs-lookup"><span data-stu-id="a6e72-241">WebHook Batching</span></span>
    - <span data-ttu-id="a6e72-242">безопасный веб-перехватчик (поддержка AAD);</span><span class="sxs-lookup"><span data-stu-id="a6e72-242">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="a6e72-243">фильтрация IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="a6e72-243">IpFiltering</span></span>
* <span data-ttu-id="a6e72-244">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="a6e72-244">Updated cmdlets:</span></span>
    - <span data-ttu-id="a6e72-245">New-AzEventGridSubscription или Update-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="a6e72-245">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="a6e72-246">Добавлены новые необязательные параметры для поддержки пакетной обработки данных веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="a6e72-246">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="a6e72-247">Добавлены новые необязательные параметры для поддержки безопасного веб-перехватчика с использованием AAD.</span><span class="sxs-lookup"><span data-stu-id="a6e72-247">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="a6e72-248">Добавлено новое перечисление для параметра EndpointType, чтобы обеспечить поддержку функции Azure и раздела служебной шины в качестве назначения.</span><span class="sxs-lookup"><span data-stu-id="a6e72-248">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="a6e72-249">Добавлен новый необязательный параметр для схемы доставки.</span><span class="sxs-lookup"><span data-stu-id="a6e72-249">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="a6e72-250">New-AzEventGridTopic или Update-AzEventGridTopic и New-AzEventGridDomain или Update-AzEventGridDomain:</span><span class="sxs-lookup"><span data-stu-id="a6e72-250">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="a6e72-251">Добавлены новые необязательные параметры для поддержки фильтрации IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="a6e72-251">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="a6e72-252">New-AzEventGridTopic или New-AzEventGridDomain:</span><span class="sxs-lookup"><span data-stu-id="a6e72-252">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="a6e72-253">Добавлены новые необязательные параметры для поддержки сопоставления входных данных.</span><span class="sxs-lookup"><span data-stu-id="a6e72-253">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a6e72-254">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a6e72-254">Az.FrontDoor</span></span>
* <span data-ttu-id="a6e72-255">Обновлен модуль для использования API версии 2020-05-01.</span><span class="sxs-lookup"><span data-stu-id="a6e72-255">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="a6e72-256">Включена поддержка Приватного канала для ресурсов службы хранилища, Key Vault и службы веб-приложений.</span><span class="sxs-lookup"><span data-stu-id="a6e72-256">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a6e72-257">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a6e72-257">Az.HDInsight</span></span>
* <span data-ttu-id="a6e72-258">Включена поддержка создания кластера с хранилищем ADLS 1-го и 2-го поколения в национальных облаках.</span><span class="sxs-lookup"><span data-stu-id="a6e72-258">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a6e72-259">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a6e72-259">Az.Monitor</span></span>
* <span data-ttu-id="a6e72-260">Исправлена ошибка с Get-AzDiagnosticSetting, связанная с присвоением значения NULL метрикам или журналам [№ 12272].</span><span class="sxs-lookup"><span data-stu-id="a6e72-260">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e72-261">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e72-261">Az.Network</span></span>
* <span data-ttu-id="a6e72-262">Исправлены ошибки с переключением параметров для подключения виртуальной сети концентратора к глобальной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="a6e72-262">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="a6e72-263">Добавлены новые командлеты для сайтов сетевых виртуальных модулей Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-263">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="a6e72-264">Get-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="a6e72-264">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="a6e72-265">New-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="a6e72-265">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="a6e72-266">Remove-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="a6e72-266">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="a6e72-267">Update-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="a6e72-267">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="a6e72-268">New-AzOffice365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="a6e72-268">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="a6e72-269">Добавлены новые командлеты для сетевого виртуального модуля Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-269">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="a6e72-270">Get-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="a6e72-270">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="a6e72-271">New-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="a6e72-271">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="a6e72-272">Remove-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="a6e72-272">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="a6e72-273">Update-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="a6e72-273">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="a6e72-274">Get-AzNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="a6e72-274">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="a6e72-275">New-AzVirtualApplianceSkuProperty</span><span class="sxs-lookup"><span data-stu-id="a6e72-275">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="a6e72-276">Общие командлеты для Шлюза приложений, подключенного к Приватному каналу.</span><span class="sxs-lookup"><span data-stu-id="a6e72-276">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="a6e72-277">Общие командлеты для службы синхронизации хранилища, подключенной к Приватному каналу.</span><span class="sxs-lookup"><span data-stu-id="a6e72-277">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="a6e72-278">Общие командлеты для службы SignalR, подключенной к Приватному каналу.</span><span class="sxs-lookup"><span data-stu-id="a6e72-278">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a6e72-279">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-279">Az.RecoveryServices</span></span>
* <span data-ttu-id="a6e72-280">Удалена ссылка на проект для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="a6e72-280">Removed project reference to Authentication</span></span>
* <span data-ttu-id="a6e72-281">В Azure Backup представлена более точная справка по командлетам.</span><span class="sxs-lookup"><span data-stu-id="a6e72-281">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="a6e72-282">В Azure Backup включена поддержка выборки заданий агента MAB с помощью командлета Get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="a6e72-282">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e72-283">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e72-283">Az.Resources</span></span>
* <span data-ttu-id="a6e72-284">Обновлен командлет Save-AzResourceGroupDeploymentTemplate для использования пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="a6e72-284">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="a6e72-285">Добавлен командлет Unregister-AzResourceProvider.</span><span class="sxs-lookup"><span data-stu-id="a6e72-285">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e72-286">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e72-286">Az.Sql</span></span>
* <span data-ttu-id="a6e72-287">Включена поддержка субъекта-службы и гостевых пользователей для командлета Set-AzSqlInstanceActiveDirectoryAdministrator.</span><span class="sxs-lookup"><span data-stu-id="a6e72-287">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="a6e72-288">Исправлена ошибка в командлетах классификации данных.</span><span class="sxs-lookup"><span data-stu-id="a6e72-288">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="a6e72-289">Включена поддержка отработки отказа Управляемого экземпляра SQL Azure. Invoke-AzSqlInstanceFailover</span><span class="sxs-lookup"><span data-stu-id="a6e72-289">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a6e72-290">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6e72-290">Az.Storage</span></span>
* <span data-ttu-id="a6e72-291">Исправлена ошибка, из-за которой в некоторых командлетах плоскости данных не добавлялся объект UserAgent.</span><span class="sxs-lookup"><span data-stu-id="a6e72-291">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="a6e72-292">Включена поддержка создания и обновления учетной записи хранения с использованием MinimumTlsVersion и AllowBlobPublicAccess.</span><span class="sxs-lookup"><span data-stu-id="a6e72-292">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="a6e72-293">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a6e72-293">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="a6e72-294">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a6e72-294">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="a6e72-295">Включена поддержка включения и отключения управления версиями в службе BLOB-объектов учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="a6e72-295">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="a6e72-296">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="a6e72-296">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="a6e72-297">Включена поддержка вывода списка BLOB-объектов с данными о версиях BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="a6e72-297">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="a6e72-298">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="a6e72-298">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="a6e72-299">Включена поддержка получения или удаления одного моментального снимка BLOB-объекта или версии BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="a6e72-299">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="a6e72-300">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="a6e72-300">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="a6e72-301">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="a6e72-301">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="a6e72-302">Включена поддержка конвейера на основе BLOB-объекта, созданного с помощью Azure.Storage.Blobs версии 12.</span><span class="sxs-lookup"><span data-stu-id="a6e72-302">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="a6e72-303">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a6e72-303">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="a6e72-304">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="a6e72-304">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="a6e72-305">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="a6e72-305">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="a6e72-306">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a6e72-306">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="a6e72-307">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a6e72-307">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="a6e72-308">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="a6e72-308">Az.StorageSync</span></span>
* <span data-ttu-id="a6e72-309">Добавлена новая версия пакета SDK StorageSync, предназначенная для API версии 2020-03-01.</span><span class="sxs-lookup"><span data-stu-id="a6e72-309">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="a6e72-310">Добавлен командлет для обновления службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="a6e72-310">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="a6e72-311">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="a6e72-311">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="a6e72-312">Добавлены классы IncomingTrafficPolicy и IncomingTrafficPolicy в командлеты службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="a6e72-312">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a6e72-313">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6e72-313">Az.Websites</span></span>
* <span data-ttu-id="a6e72-314">Включена поддержка выполнения операций для слотов, которые находятся не в той же группе ресурсов, что и план службы приложений.</span><span class="sxs-lookup"><span data-stu-id="a6e72-314">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="a6e72-315">4.3.0 — июнь 2020 года</span><span class="sxs-lookup"><span data-stu-id="a6e72-315">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a6e72-316">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e72-316">Az.Accounts</span></span>
* <span data-ttu-id="a6e72-317">Включена поддержка обнаружения параметров среды по умолчанию и добавления окружения с помощью командлета Add-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="a6e72-317">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="a6e72-318">Обновлены предварительно загруженные сборки [№ 12024], [№ 11976].</span><span class="sxs-lookup"><span data-stu-id="a6e72-318">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="a6e72-319">Обновлена сборка Azure.Core.</span><span class="sxs-lookup"><span data-stu-id="a6e72-319">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="a6e72-320">Исправлена ошибка, из-за которой выполнение Connect-AzAccount может завершаться сбоем при многопоточном выполнении [№ 11201].</span><span class="sxs-lookup"><span data-stu-id="a6e72-320">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="a6e72-321">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a6e72-321">Az.Aks</span></span>
* <span data-ttu-id="a6e72-322">Заменено использование старого [API AccessProfile](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) вызовами API [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) и [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials).</span><span class="sxs-lookup"><span data-stu-id="a6e72-322">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a6e72-323">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a6e72-323">Az.Batch</span></span>
* <span data-ttu-id="a6e72-324">Изменена версия SDK для Microsoft.Azure.Management.Batch для Az.Batch на 11.0.0.</span><span class="sxs-lookup"><span data-stu-id="a6e72-324">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="a6e72-325">Включена возможность задать удостоверение BatchAccount в командлете New-AzBatchAccount.</span><span class="sxs-lookup"><span data-stu-id="a6e72-325">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a6e72-326">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-326">Az.CognitiveServices</span></span>
* <span data-ttu-id="a6e72-327">Включена поддержка отображения возможностей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="a6e72-327">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="a6e72-328">Включена поддержка изменения PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="a6e72-328">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e72-329">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e72-329">Az.Compute</span></span>
* <span data-ttu-id="a6e72-330">Добавлен параметр SimulateEviction в командлеты Set-AzVM и Set-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="a6e72-330">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="a6e72-331">Добавлен фрагмент Premium_LRS в средство заполнения аргументов параметра StorageAccountType для командлета New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="a6e72-331">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="a6e72-332">Добавлены подсостояния для VMCustomScriptExtension [№ 11297].</span><span class="sxs-lookup"><span data-stu-id="a6e72-332">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="a6e72-333">Добавлен фрагмент Delete в средство заполнения аргументов параметра EvictionPolicy для командлетов New-AzVM и New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="a6e72-333">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="a6e72-334">Исправлено имя нового расширения виртуальной машины для SAP.</span><span class="sxs-lookup"><span data-stu-id="a6e72-334">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a6e72-335">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a6e72-335">Az.DataFactory</span></span>
* <span data-ttu-id="a6e72-336">Обновлен пакет SDK ADF для .NET до версии 4.9.0.</span><span class="sxs-lookup"><span data-stu-id="a6e72-336">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a6e72-337">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a6e72-337">Az.EventHub</span></span>
* <span data-ttu-id="a6e72-338">Добавлены параметры управляемого удостоверения для командлетов New-AzEventHubNamespace и Set-AzEventHubNamespace.</span><span class="sxs-lookup"><span data-stu-id="a6e72-338">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="a6e72-339">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="a6e72-339">Az.Functions</span></span>
* <span data-ttu-id="a6e72-340">Включена поддержка создания приложений-функций PowerShell 7.0 и Java 11.</span><span class="sxs-lookup"><span data-stu-id="a6e72-340">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a6e72-341">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a6e72-341">Az.HDInsight</span></span>
* <span data-ttu-id="a6e72-342">Включена поддержка перечисления узлов и перезагрузка отдельных узлов кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="a6e72-342">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="a6e72-343">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="a6e72-343">Az.HealthcareApis</span></span>
* <span data-ttu-id="a6e72-344">Обновлен пакет SDK до версии 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="a6e72-344">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="a6e72-345">Включена поддержка параметров экспорта и управляемого удостоверения.</span><span class="sxs-lookup"><span data-stu-id="a6e72-345">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a6e72-346">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a6e72-346">Az.Monitor</span></span>
* <span data-ttu-id="a6e72-347">Исправлен входной параметр объекта для Set-AzActivityLogAlert.</span><span class="sxs-lookup"><span data-stu-id="a6e72-347">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="a6e72-348">Исправлен параметр InputObject для Set-AzActionGroup [№ 10868].</span><span class="sxs-lookup"><span data-stu-id="a6e72-348">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e72-349">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e72-349">Az.Network</span></span>
* <span data-ttu-id="a6e72-350">Включена поддержка параметра AddressPrefixType в Remove-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="a6e72-350">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="a6e72-351">Добавлены новые командлеты для политики Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-351">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="a6e72-352">New-AzFirewallPolicyDnsSetting</span><span class="sxs-lookup"><span data-stu-id="a6e72-352">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="a6e72-353">Включена поддержка полного доменного имени назначения в правилах сети для политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="a6e72-353">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="a6e72-354">Включена поддержка операций серверного пула адресов:</span><span class="sxs-lookup"><span data-stu-id="a6e72-354">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="a6e72-355">New-AzLoadBalancerBackendAddressConfig</span><span class="sxs-lookup"><span data-stu-id="a6e72-355">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="a6e72-356">New-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a6e72-356">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="a6e72-357">Set-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a6e72-357">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="a6e72-358">Remove-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a6e72-358">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="a6e72-359">Get-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a6e72-359">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="a6e72-360">Добавлена проверка имени для New-AzIpGroup.</span><span class="sxs-lookup"><span data-stu-id="a6e72-360">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="a6e72-361">Добавлены новые командлеты для политики Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-361">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="a6e72-362">New-AzFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="a6e72-362">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="a6e72-363">Обновлены следующие команды для функции: Включена возможность настройки и удаления пользовательских DNS-серверов в шлюзе VPN P2S виртуальной глобальной сети.</span><span class="sxs-lookup"><span data-stu-id="a6e72-363">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="a6e72-364">Обновлен командлет New-AzP2sVpnGateway: добавлен необязательный параметр -CustomDnsServer, чтобы пользователи могли указывать свои DNS-серверы для настройки в шлюзе VPN P2S для использования клиентами с подключением "точка — сеть".</span><span class="sxs-lookup"><span data-stu-id="a6e72-364">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="a6e72-365">Обновлен командлет Update-AzP2sVpnGateway: добавлен необязательный параметр -CustomDnsServer, чтобы пользователи могли указывать свои DNS-серверы для настройки в шлюзе VPN P2S для использования клиентами с подключением "точка — сеть".</span><span class="sxs-lookup"><span data-stu-id="a6e72-365">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="a6e72-366">Обновлен командлет Update-AzVpnGateway:</span><span class="sxs-lookup"><span data-stu-id="a6e72-366">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="a6e72-367">добавлен необязательный параметр -BgpPeeringAddress, чтобы клиенты могли указывать пользовательские маршруты BGP для настройки в шлюзе VPN.</span><span class="sxs-lookup"><span data-stu-id="a6e72-367">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="a6e72-368">Добавлен новый командлет для сброса состояния маршрутизации ресурса VirtualHub:</span><span class="sxs-lookup"><span data-stu-id="a6e72-368">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="a6e72-369">Reset-AzHubRouter</span><span class="sxs-lookup"><span data-stu-id="a6e72-369">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="a6e72-370">Следующие обновления основаны на последнем изменении Swagger для политики брандмауэра:</span><span class="sxs-lookup"><span data-stu-id="a6e72-370">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="a6e72-371">изменены имена для RuleGroup, RuleCollectionGroup и RuleType;</span><span class="sxs-lookup"><span data-stu-id="a6e72-371">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="a6e72-372">включена поддержка коллекций правил NAT политики брандмауэра для поддержки нескольких коллекций правил NAT.</span><span class="sxs-lookup"><span data-stu-id="a6e72-372">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="a6e72-373">[Критическое изменение] Добавлен обязательный параметр SourceIpGroup для командлетов New-AzFirewallPolicyApplicationRule и New-AzFirewallPolicyNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="a6e72-373">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="a6e72-374">[Критическое изменение] Параметр SourceAddress для командлета New-AzFirewallPolicyApplicationRule сделан обязательным.</span><span class="sxs-lookup"><span data-stu-id="a6e72-374">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="a6e72-375">[Критическое изменение] Параметр SourceAddress для командлета New-AzFirewallPolicyApplicationRule сделан обязательным.</span><span class="sxs-lookup"><span data-stu-id="a6e72-375">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="a6e72-376">[Критическое изменение] Удалены обязательные параметры: TranslatedAddress и TranslatedPort для командлета New-AzFirewallPolicyNatRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="a6e72-376">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="a6e72-377">Добавлены новые командлеты для поддержки Приватного канала в Шлюзе приложений:</span><span class="sxs-lookup"><span data-stu-id="a6e72-377">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="a6e72-378">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6e72-378">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="a6e72-379">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6e72-379">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="a6e72-380">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6e72-380">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="a6e72-381">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6e72-381">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="a6e72-382">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6e72-382">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="a6e72-383">New-AzApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6e72-383">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="a6e72-384">Добавлены новые командлеты для дочернего ресурса HubRouteTables VirtualHub:</span><span class="sxs-lookup"><span data-stu-id="a6e72-384">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="a6e72-385">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="a6e72-385">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="a6e72-386">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="a6e72-386">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="a6e72-387">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="a6e72-387">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="a6e72-388">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="a6e72-388">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="a6e72-389">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="a6e72-389">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="a6e72-390">Обновлены существующие командлеты для включения поддержки необязательного входного параметра RoutingConfiguration для настраиваемой маршрутизации в виртуальной глобальной сети.</span><span class="sxs-lookup"><span data-stu-id="a6e72-390">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="a6e72-391">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="a6e72-391">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="a6e72-392">Set-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="a6e72-392">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="a6e72-393">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="a6e72-393">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="a6e72-394">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="a6e72-394">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="a6e72-395">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="a6e72-395">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="a6e72-396">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="a6e72-396">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="a6e72-397">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="a6e72-397">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="a6e72-398">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="a6e72-398">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a6e72-399">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a6e72-399">Az.OperationalInsights</span></span>
* <span data-ttu-id="a6e72-400">Исправлена ошибка, из-за которой PSWorkspace не реализует IOperationalInsightsWorkspace [№ 12135].</span><span class="sxs-lookup"><span data-stu-id="a6e72-400">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="a6e72-401">Добавлено значение pergb2018 в действительный набор значений параметра Sku в командлете Set-AzOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a6e72-401">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="a6e72-402">Добавлен псевдоним FunctionParameters для параметра FunctionParameter:</span><span class="sxs-lookup"><span data-stu-id="a6e72-402">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="a6e72-403">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="a6e72-403">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="a6e72-404">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="a6e72-404">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a6e72-405">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-405">Az.RecoveryServices</span></span>
* <span data-ttu-id="a6e72-406">Включена поддержка выборки элементов MAB в Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="a6e72-406">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="a6e72-407">Включена поддержка типа диска StandardSSD_LRS в Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="a6e72-407">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e72-408">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e72-408">Az.Resources</span></span>
* <span data-ttu-id="a6e72-409">Добавлены параметры UsageLocation, GivenName, Surname, AccountEnabled, MailNickname, Mail для PSADUser [№ 10526], [№ 10497].</span><span class="sxs-lookup"><span data-stu-id="a6e72-409">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="a6e72-410">Исправлена ошибка, из-за которой параметр -Mail не работает в командлете Get-AzADUser [№ 11981].</span><span class="sxs-lookup"><span data-stu-id="a6e72-410">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="a6e72-411">Добавлен параметр -ExcludeChangeType в командлеты Get-AzDeploymentWhatIfResult и Get-AzResourceGroupDeploymentWhatIfResult.</span><span class="sxs-lookup"><span data-stu-id="a6e72-411">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="a6e72-412">Добавлен параметр -WhatIfExcludeChangeType в командлеты New-AzDeployment и New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="a6e72-412">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="a6e72-413">Обновлены командлеты Test-Az\*Deployment для отображения улучшенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="a6e72-413">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="a6e72-414">Исправлено справочное сообщение для параметра -Name в командлетах создания развертывания и командлетах What-If.</span><span class="sxs-lookup"><span data-stu-id="a6e72-414">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e72-415">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e72-415">Az.Sql</span></span>
* <span data-ttu-id="a6e72-416">Включена поддержка субъекта-службы для командлета настройки администратора Azure Active Directory SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a6e72-416">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="a6e72-417">Исправлена ошибка синхронизации в командлетах классификации данных.</span><span class="sxs-lookup"><span data-stu-id="a6e72-417">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="a6e72-418">Включена поддержка поиска пользователей по адресу электронной почты в командлете Set-AzSqlServerActiveDirectoryAdministrator [№ 12192].</span><span class="sxs-lookup"><span data-stu-id="a6e72-418">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a6e72-419">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6e72-419">Az.Storage</span></span>
* <span data-ttu-id="a6e72-420">Включена поддержка создания учетной записи хранения с помощью RequireInfrastructureEncryption.</span><span class="sxs-lookup"><span data-stu-id="a6e72-420">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="a6e72-421">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a6e72-421">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="a6e72-422">Перемещена логика загрузки Azure.Core в Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="a6e72-422">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a6e72-423">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6e72-423">Az.Websites</span></span>
* <span data-ttu-id="a6e72-424">В командлет Restore-AzDeletedWebApp добавлена защитная мера при удалении созданного веб-приложения, если восстановление завершилось сбоем.</span><span class="sxs-lookup"><span data-stu-id="a6e72-424">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="a6e72-425">Добавлены параметры SourceWebApp.Location для командлетов New-AzWebApp и New-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="a6e72-425">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="a6e72-426">Исправлена ошибка, препятствующая изменению параметров контейнера в командлетах Set-AzWebApp и Set-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="a6e72-426">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="a6e72-427">Исправлена ошибка получения SiteConfig, когда параметр -Name не указан для командлета Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="a6e72-427">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="a6e72-428">Включена поддержка создания приложений ASP для Linux.</span><span class="sxs-lookup"><span data-stu-id="a6e72-428">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="a6e72-429">Добавлены исключения для клонирования в группах ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a6e72-429">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="a6e72-430">4.2.0 — июнь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="a6e72-430">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a6e72-431">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e72-431">Az.Accounts</span></span>
* <span data-ttu-id="a6e72-432">Исправлена проблема, из-за которой модуль Az мог пропускать журналы в заданиях службы автоматизации или PowerShell [№ 11492].</span><span class="sxs-lookup"><span data-stu-id="a6e72-432">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a6e72-433">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-433">Az.AnalysisServices</span></span>
* <span data-ttu-id="a6e72-434">Обновлена версия сборки командлетов плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="a6e72-434">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a6e72-435">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a6e72-435">Az.ApiManagement</span></span>
* <span data-ttu-id="a6e72-436">Обновлена версия сборки командлетов управления службами.</span><span class="sxs-lookup"><span data-stu-id="a6e72-436">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="a6e72-437">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="a6e72-437">Az.Billing</span></span>
* <span data-ttu-id="a6e72-438">Обновлена версия сборки командлетов потребления.</span><span class="sxs-lookup"><span data-stu-id="a6e72-438">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a6e72-439">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-439">Az.CognitiveServices</span></span>
* <span data-ttu-id="a6e72-440">Реализована поддержка элементов управления PrivateEndpoint и PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="a6e72-440">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="a6e72-441">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a6e72-441">Az.DataFactory</span></span>
* <span data-ttu-id="a6e72-442">Обновлена версия сборки командлетов фабрики данных версии 2.</span><span class="sxs-lookup"><span data-stu-id="a6e72-442">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="a6e72-443">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="a6e72-443">Az.DataShare</span></span>
* <span data-ttu-id="a6e72-444">Вышла общедоступная версия модуля Az.DataShare.</span><span class="sxs-lookup"><span data-stu-id="a6e72-444">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="a6e72-445">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="a6e72-445">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="a6e72-446">Вышла общедоступная версия модуля Az.DesktopVirtualization.</span><span class="sxs-lookup"><span data-stu-id="a6e72-446">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a6e72-447">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a6e72-447">Az.OperationalInsights</span></span>
* <span data-ttu-id="a6e72-448">Пакет SDK обновлен до версии 0.21.0.</span><span class="sxs-lookup"><span data-stu-id="a6e72-448">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="a6e72-449">Добавлены дополнительные параметры в следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="a6e72-449">Added optional parameters to</span></span> 
    - <span data-ttu-id="a6e72-450">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="a6e72-450">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="a6e72-451">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="a6e72-451">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a6e72-452">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a6e72-452">Az.PolicyInsights</span></span>
* <span data-ttu-id="a6e72-453">Исправлен пример 3 для командлета Start-AzPolicyComplianceScan.</span><span class="sxs-lookup"><span data-stu-id="a6e72-453">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="a6e72-454">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="a6e72-454">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="a6e72-455">Обновлена версия сборки командлетов PowerBI.</span><span class="sxs-lookup"><span data-stu-id="a6e72-455">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="a6e72-456">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="a6e72-456">Az.PrivateDns</span></span>
* <span data-ttu-id="a6e72-457">Исправлено форматирование строки с подробными выходными данными командлета Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="a6e72-457">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a6e72-458">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-458">Az.RecoveryServices</span></span>
* <span data-ttu-id="a6e72-459">Реализована поддержка Azure Site Recovery для создания плана восстановления и репликации между зонами из входного XML-файла.</span><span class="sxs-lookup"><span data-stu-id="a6e72-459">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="a6e72-460">Обновлена версия сборки командлетов SiteRecovery и Backup.</span><span class="sxs-lookup"><span data-stu-id="a6e72-460">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e72-461">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e72-461">Az.Resources</span></span>
* <span data-ttu-id="a6e72-462">Добавлен параметр Tail в командлеты Get-AzDeploymentScriptLog и Save-AzDeploymentScriptLog.</span><span class="sxs-lookup"><span data-stu-id="a6e72-462">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="a6e72-463">Отформатировано свойство Output и включено в отображаемые выходные данные командлета Get-AzDeploymentScript.</span><span class="sxs-lookup"><span data-stu-id="a6e72-463">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="a6e72-464">Параметр -DeploymentScriptInputObject переименован в -DeploymentScriptObject.</span><span class="sxs-lookup"><span data-stu-id="a6e72-464">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="a6e72-465">Исправлена ошибка с отсутствующими именами файлов или целевых объектов в сообщениях командлетов.</span><span class="sxs-lookup"><span data-stu-id="a6e72-465">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="a6e72-466">Обновлена версия сборки командлетов диспетчера ресурсов и обработчика тегов.</span><span class="sxs-lookup"><span data-stu-id="a6e72-466">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e72-467">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e72-467">Az.Sql</span></span>
* <span data-ttu-id="a6e72-468">Добавлен параметр UsePrivateLinkConnection в командлеты New-AzSqlSyncGroup, Update-AzSqlSyncGroup, New-AzSqlSyncMember и Update-AzSqlSyncMember.</span><span class="sxs-lookup"><span data-stu-id="a6e72-468">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="a6e72-469">Добавлен параметр SyncMemberAzureDatabaseResourceId в командлеты New-AzSqlSyncMember и Update-AzSqlSyncMember.</span><span class="sxs-lookup"><span data-stu-id="a6e72-469">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="a6e72-470">Реализована поддержка поиска гостевых пользователей в командлете для настройки администратора Active Directory в SQL Server Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-470">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a6e72-471">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6e72-471">Az.Storage</span></span>
* <span data-ttu-id="a6e72-472">Обновлена версия сборки командлетов плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="a6e72-472">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="a6e72-473">4.1.0 — май 2020 г.</span><span class="sxs-lookup"><span data-stu-id="a6e72-473">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="a6e72-474">Основные сведения о новых возможностях с момента последнего выпуска</span><span class="sxs-lookup"><span data-stu-id="a6e72-474">Highlights since the last release</span></span>
* <span data-ttu-id="a6e72-475">Поддерживаемые версии PowerShell: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="a6e72-475">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="a6e72-476">Вышла общедоступная версия модуля Az.Functions.</span><span class="sxs-lookup"><span data-stu-id="a6e72-476">General availability of Az.Functions</span></span> 
* <span data-ttu-id="a6e72-477">Состоялся основной выпуск Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources и Az.Storage.</span><span class="sxs-lookup"><span data-stu-id="a6e72-477">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a6e72-478">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e72-478">Az.Accounts</span></span>
* <span data-ttu-id="a6e72-479">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметры AzureSynapseAnalyticsEndpointResourceId и AzureSynapseAnalyticsEndpointSuffix.</span><span class="sxs-lookup"><span data-stu-id="a6e72-479">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="a6e72-480">В Az.Accounts добавлены сборки, связанные с Azure.Core. Добавлена поддержка Windows PowerShell 5.1, PowerShell Core 6.2.4 и PowerShell 7+.</span><span class="sxs-lookup"><span data-stu-id="a6e72-480">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="a6e72-481">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a6e72-481">Az.Aks</span></span>
* <span data-ttu-id="a6e72-482">Версия API обновлена до 2019-10-01.</span><span class="sxs-lookup"><span data-stu-id="a6e72-482">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="a6e72-483">Добавлена возможность создания контейнера Windows в службе Azure Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="a6e72-483">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="a6e72-484">Добавлены новые командлеты: New-AzAksNodePool, Update-AzAksNodePool, Remove-AzAksNodePool, Get-AzAksNodePool, Install-AzAksKubectl, Get-AzAksVersion.</span><span class="sxs-lookup"><span data-stu-id="a6e72-484">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a6e72-485">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a6e72-485">Az.ApiManagement</span></span>
* <span data-ttu-id="a6e72-486">В New-AzApiManagement и Set-AzApiManagement параметр -AssignIdentity переименован в -SystemAssignedIdentity.</span><span class="sxs-lookup"><span data-stu-id="a6e72-486">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="a6e72-487">В New-AzApiManagement и Set-AzApiManagement добавлен новый параметр -UserAssignedIdentity <строка[]>.</span><span class="sxs-lookup"><span data-stu-id="a6e72-487">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="a6e72-488">Командлет Get-AzApiManagementProperty переименован в Get-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="a6e72-488">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="a6e72-489">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="a6e72-489">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="a6e72-490">Командлет New-AzApiManagementProperty переименован в New-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="a6e72-490">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="a6e72-491">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="a6e72-491">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="a6e72-492">Командлет Set-AzApiManagementProperty переименован в Set-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="a6e72-492">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="a6e72-493">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="a6e72-493">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="a6e72-494">Командлет Remove-AzApiManagementProperty переименован в Remove-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="a6e72-494">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="a6e72-495">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="a6e72-495">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="a6e72-496">Добавлен новый командлет Get-AzApiManagementAuthorizationServerClientSecret, а Get-AzApiManagementAuthorizationServer теперь не возвращает секрет клиента.</span><span class="sxs-lookup"><span data-stu-id="a6e72-496">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="a6e72-497">Добавлен новый командлет Get-AzApiManagementNamedValueSecretValue, а Get-AzApiManagementNamedValue теперь не возвращает значение секрета.</span><span class="sxs-lookup"><span data-stu-id="a6e72-497">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="a6e72-498">Добавлен новый командлет Get-AzApiManagementOpenIdConnectProviderClientSecret, а Get-AzApiManagementOpenIdConnectProvider теперь не возвращает секрет клиента.</span><span class="sxs-lookup"><span data-stu-id="a6e72-498">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="a6e72-499">Добавлен новый командлет Get-AzApiManagementSubscriptionKey, а Get-AzApiManagementSubscription теперь не возвращает ключи подписки.</span><span class="sxs-lookup"><span data-stu-id="a6e72-499">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="a6e72-500">Добавлен новый командлет Get-AzApiManagementTenantAccessSecret, а Get-AzApiManagementTenantAccess теперь не возвращает ключи.</span><span class="sxs-lookup"><span data-stu-id="a6e72-500">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="a6e72-501">Добавлен новый командлет Get-AzApiManagementTenantGitAccessSecret, а Get-AzApiManagementTenantGitAccess теперь не возвращает ключи.</span><span class="sxs-lookup"><span data-stu-id="a6e72-501">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="a6e72-502">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="a6e72-502">Az.ApplicationInsights</span></span>
* <span data-ttu-id="a6e72-503">В New-AzApplicationInsights добавлены параметры RetentionInDays, PublicNetworkAccessForIngestion и PublicNetworkAccessForQuery.</span><span class="sxs-lookup"><span data-stu-id="a6e72-503">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="a6e72-504">Создан командлет Update-AzApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="a6e72-504">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="a6e72-505">Созданы командлеты для связанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="a6e72-505">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a6e72-506">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a6e72-506">Az.Batch</span></span>
* <span data-ttu-id="a6e72-507">В командлеты Az.Batch добавлена поддержка пакетов SDK Microsoft.Azure.Batch версии 13.0.0 и SDK Microsoft.Azure.Management.Batch версии 9.0.0.</span><span class="sxs-lookup"><span data-stu-id="a6e72-507">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="a6e72-508">Теперь в New-AzBatchCertificate можно выбрать тип добавляемого сертификата с помощью нового параметра -CertificateKind.</span><span class="sxs-lookup"><span data-stu-id="a6e72-508">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="a6e72-509">В PSApplication удалено свойство ApplicationPackages.</span><span class="sxs-lookup"><span data-stu-id="a6e72-509">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="a6e72-510">Отдельные пакеты в приложении теперь можно извлечь с помощью Get-AzBatchApplicationPackage.</span><span class="sxs-lookup"><span data-stu-id="a6e72-510">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="a6e72-511">Пример: Get-AzBatchApplication -AccountName моя_учетная_запись -ResourceGroupName моя_группа_ресурсов -ApplicationId мое_приложение.</span><span class="sxs-lookup"><span data-stu-id="a6e72-511">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="a6e72-512">При создании пула с помощью New-AzBatchPool свойство VirtualMachineImageId элемента PSImageReference теперь может ссылаться только на образ из Общей коллекции образов.</span><span class="sxs-lookup"><span data-stu-id="a6e72-512">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="a6e72-513">При создании пула с помощью New-AzBatchPool пул можно подготовить без общедоступного IP-адреса, используя новое свойство PublicIPAddressConfiguration элемента PSNetworkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a6e72-513">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="a6e72-514">Свойство PublicIPs элемента PSNetworkConfiguration было передано элементу PSPublicIPAddressConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a6e72-514">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="a6e72-515">Это свойство можно указать, только если параметру IPAddressProvisioningType присвоено значение UserManaged.</span><span class="sxs-lookup"><span data-stu-id="a6e72-515">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e72-516">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e72-516">Az.Compute</span></span>
* <span data-ttu-id="a6e72-517">В командлет Update-AzVM добавлен параметр HostId.</span><span class="sxs-lookup"><span data-stu-id="a6e72-517">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="a6e72-518">Обновлена справочная документация по командлетам New-AzVMConfig, New-AzVmssConfig, Update-AzVmss, Set-AzVMOperatingSystem и Set-AzVmssOsProfile.</span><span class="sxs-lookup"><span data-stu-id="a6e72-518">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="a6e72-519">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="a6e72-519">Breaking changes</span></span>
    - <span data-ttu-id="a6e72-520">Параметр FilterExpression удален из командлета Get-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="a6e72-520">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="a6e72-521">Параметр AssignIdentity удален из командлетов New-AzVmssConfig, New-AzVMConfig и Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="a6e72-521">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="a6e72-522">Параметр AutomaticRepairMaxInstanceRepairsPercent удален из командлетов New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="a6e72-522">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="a6e72-523">Свойства AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus и VirtualMachineScaleSetsColocationStatus удалены из ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="a6e72-523">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="a6e72-524">Свойство MaxInstanceRepairsPercent удалено из AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="a6e72-524">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="a6e72-525">Типы AvailabilitySets, VirtualMachines и VirtualMachineScaleSets изменены с IList<SubResource> на IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="a6e72-525">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="a6e72-526">Уточнено описание командлета Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="a6e72-526">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="a6e72-527">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a6e72-527">Az.DataFactory</span></span>
* <span data-ttu-id="a6e72-528">Добавлена поддержка операций CRUD для свойств среды выполнения потока данных в управляемой среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="a6e72-528">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a6e72-529">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a6e72-529">Az.FrontDoor</span></span>
* <span data-ttu-id="a6e72-530">Добавлены новые командлеты для создания, обновления, извлечения и удаления объекта обработчика правил Front Door.</span><span class="sxs-lookup"><span data-stu-id="a6e72-530">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="a6e72-531">Добавлены вспомогательные командлеты для создания объекта обработчика правил Front Door.</span><span class="sxs-lookup"><span data-stu-id="a6e72-531">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="a6e72-532">Добавлена ссылка обработчика правил на объект правила маршрутизации Front Door.</span><span class="sxs-lookup"><span data-stu-id="a6e72-532">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="a6e72-533">Добавлены параметры Приватного канала на серверный объект Front Door.</span><span class="sxs-lookup"><span data-stu-id="a6e72-533">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="a6e72-534">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="a6e72-534">Az.Functions</span></span>
* <span data-ttu-id="a6e72-535">Вышла общедоступная версия модуля Az.Functions.</span><span class="sxs-lookup"><span data-stu-id="a6e72-535">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a6e72-536">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a6e72-536">Az.HDInsight</span></span>
* <span data-ttu-id="a6e72-537">Добавлена поддержка шифрования управляемых клиентом ключей.</span><span class="sxs-lookup"><span data-stu-id="a6e72-537">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="a6e72-538">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="a6e72-538">Az.HealthcareApis</span></span>
* <span data-ttu-id="a6e72-539">Политики доступа для текущего субъекта теперь не используются по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a6e72-539">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a6e72-540">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a6e72-540">Az.IotHub</span></span>
* <span data-ttu-id="a6e72-541">Добавлен командлет для вызова запроса в центре Интернета вещей для получения данных с помощью SQL-подобного языка.</span><span class="sxs-lookup"><span data-stu-id="a6e72-541">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="a6e72-542">Устранена проблема, когда с помощью Add-AzIotHubDevice не удавалось создать устройство с поддержкой IoT Edge без дочерних устройств (№ 11597).</span><span class="sxs-lookup"><span data-stu-id="a6e72-542">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="a6e72-543">Добавлен командлет для создания маркера SAS для Центра Интернета вещей, устройства или модуля.</span><span class="sxs-lookup"><span data-stu-id="a6e72-543">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="a6e72-544">Добавлен командлет для вызова запроса метрик конфигурации.</span><span class="sxs-lookup"><span data-stu-id="a6e72-544">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="a6e72-545">Появилась возможность управлять автоматическим развертыванием IoT Edge в большом масштабе.</span><span class="sxs-lookup"><span data-stu-id="a6e72-545">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="a6e72-546">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="a6e72-546">New cmdlets are:</span></span>
    - <span data-ttu-id="a6e72-547">Add-AzIotHubDeployment;</span><span class="sxs-lookup"><span data-stu-id="a6e72-547">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="a6e72-548">Get-AzIotHubDeployment;</span><span class="sxs-lookup"><span data-stu-id="a6e72-548">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="a6e72-549">Remove-AzIotHubDeployment;</span><span class="sxs-lookup"><span data-stu-id="a6e72-549">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="a6e72-550">Set-AzIotHubDeployment.</span><span class="sxs-lookup"><span data-stu-id="a6e72-550">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="a6e72-551">Добавлен командлет для вызова запроса метрик развертывания IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="a6e72-551">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="a6e72-552">Добавлен командлет для применения содержимого конфигурации к указанному пограничному устройству.</span><span class="sxs-lookup"><span data-stu-id="a6e72-552">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a6e72-553">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a6e72-553">Az.KeyVault</span></span>
* <span data-ttu-id="a6e72-554">Удалены два псевдонима: New-AzKeyVaultCertificateAdministratorDetails и New-AzKeyVaultCertificateOrganizationDetails.</span><span class="sxs-lookup"><span data-stu-id="a6e72-554">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="a6e72-555">При создании хранилища ключей обратимое удаление включено по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a6e72-555">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="a6e72-556">Можно задать правила сети, чтобы при создании хранилища ключей управлять доступом из определенных сетевых расположений.</span><span class="sxs-lookup"><span data-stu-id="a6e72-556">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="a6e72-557">Добавлена возможность создания собственных ключей (BYOK).</span><span class="sxs-lookup"><span data-stu-id="a6e72-557">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="a6e72-558">С помощью Add-AzKeyVaultKey теперь можно создавать ключ обмена ключами.</span><span class="sxs-lookup"><span data-stu-id="a6e72-558">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="a6e72-559">С помощью Get-AzKeyVaultKey можно скачать открытый ключ в формате PEM.</span><span class="sxs-lookup"><span data-stu-id="a6e72-559">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="a6e72-560">Обновлен раздел KeyOps справочной документации по Add-AzKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="a6e72-560">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a6e72-561">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a6e72-561">Az.Monitor</span></span>
* <span data-ttu-id="a6e72-562">Исправлена ошибка Set-AzDiagnosticSettings, когда политика хранения не применялась ко всем категориям (№ 11589).</span><span class="sxs-lookup"><span data-stu-id="a6e72-562">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="a6e72-563">Добавлена поддержка критериев доступности веб-теста для оповещения метрики версии 2.</span><span class="sxs-lookup"><span data-stu-id="a6e72-563">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="a6e72-564">В New-AzMetricAlertRuleV2Criteria добавлена возможность создавать критерии доступности веб-теста.</span><span class="sxs-lookup"><span data-stu-id="a6e72-564">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="a6e72-565">Add-AzMetricAlertRuleV2 теперь поддерживает новые критерии доступности веб-теста.</span><span class="sxs-lookup"><span data-stu-id="a6e72-565">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="a6e72-566">В PSLogProfile исправлено избыточное определение RetentionPolicy (№ 7608).</span><span class="sxs-lookup"><span data-stu-id="a6e72-566">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="a6e72-567">В PSEventData удалены избыточные определения свойств (№ 11353).</span><span class="sxs-lookup"><span data-stu-id="a6e72-567">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="a6e72-568">Командлет Get-AzLog переименован в Get-AzActivityLog.</span><span class="sxs-lookup"><span data-stu-id="a6e72-568">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e72-569">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e72-569">Az.Network</span></span>
* <span data-ttu-id="a6e72-570">Добавлен атрибут критического изменения, сообщающий о том, что поведение зоны по умолчанию будет изменено.</span><span class="sxs-lookup"><span data-stu-id="a6e72-570">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="a6e72-571">New-AzPublicIpAddress;</span><span class="sxs-lookup"><span data-stu-id="a6e72-571">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="a6e72-572">New-AzPublicIpPrefix;</span><span class="sxs-lookup"><span data-stu-id="a6e72-572">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="a6e72-573">New-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="a6e72-573">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="a6e72-574">Добавлена поддержка нового ресурса верхнего уровня SecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="a6e72-574">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="a6e72-575">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="a6e72-575">New cmdlets added:</span></span>
        - <span data-ttu-id="a6e72-576">New-AzSecurityPartnerProvider;</span><span class="sxs-lookup"><span data-stu-id="a6e72-576">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="a6e72-577">Remove-AzSecurityPartnerProvider;</span><span class="sxs-lookup"><span data-stu-id="a6e72-577">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="a6e72-578">Get-AzSecurityPartnerProvider;</span><span class="sxs-lookup"><span data-stu-id="a6e72-578">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="a6e72-579">Set-AzSecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="a6e72-579">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="a6e72-580">В PSPrivateLinkResource добавлен параметр RequiredZoneNames, а в PSPrivateEndpointConnection — GroupId.</span><span class="sxs-lookup"><span data-stu-id="a6e72-580">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="a6e72-581">Исправлен неправильный тип параметра SuccessThresholdRoundTripTimeMs для New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.</span><span class="sxs-lookup"><span data-stu-id="a6e72-581">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="a6e72-582">В командлетах VirtualWan аргументу AllowVnetToVnetTraffic теперь по умолчанию присвоено значение True.</span><span class="sxs-lookup"><span data-stu-id="a6e72-582">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="a6e72-583">New-AzVirtualWan;</span><span class="sxs-lookup"><span data-stu-id="a6e72-583">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="a6e72-584">Update-AzVirtualWan.</span><span class="sxs-lookup"><span data-stu-id="a6e72-584">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="a6e72-585">Добавлены новые командлеты для поддержки группы зон DNS для частной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="a6e72-585">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="a6e72-586">New-AzPrivateDnsZoneConfig;</span><span class="sxs-lookup"><span data-stu-id="a6e72-586">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="a6e72-587">Get-AzPrivateDnsZoneGroup;</span><span class="sxs-lookup"><span data-stu-id="a6e72-587">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="a6e72-588">New-AzPrivateDnsZoneGroup;</span><span class="sxs-lookup"><span data-stu-id="a6e72-588">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="a6e72-589">Set-AzPrivateDnsZoneGroup;</span><span class="sxs-lookup"><span data-stu-id="a6e72-589">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="a6e72-590">Remove-AzPrivateDnsZoneGroup.</span><span class="sxs-lookup"><span data-stu-id="a6e72-590">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="a6e72-591">В AzureFirewall добавлены параметры DNSEnableProxy, DNSRequireProxyForNetworkRules и DNSServers.</span><span class="sxs-lookup"><span data-stu-id="a6e72-591">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="a6e72-592">В AzureFirewall добавлены параметры EnableDnsProxy, DnsProxyNotRequiredForNetworkRule и DnsServer.</span><span class="sxs-lookup"><span data-stu-id="a6e72-592">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="a6e72-593">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="a6e72-593">Updated cmdlet:</span></span>
        - <span data-ttu-id="a6e72-594">New-AzFirewall.</span><span class="sxs-lookup"><span data-stu-id="a6e72-594">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a6e72-595">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a6e72-595">Az.OperationalInsights</span></span>
* <span data-ttu-id="a6e72-596">Обновлен устаревший код для использования новых пакетов SDK.</span><span class="sxs-lookup"><span data-stu-id="a6e72-596">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="a6e72-597">Из-за устаревших API-интерфейсов удалены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="a6e72-597">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="a6e72-598">Get-AzOperationalInsightsSavedSearchResult (псевдоним Get-AzOperationalInsightsSavedSearchResults);</span><span class="sxs-lookup"><span data-stu-id="a6e72-598">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="a6e72-599">Get-AzOperationalInsightsSearchResult (псевдоним Get-AzOperationalInsightsSearchResults);</span><span class="sxs-lookup"><span data-stu-id="a6e72-599">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="a6e72-600">Get-AzOperationalInsightsLinkTarget (псевдоним Get-AzOperationalInsightsLinkTargets).</span><span class="sxs-lookup"><span data-stu-id="a6e72-600">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="a6e72-601">В Set-AzOperationalInsightsWorkspace и New-AzOperationalInsightsWorkspace добавлены новые параметры.</span><span class="sxs-lookup"><span data-stu-id="a6e72-601">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="a6e72-602">Созданы командлеты для связанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="a6e72-602">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="a6e72-603">Созданы командлеты для кластеров и связанной службы.</span><span class="sxs-lookup"><span data-stu-id="a6e72-603">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a6e72-604">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-604">Az.RecoveryServices</span></span>
* <span data-ttu-id="a6e72-605">В Azure Site Recovery добавлена поддержка защиты поставщика Azure для групп размещения виртуальных машин Azure близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="a6e72-605">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="a6e72-606">В Azure Site Recovery добавлена поддержка репликации из зоны в зону.</span><span class="sxs-lookup"><span data-stu-id="a6e72-606">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="a6e72-607">В Azure Backup добавлена поддержка долгосрочного хранения для точек восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-607">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="a6e72-608">В выходные данные командлета Get-AzRecoveryServicesBackupItem добавлены свойства исключения диска, добавленного в Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="a6e72-608">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="a6e72-609">Добавлена частная конечная точка для файла учетных данных хранилища для службы Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="a6e72-609">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e72-610">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e72-610">Az.Resources</span></span>
* <span data-ttu-id="a6e72-611">Добавлено предупреждение о задержке представления при создании определения роли.</span><span class="sxs-lookup"><span data-stu-id="a6e72-611">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="a6e72-612">Командлеты политики теперь выводят строго типизированные объекты.</span><span class="sxs-lookup"><span data-stu-id="a6e72-612">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="a6e72-613">Из командлета Get-AzResourceLock удален параметр -TenantLevel (№ 11335).</span><span class="sxs-lookup"><span data-stu-id="a6e72-613">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="a6e72-614">Исправлена ошибка с Remove-AzResourceGroup -Id ResourceId (№ 9882).</span><span class="sxs-lookup"><span data-stu-id="a6e72-614">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="a6e72-615">Добавлен новый командлет для получения результатов анализа гипотетических вариантов из шаблона ARM в области группы ресурсов: Get-AzDeploymentResourceGroupWhatIfResult.</span><span class="sxs-lookup"><span data-stu-id="a6e72-615">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="a6e72-616">Добавлен новый командлет для получения результатов анализа гипотетических вариантов из шаблона ARM в области подписки: Get-AzDeploymentWhatIfResult.</span><span class="sxs-lookup"><span data-stu-id="a6e72-616">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="a6e72-617">Alias: Get-AzSubscriptionDeploymentWhatIf.</span><span class="sxs-lookup"><span data-stu-id="a6e72-617">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="a6e72-618">Переопределены параметры -WhatIf и -Confirm для New-AzDeployment и New-AzResourceGroupDeployment для использования результатов анализа гипотетических вариантов из шаблона ARM.</span><span class="sxs-lookup"><span data-stu-id="a6e72-618">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="a6e72-619">В командлеты развертывания добавлено сообщение об устаревании для параметра ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="a6e72-619">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="a6e72-620">Добавлена возможность отображения улучшенных сообщений об ошибках при развертывании.</span><span class="sxs-lookup"><span data-stu-id="a6e72-620">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="a6e72-621">Добавлена возможность регистрации correlationId для сбоев развертывания.</span><span class="sxs-lookup"><span data-stu-id="a6e72-621">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="a6e72-622">В выходные данные скрипта развертывания добавлено свойство error.</span><span class="sxs-lookup"><span data-stu-id="a6e72-622">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="a6e72-623">Пакет NuGet Microsoft.Azure.Management.ResourceManager обновлен до версии 3.7.1-preview.</span><span class="sxs-lookup"><span data-stu-id="a6e72-623">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="a6e72-624">Удаленные определенные тестовые случаи как свойство error в DeploymentValidateResult были изменены на доступные только для чтения из пакета NuGet версии 3.7.1-preview.</span><span class="sxs-lookup"><span data-stu-id="a6e72-624">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="a6e72-625">Добавлен GenericResourceExpanded из пакета SDK ResourceManager версии 3.7.1-preview.</span><span class="sxs-lookup"><span data-stu-id="a6e72-625">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="a6e72-626">Добавлена поддержка тегов для всех командлетов Get для развертывания, а также для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="a6e72-626">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="a6e72-627">New-AzDeployment;</span><span class="sxs-lookup"><span data-stu-id="a6e72-627">'New-AzDeployment'</span></span>
    - <span data-ttu-id="a6e72-628">New-AzManagementGroupDeployment;</span><span class="sxs-lookup"><span data-stu-id="a6e72-628">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="a6e72-629">New-AzResourceGroupDeployment;</span><span class="sxs-lookup"><span data-stu-id="a6e72-629">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="a6e72-630">New-AzTenantDeployment.</span><span class="sxs-lookup"><span data-stu-id="a6e72-630">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a6e72-631">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a6e72-631">Az.ServiceFabric</span></span>
* <span data-ttu-id="a6e72-632">Исправлена ошибка при добавлении сертификата с помощью параметра -SecretIdentifier, когда возвращался неправильный отпечаток сертификата.</span><span class="sxs-lookup"><span data-stu-id="a6e72-632">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e72-633">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e72-633">Az.Sql</span></span>
* <span data-ttu-id="a6e72-634">Оптимизирована работа следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="a6e72-634">Enhance performance of:</span></span>
    - <span data-ttu-id="a6e72-635">Set-AzSqlDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="a6e72-635">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="a6e72-636">Set-AzSqlInstanceDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="a6e72-636">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="a6e72-637">Remove-AzSqlDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="a6e72-637">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="a6e72-638">Remove-AzSqlInstanceDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="a6e72-638">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="a6e72-639">Enable-AzSqlDatabaseSensitivityRecommendation;</span><span class="sxs-lookup"><span data-stu-id="a6e72-639">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="a6e72-640">Enable-AzSqlInstanceDatabaseSensitivityRecommendation;</span><span class="sxs-lookup"><span data-stu-id="a6e72-640">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="a6e72-641">Disable-AzSqlDatabaseSensitivityRecommendation;</span><span class="sxs-lookup"><span data-stu-id="a6e72-641">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="a6e72-642">Disable-AzSqlInstanceDatabaseSensitivityRecommendation.</span><span class="sxs-lookup"><span data-stu-id="a6e72-642">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="a6e72-643">Удалена проверка на стороне клиента параметра RetentionDays из командлета Set-AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="a6e72-643">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="a6e72-644">Добавлен аудит учетной записи хранения в виртуальной сети. Исправлена ошибка при создании роли участника данных BLOB-объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="a6e72-644">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a6e72-645">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6e72-645">Az.Storage</span></span>
* <span data-ttu-id="a6e72-646">В командлет Get-AzStorageAccount добавлен параметр -AsJob.</span><span class="sxs-lookup"><span data-stu-id="a6e72-646">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="a6e72-647">Параметр KeyVersion теперь является необязательным при изменении учетной записи хранения с помощью KeyvaultEncryption, что обеспечивает поддержку автоматической смены ключа.</span><span class="sxs-lookup"><span data-stu-id="a6e72-647">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="a6e72-648">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a6e72-648">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="a6e72-649">Исправлена ошибка при удалении каталога файлов Azure с конвейером.</span><span class="sxs-lookup"><span data-stu-id="a6e72-649">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="a6e72-650">Remove-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="a6e72-650">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="a6e72-651">Исправлена ошибка 9880. Значение DefaultAction для NetWorkRule приведено в соответствие со Swagger.</span><span class="sxs-lookup"><span data-stu-id="a6e72-651">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="a6e72-652">Update-AzStorageAccountNetworkRuleSet;</span><span class="sxs-lookup"><span data-stu-id="a6e72-652">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="a6e72-653">Get-AzStorageAccountNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="a6e72-653">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="a6e72-654">Исправлена ошибка 11624. При добавлении NetworkRules дублирующиеся правила пропускаются, чтобы не происходил сбой сервера.</span><span class="sxs-lookup"><span data-stu-id="a6e72-654">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="a6e72-655">Add-AzStorageAccountNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="a6e72-655">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="a6e72-656">Версия пакета SDK Microsoft.Azure.Cosmos.Table обновлена до 1.0.7.</span><span class="sxs-lookup"><span data-stu-id="a6e72-656">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="a6e72-657">Добавлено предупреждающее сообщение, напоминающее пользователю о необходимости повторного вывода списка с помощью ContinuationToken, когда в списке элементов Data Lake 2-го поколения возвращается только часть элементов.</span><span class="sxs-lookup"><span data-stu-id="a6e72-657">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="a6e72-658">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="a6e72-658">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="a6e72-659">Добавлена возможность создания или изменения учетной записи хранения с использованием проверки подлинности Active Directory для Файлов Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-659">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="a6e72-660">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a6e72-660">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="a6e72-661">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a6e72-661">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="a6e72-662">Добавлена возможность создания и просмотра ключей Kerberos учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="a6e72-662">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="a6e72-663">New-AzStorageAccountKey;</span><span class="sxs-lookup"><span data-stu-id="a6e72-663">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="a6e72-664">Get-AzStorageAccountKey.</span><span class="sxs-lookup"><span data-stu-id="a6e72-664">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="a6e72-665">Добавлена возможность отработки отказа для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="a6e72-665">Supported failover Storage account</span></span>
    - <span data-ttu-id="a6e72-666">Invoke-AzStorageAccountFailover.</span><span class="sxs-lookup"><span data-stu-id="a6e72-666">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="a6e72-667">Обновлена справка по Get-AzStorageBlobCopyState.</span><span class="sxs-lookup"><span data-stu-id="a6e72-667">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="a6e72-668">Обновлена справка по Get-AzStorageFileCopyState и Start-AzStorageBlobCopy.</span><span class="sxs-lookup"><span data-stu-id="a6e72-668">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="a6e72-669">Появилась интегрированная клиентская библиотека хранилища версии 12 для командлетов очередей и файлов.</span><span class="sxs-lookup"><span data-stu-id="a6e72-669">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="a6e72-670">Тип выходных данных изменен с CloudFile на AzureStorageFile. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a6e72-670">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="a6e72-671">Get-AzStorageFile;</span><span class="sxs-lookup"><span data-stu-id="a6e72-671">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="a6e72-672">Remove-AzStorageFile;</span><span class="sxs-lookup"><span data-stu-id="a6e72-672">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="a6e72-673">Get-AzStorageFileContent;</span><span class="sxs-lookup"><span data-stu-id="a6e72-673">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="a6e72-674">Set-AzStorageFileContent;</span><span class="sxs-lookup"><span data-stu-id="a6e72-674">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="a6e72-675">Start-AzStorageFileCopy.</span><span class="sxs-lookup"><span data-stu-id="a6e72-675">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="a6e72-676">Тип выходных данных изменен с CloudFileDirectory на AzureStorageFileDirectory. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a6e72-676">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="a6e72-677">New-AzStorageDirectory;</span><span class="sxs-lookup"><span data-stu-id="a6e72-677">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="a6e72-678">Remove-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="a6e72-678">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="a6e72-679">Тип выходных данных изменен с CloudFileShare на AzureStorageFileShare. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a6e72-679">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="a6e72-680">Get-AzStorageShare;</span><span class="sxs-lookup"><span data-stu-id="a6e72-680">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="a6e72-681">New-AzStorageShare;</span><span class="sxs-lookup"><span data-stu-id="a6e72-681">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="a6e72-682">Remove-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="a6e72-682">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="a6e72-683">Тип выходных данных изменен с FileShareProperties на AzureStorageFileShare. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a6e72-683">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="a6e72-684">Set-AzStorageShareQuota.</span><span class="sxs-lookup"><span data-stu-id="a6e72-684">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="a6e72-685">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a6e72-685">Az.TrafficManager</span></span>
* <span data-ttu-id="a6e72-686">Исправлено неправильное имя профиля в подробных выходных данных DisableAzureTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="a6e72-686">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a6e72-687">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6e72-687">Az.Websites</span></span>
* <span data-ttu-id="a6e72-688">Исправлена опечатка в справке по Update-AzWebAppAccessRestrictionConfig.</span><span class="sxs-lookup"><span data-stu-id="a6e72-688">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="a6e72-689">3.8.0 — апрель 2020 г.</span><span class="sxs-lookup"><span data-stu-id="a6e72-689">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="a6e72-690">Основные сведения о новых возможностях с момента последнего выпуска</span><span class="sxs-lookup"><span data-stu-id="a6e72-690">Highlights since the last release</span></span>
* <span data-ttu-id="a6e72-691">Версии PowerShell, которые поддерживает Az.Storage: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="a6e72-691">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a6e72-692">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e72-692">Az.Accounts</span></span>
* <span data-ttu-id="a6e72-693">Обновлен URL-адрес опроса Azure PowerShell в Resolve-AzError [11507].</span><span class="sxs-lookup"><span data-stu-id="a6e72-693">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a6e72-694">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a6e72-694">Az.ApiManagement</span></span>
* <span data-ttu-id="a6e72-695">Добавлено уведомление о критическом изменении для изменения выходных данных командлетов, выполняющих действия с файлами в Azure, в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="a6e72-695">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="a6e72-696">Обновлена документация для Set-AzApiManagementGroup с указанием параметра GroupId.</span><span class="sxs-lookup"><span data-stu-id="a6e72-696">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a6e72-697">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a6e72-697">Az.Cdn</span></span>
* <span data-ttu-id="a6e72-698">Исправлено отображение ценовой категории (SKU), связанной с ChinaCDN.</span><span class="sxs-lookup"><span data-stu-id="a6e72-698">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a6e72-699">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-699">Az.CognitiveServices</span></span>
* <span data-ttu-id="a6e72-700">Включена поддержка Identity, Encryption, UserOwnedStorage.</span><span class="sxs-lookup"><span data-stu-id="a6e72-700">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e72-701">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e72-701">Az.Compute</span></span>
* <span data-ttu-id="a6e72-702">Добавлен командлет Set-AzVmssOrchestrationServiceState.</span><span class="sxs-lookup"><span data-stu-id="a6e72-702">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="a6e72-703">Get-AzVmss с параметром -InstanceView отображает состояния OrchestrationService.</span><span class="sxs-lookup"><span data-stu-id="a6e72-703">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a6e72-704">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a6e72-704">Az.IotHub</span></span>
* <span data-ttu-id="a6e72-705">Реализовано управление конфигурацией двойника устройства Интернета вещей. Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="a6e72-705">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="a6e72-706">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="a6e72-706">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="a6e72-707">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="a6e72-707">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="a6e72-708">Добавлен командлет для вызова прямого метода на устройстве в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="a6e72-708">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="a6e72-709">Реализовано управление конфигурацией двойника модуля устройства Интернета вещей. Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="a6e72-709">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="a6e72-710">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="a6e72-710">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="a6e72-711">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="a6e72-711">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="a6e72-712">Реализовано управление конфигурацией автоматического управления устройствами в центре Интернета вещей в большом масштабе.</span><span class="sxs-lookup"><span data-stu-id="a6e72-712">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="a6e72-713">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="a6e72-713">New cmdlets are:</span></span>
    - <span data-ttu-id="a6e72-714">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6e72-714">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="a6e72-715">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6e72-715">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="a6e72-716">Remove-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6e72-716">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="a6e72-717">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6e72-717">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="a6e72-718">Добавлен командлет для вызова метода периферийного модуля в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="a6e72-718">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a6e72-719">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a6e72-719">Az.KeyVault</span></span>
* <span data-ttu-id="a6e72-720">Добавлен новый командлет Update-AzKeyVault, который может включать защиту от обратимого удаления и очистки в хранилище.</span><span class="sxs-lookup"><span data-stu-id="a6e72-720">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="a6e72-721">Включена поддержка Microsoft.PowerShell.SecretManagement [11178].</span><span class="sxs-lookup"><span data-stu-id="a6e72-721">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="a6e72-722">Исправлена ошибка в примерах Remove-AzKeyVaultManagedStorageSasDefinition [11479].</span><span class="sxs-lookup"><span data-stu-id="a6e72-722">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="a6e72-723">Включена поддержка частной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="a6e72-723">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="a6e72-724">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="a6e72-724">Az.Maintenance</span></span>
* <span data-ttu-id="a6e72-725">Опубликована версия выпуска командлетов обслуживания для общедоступной версии.</span><span class="sxs-lookup"><span data-stu-id="a6e72-725">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a6e72-726">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a6e72-726">Az.Monitor</span></span>
* <span data-ttu-id="a6e72-727">Добавлены командлеты для области приватных каналов:</span><span class="sxs-lookup"><span data-stu-id="a6e72-727">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="a6e72-728">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="a6e72-728">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="a6e72-729">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="a6e72-729">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="a6e72-730">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="a6e72-730">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="a6e72-731">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="a6e72-731">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="a6e72-732">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="a6e72-732">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="a6e72-733">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="a6e72-733">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="a6e72-734">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="a6e72-734">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e72-735">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e72-735">Az.Network</span></span>
* <span data-ttu-id="a6e72-736">Обновлены командлеты для включения подключения на частном IP-адресе для шлюза виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="a6e72-736">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="a6e72-737">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a6e72-737">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="a6e72-738">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a6e72-738">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="a6e72-739">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a6e72-739">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="a6e72-740">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a6e72-740">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="a6e72-741">Обновлены командлеты для включения шлюзов LocalNetworkGateways и сайтов VpnSites на основе FQDN:</span><span class="sxs-lookup"><span data-stu-id="a6e72-741">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="a6e72-742">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a6e72-742">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="a6e72-743">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="a6e72-743">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="a6e72-744">Включена поддержка семейства адресов IPv6 в ExpressRouteCircuitConnectionConfig (Global Reach).</span><span class="sxs-lookup"><span data-stu-id="a6e72-744">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="a6e72-745">Добавлен командлет Set-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="a6e72-745">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="a6e72-746">Позволяет выполнять настройку всех существующих свойств, включая IPv6CircuitConnectionProperties.</span><span class="sxs-lookup"><span data-stu-id="a6e72-746">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="a6e72-747">Обновлен командлет Add-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="a6e72-747">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="a6e72-748">Добавлен еще один необязательный параметр AddressPrefixType для указания семейства адресов префикса адреса.</span><span class="sxs-lookup"><span data-stu-id="a6e72-748">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="a6e72-749">Обновлены командлеты для включения параметра времени ожидания для обнаружения неиспользуемых одноранговых узлов (DPD) в подключениях шлюзов виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="a6e72-749">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="a6e72-750">New-AzVirtualNetworkGatewayConnection;</span><span class="sxs-lookup"><span data-stu-id="a6e72-750">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="a6e72-751">Set-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="a6e72-751">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a6e72-752">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a6e72-752">Az.PolicyInsights</span></span>
* <span data-ttu-id="a6e72-753">Добавлен командлет Start-AzPolicyComplianceScan для запуска проверок соответствия политикам.</span><span class="sxs-lookup"><span data-stu-id="a6e72-753">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="a6e72-754">Добавлены версии определения политики, определения набора и назначения в выходные данные командлета Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="a6e72-754">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a6e72-755">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a6e72-755">Az.ServiceFabric</span></span>
* <span data-ttu-id="a6e72-756">Улучшено форматирование и наглядность кода в примерах New-AzServiceFabricCluster.</span><span class="sxs-lookup"><span data-stu-id="a6e72-756">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e72-757">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e72-757">Az.Sql</span></span>
* <span data-ttu-id="a6e72-758">Добавлены командлеты Get-AzSqlInstanceOperation и Stop-AzSqlInstanceOperation.</span><span class="sxs-lookup"><span data-stu-id="a6e72-758">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="a6e72-759">Включен аудит учетной записи хранения в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="a6e72-759">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a6e72-760">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6e72-760">Az.Storage</span></span>
* <span data-ttu-id="a6e72-761">Добавлено уведомление о критическом изменении для изменения выходных данных командлетов, выполняющих действия с файлами в Azure, в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="a6e72-761">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="a6e72-762">Включена поддержка новых имен SKU StandardGZRS, StandardRAGZRS при создании или обновлении учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="a6e72-762">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="a6e72-763">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a6e72-763">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="a6e72-764">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a6e72-764">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="a6e72-765">Добавлена поддержка DataLake 2-го поколения.</span><span class="sxs-lookup"><span data-stu-id="a6e72-765">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="a6e72-766">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="a6e72-766">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="a6e72-767">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="a6e72-767">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="a6e72-768">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="a6e72-768">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="a6e72-769">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="a6e72-769">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="a6e72-770">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="a6e72-770">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="a6e72-771">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="a6e72-771">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="a6e72-772">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="a6e72-772">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="a6e72-773">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="a6e72-773">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="a6e72-774">0.10.0-preview — апрель 2020 г.</span><span class="sxs-lookup"><span data-stu-id="a6e72-774">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="a6e72-775">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="a6e72-775">General</span></span>
* <span data-ttu-id="a6e72-776">Модуль Az стали доступными в предварительной версии в Azure Stack Hub.</span><span class="sxs-lookup"><span data-stu-id="a6e72-776">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="a6e72-777">Это обеспечивает кросс-платформенную совместимость с Linux и macOs.</span><span class="sxs-lookup"><span data-stu-id="a6e72-777">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="a6e72-778">Azure Stack Hub теперь поддерживает PowerShell Core с модулями Az (см. [дополнительные сведения](https://aka.ms/az4AzureStack))</span><span class="sxs-lookup"><span data-stu-id="a6e72-778">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="a6e72-779">Модули Az поддерживают профиль 2019-03-01-hybrid:</span><span class="sxs-lookup"><span data-stu-id="a6e72-779">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="a6e72-780">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="a6e72-780">Az.Billing</span></span>
  - <span data-ttu-id="a6e72-781">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e72-781">Az.Compute</span></span>
  - <span data-ttu-id="a6e72-782">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="a6e72-782">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="a6e72-783">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a6e72-783">Az.EventHub</span></span>
  - <span data-ttu-id="a6e72-784">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a6e72-784">Az.IotHub</span></span>
  - <span data-ttu-id="a6e72-785">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a6e72-785">Az.KeyVault</span></span>
  - <span data-ttu-id="a6e72-786">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a6e72-786">Az.Monitor</span></span>
  - <span data-ttu-id="a6e72-787">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e72-787">Az.Network</span></span>
  - <span data-ttu-id="a6e72-788">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e72-788">Az.Resources</span></span>
  - <span data-ttu-id="a6e72-789">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6e72-789">Az.Storage</span></span>
  - <span data-ttu-id="a6e72-790">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6e72-790">Az.Websites</span></span>
* <span data-ttu-id="a6e72-791">В PowerShell появились три новых модуля Az, которые работают с Azure Stack Hub: Az.Databox, Az.IotHub и Az.EventHub.</span><span class="sxs-lookup"><span data-stu-id="a6e72-791">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="a6e72-792">Команды остаются прежними же за исключением незначительных изменений, таких как изменение AzureRM на Az.</span><span class="sxs-lookup"><span data-stu-id="a6e72-792">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="a6e72-793">См. обновленную ссылку на документацию по [PowerShell для Azure Stack Hub](https://aka.ms/InstallASHPowerShell)</span><span class="sxs-lookup"><span data-stu-id="a6e72-793">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="a6e72-794">3.7.0 — март 2020 г.</span><span class="sxs-lookup"><span data-stu-id="a6e72-794">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a6e72-795">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e72-795">Az.Accounts</span></span>
* <span data-ttu-id="a6e72-796">Исправлено исключение NullReferenceException командлетов Get-AzTenant/Get-AzDefault/Set-AzDefault, если вход не выполнен [10292]</span><span class="sxs-lookup"><span data-stu-id="a6e72-796">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e72-797">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e72-797">Az.Compute</span></span>
* <span data-ttu-id="a6e72-798">Добавлены следующие параметры к командлету New-AzDiskConfig:</span><span class="sxs-lookup"><span data-stu-id="a6e72-798">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="a6e72-799">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="a6e72-799">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="a6e72-800">Разрешено свойство Encryption для параметра Target командлета New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="a6e72-800">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="a6e72-801">Исправлена проблема с tempDisk для командлетов Set-AzVmss -Reimage и Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="a6e72-801">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="a6e72-802">[11354]</span><span class="sxs-lookup"><span data-stu-id="a6e72-802">[#11354]</span></span>
* <span data-ttu-id="a6e72-803">Добавлена поддержка нового расширения SAP для указанных ниже командлетов</span><span class="sxs-lookup"><span data-stu-id="a6e72-803">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="a6e72-804">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="a6e72-804">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="a6e72-805">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="a6e72-805">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="a6e72-806">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="a6e72-806">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="a6e72-807">Update-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="a6e72-807">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="a6e72-808">Исправлены ошибки в примерах справки</span><span class="sxs-lookup"><span data-stu-id="a6e72-808">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="a6e72-809">Показано точное строковое значение в табличном формате для свойства PowerState виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a6e72-809">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="a6e72-810">New-AzVmssConfig: исправлена сериализация свойства AutomaticRepairs, если параметр SinglePlacementGroup отключен.</span><span class="sxs-lookup"><span data-stu-id="a6e72-810">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="a6e72-811">[11257]</span><span class="sxs-lookup"><span data-stu-id="a6e72-811">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a6e72-812">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a6e72-812">Az.DataFactory</span></span>
* <span data-ttu-id="a6e72-813">Пакет SDK ADF для .NET обновлен до версии 4.8.0.</span><span class="sxs-lookup"><span data-stu-id="a6e72-813">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="a6e72-814">Добавлены необязательные параметры для команды Invoke-AzDataFactoryV2Pipeline для поддержки повторного запуска.</span><span class="sxs-lookup"><span data-stu-id="a6e72-814">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a6e72-815">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a6e72-815">Az.DataLakeStore</span></span>
* <span data-ttu-id="a6e72-816">Добавлено описание критического изменения для Export-AzDataLakeStoreItem и Import-AzDataLakeStoreItem.</span><span class="sxs-lookup"><span data-stu-id="a6e72-816">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="a6e72-817">Добавлен параметр кодирования байтов для New-AzDataLakeStoreItem, Add-AzDAtaLakeStoreItemContent и Get-AzDAtaLakeStoreItemContent.</span><span class="sxs-lookup"><span data-stu-id="a6e72-817">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a6e72-818">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a6e72-818">Az.HDInsight</span></span>
* <span data-ttu-id="a6e72-819">Добавлена поддержка указания минимальной поддерживаемой версии TLS при создании кластера.</span><span class="sxs-lookup"><span data-stu-id="a6e72-819">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a6e72-820">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a6e72-820">Az.IotHub</span></span>
* <span data-ttu-id="a6e72-821">Добавлена поддержка для управления распределенными параметрами на отдельных устройствах.</span><span class="sxs-lookup"><span data-stu-id="a6e72-821">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="a6e72-822">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="a6e72-822">New Cmdlets are:</span></span>
    - <span data-ttu-id="a6e72-823">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="a6e72-823">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="a6e72-824">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="a6e72-824">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a6e72-825">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a6e72-825">Az.KeyVault</span></span>
* <span data-ttu-id="a6e72-826">Добавлены атрибуты критических изменений для New-AzKeyVault.</span><span class="sxs-lookup"><span data-stu-id="a6e72-826">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a6e72-827">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a6e72-827">Az.Monitor</span></span>
* <span data-ttu-id="a6e72-828">Обновлена документация для New-AzScheduledQueryRuleLogMetricTrigger.</span><span class="sxs-lookup"><span data-stu-id="a6e72-828">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e72-829">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e72-829">Az.Network</span></span>
* <span data-ttu-id="a6e72-830">Обновлены командлеты для поддержки подключений VirtualHubVnetConnections между клиентами</span><span class="sxs-lookup"><span data-stu-id="a6e72-830">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="a6e72-831">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="a6e72-831">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="a6e72-832">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="a6e72-832">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="a6e72-833">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a6e72-833">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="a6e72-834">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a6e72-834">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="a6e72-835">Удалена зависимость пакета SDK для управления SQL.</span><span class="sxs-lookup"><span data-stu-id="a6e72-835">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a6e72-836">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a6e72-836">Az.PolicyInsights</span></span>
* <span data-ttu-id="a6e72-837">Улучшены сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="a6e72-837">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a6e72-838">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-838">Az.RecoveryServices</span></span>
* <span data-ttu-id="a6e72-839">В Azure Site Recovery реализована поддержка повторной защиты и обновлены свойства зашифрованных виртуальных машин диска Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-839">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="a6e72-840">Добавлена возможность мониторинг аварийного восстановления для свойств VmwareToAzure в Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="a6e72-840">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="a6e72-841">В Azure Backup реализована поддержка повторного обновления политики для элементов с ошибками.</span><span class="sxs-lookup"><span data-stu-id="a6e72-841">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="a6e72-842">В Azure Backup реализована поддержка параметров исключения диска во время резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="a6e72-842">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="a6e72-843">В Azure Backup реализована поддержка восстановления нескольких файлов или папок в AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="a6e72-843">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="a6e72-844">В Azure Backup реализована поддержка указанной пользователем группы Resourcegroup при обновлении политики IaasVM.</span><span class="sxs-lookup"><span data-stu-id="a6e72-844">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e72-845">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e72-845">Az.Resources</span></span>
* <span data-ttu-id="a6e72-846">Исправлена команда Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType для использования фактической версии apiVersion ресурсов (а не версии apiVersion по умолчанию) [11267].</span><span class="sxs-lookup"><span data-stu-id="a6e72-846">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="a6e72-847">Добавлена возможность регистрации correlationId для сценариев с ошибками.</span><span class="sxs-lookup"><span data-stu-id="a6e72-847">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="a6e72-848">Незначительно изменена документация по Get-AzResourceLock.</span><span class="sxs-lookup"><span data-stu-id="a6e72-848">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="a6e72-849">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="a6e72-849">Added example.</span></span>
* <span data-ttu-id="a6e72-850">Экранирована одинарная кавычка в значении параметра Get-AzADUser [11317].</span><span class="sxs-lookup"><span data-stu-id="a6e72-850">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="a6e72-851">Добавлены новые командлеты для сценариев развертывания (Get-AzDeploymentScript, Get-AzDeploymentScriptLog, Save-AzDeploymentScriptLog, Remove-AzDeploymentScript).</span><span class="sxs-lookup"><span data-stu-id="a6e72-851">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e72-852">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e72-852">Az.Sql</span></span>
* <span data-ttu-id="a6e72-853">Добавлен параметр вторичной реплики для чтения для командлета Invoke-AzSqlDatabaseFailover.</span><span class="sxs-lookup"><span data-stu-id="a6e72-853">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="a6e72-854">Добавлен командлет Disable-AzSqlServerActiveDirectoryOnlyAuthentication.</span><span class="sxs-lookup"><span data-stu-id="a6e72-854">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="a6e72-855">Сохранен приоритет конфиденциальности при классификации столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="a6e72-855">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="a6e72-856">Az.Support</span><span class="sxs-lookup"><span data-stu-id="a6e72-856">Az.Support</span></span>
* <span data-ttu-id="a6e72-857">Модуль Az.Support стал общедоступным.</span><span class="sxs-lookup"><span data-stu-id="a6e72-857">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a6e72-858">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6e72-858">Az.Websites</span></span>
* <span data-ttu-id="a6e72-859">Реализована поддержка работы с правилами маршрутизации трафика веб-приложения через указанные ниже командлеты</span><span class="sxs-lookup"><span data-stu-id="a6e72-859">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="a6e72-860">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="a6e72-860">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="a6e72-861">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="a6e72-861">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="a6e72-862">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="a6e72-862">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="a6e72-863">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="a6e72-863">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="a6e72-864">3.6.1 — март 2020 г.</span><span class="sxs-lookup"><span data-stu-id="a6e72-864">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a6e72-865">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e72-865">Az.Accounts</span></span>
* <span data-ttu-id="a6e72-866">Открытие страницы опроса Azure PowerShell в Send-Feedback [11020].</span><span class="sxs-lookup"><span data-stu-id="a6e72-866">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="a6e72-867">Отображение URL-адреса опроса Azure PowerShell в Resolve-Error [11021].</span><span class="sxs-lookup"><span data-stu-id="a6e72-867">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="a6e72-868">Добавлена версия Az в UserAgent.</span><span class="sxs-lookup"><span data-stu-id="a6e72-868">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a6e72-869">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a6e72-869">Az.ApiManagement</span></span>
* <span data-ttu-id="a6e72-870">Включена поддержка получения и настройки личного домена в конечной точке DeveloperPortal [11007].</span><span class="sxs-lookup"><span data-stu-id="a6e72-870">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="a6e72-871">Export-AzApiManagementApi: включена поддержка скачивания определения API в формате JSON [9987].</span><span class="sxs-lookup"><span data-stu-id="a6e72-871">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="a6e72-872">Import-AzApiManagementApi: включена поддержка импорта определения OpenApi 3.0 из документа JSON.</span><span class="sxs-lookup"><span data-stu-id="a6e72-872">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="a6e72-873">New-AzApiManagementIdentityProvider и Set-AzApiManagementIdentityProvider: включена поддержка настройки входа арендатора для поставщика AAD B2C [9784].</span><span class="sxs-lookup"><span data-stu-id="a6e72-873">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a6e72-874">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a6e72-874">Az.DataLakeStore</span></span>
* <span data-ttu-id="a6e72-875">Добавлена ссылка на System.Buffers явным образом в CSPROJ и PSD1.</span><span class="sxs-lookup"><span data-stu-id="a6e72-875">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a6e72-876">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a6e72-876">Az.IotHub</span></span>
* <span data-ttu-id="a6e72-877">Добавлена возможность управления устройствами в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="a6e72-877">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="a6e72-878">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="a6e72-878">New Cmdlets are:</span></span>
    - <span data-ttu-id="a6e72-879">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="a6e72-879">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="a6e72-880">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="a6e72-880">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="a6e72-881">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="a6e72-881">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="a6e72-882">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="a6e72-882">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="a6e72-883">Включена поддержка управления модулями в целевом устройстве Интернета вещей в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="a6e72-883">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="a6e72-884">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="a6e72-884">New Cmdlets are:</span></span>
    - <span data-ttu-id="a6e72-885">Add-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="a6e72-885">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="a6e72-886">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="a6e72-886">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="a6e72-887">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="a6e72-887">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="a6e72-888">Set-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="a6e72-888">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="a6e72-889">Добавлен командлет для получения строки подключения целевого устройства Интернета вещей в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="a6e72-889">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="a6e72-890">Добавлен командлет для получения строки подключения модуля на целевом устройстве Интернета вещей в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="a6e72-890">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="a6e72-891">Включена поддержка для получения или настройки родительского устройства для устройства Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="a6e72-891">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="a6e72-892">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="a6e72-892">New Cmdlets are:</span></span>
    - <span data-ttu-id="a6e72-893">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="a6e72-893">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="a6e72-894">Set-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="a6e72-894">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="a6e72-895">Включена поддержка управления связью "родители — потомки" устройства.</span><span class="sxs-lookup"><span data-stu-id="a6e72-895">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a6e72-896">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a6e72-896">Az.Monitor</span></span>
* <span data-ttu-id="a6e72-897">Исправлено выходное значение для Get-AzMetricDefinition [9714].</span><span class="sxs-lookup"><span data-stu-id="a6e72-897">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e72-898">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e72-898">Az.Network</span></span>
* <span data-ttu-id="a6e72-899">Обновлен пакет SDK для управления SQL.</span><span class="sxs-lookup"><span data-stu-id="a6e72-899">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="a6e72-900">Исправлена проблема с разницей в именовании в классе PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="a6e72-900">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="a6e72-901">Сопоставление ActionsRequired с ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="a6e72-901">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="a6e72-902">Добавление PublicNetworkAccess в команды New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="a6e72-902">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e72-903">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e72-903">Az.Resources</span></span>
* <span data-ttu-id="a6e72-904">Исправлена ошибка пустой ссылки в Get-AzRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="a6e72-904">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="a6e72-905">Параметры -Force и -PassThru помечены необязательными в Remove-AzADGroup [10849].</span><span class="sxs-lookup"><span data-stu-id="a6e72-905">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="a6e72-906">Исправлена ошибка, из-за которой MailNickname не возвращается в Remove-AzADGroup [11167].</span><span class="sxs-lookup"><span data-stu-id="a6e72-906">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="a6e72-907">Исправлена ошибка, из-за которой операция канала Remove-AzADGroup не работает [11171].</span><span class="sxs-lookup"><span data-stu-id="a6e72-907">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="a6e72-908">Исправлена ошибка с пустой ссылкой в GetAzureRoleAssignmentCommand.</span><span class="sxs-lookup"><span data-stu-id="a6e72-908">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="a6e72-909">Добавлено критическое изменение атрибутов для будущих изменений командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="a6e72-909">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="a6e72-910">Обновлена команда Get-AzResourceGroup для выполнения фильтрации тегов группы ресурсов на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="a6e72-910">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="a6e72-911">Расширены командлеты Tag для включения поддержки параметра -ResourceId.</span><span class="sxs-lookup"><span data-stu-id="a6e72-911">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="a6e72-912">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6e72-912">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="a6e72-913">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6e72-913">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="a6e72-914">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6e72-914">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="a6e72-915">Добавлен новый командлет Tag.</span><span class="sxs-lookup"><span data-stu-id="a6e72-915">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="a6e72-916">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6e72-916">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="a6e72-917">Предоставляется ScopedDeployment из пакета SDK 3.3.0.</span><span class="sxs-lookup"><span data-stu-id="a6e72-917">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e72-918">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e72-918">Az.Sql</span></span>
* <span data-ttu-id="a6e72-919">Добавление PublicNetworkAccess в команды New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="a6e72-919">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="a6e72-920">Включена поддержка конфигурации резервного копирования долгосрочного хранения для управляемых баз данных.</span><span class="sxs-lookup"><span data-stu-id="a6e72-920">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="a6e72-921">Получение или настройка политики LTR в управляемой базе данных.</span><span class="sxs-lookup"><span data-stu-id="a6e72-921">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="a6e72-922">Получение резервных копий LTR по управляемой базе данных, управляемому экземпляру или расположению.</span><span class="sxs-lookup"><span data-stu-id="a6e72-922">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="a6e72-923">Удаление резервной копии LTR.</span><span class="sxs-lookup"><span data-stu-id="a6e72-923">Remove an LTR backup</span></span>
    - <span data-ttu-id="a6e72-924">Восстановление резервной копии LTR для создания новой управляемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="a6e72-924">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="a6e72-925">Добавление MinimalTlsVersion в New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="a6e72-925">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="a6e72-926">Добавление MinimalTlsVersion в New-AzSqlInstance и Set-AzSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="a6e72-926">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="a6e72-927">Обновлена версия пакета SDK для SQL для Az.Network.</span><span class="sxs-lookup"><span data-stu-id="a6e72-927">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a6e72-928">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6e72-928">Az.Storage</span></span>
* <span data-ttu-id="a6e72-929">Включена поддержка AllowProtectedAppendWrite в ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="a6e72-929">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="a6e72-930">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a6e72-930">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="a6e72-931">Добавлено предупреждение о критическом изменении для изменения типа AzureStorageTable в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="a6e72-931">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="a6e72-932">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="a6e72-932">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="a6e72-933">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="a6e72-933">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a6e72-934">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6e72-934">Az.Websites</span></span>
* <span data-ttu-id="a6e72-935">Добавлен параметр Tag для New-AzAppServicePlan и Set-AzAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="a6e72-935">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="a6e72-936">Завершение выполнения командлета, если при добавлении личного домена на веб-сайт возникает исключение.</span><span class="sxs-lookup"><span data-stu-id="a6e72-936">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="a6e72-937">Включена поддержка выполнения операций для Служб приложений, которые находятся не в той же группе ресурсов, что и план службы приложений.</span><span class="sxs-lookup"><span data-stu-id="a6e72-937">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="a6e72-938">Применение ограничения доступа к WebApp/Function в разных группах ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a6e72-938">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="a6e72-939">Исправлена ошибка с указанием пользовательских имен узлов для WebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="a6e72-939">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="a6e72-940">3.5.0 — февраль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="a6e72-940">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a6e72-941">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="a6e72-941">Highlights since the last major release</span></span>
* <span data-ttu-id="a6e72-942">Обновлены данные телеметрии на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="a6e72-942">Updated client side telemetry.</span></span>
* <span data-ttu-id="a6e72-943">В Az.IotHub добавлены командлеты для управления устройствами.</span><span class="sxs-lookup"><span data-stu-id="a6e72-943">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="a6e72-944">В Az.SqlVirtualMachine добавлены командлеты для прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="a6e72-944">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a6e72-945">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e72-945">Az.Accounts</span></span>
* <span data-ttu-id="a6e72-946">В данные телеметрии на стороне клиента добавлены такие сведения, как идентификатор подписки, идентификатор арендатора и время выполнения.</span><span class="sxs-lookup"><span data-stu-id="a6e72-946">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a6e72-947">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a6e72-947">Az.Automation</span></span>
* <span data-ttu-id="a6e72-948">Исправлена опечатка в примере 1 в справочной документации по New-AzAutomationSoftwareUpdateConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a6e72-948">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a6e72-949">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-949">Az.CognitiveServices</span></span>
* <span data-ttu-id="a6e72-950">Обновлен пакет SDK до версии 7.0.</span><span class="sxs-lookup"><span data-stu-id="a6e72-950">Updated SDK to 7.0</span></span>
* <span data-ttu-id="a6e72-951">Улучшено сообщение об ошибке, которое появляется, если ответы сервера не содержат текст.</span><span class="sxs-lookup"><span data-stu-id="a6e72-951">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e72-952">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e72-952">Az.Compute</span></span>
* <span data-ttu-id="a6e72-953">Разрешено использовать пустое значение для ProximityPlacementGroupId во время обновления.</span><span class="sxs-lookup"><span data-stu-id="a6e72-953">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a6e72-954">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a6e72-954">Az.FrontDoor</span></span>
* <span data-ttu-id="a6e72-955">Добавлен командлет для получения определений управляемых правил, которые могут использоваться в WAF.</span><span class="sxs-lookup"><span data-stu-id="a6e72-955">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a6e72-956">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a6e72-956">Az.IotHub</span></span>
* <span data-ttu-id="a6e72-957">Добавлена возможность управления устройствами в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="a6e72-957">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="a6e72-958">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="a6e72-958">New Cmdlets are:</span></span>
    - <span data-ttu-id="a6e72-959">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="a6e72-959">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="a6e72-960">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="a6e72-960">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="a6e72-961">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="a6e72-961">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="a6e72-962">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="a6e72-962">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a6e72-963">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a6e72-963">Az.KeyVault</span></span>
* <span data-ttu-id="a6e72-964">Устранен дублирующийся текст для Add-AzKeyVaultKey.md.</span><span class="sxs-lookup"><span data-stu-id="a6e72-964">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a6e72-965">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a6e72-965">Az.Monitor</span></span>
* <span data-ttu-id="a6e72-966">Исправлено описание командлета Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="a6e72-966">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="a6e72-967">В команду New-AzMetricAlertRuleV2 добавлен новый параметр ActionGroupId.</span><span class="sxs-lookup"><span data-stu-id="a6e72-967">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="a6e72-968">Пользователь может предоставить ActionGroupId(string) или ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="a6e72-968">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e72-969">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e72-969">Az.Network</span></span>
* <span data-ttu-id="a6e72-970">Добавлен еще один параметр -EnableProxyProtocol для командлета New-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="a6e72-970">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="a6e72-971">Исправлен пример FilterData в Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="a6e72-971">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="a6e72-972">Добавлен пример Packet Capture для всех внутренних и внешних пакетов в Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="a6e72-972">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="a6e72-973">Добавлена поддерживаемая политика Брандмауэра Azure в брандмауэрах виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="a6e72-973">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="a6e72-974">Новые командлеты не добавлены.</span><span class="sxs-lookup"><span data-stu-id="a6e72-974">No new cmdlets are added.</span></span> <span data-ttu-id="a6e72-975">Снято ограничение политики брандмауэра в брандмауэрах виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="a6e72-975">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a6e72-976">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-976">Az.RecoveryServices</span></span>
* <span data-ttu-id="a6e72-977">Добавлена возможность восстановления в виде файлов для Баз данных SQL.</span><span class="sxs-lookup"><span data-stu-id="a6e72-977">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e72-978">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e72-978">Az.Resources</span></span>
* <span data-ttu-id="a6e72-979">Выполнен рефакторинг командлетов развертывания шаблона.</span><span class="sxs-lookup"><span data-stu-id="a6e72-979">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="a6e72-980">Добавлены новые командлеты для управления развертываниями в группе управления: \*-AzManagementGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="a6e72-980">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="a6e72-981">Добавлены новые командлеты для управления развертываниями в области арендатора: \*-AzTenantDeployment.</span><span class="sxs-lookup"><span data-stu-id="a6e72-981">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="a6e72-982">Выполнен рефакторинг командлетов \*-AzDeployment для работы в области подписки.</span><span class="sxs-lookup"><span data-stu-id="a6e72-982">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="a6e72-983">Созданы псевдонимы \*-AzSubscriptionDeployment для командлетов \*-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="a6e72-983">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="a6e72-984">Исправлен командлет Update-AzADApplication, когда параметр AvailableToOtherTenants не задан.</span><span class="sxs-lookup"><span data-stu-id="a6e72-984">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="a6e72-985">Удален набор параметров ApplicationObjectWithoutCredentialParameterSet, чтобы предотвратить возникновение AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="a6e72-985">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="a6e72-986">Повторно созданы файлы справки.</span><span class="sxs-lookup"><span data-stu-id="a6e72-986">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e72-987">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e72-987">Az.Sql</span></span>
* <span data-ttu-id="a6e72-988">Добавлена возможность восстановления точки во времени между подписками в Управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="a6e72-988">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="a6e72-989">Добавлена возможность изменения существующего поколения оборудования Управляемого экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="a6e72-989">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="a6e72-990">Исправлены примеры справки Update-AzSqlServerVulnerabilityAssessmentSetting: выходные данные параметра и свойства — EmailAdmins.</span><span class="sxs-lookup"><span data-stu-id="a6e72-990">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="a6e72-991">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a6e72-991">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="a6e72-992">Добавлены командлеты для прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="a6e72-992">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="a6e72-993">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="a6e72-993">Az.StorageSync</span></span>
* <span data-ttu-id="a6e72-994">В командлете Invoke-AzStorageSyncCompatibilityCheck обновлены поддерживаемые наборы символов.</span><span class="sxs-lookup"><span data-stu-id="a6e72-994">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="a6e72-995">3.4.0 — февраль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="a6e72-995">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a6e72-996">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="a6e72-996">Highlights since the last major release</span></span>
* <span data-ttu-id="a6e72-997">Выпущена первоначальная версия 0.1.0 Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="a6e72-997">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="a6e72-998">Добавлена поддержка Az.Network ConnectionMonitor V2</span><span class="sxs-lookup"><span data-stu-id="a6e72-998">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a6e72-999">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e72-999">Az.Accounts</span></span>
* <span data-ttu-id="a6e72-1000">Отключить автоматическое сохранение контекста, если AzureRmContext.json недоступен</span><span class="sxs-lookup"><span data-stu-id="a6e72-1000">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="a6e72-1001">Обновление ссылки на Azure Powershell Common до предварительной версии 1.3.5</span><span class="sxs-lookup"><span data-stu-id="a6e72-1001">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a6e72-1002">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a6e72-1002">Az.ApiManagement</span></span>
* <span data-ttu-id="a6e72-1003">**Get-AzApiManagementApiSchema** Исправлено получение схемы Open-API, связанной с API https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="a6e72-1003">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="a6e72-1004">**New-AzApiManagementProduct**\* и **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="a6e72-1004">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="a6e72-1005">Исправить документацию для https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="a6e72-1005">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="a6e72-1006">**Set-AzApiManagementApi** Добавлен пример, показывающий, как обновить ServiceUrl с помощью командлета</span><span class="sxs-lookup"><span data-stu-id="a6e72-1006">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e72-1007">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e72-1007">Az.Compute</span></span>
* <span data-ttu-id="a6e72-1008">Ограничение числа состояний виртуальных машин до 100, чтобы избежать регулирования при выполнении Get-AzVM-Status без имени виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1008">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="a6e72-1009">Добавление обновления командлета -AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="a6e72-1009">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="a6e72-1010">Добавление параметров EncryptionType и DiskEncryptionSetId в следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1010">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="a6e72-1011">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="a6e72-1011">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="a6e72-1012">Добавление параметра ColocationStatus в командлет Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1012">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a6e72-1013">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a6e72-1013">Az.DataFactory</span></span>
* <span data-ttu-id="a6e72-1014">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.7.0.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1014">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="a6e72-1015">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="a6e72-1015">Az.DeploymentManager</span></span>
* <span data-ttu-id="a6e72-1016">Добавляет операции LIST для ресурсов</span><span class="sxs-lookup"><span data-stu-id="a6e72-1016">Adds LIST operations for resources</span></span>
* <span data-ttu-id="a6e72-1017">Добавляет возможность выполнения операций на этапах Проверки работоспособности</span><span class="sxs-lookup"><span data-stu-id="a6e72-1017">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a6e72-1018">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a6e72-1018">Az.HDInsight</span></span>
* <span data-ttu-id="a6e72-1019">Исправление ошибки в документе New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1019">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a6e72-1020">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a6e72-1020">Az.KeyVault</span></span>
* <span data-ttu-id="a6e72-1021">Добавление Псевдонимов имени в атрибут VaultName, чтобы Remove-AzureKeyVault соответствовал New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1021">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e72-1022">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e72-1022">Az.Network</span></span>
* <span data-ttu-id="a6e72-1023">В Set-AzNetworkWatcherConfigFlowLog.md добавлен новый пример для демонстрации сценария отключения Аналитики трафика.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1023">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="a6e72-1024">Добавление поддержки назначения IP-конфигурации для брандмауэра Azure — выделенная подсеть и общедоступный IP-адрес, которые брандмауэр будет использовать для управления трафиком</span><span class="sxs-lookup"><span data-stu-id="a6e72-1024">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="a6e72-1025">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1025">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="a6e72-1026">добавлен параметр — ManagementPublicIpAddress (необязательный), который принимает объект общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="a6e72-1026">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="a6e72-1027">Добавлен метод SetManagementIpConfiguration для объекта брандмауэра — в качестве входных данных требуется подсеть и общедоступный IP-адрес — имя подсети должно быть "AzureFirewallManagementSubnet"</span><span class="sxs-lookup"><span data-stu-id="a6e72-1027">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="a6e72-1028">Исправлены примеры Get-AzNetworkSecurityGroup для отображения примеров для группы безопасности сети (NSG) вместо сетевых интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1028">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="a6e72-1029">Исправлена опечатка в команде New-AzVpnSite, которая препятствовала завершению параметра идентификатором ресурса.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1029">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="a6e72-1030">Добавлена поддержка конфигурации в наборе действий для правил подстановки URL-адресов в шлюзе приложения.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1030">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="a6e72-1031">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1031">New cmdlets added:</span></span>
        - <span data-ttu-id="a6e72-1032">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6e72-1032">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="a6e72-1033">В следующие командлеты добавлен необязательный параметр — UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6e72-1033">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="a6e72-1034">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="a6e72-1034">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="a6e72-1035">Добавление поддержки для ресурсов NetworkWatcher ConnectionMonitor версии 2</span><span class="sxs-lookup"><span data-stu-id="a6e72-1035">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a6e72-1036">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a6e72-1036">Az.PolicyInsights</span></span>
* <span data-ttu-id="a6e72-1037">Поддержка оценки соответствия до определения того, какой ресурс нужно исправить</span><span class="sxs-lookup"><span data-stu-id="a6e72-1037">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="a6e72-1038">Добавление параметра "—ResourceDiscoverMode" в Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="a6e72-1038">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="a6e72-1039">Добавление командлета Get-AzPolicyMetadata для получения ресурсов метаданных политики</span><span class="sxs-lookup"><span data-stu-id="a6e72-1039">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="a6e72-1040">Get-AzPolicyState и Get-AzPolicyStateSummary обновлены для API версии 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="a6e72-1040">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a6e72-1041">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-1041">Az.RecoveryServices</span></span>
* <span data-ttu-id="a6e72-1042">Поддержка Azure Site Recovery для удаления реплицированного диска.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1042">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="a6e72-1043">В Azure Backup добавлена ​​поддержка добавления тегов при создании Хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1043">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e72-1044">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e72-1044">Az.Resources</span></span>
* <span data-ttu-id="a6e72-1045">Сделайте команду "Область" необязательной в командлетах \*—AzPolicyAssignment с настройкой по умолчанию для контекстной подписки</span><span class="sxs-lookup"><span data-stu-id="a6e72-1045">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="a6e72-1046">Добавление примеров создания ADServicePrincipal с паролем и ключом учетных данных</span><span class="sxs-lookup"><span data-stu-id="a6e72-1046">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e72-1047">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e72-1047">Az.Sql</span></span>
<span data-ttu-id="a6e72-1048">Исправление командлета New-AzSqlDatabaseSecondary, чтобы проверить существование PartnerDatabaseName, а не DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1048">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a6e72-1049">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6e72-1049">Az.Storage</span></span>
* <span data-ttu-id="a6e72-1050">Поддержка набора шифрования типа ключа таблиц и очередей в создании учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="a6e72-1050">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="a6e72-1051">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a6e72-1051">New-AzStorageAccount</span></span>
* <span data-ttu-id="a6e72-1052">Представление RequestId, если StorageException не имеет ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="a6e72-1052">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="a6e72-1053">Исправление примера 6 командлета Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a6e72-1053">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a6e72-1054">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6e72-1054">Az.Websites</span></span>
* <span data-ttu-id="a6e72-1055">Set-AzWebapp и Set-AzWebappSlot поддерживают свойства AlwaysOn, MinTls и FtpsState</span><span class="sxs-lookup"><span data-stu-id="a6e72-1055">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="a6e72-1056">Устранение проблемы, при которой параметр HttpsOnly с одновременным изменением AppservicePlan с помощью одной команды Set-AzWebApp сбрасывал значение HttpsOnly до значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a6e72-1056">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="a6e72-1057">3.3.0 — январь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1057">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a6e72-1058">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e72-1058">Az.Accounts</span></span>
* <span data-ttu-id="a6e72-1059">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment: теперь они принимают параметры AzureAttestationServiceEndpointResourceId и AzureAttestationServiceEndpointSuffix.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1059">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a6e72-1060">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a6e72-1060">Az.Cdn</span></span>
* <span data-ttu-id="a6e72-1061">Теперь в командлете New-AzCdnEndpoint отображаются сведения из сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1061">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e72-1062">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e72-1062">Az.Compute</span></span>
* <span data-ttu-id="a6e72-1063">Командлет Set-AzVMCustomScriptExtension исправлен для виртуальной машины с управляемым диском ОС без профиля ОС.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1063">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="a6e72-1064">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a6e72-1064">Az.ContainerInstance</span></span>
* <span data-ttu-id="a6e72-1065">Исправлены имена параметров, используемые в примере командлета New-AzContainerGroup.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1065">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="a6e72-1066">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="a6e72-1066">Az.DataBoxEdge</span></span>
* <span data-ttu-id="a6e72-1067">Добавлен командлет Get-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1067">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="a6e72-1068">получение контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1068">Get the Edge Storage Container</span></span>
* <span data-ttu-id="a6e72-1069">Добавлен командлет New-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1069">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="a6e72-1070">создание контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1070">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="a6e72-1071">Добавлен командлет Remove-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1071">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="a6e72-1072">удаление контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1072">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="a6e72-1073">Добавлен командлет Invoke-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1073">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="a6e72-1074">вызов действия для обновления данных в контейнере хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1074">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="a6e72-1075">Добавлен командлет Get-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1075">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="a6e72-1076">получение учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1076">Get the Edge Storage Account</span></span>
* <span data-ttu-id="a6e72-1077">Добавлен командлет New-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1077">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="a6e72-1078">создание учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1078">Create new Edge Storage Account</span></span>
* <span data-ttu-id="a6e72-1079">Добавлен командлет Remove-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1079">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="a6e72-1080">удаление учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1080">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="a6e72-1081">Вызов командлета Invoke-AzDataBoxEdgeShare:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1081">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="a6e72-1082">вызов действия для обновления данных в общей папке.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1082">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="a6e72-1083">Добавлен командлет Set-AzDataBoxEdgeStorageAccountCredential:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1083">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="a6e72-1084">установка учетных данных для учетной записи хранилища Azure Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1084">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a6e72-1085">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a6e72-1085">Az.DataFactory</span></span>
* <span data-ttu-id="a6e72-1086">Добавлены свойства AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId и VersionStatus для командлета Get-AzDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1086">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="a6e72-1087">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.6.0.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1087">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="a6e72-1088">Для командлета Set-AzureRmDataFactoryV2IntegrationRuntime добавлен параметр PublicIPs, позволяющий включить создание среды Azure-SSIS IR со статическими общедоступными IP-адресами.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1088">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="a6e72-1089">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="a6e72-1089">Az.DevTestLabs</span></span>
* <span data-ttu-id="a6e72-1090">Удалена недействительная ссылка в файле Get-AzDtlAllowedVMSizesPolicy.md.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1090">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a6e72-1091">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a6e72-1091">Az.EventHub</span></span>
* <span data-ttu-id="a6e72-1092">Устранена проблема № 10634: исправлена ссылка на пустой объект для удаления пространства имен концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1092">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a6e72-1093">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a6e72-1093">Az.HDInsight</span></span>
* <span data-ttu-id="a6e72-1094">Устранена ошибка в файле Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1094">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="a6e72-1095">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="a6e72-1095">Az.MachineLearning</span></span>
* <span data-ttu-id="a6e72-1096">Вычислительная среда Машинного обучения больше недоступна, поэтому удалены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1096">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="a6e72-1097">Get-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="a6e72-1097">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="a6e72-1098">Get-AzMlOpClusterKey;</span><span class="sxs-lookup"><span data-stu-id="a6e72-1098">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="a6e72-1099">New-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="a6e72-1099">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="a6e72-1100">Remove-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="a6e72-1100">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="a6e72-1101">Set-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="a6e72-1101">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="a6e72-1102">Test-AzMlOpClusterSystemServicesUpdateAvailability;</span><span class="sxs-lookup"><span data-stu-id="a6e72-1102">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="a6e72-1103">Update-AzMlOpClusterSystemService.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1103">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e72-1104">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e72-1104">Az.Network</span></span>
* <span data-ttu-id="a6e72-1105">Обновлена зависимость Microsoft.Azure.Management.Sql от предварительной версии 1.36 до предварительной версии 1.37.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1105">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a6e72-1106">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-1106">Az.RecoveryServices</span></span>
* <span data-ttu-id="a6e72-1107">Добавлена поддержка Azure Site Recovery для виртуальных машин с управляемым диском, зашифрованных при хранении с помощью управляемых клиентом ключей, при восстановлении из Azure в поставщике Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1107">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="a6e72-1108">Добавлена поддержка Azure Site Recovery для необязательного ввода идентификатора набора шифрования диска при включении защиты в рамках восстановления из VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1108">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="a6e72-1109">Добавлена поддержка Azure Site Recovery для необязательного ввода идентификатора набора шифрования диска на уровне диска при включении защиты в рамках восстановления из VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1109">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="a6e72-1110">Добавлена поддержка Azure Site Recovery для обновления элемента, защищенного репликацией, путем сопоставления набора шифрования диска при восстановлении из HyperV в Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1110">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e72-1111">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e72-1111">Az.Resources</span></span>
* <span data-ttu-id="a6e72-1112">Исправлена ошибка в справочном документе о командлете Remove-AzTag.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1112">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e72-1113">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e72-1113">Az.Sql</span></span>
* <span data-ttu-id="a6e72-1114">Исправлена функция основных командлетов установки оценки уязвимостей: теперь она позволяет работать с базой данных master для базы данных Azure и ограничить ее в системных базах данных управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1114">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="a6e72-1115">Устранена ошибка, возникающая при создании группы отработки отказа экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1115">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="a6e72-1116">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a6e72-1116">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="a6e72-1117">Добавлен новый допустимый тип лицензии: DR (аварийное восстановление).</span><span class="sxs-lookup"><span data-stu-id="a6e72-1117">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a6e72-1118">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6e72-1118">Az.Storage</span></span>
* <span data-ttu-id="a6e72-1119">Добавлено предупреждающее сообщение о критическом изменении значения DefaultAction в следующем выпуске:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1119">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="a6e72-1120">Update-AzStorageAccountNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1120">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="a6e72-1121">Включена поддержка получения времени последней синхронизации учетной записи хранения путем выполнения командлета Get-AzureRmStorageAccount с параметром -IncludeGeoReplicationStats:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1121">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="a6e72-1122">Get-AzureRmStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1122">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="a6e72-1123">3.2.0 — декабрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1123">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="a6e72-1124">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="a6e72-1124">General</span></span>
* <span data-ttu-id="a6e72-1125">Обновление ссылок в .psd1 для использования относительного пути для всех модулей.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1125">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a6e72-1126">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e72-1126">Az.Accounts</span></span>
* <span data-ttu-id="a6e72-1127">Установка правильного параметра UserAgent для телеметрии на стороне клиента для Az 4.0 (предварительная версия).</span><span class="sxs-lookup"><span data-stu-id="a6e72-1127">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="a6e72-1128">Отображение понятного пользователю сообщения об ошибке, если в Az 4.0 (предварительная версия) не указан контекст.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1128">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a6e72-1129">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a6e72-1129">Az.Batch</span></span>
* <span data-ttu-id="a6e72-1130">Исправлена проблема [№ 10602](https://github.com/Azure/azure-powershell/issues/10602), из-за которой использование командлета **New-AzBatchPool** приводило к неправильной отправке VirtualMachineConfiguration.ContainerConfiguration или VirtualMachineConfiguration.DataDisks на сервер.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1130">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a6e72-1131">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a6e72-1131">Az.DataFactory</span></span>
* <span data-ttu-id="a6e72-1132">Обновление пакета SDK Фабрики данных для .NET до версии 4.5.0.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1132">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a6e72-1133">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a6e72-1133">Az.FrontDoor</span></span>
* <span data-ttu-id="a6e72-1134">Включена поддержка исключений управляемых правил WAF.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1134">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="a6e72-1135">Добавление SocketAddr в список автозавершения.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1135">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="a6e72-1136">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="a6e72-1136">Az.HealthcareApis</span></span>
* <span data-ttu-id="a6e72-1137">Обработка исключений.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1137">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a6e72-1138">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a6e72-1138">Az.KeyVault</span></span>
* <span data-ttu-id="a6e72-1139">Исправлена ошибка при получении доступа к значению, которое может быть не задано.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1139">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="a6e72-1140">Управление сертификатами шифрования на основе эллиптических кривых.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1140">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="a6e72-1141">Включена возможность указания кривой для политик сертификатов.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1141">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a6e72-1142">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a6e72-1142">Az.Monitor</span></span>
* <span data-ttu-id="a6e72-1143">Добавление необязательного аргумента в команду добавления параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1143">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="a6e72-1144">Существующий аргумент switch указывает на то, что экспорт в Log Analytics должен выполняться в фиксированную схему</span><span class="sxs-lookup"><span data-stu-id="a6e72-1144">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="a6e72-1145">(выделенный тип данных).</span><span class="sxs-lookup"><span data-stu-id="a6e72-1145">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e72-1146">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e72-1146">Az.Network</span></span>
* <span data-ttu-id="a6e72-1147">В приложении AzureFirewall, NAT и сетевых правилах включена поддержка IpGroups.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1147">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e72-1148">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e72-1148">Az.Resources</span></span>
* <span data-ttu-id="a6e72-1149">Устранена проблема, из-за которой при развертывании шаблона не удавалось считать его параметр, если имя параметра конфликтовало с именем встроенного параметра.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1149">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="a6e72-1150">Обновлены командлеты политики для использования новой версии API 2019-09-01 с поддержкой группирования в определениях наборов политик.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1150">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e72-1151">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e72-1151">Az.Sql</span></span>
* <span data-ttu-id="a6e72-1152">Обновлена функция автоматического создания расширенного хранилища для службы оценки уязвимостей в учетной записи StorageV2.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1152">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a6e72-1153">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6e72-1153">Az.Storage</span></span>
* <span data-ttu-id="a6e72-1154">Включена поддержка создания маркера SAS на основе удостоверения контейнера и большого двоичного объекта с аутентификацией Oauth на основе контекста службы хранилища:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1154">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="a6e72-1155">New-AzStorageContainerSASToken;</span><span class="sxs-lookup"><span data-stu-id="a6e72-1155">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="a6e72-1156">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="a6e72-1156">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="a6e72-1157">Отозвана поддержка ключей делегирования пользователя учетной записи хранения, а также всех маркеров SAS удостоверения:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1157">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="a6e72-1158">Revoke-AzStorageAccountUserDelegationKeys.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1158">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="a6e72-1159">Выполнено обновление до Microsoft.Azure.Management.Storage версии 14.2.0 для включения поддержки нового API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1159">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="a6e72-1160">Включена поддержка QuotaGiB (квота общего ресурса в ГиБ) для значений свыше 5120 в командлетах для работы с общими папками в плоскости управления и добавлен псевдоним Quota для параметра QuotaGiB.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1160">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="a6e72-1161">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="a6e72-1161">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="a6e72-1162">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="a6e72-1162">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="a6e72-1163">Добавлен псевдоним QuotaGiB для параметра Quota:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1163">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="a6e72-1164">Set-AzStorageShareQuota.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1164">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="a6e72-1165">Устранена проблема, из-за которой при использовании AzStorageContainerAcl могла очищаться хранимая политика доступа:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1165">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="a6e72-1166">Set-AzStorageContainerAcl.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1166">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="a6e72-1167">Версия 3.1.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1167">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a6e72-1168">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="a6e72-1168">Highlights since the last major release</span></span>
* <span data-ttu-id="a6e72-1169">Выпуск Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="a6e72-1169">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="a6e72-1170">Выпуск Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="a6e72-1170">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e72-1171">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e72-1171">Az.Compute</span></span>
* <span data-ttu-id="a6e72-1172">Функция повторного применения виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="a6e72-1172">VM Reapply feature</span></span>
    - <span data-ttu-id="a6e72-1173">Добавлен параметр повторного применения в командлет Set-AzVM.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1173">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="a6e72-1174">Функция AutomaticRepairs масштабируемого набора виртуальных машин:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1174">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="a6e72-1175">Добавлены параметры EnableAutomaticRepair, AutomaticRepairGracePeriod и AutomaticRepairMaxInstanceRepairsPercent в следующие командлеты:   New-AzVmssConfig Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a6e72-1175">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="a6e72-1176">Включена поддержка образа из коллекции разных клиентов для New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1176">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="a6e72-1177">Добавлен фрагмент Spot в средство заполнения аргументов параметра Priority в командлетах New-AzVM, New-AzVMConfig и New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1177">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="a6e72-1178">Добавлены параметры DiskIOPSReadWrite и DiskMBpsReadWrite в командлет Add-AzVmssDataDisk.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1178">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="a6e72-1179">Изменен параметр SourceImageId командлета New-AzGalleryImageVersion на необязательный.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1179">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="a6e72-1180">Добавлены параметры OSDiskImage и DataDiskImage в командлет New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1180">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="a6e72-1181">Добавлен параметр HyperVGeneration в командлет New-AzGalleryImageDefinition.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1181">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="a6e72-1182">Добавлены параметры SkipExtensionsOnOverprovisionedVMs в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1182">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="a6e72-1183">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="a6e72-1183">Az.DataBoxEdge</span></span>
* <span data-ttu-id="a6e72-1184">Добавлен командлет `Get-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1184">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="a6e72-1185">Получение заказа.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1185">Get the Order</span></span>
* <span data-ttu-id="a6e72-1186">Добавлен командлет `New-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1186">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="a6e72-1187">Создание заказа.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1187">Create new Order</span></span>
* <span data-ttu-id="a6e72-1188">Добавлен командлет `Remove-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1188">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="a6e72-1189">Удаление заказа.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1189">Remove the Order</span></span>
* <span data-ttu-id="a6e72-1190">Изменен командлет `New-AzDataBoxEdgeShare`.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1190">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="a6e72-1191">Создание локальной общей папки.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1191">Now creates Local Share</span></span>
* <span data-ttu-id="a6e72-1192">Добавлен командлет `Set-AzDataBoxEdgeRole`.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1192">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="a6e72-1193">Сопоставление IotRole с общей папкой.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1193">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="a6e72-1194">Добавлен командлет `Invoke-AzDataBoxEdgeDevice`.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1194">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="a6e72-1195">Вызов проверки обновлений, скачивание обновления, установка обновления на устройстве.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1195">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="a6e72-1196">Добавлен командлет `Get-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1196">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="a6e72-1197">Получение сведений о триггерах.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1197">Gets the information about Triggers</span></span>
* <span data-ttu-id="a6e72-1198">Добавлен командлет `New-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1198">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="a6e72-1199">Создание триггеров.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1199">Create new Triggers</span></span>
* <span data-ttu-id="a6e72-1200">Добавлен командлет `Remove-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1200">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="a6e72-1201">Удаление триггеров.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1201">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a6e72-1202">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a6e72-1202">Az.DataFactory</span></span>
* <span data-ttu-id="a6e72-1203">Обновление пакета SDK Фабрики данных для .NET до версии 4.4.0.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1203">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="a6e72-1204">Добавлен параметр ExpressCustomSetup в командлет Set-AzureRmDataFactoryV2IntegrationRuntime для включения конфигураций установки и сторонних компонентов без использования настраиваемого скрипта установки.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1204">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a6e72-1205">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a6e72-1205">Az.DataLakeStore</span></span>
* <span data-ttu-id="a6e72-1206">Обновлена документация по Get-AzDataLakeStoreDeletedItem и Restore-AzDataLakeStoreDeletedItem.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1206">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a6e72-1207">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a6e72-1207">Az.EventHub</span></span>
* <span data-ttu-id="a6e72-1208">Исправлена проблема № 10301. Исправлен формат даты маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1208">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a6e72-1209">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a6e72-1209">Az.FrontDoor</span></span>
* <span data-ttu-id="a6e72-1210">Добавлен параметр MinimumTlsVersion в Enable-AzFrontDoorCustomDomainHttps и New-AzFrontDoorFrontendEndpointObject.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1210">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="a6e72-1211">Добавлены параметры HealthProbeMethod и EnabledState в New-AzFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1211">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="a6e72-1212">Добавлен новый командлет для создания объекта BackendPoolsSettings для передачи при создании и обновлении Front Door.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1212">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="a6e72-1213">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="a6e72-1213">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e72-1214">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e72-1214">Az.Network</span></span>
* <span data-ttu-id="a6e72-1215">Изменены примеры параметра FilterData Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1215">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="a6e72-1216">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="a6e72-1216">Az.PrivateDns</span></span>
* <span data-ttu-id="a6e72-1217">Пакет SDK PrivateDns для .NET обновлен до версии 1.0.0</span><span class="sxs-lookup"><span data-stu-id="a6e72-1217">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a6e72-1218">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-1218">Az.RecoveryServices</span></span>
* <span data-ttu-id="a6e72-1219">Включена поддержка Azure Site Recovery для выбора типа диска при включении защиты.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1219">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="a6e72-1220">Внесено исправление Azure Site Recovery для изменения действия плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1220">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="a6e72-1221">Включена поддержка восстановления SQL Azure Backup для принятия баз данных файлового потока.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1221">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="a6e72-1222">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a6e72-1222">Az.RedisCache</span></span>
* <span data-ttu-id="a6e72-1223">Добавлен параметр MinimumTlsVersion в командлеты New-AzRedisCache и Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1223">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="a6e72-1224">Кроме того, добавлен параметр MinimumTlsVersion в выходные данные командлета Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1224">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="a6e72-1225">Добавлена проверка параметра -Size для командлетов Set-AzRedisCache и New-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1225">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e72-1226">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e72-1226">Az.Resources</span></span>
- <span data-ttu-id="a6e72-1227">Обновлены командлеты политики для использования новой версии API 2019-06-01 с новым свойством EnforcementMode в назначении политики.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1227">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="a6e72-1228">Обновлен пример справки по созданию определения политики</span><span class="sxs-lookup"><span data-stu-id="a6e72-1228">Updated create policy definition help example</span></span>
- <span data-ttu-id="a6e72-1229">Исправлена ошибка с параметром -ServicePrincipalName командлета Remove-AZADServicePrincipal с возвратом пустой ссылки, если имя субъекта службы не найдено.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1229">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="a6e72-1230">Исправлена ошибка с New-AZADServicePrincipal с возвратом пустой ссылки, если у клиента нет подписки.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1230">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="a6e72-1231">Изменен командлет New-AzAdServicePrincipal для добавления учетных данных только для связанного приложения.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1231">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e72-1232">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e72-1232">Az.Sql</span></span>
* <span data-ttu-id="a6e72-1233">Добавлена поддержка ReadReplicaCount для базы данных.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1233">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="a6e72-1234">Исправлена ошибка с Set-AzSqlDatabase, если избыточность в пределах зоны не настроена.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1234">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="a6e72-1235">Версия 3.0.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1235">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="a6e72-1236">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="a6e72-1236">General</span></span>
* <span data-ttu-id="a6e72-1237">Выпущена версия Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="a6e72-1237">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a6e72-1238">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e72-1238">Az.Accounts</span></span>
* <span data-ttu-id="a6e72-1239">Добавлено сообщение об устаревании для псевдонима "Resolve-Error".</span><span class="sxs-lookup"><span data-stu-id="a6e72-1239">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="a6e72-1240">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="a6e72-1240">Az.Advisor</span></span>
* <span data-ttu-id="a6e72-1241">Добавлена новая категория Operational Excellence (Эффективность работы) в командлет Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1241">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a6e72-1242">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a6e72-1242">Az.Batch</span></span>
* <span data-ttu-id="a6e72-1243">`CoreQuota` в `BatchAccountContext` переименован в `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1243">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="a6e72-1244">Также появился новый `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1244">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="a6e72-1245">Это влияет на **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1245">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="a6e72-1246">Параметр **New-AzBatchTask** `-ResourceFile` теперь принимает коллекцию объектов `PSResourceFile`, которые можно создать с помощью нового командлета **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1246">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="a6e72-1247">Новый командлет **New-AzBatchResourceFile**, который помогает создавать объекты `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1247">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="a6e72-1248">Их можно передавать в **New-AzBatchTask** в параметре `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1248">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="a6e72-1249">Это позволяет поддерживать два новых типа файлов ресурсов, которые дополняют существующий метод `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1249">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="a6e72-1250">Файлы ресурсов на основе `AutoStorageContainerName` скачивают весь контейнер автоматического хранения в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1250">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="a6e72-1251">Файлы ресурсов на основе `StorageContainerUrl` скачивают указанный в URL-адресе контейнер в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1251">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="a6e72-1252">Удалено свойство `ApplicationPackages` в `PSApplication`, который возвращается из **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1252">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="a6e72-1253">Отдельные пакеты в приложении теперь можно извлечь с помощью **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1253">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="a6e72-1254">Например: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1254">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="a6e72-1255">`ApplicationId` переименован в `ApplicationName` для **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** и **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1255">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="a6e72-1256">Теперь `ApplicationId` является псевдонимом для `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1256">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="a6e72-1257">Добавлено новое свойство `PSWindowsUserConfiguration` в `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1257">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="a6e72-1258">`Version` переименован в `Name` для `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1258">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="a6e72-1259">`BlobSource` переименован в `HttpUrl` для `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1259">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="a6e72-1260">Удалено свойство `OSDisk` из `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1260">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="a6e72-1261">Удалена операция **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1261">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="a6e72-1262">Больше она не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1262">This operation is no longer supported.</span></span>
* <span data-ttu-id="a6e72-1263">Удалено `TargetOSVersion` из `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1263">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="a6e72-1264">`CurrentOSVersion` переименован в `OSVersion` для `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1264">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="a6e72-1265">Удалено `DataEgressGiB` и `DataIngressGiB` из `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1265">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="a6e72-1266">Операция **Get-AzBatchNodeAgentSku** удалена и заменена на **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1266">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="a6e72-1267">**Get-AzBatchSupportedImage** возвращает те же данные, что и **Get-AzBatchNodeAgentSku**, но в более удобном формате.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1267">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="a6e72-1268">Также возвращаются новые непроверенные образы.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1268">New non-verified images are also now returned.</span></span> <span data-ttu-id="a6e72-1269">Включается и дополнительная информация о `Capabilities` и `BatchSupportEndOfLife` для каждого образа.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1269">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="a6e72-1270">Добавлена возможность монтировать файловые системы на каждом узле пула с помощью нового параметра `MountConfiguration` в **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1270">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="a6e72-1271">Теперь поддерживаются правила безопасности сети, которые блокируют сетевой доступ к пулу по исходящему порту трафика.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1271">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="a6e72-1272">Это выполняется с помощью свойства `SourcePortRanges` для `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1272">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="a6e72-1273">Что касается выполнения контейнеров, пакетная служба теперь поддерживает выполнение задачи в рабочей папке контейнера или рабочей папке задачи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1273">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="a6e72-1274">Выбор зависит от параметра `WorkingDirectory` в `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1274">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="a6e72-1275">Добавлена возможность указать коллекцию общедоступных IP-адресов для `PSNetworkConfiguration` с помощью нового свойства `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1275">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="a6e72-1276">Это гарантирует, что узлы в пуле будут иметь IP-адреса из списка, предоставленного пользователем.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1276">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="a6e72-1277">Если значение не задано, по умолчанию для `WaitForSuccess` в `PSSTartTask` используется значение `$True` (ранее `$False`).</span><span class="sxs-lookup"><span data-stu-id="a6e72-1277">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="a6e72-1278">Если значение не задано, по умолчанию для `Scope` в `PSAutoUserSpecification` используется значение `Pool` (ранее `Task` для Windows или `Pool` для Linux).</span><span class="sxs-lookup"><span data-stu-id="a6e72-1278">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a6e72-1279">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a6e72-1279">Az.Cdn</span></span>
* <span data-ttu-id="a6e72-1280">Добавлены UrlRewriteAction и CacheKeyQueryStringAction в RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1280">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="a6e72-1281">Исправлено несколько ошибок, таких как отсутствующий входной параметр Selector в командлете New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1281">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e72-1282">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e72-1282">Az.Compute</span></span>
* <span data-ttu-id="a6e72-1283">Функция набора шифрования диска</span><span class="sxs-lookup"><span data-stu-id="a6e72-1283">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="a6e72-1284">Новые командлеты:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="a6e72-1284">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="a6e72-1285">Добавлен параметр ProximityPlacementGroupId в следующие командлеты:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="a6e72-1285">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="a6e72-1286">Параметры DiskEncryptionSetId и EncryptionType добавлены в следующие командлеты:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="a6e72-1286">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="a6e72-1287">Добавлен параметр PublicIPAddressVersion в New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="a6e72-1287">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="a6e72-1288">FileUris для расширения пользовательских скриптов теперь будет защищенным, а не общедоступным параметром</span><span class="sxs-lookup"><span data-stu-id="a6e72-1288">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="a6e72-1289">Добавлено ScaleInPolicy в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a6e72-1289">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="a6e72-1290">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="a6e72-1290">Breaking changes</span></span>
    - <span data-ttu-id="a6e72-1291">Параметр UploadSizeInBytes применяется теперь вместо DiskSizeGB для New-AzDiskConfig, если CreateOption имеет значение Upload</span><span class="sxs-lookup"><span data-stu-id="a6e72-1291">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="a6e72-1292">PublishingProfile.Source.ManagedImage.Id заменяется на StorageProfile.Source.Id в объекте GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="a6e72-1292">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a6e72-1293">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a6e72-1293">Az.DataFactory</span></span>
* <span data-ttu-id="a6e72-1294">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.3.0.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1294">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a6e72-1295">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a6e72-1295">Az.DataLakeStore</span></span>
* <span data-ttu-id="a6e72-1296">Обновлен пакет SDK для ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), включает следующие исправления</span><span class="sxs-lookup"><span data-stu-id="a6e72-1296">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="a6e72-1297">Не создается исключение при невозможности десериализовать значение времени создания для записи в корзине или каталоге.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1297">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="a6e72-1298">Предоставляется параметр для времени ожидания запроса в adlsclient</span><span class="sxs-lookup"><span data-stu-id="a6e72-1298">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="a6e72-1299">Исправлена передача исходного значения syncflag для восстановления badoffset</span><span class="sxs-lookup"><span data-stu-id="a6e72-1299">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="a6e72-1300">Исправлена операция EnumerateDirectory, чтобы она извлекала токен продолжения после проверки ответа</span><span class="sxs-lookup"><span data-stu-id="a6e72-1300">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="a6e72-1301">Исправлена ошибка объединения</span><span class="sxs-lookup"><span data-stu-id="a6e72-1301">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a6e72-1302">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a6e72-1302">Az.FrontDoor</span></span>
* <span data-ttu-id="a6e72-1303">Исправлены разные опечатки в разных частях модуля</span><span class="sxs-lookup"><span data-stu-id="a6e72-1303">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a6e72-1304">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a6e72-1304">Az.HDInsight</span></span>
* <span data-ttu-id="a6e72-1305">Исправлена ошибка, из-за которой клиент получал сообщение об ошибке 'Not a valid Base-64 string' (Не является допустимой строкой Base64) при выполнении Get-AzHDInsightCluster для получения кластера с хранилищем ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1305">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="a6e72-1306">Добавлен параметр с именем ApplicationId в три командлета Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig и New-AzHDInsightCluster, чтобы клиент мог предоставить идентификатор приложения субъекта-службы для доступа к Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1306">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="a6e72-1307">Для Microsoft.Azure.Management.HDInsight изменена версия с 2.1.0 на 5.1.0</span><span class="sxs-lookup"><span data-stu-id="a6e72-1307">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="a6e72-1308">Удалены пять командлетов:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1308">Removed five cmdlets:</span></span>
    - <span data-ttu-id="a6e72-1309">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="a6e72-1309">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="a6e72-1310">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="a6e72-1310">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="a6e72-1311">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="a6e72-1311">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="a6e72-1312">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a6e72-1312">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="a6e72-1313">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a6e72-1313">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="a6e72-1314">Добавлены три командлета:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1314">Added three cmdlets:</span></span>
    - <span data-ttu-id="a6e72-1315">Get-AzHDInsightMonitoring заменяет собой Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1315">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="a6e72-1316">Enable-AzHDInsightMonitoring заменяет собой Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1316">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="a6e72-1317">Disable-AzHDInsightMonitoring заменяет собой Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1317">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="a6e72-1318">Исправлен командлет Get-AzHDInsightProperties, чтобы он поддерживал получение сведений о возможностях из определенного расположения.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1318">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="a6e72-1319">Удалены наборы параметров ("Spark1", "Spark2") из Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1319">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="a6e72-1320">Добавлены примеры в справочные документы по командлету Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1320">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="a6e72-1321">Изменен тип выходных данных для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1321">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="a6e72-1322">Для Get-AzHDInsightProperties тип выходных данных изменен с CapabilitiesResponse на AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1322">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="a6e72-1323">Для Remove-AzHDInsightCluster тип выходных данных изменен с ClusterGetResponse на bool.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1323">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="a6e72-1324">Для Set-AzHDInsightGatewaySettings тип выходных данных изменен с HttpConnectivitySettings на GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1324">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="a6e72-1325">Добавлены несколько условий для проверки сценариев.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1325">Added some scenario test cases.</span></span>
* <span data-ttu-id="a6e72-1326">Удалены несколько псевдонимов: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1326">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a6e72-1327">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a6e72-1327">Az.IotHub</span></span>
* <span data-ttu-id="a6e72-1328">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="a6e72-1328">Breaking changes:</span></span>
    - <span data-ttu-id="a6e72-1329">Командлет Add-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1329">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="a6e72-1330">Удален набор параметров __AllParameterSets для командлета Add-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1330">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="a6e72-1331">Командлет Get-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1331">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="a6e72-1332">Удален набор параметров __AllParameterSets для командлета Get-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1332">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="a6e72-1333">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1333">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="a6e72-1334">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1334">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="a6e72-1335">Командлет New-AzIotHubExportDevice больше не поддерживает псевдоним New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1335">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="a6e72-1336">Командлет New-AzIotHubImportDevice больше не поддерживает псевдоним New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1336">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="a6e72-1337">Командлет Remove-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1337">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="a6e72-1338">Удален набор параметров __AllParameterSets для командлета Remove-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1338">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="a6e72-1339">Командлет Set-AzIotHub теперь не поддерживает параметр OperationsMonitoringProperties и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1339">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="a6e72-1340">Удален набор параметров UpdateOperationsMonitoringProperties для командлета Set-AzIotHub.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1340">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a6e72-1341">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-1341">Az.RecoveryServices</span></span>
* <span data-ttu-id="a6e72-1342">Azure Site Recovery поддерживает настройку сетевых ресурсов, например групп безопасности сети, общедоступных IP-адресов и внутренних подсистем балансировки нагрузки из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1342">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="a6e72-1343">Azure Site Recovery поддерживает запись на управляемый диск из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1343">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="a6e72-1344">Azure Site Recovery поддерживает сокращение NIC из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1344">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="a6e72-1345">Azure Site Recovery поддерживает ускорение сети NIC из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1345">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="a6e72-1346">Azure Site Recovery поддерживает автоматическое обновление агента из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1346">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="a6e72-1347">Azure Site Recovery поддерживает стандартный SSD-накопитель из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1347">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="a6e72-1348">Azure Site Recovery поддерживает двухпроходное шифрование диска Azure из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1348">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="a6e72-1349">Azure Site Recovery поддерживает новый добавленный диск из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1349">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="a6e72-1350">Добавлена функция SoftDelete для виртуальных машин и соответствующие тесты</span><span class="sxs-lookup"><span data-stu-id="a6e72-1350">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e72-1351">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e72-1351">Az.Resources</span></span>
* <span data-ttu-id="a6e72-1352">Обновлена сборка зависимостей Microsoft.Extensions.Caching.Memory с версии 1.1.1 до 2.2</span><span class="sxs-lookup"><span data-stu-id="a6e72-1352">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e72-1353">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e72-1353">Az.Network</span></span>
* <span data-ttu-id="a6e72-1354">Изменены все командлеты для PrivateEndpointConnection, чтобы они поддерживали универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1354">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="a6e72-1355">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1355">Updated cmdlet:</span></span>
        - <span data-ttu-id="a6e72-1356">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1356">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a6e72-1357">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1357">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a6e72-1358">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1358">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a6e72-1359">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1359">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a6e72-1360">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a6e72-1360">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="a6e72-1361">Добавлен новый командлет для PrivateLinkResource, который поддерживает универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1361">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="a6e72-1362">Новый командлет</span><span class="sxs-lookup"><span data-stu-id="a6e72-1362">New cmdlet:</span></span>
        - <span data-ttu-id="a6e72-1363">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="a6e72-1363">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="a6e72-1364">Добавлены новые поля и параметр для протокола прокси версии 2.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1364">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="a6e72-1365">Добавлено свойство EnableProxyProtocol в PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a6e72-1365">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="a6e72-1366">Добавлено свойство LinkIdentifier в PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a6e72-1366">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="a6e72-1367">Обновлен New-AzPrivateLinkService для поддержки нового необязательного параметра EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1367">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="a6e72-1368">Исправлено описание параметра в справочной документации по командлету New-AzApplicationGatewaySku.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1368">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="a6e72-1369">Новые командлеты для поддержки политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="a6e72-1369">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="a6e72-1370">Добавлена поддержка дочерних ресурсов RouteTables для VirtualHub</span><span class="sxs-lookup"><span data-stu-id="a6e72-1370">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="a6e72-1371">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1371">New cmdlets added:</span></span>
        - <span data-ttu-id="a6e72-1372">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="a6e72-1372">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="a6e72-1373">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="a6e72-1373">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="a6e72-1374">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="a6e72-1374">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="a6e72-1375">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="a6e72-1375">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="a6e72-1376">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a6e72-1376">Set-AzVirtualHub</span></span>
* <span data-ttu-id="a6e72-1377">Добавлена поддержка новых свойств SKU для VirtualHub и VirtualWANType в VirtualWan</span><span class="sxs-lookup"><span data-stu-id="a6e72-1377">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="a6e72-1378">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1378">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="a6e72-1379">New-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="a6e72-1379">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="a6e72-1380">Update-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="a6e72-1380">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="a6e72-1381">New-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="a6e72-1381">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="a6e72-1382">Update-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="a6e72-1382">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="a6e72-1383">Добавлена поддержка свойства EnableInternetSecurity для HubVnetConnection, VpnConnection и ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="a6e72-1383">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="a6e72-1384">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1384">New cmdlets added:</span></span>
        - <span data-ttu-id="a6e72-1385">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="a6e72-1385">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="a6e72-1386">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1386">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="a6e72-1387">New-AzureRmVirtualHubVnetConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="a6e72-1387">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="a6e72-1388">New-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="a6e72-1388">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="a6e72-1389">Update-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="a6e72-1389">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="a6e72-1390">New-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="a6e72-1390">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="a6e72-1391">Set-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="a6e72-1391">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="a6e72-1392">Добавлена поддержка настройки политики верхнего уровня WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="a6e72-1392">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="a6e72-1393">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1393">New cmdlets added:</span></span>
        - <span data-ttu-id="a6e72-1394">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="a6e72-1394">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="a6e72-1395">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="a6e72-1395">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="a6e72-1396">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="a6e72-1396">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="a6e72-1397">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="a6e72-1397">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="a6e72-1398">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="a6e72-1398">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="a6e72-1399">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="a6e72-1399">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="a6e72-1400">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1400">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="a6e72-1401">New-AzApplicationGatewayFirewallPolicy: добавлены параметры PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="a6e72-1401">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="a6e72-1402">Добавлена поддержка оператора Geo-Match для CustomRule</span><span class="sxs-lookup"><span data-stu-id="a6e72-1402">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="a6e72-1403">Добавлен параметр GeoMatch в оператор для FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="a6e72-1403">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="a6e72-1404">Добавлена поддержка политики брандмауэра perListener и perSite</span><span class="sxs-lookup"><span data-stu-id="a6e72-1404">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="a6e72-1405">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1405">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="a6e72-1406">New-AzApplicationGatewayHttpListener: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="a6e72-1406">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="a6e72-1407">New-AzApplicationGatewayPathRuleConfig: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="a6e72-1407">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="a6e72-1408">Исправлен учет регистра для требуемой подсети с именем AzureBastionSubnet в PSBastion</span><span class="sxs-lookup"><span data-stu-id="a6e72-1408">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="a6e72-1409">Поддержка полного доменного имени назначения в правилах сети и преобразованного полного доменного имени в правилах NAT для брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="a6e72-1409">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="a6e72-1410">Добавлена поддержка ресурсов верхнего уровня RouteTables для IpGroup</span><span class="sxs-lookup"><span data-stu-id="a6e72-1410">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="a6e72-1411">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1411">New cmdlets added:</span></span>
        - <span data-ttu-id="a6e72-1412">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="a6e72-1412">New-AzIpGroup</span></span>
        - <span data-ttu-id="a6e72-1413">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="a6e72-1413">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="a6e72-1414">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="a6e72-1414">Get-AzIpGroup</span></span>
        - <span data-ttu-id="a6e72-1415">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="a6e72-1415">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a6e72-1416">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a6e72-1416">Az.ServiceFabric</span></span>
* <span data-ttu-id="a6e72-1417">Удален командлет Add-AzServiceFabricApplicationCertificate, так как соответствующий сценарий выполняется командлетом Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1417">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e72-1418">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e72-1418">Az.Sql</span></span>
* <span data-ttu-id="a6e72-1419">Добавлена поддержка восстановления удаленных баз данных в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1419">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="a6e72-1420">Из кода удалены старые командлеты аудита.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1420">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="a6e72-1421">Удалены нерекомендуемые псевдонимы:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1421">Removed deprecated aliases:</span></span>
* <span data-ttu-id="a6e72-1422">Get-AzSqlDatabaseIndexRecommendations (вместо него используйте Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="a6e72-1422">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="a6e72-1423">Get-AzSqlDatabaseRestorePoints (вместо него используйте Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="a6e72-1423">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="a6e72-1424">Удален командлет Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a6e72-1424">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="a6e72-1425">Удалены псевдонимы для нерекомендуемых командлетов параметров оценки уязвимостей</span><span class="sxs-lookup"><span data-stu-id="a6e72-1425">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="a6e72-1426">Командлеты расширенного обнаружения угроз объявлены устаревшими</span><span class="sxs-lookup"><span data-stu-id="a6e72-1426">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="a6e72-1427">Добавлены командлеты для отключения и включения рекомендаций о конфиденциальности для столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1427">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a6e72-1428">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6e72-1428">Az.Storage</span></span>
* <span data-ttu-id="a6e72-1429">Поддержка включения большой общей папки при создании или обновлении учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="a6e72-1429">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="a6e72-1430">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a6e72-1430">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="a6e72-1431">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a6e72-1431">Set-AzStorageAccount</span></span>
* <span data-ttu-id="a6e72-1432">При закрытии или получении маркера файла пропускается проверка того, является ли входной путь файлом или каталогом, чтобы избежать сбоев при получении объектов в состоянии DeletePending.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1432">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="a6e72-1433">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="a6e72-1433">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="a6e72-1434">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="a6e72-1434">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="a6e72-1435">2.8.0 — октябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1435">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="a6e72-1436">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="a6e72-1436">General</span></span>
* <span data-ttu-id="a6e72-1437">Выпуск Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="a6e72-1437">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a6e72-1438">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e72-1438">Az.Accounts</span></span>
* <span data-ttu-id="a6e72-1439">Обновление телеметрии и перезаписи URL-адресов для созданных модулей, исправление для модульных тестов Windows.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1439">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a6e72-1440">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a6e72-1440">Az.ApiManagement</span></span>
* <span data-ttu-id="a6e72-1441">**Set-AzApiManagementApi** — в ApiVersionSet добавлена поддержка обновления API.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1441">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="a6e72-1442">исправлена проблема https://github.com/Azure/azure-powershell/issues/10068.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1442">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a6e72-1443">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a6e72-1443">Az.Automation</span></span>
* <span data-ttu-id="a6e72-1444">Исправлен командлет New-AzureAutomationSoftwareUpdateConfiguration для параметра перезагрузки Linux.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1444">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a6e72-1445">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a6e72-1445">Az.Batch</span></span>
* <span data-ttu-id="a6e72-1446">Командлет **Get-AzBatchNodeAgentSku** объявлен устаревшим и будет заменен на **Get-AzBatchSupportImage** в версии 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1446">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e72-1447">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e72-1447">Az.Compute</span></span>
* <span data-ttu-id="a6e72-1448">В командлеты New-AzVM и New-AzVmss добавлены параметры Priority, EvictionPolicy и MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1448">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="a6e72-1449">Исправлены предупреждающее сообщение для командлетов Add-AzVMAdditionalUnattendContent и Add-AzVMSshPublicKey и справочная документация по ним.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1449">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="a6e72-1450">Для Set-AzVMDiskEncryptionExtension исправлено исключение -skipVmBackup для виртуальных машин Linux с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1450">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="a6e72-1451">Исправлена ошибка при изменении параметров шифрования в Set-AzVMDiskEncryptionExtension, реализован двухэтапный сценарий.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1451">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a6e72-1452">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a6e72-1452">Az.DataFactory</span></span>
* <span data-ttu-id="a6e72-1453">Добавлены команды CRUD для потока данных Фабрики данных Azure версии 2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow и Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1453">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="a6e72-1454">Добавлены команды действий для сеанса отладки потока данных Фабрики данных Azure версии 2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand и Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1454">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="a6e72-1455">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.2.0.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1455">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a6e72-1456">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a6e72-1456">Az.DataLakeStore</span></span>
* <span data-ttu-id="a6e72-1457">Проверка учетной записи исправлена так, чтобы учетные записи, содержащие знак "-", можно было передавать без домена.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1457">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="a6e72-1458">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="a6e72-1458">Az.HealthcareApis</span></span>
* <span data-ttu-id="a6e72-1459">Версия PowerShell обновлена до 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1459">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="a6e72-1460">Версия пакета SDK обновлена до 1.0.2.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1460">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="a6e72-1461">В тестах обновлены ссылки на новую версию пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1461">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="a6e72-1462">Вложенная выходная структура заменена на плоскую.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1462">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a6e72-1463">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a6e72-1463">Az.IotHub</span></span>
* <span data-ttu-id="a6e72-1464">Добавлен новый источник маршрутизации DigitalTwinChangeEvents.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1464">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="a6e72-1465">Исправлены незначительные ошибки: Get-AzIothub не возвращает subscriptionId.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1465">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a6e72-1466">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a6e72-1466">Az.Monitor</span></span>
* <span data-ttu-id="a6e72-1467">Добавлены новые получатели групп действий: -ItsmReceiver, -VoiceReceiver, -ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1467">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="a6e72-1468">Для получателей включите общую схему оповещений.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1468">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="a6e72-1469">Это не касается получателей SMS, push-уведомлений приложения Azure, ITSM и голосовых сообщений.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1469">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="a6e72-1470">Веб-перехватчики теперь поддерживают аутентификацию Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1470">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e72-1471">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e72-1471">Az.Network</span></span>
* <span data-ttu-id="a6e72-1472">Добавлен новый командлет Get-AzAvailableServiceAlias, позволяющий получить псевдонимы для политик конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1472">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="a6e72-1473">В подключениях шлюза виртуальной сети появилась возможность добавлять селекторы трафика.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1473">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="a6e72-1474">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1474">New cmdlets added:</span></span>
        - <span data-ttu-id="a6e72-1475">New-AzureRmTrafficSelectorPolicy.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1475">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="a6e72-1476">В командлеты добавлены необязательные параметры -TrafficSelectorPolicies, -New-AzureRmVirtualNetworkGatewayConnection, -Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1476">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="a6e72-1477">В конфигурациях правил сетевой безопасности добавлена поддержка протоколов ESP и AH.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1477">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="a6e72-1478">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1478">Updated cmdlets:</span></span>
        - <span data-ttu-id="a6e72-1479">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1479">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="a6e72-1480">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1480">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="a6e72-1481">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1481">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="a6e72-1482">Улучшена обработка исключений в командлетах Cortex.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1482">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="a6e72-1483">Выпущены новые поколения и номера SKU VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1483">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="a6e72-1484">Представлены новые поколения VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1484">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="a6e72-1485">Представлены новые номера SKU VirtualNetworkGateways с высокой пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1485">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="a6e72-1486">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a6e72-1486">Az.RedisCache</span></span>
* <span data-ttu-id="a6e72-1487">В справочную документацию по Set-AzRedisCache добавлены недостающие значения для параметра -Size.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1487">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e72-1488">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e72-1488">Az.Sql</span></span>
* <span data-ttu-id="a6e72-1489">Добавлена возможность назначать администратора Active Directory в Управляемом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1489">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a6e72-1490">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6e72-1490">Az.Storage</span></span>
* <span data-ttu-id="a6e72-1491">Клиентская библиотека службы хранилища Azure обновлена до версии 11.1.0.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1491">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="a6e72-1492">NextPageLink теперь позволяет получить список контейнеров с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1492">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="a6e72-1493">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a6e72-1493">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="a6e72-1494">NextPageLink теперь позволяет получить список учетных записей хранения из подписки.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1494">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="a6e72-1495">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a6e72-1495">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="a6e72-1496">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="a6e72-1496">Az.StorageSync</span></span>
* <span data-ttu-id="a6e72-1497">Исправлена проблема 9810 с Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1497">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a6e72-1498">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6e72-1498">Az.Websites</span></span>
* <span data-ttu-id="a6e72-1499">Обновление плана службы приложений с помощью Set-AzWebApp приводило к сбою приложения.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1499">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="a6e72-1500">2.7.0 — сентябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1500">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="a6e72-1501">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a6e72-1501">Az.ApiManagement</span></span>
* <span data-ttu-id="a6e72-1502">В справочной документации по командлету Set-AzApiManagementPolicy обновлено описание параметра -Format.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1502">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="a6e72-1503">Из справочной документации удалены ссылки на нерекомендуемый командлет Update-AzApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1503">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="a6e72-1504">Вместо него следует использовать командлет Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1504">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a6e72-1505">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a6e72-1505">Az.Automation</span></span>
* <span data-ttu-id="a6e72-1506">В справочной документации по командлету Register-AzAutomationDscNode исправлена опечатка в примере.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1506">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="a6e72-1507">Добавлено уточнение об ограничениях ОС для командлета Register-AzAutomationDSCNode.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1507">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="a6e72-1508">Исправлено исключение пустой ссылки для параметра -Wait в командлете Start-AzAutomationRunbook.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1508">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e72-1509">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e72-1509">Az.Compute</span></span>
* <span data-ttu-id="a6e72-1510">Добавлен параметр UploadSizeInBytes для командлета New-AzDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1510">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="a6e72-1511">Добавлен добавочный параметр для командлета New-AzSnapshotConfig.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1511">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="a6e72-1512">Для виртуальной машины добавлены такие функции с низким приоритетом:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1512">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="a6e72-1513">Для командлета New-AzVMConfig добавлены параметры MaxPrice, EvictionPolicy и Priority.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1513">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="a6e72-1514">Для командлетов New-AzVmssConfig, Update-AzVM и Update-AzVmss добавлен параметр MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1514">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="a6e72-1515">Для командлета Get-AzAvailabilitySet устранена проблема со ссылкой на виртуальную машину, когда в нем перечисляются все группы доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1515">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="a6e72-1516">Исправлено исключение NULL для командлета Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1516">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="a6e72-1517">Исправлен метод поиска VHD для относительной конечной позиции.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1517">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="a6e72-1518">Устранена проблема с UltraSSD для командлетов New-AzVM и Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1518">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a6e72-1519">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a6e72-1519">Az.DataFactory</span></span>
* <span data-ttu-id="a6e72-1520">Добавлены 3 новые команды для ADF версии 2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription и Get-AzDataFactoryV2TriggerSubscriptionStatus.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1520">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="a6e72-1521">Пакет SDK ADF для .NET обновлен до версии 4.1.3.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1521">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a6e72-1522">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a6e72-1522">Az.HDInsight</span></span>
* <span data-ttu-id="a6e72-1523">Укажите критические изменения.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1523">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a6e72-1524">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a6e72-1524">Az.IotHub</span></span>
* <span data-ttu-id="a6e72-1525">Добавлена поддержка для вызова отработки отказа для IotHub в георегион аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1525">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="a6e72-1526">Добавлена поддержка для управления обогащением сообщений для IotHub.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1526">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="a6e72-1527">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1527">New cmdlets are:</span></span>
    - <span data-ttu-id="a6e72-1528">Add-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="a6e72-1528">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="a6e72-1529">Get-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="a6e72-1529">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="a6e72-1530">Remove-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="a6e72-1530">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="a6e72-1531">Set-AzIotHubMessageEnrichment.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1531">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a6e72-1532">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a6e72-1532">Az.Monitor</span></span>
* <span data-ttu-id="a6e72-1533">Указание на самую последнюю версию пакета SDK для монитора, т. е. 0.24.1-preview:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1533">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="a6e72-1534">В командлеты метрик добавлены некритические изменения, т. е. перечисление единиц поддерживает несколько новых значений.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1534">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="a6e72-1535">Эти командлеты доступны только для чтения, поэтому входные данные командлетов не будут изменены.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1535">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="a6e72-1536">Актуальная версия API запросов **ActionGroups** — **2019-06-01**. До этого была версия **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1536">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="a6e72-1537">Тесты сценария обновлены в соответствии с этим изменением.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1537">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="a6e72-1538">В конструкторы классов **EmailReceiver** и **WebhookReceiver** добавлен один новый обязательный аргумент — логическое значение с именем **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1538">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="a6e72-1539">Сейчас для него установлено значение **false**, чтобы скрыть это критическое изменение от командлетов.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1539">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="a6e72-1540">**Примечание**. Это временное изменение, которое должно быть подтверждено командой оповещения.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1540">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="a6e72-1541">Порядок аргументов для конструктора класса **Source** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1541">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="a6e72-1542">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1542">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="a6e72-1543">Порядок аргументов для конструктора класса **AlertingAction** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1543">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="a6e72-1544">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1544">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="a6e72-1545">Добавлена поддержка критериев динамического порога для оповещения метрики версии 2:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1545">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="a6e72-1546">New-AzMetricAlertRuleV2Criteria: теперь также позволяет создавать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1546">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="a6e72-1547">Add-AzMetricAlertRuleV2: теперь также позволяет принимать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1547">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="a6e72-1548">Добавлены усовершенствования в командлетах запланированных правил запросов (SQR).</span><span class="sxs-lookup"><span data-stu-id="a6e72-1548">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="a6e72-1549">Командлеты будут принимать параметр Location в обоих форматах: расположение (например, eastus) или отображаемое имя расположения (например, "восточная часть США").</span><span class="sxs-lookup"><span data-stu-id="a6e72-1549">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="a6e72-1550">Параметр Enabled проиллюстрирован в файлах справки надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1550">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="a6e72-1551">Добавлены примеры для необязательного параметра ActionGroup.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1551">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="a6e72-1552">Все файлы справки улучшены.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1552">Overall improved help files</span></span>
* <span data-ttu-id="a6e72-1553">Исправлена ошибка в определении типа области для командлета Set-AzActionRule.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1553">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e72-1554">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e72-1554">Az.Network</span></span>
* <span data-ttu-id="a6e72-1555">Исправлен неправильный пример в справочной документации по командлету New-AzApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1555">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="a6e72-1556">В справочную документацию по командлету Get-AzNetworkWatcherPacketCapture добавлено примечание, посвященное извлечению всех свойств для записи пакетов.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1556">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="a6e72-1557">В справочной документации по командлету Test-AzNetworkWatcherIPFlow исправлен пример: теперь он правильно перечисляет сетевые карты.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1557">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="a6e72-1558">Улучшен анализ облачных исключений для отображения дополнительных сведений (при их наличии).</span><span class="sxs-lookup"><span data-stu-id="a6e72-1558">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="a6e72-1559">Улучшен анализ облачных исключений для обработки дополнительного типа исключения SDK.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1559">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="a6e72-1560">Исправлено неправильное сопоставление моделей правил безопасности.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1560">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="a6e72-1561">Добавлены свойства сетевого интерфейса для компонента частного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1561">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="a6e72-1562">Для интерфейса PSNetworkInterface добавлено свойство PrivateEndpoint с типом PSResourceId.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1562">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="a6e72-1563">В PSNetworkInterfaceIPConfiguration добавлено свойство PrivateLinkConnectionProperties с типом PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1563">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="a6e72-1564">Добавлен новый класс модели: PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1564">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="a6e72-1565">Добавлен новый тип ApplicationRuleProtocolType "mssql" для ресурса Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1565">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="a6e72-1566">Поддержка многоканального подключения в Виртуальной глобальной сети:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1566">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="a6e72-1567">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="a6e72-1567">New cmdlets</span></span>
        - <span data-ttu-id="a6e72-1568">New-AzVpnSiteLink;</span><span class="sxs-lookup"><span data-stu-id="a6e72-1568">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="a6e72-1569">New-AzVpnSiteLinkConnection;</span><span class="sxs-lookup"><span data-stu-id="a6e72-1569">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="a6e72-1570">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1570">Updated cmdlet:</span></span>
        - <span data-ttu-id="a6e72-1571">New-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="a6e72-1571">New-VpnSite</span></span>
        - <span data-ttu-id="a6e72-1572">Update-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="a6e72-1572">Update-VpnSite</span></span>
        - <span data-ttu-id="a6e72-1573">New-VpnConnection;</span><span class="sxs-lookup"><span data-stu-id="a6e72-1573">New-VpnConnection</span></span>
        - <span data-ttu-id="a6e72-1574">Update-VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1574">Update-VpnConnection</span></span>
* <span data-ttu-id="a6e72-1575">Исправлены документы с некоторыми примерами PowerShell для использования командлетов AZ вместо командлетов AzureRM.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1575">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a6e72-1576">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-1576">Az.RecoveryServices</span></span>
* <span data-ttu-id="a6e72-1577">Для объекта AzureVMpolicy добавлен новый атрибут — ProtectedItemsCount.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1577">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="a6e72-1578">Добавлены тесты для политики виртуальной машины и восстановления исходной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1578">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e72-1579">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e72-1579">Az.Resources</span></span>
* <span data-ttu-id="a6e72-1580">Исправлена ошибка, при которой не удавалось вызвать командлет New-AzRoleAssignment без параметра Scope.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1580">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a6e72-1581">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a6e72-1581">Az.ServiceFabric</span></span>
* <span data-ttu-id="a6e72-1582">Исправлена опечатка в примере в справочной документации по командлету Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1582">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="a6e72-1583">Добавлены новые командлеты для управления приложениями и службами:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1583">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="a6e72-1584">New-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="a6e72-1584">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="a6e72-1585">New-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="a6e72-1585">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="a6e72-1586">New-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="a6e72-1586">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="a6e72-1587">New-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="a6e72-1587">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="a6e72-1588">Update-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="a6e72-1588">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="a6e72-1589">Get-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="a6e72-1589">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="a6e72-1590">Get-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="a6e72-1590">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="a6e72-1591">Get-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="a6e72-1591">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="a6e72-1592">Get-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="a6e72-1592">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="a6e72-1593">Remove-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="a6e72-1593">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="a6e72-1594">Remove-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="a6e72-1594">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="a6e72-1595">Remove-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="a6e72-1595">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="a6e72-1596">Remove-AzServiceFabricServic.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1596">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="a6e72-1597">Пакет SDK для Service Fabric обновлен до версии 1.2.0, в которой используется версия API 2019-03-01 поставщика ресурсов Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1597">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a6e72-1598">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a6e72-1598">Az.SignalR</span></span>
* <span data-ttu-id="a6e72-1599">Добавлены командлеты Update, Restart, CheckNameAvailability и GetUsage.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1599">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e72-1600">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e72-1600">Az.Sql</span></span>
* <span data-ttu-id="a6e72-1601">Обновлен пример в справочной документации по командлету Get-AzSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1601">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="a6e72-1602">Добавлен пример виртуального ядра для командлета создания эластичного пула (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="a6e72-1602">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="a6e72-1603">Удалена проверка свойства EmailAddresses и того, что свойство EmailAdmins правильное в случае, если свойство EmailAddresses пустое в командлетах Set-AzSqlServerAdvancedThreatProtectionPolicy и Set-AzSqlDatabaseAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1603">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="a6e72-1604">Теперь, если существует несколько параметров диагностики, включающих категорию аудита, параметры аудита сервера и базы данных удаляются.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1604">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="a6e72-1605">Исправлена проверка адресов электронной почты в нескольких командлетах оценки уязвимостей SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting и Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="a6e72-1605">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a6e72-1606">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6e72-1606">Az.Storage</span></span>
* <span data-ttu-id="a6e72-1607">Обновлен пример в справочной документации по командлету Get-AzStorageAccountKey.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1607">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="a6e72-1608">Теперь при отправке и загрузке файла Azure в конечном файле сохраняются свойства SMB исходного файла (атрибуты файла, время создания файла, время последней записи файла).</span><span class="sxs-lookup"><span data-stu-id="a6e72-1608">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="a6e72-1609">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a6e72-1609">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="a6e72-1610">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a6e72-1610">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="a6e72-1611">Исправлена операция отправки блочного BLOB-объекта, в которой происходили сбои свойств и метаданных в контейнере с включенной ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1611">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="a6e72-1612">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a6e72-1612">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="a6e72-1613">Добавлена поддержка управления общими папками Azure в API плоскости управления с помощью таких командлетов:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1613">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="a6e72-1614">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="a6e72-1614">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="a6e72-1615">Get-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="a6e72-1615">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="a6e72-1616">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="a6e72-1616">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="a6e72-1617">Remove-AzRmStorageShare.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1617">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a6e72-1618">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6e72-1618">Az.Websites</span></span>
* <span data-ttu-id="a6e72-1619">Устранена проблема, из-за которой теги webapp удалялись при переносе приложения в новый ASP.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1619">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="a6e72-1620">Теперь командлет Publish-AzureWebapp работает в Linux и Windows.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1620">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="a6e72-1621">Обновлен пример в справочной документации по командлету Get-AzWebAppPublishingProfile.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1621">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="a6e72-1622">2.6.0 — август 2019 г.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1622">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="a6e72-1623">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="a6e72-1623">General</span></span>
* <span data-ttu-id="a6e72-1624">Исправлены опечатки в модулях.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1624">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a6e72-1625">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e72-1625">Az.Accounts</span></span>
* <span data-ttu-id="a6e72-1626">Добавлена поддержка назначаемого пользователем удостоверения MSI при проверке подлинности в Функциях Azure (№ 9479).</span><span class="sxs-lookup"><span data-stu-id="a6e72-1626">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="a6e72-1627">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a6e72-1627">Az.Aks</span></span>
* <span data-ttu-id="a6e72-1628">Устранена проблема с выходными данными для Get-AzAks.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1628">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="a6e72-1629">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9847.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1629">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a6e72-1630">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a6e72-1630">Az.ApiManagement</span></span>
* <span data-ttu-id="a6e72-1631">исправлена проблема https://github.com/Azure/azure-powershell/issues/9351.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1631">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="a6e72-1632">Обновлена версия NuGet для .NET, которая не накладывает ограничений на productId, apiId, groupId и userId.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1632">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="a6e72-1633">**Get-AzApiManagementProduct**. Добавлена поддержка запросов к продуктам с помощью API.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1633">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="a6e72-1634">**New-AzApiManagementApiRevision**. Устранена проблема, из-за которой не задавался параметр ApiRevisionDescription при создании новой редакции API https://github.com/Azure/azure-powershell/issues/9752.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1634">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="a6e72-1635">Исправлено написание имени модели c PsApiManagementOAuth2AuthrozationServer на PsApiManagementOAuth2AuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1635">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a6e72-1636">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a6e72-1636">Az.Batch</span></span>
* <span data-ttu-id="a6e72-1637">Исправлена опечатка в написании Windows со строчной буквы в справочных сообщениях и документации.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1637">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a6e72-1638">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a6e72-1638">Az.Cdn</span></span>
* <span data-ttu-id="a6e72-1639">Исправлена опечатка во вспомогательном приложении модуля CDN.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1639">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e72-1640">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e72-1640">Az.Compute</span></span>
* <span data-ttu-id="a6e72-1641">Добавлен параметр VmssId в новый командлет Add New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1641">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="a6e72-1642">Добавлены параметры TerminateScheduledEvents и TerminateScheduledEventNotBeforeTimeoutInMinutes в New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1642">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="a6e72-1643">Добавлено свойство HyperVGeneration в объект образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1643">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="a6e72-1644">Добавлены компоненты Host и HostGroup.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1644">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="a6e72-1645">Новые командлеты:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="a6e72-1645">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="a6e72-1646">Параметр HostId добавлен в New-AzVMConfig и New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1646">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="a6e72-1647">Исправлен пример в документации по Invoke-AzVMRunCommand, в котором теперь используется правильное имя параметра.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1647">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="a6e72-1648">Исправлено описание VolumeType в справочной документации по Set-AzVMDiskEncryptionExtension и Set-AzVmssDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1648">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a6e72-1649">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a6e72-1649">Az.DataFactory</span></span>
* <span data-ttu-id="a6e72-1650">Исправлена опечатка в написании Windows со строчной буквы в документации по New-AzDataFactoryEncryptValue.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1650">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="a6e72-1651">Пакет SDK ADF для .NET обновлен до версии 4.1.2.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1651">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="a6e72-1652">Добавлены параметры DataProxyIntegrationRuntimeName, DataProxyStagingLinkedServiceName и DataProxyStagingPath в командлет Set-AzureRmDataFactoryV2IntegrationRuntime, что позволяет настраивать локальную среду выполнения интеграции в качестве прокси-сервера для Azure-SSIS Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1652">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="a6e72-1653">Обновлены PSTriggerRun для отображения активированных конвейеров, сообщений и свойств и PSActivityRun для отображения типа действия.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1653">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a6e72-1654">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a6e72-1654">Az.DataLakeStore</span></span>
* <span data-ttu-id="a6e72-1655">Устранена проблема, при которой Get-DataLakeStoreDeletedItem переставал отвечать на запросы при возникновении ошибок или удаленных исключений.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1655">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a6e72-1656">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a6e72-1656">Az.EventHub</span></span>
* <span data-ttu-id="a6e72-1657">Исправлена проблема № 9658: опечатка в написании параметра VirtualNteworkRule у Set-AzEventHubNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1657">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="a6e72-1658">Исправлена проблема № 9558: в Set-AzEventHubNamespace используется PATCH вместо PUT.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1658">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="a6e72-1659">В командлет Set-AzEventHubNamespace добавлен параметр EnableKafka.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1659">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="a6e72-1660">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1660">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="a6e72-1661">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="a6e72-1661">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="a6e72-1662">Исправлено написание Azure со строчной буквы.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1662">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a6e72-1663">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a6e72-1663">Az.Monitor</span></span>
* <span data-ttu-id="a6e72-1664">Исправлены неправильные имена параметров в справочной документации.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1664">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e72-1665">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e72-1665">Az.Network</span></span>
* <span data-ttu-id="a6e72-1666">Обновлен New-AzPrivateLinkServiceIpConfig.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1666">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="a6e72-1667">Параметр PublicIpAddress объявлен нерекомендуемым, так как он не используется на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1667">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="a6e72-1668">Добавлен необязательный параметр Primary, указывающий, является ли текущая IP-конфигурация основной.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1668">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="a6e72-1669">Улучшена обработка исключений из-за ошибок запроса от пакета SDK. Устранена проблема, при которой исключения пакета SDK не обрабатывались правильно, из-за чего не отображались основные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1669">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="a6e72-1670">Настроена логика проверки для префикса IPv6 IP-адреса для проверки правильности длины префикса IPv6.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1670">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="a6e72-1671">Обновлен Get-AzVirtualNetworkSubnetConfig: добавлен набор параметров для получения по идентификатору ресурса подсети.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1671">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="a6e72-1672">Обновлено описание параметра Location для AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1672">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a6e72-1673">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a6e72-1673">Az.OperationalInsights</span></span>
* <span data-ttu-id="a6e72-1674">Обновлена документация по New-AzOperationalInsightsLinuxSyslogDataSource.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1674">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="a6e72-1675">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1675">Added example</span></span>
    - <span data-ttu-id="a6e72-1676">Обновлено описание параметра -Name.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1676">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="a6e72-1677">Добавлен пример для New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="a6e72-1677">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="a6e72-1678">Изменено описание параметра -Name для New-AzOperationalInsightsWindowsEventDataSource.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1678">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a6e72-1679">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-1679">Az.RecoveryServices</span></span>
* <span data-ttu-id="a6e72-1680">Обновлен Get-AzRecoveryServicesBackupJobDetail.md.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1680">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e72-1681">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e72-1681">Az.Resources</span></span>
* <span data-ttu-id="a6e72-1682">Добавлена поддержка новой версии API 2019-05-10 для Microsoft.Resource.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1682">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="a6e72-1683">Добавлена поддержка copy.count = 0 для переменных, ресурсов и свойств.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1683">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="a6e72-1684">Ресурсы, у которых condition = false или copy.count = 0, будут удаляться в полном режиме.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1684">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="a6e72-1685">В справочную документацию добавлен пример назначения политики на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1685">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a6e72-1686">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a6e72-1686">Az.ServiceBus</span></span>
* <span data-ttu-id="a6e72-1687">Исправлена проблема № 9658: опечатка в написании параметра VirtualNetworkRule В Set-AzServiceBusNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1687">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="a6e72-1688">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1688">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="a6e72-1689">Добавлена новая команда Test-AzServiceBusNameAvailability для проверки доступности имени для очереди и раздела.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1689">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a6e72-1690">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a6e72-1690">Az.ServiceFabric</span></span>
* <span data-ttu-id="a6e72-1691">Устранены ошибки командлета для добавления типа узла:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1691">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="a6e72-1692">ошибка NullReferenceException, возникавшая, если у группы ресурсов были другие VMSS, не связанные с кластером Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1692">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="a6e72-1693">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8681.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1693">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="a6e72-1694">Исправлена ошибка, из-за которой командлет завершился сбоем, если virtualNetwork находилась не в той группе ресурсов, к которой относится кластер.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1694">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="a6e72-1695">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8407.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1695">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="a6e72-1696">Командлет Add-AzServiceFabricApplicationCertificate объявлен нерекомендуемым.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1696">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e72-1697">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e72-1697">Az.Sql</span></span>
* <span data-ttu-id="a6e72-1698">Обновление документации по старым командлетам аудита.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1698">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a6e72-1699">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6e72-1699">Az.Storage</span></span>
* <span data-ttu-id="a6e72-1700">Обновлена справка по Get/Close-AzStorageFileHandle: в примеры добавлены сценарии использования командлетов и обновлено описание параметров.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1700">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="a6e72-1701">Добавлена поддержка StandardBlobTier в операции отправки BLOB-объекта и копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1701">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="a6e72-1702">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a6e72-1702">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="a6e72-1703">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a6e72-1703">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="a6e72-1704">Добавлена поддержка приоритета восстановления в операцию копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1704">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="a6e72-1705">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a6e72-1705">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a6e72-1706">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6e72-1706">Az.Websites</span></span>
* <span data-ttu-id="a6e72-1707">Добавлены уточнение для параметра -AppSettings в Set-AzWebApp и Set-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1707">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="a6e72-1708">2.5.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1708">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a6e72-1709">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e72-1709">Az.Accounts</span></span>
* <span data-ttu-id="a6e72-1710">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1710">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="a6e72-1711">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="a6e72-1711">Az.ApplicationInsights</span></span>
* <span data-ttu-id="a6e72-1712">Исправлена опечатка в примере в документации по Remove-AzApplicationInsightsApiKey.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1712">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a6e72-1713">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a6e72-1713">Az.Automation</span></span>
* <span data-ttu-id="a6e72-1714">Исправлена опечатка в строке ресурса.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1714">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a6e72-1715">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-1715">Az.CognitiveServices</span></span>
* <span data-ttu-id="a6e72-1716">Добавлена поддержка NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1716">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e72-1717">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e72-1717">Az.Compute</span></span>
* <span data-ttu-id="a6e72-1718">Добавлены недостающие свойства (ComputerName, OsName, OsVersion и HyperVGeneration) для объекта представления экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1718">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="a6e72-1719">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a6e72-1719">Az.ContainerRegistry</span></span>
* <span data-ttu-id="a6e72-1720">Исправлена опечатка в Remove-AzContainerRegistryReplication для параметра репликации.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1720">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="a6e72-1721">См. подробнее: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1721">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a6e72-1722">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a6e72-1722">Az.DataFactory</span></span>
* <span data-ttu-id="a6e72-1723">Пакет SDK для ADF .NET обновлен до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1723">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="a6e72-1724">Исправлена опечатка в документации по Get-AzDataFactoryV2PipelineRun.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1724">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a6e72-1725">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a6e72-1725">Az.EventHub</span></span>
* <span data-ttu-id="a6e72-1726">Добавлен новый командлет для создания маркера SAS: New-AzEventHubAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1726">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="a6e72-1727">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="a6e72-1727">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a6e72-1728">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a6e72-1728">Az.KeyVault</span></span>
* <span data-ttu-id="a6e72-1729">Добавлена поддержка для настройки параметра KeySize в политиках сертификатов.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1729">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a6e72-1730">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a6e72-1730">Az.LogicApp</span></span>
* <span data-ttu-id="a6e72-1731">Get-AzIntegrationAccountMap теперь надлежащим образом выводит все типы сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1731">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="a6e72-1732">Добавлен новый параметр MapType для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1732">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="a6e72-1733">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-1733">Az.ManagedServices</span></span>
* <span data-ttu-id="a6e72-1734">Добавлена поддержка API версии 2019-06-01 (общедоступная).</span><span class="sxs-lookup"><span data-stu-id="a6e72-1734">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e72-1735">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e72-1735">Az.Network</span></span>
* <span data-ttu-id="a6e72-1736">Добавлена поддержка частной конечной точки и службы приватного канала.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1736">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="a6e72-1737">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="a6e72-1737">New cmdlets</span></span>
        - <span data-ttu-id="a6e72-1738">Set-AzPrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1738">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="a6e72-1739">Set-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1739">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="a6e72-1740">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1740">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a6e72-1741">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1741">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a6e72-1742">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1742">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a6e72-1743">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1743">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a6e72-1744">Test-AzPrivateLinkServiceVisibility.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1744">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="a6e72-1745">Get-AzAutoApprovedPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1745">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="a6e72-1746">Обновлены следующие команды для функции: Флаг PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies в подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1746">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="a6e72-1747">Обновлены командлеты New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1747">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="a6e72-1748">Добавлен необязательный параметр -PrivateEndpointNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к частной конечной точке в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1748">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="a6e72-1749">Добавлен необязательный параметр -PrivateLinkServiceNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к службе приватного канала в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1749">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="a6e72-1750">Параметр ServiceName командлета AzPrivateLinkService был переименован на Name с псевдонимом ServiceName для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1750">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="a6e72-1751">Включен протокол ICMP для настройки правил безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1751">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="a6e72-1752">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="a6e72-1752">Updated cmdlets</span></span>
        - <span data-ttu-id="a6e72-1753">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1753">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="a6e72-1754">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1754">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="a6e72-1755">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1755">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="a6e72-1756">Добавлен ConnectionProtocolType (Ikev1/Ikev2) в качестве настраиваемого параметра для командлета New-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1756">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="a6e72-1757">Добавлен PrivateIpAddressVersion в LoadBalancerFrontendIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1757">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="a6e72-1758">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1758">Updated cmdlet:</span></span>
        - <span data-ttu-id="a6e72-1759">New-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1759">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="a6e72-1760">Add-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1760">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="a6e72-1761">Set-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1761">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="a6e72-1762">Команда New-AzApplicationGatewayProbeConfig Шлюза приложений обновлена для поддержки настраиваемого порта в зонде.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1762">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="a6e72-1763">Обновлен командлет New-AzApplicationGatewayProbeConfig: добавлен необязательный параметр Port, который используется при проверке внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1763">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="a6e72-1764">Этот параметр применяется к номерам SKU Standard_V2 и WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1764">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a6e72-1765">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a6e72-1765">Az.OperationalInsights</span></span>
* <span data-ttu-id="a6e72-1766">Обновленная версия по умолчанию для сохраненных операций поиска имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1766">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="a6e72-1767">Исправлены ошибки при обработке регулярных выражений со значениями NULL в журналах.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1767">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a6e72-1768">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-1768">Az.RecoveryServices</span></span>
* <span data-ttu-id="a6e72-1769">Обновлен файл Get-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1769">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="a6e72-1770">Обновлен файл Get-AzRecoveryServicesBackupContainer.md.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1770">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="a6e72-1771">Обновлен файл Get-AzRecoveryServicesVault.md.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1771">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="a6e72-1772">Обновлен файл Wait-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1772">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="a6e72-1773">Обновлен файл Set-AzRecoveryServicesVaultContext.md.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1773">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="a6e72-1774">Обновлен файл Get-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1774">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="a6e72-1775">Обновлен файл Get-AzRecoveryServicesBackupRecoveryPoint.md.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1775">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="a6e72-1776">Обновлен файл Restore-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1776">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="a6e72-1777">Обновлен вызов службы для отмены регистрации контейнера в общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1777">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="a6e72-1778">Обновлен файл Set-AzRecoveryServicesAsrAlertSetting.md.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1778">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e72-1779">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e72-1779">Az.Resources</span></span>
- <span data-ttu-id="a6e72-1780">Удален отсутствующий командлет, который упоминается в документации по New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1780">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="a6e72-1781">Обновлены командлеты политик для использования новой версии API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1781">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a6e72-1782">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a6e72-1782">Az.ServiceBus</span></span>
* <span data-ttu-id="a6e72-1783">Добавлен новый командлет для создания маркера SAS: New-AzServiceBusAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1783">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="a6e72-1784">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="a6e72-1784">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e72-1785">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e72-1785">Az.Sql</span></span>
* <span data-ttu-id="a6e72-1786">Исправлены отсутствующие примеры для командлета Set-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1786">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="a6e72-1787">Исправлены заданные повторяющиеся проверки для оценки наличия уязвимостей без указания адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1787">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="a6e72-1788">Исправлена незначительная опечатка в сообщении предупреждения.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1788">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a6e72-1789">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6e72-1789">Az.Storage</span></span>
* <span data-ttu-id="a6e72-1790">Обновлен пример в справочной документации для использования командлетом Get-AzStorageAccount правильного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1790">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="a6e72-1791">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="a6e72-1791">Az.StorageSync</span></span>
* <span data-ttu-id="a6e72-1792">Добавлен командлет Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1792">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="a6e72-1793">Исправлена проблема № 9551, связанная с TierFilesOlderThanDays.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1793">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a6e72-1794">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6e72-1794">Az.Websites</span></span>
* <span data-ttu-id="a6e72-1795">Исправлена ошибка, при которой некоторые свойства SiteConfig не возвращались Get-AzWebApp и Set-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1795">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="a6e72-1796">Добавлен новый параметр Location в Get-AzDeletedWebApp и Restore-AzDeletedWebApp.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1796">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="a6e72-1797">Исправлена ошибка, которая возникала при клонировании слотов веб-приложений с помощью командлета New-AzWebApp-IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1797">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="a6e72-1798">2.4.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1798">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a6e72-1799">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e72-1799">Az.Accounts</span></span>
* <span data-ttu-id="a6e72-1800">Добавлена поддержка командлетов профиля.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1800">Add support for profile cmdlets</span></span>
* <span data-ttu-id="a6e72-1801">Добавлена поддержка сред и плоскостей данных в созданных командлетах.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1801">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="a6e72-1802">Исправлена ошибка, когда в командлетах плоскости данных в Windows PowerShell в некоторых случаях использовалась неправильная конечная точка.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1802">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="a6e72-1803">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="a6e72-1803">Az.Advisor</span></span>
* <span data-ttu-id="a6e72-1804">Выпущена общедоступная версия Az.Advisor.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1804">GA release of Az.Advisor</span></span>
* <span data-ttu-id="a6e72-1805">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1805">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a6e72-1806">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a6e72-1806">Az.ApiManagement</span></span>
* <span data-ttu-id="a6e72-1807">исправлена проблема https://github.com/Azure/azure-powershell/issues/8671.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1807">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="a6e72-1808">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="a6e72-1808">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="a6e72-1809">Добавлена поддержка запрашивания подписок по пользователю и продукту.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1809">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="a6e72-1810">Добавлена поддержка создания запросов с использованием области "/", "/apis", "/apis/echo-api".</span><span class="sxs-lookup"><span data-stu-id="a6e72-1810">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="a6e72-1811">Исправлены проблемы https://github.com/Azure/azure-powershell/issues/9307 и https://github.com/Azure/azure-powershell/issues/8432.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1811">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="a6e72-1812">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="a6e72-1812">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="a6e72-1813">Добавлена поддержка указания ApiVersion и ApiVersionSetId при импорте API-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1813">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a6e72-1814">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a6e72-1814">Az.Automation</span></span>
* <span data-ttu-id="a6e72-1815">Исправлена ошибка командлета Set-AzAutomationConnectionFieldValue при обработке строкового значения.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1815">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e72-1816">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e72-1816">Az.Compute</span></span>
* <span data-ttu-id="a6e72-1817">В New AzImageConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1817">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a6e72-1818">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a6e72-1818">Az.DataFactory</span></span>
* <span data-ttu-id="a6e72-1819">Обновление выходных данных командлетов ADF, предназначенных для получения числа выполнений действий, конвейеров и триггеров, для поддержки канала Select-Object.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1819">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a6e72-1820">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a6e72-1820">Az.EventGrid</span></span>
* <span data-ttu-id="a6e72-1821">Исправлена опечатка в документации по командлету New-AzEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1821">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a6e72-1822">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a6e72-1822">Az.IotHub</span></span>
* <span data-ttu-id="a6e72-1823">Добавлена поддержка повторного создания ключей политики авторизации.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1823">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e72-1824">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e72-1824">Az.Network</span></span>
* <span data-ttu-id="a6e72-1825">К тегам общедоступного IP-адреса добавлен тег RoutingPreference.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1825">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="a6e72-1826">Улучшены примеры для справочной документации по командлету Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1826">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a6e72-1827">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a6e72-1827">Az.PolicyInsights</span></span>
* <span data-ttu-id="a6e72-1828">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1828">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="a6e72-1829">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9446.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1829">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a6e72-1830">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a6e72-1830">Az.OperationalInsights</span></span>
* <span data-ttu-id="a6e72-1831">Исправленная модель источника данных CustomLog возвращена в командлет Get-AzOperationalInsightsDataSource.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1831">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a6e72-1832">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-1832">Az.RecoveryServices</span></span>
* <span data-ttu-id="a6e72-1833">Выпущено исправление для команды get-policy для виртуальных машин IaaS.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1833">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e72-1834">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e72-1834">Az.Resources</span></span>
    - <span data-ttu-id="a6e72-1835">Исправлен текст справки по параметру Get-AzPolicyState -Top.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1835">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="a6e72-1836">Добавлена поддержка разбиения по страницам на стороне клиента для Get-AzPolicyAlias.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1836">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="a6e72-1837">Добавлены новые параметры для Set-AzPolicyAssignment, -PolicyParameters и -PolicyParametersObject.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1837">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="a6e72-1838">Добавлен ряд обновлений документов и примеров для командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1838">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a6e72-1839">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a6e72-1839">Az.ServiceBus</span></span>
* <span data-ttu-id="a6e72-1840">Исправление ошибки № 4938: командлет New-AzureRmServiceBusQueue возвращает ответ BadRequest (Недопустимый запрос) при задании значения MaxSizeInMegabytes.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1840">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e72-1841">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e72-1841">Az.Sql</span></span>
* <span data-ttu-id="a6e72-1842">Из выпуска предварительной версии в выпуск общедоступной версии добавлены командлеты группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1842">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="a6e72-1843">Поддержка аудита Azure SQL Server и баз данных с помощью новых командлетов:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1843">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="a6e72-1844">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="a6e72-1844">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="a6e72-1845">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="a6e72-1845">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="a6e72-1846">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="a6e72-1846">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="a6e72-1847">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="a6e72-1847">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="a6e72-1848">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="a6e72-1848">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="a6e72-1849">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="a6e72-1849">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="a6e72-1850">Из параметров оценки уязвимостей удалены ограничения, касающиеся электронной почты.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1850">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a6e72-1851">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6e72-1851">Az.Storage</span></span>
* <span data-ttu-id="a6e72-1852">Два параметра в указанном ниже командлете — -IndexDocument и -ErrorDocument404Path, — которые ранее были обязательными, стали необязательными:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1852">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="a6e72-1853">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="a6e72-1853">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="a6e72-1854">Обновлена справка по командлету Get-AzStorageBlobContent: добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1854">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="a6e72-1855">При сбое выполнения командлета с ошибкой StorageException отображаются дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1855">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="a6e72-1856">Добавлена поддержка создания или обновления учетной записи хранения с использованием проверки подлинности AAD DS для службы "Файлы Azure".</span><span class="sxs-lookup"><span data-stu-id="a6e72-1856">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="a6e72-1857">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a6e72-1857">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="a6e72-1858">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a6e72-1858">Set-AzStorageAccount</span></span>
* <span data-ttu-id="a6e72-1859">Добавлена поддержка перечисления или закрытия дескрипторов файлов для общей папки, каталога файлов или файла:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1859">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="a6e72-1860">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="a6e72-1860">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="a6e72-1861">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="a6e72-1861">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="a6e72-1862">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="a6e72-1862">Az.StorageSync</span></span>
* <span data-ttu-id="a6e72-1863">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1863">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="a6e72-1864">2.3.2 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1864">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a6e72-1865">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e72-1865">Az.Accounts</span></span>
* <span data-ttu-id="a6e72-1866">Исправлена ошибка, связанная с использованием неправильного URL-адреса для вызовов функций.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1866">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="a6e72-1867">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8983.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1867">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="a6e72-1868">Устранена проблема с псевдонимами из AzureRM для командлетов Az.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1868">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="a6e72-1869">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1869">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="a6e72-1870">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1870">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e72-1871">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e72-1871">Az.Compute</span></span>
* <span data-ttu-id="a6e72-1872">Простые наборы параметров New-AzVm и New-AzVmss теперь принимают параметр ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1872">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="a6e72-1873">Исправлена опечатка в справочной документации по New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1873">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="a6e72-1874">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="a6e72-1874">Az.Dns</span></span>
* <span data-ttu-id="a6e72-1875">Исправлена опечатка в справочных примерах по использованию Set-AzDnsZone.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1875">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a6e72-1876">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a6e72-1876">Az.EventGrid</span></span>
* <span data-ttu-id="a6e72-1877">Обновлен для использования API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1877">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="a6e72-1878">Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1878">New cmdlets:</span></span>
    - <span data-ttu-id="a6e72-1879">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="a6e72-1879">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="a6e72-1880">Создает домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1880">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="a6e72-1881">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="a6e72-1881">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="a6e72-1882">Возвращает сведения о домене Сетки событий или список всех доменов Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1882">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="a6e72-1883">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="a6e72-1883">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="a6e72-1884">Удаляет домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1884">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="a6e72-1885">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="a6e72-1885">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="a6e72-1886">Повторно создает ключ общего доступа для домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1886">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="a6e72-1887">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="a6e72-1887">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="a6e72-1888">Возвращает ключи общего доступа, используемые для публикации событий в домене Сетки событий.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1888">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="a6e72-1889">New-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="a6e72-1889">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="a6e72-1890">Создает раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1890">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="a6e72-1891">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="a6e72-1891">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="a6e72-1892">Возвращает сведения о разделе домена Сетки событий или список всех разделов определенного домена Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1892">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="a6e72-1893">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="a6e72-1893">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="a6e72-1894">Удаляет раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1894">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="a6e72-1895">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1895">Updated cmdlets:</span></span>
    - <span data-ttu-id="a6e72-1896">New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="a6e72-1896">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="a6e72-1897">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для нового домена Сетки событий и раздела домена Сетки событий и позволяющие создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1897">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="a6e72-1898">Добавляют новые обязательные параметры для указания имени нового домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1898">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="a6e72-1899">Добавляют новые наборы параметров для доменов и разделов домена и позволяют повторно использовать существующие параметры (например, EndPointType, SubjectBeginsWith и т. д.).</span><span class="sxs-lookup"><span data-stu-id="a6e72-1899">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="a6e72-1900">Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1900">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="a6e72-1901">срока действия подписки на событие;</span><span class="sxs-lookup"><span data-stu-id="a6e72-1901">Event subscription expiration date,</span></span>
            - <span data-ttu-id="a6e72-1902">параметров расширенной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1902">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="a6e72-1903">Добавляют новое перечисление для ServiceBusQueue в качестве места назначения.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1903">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="a6e72-1904">Запрещают использование значение All в параметре -IncludedEventType и заменяют его следующим:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1904">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="a6e72-1905">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="a6e72-1905">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="a6e72-1906">Добавляют новые необязательные параметры (Top, ODataQuery и NextLink) для поддержки разбиения на страницы и фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1906">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="a6e72-1907">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="a6e72-1907">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="a6e72-1908">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для домена Сетки событий и раздела домена Сетки событий и позволяющие удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1908">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="a6e72-1909">Добавляют новые обязательные параметры для указания имени домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1909">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a6e72-1910">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a6e72-1910">Az.FrontDoor</span></span>
* <span data-ttu-id="a6e72-1911">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="a6e72-1911">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="a6e72-1912">Добавляет поддержку преобразований и новое значение оператора автозавершения (RegEx).</span><span class="sxs-lookup"><span data-stu-id="a6e72-1912">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="a6e72-1913">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="a6e72-1913">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="a6e72-1914">Добавляет новые значения автозавершения.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1914">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e72-1915">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e72-1915">Az.Network</span></span>
* <span data-ttu-id="a6e72-1916">Добавляет поддержку ресурса шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1916">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="a6e72-1917">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="a6e72-1917">New cmdlets</span></span>
        - <span data-ttu-id="a6e72-1918">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="a6e72-1918">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="a6e72-1919">Добавляет AvailablePrivateEndpointType.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1919">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="a6e72-1920">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="a6e72-1920">New cmdlets</span></span>
        - <span data-ttu-id="a6e72-1921">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="a6e72-1921">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="a6e72-1922">Добавляет PrivatePrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1922">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="a6e72-1923">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="a6e72-1923">New cmdlets</span></span>
        - <span data-ttu-id="a6e72-1924">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a6e72-1924">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="a6e72-1925">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a6e72-1925">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="a6e72-1926">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a6e72-1926">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="a6e72-1927">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a6e72-1927">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="a6e72-1928">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a6e72-1928">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="a6e72-1929">Добавляет PrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1929">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="a6e72-1930">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="a6e72-1930">New cmdlets</span></span>
        - <span data-ttu-id="a6e72-1931">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a6e72-1931">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="a6e72-1932">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a6e72-1932">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="a6e72-1933">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a6e72-1933">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="a6e72-1934">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="a6e72-1934">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="a6e72-1935">Обновлены следующие команды для функции: флаг UseLocalAzureIpAddress для VPN-подключения.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1935">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="a6e72-1936">Обновлен командлет New-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1936">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="a6e72-1937">Обновлен командлет Set-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1937">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="a6e72-1938">В пиринг ExpressRoute добавлено поле только для чтения PeeredConnections.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1938">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="a6e72-1939">В ExpressRoute добавлено поле только для чтения GlobalReachEnabled.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1939">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="a6e72-1940">Добавлен атрибут в рамках критического изменения, отменяющего статус устаревшего поля AllowGlobalReach в модели ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1940">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="a6e72-1941">Исправлена проблема, связанная с ошибкой 8756, при использовании TargetListenerID с командлетами AzApplicationGatewayRedirectConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1941">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="a6e72-1942">Исправлена ошибка в New-AzApplicationGatewayPathRuleConfig, не позволявшая задавать набор правил повторного создания.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1942">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="a6e72-1943">Исправлено отображение VirtualNetworkTaps в NetworkInterfaceIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1943">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="a6e72-1944">Исправлены командлеты Cortex Get для отображения всех частей.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1944">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="a6e72-1945">Исправлено создание ссылок VirtualHub для ExpressRouteGateways и VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1945">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="a6e72-1946">В AzureFirewall и NatGateway добавлена поддержка Зон доступности.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1946">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="a6e72-1947">Добавлен командлет Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1947">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="a6e72-1948">Добавлена поддержка нескольких общедоступных IP-адресов для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1948">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="a6e72-1949">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="a6e72-1949">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="a6e72-1950">Добавлен параметр -PublicIpAddress, который принимает один или несколько объектов общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1950">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="a6e72-1951">Добавлен параметр -VirtualNetwork, который принимает объект виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1951">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="a6e72-1952">Добавлены методы AddPublicIpAddress и RemovePublicIpAddress для объекта брандмауэра. Они принимают объект общедоступного IP-адреса в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1952">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="a6e72-1953">Не рекомендуется использовать параметры -PublicIpName и -VirtualNetworkName.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1953">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="a6e72-1954">Обновлены следующие команды для функции: В параметрах проверки подлинности AAD VPN-клиента задан ресурс шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1954">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="a6e72-1955">Обновлен командлет New-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1955">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="a6e72-1956">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1956">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="a6e72-1957">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр-переключатель RemoveAadAuthentication для удаления в шлюзе параметров проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1957">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a6e72-1958">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a6e72-1958">Az.OperationalInsights</span></span>
* <span data-ttu-id="a6e72-1959">Добавлена поддержка SKU **pergb2018** в команде New-AzureRmOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1959">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e72-1960">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e72-1960">Az.Resources</span></span>
* <span data-ttu-id="a6e72-1961">Поддержка дополнительных вариантов экспорта шаблона.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1961">Support for additional Template Export options</span></span>
    - <span data-ttu-id="a6e72-1962">В Export-AzResourceGroup добавлен параметр -SkipResourceNameParameterization.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1962">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="a6e72-1963">В Export-AzResourceGroup добавлен параметр -SkipAllParameterization.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1963">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="a6e72-1964">В Export-AzResourceGroup добавлен параметр -Resource для фильтрации экспортированных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1964">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a6e72-1965">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a6e72-1965">Az.ServiceFabric</span></span>
* <span data-ttu-id="a6e72-1966">Исправлена ошибка, связанная с получением иногда неправильных отпечатков при добавлении сертификата ByExistingKeyVault.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1966">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e72-1967">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e72-1967">Az.Sql</span></span>
* <span data-ttu-id="a6e72-1968">Исправлен суффикс конечной точки хранилища службы "Расширенная защита от угроз Azure".</span><span class="sxs-lookup"><span data-stu-id="a6e72-1968">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="a6e72-1969">Исправлена ошибка, связанная с возможностью пакета "Расширенная защита данных" переопределять политику службы "Расширенная защита от угроз".</span><span class="sxs-lookup"><span data-stu-id="a6e72-1969">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="a6e72-1970">Новые командлеты для Management.Sql позволяют клиентам добавлять ключи TDE и задавать средство защиты TDE для управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1970">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="a6e72-1971">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a6e72-1971">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="a6e72-1972">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a6e72-1972">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="a6e72-1973">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a6e72-1973">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="a6e72-1974">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="a6e72-1974">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="a6e72-1975">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="a6e72-1975">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a6e72-1976">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6e72-1976">Az.Storage</span></span>
* <span data-ttu-id="a6e72-1977">Поддержка класса Kind в FileStorage и значения Premium_ZRS в SkuName при создании учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1977">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="a6e72-1978">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a6e72-1978">New-AzStorageAccount</span></span>
* <span data-ttu-id="a6e72-1979">Уточнено описание командлета неизменности BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1979">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="a6e72-1980">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a6e72-1980">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a6e72-1981">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6e72-1981">Az.Websites</span></span>
* <span data-ttu-id="a6e72-1982">Оптимизирует Get-AzWebAppCertificate для фильтрации по группе ресурсов на сервере, а не в клиенте.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1982">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="a6e72-1983">Добавляет параметр-переключатель - UseDisasterRecovery в Get AzWebAppSnapshot.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1983">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="a6e72-1984">2.2.0 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1984">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="a6e72-1985">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a6e72-1985">Az.Cdn</span></span>
* <span data-ttu-id="a6e72-1986">Обновлены командлеты для поддержки функции rulesEngine на основе API версии 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1986">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e72-1987">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e72-1987">Az.Compute</span></span>
* <span data-ttu-id="a6e72-1988">Добавлен параметр `NoWait`, который запускает операцию и немедленно возвращает значение еще до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1988">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="a6e72-1989">Обновлены командлеты:   Export-AzLogAnalyticRequestRateByInterval; Export-AzLogAnalyticThrottledRequest; Remove-AzVM; Remove-AzVMAccessExtension; Remove-AzVMAEMExtension; Remove-AzVMChefExtension; Remove-AzVMCustomScriptExtension; Remove-AzVMDiagnosticsExtension; Remove-AzVMDiskEncryptionExtension; Remove-AzVMDscExtension; Remove-AzVMSqlServerExtension; Restart-AzVM; Set-AzVM; Set-AzVMAccessExtension; Set-AzVMADDomainExtension; Set-AzVMAEMExtension; Set-AzVMBginfoExtension; Set-AzVMChefExtension; Set-AzVMCustomScriptExtension; Set-AzVMDiagnosticsExtension; Set-AzVMDscExtension; Set-AzVMExtension; Start-AzVM; Stop-AzVM; Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1989">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a6e72-1990">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a6e72-1990">Az.EventHub</span></span>
* <span data-ttu-id="a6e72-1991">Исправлена ошибка № 9231. Командлет Get-AzEventHubNamespace не возвращал теги.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1991">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="a6e72-1992">Исправлена ошибка № 9230. Командлет Get-AzEventHubNamespace возвращал значение ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1992">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e72-1993">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e72-1993">Az.Network</span></span>
* <span data-ttu-id="a6e72-1994">Обновлены параметры ResourceId и InputObject для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1994">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="a6e72-1995">Добавлены псевдонимы для параметров ResourceId и InputObject.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1995">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a6e72-1996">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a6e72-1996">Az.PolicyInsights</span></span>
* <span data-ttu-id="a6e72-1997">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyEvent.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1997">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a6e72-1998">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-1998">Az.RecoveryServices</span></span>
* <span data-ttu-id="a6e72-1999">Минимальный срок хранения политики IaaSVM изменился с 1 до 7 дней.</span><span class="sxs-lookup"><span data-stu-id="a6e72-1999">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a6e72-2000">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a6e72-2000">Az.ServiceBus</span></span>
* <span data-ttu-id="a6e72-2001">Исправлена ошибка № 9182. Командлет Get-AzServiceBusNamespace возвращал ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2001">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a6e72-2002">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a6e72-2002">Az.ServiceFabric</span></span>
* <span data-ttu-id="a6e72-2003">Исправлена опечатка в сообщении об ошибке для командлета Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2003">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="a6e72-2004">Добавлен отсутствующий символ в командных строках Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2004">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e72-2005">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e72-2005">Az.Sql</span></span>
* <span data-ttu-id="a6e72-2006">Для командлета New-AzureSqlInstance добавлен параметр DnsZonePartner, обеспечивающий поддержку AutoDr для Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2006">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="a6e72-2007">Командлет Get-AzSqlDatabaseSecureConnectionPolicy объявлен неподдерживаемым.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2007">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="a6e72-2008">Командлеты обнаружения угроз переименованы в командлеты Расширенной защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2008">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="a6e72-2009">Параметры -StorageSizeInGB и -LicenseType командлета New-AzSqlInstance теперь необязательны.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2009">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a6e72-2010">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6e72-2010">Az.Websites</span></span>
* <span data-ttu-id="a6e72-2011">Исправлены проблемы, когда удалялись теги при использовании Set-AzWebApp и Set-AzWebAppSlot со свойством -WebApp.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2011">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="a6e72-2012">2.1.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2012">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="a6e72-2013">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a6e72-2013">Az.ApiManagement</span></span>
* <span data-ttu-id="a6e72-2014">Созданы командлеты для управления диагностикой в глобальной области и в области API.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2014">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="a6e72-2015">**Get-AzApiManagementDiagnostic** — получение диагностики, заданной глобально или на уровне области API.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2015">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="a6e72-2016">**New-AzApiManagementDiagnostic** — создание диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2016">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="a6e72-2017">**New-AzApiManagementHttpMessageDiagnostic** — создание параметра диагностики, для которого регистрируются заголовки и размер байтов тела.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2017">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="a6e72-2018">**New-AzApiManagementPipelineDiagnosticSetting** — создание параметров диагностики для сообщений HTTP, поступающих в шлюз или исходящих из него.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2018">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="a6e72-2019">**New-AzApiManagementSamplingSetting** — создание параметра выборки для запросов и ответов касательно диагностики.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2019">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="a6e72-2020">**Remove-AzApiManagementDiagnostic** — удаление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2020">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="a6e72-2021">**Set-AzApiManagementDiagnostic** — обновление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2021">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="a6e72-2022">Созданы командлеты для управления кэшем в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2022">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="a6e72-2023">**Get-AzApiManagementCache** — получение сведений о кэше, указанном идентификатором, или обо всех кэшах.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2023">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="a6e72-2024">**New-AzApiManagementCache** — создание кэша по умолчанию или кэша в определенном регионе Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2024">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="a6e72-2025">**Remove-AzApiManagementCache** — удаление кэша.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2025">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="a6e72-2026">**Update-AzApiManagementCache** — обновление кэша.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2026">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="a6e72-2027">Созданы командлеты для управления схемой API.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2027">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="a6e72-2028">**New-AzApiManagementSchema** — создание схемы для API.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2028">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="a6e72-2029">**Get-AzApiManagementSchema** — получение схем, настроенных в API.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2029">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="a6e72-2030">**Remove-AzApiManagementSchema** — удаление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2030">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="a6e72-2031">**Set-AzApiManagementSchema** — обновление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2031">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="a6e72-2032">Создан командлет для создания токена пользователя.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2032">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="a6e72-2033">**New-AzApiManagementUserToken** — создание токена пользователя, по умолчанию действительного в течение 8 часов. С помощью этого командлета можно создавать токен для пользователя GIT.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2033">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="a6e72-2034">Создан командлет для получения состояния сети.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2034">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="a6e72-2035">**Get-AzApiManagementNetworkStatus** — получение состояния подключения сети ресурсов, от которых зависит служба "Управление API".</span><span class="sxs-lookup"><span data-stu-id="a6e72-2035">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="a6e72-2036">Это полезно при развертывании службы ApiManagement в виртуальной сети и проверке того, не нарушена ли какая-либо из зависимостей.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2036">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="a6e72-2037">Обновлен командлет **New-AzApiManagement** для управления службой ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2037">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="a6e72-2038">Добавлена поддержка нового SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2038">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="a6e72-2039">Добавлена поддержка для включения флага EnableClientCertificate в SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2039">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="a6e72-2040">Новый командлет **New-AzApiManagementSslSetting** позволяет настраивать параметр TLS/SSL для сервера (Backend) и внешнего интерфейса (Frontend).</span><span class="sxs-lookup"><span data-stu-id="a6e72-2040">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="a6e72-2041">Его также можно использовать для настройки Ciphers как 3DES, в ServerProtocols как Http2 для внешнего интерфейса (Frontend) службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2041">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="a6e72-2042">Добавлена поддержка настройки имени узла DeveloperPortal в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2042">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="a6e72-2043">Обновлен командлет **Get-AzApiManagementSsoToken** для извлечения объекта PsApiManagement в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2043">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="a6e72-2044">Обновлен командлет для отображения встроенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2044">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="a6e72-2045">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Код ошибки: ValidationError. Сообщение об ошибке: "Некоторые поля содержат неправильные значения". Сведения об ошибке: [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="a6e72-2045">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="a6e72-2046">Обновлен командлет **Export-AzApiManagementApi** для экспортирования программных интерфейсов в формате OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2046">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="a6e72-2047">Обновлен командлет **Import-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="a6e72-2047">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="a6e72-2048">Для импортирования API из спецификации документа OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2048">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="a6e72-2049">Для переопределения свойства PsApiManagementSchema, указанного в любом документе (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="a6e72-2049">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="a6e72-2050">Для переопределения свойства ServiceUrl, указанного в любом документе.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2050">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="a6e72-2051">Обновлен командлет **Get-AzApiManagementPolicy** для возврата политики в формате, экранированном не для XML, с использованием rawxml.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2051">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="a6e72-2052">Обновлен командлет **Set-AzApiManagementPolicy**. Он принимает политику в формате, экранированном не для XML, с использованием rawxml и в формате, экранированном для XML, с использованием XML.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2052">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="a6e72-2053">Обновлен командлет **New-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="a6e72-2053">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="a6e72-2054">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2054">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="a6e72-2055">Для создания API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2055">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="a6e72-2056">Для клонирования API с использованием значений SourceApiId и SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2056">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="a6e72-2057">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2057">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="a6e72-2058">Обновлен командлет **Set-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="a6e72-2058">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="a6e72-2059">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2059">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="a6e72-2060">Для обновления API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2060">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="a6e72-2061">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2061">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="a6e72-2062">Обновлен командлет **New-AzApiManagementRevision**:</span><span class="sxs-lookup"><span data-stu-id="a6e72-2062">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="a6e72-2063">Для клонирования (копирования тегов, продуктов, операций и политик) существующей редакции с использованием SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2063">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="a6e72-2064">Новая редакция предполагает родительский идентификатор ApiId.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2064">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="a6e72-2065">Для предоставления ApiRevisionDescription.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2065">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="a6e72-2066">Для переопределения значения ServiceUrl при клонировании API.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2066">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="a6e72-2067">Обновлен командлет **New-AzApiManagementIdentityProvider**:</span><span class="sxs-lookup"><span data-stu-id="a6e72-2067">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="a6e72-2068">Для настройки AAD или AADB2C с Authority.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2068">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="a6e72-2069">Для установки политик SignupPolicy, SigninPolicy, ProfileEditingPolicy и PasswordResetPolicy.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2069">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="a6e72-2070">Обновлен командлет **New-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2070">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="a6e72-2071">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2071">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="a6e72-2072">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2072">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="a6e72-2073">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2073">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="a6e72-2074">Обновлен командлет **Set-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2074">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="a6e72-2075">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2075">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="a6e72-2076">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2076">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="a6e72-2077">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2077">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="a6e72-2078">Следующие командлеты обновлены, чтобы принимать значение ResourceId в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2078">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="a6e72-2079">New-AzApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2079">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="a6e72-2080">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="a6e72-2080">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="a6e72-2081">Get-AzApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2081">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="a6e72-2082">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="a6e72-2082">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="a6e72-2083">Get-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2083">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="a6e72-2084">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="a6e72-2084">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="a6e72-2085">Get-AzApiManagementAuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2085">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="a6e72-2086">Get-AzApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2086">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="a6e72-2087">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="a6e72-2087">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="a6e72-2088">Get-AzApiManagementCertificate.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2088">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="a6e72-2089">Remove-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2089">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="a6e72-2090">Remove-AzApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2090">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a6e72-2091">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a6e72-2091">Az.Automation</span></span>
* <span data-ttu-id="a6e72-2092">Обновлен командлет Get-AzAutomationJobOutputRecord для обработки значений в формате JSON и в виде текстовой записи.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2092">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="a6e72-2093">исправлена проблема https://github.com/Azure/azure-powershell/issues/7977.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2093">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="a6e72-2094">исправлена проблема https://github.com/Azure/azure-powershell/issues/8600.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2094">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="a6e72-2095">Поведение командлета Start-AzAutomationDscCompilationJob изменено так, чтобы сразу же запустить задание, а не ждать его завершения.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2095">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="a6e72-2096">исправлена проблема https://github.com/Azure/azure-powershell/issues/8347.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2096">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="a6e72-2097">Исправлен командлет Get-AzAutomationDscNode, возвращающий все узлы при использовании -Name.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2097">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="a6e72-2098">Теперь он возвращает только соответствующий узел.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2098">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e72-2099">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e72-2099">Az.Compute</span></span>
* <span data-ttu-id="a6e72-2100">Добавлены параметры ProtectFromScaleIn и ProtectFromScaleSetAction для командлета Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2100">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="a6e72-2101">Командлет New-AzVM с простым набором параметров теперь по умолчанию использует доступное расположение, если регион "восточная часть США" не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2101">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a6e72-2102">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a6e72-2102">Az.DataLakeStore</span></span>
* <span data-ttu-id="a6e72-2103">Обновлен пакет SDK ADLS для использования httpclient. В инфраструктуру Azure интегрирована проверка плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2103">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a6e72-2104">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a6e72-2104">Az.Monitor</span></span>
* <span data-ttu-id="a6e72-2105">Исправлены неправильные имена параметров в справочных примерах.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2105">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e72-2106">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e72-2106">Az.Network</span></span>
* <span data-ttu-id="a6e72-2107">Добавлен флаг DisableBgpRoutePropagation для выходных данных действующей таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2107">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="a6e72-2108">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="a6e72-2108">Updated cmdlet:</span></span>
        - <span data-ttu-id="a6e72-2109">Get-AzEffectiveRouteTable.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2109">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="a6e72-2110">Исправлен двойной дефис в документации New-AzApplicationGatewayTrustedRootCertificate.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2110">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e72-2111">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e72-2111">Az.Resources</span></span>
* <span data-ttu-id="a6e72-2112">Добавлен новый командлет Get-AzureRmDenyAssignment для получения запрещающих назначений.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2112">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e72-2113">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e72-2113">Az.Sql</span></span>
* <span data-ttu-id="a6e72-2114">Командлеты Расширенной защиты от угроз переименованы на командлеты Расширенной защиты данных, и оценка уязвимости включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2114">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="a6e72-2115">2.0.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2115">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a6e72-2116">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e72-2116">Az.Accounts</span></span>
* <span data-ttu-id="a6e72-2117">Обновлена библиотека аутентификации для устранения проблем с ADFS при использовании аутентификации на основе имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2117">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a6e72-2118">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-2118">Az.CognitiveServices</span></span>
* <span data-ttu-id="a6e72-2119">Отображается только заявление об отказе Bing для служб Поиска Bing.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2119">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="a6e72-2120">Исправлена проблема с созданием учетной записи.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2120">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e72-2121">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e72-2121">Az.Compute</span></span>
* <span data-ttu-id="a6e72-2122">Функция группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2122">Proximity placement group feature.</span></span>
    - <span data-ttu-id="a6e72-2123">Добавлены следующие новые командлеты:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="a6e72-2123">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="a6e72-2124">Новый параметр ProximityPlacementGroupId будет добавлен в следующие командлеты:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="a6e72-2124">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="a6e72-2125">В командлет New-AzGalleryImageVersion добавлен параметр StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2125">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="a6e72-2126">TargetRegion в командлете New-AzGalleryImageVersion может содержать StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2126">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="a6e72-2127">Параметр-переключатель SkipShutdown добавлен в командлеты Stop-AzVM и Stop-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2127">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="a6e72-2128">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="a6e72-2128">Breaking changes</span></span>
    - <span data-ttu-id="a6e72-2129">Командлет SET-AzVMBootDiagnostics изменен на Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2129">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="a6e72-2130">Командлет Export-AzLogAnalyticThrottledRequests изменен на Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2130">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="a6e72-2131">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="a6e72-2131">Az.DeploymentManager</span></span>
* <span data-ttu-id="a6e72-2132">Первая общедоступная версия командлетов диспетчера развертывания Azure</span><span class="sxs-lookup"><span data-stu-id="a6e72-2132">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="a6e72-2133">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="a6e72-2133">Az.Dns</span></span>
* <span data-ttu-id="a6e72-2134">Автоматическое делегирование DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="a6e72-2134">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="a6e72-2135">Командлет для создания зоны DNS принимает имя родительской зоны в качестве дополнительного необязательного параметра.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2135">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="a6e72-2136">Он добавляет записи NS в родительской зоне для созданной дочерней зоны.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2136">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a6e72-2137">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a6e72-2137">Az.FrontDoor</span></span>
* <span data-ttu-id="a6e72-2138">Первая общедоступная версия командлетов Azure FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2138">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="a6e72-2139">Переименованы командлеты WAF для включения Waf.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2139">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="a6e72-2140">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a6e72-2140">Az.HDInsight</span></span>
* <span data-ttu-id="a6e72-2141">Удалены два командлета:</span><span class="sxs-lookup"><span data-stu-id="a6e72-2141">Removed two cmdlets:</span></span>
    - <span data-ttu-id="a6e72-2142">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a6e72-2142">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="a6e72-2143">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a6e72-2143">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="a6e72-2144">Добавлен новый командлет Set-AzHDInsightGatewayCredential для замены Grant-AzHDInsightHttpServicesAccess.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2144">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="a6e72-2145">Обновлен командлет Get-AzHDInsightJobOutput для различения ролей читателя и оператора HDInsight:</span><span class="sxs-lookup"><span data-stu-id="a6e72-2145">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="a6e72-2146">Пользователям с ролью читателя не нужно указывать параметр DefaultStorageAccountKey явным образом, иначе возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2146">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="a6e72-2147">На пользователей с ролью оператора HDInsight это не повлияет.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2147">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a6e72-2148">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a6e72-2148">Az.Monitor</span></span>
* <span data-ttu-id="a6e72-2149">Новые командлеты для API SQR (запланированное правило запросов)</span><span class="sxs-lookup"><span data-stu-id="a6e72-2149">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="a6e72-2150">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="a6e72-2150">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="a6e72-2151">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="a6e72-2151">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="a6e72-2152">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="a6e72-2152">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="a6e72-2153">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="a6e72-2153">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="a6e72-2154">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="a6e72-2154">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="a6e72-2155">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="a6e72-2155">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="a6e72-2156">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a6e72-2156">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a6e72-2157">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a6e72-2157">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a6e72-2158">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a6e72-2158">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a6e72-2159">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a6e72-2159">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a6e72-2160">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a6e72-2160">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a6e72-2161">См. подробнее об [API SQR](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules).</span><span class="sxs-lookup"><span data-stu-id="a6e72-2161">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="a6e72-2162">Обновлен файл Az.Monitor.md для включения командлетов для правила генерации оповещений на основе метрик GenV2(не классическая версия).</span><span class="sxs-lookup"><span data-stu-id="a6e72-2162">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e72-2163">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e72-2163">Az.Network</span></span>
* <span data-ttu-id="a6e72-2164">Добавлена поддержка для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2164">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="a6e72-2165">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="a6e72-2165">New cmdlets</span></span>
        - <span data-ttu-id="a6e72-2166">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a6e72-2166">New-AzNatGateway</span></span>
        - <span data-ttu-id="a6e72-2167">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a6e72-2167">Get-AzNatGateway</span></span>
        - <span data-ttu-id="a6e72-2168">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a6e72-2168">Set-AzNatGateway</span></span>
        - <span data-ttu-id="a6e72-2169">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a6e72-2169">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="a6e72-2170">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="a6e72-2170">Updated cmdlets</span></span>
        - <span data-ttu-id="a6e72-2171">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="a6e72-2171">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="a6e72-2172">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="a6e72-2172">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="a6e72-2173">Обновлены следующие команды для функции: Настройка и удаление пользовательских маршрутов через шлюз в Бруклине.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2173">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="a6e72-2174">Обновлен командлет New-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2174">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="a6e72-2175">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2175">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a6e72-2176">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a6e72-2176">Az.PolicyInsights</span></span>
* <span data-ttu-id="a6e72-2177">Добавлена поддержка сведений об оценке политики запросов.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2177">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="a6e72-2178">Добавлен параметр -Expand в командлет Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2178">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="a6e72-2179">Добавлена поддержка -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2179">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a6e72-2180">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-2180">Az.RecoveryServices</span></span>
* <span data-ttu-id="a6e72-2181">Добавлена поддержка перекрестной подписки на Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2181">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="a6e72-2182">Добавлена возможность отмечать предстоящие критически важные изменения для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2182">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="a6e72-2183">Исправлены план восстановления и план действий для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2183">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="a6e72-2184">Исправлено сетевое сопоставление обновления Azure Site Recovery (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="a6e72-2184">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="a6e72-2185">Исправлено направление защиты обновления Azure Site Recovery для управляемых дисков (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="a6e72-2185">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="a6e72-2186">Добавлены другие незначительные исправления.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2186">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="a6e72-2187">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="a6e72-2187">Az.Relay</span></span>
* <span data-ttu-id="a6e72-2188">Исправлены опечатки в сообщениях для клиентов.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2188">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a6e72-2189">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a6e72-2189">Az.ServiceBus</span></span>
* <span data-ttu-id="a6e72-2190">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2190">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a6e72-2191">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6e72-2191">Az.Storage</span></span>
* <span data-ttu-id="a6e72-2192">Выполнено обновление клиентской библиотеки хранилища до версии 10.0.1 (пространство имен всех объектов из этого пакета SDK изменено с Microsoft.WindowsAzure.Storage. *на Microsoft.Azure.Storage*).</span><span class="sxs-lookup"><span data-stu-id="a6e72-2192">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="a6e72-2193">Выполнено обновление до Microsoft.Azure.Management.Storage версии 11.0.0 для включения поддержки нового API версии 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2193">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="a6e72-2194">Значение свойства Kind по умолчанию в учетной записи хранения изменено со Storage на StorageV2.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2194">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="a6e72-2195">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a6e72-2195">New-AzStorageAccount</span></span>
* <span data-ttu-id="a6e72-2196">Изменено значение Sku.Name в выходных данных командлета учетной записи хранения в соответствии со значением Sku.Name во входных данных путем добавления _ (например, StandardLRS изменено на Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="a6e72-2196">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="a6e72-2197">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a6e72-2197">New-AzStorageAccount</span></span>
    - <span data-ttu-id="a6e72-2198">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a6e72-2198">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="a6e72-2199">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a6e72-2199">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a6e72-2200">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6e72-2200">Az.Websites</span></span>
* <span data-ttu-id="a6e72-2201">Свойство Kind теперь будет задаваться объектам PSSite, возвращаемым командлетом Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2201">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="a6e72-2202">Get-AzWebApp\*Metrics и Get-AzAppServicePlanMetrics считаются нерекомендуемыми.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2202">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="a6e72-2203">1.8.0 — апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2203">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a6e72-2204">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="a6e72-2204">Highlights since the last major release</span></span>
* <span data-ttu-id="a6e72-2205">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2205">General availability of `Az` module</span></span>
* <span data-ttu-id="a6e72-2206">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="a6e72-2206">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="a6e72-2207">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="a6e72-2207">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="a6e72-2208">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2208">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="a6e72-2209">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2209">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a6e72-2210">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2210">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="a6e72-2211">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="a6e72-2211">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a6e72-2212">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e72-2212">Az.Accounts</span></span>
* <span data-ttu-id="a6e72-2213">Обновлен командлет Uninstall-AzureRm для правильного удаления модулей в Mac.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2213">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a6e72-2214">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a6e72-2214">Az.Batch</span></span>
* <span data-ttu-id="a6e72-2215">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2215">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a6e72-2216">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a6e72-2216">Az.Cdn</span></span>
* <span data-ttu-id="a6e72-2217">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2217">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a6e72-2218">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-2218">Az.CognitiveServices</span></span>
* <span data-ttu-id="a6e72-2219">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2219">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e72-2220">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e72-2220">Az.Compute</span></span>
* <span data-ttu-id="a6e72-2221">Устранена проблема с установкой AEM, если в идентификаторах ресурсов дисков группа ресурсов указана в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2221">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="a6e72-2222">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2222">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a6e72-2223">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2223">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a6e72-2224">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a6e72-2224">Az.DataFactory</span></span>
* <span data-ttu-id="a6e72-2225">Добавлены свойства SsisProperties, если NodeCount не имеет значения NULL для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2225">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a6e72-2226">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a6e72-2226">Az.DataLakeStore</span></span>
* <span data-ttu-id="a6e72-2227">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2227">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a6e72-2228">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a6e72-2228">Az.EventGrid</span></span>
* <span data-ttu-id="a6e72-2229">Обновлен текст справки для конечной точки, указывающий, что необходимо создать ресурсы, прежде чем использовать командлеты для создания или обновления подписки на события.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2229">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a6e72-2230">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a6e72-2230">Az.EventHub</span></span>
* <span data-ttu-id="a6e72-2231">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2231">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a6e72-2232">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a6e72-2232">Az.HDInsight</span></span>
* <span data-ttu-id="a6e72-2233">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2233">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a6e72-2234">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a6e72-2234">Az.IotHub</span></span>
* <span data-ttu-id="a6e72-2235">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2235">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a6e72-2236">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a6e72-2236">Az.KeyVault</span></span>
* <span data-ttu-id="a6e72-2237">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2237">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a6e72-2238">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2238">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="a6e72-2239">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="a6e72-2239">Az.MachineLearning</span></span>
* <span data-ttu-id="a6e72-2240">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2240">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="a6e72-2241">Az.Media</span><span class="sxs-lookup"><span data-stu-id="a6e72-2241">Az.Media</span></span>
* <span data-ttu-id="a6e72-2242">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2242">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a6e72-2243">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a6e72-2243">Az.Monitor</span></span>
  * <span data-ttu-id="a6e72-2244">Добавлены новые командлеты для правила генерации оповещений на основе метрик GenV2 (не классических).</span><span class="sxs-lookup"><span data-stu-id="a6e72-2244">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="a6e72-2245">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="a6e72-2245">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="a6e72-2246">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="a6e72-2246">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="a6e72-2247">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a6e72-2247">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="a6e72-2248">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a6e72-2248">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="a6e72-2249">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a6e72-2249">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="a6e72-2250">Обновлен пакет SDK Monitor до предварительной версии 0.22.0.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2250">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e72-2251">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e72-2251">Az.Network</span></span>
* <span data-ttu-id="a6e72-2252">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2252">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a6e72-2253">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2253">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="a6e72-2254">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="a6e72-2254">Az.NotificationHubs</span></span>
* <span data-ttu-id="a6e72-2255">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2255">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a6e72-2256">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a6e72-2256">Az.OperationalInsights</span></span>
* <span data-ttu-id="a6e72-2257">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2257">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="a6e72-2258">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="a6e72-2258">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="a6e72-2259">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2259">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a6e72-2260">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-2260">Az.RecoveryServices</span></span>
* <span data-ttu-id="a6e72-2261">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2261">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a6e72-2262">Обновлен табличный формат для SQL на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2262">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="a6e72-2263">Добавлен альтернативный метод для получения расположения в Общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2263">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="a6e72-2264">Обновлено значение ScheduleRunDays в объекте SchedulePolicy в соответствии с часовым поясом.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2264">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="a6e72-2265">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a6e72-2265">Az.RedisCache</span></span>
* <span data-ttu-id="a6e72-2266">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2266">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e72-2267">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e72-2267">Az.Resources</span></span>
* <span data-ttu-id="a6e72-2268">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2268">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e72-2269">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e72-2269">Az.Sql</span></span>
* <span data-ttu-id="a6e72-2270">Заменена зависимость от пакета SDK монитора на обычный код.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2270">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="a6e72-2271">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2271">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a6e72-2272">Улучшен процесс классификации нескольких столбцов.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2272">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="a6e72-2273">Добавлены свойства SKU (имя, семейство, производительность SKU) в отклике Get-AzSqlServerServiceObjective, а также по умолчанию задан табличный формат.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2273">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="a6e72-2274">C помощью Get-AzSqlServerServiceObjective теперь можно получать список доступных целевых служб по расположению без необходимости заранее размещать сервер в регионе.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2274">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="a6e72-2275">Поддерживается параметр часового пояса при создании Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2275">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="a6e72-2276">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2276">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a6e72-2277">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6e72-2277">Az.Websites</span></span>
* <span data-ttu-id="a6e72-2278">Исправлены командлеты Set-AzWebApp и Set-AzWebAppSlot, которые теперь не удаляют теги при выполнении.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2278">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="a6e72-2279">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2279">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a6e72-2280">Обновлен пакет SDK веб-узлов.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2280">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="a6e72-2281">Удалено свойство AdminSiteName из PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2281">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="a6e72-2282">1.7.0 —апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2282">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a6e72-2283">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="a6e72-2283">Highlights since the last major release</span></span>
* <span data-ttu-id="a6e72-2284">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2284">General availability of `Az` module</span></span>
* <span data-ttu-id="a6e72-2285">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="a6e72-2285">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="a6e72-2286">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="a6e72-2286">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="a6e72-2287">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2287">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="a6e72-2288">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2288">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a6e72-2289">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2289">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="a6e72-2290">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="a6e72-2290">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a6e72-2291">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e72-2291">Az.Accounts</span></span>
* <span data-ttu-id="a6e72-2292">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметр AzureAnalysisServicesEndpointResourceId.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2292">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a6e72-2293">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-2293">Az.AnalysisServices</span></span>
* <span data-ttu-id="a6e72-2294">Использование ServiceClient в командлетах плоскости данных и удаление исходной логики проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2294">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="a6e72-2295">Add-AzureASAccount используется как оболочка для Connect-AzAccount во избежание критических изменений.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2295">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a6e72-2296">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a6e72-2296">Az.Automation</span></span>
* <span data-ttu-id="a6e72-2297">Исправлена ошибка командлета New-AzAutomationSoftwareUpdateConfiguration, связанная с включением.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2297">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="a6e72-2298">Теперь параметры IncludedKbNumber и IncludedPackageNameMask должны работать нормально.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2298">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="a6e72-2299">Исправлена ошибка динамической группы управления обновлениями службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2299">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e72-2300">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e72-2300">Az.Compute</span></span>
* <span data-ttu-id="a6e72-2301">В командлеты New-AzDiskConfig и New-AzSnapshotConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2301">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="a6e72-2302">Теперь можно создавать виртуальные машину на основе образов из коллекции от других клиентов.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2302">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="a6e72-2303">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a6e72-2303">Az.ContainerInstance</span></span>
* <span data-ttu-id="a6e72-2304">Исправлена проблема в параметре -Command командлета New-AzContainerGroup, из-за которой в конце добавлялся пустой аргумент.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2304">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a6e72-2305">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a6e72-2305">Az.DataFactory</span></span>
* <span data-ttu-id="a6e72-2306">Пакет SDK для ADF .NET обновлен до версии 3.0.2.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2306">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="a6e72-2307">Командлет Set-AzDataFactoryV2 обновлен с помощью дополнительных параметров для настроек, связанных с RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2307">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e72-2308">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e72-2308">Az.Resources</span></span>
* <span data-ttu-id="a6e72-2309">Улучшена обработка поставщиков Get-AzResource при предоставлении параметров -ResourceId или -ResourceGroupName, -Name и -ResourceType.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2309">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="a6e72-2310">Улучшена обработка ошибок в командлетах Test-AzDeployment и Test-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2310">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="a6e72-2311">Теперь ошибки, возникающие за пределами проверки развертывания, обрабатываются и включаются в выходные данные команды.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2311">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="a6e72-2312">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2312">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="a6e72-2313">Добавлен параметр-переключатель -IgnoreDynamicParameters, с помощью которого можно настроить командлеты развертывания так, чтобы они пропускали запросы в сценариях скриптов и заданий.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2313">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="a6e72-2314">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2314">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e72-2315">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e72-2315">Az.Sql</span></span>
* <span data-ttu-id="a6e72-2316">Поддержка классификации данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2316">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a6e72-2317">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6e72-2317">Az.Storage</span></span>
* <span data-ttu-id="a6e72-2318">Подробные сообщения об ошибке передаются при создании контекста хранилища с помощью параметра -UseConnectedAccount, но без входа в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2318">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="a6e72-2319">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a6e72-2319">New-AzStorageContext</span></span>
* <span data-ttu-id="a6e72-2320">Поддержка свойств службы управления BLOB-объектов в указанной учетной записи хранения с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2320">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="a6e72-2321">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="a6e72-2321">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="a6e72-2322">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="a6e72-2322">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="a6e72-2323">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a6e72-2323">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="a6e72-2324">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a6e72-2324">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="a6e72-2325">Поддержка параметра -AsJob в командлетах для отправки и скачивания больших двоичных объектов и файлов.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2325">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="a6e72-2326">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a6e72-2326">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="a6e72-2327">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a6e72-2327">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="a6e72-2328">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a6e72-2328">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="a6e72-2329">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a6e72-2329">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="a6e72-2330">1.6.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2330">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a6e72-2331">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="a6e72-2331">Highlights since the last major release</span></span>
* <span data-ttu-id="a6e72-2332">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2332">General availability of `Az` module</span></span>
* <span data-ttu-id="a6e72-2333">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="a6e72-2333">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="a6e72-2334">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="a6e72-2334">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="a6e72-2335">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2335">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="a6e72-2336">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2336">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a6e72-2337">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2337">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="a6e72-2338">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="a6e72-2338">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a6e72-2339">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a6e72-2339">Az.Automation</span></span>
* <span data-ttu-id="a6e72-2340">В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:</span><span class="sxs-lookup"><span data-stu-id="a6e72-2340">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="a6e72-2341">динамическое группирование;</span><span class="sxs-lookup"><span data-stu-id="a6e72-2341">Dynamic grouping</span></span>
    * <span data-ttu-id="a6e72-2342">скрипты предварительного или последующего выполнения;</span><span class="sxs-lookup"><span data-stu-id="a6e72-2342">Pre-Post script</span></span>
    * <span data-ttu-id="a6e72-2343">параметр перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2343">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e72-2344">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e72-2344">Az.Compute</span></span>
* <span data-ttu-id="a6e72-2345">Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2345">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="a6e72-2346">Обновление клиентской библиотеки вычислений до версии 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2346">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a6e72-2347">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a6e72-2347">Az.KeyVault</span></span>
* <span data-ttu-id="a6e72-2348">Добавлена поддержка подстановочных знаков в командлетах KeyVault.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2348">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e72-2349">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e72-2349">Az.Network</span></span>
* <span data-ttu-id="a6e72-2350">Добавлена поддержка анализа угроз для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2350">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="a6e72-2351">Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2351">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a6e72-2352">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-2352">Az.RecoveryServices</span></span>
* <span data-ttu-id="a6e72-2353">В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2353">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="a6e72-2354">Добавлена поддержка канала для отмены регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2354">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e72-2355">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e72-2355">Az.Resources</span></span>
* <span data-ttu-id="a6e72-2356">Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2356">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="a6e72-2357">Обновлены учетные данные, используемые при общих вызовах к ARM.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2357">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e72-2358">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e72-2358">Az.Sql</span></span>
* <span data-ttu-id="a6e72-2359">Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2359">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a6e72-2360">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6e72-2360">Az.Storage</span></span>
* <span data-ttu-id="a6e72-2361">Поддержка получения, настройки и удаления политики управления в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2361">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="a6e72-2362">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a6e72-2362">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="a6e72-2363">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a6e72-2363">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="a6e72-2364">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a6e72-2364">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="a6e72-2365">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="a6e72-2365">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="a6e72-2366">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="a6e72-2366">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="a6e72-2367">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="a6e72-2367">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a6e72-2368">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6e72-2368">Az.Websites</span></span>
* <span data-ttu-id="a6e72-2369">Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2369">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="a6e72-2370">1.5.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2370">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a6e72-2371">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e72-2371">Az.Accounts</span></span>
* <span data-ttu-id="a6e72-2372">Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2372">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="a6e72-2373">Обновлены примеры для Connect AzAccount.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2373">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a6e72-2374">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a6e72-2374">Az.Automation</span></span>
* <span data-ttu-id="a6e72-2375">Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2375">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="a6e72-2376">Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2376">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="a6e72-2377">Теперь он возвращает все узлы.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2377">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a6e72-2378">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a6e72-2378">Az.Cdn</span></span>
* <span data-ttu-id="a6e72-2379">Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2379">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e72-2380">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e72-2380">Az.Compute</span></span>
* <span data-ttu-id="a6e72-2381">Добавлена поддержка подстановочных знаков в командлетах Get.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2381">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a6e72-2382">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a6e72-2382">Az.DataFactory</span></span>
* <span data-ttu-id="a6e72-2383">Обновлен пакет SDK для ADF .NET до версии 3.0.1.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2383">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a6e72-2384">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a6e72-2384">Az.LogicApp</span></span>
* <span data-ttu-id="a6e72-2385">Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2385">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e72-2386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e72-2386">Az.Network</span></span>
* <span data-ttu-id="a6e72-2387">Добавлена поддержка подстановочных знаков в командлетах Network.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2387">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a6e72-2388">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-2388">Az.RecoveryServices</span></span>
* <span data-ttu-id="a6e72-2389">Добавлена поддержка SQL Server на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2389">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="a6e72-2390">Обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="a6e72-2390">SDK Update</span></span>
* <span data-ttu-id="a6e72-2391">Удалена проверка VMappContainer в Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2391">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="a6e72-2392">Добавлены параметры Name и ServerName для Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2392">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e72-2393">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e72-2393">Az.Resources</span></span>
* <span data-ttu-id="a6e72-2394">Добавлен параметр `-TemplateObject` в командлеты для развертывания.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2394">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="a6e72-2395">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2395">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="a6e72-2396">Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2396">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="a6e72-2397">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2397">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="a6e72-2398">Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2398">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="a6e72-2399">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2399">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e72-2400">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e72-2400">Az.Sql</span></span>
* <span data-ttu-id="a6e72-2401">Обновление AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2401">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="a6e72-2402">Исправлено поведение для пограничного случая при создании параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2402">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a6e72-2403">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6e72-2403">Az.Storage</span></span>
* <span data-ttu-id="a6e72-2404">Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2404">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="a6e72-2405">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2405">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="a6e72-2406">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-2406">Az.AnalysisServices</span></span>
* <span data-ttu-id="a6e72-2407">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2407">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a6e72-2408">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a6e72-2408">Az.Automation</span></span>
* <span data-ttu-id="a6e72-2409">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2409">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="a6e72-2410">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2410">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="a6e72-2411">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2411">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a6e72-2412">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-2412">Az.CognitiveServices</span></span>
* <span data-ttu-id="a6e72-2413">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2413">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e72-2414">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e72-2414">Az.Compute</span></span>
* <span data-ttu-id="a6e72-2415">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2415">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="a6e72-2416">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2416">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="a6e72-2417">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2417">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="a6e72-2418">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2418">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a6e72-2419">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a6e72-2419">Az.DataLakeStore</span></span>
* <span data-ttu-id="a6e72-2420">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2420">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a6e72-2421">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a6e72-2421">Az.EventHub</span></span>
* <span data-ttu-id="a6e72-2422">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2422">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a6e72-2423">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a6e72-2423">Az.KeyVault</span></span>
* <span data-ttu-id="a6e72-2424">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2424">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a6e72-2425">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a6e72-2425">Az.LogicApp</span></span>
* <span data-ttu-id="a6e72-2426">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2426">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="a6e72-2427">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2427">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="a6e72-2428">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="a6e72-2428">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="a6e72-2429">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="a6e72-2429">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a6e72-2430">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="a6e72-2430">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a6e72-2431">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="a6e72-2431">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a6e72-2432">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2432">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="a6e72-2433">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="a6e72-2433">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="a6e72-2434">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="a6e72-2434">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a6e72-2435">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="a6e72-2435">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a6e72-2436">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="a6e72-2436">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a6e72-2437">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2437">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="a6e72-2438">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2438">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a6e72-2439">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a6e72-2439">Az.Monitor</span></span>
* <span data-ttu-id="a6e72-2440">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2440">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e72-2441">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e72-2441">Az.Network</span></span>
* <span data-ttu-id="a6e72-2442">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2442">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a6e72-2443">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a6e72-2443">Az.OperationalInsights</span></span>
* <span data-ttu-id="a6e72-2444">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2444">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="a6e72-2445">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2445">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="a6e72-2446">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2446">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e72-2447">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e72-2447">Az.Resources</span></span>
* <span data-ttu-id="a6e72-2448">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2448">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="a6e72-2449">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2449">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="a6e72-2450">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2450">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="a6e72-2451">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2451">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e72-2452">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e72-2452">Az.Sql</span></span>
* <span data-ttu-id="a6e72-2453">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2453">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="a6e72-2454">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2454">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a6e72-2455">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6e72-2455">Az.Websites</span></span>
* <span data-ttu-id="a6e72-2456">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2456">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="a6e72-2457">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2457">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a6e72-2458">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e72-2458">Az.Accounts</span></span>
* <span data-ttu-id="a6e72-2459">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="a6e72-2459">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a6e72-2460">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-2460">Az.AnalysisServices</span></span>
<span data-ttu-id="a6e72-2461">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2461">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e72-2462">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e72-2462">Az.Compute</span></span>
* <span data-ttu-id="a6e72-2463">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2463">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="a6e72-2464">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2464">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="a6e72-2465">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2465">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a6e72-2466">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-2466">Az.RecoveryServices</span></span>
<span data-ttu-id="a6e72-2467">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2467">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e72-2468">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e72-2468">Az.Resources</span></span>
* <span data-ttu-id="a6e72-2469">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2469">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="a6e72-2470">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2470">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="a6e72-2471">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2471">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="a6e72-2472">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2472">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e72-2473">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e72-2473">Az.Sql</span></span>
* <span data-ttu-id="a6e72-2474">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2474">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="a6e72-2475">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2475">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="a6e72-2476">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2476">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="a6e72-2477">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2477">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a6e72-2478">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e72-2478">Az.Accounts</span></span>
* <span data-ttu-id="a6e72-2479">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2479">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a6e72-2480">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-2480">Az.AnalysisServices</span></span>
* <span data-ttu-id="a6e72-2481">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2481">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a6e72-2482">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-2482">Az.RecoveryServices</span></span>
* <span data-ttu-id="a6e72-2483">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2483">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="a6e72-2484">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2484">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a6e72-2485">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e72-2485">Az.Accounts</span></span>
* <span data-ttu-id="a6e72-2486">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2486">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a6e72-2487">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2487">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a6e72-2488">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2488">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="a6e72-2489">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a6e72-2489">Az.Aks</span></span>
* <span data-ttu-id="a6e72-2490">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2490">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a6e72-2491">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a6e72-2491">Az.Automation</span></span>
* <span data-ttu-id="a6e72-2492">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2492">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="a6e72-2493">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2493">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a6e72-2494">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a6e72-2494">Az.Cdn</span></span>
* <span data-ttu-id="a6e72-2495">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2495">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e72-2496">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e72-2496">Az.Compute</span></span>
* <span data-ttu-id="a6e72-2497">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2497">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="a6e72-2498">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2498">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="a6e72-2499">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2499">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="a6e72-2500">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a6e72-2500">Az.ContainerRegistry</span></span>
* <span data-ttu-id="a6e72-2501">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2501">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a6e72-2502">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a6e72-2502">Az.DataFactory</span></span>
* <span data-ttu-id="a6e72-2503">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2503">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a6e72-2504">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a6e72-2504">Az.DataLakeStore</span></span>
* <span data-ttu-id="a6e72-2505">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2505">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="a6e72-2506">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2506">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="a6e72-2507">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2507">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a6e72-2508">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a6e72-2508">Az.IotHub</span></span>
* <span data-ttu-id="a6e72-2509">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2509">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a6e72-2510">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a6e72-2510">Az.KeyVault</span></span>
* <span data-ttu-id="a6e72-2511">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2511">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e72-2512">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e72-2512">Az.Network</span></span>
* <span data-ttu-id="a6e72-2513">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2513">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e72-2514">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e72-2514">Az.Resources</span></span>
* <span data-ttu-id="a6e72-2515">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2515">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="a6e72-2516">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2516">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="a6e72-2517">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2517">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="a6e72-2518">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2518">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="a6e72-2519">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2519">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="a6e72-2520">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2520">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="a6e72-2521">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2521">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a6e72-2522">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a6e72-2522">Az.ServiceFabric</span></span>
* <span data-ttu-id="a6e72-2523">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2523">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="a6e72-2524">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2524">Fix some error messages.</span></span>
* <span data-ttu-id="a6e72-2525">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2525">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="a6e72-2526">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2526">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a6e72-2527">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a6e72-2527">Az.SignalR</span></span>
* <span data-ttu-id="a6e72-2528">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2528">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e72-2529">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e72-2529">Az.Sql</span></span>
* <span data-ttu-id="a6e72-2530">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2530">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a6e72-2531">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2531">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="a6e72-2532">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2532">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="a6e72-2533">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2533">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a6e72-2534">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6e72-2534">Az.Storage</span></span>
* <span data-ttu-id="a6e72-2535">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2535">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a6e72-2536">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2536">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="a6e72-2537">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="a6e72-2537">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="a6e72-2538">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="a6e72-2538">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="a6e72-2539">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a6e72-2539">Az.TrafficManager</span></span>
* <span data-ttu-id="a6e72-2540">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2540">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a6e72-2541">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6e72-2541">Az.Websites</span></span>
* <span data-ttu-id="a6e72-2542">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2542">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a6e72-2543">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2543">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="a6e72-2544">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2544">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="a6e72-2545">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2545">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a6e72-2546">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e72-2546">Az.Accounts</span></span>
* <span data-ttu-id="a6e72-2547">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2547">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e72-2548">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e72-2548">Az.Compute</span></span>
* <span data-ttu-id="a6e72-2549">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2549">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="a6e72-2550">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2550">Updated the description of ID in help files</span></span>
* <span data-ttu-id="a6e72-2551">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2551">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a6e72-2552">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a6e72-2552">Az.DataLakeStore</span></span>
* <span data-ttu-id="a6e72-2553">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2553">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="a6e72-2554">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2554">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a6e72-2555">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a6e72-2555">Az.EventGrid</span></span>
* <span data-ttu-id="a6e72-2556">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2556">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="a6e72-2557">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2557">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="a6e72-2558">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="a6e72-2558">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="a6e72-2559">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="a6e72-2559">Event Time-To-Live,</span></span>
        - <span data-ttu-id="a6e72-2560">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="a6e72-2560">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="a6e72-2561">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2561">Dead letter endpoint.</span></span>
    - <span data-ttu-id="a6e72-2562">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="a6e72-2562">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="a6e72-2563">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="a6e72-2563">Event Time-To-Live,</span></span>
        - <span data-ttu-id="a6e72-2564">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="a6e72-2564">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="a6e72-2565">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2565">Dead letter endpoint.</span></span>
* <span data-ttu-id="a6e72-2566">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2566">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="a6e72-2567">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2567">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a6e72-2568">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a6e72-2568">Az.IotHub</span></span>
* <span data-ttu-id="a6e72-2569">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2569">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a6e72-2570">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a6e72-2570">Az.LogicApp</span></span>
* <span data-ttu-id="a6e72-2571">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2571">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e72-2572">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e72-2572">Az.Resources</span></span>
* <span data-ttu-id="a6e72-2573">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="a6e72-2573">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="a6e72-2574">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2574">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="a6e72-2575">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2575">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="a6e72-2576">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2576">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="a6e72-2577">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="a6e72-2577">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="a6e72-2578">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2578">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a6e72-2579">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a6e72-2579">Az.SignalR</span></span>
* <span data-ttu-id="a6e72-2580">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2580">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e72-2581">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e72-2581">Az.Sql</span></span>
* <span data-ttu-id="a6e72-2582">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2582">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a6e72-2583">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6e72-2583">Az.Storage</span></span>
* <span data-ttu-id="a6e72-2584">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2584">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="a6e72-2585">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a6e72-2585">New-AzStorageContext</span></span>
* <span data-ttu-id="a6e72-2586">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2586">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="a6e72-2587">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="a6e72-2587">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a6e72-2588">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6e72-2588">Az.Websites</span></span>
* <span data-ttu-id="a6e72-2589">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="a6e72-2589">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="a6e72-2590">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2590">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="a6e72-2591">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2591">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="a6e72-2592">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="a6e72-2592">General</span></span>

- <span data-ttu-id="a6e72-2593">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2593">General Availability of Az Module</span></span>
- <span data-ttu-id="a6e72-2594">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2594">Online help for each module</span></span>
- <span data-ttu-id="a6e72-2595">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="a6e72-2595">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="a6e72-2596">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="a6e72-2596">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="a6e72-2597">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e72-2597">Az.Accounts</span></span>
- <span data-ttu-id="a6e72-2598">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2598">Changed from Az.Profile</span></span>
- <span data-ttu-id="a6e72-2599">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2599">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="a6e72-2600">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a6e72-2600">Az.ApiManagement</span></span>
- <span data-ttu-id="a6e72-2601">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2601">Fixes for #7002</span></span>
- <span data-ttu-id="a6e72-2602">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="a6e72-2602">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="a6e72-2603">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a6e72-2603">Az.Batch</span></span>
- <span data-ttu-id="a6e72-2604">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2604">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="a6e72-2605">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2605">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="a6e72-2606">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="a6e72-2606">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="a6e72-2607">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="a6e72-2607">Az.Billing</span></span>
- <span data-ttu-id="a6e72-2608">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="a6e72-2608">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="a6e72-2609">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-2609">Az.CognitivServices</span></span>
- <span data-ttu-id="a6e72-2610">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2610">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="a6e72-2611">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2611">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="a6e72-2612">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a6e72-2612">Az.ContainerInstance</span></span>
- <span data-ttu-id="a6e72-2613">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2613">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="a6e72-2614">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="a6e72-2614">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="a6e72-2615">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="a6e72-2615">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="a6e72-2616">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a6e72-2616">Az.DataLakeStore</span></span>
- <span data-ttu-id="a6e72-2617">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="a6e72-2617">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="a6e72-2618">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a6e72-2618">Az.Monitor</span></span>
- <span data-ttu-id="a6e72-2619">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="a6e72-2619">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="a6e72-2620">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a6e72-2620">Az.KeyVault</span></span>
- <span data-ttu-id="a6e72-2621">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="a6e72-2621">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="a6e72-2622">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="a6e72-2622">Az.MachineLearning</span></span>
- <span data-ttu-id="a6e72-2623">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="a6e72-2623">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="a6e72-2624">Az.Media</span><span class="sxs-lookup"><span data-stu-id="a6e72-2624">Az.Media</span></span>
- <span data-ttu-id="a6e72-2625">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="a6e72-2625">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="a6e72-2626">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e72-2626">Az.Network</span></span>
<span data-ttu-id="a6e72-2627">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="a6e72-2627">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="a6e72-2628">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="a6e72-2628">New cmdlets added:</span></span>
        - <span data-ttu-id="a6e72-2629">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a6e72-2629">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a6e72-2630">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a6e72-2630">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a6e72-2631">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a6e72-2631">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a6e72-2632">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a6e72-2632">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a6e72-2633">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a6e72-2633">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a6e72-2634">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="a6e72-2634">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="a6e72-2635">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="a6e72-2635">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="a6e72-2636">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6e72-2636">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="a6e72-2637">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a6e72-2637">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="a6e72-2638">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a6e72-2638">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="a6e72-2639">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a6e72-2639">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="a6e72-2640">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a6e72-2640">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="a6e72-2641">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a6e72-2641">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="a6e72-2642">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a6e72-2642">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="a6e72-2643">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2643">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="a6e72-2644">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a6e72-2644">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="a6e72-2645">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a6e72-2645">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="a6e72-2646">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a6e72-2646">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="a6e72-2647">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a6e72-2647">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="a6e72-2648">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="a6e72-2648">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="a6e72-2649">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="a6e72-2649">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="a6e72-2650">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a6e72-2650">Az.OperationalInsights</span></span>
- <span data-ttu-id="a6e72-2651">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="a6e72-2651">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="a6e72-2652">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a6e72-2652">Az.Profile</span></span>
- <span data-ttu-id="a6e72-2653">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2653">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="a6e72-2654">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-2654">Az.RecoveryServices</span></span>
- <span data-ttu-id="a6e72-2655">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="a6e72-2655">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="a6e72-2656">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e72-2656">Az.Resources</span></span>
- <span data-ttu-id="a6e72-2657">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="a6e72-2657">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="a6e72-2658">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a6e72-2658">Az.ServiceFabric</span></span>
- <span data-ttu-id="a6e72-2659">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="a6e72-2659">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="a6e72-2660">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="a6e72-2660">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="a6e72-2661">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="a6e72-2661">Az.SIgnalR</span></span>
- <span data-ttu-id="a6e72-2662">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="a6e72-2662">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="a6e72-2663">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e72-2663">Az.Sql</span></span>
- <span data-ttu-id="a6e72-2664">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="a6e72-2664">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="a6e72-2665">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="a6e72-2665">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="a6e72-2666">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="a6e72-2666">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="a6e72-2667">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6e72-2667">Az.Storage</span></span>
- <span data-ttu-id="a6e72-2668">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="a6e72-2668">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="a6e72-2669">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6e72-2669">Az.Websites</span></span>
- <span data-ttu-id="a6e72-2670">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="a6e72-2670">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="a6e72-2671">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2671">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="a6e72-2672">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="a6e72-2672">General</span></span>

* <span data-ttu-id="a6e72-2673">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="a6e72-2673">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="a6e72-2674">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e72-2674">Az.Compute</span></span>

* <span data-ttu-id="a6e72-2675">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2675">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="a6e72-2676">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a6e72-2676">Az.DataLakeStore</span></span>

* <span data-ttu-id="a6e72-2677">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="a6e72-2677">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="a6e72-2678">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a6e72-2678">Az.FrontDoor</span></span>

* <span data-ttu-id="a6e72-2679">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="a6e72-2679">Fixed some broken links</span></span>
    - <span data-ttu-id="a6e72-2680">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2680">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="a6e72-2681">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2681">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="a6e72-2682">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-2682">Az.RecoveryServices</span></span>

* <span data-ttu-id="a6e72-2683">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2683">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="a6e72-2684">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2684">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="a6e72-2685">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e72-2685">Az.Resources</span></span>

* <span data-ttu-id="a6e72-2686">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2686">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="a6e72-2687">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2687">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="a6e72-2688">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e72-2688">Az.Sql</span></span>

* <span data-ttu-id="a6e72-2689">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="a6e72-2689">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="a6e72-2690">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2690">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="a6e72-2691">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2691">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="a6e72-2692">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6e72-2692">Az.Storage</span></span>

* <span data-ttu-id="a6e72-2693">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a6e72-2693">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="a6e72-2694">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="a6e72-2694">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="a6e72-2695">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="a6e72-2695">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="a6e72-2696">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="a6e72-2696">Support Static Website configuration</span></span>
    - <span data-ttu-id="a6e72-2697">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="a6e72-2697">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="a6e72-2698">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="a6e72-2698">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="a6e72-2699">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6e72-2699">Az.Websites</span></span>

* <span data-ttu-id="a6e72-2700">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a6e72-2700">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="a6e72-2701">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2701">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="a6e72-2702">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2702">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="a6e72-2703">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2703">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="a6e72-2704">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a6e72-2704">Az.ApiManagement</span></span>
* <span data-ttu-id="a6e72-2705">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2705">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="a6e72-2706">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a6e72-2706">Az.Automation</span></span>
* <span data-ttu-id="a6e72-2707">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2707">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="a6e72-2708">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2708">Added Update Management cmdlets</span></span>
* <span data-ttu-id="a6e72-2709">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2709">Added Source Control cmdlets</span></span>
* <span data-ttu-id="a6e72-2710">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2710">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="a6e72-2711">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2711">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="a6e72-2712">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e72-2712">Az.Compute</span></span>
* <span data-ttu-id="a6e72-2713">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2713">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="a6e72-2714">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2714">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="a6e72-2715">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a6e72-2715">Az.ContainerInstance</span></span>
* <span data-ttu-id="a6e72-2716">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2716">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="a6e72-2717">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="a6e72-2717">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="a6e72-2718">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2718">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="a6e72-2719">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e72-2719">Az.Network</span></span>
* <span data-ttu-id="a6e72-2720">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2720">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="a6e72-2721">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2721">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="a6e72-2722">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2722">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="a6e72-2723">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2723">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="a6e72-2724">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a6e72-2724">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a6e72-2725">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2725">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="a6e72-2726">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2726">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="a6e72-2727">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="a6e72-2727">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="a6e72-2728">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2728">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="a6e72-2729">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2729">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="a6e72-2730">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="a6e72-2730">Az.Relay</span></span>
* <span data-ttu-id="a6e72-2731">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2731">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="a6e72-2732">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e72-2732">Az.Resources</span></span>
* <span data-ttu-id="a6e72-2733">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2733">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="a6e72-2734">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2734">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="a6e72-2735">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2735">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="a6e72-2736">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a6e72-2736">Az.ServiceFabric</span></span>
* <span data-ttu-id="a6e72-2737">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2737">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="a6e72-2738">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e72-2738">Az.Sql</span></span>
* <span data-ttu-id="a6e72-2739">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2739">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="a6e72-2740">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2740">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a6e72-2741">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2741">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a6e72-2742">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2742">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a6e72-2743">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2743">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a6e72-2744">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2744">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a6e72-2745">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2745">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a6e72-2746">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2746">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a6e72-2747">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2747">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="a6e72-2748">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2748">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="a6e72-2749">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2749">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="a6e72-2750">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2750">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="a6e72-2751">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2751">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="a6e72-2752">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2752">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="a6e72-2753">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2753">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="a6e72-2754">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2754">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="a6e72-2755">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2755">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="a6e72-2756">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2756">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a6e72-2757">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="a6e72-2757">General</span></span>
* <span data-ttu-id="a6e72-2758">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="a6e72-2758">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="a6e72-2759">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a6e72-2759">Az.Profile</span></span>
* <span data-ttu-id="a6e72-2760">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2760">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="a6e72-2761">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="a6e72-2761">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="a6e72-2762">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="a6e72-2762">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="a6e72-2763">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2763">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="a6e72-2764">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2764">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="a6e72-2765">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2765">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="a6e72-2766">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="a6e72-2766">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="a6e72-2767">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-2767">Az.CognitiveServices</span></span>
* <span data-ttu-id="a6e72-2768">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2768">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e72-2769">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e72-2769">Az.Compute</span></span>
* <span data-ttu-id="a6e72-2770">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="a6e72-2770">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="a6e72-2771">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="a6e72-2771">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="a6e72-2772">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2772">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a6e72-2773">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a6e72-2773">Az.DataLakeStore</span></span>
* <span data-ttu-id="a6e72-2774">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2774">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="a6e72-2775">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2775">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="a6e72-2776">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="a6e72-2776">Az.Insights</span></span>
* <span data-ttu-id="a6e72-2777">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="a6e72-2777">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="a6e72-2778">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="a6e72-2778">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="a6e72-2779">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="a6e72-2779">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="a6e72-2780">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2780">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e72-2781">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e72-2781">Az.Network</span></span>
* <span data-ttu-id="a6e72-2782">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="a6e72-2782">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="a6e72-2783">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="a6e72-2783">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="a6e72-2784">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="a6e72-2784">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="a6e72-2785">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a6e72-2785">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="a6e72-2786">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="a6e72-2786">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="a6e72-2787">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="a6e72-2787">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="a6e72-2788">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a6e72-2788">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a6e72-2789">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a6e72-2789">Az.PolicyInsights</span></span>
* <span data-ttu-id="a6e72-2790">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2790">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e72-2791">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e72-2791">Az.Resources</span></span>
* <span data-ttu-id="a6e72-2792">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2792">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="a6e72-2793">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="a6e72-2793">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a6e72-2794">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a6e72-2794">Az.ServiceBus</span></span>
* <span data-ttu-id="a6e72-2795">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2795">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a6e72-2796">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a6e72-2796">Az.ServiceFabric</span></span>
* <span data-ttu-id="a6e72-2797">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2797">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="a6e72-2798">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="a6e72-2798">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="a6e72-2799">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="a6e72-2799">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="a6e72-2800">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="a6e72-2800">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="a6e72-2801">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2801">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="a6e72-2802">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2802">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="a6e72-2803">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a6e72-2803">Az.Profile</span></span>
* <span data-ttu-id="a6e72-2804">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="a6e72-2804">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="a6e72-2805">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2805">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e72-2806">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e72-2806">Az.Compute</span></span>
* <span data-ttu-id="a6e72-2807">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="a6e72-2807">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="a6e72-2808">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2808">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a6e72-2809">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a6e72-2809">Az.DataLakeStore</span></span>
* <span data-ttu-id="a6e72-2810">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="a6e72-2810">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="a6e72-2811">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2811">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="a6e72-2812">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2812">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="a6e72-2813">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2813">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="a6e72-2814">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2814">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e72-2815">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e72-2815">Az.Network</span></span>
* <span data-ttu-id="a6e72-2816">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2816">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="a6e72-2817">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2817">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e72-2818">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e72-2818">Az.Resources</span></span>
* <span data-ttu-id="a6e72-2819">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2819">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="a6e72-2820">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2820">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="a6e72-2821">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2821">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="a6e72-2822">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="a6e72-2822">Azure.Storage</span></span>
* <span data-ttu-id="a6e72-2823">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2823">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="a6e72-2824">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a6e72-2824">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="a6e72-2825">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="a6e72-2825">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="a6e72-2826">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2826">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="a6e72-2827">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="a6e72-2827">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a6e72-2828">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a6e72-2828">Az.CognitiveServices</span></span>
* <span data-ttu-id="a6e72-2829">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2829">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e72-2830">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e72-2830">Az.Compute</span></span>
* <span data-ttu-id="a6e72-2831">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="a6e72-2831">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="a6e72-2832">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2832">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="a6e72-2833">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2833">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="a6e72-2834">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a6e72-2834">Az.DataFactoryV2</span></span>
* <span data-ttu-id="a6e72-2835">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2835">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e72-2836">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e72-2836">Az.Network</span></span>
* <span data-ttu-id="a6e72-2837">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2837">Added NetworkProfile functionality.</span></span> <span data-ttu-id="a6e72-2838">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="a6e72-2838">new cmdlets added</span></span>
    - <span data-ttu-id="a6e72-2839">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a6e72-2839">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="a6e72-2840">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a6e72-2840">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="a6e72-2841">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a6e72-2841">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="a6e72-2842">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a6e72-2842">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="a6e72-2843">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="a6e72-2843">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="a6e72-2844">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="a6e72-2844">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="a6e72-2845">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2845">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="a6e72-2846">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="a6e72-2846">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="a6e72-2847">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="a6e72-2847">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="a6e72-2848">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a6e72-2848">Az.RedisCache</span></span>
* <span data-ttu-id="a6e72-2849">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2849">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="a6e72-2850">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2850">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e72-2851">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e72-2851">Az.Resources</span></span>
* <span data-ttu-id="a6e72-2852">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a6e72-2852">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="a6e72-2853">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="a6e72-2853">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e72-2854">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e72-2854">Az.Sql</span></span>
* <span data-ttu-id="a6e72-2855">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2855">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a6e72-2856">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6e72-2856">Az.Websites</span></span>
* <span data-ttu-id="a6e72-2857">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="a6e72-2857">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="a6e72-2858">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="a6e72-2858">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="a6e72-2859">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="a6e72-2859">0.2.0 - September 2018</span></span>
 <span data-ttu-id="a6e72-2860">Начальный выпуск</span><span class="sxs-lookup"><span data-stu-id="a6e72-2860">Initial Release</span></span>
