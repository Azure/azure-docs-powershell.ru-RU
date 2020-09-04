---
title: Заметки о выпуске Azure PowerShell
description: Узнайте обо всех последних обновлениях модулей Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 04e85c32b1af0bbdfb622973e0900724b8e3c8e3
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "89244234"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="cb73b-103">Заметки о выпуске Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="cb73b-103">Azure PowerShell release notes</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="cb73b-104">4.6.1 — август 2020 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-104">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="cb73b-105">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb73b-105">Az.Compute</span></span>
* <span data-ttu-id="cb73b-106">Исправлен параметр -EncryptionAtHost в New-AzVm для удаления значения false по умолчанию [№ 12776].</span><span class="sxs-lookup"><span data-stu-id="cb73b-106">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="cb73b-107">4.6.0 — август 2020 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-107">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb73b-108">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb73b-108">Az.Accounts</span></span>
* <span data-ttu-id="cb73b-109">Загружаются все общедоступные облачные среды, когда конечная точка обнаружения не возвращает AzureCloud по умолчанию или другие общедоступные среды [№ 12633]</span><span class="sxs-lookup"><span data-stu-id="cb73b-109">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="cb73b-110">В Get-AzSubscription предоставлен параметр SubscriptionPolicies [№ 12551].</span><span class="sxs-lookup"><span data-stu-id="cb73b-110">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb73b-111">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb73b-111">Az.Automation</span></span>
* <span data-ttu-id="cb73b-112">В Set-AzAutomationWebhook добавлен параметр -RunOn для определения группы гибридной рабочей роли.</span><span class="sxs-lookup"><span data-stu-id="cb73b-112">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb73b-113">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb73b-113">Az.Compute</span></span>
* <span data-ttu-id="cb73b-114">В New-AzVm, New-AzVmss, New-AzVMConfig, New-AzVmssConfig, Update-AzVM и Update-AzVmss добавлен параметр -EncryptionAtHost.</span><span class="sxs-lookup"><span data-stu-id="cb73b-114">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="cb73b-115">В возвращаемый объект Get-AzVM и Get-AzVmss добавлен параметр SecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="cb73b-115">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="cb73b-116">В Get-AzHostGroup добавлен необязательный параметр -InstanceView.</span><span class="sxs-lookup"><span data-stu-id="cb73b-116">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="cb73b-117">Добавлен новый командлет Invoke-AzVmPatchAssessment.</span><span class="sxs-lookup"><span data-stu-id="cb73b-117">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb73b-118">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb73b-118">Az.DataFactory</span></span>
* <span data-ttu-id="cb73b-119">В класс PSPipelineRun добавлены отсутствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="cb73b-119">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cb73b-120">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cb73b-120">Az.HDInsight</span></span>
* <span data-ttu-id="cb73b-121">Включена поддержка создания кластера с функцией шифрования на узле.</span><span class="sxs-lookup"><span data-stu-id="cb73b-121">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cb73b-122">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb73b-122">Az.KeyVault</span></span>
* <span data-ttu-id="cb73b-123">Добавлены предупреждающие сообщения для планирования отключения обратимого удаления.</span><span class="sxs-lookup"><span data-stu-id="cb73b-123">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="cb73b-124">Добавлены предупреждающие сообщения для планирования удаления атрибута SecretValueText.</span><span class="sxs-lookup"><span data-stu-id="cb73b-124">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="cb73b-125">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="cb73b-125">Az.Maintenance</span></span>
* <span data-ttu-id="cb73b-126">В New-AzMaintenanceConfiguration добавлены дополнительные поля, связанные с расписанием.</span><span class="sxs-lookup"><span data-stu-id="cb73b-126">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="cb73b-127">Добавлен новый командлет для Get-AzMaintenancePublicConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cb73b-127">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="cb73b-128">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-128">Az.ManagedServices</span></span>
* <span data-ttu-id="cb73b-129">Добавлены предупреждения о критических изменениях в командлетах назначения и определения управляемых служб.</span><span class="sxs-lookup"><span data-stu-id="cb73b-129">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb73b-130">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb73b-130">Az.Monitor</span></span>
* <span data-ttu-id="cb73b-131">Расширен набор параметров, заданный в Set-AzDiagnosticSetting, для разделения включения журналов и метрик [№ 12482].</span><span class="sxs-lookup"><span data-stu-id="cb73b-131">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="cb73b-132">Для Add-AzMetricAlertRuleV2 исправлена ошибка, возникающая при получении оповещения метрики из конвейера.</span><span class="sxs-lookup"><span data-stu-id="cb73b-132">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb73b-133">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb73b-133">Az.Resources</span></span>
* <span data-ttu-id="cb73b-134">Изменен ответ Get-AzPolicyAlias для включения сведений о том, изменяется ли этот псевдоним Политикой Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-134">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="cb73b-135">Создан новый командлет Set-AzRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="cb73b-135">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="cb73b-136">Добавлен командлет Get-AzDeploymentManagementGroupWhatIfResult для получения результатов выполнения What-If в шаблоне ARM в области группы управления.</span><span class="sxs-lookup"><span data-stu-id="cb73b-136">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="cb73b-137">Добавлен командлет Get-AzTenantWhatIfResult для получения результатов выполнения What-If в шаблоне ARM в области арендатора.</span><span class="sxs-lookup"><span data-stu-id="cb73b-137">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="cb73b-138">Переопределены параметры -WhatIf и -Confirm для New-AzManagementGroupDeployment и New-AzTenantDeployment для использования результатов выполнения What-If в шаблоне ARM.</span><span class="sxs-lookup"><span data-stu-id="cb73b-138">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="cb73b-139">Исправлено поведение параметров -WhatIf и -Confirm для новых командлетов развертывания, чтобы они соответствовали значению False.</span><span class="sxs-lookup"><span data-stu-id="cb73b-139">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="cb73b-140">Исправлена ошибка сериализации для -TemplateObject и TemplateParameterObject [№ 1528] [№ 6292].</span><span class="sxs-lookup"><span data-stu-id="cb73b-140">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="cb73b-141">Добавлен атрибут критического изменения в Get-AzResourceGroupDeploymentOperation для предстоящего изменения типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="cb73b-141">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="cb73b-142">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="cb73b-142">Az.SignalR</span></span>
* <span data-ttu-id="cb73b-143">Исправлены ошибки файлов справки Restart-AzSignalR и Update-AzSignalR.</span><span class="sxs-lookup"><span data-stu-id="cb73b-143">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="cb73b-144">Добавлены командлеты Update-AzSignalRNetworkAcl, Set-AzSignalRUpstream.</span><span class="sxs-lookup"><span data-stu-id="cb73b-144">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb73b-145">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb73b-145">Az.Storage</span></span>
* <span data-ttu-id="cb73b-146">Поддерживается ускорение запросов больших двоичных объектов:</span><span class="sxs-lookup"><span data-stu-id="cb73b-146">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="cb73b-147">Get-AzStorageBlobQueryResult;</span><span class="sxs-lookup"><span data-stu-id="cb73b-147">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="cb73b-148">New-AzStorageBlobQueryConfig.</span><span class="sxs-lookup"><span data-stu-id="cb73b-148">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="cb73b-149">Обновлен файл справки; дополнено описание и исправлена опечатка.</span><span class="sxs-lookup"><span data-stu-id="cb73b-149">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="cb73b-150">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="cb73b-150">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="cb73b-151">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="cb73b-151">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="cb73b-152">Исправлена ошибка, из-за которой работа большого двоичного объекта завершается ошибкой, если связанный подкаталог не существует [№ 12592].</span><span class="sxs-lookup"><span data-stu-id="cb73b-152">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="cb73b-153">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cb73b-153">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="cb73b-154">Включена поддержка задания, получения и удаления политики репликации объекта в учетных записях хранения:</span><span class="sxs-lookup"><span data-stu-id="cb73b-154">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="cb73b-155">New-AzStorageObjectReplicationPolicyRule;</span><span class="sxs-lookup"><span data-stu-id="cb73b-155">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="cb73b-156">Set-AzStorageObjectReplicationPolicy;</span><span class="sxs-lookup"><span data-stu-id="cb73b-156">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="cb73b-157">Get-AzStorageObjectReplicationPolicy;</span><span class="sxs-lookup"><span data-stu-id="cb73b-157">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="cb73b-158">Remove-AzStorageObjectReplicationPolicy.</span><span class="sxs-lookup"><span data-stu-id="cb73b-158">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="cb73b-159">Включена поддержка включения и отключения канала изменений в службе BLOB-объектов учетной записи хранения:</span><span class="sxs-lookup"><span data-stu-id="cb73b-159">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="cb73b-160">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="cb73b-160">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="cb73b-161">4.5.0 — август 2020 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-161">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb73b-162">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb73b-162">Az.Accounts</span></span>
* <span data-ttu-id="cb73b-163">Командлет Connect-AzAccount теперь принимает параметр MaxContextPopulation (№ 9865).</span><span class="sxs-lookup"><span data-stu-id="cb73b-163">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="cb73b-164">Версия SubscriptionClient обновлена до 2019-06-01 и поддерживает отображение доменов арендаторов (№ 9838).</span><span class="sxs-lookup"><span data-stu-id="cb73b-164">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="cb73b-165">Добавлена поддержка домашнего арендатора и сведений managedBy арендатора для подписки.</span><span class="sxs-lookup"><span data-stu-id="cb73b-165">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="cb73b-166">Исправлено имя модуля и сведения о версии в данных телеметрии.</span><span class="sxs-lookup"><span data-stu-id="cb73b-166">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="cb73b-167">Исправлено поведение SqlDatabaseDnsSuffix и ServiceManagementUrl, когда конечная точка метаданных среды возвращает несовместимое значение.</span><span class="sxs-lookup"><span data-stu-id="cb73b-167">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="cb73b-168">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cb73b-168">Az.Aks</span></span>
* <span data-ttu-id="cb73b-169">Параметр ClientIdAndSecret замен на ServicePrincipalIdAndSecret и задан в виде псевдонима (№ 12381).</span><span class="sxs-lookup"><span data-stu-id="cb73b-169">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="cb73b-170">Командлеты Get-AzAks, New-AzAks, Remove-AzAks, Set-AzAks заменены на Get-AzAksCluster, New-AzAksCluster, Remove-AzAksCluster, Set-AzAksCluster. Исходные командлеты заданы в виде псевдонимов (№ 12373).</span><span class="sxs-lookup"><span data-stu-id="cb73b-170">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cb73b-171">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb73b-171">Az.ApiManagement</span></span>
* <span data-ttu-id="cb73b-172">Добавлен новый командлет Add-AzApiManagementApiToGateway.</span><span class="sxs-lookup"><span data-stu-id="cb73b-172">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="cb73b-173">Добавлен новый командлет Get-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="cb73b-173">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="cb73b-174">Добавлен новый командлет Get-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cb73b-174">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="cb73b-175">Добавлен новый командлет Get-AzApiManagementGatewayKey.</span><span class="sxs-lookup"><span data-stu-id="cb73b-175">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="cb73b-176">Добавлен новый командлет New-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="cb73b-176">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="cb73b-177">Добавлен новый командлет New-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cb73b-177">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="cb73b-178">Добавлен новый командлет New-AzApiManagementResourceLocationObject.</span><span class="sxs-lookup"><span data-stu-id="cb73b-178">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="cb73b-179">Добавлен новый командлет Remove-AzApiManagementApiFromGateway.</span><span class="sxs-lookup"><span data-stu-id="cb73b-179">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="cb73b-180">Добавлен новый командлет Remove-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="cb73b-180">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="cb73b-181">Добавлен новый командлет Remove-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cb73b-181">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="cb73b-182">Добавлен новый командлет Update-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="cb73b-182">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="cb73b-183">Добавлен новый необязательный параметр [-GatewayId] в командлет Get-AzApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="cb73b-183">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cb73b-184">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-184">Az.CognitiveServices</span></span>
* <span data-ttu-id="cb73b-185">Задано явное использование действия "Отклонить" в качестве действия NetworkRules по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cb73b-185">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cb73b-186">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cb73b-186">Az.FrontDoor</span></span>
* <span data-ttu-id="cb73b-187">Исправлена проблема, связанная с возникновением исключения при попытке Enum.Parse привести значение NULL к значениям перечисления Enabled или Disabled (№ 12344).</span><span class="sxs-lookup"><span data-stu-id="cb73b-187">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cb73b-188">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cb73b-188">Az.HDInsight</span></span>
* <span data-ttu-id="cb73b-189">Добавлена поддержка создания кластера с функцией шифрования передаваемых данных.</span><span class="sxs-lookup"><span data-stu-id="cb73b-189">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="cb73b-190">Добавлен новый параметр EncryptionInTransit в командлет New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="cb73b-190">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="cb73b-191">Добавлен новый параметр EncryptionInTransit в командлет New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="cb73b-191">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="cb73b-192">Добавлена поддержка создания кластера с функцией приватного канала:</span><span class="sxs-lookup"><span data-stu-id="cb73b-192">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="cb73b-193">Добавлен новый параметр PublicNetworkAccessType и OutboundPublicNetworkAccessType в командлет New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="cb73b-193">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="cb73b-194">Добавлен новый параметр PublicNetworkAccessType и OutboundPublicNetworkAccessType в командлет New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="cb73b-194">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="cb73b-195">Реализовано возвращение сведений о виртуальной сети при вызове New-AzHDInsightCluster или Get-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="cb73b-195">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb73b-196">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb73b-196">Az.Network</span></span>
* <span data-ttu-id="cb73b-197">Включена поддержка параметра AddressPrefixType в Remove-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="cb73b-197">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="cb73b-198">Реализованы некритические изменения: функциональность PeerAddressType для частного пиринга в Remove-AzExpressRouteCircutPeeringConfig.</span><span class="sxs-lookup"><span data-stu-id="cb73b-198">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="cb73b-199">Код изменен для игнорирования регистра в параметрах AddressPrefixType и PeerAddressType.</span><span class="sxs-lookup"><span data-stu-id="cb73b-199">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="cb73b-200">Изменено сообщение с предупреждением для New-AzLoadBalancerFrontendIpConfig, New-AzPublicIpAddress и New-AzPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="cb73b-200">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cb73b-201">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cb73b-201">Az.OperationalInsights</span></span>
* <span data-ttu-id="cb73b-202">Добавлен параметр -ForceDelete для Remove-AzOperationalInsightsworkspace.</span><span class="sxs-lookup"><span data-stu-id="cb73b-202">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="cb73b-203">Добавлен новый командлет Get-AzOperationalInsightsDeletedWorkspace.</span><span class="sxs-lookup"><span data-stu-id="cb73b-203">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="cb73b-204">Добавлен новый командлет Restore-AzOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="cb73b-204">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb73b-205">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-205">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb73b-206">Улучшена работа с обнаружением контейнеров и элементов Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="cb73b-206">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb73b-207">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb73b-207">Az.Resources</span></span>
* <span data-ttu-id="cb73b-208">Добавлены свойства Condition, ConditionVersion и Description в New-AzRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="cb73b-208">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="cb73b-209">Это касается всех соответствующих изменений моделей данных.</span><span class="sxs-lookup"><span data-stu-id="cb73b-209">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb73b-210">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb73b-210">Az.Sql</span></span>
* <span data-ttu-id="cb73b-211">Исправлена ошибка, связанная с потенциальным игнорированием регистра имени сервера в New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="cb73b-211">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="cb73b-212">Исправлена ошибка, из-за которой возвращалось неправильное имя существующей базы данных в New-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="cb73b-212">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb73b-213">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb73b-213">Az.Storage</span></span>
* <span data-ttu-id="cb73b-214">Добавлена поддержка создания маркера SAS контейнера и BLOB-объекта с новым разрешением x,t.</span><span class="sxs-lookup"><span data-stu-id="cb73b-214">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="cb73b-215">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="cb73b-215">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="cb73b-216">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="cb73b-216">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="cb73b-217">Добавлена поддержка создания маркера SAS учетной записи с новым разрешением x,t,f.</span><span class="sxs-lookup"><span data-stu-id="cb73b-217">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="cb73b-218">New-AzStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="cb73b-218">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="cb73b-219">Добавлена поддержка получения данных об использовании одной общей папки.</span><span class="sxs-lookup"><span data-stu-id="cb73b-219">Supported get single file share usage</span></span>
    - <span data-ttu-id="cb73b-220">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="cb73b-220">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="cb73b-221">4.4.0 — июль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-221">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb73b-222">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb73b-222">Az.Accounts</span></span>
* <span data-ttu-id="cb73b-223">Добавлен новый командлет Invoke-AzRestMethod.</span><span class="sxs-lookup"><span data-stu-id="cb73b-223">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="cb73b-224">Устранена неполадка, из-за которой могли возникать ошибки с проверкой подлинности в сценариях с несколькими процессами, такими как выполнение нескольких командлетов Azure PowerShell с помощью Start-Job [№ 9448].</span><span class="sxs-lookup"><span data-stu-id="cb73b-224">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="cb73b-225">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cb73b-225">Az.Aks</span></span>
* <span data-ttu-id="cb73b-226">Исправлена ошибка, из-за которой Get-AzAks выводит не все кластеры [ №12296].</span><span class="sxs-lookup"><span data-stu-id="cb73b-226">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="cb73b-227">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-227">Az.AnalysisServices</span></span>
* <span data-ttu-id="cb73b-228">Удалена ссылка на проект для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="cb73b-228">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb73b-229">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb73b-229">Az.Automation</span></span>
* <span data-ttu-id="cb73b-230">Исправлена ошибка, из-за которой строка с escape-символами не преобразовывалась в объект JSON.</span><span class="sxs-lookup"><span data-stu-id="cb73b-230">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb73b-231">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb73b-231">Az.Compute</span></span>
* <span data-ttu-id="cb73b-232">Добавлено предупреждение, которое отображается при использовании New-AzVmss, если версия образа не является последней.</span><span class="sxs-lookup"><span data-stu-id="cb73b-232">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb73b-233">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb73b-233">Az.DataFactory</span></span>
* <span data-ttu-id="cb73b-234">Добавлены глобальные параметры в Фабрику данных.</span><span class="sxs-lookup"><span data-stu-id="cb73b-234">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="cb73b-235">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="cb73b-235">Az.EventGrid</span></span>
* <span data-ttu-id="cb73b-236">Обновлен модуль для использования API версии 2020-06-01.</span><span class="sxs-lookup"><span data-stu-id="cb73b-236">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="cb73b-237">Добавлены новые возможности:</span><span class="sxs-lookup"><span data-stu-id="cb73b-237">Added new features:</span></span>
    - <span data-ttu-id="cb73b-238">сопоставление входных данных;</span><span class="sxs-lookup"><span data-stu-id="cb73b-238">Input mapping</span></span>
    - <span data-ttu-id="cb73b-239">схема доставки событий;</span><span class="sxs-lookup"><span data-stu-id="cb73b-239">Event Delivery Schema</span></span>
    - <span data-ttu-id="cb73b-240">Приватный канал</span><span class="sxs-lookup"><span data-stu-id="cb73b-240">Private Link</span></span>
    - <span data-ttu-id="cb73b-241">схема событий облака (версия 1.0);</span><span class="sxs-lookup"><span data-stu-id="cb73b-241">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="cb73b-242">раздел служебной шины как назначение;</span><span class="sxs-lookup"><span data-stu-id="cb73b-242">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="cb73b-243">функция Azure как назначение;</span><span class="sxs-lookup"><span data-stu-id="cb73b-243">Azure Function As Destination</span></span>
    - <span data-ttu-id="cb73b-244">пакетная обработка данных веб-перехватчика;</span><span class="sxs-lookup"><span data-stu-id="cb73b-244">WebHook Batching</span></span>
    - <span data-ttu-id="cb73b-245">безопасный веб-перехватчик (поддержка AAD);</span><span class="sxs-lookup"><span data-stu-id="cb73b-245">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="cb73b-246">фильтрация IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="cb73b-246">IpFiltering</span></span>
* <span data-ttu-id="cb73b-247">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="cb73b-247">Updated cmdlets:</span></span>
    - <span data-ttu-id="cb73b-248">New-AzEventGridSubscription или Update-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="cb73b-248">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="cb73b-249">Добавлены новые необязательные параметры для поддержки пакетной обработки данных веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="cb73b-249">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="cb73b-250">Добавлены новые необязательные параметры для поддержки безопасного веб-перехватчика с использованием AAD.</span><span class="sxs-lookup"><span data-stu-id="cb73b-250">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="cb73b-251">Добавлено новое перечисление для параметра EndpointType, чтобы обеспечить поддержку функции Azure и раздела служебной шины в качестве назначения.</span><span class="sxs-lookup"><span data-stu-id="cb73b-251">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="cb73b-252">Добавлен новый необязательный параметр для схемы доставки.</span><span class="sxs-lookup"><span data-stu-id="cb73b-252">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="cb73b-253">New-AzEventGridTopic или Update-AzEventGridTopic и New-AzEventGridDomain или Update-AzEventGridDomain:</span><span class="sxs-lookup"><span data-stu-id="cb73b-253">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="cb73b-254">Добавлены новые необязательные параметры для поддержки фильтрации IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="cb73b-254">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="cb73b-255">New-AzEventGridTopic или New-AzEventGridDomain:</span><span class="sxs-lookup"><span data-stu-id="cb73b-255">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="cb73b-256">Добавлены новые необязательные параметры для поддержки сопоставления входных данных.</span><span class="sxs-lookup"><span data-stu-id="cb73b-256">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cb73b-257">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cb73b-257">Az.FrontDoor</span></span>
* <span data-ttu-id="cb73b-258">Обновлен модуль для использования API версии 2020-05-01.</span><span class="sxs-lookup"><span data-stu-id="cb73b-258">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="cb73b-259">Включена поддержка Приватного канала для ресурсов службы хранилища, Key Vault и службы веб-приложений.</span><span class="sxs-lookup"><span data-stu-id="cb73b-259">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cb73b-260">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cb73b-260">Az.HDInsight</span></span>
* <span data-ttu-id="cb73b-261">Включена поддержка создания кластера с хранилищем ADLS 1-го и 2-го поколения в национальных облаках.</span><span class="sxs-lookup"><span data-stu-id="cb73b-261">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb73b-262">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb73b-262">Az.Monitor</span></span>
* <span data-ttu-id="cb73b-263">Исправлена ошибка с Get-AzDiagnosticSetting, связанная с присвоением значения NULL метрикам или журналам [№ 12272].</span><span class="sxs-lookup"><span data-stu-id="cb73b-263">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb73b-264">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb73b-264">Az.Network</span></span>
* <span data-ttu-id="cb73b-265">Исправлены ошибки с переключением параметров для подключения виртуальной сети концентратора к глобальной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="cb73b-265">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="cb73b-266">Добавлены новые командлеты для сайтов сетевых виртуальных модулей Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-266">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="cb73b-267">Get-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="cb73b-267">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="cb73b-268">New-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="cb73b-268">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="cb73b-269">Remove-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="cb73b-269">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="cb73b-270">Update-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="cb73b-270">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="cb73b-271">New-AzOffice365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="cb73b-271">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="cb73b-272">Добавлены новые командлеты для сетевого виртуального модуля Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-272">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="cb73b-273">Get-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="cb73b-273">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="cb73b-274">New-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="cb73b-274">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="cb73b-275">Remove-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="cb73b-275">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="cb73b-276">Update-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="cb73b-276">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="cb73b-277">Get-AzNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="cb73b-277">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="cb73b-278">New-AzVirtualApplianceSkuProperty</span><span class="sxs-lookup"><span data-stu-id="cb73b-278">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="cb73b-279">Общие командлеты для Шлюза приложений, подключенного к Приватному каналу.</span><span class="sxs-lookup"><span data-stu-id="cb73b-279">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="cb73b-280">Общие командлеты для службы синхронизации хранилища, подключенной к Приватному каналу.</span><span class="sxs-lookup"><span data-stu-id="cb73b-280">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="cb73b-281">Общие командлеты для службы SignalR, подключенной к Приватному каналу.</span><span class="sxs-lookup"><span data-stu-id="cb73b-281">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb73b-282">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-282">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb73b-283">Удалена ссылка на проект для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="cb73b-283">Removed project reference to Authentication</span></span>
* <span data-ttu-id="cb73b-284">В Azure Backup представлена более точная справка по командлетам.</span><span class="sxs-lookup"><span data-stu-id="cb73b-284">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="cb73b-285">В Azure Backup включена поддержка выборки заданий агента MAB с помощью командлета Get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="cb73b-285">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb73b-286">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb73b-286">Az.Resources</span></span>
* <span data-ttu-id="cb73b-287">Обновлен командлет Save-AzResourceGroupDeploymentTemplate для использования пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="cb73b-287">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="cb73b-288">Добавлен командлет Unregister-AzResourceProvider.</span><span class="sxs-lookup"><span data-stu-id="cb73b-288">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb73b-289">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb73b-289">Az.Sql</span></span>
* <span data-ttu-id="cb73b-290">Включена поддержка субъекта-службы и гостевых пользователей для командлета Set-AzSqlInstanceActiveDirectoryAdministrator.</span><span class="sxs-lookup"><span data-stu-id="cb73b-290">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="cb73b-291">Исправлена ошибка в командлетах классификации данных.</span><span class="sxs-lookup"><span data-stu-id="cb73b-291">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="cb73b-292">Включена поддержка отработки отказа Управляемого экземпляра SQL Azure. Invoke-AzSqlInstanceFailover</span><span class="sxs-lookup"><span data-stu-id="cb73b-292">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb73b-293">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb73b-293">Az.Storage</span></span>
* <span data-ttu-id="cb73b-294">Исправлена ошибка, из-за которой в некоторых командлетах плоскости данных не добавлялся объект UserAgent.</span><span class="sxs-lookup"><span data-stu-id="cb73b-294">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="cb73b-295">Включена поддержка создания и обновления учетной записи хранения с использованием MinimumTlsVersion и AllowBlobPublicAccess.</span><span class="sxs-lookup"><span data-stu-id="cb73b-295">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="cb73b-296">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb73b-296">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="cb73b-297">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb73b-297">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="cb73b-298">Включена поддержка включения и отключения управления версиями в службе BLOB-объектов учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="cb73b-298">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="cb73b-299">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="cb73b-299">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="cb73b-300">Включена поддержка вывода списка BLOB-объектов с данными о версиях BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="cb73b-300">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="cb73b-301">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="cb73b-301">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="cb73b-302">Включена поддержка получения или удаления одного моментального снимка BLOB-объекта или версии BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="cb73b-302">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="cb73b-303">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="cb73b-303">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="cb73b-304">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="cb73b-304">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="cb73b-305">Включена поддержка конвейера на основе BLOB-объекта, созданного с помощью Azure.Storage.Blobs версии 12.</span><span class="sxs-lookup"><span data-stu-id="cb73b-305">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="cb73b-306">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cb73b-306">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="cb73b-307">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="cb73b-307">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="cb73b-308">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="cb73b-308">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="cb73b-309">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cb73b-309">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="cb73b-310">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="cb73b-310">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="cb73b-311">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="cb73b-311">Az.StorageSync</span></span>
* <span data-ttu-id="cb73b-312">Добавлена новая версия пакета SDK StorageSync, предназначенная для API версии 2020-03-01.</span><span class="sxs-lookup"><span data-stu-id="cb73b-312">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="cb73b-313">Добавлен командлет для обновления службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="cb73b-313">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="cb73b-314">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="cb73b-314">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="cb73b-315">Добавлены классы IncomingTrafficPolicy и IncomingTrafficPolicy в командлеты службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="cb73b-315">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb73b-316">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb73b-316">Az.Websites</span></span>
* <span data-ttu-id="cb73b-317">Включена поддержка выполнения операций для слотов, которые находятся не в той же группе ресурсов, что и план службы приложений.</span><span class="sxs-lookup"><span data-stu-id="cb73b-317">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="cb73b-318">4.3.0 — июнь 2020 года</span><span class="sxs-lookup"><span data-stu-id="cb73b-318">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb73b-319">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb73b-319">Az.Accounts</span></span>
* <span data-ttu-id="cb73b-320">Включена поддержка обнаружения параметров среды по умолчанию и добавления окружения с помощью командлета Add-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="cb73b-320">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="cb73b-321">Обновлены предварительно загруженные сборки [№ 12024], [№ 11976].</span><span class="sxs-lookup"><span data-stu-id="cb73b-321">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="cb73b-322">Обновлена сборка Azure.Core.</span><span class="sxs-lookup"><span data-stu-id="cb73b-322">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="cb73b-323">Исправлена ошибка, из-за которой выполнение Connect-AzAccount может завершаться сбоем при многопоточном выполнении [№ 11201].</span><span class="sxs-lookup"><span data-stu-id="cb73b-323">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="cb73b-324">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cb73b-324">Az.Aks</span></span>
* <span data-ttu-id="cb73b-325">Заменено использование старого [API AccessProfile](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) вызовами API [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) и [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials).</span><span class="sxs-lookup"><span data-stu-id="cb73b-325">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="cb73b-326">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cb73b-326">Az.Batch</span></span>
* <span data-ttu-id="cb73b-327">Изменена версия SDK для Microsoft.Azure.Management.Batch для Az.Batch на 11.0.0.</span><span class="sxs-lookup"><span data-stu-id="cb73b-327">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="cb73b-328">Включена возможность задать удостоверение BatchAccount в командлете New-AzBatchAccount.</span><span class="sxs-lookup"><span data-stu-id="cb73b-328">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cb73b-329">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-329">Az.CognitiveServices</span></span>
* <span data-ttu-id="cb73b-330">Включена поддержка отображения возможностей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="cb73b-330">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="cb73b-331">Включена поддержка изменения PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="cb73b-331">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb73b-332">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb73b-332">Az.Compute</span></span>
* <span data-ttu-id="cb73b-333">Добавлен параметр SimulateEviction в командлеты Set-AzVM и Set-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="cb73b-333">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="cb73b-334">Добавлен фрагмент Premium_LRS в средство заполнения аргументов параметра StorageAccountType для командлета New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="cb73b-334">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="cb73b-335">Добавлены подсостояния для VMCustomScriptExtension [№ 11297].</span><span class="sxs-lookup"><span data-stu-id="cb73b-335">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="cb73b-336">Добавлен фрагмент Delete в средство заполнения аргументов параметра EvictionPolicy для командлетов New-AzVM и New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="cb73b-336">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="cb73b-337">Исправлено имя нового расширения виртуальной машины для SAP.</span><span class="sxs-lookup"><span data-stu-id="cb73b-337">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb73b-338">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb73b-338">Az.DataFactory</span></span>
* <span data-ttu-id="cb73b-339">Обновлен пакет SDK ADF для .NET до версии 4.9.0.</span><span class="sxs-lookup"><span data-stu-id="cb73b-339">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cb73b-340">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cb73b-340">Az.EventHub</span></span>
* <span data-ttu-id="cb73b-341">Добавлены параметры управляемого удостоверения для командлетов New-AzEventHubNamespace и Set-AzEventHubNamespace.</span><span class="sxs-lookup"><span data-stu-id="cb73b-341">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="cb73b-342">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="cb73b-342">Az.Functions</span></span>
* <span data-ttu-id="cb73b-343">Включена поддержка создания приложений-функций PowerShell 7.0 и Java 11.</span><span class="sxs-lookup"><span data-stu-id="cb73b-343">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cb73b-344">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cb73b-344">Az.HDInsight</span></span>
* <span data-ttu-id="cb73b-345">Включена поддержка перечисления узлов и перезагрузка отдельных узлов кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="cb73b-345">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="cb73b-346">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="cb73b-346">Az.HealthcareApis</span></span>
* <span data-ttu-id="cb73b-347">Обновлен пакет SDK до версии 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="cb73b-347">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="cb73b-348">Включена поддержка параметров экспорта и управляемого удостоверения.</span><span class="sxs-lookup"><span data-stu-id="cb73b-348">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb73b-349">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb73b-349">Az.Monitor</span></span>
* <span data-ttu-id="cb73b-350">Исправлен входной параметр объекта для Set-AzActivityLogAlert.</span><span class="sxs-lookup"><span data-stu-id="cb73b-350">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="cb73b-351">Исправлен параметр InputObject для Set-AzActionGroup [№ 10868].</span><span class="sxs-lookup"><span data-stu-id="cb73b-351">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb73b-352">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb73b-352">Az.Network</span></span>
* <span data-ttu-id="cb73b-353">Включена поддержка параметра AddressPrefixType в Remove-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="cb73b-353">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="cb73b-354">Добавлены новые командлеты для политики Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-354">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="cb73b-355">New-AzFirewallPolicyDnsSetting</span><span class="sxs-lookup"><span data-stu-id="cb73b-355">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="cb73b-356">Включена поддержка полного доменного имени назначения в правилах сети для политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="cb73b-356">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="cb73b-357">Включена поддержка операций серверного пула адресов:</span><span class="sxs-lookup"><span data-stu-id="cb73b-357">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="cb73b-358">New-AzLoadBalancerBackendAddressConfig</span><span class="sxs-lookup"><span data-stu-id="cb73b-358">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="cb73b-359">New-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="cb73b-359">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="cb73b-360">Set-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="cb73b-360">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="cb73b-361">Remove-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="cb73b-361">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="cb73b-362">Get-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="cb73b-362">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="cb73b-363">Добавлена проверка имени для New-AzIpGroup.</span><span class="sxs-lookup"><span data-stu-id="cb73b-363">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="cb73b-364">Добавлены новые командлеты для политики Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-364">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="cb73b-365">New-AzFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="cb73b-365">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="cb73b-366">Обновлены следующие команды для функции: Включена возможность настройки и удаления пользовательских DNS-серверов в шлюзе VPN P2S виртуальной глобальной сети.</span><span class="sxs-lookup"><span data-stu-id="cb73b-366">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="cb73b-367">Обновлен командлет New-AzP2sVpnGateway: добавлен необязательный параметр -CustomDnsServer, чтобы пользователи могли указывать свои DNS-серверы для настройки в шлюзе VPN P2S для использования клиентами с подключением "точка — сеть".</span><span class="sxs-lookup"><span data-stu-id="cb73b-367">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="cb73b-368">Обновлен командлет Update-AzP2sVpnGateway: добавлен необязательный параметр -CustomDnsServer, чтобы пользователи могли указывать свои DNS-серверы для настройки в шлюзе VPN P2S для использования клиентами с подключением "точка — сеть".</span><span class="sxs-lookup"><span data-stu-id="cb73b-368">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="cb73b-369">Обновлен командлет Update-AzVpnGateway:</span><span class="sxs-lookup"><span data-stu-id="cb73b-369">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="cb73b-370">добавлен необязательный параметр -BgpPeeringAddress, чтобы клиенты могли указывать пользовательские маршруты BGP для настройки в шлюзе VPN.</span><span class="sxs-lookup"><span data-stu-id="cb73b-370">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="cb73b-371">Добавлен новый командлет для сброса состояния маршрутизации ресурса VirtualHub:</span><span class="sxs-lookup"><span data-stu-id="cb73b-371">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="cb73b-372">Reset-AzHubRouter</span><span class="sxs-lookup"><span data-stu-id="cb73b-372">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="cb73b-373">Следующие обновления основаны на последнем изменении Swagger для политики брандмауэра:</span><span class="sxs-lookup"><span data-stu-id="cb73b-373">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="cb73b-374">изменены имена для RuleGroup, RuleCollectionGroup и RuleType;</span><span class="sxs-lookup"><span data-stu-id="cb73b-374">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="cb73b-375">включена поддержка коллекций правил NAT политики брандмауэра для поддержки нескольких коллекций правил NAT.</span><span class="sxs-lookup"><span data-stu-id="cb73b-375">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="cb73b-376">[Критическое изменение] Добавлен обязательный параметр SourceIpGroup для командлетов New-AzFirewallPolicyApplicationRule и New-AzFirewallPolicyNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="cb73b-376">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="cb73b-377">[Критическое изменение] Параметр SourceAddress для командлета New-AzFirewallPolicyApplicationRule сделан обязательным.</span><span class="sxs-lookup"><span data-stu-id="cb73b-377">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="cb73b-378">[Критическое изменение] Параметр SourceAddress для командлета New-AzFirewallPolicyApplicationRule сделан обязательным.</span><span class="sxs-lookup"><span data-stu-id="cb73b-378">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="cb73b-379">[Критическое изменение] Удалены обязательные параметры: TranslatedAddress и TranslatedPort для командлета New-AzFirewallPolicyNatRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="cb73b-379">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="cb73b-380">Добавлены новые командлеты для поддержки Приватного канала в Шлюзе приложений:</span><span class="sxs-lookup"><span data-stu-id="cb73b-380">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="cb73b-381">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb73b-381">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="cb73b-382">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb73b-382">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="cb73b-383">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb73b-383">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="cb73b-384">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb73b-384">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="cb73b-385">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb73b-385">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="cb73b-386">New-AzApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb73b-386">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="cb73b-387">Добавлены новые командлеты для дочернего ресурса HubRouteTables VirtualHub:</span><span class="sxs-lookup"><span data-stu-id="cb73b-387">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="cb73b-388">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="cb73b-388">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="cb73b-389">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="cb73b-389">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="cb73b-390">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="cb73b-390">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="cb73b-391">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="cb73b-391">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="cb73b-392">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="cb73b-392">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="cb73b-393">Обновлены существующие командлеты для включения поддержки необязательного входного параметра RoutingConfiguration для настраиваемой маршрутизации в виртуальной глобальной сети.</span><span class="sxs-lookup"><span data-stu-id="cb73b-393">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="cb73b-394">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="cb73b-394">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="cb73b-395">Set-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="cb73b-395">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="cb73b-396">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="cb73b-396">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="cb73b-397">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="cb73b-397">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="cb73b-398">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="cb73b-398">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="cb73b-399">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="cb73b-399">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="cb73b-400">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="cb73b-400">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="cb73b-401">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="cb73b-401">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cb73b-402">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cb73b-402">Az.OperationalInsights</span></span>
* <span data-ttu-id="cb73b-403">Исправлена ошибка, из-за которой PSWorkspace не реализует IOperationalInsightsWorkspace [№ 12135].</span><span class="sxs-lookup"><span data-stu-id="cb73b-403">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="cb73b-404">Добавлено значение pergb2018 в действительный набор значений параметра Sku в командлете Set-AzOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="cb73b-404">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="cb73b-405">Добавлен псевдоним FunctionParameters для параметра FunctionParameter:</span><span class="sxs-lookup"><span data-stu-id="cb73b-405">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="cb73b-406">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="cb73b-406">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="cb73b-407">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="cb73b-407">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb73b-408">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-408">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb73b-409">Включена поддержка выборки элементов MAB в Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="cb73b-409">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="cb73b-410">Включена поддержка типа диска StandardSSD_LRS в Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="cb73b-410">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb73b-411">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb73b-411">Az.Resources</span></span>
* <span data-ttu-id="cb73b-412">Добавлены параметры UsageLocation, GivenName, Surname, AccountEnabled, MailNickname, Mail для PSADUser [№ 10526], [№ 10497].</span><span class="sxs-lookup"><span data-stu-id="cb73b-412">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="cb73b-413">Исправлена ошибка, из-за которой параметр -Mail не работает в командлете Get-AzADUser [№ 11981].</span><span class="sxs-lookup"><span data-stu-id="cb73b-413">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="cb73b-414">Добавлен параметр -ExcludeChangeType в командлеты Get-AzDeploymentWhatIfResult и Get-AzResourceGroupDeploymentWhatIfResult.</span><span class="sxs-lookup"><span data-stu-id="cb73b-414">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="cb73b-415">Добавлен параметр -WhatIfExcludeChangeType в командлеты New-AzDeployment и New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="cb73b-415">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="cb73b-416">Обновлены командлеты Test-Az\*Deployment для отображения улучшенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="cb73b-416">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="cb73b-417">Исправлено справочное сообщение для параметра -Name в командлетах создания развертывания и командлетах What-If.</span><span class="sxs-lookup"><span data-stu-id="cb73b-417">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb73b-418">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb73b-418">Az.Sql</span></span>
* <span data-ttu-id="cb73b-419">Включена поддержка субъекта-службы для командлета настройки администратора Azure Active Directory SQL Server.</span><span class="sxs-lookup"><span data-stu-id="cb73b-419">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="cb73b-420">Исправлена ошибка синхронизации в командлетах классификации данных.</span><span class="sxs-lookup"><span data-stu-id="cb73b-420">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="cb73b-421">Включена поддержка поиска пользователей по адресу электронной почты в командлете Set-AzSqlServerActiveDirectoryAdministrator [№ 12192].</span><span class="sxs-lookup"><span data-stu-id="cb73b-421">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb73b-422">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb73b-422">Az.Storage</span></span>
* <span data-ttu-id="cb73b-423">Включена поддержка создания учетной записи хранения с помощью RequireInfrastructureEncryption.</span><span class="sxs-lookup"><span data-stu-id="cb73b-423">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="cb73b-424">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb73b-424">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="cb73b-425">Перемещена логика загрузки Azure.Core в Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="cb73b-425">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb73b-426">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb73b-426">Az.Websites</span></span>
* <span data-ttu-id="cb73b-427">В командлет Restore-AzDeletedWebApp добавлена защитная мера при удалении созданного веб-приложения, если восстановление завершилось сбоем.</span><span class="sxs-lookup"><span data-stu-id="cb73b-427">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="cb73b-428">Добавлены параметры SourceWebApp.Location для командлетов New-AzWebApp и New-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="cb73b-428">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="cb73b-429">Исправлена ошибка, препятствующая изменению параметров контейнера в командлетах Set-AzWebApp и Set-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="cb73b-429">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="cb73b-430">Исправлена ошибка получения SiteConfig, когда параметр -Name не указан для командлета Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="cb73b-430">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="cb73b-431">Включена поддержка создания приложений ASP для Linux.</span><span class="sxs-lookup"><span data-stu-id="cb73b-431">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="cb73b-432">Добавлены исключения для клонирования в группах ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cb73b-432">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="cb73b-433">4.2.0 — июнь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-433">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb73b-434">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb73b-434">Az.Accounts</span></span>
* <span data-ttu-id="cb73b-435">Исправлена проблема, из-за которой модуль Az мог пропускать журналы в заданиях службы автоматизации или PowerShell [№ 11492].</span><span class="sxs-lookup"><span data-stu-id="cb73b-435">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="cb73b-436">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-436">Az.AnalysisServices</span></span>
* <span data-ttu-id="cb73b-437">Обновлена версия сборки командлетов плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="cb73b-437">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cb73b-438">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb73b-438">Az.ApiManagement</span></span>
* <span data-ttu-id="cb73b-439">Обновлена версия сборки командлетов управления службами.</span><span class="sxs-lookup"><span data-stu-id="cb73b-439">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="cb73b-440">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="cb73b-440">Az.Billing</span></span>
* <span data-ttu-id="cb73b-441">Обновлена версия сборки командлетов потребления.</span><span class="sxs-lookup"><span data-stu-id="cb73b-441">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cb73b-442">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-442">Az.CognitiveServices</span></span>
* <span data-ttu-id="cb73b-443">Реализована поддержка элементов управления PrivateEndpoint и PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="cb73b-443">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="cb73b-444">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb73b-444">Az.DataFactory</span></span>
* <span data-ttu-id="cb73b-445">Обновлена версия сборки командлетов фабрики данных версии 2.</span><span class="sxs-lookup"><span data-stu-id="cb73b-445">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="cb73b-446">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="cb73b-446">Az.DataShare</span></span>
* <span data-ttu-id="cb73b-447">Вышла общедоступная версия модуля Az.DataShare.</span><span class="sxs-lookup"><span data-stu-id="cb73b-447">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="cb73b-448">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="cb73b-448">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="cb73b-449">Вышла общедоступная версия модуля Az.DesktopVirtualization.</span><span class="sxs-lookup"><span data-stu-id="cb73b-449">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cb73b-450">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cb73b-450">Az.OperationalInsights</span></span>
* <span data-ttu-id="cb73b-451">Пакет SDK обновлен до версии 0.21.0.</span><span class="sxs-lookup"><span data-stu-id="cb73b-451">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="cb73b-452">Добавлены дополнительные параметры в следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="cb73b-452">Added optional parameters to</span></span> 
    - <span data-ttu-id="cb73b-453">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="cb73b-453">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="cb73b-454">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="cb73b-454">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cb73b-455">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cb73b-455">Az.PolicyInsights</span></span>
* <span data-ttu-id="cb73b-456">Исправлен пример 3 для командлета Start-AzPolicyComplianceScan.</span><span class="sxs-lookup"><span data-stu-id="cb73b-456">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="cb73b-457">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="cb73b-457">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="cb73b-458">Обновлена версия сборки командлетов PowerBI.</span><span class="sxs-lookup"><span data-stu-id="cb73b-458">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="cb73b-459">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="cb73b-459">Az.PrivateDns</span></span>
* <span data-ttu-id="cb73b-460">Исправлено форматирование строки с подробными выходными данными командлета Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="cb73b-460">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb73b-461">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-461">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb73b-462">Реализована поддержка Azure Site Recovery для создания плана восстановления и репликации между зонами из входного XML-файла.</span><span class="sxs-lookup"><span data-stu-id="cb73b-462">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="cb73b-463">Обновлена версия сборки командлетов SiteRecovery и Backup.</span><span class="sxs-lookup"><span data-stu-id="cb73b-463">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb73b-464">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb73b-464">Az.Resources</span></span>
* <span data-ttu-id="cb73b-465">Добавлен параметр Tail в командлеты Get-AzDeploymentScriptLog и Save-AzDeploymentScriptLog.</span><span class="sxs-lookup"><span data-stu-id="cb73b-465">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="cb73b-466">Отформатировано свойство Output и включено в отображаемые выходные данные командлета Get-AzDeploymentScript.</span><span class="sxs-lookup"><span data-stu-id="cb73b-466">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="cb73b-467">Параметр -DeploymentScriptInputObject переименован в -DeploymentScriptObject.</span><span class="sxs-lookup"><span data-stu-id="cb73b-467">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="cb73b-468">Исправлена ошибка с отсутствующими именами файлов или целевых объектов в сообщениях командлетов.</span><span class="sxs-lookup"><span data-stu-id="cb73b-468">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="cb73b-469">Обновлена версия сборки командлетов диспетчера ресурсов и обработчика тегов.</span><span class="sxs-lookup"><span data-stu-id="cb73b-469">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb73b-470">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb73b-470">Az.Sql</span></span>
* <span data-ttu-id="cb73b-471">Добавлен параметр UsePrivateLinkConnection в командлеты New-AzSqlSyncGroup, Update-AzSqlSyncGroup, New-AzSqlSyncMember и Update-AzSqlSyncMember.</span><span class="sxs-lookup"><span data-stu-id="cb73b-471">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="cb73b-472">Добавлен параметр SyncMemberAzureDatabaseResourceId в командлеты New-AzSqlSyncMember и Update-AzSqlSyncMember.</span><span class="sxs-lookup"><span data-stu-id="cb73b-472">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="cb73b-473">Реализована поддержка поиска гостевых пользователей в командлете для настройки администратора Active Directory в SQL Server Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-473">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb73b-474">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb73b-474">Az.Storage</span></span>
* <span data-ttu-id="cb73b-475">Обновлена версия сборки командлетов плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="cb73b-475">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="cb73b-476">4.1.0 — май 2020 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-476">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="cb73b-477">Основные сведения о новых возможностях с момента последнего выпуска</span><span class="sxs-lookup"><span data-stu-id="cb73b-477">Highlights since the last release</span></span>
* <span data-ttu-id="cb73b-478">Поддерживаемые версии PowerShell: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="cb73b-478">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="cb73b-479">Вышла общедоступная версия модуля Az.Functions.</span><span class="sxs-lookup"><span data-stu-id="cb73b-479">General availability of Az.Functions</span></span> 
* <span data-ttu-id="cb73b-480">Состоялся основной выпуск Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources и Az.Storage.</span><span class="sxs-lookup"><span data-stu-id="cb73b-480">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cb73b-481">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb73b-481">Az.Accounts</span></span>
* <span data-ttu-id="cb73b-482">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметры AzureSynapseAnalyticsEndpointResourceId и AzureSynapseAnalyticsEndpointSuffix.</span><span class="sxs-lookup"><span data-stu-id="cb73b-482">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="cb73b-483">В Az.Accounts добавлены сборки, связанные с Azure.Core. Добавлена поддержка Windows PowerShell 5.1, PowerShell Core 6.2.4 и PowerShell 7+.</span><span class="sxs-lookup"><span data-stu-id="cb73b-483">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="cb73b-484">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cb73b-484">Az.Aks</span></span>
* <span data-ttu-id="cb73b-485">Версия API обновлена до 2019-10-01.</span><span class="sxs-lookup"><span data-stu-id="cb73b-485">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="cb73b-486">Добавлена возможность создания контейнера Windows в службе Azure Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="cb73b-486">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="cb73b-487">Добавлены новые командлеты: New-AzAksNodePool, Update-AzAksNodePool, Remove-AzAksNodePool, Get-AzAksNodePool, Install-AzAksKubectl, Get-AzAksVersion.</span><span class="sxs-lookup"><span data-stu-id="cb73b-487">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cb73b-488">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb73b-488">Az.ApiManagement</span></span>
* <span data-ttu-id="cb73b-489">В New-AzApiManagement и Set-AzApiManagement параметр -AssignIdentity переименован в -SystemAssignedIdentity.</span><span class="sxs-lookup"><span data-stu-id="cb73b-489">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="cb73b-490">В New-AzApiManagement и Set-AzApiManagement добавлен новый параметр -UserAssignedIdentity <строка[]>.</span><span class="sxs-lookup"><span data-stu-id="cb73b-490">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="cb73b-491">Командлет Get-AzApiManagementProperty переименован в Get-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="cb73b-491">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="cb73b-492">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="cb73b-492">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="cb73b-493">Командлет New-AzApiManagementProperty переименован в New-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="cb73b-493">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="cb73b-494">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="cb73b-494">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="cb73b-495">Командлет Set-AzApiManagementProperty переименован в Set-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="cb73b-495">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="cb73b-496">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="cb73b-496">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="cb73b-497">Командлет Remove-AzApiManagementProperty переименован в Remove-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="cb73b-497">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="cb73b-498">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="cb73b-498">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="cb73b-499">Добавлен новый командлет Get-AzApiManagementAuthorizationServerClientSecret, а Get-AzApiManagementAuthorizationServer теперь не возвращает секрет клиента.</span><span class="sxs-lookup"><span data-stu-id="cb73b-499">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="cb73b-500">Добавлен новый командлет Get-AzApiManagementNamedValueSecretValue, а Get-AzApiManagementNamedValue теперь не возвращает значение секрета.</span><span class="sxs-lookup"><span data-stu-id="cb73b-500">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="cb73b-501">Добавлен новый командлет Get-AzApiManagementOpenIdConnectProviderClientSecret, а Get-AzApiManagementOpenIdConnectProvider теперь не возвращает секрет клиента.</span><span class="sxs-lookup"><span data-stu-id="cb73b-501">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="cb73b-502">Добавлен новый командлет Get-AzApiManagementSubscriptionKey, а Get-AzApiManagementSubscription теперь не возвращает ключи подписки.</span><span class="sxs-lookup"><span data-stu-id="cb73b-502">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="cb73b-503">Добавлен новый командлет Get-AzApiManagementTenantAccessSecret, а Get-AzApiManagementTenantAccess теперь не возвращает ключи.</span><span class="sxs-lookup"><span data-stu-id="cb73b-503">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="cb73b-504">Добавлен новый командлет Get-AzApiManagementTenantGitAccessSecret, а Get-AzApiManagementTenantGitAccess теперь не возвращает ключи.</span><span class="sxs-lookup"><span data-stu-id="cb73b-504">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="cb73b-505">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="cb73b-505">Az.ApplicationInsights</span></span>
* <span data-ttu-id="cb73b-506">В New-AzApplicationInsights добавлены параметры RetentionInDays, PublicNetworkAccessForIngestion и PublicNetworkAccessForQuery.</span><span class="sxs-lookup"><span data-stu-id="cb73b-506">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="cb73b-507">Создан командлет Update-AzApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="cb73b-507">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="cb73b-508">Созданы командлеты для связанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="cb73b-508">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="cb73b-509">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cb73b-509">Az.Batch</span></span>
* <span data-ttu-id="cb73b-510">В командлеты Az.Batch добавлена поддержка пакетов SDK Microsoft.Azure.Batch версии 13.0.0 и SDK Microsoft.Azure.Management.Batch версии 9.0.0.</span><span class="sxs-lookup"><span data-stu-id="cb73b-510">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="cb73b-511">Теперь в New-AzBatchCertificate можно выбрать тип добавляемого сертификата с помощью нового параметра -CertificateKind.</span><span class="sxs-lookup"><span data-stu-id="cb73b-511">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="cb73b-512">В PSApplication удалено свойство ApplicationPackages.</span><span class="sxs-lookup"><span data-stu-id="cb73b-512">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="cb73b-513">Отдельные пакеты в приложении теперь можно извлечь с помощью Get-AzBatchApplicationPackage.</span><span class="sxs-lookup"><span data-stu-id="cb73b-513">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="cb73b-514">Пример: Get-AzBatchApplication -AccountName моя_учетная_запись -ResourceGroupName моя_группа_ресурсов -ApplicationId мое_приложение.</span><span class="sxs-lookup"><span data-stu-id="cb73b-514">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="cb73b-515">При создании пула с помощью New-AzBatchPool свойство VirtualMachineImageId элемента PSImageReference теперь может ссылаться только на образ из Общей коллекции образов.</span><span class="sxs-lookup"><span data-stu-id="cb73b-515">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="cb73b-516">При создании пула с помощью New-AzBatchPool пул можно подготовить без общедоступного IP-адреса, используя новое свойство PublicIPAddressConfiguration элемента PSNetworkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cb73b-516">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="cb73b-517">Свойство PublicIPs элемента PSNetworkConfiguration было передано элементу PSPublicIPAddressConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cb73b-517">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="cb73b-518">Это свойство можно указать, только если параметру IPAddressProvisioningType присвоено значение UserManaged.</span><span class="sxs-lookup"><span data-stu-id="cb73b-518">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb73b-519">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb73b-519">Az.Compute</span></span>
* <span data-ttu-id="cb73b-520">В командлет Update-AzVM добавлен параметр HostId.</span><span class="sxs-lookup"><span data-stu-id="cb73b-520">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="cb73b-521">Обновлена справочная документация по командлетам New-AzVMConfig, New-AzVmssConfig, Update-AzVmss, Set-AzVMOperatingSystem и Set-AzVmssOsProfile.</span><span class="sxs-lookup"><span data-stu-id="cb73b-521">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="cb73b-522">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="cb73b-522">Breaking changes</span></span>
    - <span data-ttu-id="cb73b-523">Параметр FilterExpression удален из командлета Get-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="cb73b-523">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="cb73b-524">Параметр AssignIdentity удален из командлетов New-AzVmssConfig, New-AzVMConfig и Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="cb73b-524">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="cb73b-525">Параметр AutomaticRepairMaxInstanceRepairsPercent удален из командлетов New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="cb73b-525">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="cb73b-526">Свойства AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus и VirtualMachineScaleSetsColocationStatus удалены из ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="cb73b-526">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="cb73b-527">Свойство MaxInstanceRepairsPercent удалено из AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="cb73b-527">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="cb73b-528">Типы AvailabilitySets, VirtualMachines и VirtualMachineScaleSets изменены с IList<SubResource> на IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="cb73b-528">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="cb73b-529">Уточнено описание командлета Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="cb73b-529">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="cb73b-530">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb73b-530">Az.DataFactory</span></span>
* <span data-ttu-id="cb73b-531">Добавлена поддержка операций CRUD для свойств среды выполнения потока данных в управляемой среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="cb73b-531">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cb73b-532">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cb73b-532">Az.FrontDoor</span></span>
* <span data-ttu-id="cb73b-533">Добавлены новые командлеты для создания, обновления, извлечения и удаления объекта обработчика правил Front Door.</span><span class="sxs-lookup"><span data-stu-id="cb73b-533">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="cb73b-534">Добавлены вспомогательные командлеты для создания объекта обработчика правил Front Door.</span><span class="sxs-lookup"><span data-stu-id="cb73b-534">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="cb73b-535">Добавлена ссылка обработчика правил на объект правила маршрутизации Front Door.</span><span class="sxs-lookup"><span data-stu-id="cb73b-535">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="cb73b-536">Добавлены параметры Приватного канала на серверный объект Front Door.</span><span class="sxs-lookup"><span data-stu-id="cb73b-536">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="cb73b-537">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="cb73b-537">Az.Functions</span></span>
* <span data-ttu-id="cb73b-538">Вышла общедоступная версия модуля Az.Functions.</span><span class="sxs-lookup"><span data-stu-id="cb73b-538">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cb73b-539">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cb73b-539">Az.HDInsight</span></span>
* <span data-ttu-id="cb73b-540">Добавлена поддержка шифрования управляемых клиентом ключей.</span><span class="sxs-lookup"><span data-stu-id="cb73b-540">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="cb73b-541">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="cb73b-541">Az.HealthcareApis</span></span>
* <span data-ttu-id="cb73b-542">Политики доступа для текущего субъекта теперь не используются по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cb73b-542">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cb73b-543">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cb73b-543">Az.IotHub</span></span>
* <span data-ttu-id="cb73b-544">Добавлен командлет для вызова запроса в центре Интернета вещей для получения данных с помощью SQL-подобного языка.</span><span class="sxs-lookup"><span data-stu-id="cb73b-544">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="cb73b-545">Устранена проблема, когда с помощью Add-AzIotHubDevice не удавалось создать устройство с поддержкой IoT Edge без дочерних устройств (№ 11597).</span><span class="sxs-lookup"><span data-stu-id="cb73b-545">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="cb73b-546">Добавлен командлет для создания маркера SAS для Центра Интернета вещей, устройства или модуля.</span><span class="sxs-lookup"><span data-stu-id="cb73b-546">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="cb73b-547">Добавлен командлет для вызова запроса метрик конфигурации.</span><span class="sxs-lookup"><span data-stu-id="cb73b-547">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="cb73b-548">Появилась возможность управлять автоматическим развертыванием IoT Edge в большом масштабе.</span><span class="sxs-lookup"><span data-stu-id="cb73b-548">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="cb73b-549">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="cb73b-549">New cmdlets are:</span></span>
    - <span data-ttu-id="cb73b-550">Add-AzIotHubDeployment;</span><span class="sxs-lookup"><span data-stu-id="cb73b-550">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="cb73b-551">Get-AzIotHubDeployment;</span><span class="sxs-lookup"><span data-stu-id="cb73b-551">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="cb73b-552">Remove-AzIotHubDeployment;</span><span class="sxs-lookup"><span data-stu-id="cb73b-552">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="cb73b-553">Set-AzIotHubDeployment.</span><span class="sxs-lookup"><span data-stu-id="cb73b-553">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="cb73b-554">Добавлен командлет для вызова запроса метрик развертывания IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="cb73b-554">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="cb73b-555">Добавлен командлет для применения содержимого конфигурации к указанному пограничному устройству.</span><span class="sxs-lookup"><span data-stu-id="cb73b-555">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cb73b-556">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb73b-556">Az.KeyVault</span></span>
* <span data-ttu-id="cb73b-557">Удалены два псевдонима: New-AzKeyVaultCertificateAdministratorDetails и New-AzKeyVaultCertificateOrganizationDetails.</span><span class="sxs-lookup"><span data-stu-id="cb73b-557">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="cb73b-558">При создании хранилища ключей обратимое удаление включено по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cb73b-558">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="cb73b-559">Можно задать правила сети, чтобы при создании хранилища ключей управлять доступом из определенных сетевых расположений.</span><span class="sxs-lookup"><span data-stu-id="cb73b-559">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="cb73b-560">Добавлена возможность создания собственных ключей (BYOK).</span><span class="sxs-lookup"><span data-stu-id="cb73b-560">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="cb73b-561">С помощью Add-AzKeyVaultKey теперь можно создавать ключ обмена ключами.</span><span class="sxs-lookup"><span data-stu-id="cb73b-561">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="cb73b-562">С помощью Get-AzKeyVaultKey можно скачать открытый ключ в формате PEM.</span><span class="sxs-lookup"><span data-stu-id="cb73b-562">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="cb73b-563">Обновлен раздел KeyOps справочной документации по Add-AzKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="cb73b-563">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb73b-564">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb73b-564">Az.Monitor</span></span>
* <span data-ttu-id="cb73b-565">Исправлена ошибка Set-AzDiagnosticSettings, когда политика хранения не применялась ко всем категориям (№ 11589).</span><span class="sxs-lookup"><span data-stu-id="cb73b-565">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="cb73b-566">Добавлена поддержка критериев доступности веб-теста для оповещения метрики версии 2.</span><span class="sxs-lookup"><span data-stu-id="cb73b-566">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="cb73b-567">В New-AzMetricAlertRuleV2Criteria добавлена возможность создавать критерии доступности веб-теста.</span><span class="sxs-lookup"><span data-stu-id="cb73b-567">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="cb73b-568">Add-AzMetricAlertRuleV2 теперь поддерживает новые критерии доступности веб-теста.</span><span class="sxs-lookup"><span data-stu-id="cb73b-568">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="cb73b-569">В PSLogProfile исправлено избыточное определение RetentionPolicy (№ 7608).</span><span class="sxs-lookup"><span data-stu-id="cb73b-569">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="cb73b-570">В PSEventData удалены избыточные определения свойств (№ 11353).</span><span class="sxs-lookup"><span data-stu-id="cb73b-570">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="cb73b-571">Командлет Get-AzLog переименован в Get-AzActivityLog.</span><span class="sxs-lookup"><span data-stu-id="cb73b-571">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb73b-572">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb73b-572">Az.Network</span></span>
* <span data-ttu-id="cb73b-573">Добавлен атрибут критического изменения, сообщающий о том, что поведение зоны по умолчанию будет изменено.</span><span class="sxs-lookup"><span data-stu-id="cb73b-573">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="cb73b-574">New-AzPublicIpAddress;</span><span class="sxs-lookup"><span data-stu-id="cb73b-574">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="cb73b-575">New-AzPublicIpPrefix;</span><span class="sxs-lookup"><span data-stu-id="cb73b-575">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="cb73b-576">New-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="cb73b-576">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="cb73b-577">Добавлена поддержка нового ресурса верхнего уровня SecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="cb73b-577">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="cb73b-578">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="cb73b-578">New cmdlets added:</span></span>
        - <span data-ttu-id="cb73b-579">New-AzSecurityPartnerProvider;</span><span class="sxs-lookup"><span data-stu-id="cb73b-579">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="cb73b-580">Remove-AzSecurityPartnerProvider;</span><span class="sxs-lookup"><span data-stu-id="cb73b-580">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="cb73b-581">Get-AzSecurityPartnerProvider;</span><span class="sxs-lookup"><span data-stu-id="cb73b-581">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="cb73b-582">Set-AzSecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="cb73b-582">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="cb73b-583">В PSPrivateLinkResource добавлен параметр RequiredZoneNames, а в PSPrivateEndpointConnection — GroupId.</span><span class="sxs-lookup"><span data-stu-id="cb73b-583">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="cb73b-584">Исправлен неправильный тип параметра SuccessThresholdRoundTripTimeMs для New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.</span><span class="sxs-lookup"><span data-stu-id="cb73b-584">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="cb73b-585">В командлетах VirtualWan аргументу AllowVnetToVnetTraffic теперь по умолчанию присвоено значение True.</span><span class="sxs-lookup"><span data-stu-id="cb73b-585">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="cb73b-586">New-AzVirtualWan;</span><span class="sxs-lookup"><span data-stu-id="cb73b-586">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="cb73b-587">Update-AzVirtualWan.</span><span class="sxs-lookup"><span data-stu-id="cb73b-587">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="cb73b-588">Добавлены новые командлеты для поддержки группы зон DNS для частной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="cb73b-588">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="cb73b-589">New-AzPrivateDnsZoneConfig;</span><span class="sxs-lookup"><span data-stu-id="cb73b-589">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="cb73b-590">Get-AzPrivateDnsZoneGroup;</span><span class="sxs-lookup"><span data-stu-id="cb73b-590">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="cb73b-591">New-AzPrivateDnsZoneGroup;</span><span class="sxs-lookup"><span data-stu-id="cb73b-591">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="cb73b-592">Set-AzPrivateDnsZoneGroup;</span><span class="sxs-lookup"><span data-stu-id="cb73b-592">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="cb73b-593">Remove-AzPrivateDnsZoneGroup.</span><span class="sxs-lookup"><span data-stu-id="cb73b-593">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="cb73b-594">В AzureFirewall добавлены параметры DNSEnableProxy, DNSRequireProxyForNetworkRules и DNSServers.</span><span class="sxs-lookup"><span data-stu-id="cb73b-594">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="cb73b-595">В AzureFirewall добавлены параметры EnableDnsProxy, DnsProxyNotRequiredForNetworkRule и DnsServer.</span><span class="sxs-lookup"><span data-stu-id="cb73b-595">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="cb73b-596">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="cb73b-596">Updated cmdlet:</span></span>
        - <span data-ttu-id="cb73b-597">New-AzFirewall.</span><span class="sxs-lookup"><span data-stu-id="cb73b-597">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cb73b-598">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cb73b-598">Az.OperationalInsights</span></span>
* <span data-ttu-id="cb73b-599">Обновлен устаревший код для использования новых пакетов SDK.</span><span class="sxs-lookup"><span data-stu-id="cb73b-599">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="cb73b-600">Из-за устаревших API-интерфейсов удалены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="cb73b-600">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="cb73b-601">Get-AzOperationalInsightsSavedSearchResult (псевдоним Get-AzOperationalInsightsSavedSearchResults);</span><span class="sxs-lookup"><span data-stu-id="cb73b-601">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="cb73b-602">Get-AzOperationalInsightsSearchResult (псевдоним Get-AzOperationalInsightsSearchResults);</span><span class="sxs-lookup"><span data-stu-id="cb73b-602">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="cb73b-603">Get-AzOperationalInsightsLinkTarget (псевдоним Get-AzOperationalInsightsLinkTargets).</span><span class="sxs-lookup"><span data-stu-id="cb73b-603">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="cb73b-604">В Set-AzOperationalInsightsWorkspace и New-AzOperationalInsightsWorkspace добавлены новые параметры.</span><span class="sxs-lookup"><span data-stu-id="cb73b-604">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="cb73b-605">Созданы командлеты для связанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="cb73b-605">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="cb73b-606">Созданы командлеты для кластеров и связанной службы.</span><span class="sxs-lookup"><span data-stu-id="cb73b-606">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb73b-607">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-607">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb73b-608">В Azure Site Recovery добавлена поддержка защиты поставщика Azure для групп размещения виртуальных машин Azure близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="cb73b-608">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="cb73b-609">В Azure Site Recovery добавлена поддержка репликации из зоны в зону.</span><span class="sxs-lookup"><span data-stu-id="cb73b-609">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="cb73b-610">В Azure Backup добавлена поддержка долгосрочного хранения для точек восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-610">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="cb73b-611">В выходные данные командлета Get-AzRecoveryServicesBackupItem добавлены свойства исключения диска, добавленного в Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="cb73b-611">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="cb73b-612">Добавлена частная конечная точка для файла учетных данных хранилища для службы Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="cb73b-612">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb73b-613">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb73b-613">Az.Resources</span></span>
* <span data-ttu-id="cb73b-614">Добавлено предупреждение о задержке представления при создании определения роли.</span><span class="sxs-lookup"><span data-stu-id="cb73b-614">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="cb73b-615">Командлеты политики теперь выводят строго типизированные объекты.</span><span class="sxs-lookup"><span data-stu-id="cb73b-615">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="cb73b-616">Из командлета Get-AzResourceLock удален параметр -TenantLevel (№ 11335).</span><span class="sxs-lookup"><span data-stu-id="cb73b-616">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="cb73b-617">Исправлена ошибка с Remove-AzResourceGroup -Id ResourceId (№ 9882).</span><span class="sxs-lookup"><span data-stu-id="cb73b-617">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="cb73b-618">Добавлен новый командлет для получения результатов анализа гипотетических вариантов из шаблона ARM в области группы ресурсов: Get-AzDeploymentResourceGroupWhatIfResult.</span><span class="sxs-lookup"><span data-stu-id="cb73b-618">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="cb73b-619">Добавлен новый командлет для получения результатов анализа гипотетических вариантов из шаблона ARM в области подписки: Get-AzDeploymentWhatIfResult.</span><span class="sxs-lookup"><span data-stu-id="cb73b-619">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="cb73b-620">Alias: Get-AzSubscriptionDeploymentWhatIf.</span><span class="sxs-lookup"><span data-stu-id="cb73b-620">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="cb73b-621">Переопределены параметры -WhatIf и -Confirm для New-AzDeployment и New-AzResourceGroupDeployment для использования результатов анализа гипотетических вариантов из шаблона ARM.</span><span class="sxs-lookup"><span data-stu-id="cb73b-621">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="cb73b-622">В командлеты развертывания добавлено сообщение об устаревании для параметра ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="cb73b-622">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="cb73b-623">Добавлена возможность отображения улучшенных сообщений об ошибках при развертывании.</span><span class="sxs-lookup"><span data-stu-id="cb73b-623">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="cb73b-624">Добавлена возможность регистрации correlationId для сбоев развертывания.</span><span class="sxs-lookup"><span data-stu-id="cb73b-624">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="cb73b-625">В выходные данные скрипта развертывания добавлено свойство error.</span><span class="sxs-lookup"><span data-stu-id="cb73b-625">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="cb73b-626">Пакет NuGet Microsoft.Azure.Management.ResourceManager обновлен до версии 3.7.1-preview.</span><span class="sxs-lookup"><span data-stu-id="cb73b-626">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="cb73b-627">Удаленные определенные тестовые случаи как свойство error в DeploymentValidateResult были изменены на доступные только для чтения из пакета NuGet версии 3.7.1-preview.</span><span class="sxs-lookup"><span data-stu-id="cb73b-627">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="cb73b-628">Добавлен GenericResourceExpanded из пакета SDK ResourceManager версии 3.7.1-preview.</span><span class="sxs-lookup"><span data-stu-id="cb73b-628">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="cb73b-629">Добавлена поддержка тегов для всех командлетов Get для развертывания, а также для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="cb73b-629">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="cb73b-630">New-AzDeployment;</span><span class="sxs-lookup"><span data-stu-id="cb73b-630">'New-AzDeployment'</span></span>
    - <span data-ttu-id="cb73b-631">New-AzManagementGroupDeployment;</span><span class="sxs-lookup"><span data-stu-id="cb73b-631">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="cb73b-632">New-AzResourceGroupDeployment;</span><span class="sxs-lookup"><span data-stu-id="cb73b-632">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="cb73b-633">New-AzTenantDeployment.</span><span class="sxs-lookup"><span data-stu-id="cb73b-633">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cb73b-634">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cb73b-634">Az.ServiceFabric</span></span>
* <span data-ttu-id="cb73b-635">Исправлена ошибка при добавлении сертификата с помощью параметра -SecretIdentifier, когда возвращался неправильный отпечаток сертификата.</span><span class="sxs-lookup"><span data-stu-id="cb73b-635">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb73b-636">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb73b-636">Az.Sql</span></span>
* <span data-ttu-id="cb73b-637">Оптимизирована работа следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="cb73b-637">Enhance performance of:</span></span>
    - <span data-ttu-id="cb73b-638">Set-AzSqlDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="cb73b-638">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="cb73b-639">Set-AzSqlInstanceDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="cb73b-639">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="cb73b-640">Remove-AzSqlDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="cb73b-640">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="cb73b-641">Remove-AzSqlInstanceDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="cb73b-641">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="cb73b-642">Enable-AzSqlDatabaseSensitivityRecommendation;</span><span class="sxs-lookup"><span data-stu-id="cb73b-642">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="cb73b-643">Enable-AzSqlInstanceDatabaseSensitivityRecommendation;</span><span class="sxs-lookup"><span data-stu-id="cb73b-643">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="cb73b-644">Disable-AzSqlDatabaseSensitivityRecommendation;</span><span class="sxs-lookup"><span data-stu-id="cb73b-644">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="cb73b-645">Disable-AzSqlInstanceDatabaseSensitivityRecommendation.</span><span class="sxs-lookup"><span data-stu-id="cb73b-645">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="cb73b-646">Удалена проверка на стороне клиента параметра RetentionDays из командлета Set-AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="cb73b-646">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="cb73b-647">Добавлен аудит учетной записи хранения в виртуальной сети. Исправлена ошибка при создании роли участника данных BLOB-объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="cb73b-647">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb73b-648">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb73b-648">Az.Storage</span></span>
* <span data-ttu-id="cb73b-649">В командлет Get-AzStorageAccount добавлен параметр -AsJob.</span><span class="sxs-lookup"><span data-stu-id="cb73b-649">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="cb73b-650">Параметр KeyVersion теперь является необязательным при изменении учетной записи хранения с помощью KeyvaultEncryption, что обеспечивает поддержку автоматической смены ключа.</span><span class="sxs-lookup"><span data-stu-id="cb73b-650">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="cb73b-651">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb73b-651">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="cb73b-652">Исправлена ошибка при удалении каталога файлов Azure с конвейером.</span><span class="sxs-lookup"><span data-stu-id="cb73b-652">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="cb73b-653">Remove-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="cb73b-653">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="cb73b-654">Исправлена ошибка 9880. Значение DefaultAction для NetWorkRule приведено в соответствие со Swagger.</span><span class="sxs-lookup"><span data-stu-id="cb73b-654">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="cb73b-655">Update-AzStorageAccountNetworkRuleSet;</span><span class="sxs-lookup"><span data-stu-id="cb73b-655">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="cb73b-656">Get-AzStorageAccountNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="cb73b-656">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="cb73b-657">Исправлена ошибка 11624. При добавлении NetworkRules дублирующиеся правила пропускаются, чтобы не происходил сбой сервера.</span><span class="sxs-lookup"><span data-stu-id="cb73b-657">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="cb73b-658">Add-AzStorageAccountNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="cb73b-658">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="cb73b-659">Версия пакета SDK Microsoft.Azure.Cosmos.Table обновлена до 1.0.7.</span><span class="sxs-lookup"><span data-stu-id="cb73b-659">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="cb73b-660">Добавлено предупреждающее сообщение, напоминающее пользователю о необходимости повторного вывода списка с помощью ContinuationToken, когда в списке элементов Data Lake 2-го поколения возвращается только часть элементов.</span><span class="sxs-lookup"><span data-stu-id="cb73b-660">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="cb73b-661">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="cb73b-661">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="cb73b-662">Добавлена возможность создания или изменения учетной записи хранения с использованием проверки подлинности Active Directory для Файлов Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-662">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="cb73b-663">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb73b-663">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="cb73b-664">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb73b-664">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="cb73b-665">Добавлена возможность создания и просмотра ключей Kerberos учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="cb73b-665">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="cb73b-666">New-AzStorageAccountKey;</span><span class="sxs-lookup"><span data-stu-id="cb73b-666">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="cb73b-667">Get-AzStorageAccountKey.</span><span class="sxs-lookup"><span data-stu-id="cb73b-667">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="cb73b-668">Добавлена возможность отработки отказа для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="cb73b-668">Supported failover Storage account</span></span>
    - <span data-ttu-id="cb73b-669">Invoke-AzStorageAccountFailover.</span><span class="sxs-lookup"><span data-stu-id="cb73b-669">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="cb73b-670">Обновлена справка по Get-AzStorageBlobCopyState.</span><span class="sxs-lookup"><span data-stu-id="cb73b-670">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="cb73b-671">Обновлена справка по Get-AzStorageFileCopyState и Start-AzStorageBlobCopy.</span><span class="sxs-lookup"><span data-stu-id="cb73b-671">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="cb73b-672">Появилась интегрированная клиентская библиотека хранилища версии 12 для командлетов очередей и файлов.</span><span class="sxs-lookup"><span data-stu-id="cb73b-672">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="cb73b-673">Тип выходных данных изменен с CloudFile на AzureStorageFile. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="cb73b-673">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="cb73b-674">Get-AzStorageFile;</span><span class="sxs-lookup"><span data-stu-id="cb73b-674">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="cb73b-675">Remove-AzStorageFile;</span><span class="sxs-lookup"><span data-stu-id="cb73b-675">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="cb73b-676">Get-AzStorageFileContent;</span><span class="sxs-lookup"><span data-stu-id="cb73b-676">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="cb73b-677">Set-AzStorageFileContent;</span><span class="sxs-lookup"><span data-stu-id="cb73b-677">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="cb73b-678">Start-AzStorageFileCopy.</span><span class="sxs-lookup"><span data-stu-id="cb73b-678">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="cb73b-679">Тип выходных данных изменен с CloudFileDirectory на AzureStorageFileDirectory. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="cb73b-679">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="cb73b-680">New-AzStorageDirectory;</span><span class="sxs-lookup"><span data-stu-id="cb73b-680">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="cb73b-681">Remove-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="cb73b-681">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="cb73b-682">Тип выходных данных изменен с CloudFileShare на AzureStorageFileShare. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="cb73b-682">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="cb73b-683">Get-AzStorageShare;</span><span class="sxs-lookup"><span data-stu-id="cb73b-683">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="cb73b-684">New-AzStorageShare;</span><span class="sxs-lookup"><span data-stu-id="cb73b-684">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="cb73b-685">Remove-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="cb73b-685">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="cb73b-686">Тип выходных данных изменен с FileShareProperties на AzureStorageFileShare. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="cb73b-686">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="cb73b-687">Set-AzStorageShareQuota.</span><span class="sxs-lookup"><span data-stu-id="cb73b-687">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="cb73b-688">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="cb73b-688">Az.TrafficManager</span></span>
* <span data-ttu-id="cb73b-689">Исправлено неправильное имя профиля в подробных выходных данных DisableAzureTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="cb73b-689">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb73b-690">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb73b-690">Az.Websites</span></span>
* <span data-ttu-id="cb73b-691">Исправлена опечатка в справке по Update-AzWebAppAccessRestrictionConfig.</span><span class="sxs-lookup"><span data-stu-id="cb73b-691">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="cb73b-692">3.8.0 — апрель 2020 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-692">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="cb73b-693">Основные сведения о новых возможностях с момента последнего выпуска</span><span class="sxs-lookup"><span data-stu-id="cb73b-693">Highlights since the last release</span></span>
* <span data-ttu-id="cb73b-694">Версии PowerShell, которые поддерживает Az.Storage: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="cb73b-694">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cb73b-695">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb73b-695">Az.Accounts</span></span>
* <span data-ttu-id="cb73b-696">Обновлен URL-адрес опроса Azure PowerShell в Resolve-AzError [11507].</span><span class="sxs-lookup"><span data-stu-id="cb73b-696">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cb73b-697">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb73b-697">Az.ApiManagement</span></span>
* <span data-ttu-id="cb73b-698">Добавлено уведомление о критическом изменении для изменения выходных данных командлетов, выполняющих действия с файлами в Azure, в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="cb73b-698">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="cb73b-699">Обновлена документация для Set-AzApiManagementGroup с указанием параметра GroupId.</span><span class="sxs-lookup"><span data-stu-id="cb73b-699">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cb73b-700">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cb73b-700">Az.Cdn</span></span>
* <span data-ttu-id="cb73b-701">Исправлено отображение ценовой категории (SKU), связанной с ChinaCDN.</span><span class="sxs-lookup"><span data-stu-id="cb73b-701">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cb73b-702">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-702">Az.CognitiveServices</span></span>
* <span data-ttu-id="cb73b-703">Включена поддержка Identity, Encryption, UserOwnedStorage.</span><span class="sxs-lookup"><span data-stu-id="cb73b-703">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb73b-704">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb73b-704">Az.Compute</span></span>
* <span data-ttu-id="cb73b-705">Добавлен командлет Set-AzVmssOrchestrationServiceState.</span><span class="sxs-lookup"><span data-stu-id="cb73b-705">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="cb73b-706">Get-AzVmss с параметром -InstanceView отображает состояния OrchestrationService.</span><span class="sxs-lookup"><span data-stu-id="cb73b-706">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cb73b-707">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cb73b-707">Az.IotHub</span></span>
* <span data-ttu-id="cb73b-708">Реализовано управление конфигурацией двойника устройства Интернета вещей. Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="cb73b-708">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="cb73b-709">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="cb73b-709">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="cb73b-710">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="cb73b-710">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="cb73b-711">Добавлен командлет для вызова прямого метода на устройстве в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="cb73b-711">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="cb73b-712">Реализовано управление конфигурацией двойника модуля устройства Интернета вещей. Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="cb73b-712">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="cb73b-713">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="cb73b-713">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="cb73b-714">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="cb73b-714">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="cb73b-715">Реализовано управление конфигурацией автоматического управления устройствами в центре Интернета вещей в большом масштабе.</span><span class="sxs-lookup"><span data-stu-id="cb73b-715">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="cb73b-716">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="cb73b-716">New cmdlets are:</span></span>
    - <span data-ttu-id="cb73b-717">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb73b-717">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="cb73b-718">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb73b-718">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="cb73b-719">Remove-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb73b-719">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="cb73b-720">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb73b-720">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="cb73b-721">Добавлен командлет для вызова метода периферийного модуля в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="cb73b-721">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cb73b-722">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb73b-722">Az.KeyVault</span></span>
* <span data-ttu-id="cb73b-723">Добавлен новый командлет Update-AzKeyVault, который может включать защиту от обратимого удаления и очистки в хранилище.</span><span class="sxs-lookup"><span data-stu-id="cb73b-723">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="cb73b-724">Включена поддержка Microsoft.PowerShell.SecretManagement [11178].</span><span class="sxs-lookup"><span data-stu-id="cb73b-724">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="cb73b-725">Исправлена ошибка в примерах Remove-AzKeyVaultManagedStorageSasDefinition [11479].</span><span class="sxs-lookup"><span data-stu-id="cb73b-725">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="cb73b-726">Включена поддержка частной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="cb73b-726">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="cb73b-727">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="cb73b-727">Az.Maintenance</span></span>
* <span data-ttu-id="cb73b-728">Опубликована версия выпуска командлетов обслуживания для общедоступной версии.</span><span class="sxs-lookup"><span data-stu-id="cb73b-728">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb73b-729">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb73b-729">Az.Monitor</span></span>
* <span data-ttu-id="cb73b-730">Добавлены командлеты для области приватных каналов:</span><span class="sxs-lookup"><span data-stu-id="cb73b-730">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="cb73b-731">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="cb73b-731">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="cb73b-732">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="cb73b-732">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="cb73b-733">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="cb73b-733">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="cb73b-734">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="cb73b-734">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="cb73b-735">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="cb73b-735">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="cb73b-736">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="cb73b-736">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="cb73b-737">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="cb73b-737">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb73b-738">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb73b-738">Az.Network</span></span>
* <span data-ttu-id="cb73b-739">Обновлены командлеты для включения подключения на частном IP-адресе для шлюза виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="cb73b-739">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="cb73b-740">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cb73b-740">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="cb73b-741">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cb73b-741">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="cb73b-742">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cb73b-742">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="cb73b-743">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cb73b-743">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="cb73b-744">Обновлены командлеты для включения шлюзов LocalNetworkGateways и сайтов VpnSites на основе FQDN:</span><span class="sxs-lookup"><span data-stu-id="cb73b-744">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="cb73b-745">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cb73b-745">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="cb73b-746">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="cb73b-746">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="cb73b-747">Включена поддержка семейства адресов IPv6 в ExpressRouteCircuitConnectionConfig (Global Reach).</span><span class="sxs-lookup"><span data-stu-id="cb73b-747">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="cb73b-748">Добавлен командлет Set-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="cb73b-748">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="cb73b-749">Позволяет выполнять настройку всех существующих свойств, включая IPv6CircuitConnectionProperties.</span><span class="sxs-lookup"><span data-stu-id="cb73b-749">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="cb73b-750">Обновлен командлет Add-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="cb73b-750">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="cb73b-751">Добавлен еще один необязательный параметр AddressPrefixType для указания семейства адресов префикса адреса.</span><span class="sxs-lookup"><span data-stu-id="cb73b-751">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="cb73b-752">Обновлены командлеты для включения параметра времени ожидания для обнаружения неиспользуемых одноранговых узлов (DPD) в подключениях шлюзов виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="cb73b-752">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="cb73b-753">New-AzVirtualNetworkGatewayConnection;</span><span class="sxs-lookup"><span data-stu-id="cb73b-753">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="cb73b-754">Set-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="cb73b-754">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cb73b-755">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cb73b-755">Az.PolicyInsights</span></span>
* <span data-ttu-id="cb73b-756">Добавлен командлет Start-AzPolicyComplianceScan для запуска проверок соответствия политикам.</span><span class="sxs-lookup"><span data-stu-id="cb73b-756">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="cb73b-757">Добавлены версии определения политики, определения набора и назначения в выходные данные командлета Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="cb73b-757">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cb73b-758">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cb73b-758">Az.ServiceFabric</span></span>
* <span data-ttu-id="cb73b-759">Улучшено форматирование и наглядность кода в примерах New-AzServiceFabricCluster.</span><span class="sxs-lookup"><span data-stu-id="cb73b-759">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb73b-760">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb73b-760">Az.Sql</span></span>
* <span data-ttu-id="cb73b-761">Добавлены командлеты Get-AzSqlInstanceOperation и Stop-AzSqlInstanceOperation.</span><span class="sxs-lookup"><span data-stu-id="cb73b-761">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="cb73b-762">Включен аудит учетной записи хранения в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="cb73b-762">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb73b-763">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb73b-763">Az.Storage</span></span>
* <span data-ttu-id="cb73b-764">Добавлено уведомление о критическом изменении для изменения выходных данных командлетов, выполняющих действия с файлами в Azure, в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="cb73b-764">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="cb73b-765">Включена поддержка новых имен SKU StandardGZRS, StandardRAGZRS при создании или обновлении учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="cb73b-765">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="cb73b-766">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb73b-766">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="cb73b-767">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb73b-767">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="cb73b-768">Добавлена поддержка DataLake 2-го поколения.</span><span class="sxs-lookup"><span data-stu-id="cb73b-768">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="cb73b-769">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="cb73b-769">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="cb73b-770">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="cb73b-770">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="cb73b-771">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="cb73b-771">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="cb73b-772">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="cb73b-772">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="cb73b-773">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="cb73b-773">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="cb73b-774">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="cb73b-774">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="cb73b-775">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="cb73b-775">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="cb73b-776">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="cb73b-776">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="cb73b-777">0.10.0-preview — апрель 2020 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-777">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="cb73b-778">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="cb73b-778">General</span></span>
* <span data-ttu-id="cb73b-779">Модуль Az стали доступными в предварительной версии в Azure Stack Hub.</span><span class="sxs-lookup"><span data-stu-id="cb73b-779">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="cb73b-780">Это обеспечивает кросс-платформенную совместимость с Linux и macOs.</span><span class="sxs-lookup"><span data-stu-id="cb73b-780">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="cb73b-781">Azure Stack Hub теперь поддерживает PowerShell Core с модулями Az (см. [дополнительные сведения](https://aka.ms/az4AzureStack))</span><span class="sxs-lookup"><span data-stu-id="cb73b-781">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="cb73b-782">Модули Az поддерживают профиль 2019-03-01-hybrid:</span><span class="sxs-lookup"><span data-stu-id="cb73b-782">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="cb73b-783">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="cb73b-783">Az.Billing</span></span>
  - <span data-ttu-id="cb73b-784">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb73b-784">Az.Compute</span></span>
  - <span data-ttu-id="cb73b-785">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="cb73b-785">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="cb73b-786">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cb73b-786">Az.EventHub</span></span>
  - <span data-ttu-id="cb73b-787">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cb73b-787">Az.IotHub</span></span>
  - <span data-ttu-id="cb73b-788">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb73b-788">Az.KeyVault</span></span>
  - <span data-ttu-id="cb73b-789">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb73b-789">Az.Monitor</span></span>
  - <span data-ttu-id="cb73b-790">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb73b-790">Az.Network</span></span>
  - <span data-ttu-id="cb73b-791">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb73b-791">Az.Resources</span></span>
  - <span data-ttu-id="cb73b-792">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb73b-792">Az.Storage</span></span>
  - <span data-ttu-id="cb73b-793">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb73b-793">Az.Websites</span></span>
* <span data-ttu-id="cb73b-794">В PowerShell появились три новых модуля Az, которые работают с Azure Stack Hub: Az.Databox, Az.IotHub и Az.EventHub.</span><span class="sxs-lookup"><span data-stu-id="cb73b-794">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="cb73b-795">Команды остаются прежними же за исключением незначительных изменений, таких как изменение AzureRM на Az.</span><span class="sxs-lookup"><span data-stu-id="cb73b-795">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="cb73b-796">См. обновленную ссылку на документацию по [PowerShell для Azure Stack Hub](https://aka.ms/InstallASHPowerShell)</span><span class="sxs-lookup"><span data-stu-id="cb73b-796">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="cb73b-797">3.7.0 — март 2020 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-797">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb73b-798">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb73b-798">Az.Accounts</span></span>
* <span data-ttu-id="cb73b-799">Исправлено исключение NullReferenceException командлетов Get-AzTenant/Get-AzDefault/Set-AzDefault, если вход не выполнен [10292]</span><span class="sxs-lookup"><span data-stu-id="cb73b-799">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb73b-800">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb73b-800">Az.Compute</span></span>
* <span data-ttu-id="cb73b-801">Добавлены следующие параметры к командлету New-AzDiskConfig:</span><span class="sxs-lookup"><span data-stu-id="cb73b-801">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="cb73b-802">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="cb73b-802">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="cb73b-803">Разрешено свойство Encryption для параметра Target командлета New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="cb73b-803">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="cb73b-804">Исправлена проблема с tempDisk для командлетов Set-AzVmss -Reimage и Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="cb73b-804">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="cb73b-805">[11354]</span><span class="sxs-lookup"><span data-stu-id="cb73b-805">[#11354]</span></span>
* <span data-ttu-id="cb73b-806">Добавлена поддержка нового расширения SAP для указанных ниже командлетов</span><span class="sxs-lookup"><span data-stu-id="cb73b-806">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="cb73b-807">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="cb73b-807">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="cb73b-808">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="cb73b-808">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="cb73b-809">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="cb73b-809">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="cb73b-810">Update-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="cb73b-810">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="cb73b-811">Исправлены ошибки в примерах справки</span><span class="sxs-lookup"><span data-stu-id="cb73b-811">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="cb73b-812">Показано точное строковое значение в табличном формате для свойства PowerState виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cb73b-812">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="cb73b-813">New-AzVmssConfig: исправлена сериализация свойства AutomaticRepairs, если параметр SinglePlacementGroup отключен.</span><span class="sxs-lookup"><span data-stu-id="cb73b-813">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="cb73b-814">[11257]</span><span class="sxs-lookup"><span data-stu-id="cb73b-814">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb73b-815">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb73b-815">Az.DataFactory</span></span>
* <span data-ttu-id="cb73b-816">Пакет SDK ADF для .NET обновлен до версии 4.8.0.</span><span class="sxs-lookup"><span data-stu-id="cb73b-816">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="cb73b-817">Добавлены необязательные параметры для команды Invoke-AzDataFactoryV2Pipeline для поддержки повторного запуска.</span><span class="sxs-lookup"><span data-stu-id="cb73b-817">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb73b-818">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb73b-818">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb73b-819">Добавлено описание критического изменения для Export-AzDataLakeStoreItem и Import-AzDataLakeStoreItem.</span><span class="sxs-lookup"><span data-stu-id="cb73b-819">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="cb73b-820">Добавлен параметр кодирования байтов для New-AzDataLakeStoreItem, Add-AzDAtaLakeStoreItemContent и Get-AzDAtaLakeStoreItemContent.</span><span class="sxs-lookup"><span data-stu-id="cb73b-820">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cb73b-821">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cb73b-821">Az.HDInsight</span></span>
* <span data-ttu-id="cb73b-822">Добавлена поддержка указания минимальной поддерживаемой версии TLS при создании кластера.</span><span class="sxs-lookup"><span data-stu-id="cb73b-822">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cb73b-823">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cb73b-823">Az.IotHub</span></span>
* <span data-ttu-id="cb73b-824">Добавлена поддержка для управления распределенными параметрами на отдельных устройствах.</span><span class="sxs-lookup"><span data-stu-id="cb73b-824">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="cb73b-825">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="cb73b-825">New Cmdlets are:</span></span>
    - <span data-ttu-id="cb73b-826">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="cb73b-826">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="cb73b-827">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="cb73b-827">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cb73b-828">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb73b-828">Az.KeyVault</span></span>
* <span data-ttu-id="cb73b-829">Добавлены атрибуты критических изменений для New-AzKeyVault.</span><span class="sxs-lookup"><span data-stu-id="cb73b-829">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb73b-830">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb73b-830">Az.Monitor</span></span>
* <span data-ttu-id="cb73b-831">Обновлена документация для New-AzScheduledQueryRuleLogMetricTrigger.</span><span class="sxs-lookup"><span data-stu-id="cb73b-831">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb73b-832">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb73b-832">Az.Network</span></span>
* <span data-ttu-id="cb73b-833">Обновлены командлеты для поддержки подключений VirtualHubVnetConnections между клиентами</span><span class="sxs-lookup"><span data-stu-id="cb73b-833">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="cb73b-834">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="cb73b-834">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="cb73b-835">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="cb73b-835">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="cb73b-836">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="cb73b-836">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="cb73b-837">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="cb73b-837">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="cb73b-838">Удалена зависимость пакета SDK для управления SQL.</span><span class="sxs-lookup"><span data-stu-id="cb73b-838">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cb73b-839">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cb73b-839">Az.PolicyInsights</span></span>
* <span data-ttu-id="cb73b-840">Улучшены сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="cb73b-840">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb73b-841">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-841">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb73b-842">В Azure Site Recovery реализована поддержка повторной защиты и обновлены свойства зашифрованных виртуальных машин диска Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-842">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="cb73b-843">Добавлена возможность мониторинг аварийного восстановления для свойств VmwareToAzure в Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="cb73b-843">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="cb73b-844">В Azure Backup реализована поддержка повторного обновления политики для элементов с ошибками.</span><span class="sxs-lookup"><span data-stu-id="cb73b-844">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="cb73b-845">В Azure Backup реализована поддержка параметров исключения диска во время резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="cb73b-845">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="cb73b-846">В Azure Backup реализована поддержка восстановления нескольких файлов или папок в AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="cb73b-846">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="cb73b-847">В Azure Backup реализована поддержка указанной пользователем группы Resourcegroup при обновлении политики IaasVM.</span><span class="sxs-lookup"><span data-stu-id="cb73b-847">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb73b-848">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb73b-848">Az.Resources</span></span>
* <span data-ttu-id="cb73b-849">Исправлена команда Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType для использования фактической версии apiVersion ресурсов (а не версии apiVersion по умолчанию) [11267].</span><span class="sxs-lookup"><span data-stu-id="cb73b-849">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="cb73b-850">Добавлена возможность регистрации correlationId для сценариев с ошибками.</span><span class="sxs-lookup"><span data-stu-id="cb73b-850">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="cb73b-851">Незначительно изменена документация по Get-AzResourceLock.</span><span class="sxs-lookup"><span data-stu-id="cb73b-851">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="cb73b-852">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="cb73b-852">Added example.</span></span>
* <span data-ttu-id="cb73b-853">Экранирована одинарная кавычка в значении параметра Get-AzADUser [11317].</span><span class="sxs-lookup"><span data-stu-id="cb73b-853">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="cb73b-854">Добавлены новые командлеты для сценариев развертывания (Get-AzDeploymentScript, Get-AzDeploymentScriptLog, Save-AzDeploymentScriptLog, Remove-AzDeploymentScript).</span><span class="sxs-lookup"><span data-stu-id="cb73b-854">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb73b-855">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb73b-855">Az.Sql</span></span>
* <span data-ttu-id="cb73b-856">Добавлен параметр вторичной реплики для чтения для командлета Invoke-AzSqlDatabaseFailover.</span><span class="sxs-lookup"><span data-stu-id="cb73b-856">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="cb73b-857">Добавлен командлет Disable-AzSqlServerActiveDirectoryOnlyAuthentication.</span><span class="sxs-lookup"><span data-stu-id="cb73b-857">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="cb73b-858">Сохранен приоритет конфиденциальности при классификации столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="cb73b-858">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="cb73b-859">Az.Support</span><span class="sxs-lookup"><span data-stu-id="cb73b-859">Az.Support</span></span>
* <span data-ttu-id="cb73b-860">Модуль Az.Support стал общедоступным.</span><span class="sxs-lookup"><span data-stu-id="cb73b-860">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb73b-861">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb73b-861">Az.Websites</span></span>
* <span data-ttu-id="cb73b-862">Реализована поддержка работы с правилами маршрутизации трафика веб-приложения через указанные ниже командлеты</span><span class="sxs-lookup"><span data-stu-id="cb73b-862">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="cb73b-863">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="cb73b-863">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="cb73b-864">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="cb73b-864">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="cb73b-865">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="cb73b-865">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="cb73b-866">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="cb73b-866">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="cb73b-867">3.6.1 — март 2020 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-867">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb73b-868">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb73b-868">Az.Accounts</span></span>
* <span data-ttu-id="cb73b-869">Открытие страницы опроса Azure PowerShell в Send-Feedback [11020].</span><span class="sxs-lookup"><span data-stu-id="cb73b-869">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="cb73b-870">Отображение URL-адреса опроса Azure PowerShell в Resolve-Error [11021].</span><span class="sxs-lookup"><span data-stu-id="cb73b-870">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="cb73b-871">Добавлена версия Az в UserAgent.</span><span class="sxs-lookup"><span data-stu-id="cb73b-871">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cb73b-872">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb73b-872">Az.ApiManagement</span></span>
* <span data-ttu-id="cb73b-873">Включена поддержка получения и настройки личного домена в конечной точке DeveloperPortal [11007].</span><span class="sxs-lookup"><span data-stu-id="cb73b-873">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="cb73b-874">Export-AzApiManagementApi: включена поддержка скачивания определения API в формате JSON [9987].</span><span class="sxs-lookup"><span data-stu-id="cb73b-874">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="cb73b-875">Import-AzApiManagementApi: включена поддержка импорта определения OpenApi 3.0 из документа JSON.</span><span class="sxs-lookup"><span data-stu-id="cb73b-875">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="cb73b-876">New-AzApiManagementIdentityProvider и Set-AzApiManagementIdentityProvider: включена поддержка настройки входа арендатора для поставщика AAD B2C [9784].</span><span class="sxs-lookup"><span data-stu-id="cb73b-876">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb73b-877">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb73b-877">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb73b-878">Добавлена ссылка на System.Buffers явным образом в CSPROJ и PSD1.</span><span class="sxs-lookup"><span data-stu-id="cb73b-878">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cb73b-879">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cb73b-879">Az.IotHub</span></span>
* <span data-ttu-id="cb73b-880">Добавлена возможность управления устройствами в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="cb73b-880">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="cb73b-881">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="cb73b-881">New Cmdlets are:</span></span>
    - <span data-ttu-id="cb73b-882">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="cb73b-882">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="cb73b-883">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="cb73b-883">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="cb73b-884">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="cb73b-884">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="cb73b-885">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="cb73b-885">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="cb73b-886">Включена поддержка управления модулями в целевом устройстве Интернета вещей в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="cb73b-886">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="cb73b-887">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="cb73b-887">New Cmdlets are:</span></span>
    - <span data-ttu-id="cb73b-888">Add-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="cb73b-888">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="cb73b-889">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="cb73b-889">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="cb73b-890">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="cb73b-890">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="cb73b-891">Set-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="cb73b-891">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="cb73b-892">Добавлен командлет для получения строки подключения целевого устройства Интернета вещей в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="cb73b-892">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="cb73b-893">Добавлен командлет для получения строки подключения модуля на целевом устройстве Интернета вещей в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="cb73b-893">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="cb73b-894">Включена поддержка для получения или настройки родительского устройства для устройства Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="cb73b-894">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="cb73b-895">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="cb73b-895">New Cmdlets are:</span></span>
    - <span data-ttu-id="cb73b-896">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="cb73b-896">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="cb73b-897">Set-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="cb73b-897">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="cb73b-898">Включена поддержка управления связью "родители — потомки" устройства.</span><span class="sxs-lookup"><span data-stu-id="cb73b-898">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb73b-899">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb73b-899">Az.Monitor</span></span>
* <span data-ttu-id="cb73b-900">Исправлено выходное значение для Get-AzMetricDefinition [9714].</span><span class="sxs-lookup"><span data-stu-id="cb73b-900">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb73b-901">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb73b-901">Az.Network</span></span>
* <span data-ttu-id="cb73b-902">Обновлен пакет SDK для управления SQL.</span><span class="sxs-lookup"><span data-stu-id="cb73b-902">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="cb73b-903">Исправлена проблема с разницей в именовании в классе PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="cb73b-903">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="cb73b-904">Сопоставление ActionsRequired с ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="cb73b-904">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="cb73b-905">Добавление PublicNetworkAccess в команды New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="cb73b-905">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb73b-906">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb73b-906">Az.Resources</span></span>
* <span data-ttu-id="cb73b-907">Исправлена ошибка пустой ссылки в Get-AzRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="cb73b-907">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="cb73b-908">Параметры -Force и -PassThru помечены необязательными в Remove-AzADGroup [10849].</span><span class="sxs-lookup"><span data-stu-id="cb73b-908">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="cb73b-909">Исправлена ошибка, из-за которой MailNickname не возвращается в Remove-AzADGroup [11167].</span><span class="sxs-lookup"><span data-stu-id="cb73b-909">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="cb73b-910">Исправлена ошибка, из-за которой операция канала Remove-AzADGroup не работает [11171].</span><span class="sxs-lookup"><span data-stu-id="cb73b-910">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="cb73b-911">Исправлена ошибка с пустой ссылкой в GetAzureRoleAssignmentCommand.</span><span class="sxs-lookup"><span data-stu-id="cb73b-911">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="cb73b-912">Добавлено критическое изменение атрибутов для будущих изменений командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="cb73b-912">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="cb73b-913">Обновлена команда Get-AzResourceGroup для выполнения фильтрации тегов группы ресурсов на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="cb73b-913">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="cb73b-914">Расширены командлеты Tag для включения поддержки параметра -ResourceId.</span><span class="sxs-lookup"><span data-stu-id="cb73b-914">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="cb73b-915">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb73b-915">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="cb73b-916">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb73b-916">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="cb73b-917">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb73b-917">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="cb73b-918">Добавлен новый командлет Tag.</span><span class="sxs-lookup"><span data-stu-id="cb73b-918">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="cb73b-919">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb73b-919">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="cb73b-920">Предоставляется ScopedDeployment из пакета SDK 3.3.0.</span><span class="sxs-lookup"><span data-stu-id="cb73b-920">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb73b-921">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb73b-921">Az.Sql</span></span>
* <span data-ttu-id="cb73b-922">Добавление PublicNetworkAccess в команды New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="cb73b-922">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="cb73b-923">Включена поддержка конфигурации резервного копирования долгосрочного хранения для управляемых баз данных.</span><span class="sxs-lookup"><span data-stu-id="cb73b-923">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="cb73b-924">Получение или настройка политики LTR в управляемой базе данных.</span><span class="sxs-lookup"><span data-stu-id="cb73b-924">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="cb73b-925">Получение резервных копий LTR по управляемой базе данных, управляемому экземпляру или расположению.</span><span class="sxs-lookup"><span data-stu-id="cb73b-925">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="cb73b-926">Удаление резервной копии LTR.</span><span class="sxs-lookup"><span data-stu-id="cb73b-926">Remove an LTR backup</span></span>
    - <span data-ttu-id="cb73b-927">Восстановление резервной копии LTR для создания новой управляемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="cb73b-927">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="cb73b-928">Добавление MinimalTlsVersion в New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="cb73b-928">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="cb73b-929">Добавление MinimalTlsVersion в New-AzSqlInstance и Set-AzSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="cb73b-929">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="cb73b-930">Обновлена версия пакета SDK для SQL для Az.Network.</span><span class="sxs-lookup"><span data-stu-id="cb73b-930">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb73b-931">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb73b-931">Az.Storage</span></span>
* <span data-ttu-id="cb73b-932">Включена поддержка AllowProtectedAppendWrite в ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="cb73b-932">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="cb73b-933">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="cb73b-933">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="cb73b-934">Добавлено предупреждение о критическом изменении для изменения типа AzureStorageTable в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="cb73b-934">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="cb73b-935">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="cb73b-935">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="cb73b-936">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="cb73b-936">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb73b-937">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb73b-937">Az.Websites</span></span>
* <span data-ttu-id="cb73b-938">Добавлен параметр Tag для New-AzAppServicePlan и Set-AzAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="cb73b-938">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="cb73b-939">Завершение выполнения командлета, если при добавлении личного домена на веб-сайт возникает исключение.</span><span class="sxs-lookup"><span data-stu-id="cb73b-939">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="cb73b-940">Включена поддержка выполнения операций для Служб приложений, которые находятся не в той же группе ресурсов, что и план службы приложений.</span><span class="sxs-lookup"><span data-stu-id="cb73b-940">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="cb73b-941">Применение ограничения доступа к WebApp/Function в разных группах ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cb73b-941">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="cb73b-942">Исправлена ошибка с указанием пользовательских имен узлов для WebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="cb73b-942">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="cb73b-943">3.5.0 — февраль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-943">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cb73b-944">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="cb73b-944">Highlights since the last major release</span></span>
* <span data-ttu-id="cb73b-945">Обновлены данные телеметрии на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="cb73b-945">Updated client side telemetry.</span></span>
* <span data-ttu-id="cb73b-946">В Az.IotHub добавлены командлеты для управления устройствами.</span><span class="sxs-lookup"><span data-stu-id="cb73b-946">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="cb73b-947">В Az.SqlVirtualMachine добавлены командлеты для прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="cb73b-947">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cb73b-948">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb73b-948">Az.Accounts</span></span>
* <span data-ttu-id="cb73b-949">В данные телеметрии на стороне клиента добавлены такие сведения, как идентификатор подписки, идентификатор арендатора и время выполнения.</span><span class="sxs-lookup"><span data-stu-id="cb73b-949">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb73b-950">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb73b-950">Az.Automation</span></span>
* <span data-ttu-id="cb73b-951">Исправлена опечатка в примере 1 в справочной документации по New-AzAutomationSoftwareUpdateConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cb73b-951">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cb73b-952">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-952">Az.CognitiveServices</span></span>
* <span data-ttu-id="cb73b-953">Обновлен пакет SDK до версии 7.0.</span><span class="sxs-lookup"><span data-stu-id="cb73b-953">Updated SDK to 7.0</span></span>
* <span data-ttu-id="cb73b-954">Улучшено сообщение об ошибке, которое появляется, если ответы сервера не содержат текст.</span><span class="sxs-lookup"><span data-stu-id="cb73b-954">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb73b-955">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb73b-955">Az.Compute</span></span>
* <span data-ttu-id="cb73b-956">Разрешено использовать пустое значение для ProximityPlacementGroupId во время обновления.</span><span class="sxs-lookup"><span data-stu-id="cb73b-956">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cb73b-957">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cb73b-957">Az.FrontDoor</span></span>
* <span data-ttu-id="cb73b-958">Добавлен командлет для получения определений управляемых правил, которые могут использоваться в WAF.</span><span class="sxs-lookup"><span data-stu-id="cb73b-958">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cb73b-959">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cb73b-959">Az.IotHub</span></span>
* <span data-ttu-id="cb73b-960">Добавлена возможность управления устройствами в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="cb73b-960">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="cb73b-961">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="cb73b-961">New Cmdlets are:</span></span>
    - <span data-ttu-id="cb73b-962">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="cb73b-962">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="cb73b-963">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="cb73b-963">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="cb73b-964">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="cb73b-964">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="cb73b-965">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="cb73b-965">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cb73b-966">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb73b-966">Az.KeyVault</span></span>
* <span data-ttu-id="cb73b-967">Устранен дублирующийся текст для Add-AzKeyVaultKey.md.</span><span class="sxs-lookup"><span data-stu-id="cb73b-967">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb73b-968">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb73b-968">Az.Monitor</span></span>
* <span data-ttu-id="cb73b-969">Исправлено описание командлета Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="cb73b-969">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="cb73b-970">В команду New-AzMetricAlertRuleV2 добавлен новый параметр ActionGroupId.</span><span class="sxs-lookup"><span data-stu-id="cb73b-970">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="cb73b-971">Пользователь может предоставить ActionGroupId(string) или ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="cb73b-971">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb73b-972">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb73b-972">Az.Network</span></span>
* <span data-ttu-id="cb73b-973">Добавлен еще один параметр -EnableProxyProtocol для командлета New-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="cb73b-973">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="cb73b-974">Исправлен пример FilterData в Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="cb73b-974">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="cb73b-975">Добавлен пример Packet Capture для всех внутренних и внешних пакетов в Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="cb73b-975">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="cb73b-976">Добавлена поддерживаемая политика Брандмауэра Azure в брандмауэрах виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="cb73b-976">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="cb73b-977">Новые командлеты не добавлены.</span><span class="sxs-lookup"><span data-stu-id="cb73b-977">No new cmdlets are added.</span></span> <span data-ttu-id="cb73b-978">Снято ограничение политики брандмауэра в брандмауэрах виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="cb73b-978">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb73b-979">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-979">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb73b-980">Добавлена возможность восстановления в виде файлов для Баз данных SQL.</span><span class="sxs-lookup"><span data-stu-id="cb73b-980">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb73b-981">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb73b-981">Az.Resources</span></span>
* <span data-ttu-id="cb73b-982">Выполнен рефакторинг командлетов развертывания шаблона.</span><span class="sxs-lookup"><span data-stu-id="cb73b-982">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="cb73b-983">Добавлены новые командлеты для управления развертываниями в группе управления: \*-AzManagementGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="cb73b-983">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="cb73b-984">Добавлены новые командлеты для управления развертываниями в области арендатора: \*-AzTenantDeployment.</span><span class="sxs-lookup"><span data-stu-id="cb73b-984">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="cb73b-985">Выполнен рефакторинг командлетов \*-AzDeployment для работы в области подписки.</span><span class="sxs-lookup"><span data-stu-id="cb73b-985">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="cb73b-986">Созданы псевдонимы \*-AzSubscriptionDeployment для командлетов \*-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="cb73b-986">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="cb73b-987">Исправлен командлет Update-AzADApplication, когда параметр AvailableToOtherTenants не задан.</span><span class="sxs-lookup"><span data-stu-id="cb73b-987">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="cb73b-988">Удален набор параметров ApplicationObjectWithoutCredentialParameterSet, чтобы предотвратить возникновение AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="cb73b-988">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="cb73b-989">Повторно созданы файлы справки.</span><span class="sxs-lookup"><span data-stu-id="cb73b-989">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb73b-990">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb73b-990">Az.Sql</span></span>
* <span data-ttu-id="cb73b-991">Добавлена возможность восстановления точки во времени между подписками в Управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="cb73b-991">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="cb73b-992">Добавлена возможность изменения существующего поколения оборудования Управляемого экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="cb73b-992">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="cb73b-993">Исправлены примеры справки Update-AzSqlServerVulnerabilityAssessmentSetting: выходные данные параметра и свойства — EmailAdmins.</span><span class="sxs-lookup"><span data-stu-id="cb73b-993">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="cb73b-994">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="cb73b-994">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="cb73b-995">Добавлены командлеты для прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="cb73b-995">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="cb73b-996">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="cb73b-996">Az.StorageSync</span></span>
* <span data-ttu-id="cb73b-997">В командлете Invoke-AzStorageSyncCompatibilityCheck обновлены поддерживаемые наборы символов.</span><span class="sxs-lookup"><span data-stu-id="cb73b-997">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="cb73b-998">3.4.0 — февраль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-998">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cb73b-999">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="cb73b-999">Highlights since the last major release</span></span>
* <span data-ttu-id="cb73b-1000">Выпущена первоначальная версия 0.1.0 Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="cb73b-1000">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="cb73b-1001">Добавлена поддержка Az.Network ConnectionMonitor V2</span><span class="sxs-lookup"><span data-stu-id="cb73b-1001">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cb73b-1002">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb73b-1002">Az.Accounts</span></span>
* <span data-ttu-id="cb73b-1003">Отключить автоматическое сохранение контекста, если AzureRmContext.json недоступен</span><span class="sxs-lookup"><span data-stu-id="cb73b-1003">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="cb73b-1004">Обновление ссылки на Azure Powershell Common до предварительной версии 1.3.5</span><span class="sxs-lookup"><span data-stu-id="cb73b-1004">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cb73b-1005">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb73b-1005">Az.ApiManagement</span></span>
* <span data-ttu-id="cb73b-1006">**Get-AzApiManagementApiSchema** Исправлено получение схемы Open-API, связанной с API https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="cb73b-1006">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="cb73b-1007">**New-AzApiManagementProduct**\* и **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="cb73b-1007">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="cb73b-1008">Исправить документацию для https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="cb73b-1008">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="cb73b-1009">**Set-AzApiManagementApi** Добавлен пример, показывающий, как обновить ServiceUrl с помощью командлета</span><span class="sxs-lookup"><span data-stu-id="cb73b-1009">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb73b-1010">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb73b-1010">Az.Compute</span></span>
* <span data-ttu-id="cb73b-1011">Ограничение числа состояний виртуальных машин до 100, чтобы избежать регулирования при выполнении Get-AzVM-Status без имени виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1011">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="cb73b-1012">Добавление обновления командлета -AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="cb73b-1012">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="cb73b-1013">Добавление параметров EncryptionType и DiskEncryptionSetId в следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1013">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="cb73b-1014">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="cb73b-1014">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="cb73b-1015">Добавление параметра ColocationStatus в командлет Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1015">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb73b-1016">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb73b-1016">Az.DataFactory</span></span>
* <span data-ttu-id="cb73b-1017">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.7.0.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1017">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="cb73b-1018">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="cb73b-1018">Az.DeploymentManager</span></span>
* <span data-ttu-id="cb73b-1019">Добавляет операции LIST для ресурсов</span><span class="sxs-lookup"><span data-stu-id="cb73b-1019">Adds LIST operations for resources</span></span>
* <span data-ttu-id="cb73b-1020">Добавляет возможность выполнения операций на этапах Проверки работоспособности</span><span class="sxs-lookup"><span data-stu-id="cb73b-1020">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cb73b-1021">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cb73b-1021">Az.HDInsight</span></span>
* <span data-ttu-id="cb73b-1022">Исправление ошибки в документе New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1022">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cb73b-1023">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb73b-1023">Az.KeyVault</span></span>
* <span data-ttu-id="cb73b-1024">Добавление Псевдонимов имени в атрибут VaultName, чтобы Remove-AzureKeyVault соответствовал New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1024">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb73b-1025">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb73b-1025">Az.Network</span></span>
* <span data-ttu-id="cb73b-1026">В Set-AzNetworkWatcherConfigFlowLog.md добавлен новый пример для демонстрации сценария отключения Аналитики трафика.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1026">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="cb73b-1027">Добавление поддержки назначения IP-конфигурации для брандмауэра Azure — выделенная подсеть и общедоступный IP-адрес, которые брандмауэр будет использовать для управления трафиком</span><span class="sxs-lookup"><span data-stu-id="cb73b-1027">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="cb73b-1028">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1028">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="cb73b-1029">добавлен параметр — ManagementPublicIpAddress (необязательный), который принимает объект общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="cb73b-1029">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="cb73b-1030">Добавлен метод SetManagementIpConfiguration для объекта брандмауэра — в качестве входных данных требуется подсеть и общедоступный IP-адрес — имя подсети должно быть "AzureFirewallManagementSubnet"</span><span class="sxs-lookup"><span data-stu-id="cb73b-1030">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="cb73b-1031">Исправлены примеры Get-AzNetworkSecurityGroup для отображения примеров для группы безопасности сети (NSG) вместо сетевых интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1031">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="cb73b-1032">Исправлена опечатка в команде New-AzVpnSite, которая препятствовала завершению параметра идентификатором ресурса.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1032">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="cb73b-1033">Добавлена поддержка конфигурации в наборе действий для правил подстановки URL-адресов в шлюзе приложения.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1033">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="cb73b-1034">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1034">New cmdlets added:</span></span>
        - <span data-ttu-id="cb73b-1035">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb73b-1035">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="cb73b-1036">В следующие командлеты добавлен необязательный параметр — UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb73b-1036">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="cb73b-1037">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="cb73b-1037">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="cb73b-1038">Добавление поддержки для ресурсов NetworkWatcher ConnectionMonitor версии 2</span><span class="sxs-lookup"><span data-stu-id="cb73b-1038">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cb73b-1039">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cb73b-1039">Az.PolicyInsights</span></span>
* <span data-ttu-id="cb73b-1040">Поддержка оценки соответствия до определения того, какой ресурс нужно исправить</span><span class="sxs-lookup"><span data-stu-id="cb73b-1040">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="cb73b-1041">Добавление параметра "—ResourceDiscoverMode" в Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="cb73b-1041">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="cb73b-1042">Добавление командлета Get-AzPolicyMetadata для получения ресурсов метаданных политики</span><span class="sxs-lookup"><span data-stu-id="cb73b-1042">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="cb73b-1043">Get-AzPolicyState и Get-AzPolicyStateSummary обновлены для API версии 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="cb73b-1043">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb73b-1044">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-1044">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb73b-1045">Поддержка Azure Site Recovery для удаления реплицированного диска.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1045">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="cb73b-1046">В Azure Backup добавлена ​​поддержка добавления тегов при создании Хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1046">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb73b-1047">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb73b-1047">Az.Resources</span></span>
* <span data-ttu-id="cb73b-1048">Сделайте команду "Область" необязательной в командлетах \*—AzPolicyAssignment с настройкой по умолчанию для контекстной подписки</span><span class="sxs-lookup"><span data-stu-id="cb73b-1048">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="cb73b-1049">Добавление примеров создания ADServicePrincipal с паролем и ключом учетных данных</span><span class="sxs-lookup"><span data-stu-id="cb73b-1049">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb73b-1050">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb73b-1050">Az.Sql</span></span>
<span data-ttu-id="cb73b-1051">Исправление командлета New-AzSqlDatabaseSecondary, чтобы проверить существование PartnerDatabaseName, а не DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1051">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb73b-1052">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb73b-1052">Az.Storage</span></span>
* <span data-ttu-id="cb73b-1053">Поддержка набора шифрования типа ключа таблиц и очередей в создании учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="cb73b-1053">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="cb73b-1054">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb73b-1054">New-AzStorageAccount</span></span>
* <span data-ttu-id="cb73b-1055">Представление RequestId, если StorageException не имеет ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="cb73b-1055">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="cb73b-1056">Исправление примера 6 командлета Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="cb73b-1056">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb73b-1057">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb73b-1057">Az.Websites</span></span>
* <span data-ttu-id="cb73b-1058">Set-AzWebapp и Set-AzWebappSlot поддерживают свойства AlwaysOn, MinTls и FtpsState</span><span class="sxs-lookup"><span data-stu-id="cb73b-1058">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="cb73b-1059">Устранение проблемы, при которой параметр HttpsOnly с одновременным изменением AppservicePlan с помощью одной команды Set-AzWebApp сбрасывал значение HttpsOnly до значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="cb73b-1059">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="cb73b-1060">3.3.0 — январь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1060">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb73b-1061">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb73b-1061">Az.Accounts</span></span>
* <span data-ttu-id="cb73b-1062">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment: теперь они принимают параметры AzureAttestationServiceEndpointResourceId и AzureAttestationServiceEndpointSuffix.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1062">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cb73b-1063">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cb73b-1063">Az.Cdn</span></span>
* <span data-ttu-id="cb73b-1064">Теперь в командлете New-AzCdnEndpoint отображаются сведения из сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1064">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb73b-1065">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb73b-1065">Az.Compute</span></span>
* <span data-ttu-id="cb73b-1066">Командлет Set-AzVMCustomScriptExtension исправлен для виртуальной машины с управляемым диском ОС без профиля ОС.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1066">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="cb73b-1067">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="cb73b-1067">Az.ContainerInstance</span></span>
* <span data-ttu-id="cb73b-1068">Исправлены имена параметров, используемые в примере командлета New-AzContainerGroup.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1068">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="cb73b-1069">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="cb73b-1069">Az.DataBoxEdge</span></span>
* <span data-ttu-id="cb73b-1070">Добавлен командлет Get-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1070">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="cb73b-1071">получение контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1071">Get the Edge Storage Container</span></span>
* <span data-ttu-id="cb73b-1072">Добавлен командлет New-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1072">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="cb73b-1073">создание контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1073">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="cb73b-1074">Добавлен командлет Remove-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1074">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="cb73b-1075">удаление контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1075">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="cb73b-1076">Добавлен командлет Invoke-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1076">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="cb73b-1077">вызов действия для обновления данных в контейнере хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1077">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="cb73b-1078">Добавлен командлет Get-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1078">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="cb73b-1079">получение учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1079">Get the Edge Storage Account</span></span>
* <span data-ttu-id="cb73b-1080">Добавлен командлет New-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1080">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="cb73b-1081">создание учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1081">Create new Edge Storage Account</span></span>
* <span data-ttu-id="cb73b-1082">Добавлен командлет Remove-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1082">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="cb73b-1083">удаление учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1083">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="cb73b-1084">Вызов командлета Invoke-AzDataBoxEdgeShare:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1084">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="cb73b-1085">вызов действия для обновления данных в общей папке.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1085">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="cb73b-1086">Добавлен командлет Set-AzDataBoxEdgeStorageAccountCredential:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1086">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="cb73b-1087">установка учетных данных для учетной записи хранилища Azure Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1087">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb73b-1088">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb73b-1088">Az.DataFactory</span></span>
* <span data-ttu-id="cb73b-1089">Добавлены свойства AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId и VersionStatus для командлета Get-AzDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1089">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="cb73b-1090">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.6.0.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1090">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="cb73b-1091">Для командлета Set-AzureRmDataFactoryV2IntegrationRuntime добавлен параметр PublicIPs, позволяющий включить создание среды Azure-SSIS IR со статическими общедоступными IP-адресами.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1091">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="cb73b-1092">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="cb73b-1092">Az.DevTestLabs</span></span>
* <span data-ttu-id="cb73b-1093">Удалена недействительная ссылка в файле Get-AzDtlAllowedVMSizesPolicy.md.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1093">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cb73b-1094">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cb73b-1094">Az.EventHub</span></span>
* <span data-ttu-id="cb73b-1095">Устранена проблема № 10634: исправлена ссылка на пустой объект для удаления пространства имен концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1095">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cb73b-1096">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cb73b-1096">Az.HDInsight</span></span>
* <span data-ttu-id="cb73b-1097">Устранена ошибка в файле Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1097">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="cb73b-1098">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="cb73b-1098">Az.MachineLearning</span></span>
* <span data-ttu-id="cb73b-1099">Вычислительная среда Машинного обучения больше недоступна, поэтому удалены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1099">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="cb73b-1100">Get-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="cb73b-1100">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="cb73b-1101">Get-AzMlOpClusterKey;</span><span class="sxs-lookup"><span data-stu-id="cb73b-1101">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="cb73b-1102">New-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="cb73b-1102">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="cb73b-1103">Remove-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="cb73b-1103">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="cb73b-1104">Set-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="cb73b-1104">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="cb73b-1105">Test-AzMlOpClusterSystemServicesUpdateAvailability;</span><span class="sxs-lookup"><span data-stu-id="cb73b-1105">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="cb73b-1106">Update-AzMlOpClusterSystemService.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1106">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb73b-1107">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb73b-1107">Az.Network</span></span>
* <span data-ttu-id="cb73b-1108">Обновлена зависимость Microsoft.Azure.Management.Sql от предварительной версии 1.36 до предварительной версии 1.37.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1108">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb73b-1109">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-1109">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb73b-1110">Добавлена поддержка Azure Site Recovery для виртуальных машин с управляемым диском, зашифрованных при хранении с помощью управляемых клиентом ключей, при восстановлении из Azure в поставщике Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1110">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="cb73b-1111">Добавлена поддержка Azure Site Recovery для необязательного ввода идентификатора набора шифрования диска при включении защиты в рамках восстановления из VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1111">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="cb73b-1112">Добавлена поддержка Azure Site Recovery для необязательного ввода идентификатора набора шифрования диска на уровне диска при включении защиты в рамках восстановления из VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1112">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="cb73b-1113">Добавлена поддержка Azure Site Recovery для обновления элемента, защищенного репликацией, путем сопоставления набора шифрования диска при восстановлении из HyperV в Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1113">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb73b-1114">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb73b-1114">Az.Resources</span></span>
* <span data-ttu-id="cb73b-1115">Исправлена ошибка в справочном документе о командлете Remove-AzTag.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1115">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb73b-1116">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb73b-1116">Az.Sql</span></span>
* <span data-ttu-id="cb73b-1117">Исправлена функция основных командлетов установки оценки уязвимостей: теперь она позволяет работать с базой данных master для базы данных Azure и ограничить ее в системных базах данных управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1117">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="cb73b-1118">Устранена ошибка, возникающая при создании группы отработки отказа экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1118">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="cb73b-1119">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="cb73b-1119">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="cb73b-1120">Добавлен новый допустимый тип лицензии: DR (аварийное восстановление).</span><span class="sxs-lookup"><span data-stu-id="cb73b-1120">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb73b-1121">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb73b-1121">Az.Storage</span></span>
* <span data-ttu-id="cb73b-1122">Добавлено предупреждающее сообщение о критическом изменении значения DefaultAction в следующем выпуске:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1122">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="cb73b-1123">Update-AzStorageAccountNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1123">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="cb73b-1124">Включена поддержка получения времени последней синхронизации учетной записи хранения путем выполнения командлета Get-AzureRmStorageAccount с параметром -IncludeGeoReplicationStats:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1124">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="cb73b-1125">Get-AzureRmStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1125">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="cb73b-1126">3.2.0 — декабрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1126">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="cb73b-1127">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="cb73b-1127">General</span></span>
* <span data-ttu-id="cb73b-1128">Обновление ссылок в .psd1 для использования относительного пути для всех модулей.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1128">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cb73b-1129">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb73b-1129">Az.Accounts</span></span>
* <span data-ttu-id="cb73b-1130">Установка правильного параметра UserAgent для телеметрии на стороне клиента для Az 4.0 (предварительная версия).</span><span class="sxs-lookup"><span data-stu-id="cb73b-1130">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="cb73b-1131">Отображение понятного пользователю сообщения об ошибке, если в Az 4.0 (предварительная версия) не указан контекст.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1131">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="cb73b-1132">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cb73b-1132">Az.Batch</span></span>
* <span data-ttu-id="cb73b-1133">Исправлена проблема [№ 10602](https://github.com/Azure/azure-powershell/issues/10602), из-за которой использование командлета **New-AzBatchPool** приводило к неправильной отправке VirtualMachineConfiguration.ContainerConfiguration или VirtualMachineConfiguration.DataDisks на сервер.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1133">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb73b-1134">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb73b-1134">Az.DataFactory</span></span>
* <span data-ttu-id="cb73b-1135">Обновление пакета SDK Фабрики данных для .NET до версии 4.5.0.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1135">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cb73b-1136">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cb73b-1136">Az.FrontDoor</span></span>
* <span data-ttu-id="cb73b-1137">Включена поддержка исключений управляемых правил WAF.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1137">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="cb73b-1138">Добавление SocketAddr в список автозавершения.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1138">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="cb73b-1139">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="cb73b-1139">Az.HealthcareApis</span></span>
* <span data-ttu-id="cb73b-1140">Обработка исключений.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1140">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cb73b-1141">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb73b-1141">Az.KeyVault</span></span>
* <span data-ttu-id="cb73b-1142">Исправлена ошибка при получении доступа к значению, которое может быть не задано.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1142">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="cb73b-1143">Управление сертификатами шифрования на основе эллиптических кривых.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1143">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="cb73b-1144">Включена возможность указания кривой для политик сертификатов.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1144">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb73b-1145">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb73b-1145">Az.Monitor</span></span>
* <span data-ttu-id="cb73b-1146">Добавление необязательного аргумента в команду добавления параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1146">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="cb73b-1147">Существующий аргумент switch указывает на то, что экспорт в Log Analytics должен выполняться в фиксированную схему</span><span class="sxs-lookup"><span data-stu-id="cb73b-1147">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="cb73b-1148">(выделенный тип данных).</span><span class="sxs-lookup"><span data-stu-id="cb73b-1148">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb73b-1149">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb73b-1149">Az.Network</span></span>
* <span data-ttu-id="cb73b-1150">В приложении AzureFirewall, NAT и сетевых правилах включена поддержка IpGroups.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1150">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb73b-1151">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb73b-1151">Az.Resources</span></span>
* <span data-ttu-id="cb73b-1152">Устранена проблема, из-за которой при развертывании шаблона не удавалось считать его параметр, если имя параметра конфликтовало с именем встроенного параметра.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1152">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="cb73b-1153">Обновлены командлеты политики для использования новой версии API 2019-09-01 с поддержкой группирования в определениях наборов политик.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1153">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb73b-1154">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb73b-1154">Az.Sql</span></span>
* <span data-ttu-id="cb73b-1155">Обновлена функция автоматического создания расширенного хранилища для службы оценки уязвимостей в учетной записи StorageV2.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1155">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb73b-1156">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb73b-1156">Az.Storage</span></span>
* <span data-ttu-id="cb73b-1157">Включена поддержка создания маркера SAS на основе удостоверения контейнера и большого двоичного объекта с аутентификацией Oauth на основе контекста службы хранилища:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1157">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="cb73b-1158">New-AzStorageContainerSASToken;</span><span class="sxs-lookup"><span data-stu-id="cb73b-1158">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="cb73b-1159">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="cb73b-1159">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="cb73b-1160">Отозвана поддержка ключей делегирования пользователя учетной записи хранения, а также всех маркеров SAS удостоверения:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1160">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="cb73b-1161">Revoke-AzStorageAccountUserDelegationKeys.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1161">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="cb73b-1162">Выполнено обновление до Microsoft.Azure.Management.Storage версии 14.2.0 для включения поддержки нового API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1162">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="cb73b-1163">Включена поддержка QuotaGiB (квота общего ресурса в ГиБ) для значений свыше 5120 в командлетах для работы с общими папками в плоскости управления и добавлен псевдоним Quota для параметра QuotaGiB.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1163">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="cb73b-1164">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="cb73b-1164">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="cb73b-1165">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="cb73b-1165">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="cb73b-1166">Добавлен псевдоним QuotaGiB для параметра Quota:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1166">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="cb73b-1167">Set-AzStorageShareQuota.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1167">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="cb73b-1168">Устранена проблема, из-за которой при использовании AzStorageContainerAcl могла очищаться хранимая политика доступа:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1168">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="cb73b-1169">Set-AzStorageContainerAcl.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1169">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="cb73b-1170">Версия 3.1.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1170">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cb73b-1171">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="cb73b-1171">Highlights since the last major release</span></span>
* <span data-ttu-id="cb73b-1172">Выпуск Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="cb73b-1172">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="cb73b-1173">Выпуск Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="cb73b-1173">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb73b-1174">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb73b-1174">Az.Compute</span></span>
* <span data-ttu-id="cb73b-1175">Функция повторного применения виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="cb73b-1175">VM Reapply feature</span></span>
    - <span data-ttu-id="cb73b-1176">Добавлен параметр повторного применения в командлет Set-AzVM.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1176">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="cb73b-1177">Функция AutomaticRepairs масштабируемого набора виртуальных машин:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1177">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="cb73b-1178">Добавлены параметры EnableAutomaticRepair, AutomaticRepairGracePeriod и AutomaticRepairMaxInstanceRepairsPercent в следующие командлеты:   New-AzVmssConfig Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cb73b-1178">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="cb73b-1179">Включена поддержка образа из коллекции разных клиентов для New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1179">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="cb73b-1180">Добавлен фрагмент Spot в средство заполнения аргументов параметра Priority в командлетах New-AzVM, New-AzVMConfig и New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1180">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="cb73b-1181">Добавлены параметры DiskIOPSReadWrite и DiskMBpsReadWrite в командлет Add-AzVmssDataDisk.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1181">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="cb73b-1182">Изменен параметр SourceImageId командлета New-AzGalleryImageVersion на необязательный.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1182">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="cb73b-1183">Добавлены параметры OSDiskImage и DataDiskImage в командлет New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1183">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="cb73b-1184">Добавлен параметр HyperVGeneration в командлет New-AzGalleryImageDefinition.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1184">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="cb73b-1185">Добавлены параметры SkipExtensionsOnOverprovisionedVMs в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1185">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="cb73b-1186">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="cb73b-1186">Az.DataBoxEdge</span></span>
* <span data-ttu-id="cb73b-1187">Добавлен командлет `Get-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1187">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="cb73b-1188">Получение заказа.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1188">Get the Order</span></span>
* <span data-ttu-id="cb73b-1189">Добавлен командлет `New-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1189">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="cb73b-1190">Создание заказа.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1190">Create new Order</span></span>
* <span data-ttu-id="cb73b-1191">Добавлен командлет `Remove-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1191">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="cb73b-1192">Удаление заказа.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1192">Remove the Order</span></span>
* <span data-ttu-id="cb73b-1193">Изменен командлет `New-AzDataBoxEdgeShare`.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1193">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="cb73b-1194">Создание локальной общей папки.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1194">Now creates Local Share</span></span>
* <span data-ttu-id="cb73b-1195">Добавлен командлет `Set-AzDataBoxEdgeRole`.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1195">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="cb73b-1196">Сопоставление IotRole с общей папкой.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1196">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="cb73b-1197">Добавлен командлет `Invoke-AzDataBoxEdgeDevice`.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1197">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="cb73b-1198">Вызов проверки обновлений, скачивание обновления, установка обновления на устройстве.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1198">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="cb73b-1199">Добавлен командлет `Get-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1199">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="cb73b-1200">Получение сведений о триггерах.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1200">Gets the information about Triggers</span></span>
* <span data-ttu-id="cb73b-1201">Добавлен командлет `New-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1201">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="cb73b-1202">Создание триггеров.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1202">Create new Triggers</span></span>
* <span data-ttu-id="cb73b-1203">Добавлен командлет `Remove-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1203">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="cb73b-1204">Удаление триггеров.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1204">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb73b-1205">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb73b-1205">Az.DataFactory</span></span>
* <span data-ttu-id="cb73b-1206">Обновление пакета SDK Фабрики данных для .NET до версии 4.4.0.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1206">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="cb73b-1207">Добавлен параметр ExpressCustomSetup в командлет Set-AzureRmDataFactoryV2IntegrationRuntime для включения конфигураций установки и сторонних компонентов без использования настраиваемого скрипта установки.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1207">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb73b-1208">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb73b-1208">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb73b-1209">Обновлена документация по Get-AzDataLakeStoreDeletedItem и Restore-AzDataLakeStoreDeletedItem.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1209">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cb73b-1210">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cb73b-1210">Az.EventHub</span></span>
* <span data-ttu-id="cb73b-1211">Исправлена проблема № 10301. Исправлен формат даты маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1211">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cb73b-1212">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cb73b-1212">Az.FrontDoor</span></span>
* <span data-ttu-id="cb73b-1213">Добавлен параметр MinimumTlsVersion в Enable-AzFrontDoorCustomDomainHttps и New-AzFrontDoorFrontendEndpointObject.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1213">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="cb73b-1214">Добавлены параметры HealthProbeMethod и EnabledState в New-AzFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1214">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="cb73b-1215">Добавлен новый командлет для создания объекта BackendPoolsSettings для передачи при создании и обновлении Front Door.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1215">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="cb73b-1216">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="cb73b-1216">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb73b-1217">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb73b-1217">Az.Network</span></span>
* <span data-ttu-id="cb73b-1218">Изменены примеры параметра FilterData Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1218">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="cb73b-1219">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="cb73b-1219">Az.PrivateDns</span></span>
* <span data-ttu-id="cb73b-1220">Пакет SDK PrivateDns для .NET обновлен до версии 1.0.0</span><span class="sxs-lookup"><span data-stu-id="cb73b-1220">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb73b-1221">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-1221">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb73b-1222">Включена поддержка Azure Site Recovery для выбора типа диска при включении защиты.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1222">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="cb73b-1223">Внесено исправление Azure Site Recovery для изменения действия плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1223">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="cb73b-1224">Включена поддержка восстановления SQL Azure Backup для принятия баз данных файлового потока.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1224">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="cb73b-1225">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="cb73b-1225">Az.RedisCache</span></span>
* <span data-ttu-id="cb73b-1226">Добавлен параметр MinimumTlsVersion в командлеты New-AzRedisCache и Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1226">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="cb73b-1227">Кроме того, добавлен параметр MinimumTlsVersion в выходные данные командлета Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1227">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="cb73b-1228">Добавлена проверка параметра -Size для командлетов Set-AzRedisCache и New-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1228">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb73b-1229">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb73b-1229">Az.Resources</span></span>
- <span data-ttu-id="cb73b-1230">Обновлены командлеты политики для использования новой версии API 2019-06-01 с новым свойством EnforcementMode в назначении политики.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1230">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="cb73b-1231">Обновлен пример справки по созданию определения политики</span><span class="sxs-lookup"><span data-stu-id="cb73b-1231">Updated create policy definition help example</span></span>
- <span data-ttu-id="cb73b-1232">Исправлена ошибка с параметром -ServicePrincipalName командлета Remove-AZADServicePrincipal с возвратом пустой ссылки, если имя субъекта службы не найдено.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1232">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="cb73b-1233">Исправлена ошибка с New-AZADServicePrincipal с возвратом пустой ссылки, если у клиента нет подписки.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1233">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="cb73b-1234">Изменен командлет New-AzAdServicePrincipal для добавления учетных данных только для связанного приложения.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1234">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb73b-1235">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb73b-1235">Az.Sql</span></span>
* <span data-ttu-id="cb73b-1236">Добавлена поддержка ReadReplicaCount для базы данных.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1236">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="cb73b-1237">Исправлена ошибка с Set-AzSqlDatabase, если избыточность в пределах зоны не настроена.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1237">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="cb73b-1238">Версия 3.0.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1238">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="cb73b-1239">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="cb73b-1239">General</span></span>
* <span data-ttu-id="cb73b-1240">Выпущена версия Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="cb73b-1240">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cb73b-1241">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb73b-1241">Az.Accounts</span></span>
* <span data-ttu-id="cb73b-1242">Добавлено сообщение об устаревании для псевдонима "Resolve-Error".</span><span class="sxs-lookup"><span data-stu-id="cb73b-1242">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="cb73b-1243">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="cb73b-1243">Az.Advisor</span></span>
* <span data-ttu-id="cb73b-1244">Добавлена новая категория Operational Excellence (Эффективность работы) в командлет Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1244">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="cb73b-1245">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cb73b-1245">Az.Batch</span></span>
* <span data-ttu-id="cb73b-1246">`CoreQuota` в `BatchAccountContext` переименован в `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1246">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="cb73b-1247">Также появился новый `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1247">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="cb73b-1248">Это влияет на **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1248">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="cb73b-1249">Параметр **New-AzBatchTask** `-ResourceFile` теперь принимает коллекцию объектов `PSResourceFile`, которые можно создать с помощью нового командлета **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1249">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="cb73b-1250">Новый командлет **New-AzBatchResourceFile**, который помогает создавать объекты `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1250">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="cb73b-1251">Их можно передавать в **New-AzBatchTask** в параметре `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1251">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="cb73b-1252">Это позволяет поддерживать два новых типа файлов ресурсов, которые дополняют существующий метод `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1252">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="cb73b-1253">Файлы ресурсов на основе `AutoStorageContainerName` скачивают весь контейнер автоматического хранения в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1253">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="cb73b-1254">Файлы ресурсов на основе `StorageContainerUrl` скачивают указанный в URL-адресе контейнер в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1254">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="cb73b-1255">Удалено свойство `ApplicationPackages` в `PSApplication`, который возвращается из **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1255">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="cb73b-1256">Отдельные пакеты в приложении теперь можно извлечь с помощью **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1256">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="cb73b-1257">Например: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1257">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="cb73b-1258">`ApplicationId` переименован в `ApplicationName` для **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** и **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1258">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="cb73b-1259">Теперь `ApplicationId` является псевдонимом для `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1259">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="cb73b-1260">Добавлено новое свойство `PSWindowsUserConfiguration` в `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1260">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="cb73b-1261">`Version` переименован в `Name` для `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1261">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="cb73b-1262">`BlobSource` переименован в `HttpUrl` для `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1262">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="cb73b-1263">Удалено свойство `OSDisk` из `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1263">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="cb73b-1264">Удалена операция **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1264">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="cb73b-1265">Больше она не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1265">This operation is no longer supported.</span></span>
* <span data-ttu-id="cb73b-1266">Удалено `TargetOSVersion` из `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1266">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="cb73b-1267">`CurrentOSVersion` переименован в `OSVersion` для `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1267">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="cb73b-1268">Удалено `DataEgressGiB` и `DataIngressGiB` из `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1268">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="cb73b-1269">Операция **Get-AzBatchNodeAgentSku** удалена и заменена на **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1269">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="cb73b-1270">**Get-AzBatchSupportedImage** возвращает те же данные, что и **Get-AzBatchNodeAgentSku**, но в более удобном формате.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1270">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="cb73b-1271">Также возвращаются новые непроверенные образы.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1271">New non-verified images are also now returned.</span></span> <span data-ttu-id="cb73b-1272">Включается и дополнительная информация о `Capabilities` и `BatchSupportEndOfLife` для каждого образа.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1272">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="cb73b-1273">Добавлена возможность монтировать файловые системы на каждом узле пула с помощью нового параметра `MountConfiguration` в **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1273">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="cb73b-1274">Теперь поддерживаются правила безопасности сети, которые блокируют сетевой доступ к пулу по исходящему порту трафика.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1274">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="cb73b-1275">Это выполняется с помощью свойства `SourcePortRanges` для `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1275">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="cb73b-1276">Что касается выполнения контейнеров, пакетная служба теперь поддерживает выполнение задачи в рабочей папке контейнера или рабочей папке задачи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1276">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="cb73b-1277">Выбор зависит от параметра `WorkingDirectory` в `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1277">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="cb73b-1278">Добавлена возможность указать коллекцию общедоступных IP-адресов для `PSNetworkConfiguration` с помощью нового свойства `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1278">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="cb73b-1279">Это гарантирует, что узлы в пуле будут иметь IP-адреса из списка, предоставленного пользователем.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1279">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="cb73b-1280">Если значение не задано, по умолчанию для `WaitForSuccess` в `PSSTartTask` используется значение `$True` (ранее `$False`).</span><span class="sxs-lookup"><span data-stu-id="cb73b-1280">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="cb73b-1281">Если значение не задано, по умолчанию для `Scope` в `PSAutoUserSpecification` используется значение `Pool` (ранее `Task` для Windows или `Pool` для Linux).</span><span class="sxs-lookup"><span data-stu-id="cb73b-1281">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cb73b-1282">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cb73b-1282">Az.Cdn</span></span>
* <span data-ttu-id="cb73b-1283">Добавлены UrlRewriteAction и CacheKeyQueryStringAction в RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1283">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="cb73b-1284">Исправлено несколько ошибок, таких как отсутствующий входной параметр Selector в командлете New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1284">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb73b-1285">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb73b-1285">Az.Compute</span></span>
* <span data-ttu-id="cb73b-1286">Функция набора шифрования диска</span><span class="sxs-lookup"><span data-stu-id="cb73b-1286">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="cb73b-1287">Новые командлеты:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="cb73b-1287">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="cb73b-1288">Добавлен параметр ProximityPlacementGroupId в следующие командлеты:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="cb73b-1288">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="cb73b-1289">Параметры DiskEncryptionSetId и EncryptionType добавлены в следующие командлеты:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="cb73b-1289">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="cb73b-1290">Добавлен параметр PublicIPAddressVersion в New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="cb73b-1290">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="cb73b-1291">FileUris для расширения пользовательских скриптов теперь будет защищенным, а не общедоступным параметром</span><span class="sxs-lookup"><span data-stu-id="cb73b-1291">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="cb73b-1292">Добавлено ScaleInPolicy в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cb73b-1292">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="cb73b-1293">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="cb73b-1293">Breaking changes</span></span>
    - <span data-ttu-id="cb73b-1294">Параметр UploadSizeInBytes применяется теперь вместо DiskSizeGB для New-AzDiskConfig, если CreateOption имеет значение Upload</span><span class="sxs-lookup"><span data-stu-id="cb73b-1294">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="cb73b-1295">PublishingProfile.Source.ManagedImage.Id заменяется на StorageProfile.Source.Id в объекте GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="cb73b-1295">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb73b-1296">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb73b-1296">Az.DataFactory</span></span>
* <span data-ttu-id="cb73b-1297">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.3.0.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1297">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb73b-1298">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb73b-1298">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb73b-1299">Обновлен пакет SDK для ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), включает следующие исправления</span><span class="sxs-lookup"><span data-stu-id="cb73b-1299">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="cb73b-1300">Не создается исключение при невозможности десериализовать значение времени создания для записи в корзине или каталоге.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1300">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="cb73b-1301">Предоставляется параметр для времени ожидания запроса в adlsclient</span><span class="sxs-lookup"><span data-stu-id="cb73b-1301">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="cb73b-1302">Исправлена передача исходного значения syncflag для восстановления badoffset</span><span class="sxs-lookup"><span data-stu-id="cb73b-1302">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="cb73b-1303">Исправлена операция EnumerateDirectory, чтобы она извлекала токен продолжения после проверки ответа</span><span class="sxs-lookup"><span data-stu-id="cb73b-1303">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="cb73b-1304">Исправлена ошибка объединения</span><span class="sxs-lookup"><span data-stu-id="cb73b-1304">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cb73b-1305">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cb73b-1305">Az.FrontDoor</span></span>
* <span data-ttu-id="cb73b-1306">Исправлены разные опечатки в разных частях модуля</span><span class="sxs-lookup"><span data-stu-id="cb73b-1306">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cb73b-1307">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cb73b-1307">Az.HDInsight</span></span>
* <span data-ttu-id="cb73b-1308">Исправлена ошибка, из-за которой клиент получал сообщение об ошибке 'Not a valid Base-64 string' (Не является допустимой строкой Base64) при выполнении Get-AzHDInsightCluster для получения кластера с хранилищем ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1308">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="cb73b-1309">Добавлен параметр с именем ApplicationId в три командлета Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig и New-AzHDInsightCluster, чтобы клиент мог предоставить идентификатор приложения субъекта-службы для доступа к Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1309">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="cb73b-1310">Для Microsoft.Azure.Management.HDInsight изменена версия с 2.1.0 на 5.1.0</span><span class="sxs-lookup"><span data-stu-id="cb73b-1310">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="cb73b-1311">Удалены пять командлетов:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1311">Removed five cmdlets:</span></span>
    - <span data-ttu-id="cb73b-1312">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="cb73b-1312">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="cb73b-1313">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="cb73b-1313">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="cb73b-1314">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="cb73b-1314">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="cb73b-1315">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="cb73b-1315">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="cb73b-1316">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="cb73b-1316">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="cb73b-1317">Добавлены три командлета:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1317">Added three cmdlets:</span></span>
    - <span data-ttu-id="cb73b-1318">Get-AzHDInsightMonitoring заменяет собой Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1318">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="cb73b-1319">Enable-AzHDInsightMonitoring заменяет собой Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1319">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="cb73b-1320">Disable-AzHDInsightMonitoring заменяет собой Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1320">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="cb73b-1321">Исправлен командлет Get-AzHDInsightProperties, чтобы он поддерживал получение сведений о возможностях из определенного расположения.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1321">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="cb73b-1322">Удалены наборы параметров ("Spark1", "Spark2") из Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1322">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="cb73b-1323">Добавлены примеры в справочные документы по командлету Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1323">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="cb73b-1324">Изменен тип выходных данных для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1324">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="cb73b-1325">Для Get-AzHDInsightProperties тип выходных данных изменен с CapabilitiesResponse на AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1325">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="cb73b-1326">Для Remove-AzHDInsightCluster тип выходных данных изменен с ClusterGetResponse на bool.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1326">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="cb73b-1327">Для Set-AzHDInsightGatewaySettings тип выходных данных изменен с HttpConnectivitySettings на GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1327">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="cb73b-1328">Добавлены несколько условий для проверки сценариев.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1328">Added some scenario test cases.</span></span>
* <span data-ttu-id="cb73b-1329">Удалены несколько псевдонимов: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1329">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cb73b-1330">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cb73b-1330">Az.IotHub</span></span>
* <span data-ttu-id="cb73b-1331">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="cb73b-1331">Breaking changes:</span></span>
    - <span data-ttu-id="cb73b-1332">Командлет Add-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1332">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="cb73b-1333">Удален набор параметров __AllParameterSets для командлета Add-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1333">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="cb73b-1334">Командлет Get-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1334">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="cb73b-1335">Удален набор параметров __AllParameterSets для командлета Get-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1335">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="cb73b-1336">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1336">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="cb73b-1337">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1337">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="cb73b-1338">Командлет New-AzIotHubExportDevice больше не поддерживает псевдоним New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1338">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="cb73b-1339">Командлет New-AzIotHubImportDevice больше не поддерживает псевдоним New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1339">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="cb73b-1340">Командлет Remove-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1340">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="cb73b-1341">Удален набор параметров __AllParameterSets для командлета Remove-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1341">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="cb73b-1342">Командлет Set-AzIotHub теперь не поддерживает параметр OperationsMonitoringProperties и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1342">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="cb73b-1343">Удален набор параметров UpdateOperationsMonitoringProperties для командлета Set-AzIotHub.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1343">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb73b-1344">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-1344">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb73b-1345">Azure Site Recovery поддерживает настройку сетевых ресурсов, например групп безопасности сети, общедоступных IP-адресов и внутренних подсистем балансировки нагрузки из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1345">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="cb73b-1346">Azure Site Recovery поддерживает запись на управляемый диск из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1346">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="cb73b-1347">Azure Site Recovery поддерживает сокращение NIC из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1347">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="cb73b-1348">Azure Site Recovery поддерживает ускорение сети NIC из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1348">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="cb73b-1349">Azure Site Recovery поддерживает автоматическое обновление агента из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1349">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="cb73b-1350">Azure Site Recovery поддерживает стандартный SSD-накопитель из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1350">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="cb73b-1351">Azure Site Recovery поддерживает двухпроходное шифрование диска Azure из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1351">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="cb73b-1352">Azure Site Recovery поддерживает новый добавленный диск из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1352">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="cb73b-1353">Добавлена функция SoftDelete для виртуальных машин и соответствующие тесты</span><span class="sxs-lookup"><span data-stu-id="cb73b-1353">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb73b-1354">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb73b-1354">Az.Resources</span></span>
* <span data-ttu-id="cb73b-1355">Обновлена сборка зависимостей Microsoft.Extensions.Caching.Memory с версии 1.1.1 до 2.2</span><span class="sxs-lookup"><span data-stu-id="cb73b-1355">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb73b-1356">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb73b-1356">Az.Network</span></span>
* <span data-ttu-id="cb73b-1357">Изменены все командлеты для PrivateEndpointConnection, чтобы они поддерживали универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1357">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="cb73b-1358">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1358">Updated cmdlet:</span></span>
        - <span data-ttu-id="cb73b-1359">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1359">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="cb73b-1360">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1360">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="cb73b-1361">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1361">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="cb73b-1362">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1362">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="cb73b-1363">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cb73b-1363">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="cb73b-1364">Добавлен новый командлет для PrivateLinkResource, который поддерживает универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1364">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="cb73b-1365">Новый командлет</span><span class="sxs-lookup"><span data-stu-id="cb73b-1365">New cmdlet:</span></span>
        - <span data-ttu-id="cb73b-1366">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="cb73b-1366">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="cb73b-1367">Добавлены новые поля и параметр для протокола прокси версии 2.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1367">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="cb73b-1368">Добавлено свойство EnableProxyProtocol в PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="cb73b-1368">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="cb73b-1369">Добавлено свойство LinkIdentifier в PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cb73b-1369">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="cb73b-1370">Обновлен New-AzPrivateLinkService для поддержки нового необязательного параметра EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1370">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="cb73b-1371">Исправлено описание параметра в справочной документации по командлету New-AzApplicationGatewaySku.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1371">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="cb73b-1372">Новые командлеты для поддержки политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="cb73b-1372">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="cb73b-1373">Добавлена поддержка дочерних ресурсов RouteTables для VirtualHub</span><span class="sxs-lookup"><span data-stu-id="cb73b-1373">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="cb73b-1374">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1374">New cmdlets added:</span></span>
        - <span data-ttu-id="cb73b-1375">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="cb73b-1375">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="cb73b-1376">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="cb73b-1376">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="cb73b-1377">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="cb73b-1377">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="cb73b-1378">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="cb73b-1378">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="cb73b-1379">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="cb73b-1379">Set-AzVirtualHub</span></span>
* <span data-ttu-id="cb73b-1380">Добавлена поддержка новых свойств SKU для VirtualHub и VirtualWANType в VirtualWan</span><span class="sxs-lookup"><span data-stu-id="cb73b-1380">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="cb73b-1381">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1381">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="cb73b-1382">New-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="cb73b-1382">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="cb73b-1383">Update-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="cb73b-1383">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="cb73b-1384">New-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="cb73b-1384">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="cb73b-1385">Update-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="cb73b-1385">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="cb73b-1386">Добавлена поддержка свойства EnableInternetSecurity для HubVnetConnection, VpnConnection и ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="cb73b-1386">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="cb73b-1387">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1387">New cmdlets added:</span></span>
        - <span data-ttu-id="cb73b-1388">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="cb73b-1388">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="cb73b-1389">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1389">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="cb73b-1390">New-AzureRmVirtualHubVnetConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="cb73b-1390">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="cb73b-1391">New-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="cb73b-1391">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="cb73b-1392">Update-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="cb73b-1392">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="cb73b-1393">New-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="cb73b-1393">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="cb73b-1394">Set-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="cb73b-1394">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="cb73b-1395">Добавлена поддержка настройки политики верхнего уровня WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="cb73b-1395">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="cb73b-1396">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1396">New cmdlets added:</span></span>
        - <span data-ttu-id="cb73b-1397">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="cb73b-1397">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="cb73b-1398">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="cb73b-1398">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="cb73b-1399">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="cb73b-1399">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="cb73b-1400">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="cb73b-1400">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="cb73b-1401">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="cb73b-1401">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="cb73b-1402">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb73b-1402">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="cb73b-1403">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1403">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="cb73b-1404">New-AzApplicationGatewayFirewallPolicy: добавлены параметры PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="cb73b-1404">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="cb73b-1405">Добавлена поддержка оператора Geo-Match для CustomRule</span><span class="sxs-lookup"><span data-stu-id="cb73b-1405">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="cb73b-1406">Добавлен параметр GeoMatch в оператор для FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="cb73b-1406">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="cb73b-1407">Добавлена поддержка политики брандмауэра perListener и perSite</span><span class="sxs-lookup"><span data-stu-id="cb73b-1407">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="cb73b-1408">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1408">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="cb73b-1409">New-AzApplicationGatewayHttpListener: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="cb73b-1409">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="cb73b-1410">New-AzApplicationGatewayPathRuleConfig: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="cb73b-1410">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="cb73b-1411">Исправлен учет регистра для требуемой подсети с именем AzureBastionSubnet в PSBastion</span><span class="sxs-lookup"><span data-stu-id="cb73b-1411">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="cb73b-1412">Поддержка полного доменного имени назначения в правилах сети и преобразованного полного доменного имени в правилах NAT для брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="cb73b-1412">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="cb73b-1413">Добавлена поддержка ресурсов верхнего уровня RouteTables для IpGroup</span><span class="sxs-lookup"><span data-stu-id="cb73b-1413">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="cb73b-1414">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1414">New cmdlets added:</span></span>
        - <span data-ttu-id="cb73b-1415">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="cb73b-1415">New-AzIpGroup</span></span>
        - <span data-ttu-id="cb73b-1416">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="cb73b-1416">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="cb73b-1417">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="cb73b-1417">Get-AzIpGroup</span></span>
        - <span data-ttu-id="cb73b-1418">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="cb73b-1418">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cb73b-1419">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cb73b-1419">Az.ServiceFabric</span></span>
* <span data-ttu-id="cb73b-1420">Удален командлет Add-AzServiceFabricApplicationCertificate, так как соответствующий сценарий выполняется командлетом Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1420">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb73b-1421">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb73b-1421">Az.Sql</span></span>
* <span data-ttu-id="cb73b-1422">Добавлена поддержка восстановления удаленных баз данных в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1422">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="cb73b-1423">Из кода удалены старые командлеты аудита.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1423">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="cb73b-1424">Удалены нерекомендуемые псевдонимы:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1424">Removed deprecated aliases:</span></span>
* <span data-ttu-id="cb73b-1425">Get-AzSqlDatabaseIndexRecommendations (вместо него используйте Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="cb73b-1425">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="cb73b-1426">Get-AzSqlDatabaseRestorePoints (вместо него используйте Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="cb73b-1426">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="cb73b-1427">Удален командлет Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="cb73b-1427">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="cb73b-1428">Удалены псевдонимы для нерекомендуемых командлетов параметров оценки уязвимостей</span><span class="sxs-lookup"><span data-stu-id="cb73b-1428">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="cb73b-1429">Командлеты расширенного обнаружения угроз объявлены устаревшими</span><span class="sxs-lookup"><span data-stu-id="cb73b-1429">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="cb73b-1430">Добавлены командлеты для отключения и включения рекомендаций о конфиденциальности для столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1430">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb73b-1431">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb73b-1431">Az.Storage</span></span>
* <span data-ttu-id="cb73b-1432">Поддержка включения большой общей папки при создании или обновлении учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="cb73b-1432">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="cb73b-1433">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb73b-1433">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="cb73b-1434">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb73b-1434">Set-AzStorageAccount</span></span>
* <span data-ttu-id="cb73b-1435">При закрытии или получении маркера файла пропускается проверка того, является ли входной путь файлом или каталогом, чтобы избежать сбоев при получении объектов в состоянии DeletePending.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1435">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="cb73b-1436">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="cb73b-1436">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="cb73b-1437">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="cb73b-1437">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="cb73b-1438">2.8.0 — октябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1438">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="cb73b-1439">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="cb73b-1439">General</span></span>
* <span data-ttu-id="cb73b-1440">Выпуск Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="cb73b-1440">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cb73b-1441">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb73b-1441">Az.Accounts</span></span>
* <span data-ttu-id="cb73b-1442">Обновление телеметрии и перезаписи URL-адресов для созданных модулей, исправление для модульных тестов Windows.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1442">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cb73b-1443">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb73b-1443">Az.ApiManagement</span></span>
* <span data-ttu-id="cb73b-1444">**Set-AzApiManagementApi** — в ApiVersionSet добавлена поддержка обновления API.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1444">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="cb73b-1445">исправлена проблема https://github.com/Azure/azure-powershell/issues/10068.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1445">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb73b-1446">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb73b-1446">Az.Automation</span></span>
* <span data-ttu-id="cb73b-1447">Исправлен командлет New-AzureAutomationSoftwareUpdateConfiguration для параметра перезагрузки Linux.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1447">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="cb73b-1448">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cb73b-1448">Az.Batch</span></span>
* <span data-ttu-id="cb73b-1449">Командлет **Get-AzBatchNodeAgentSku** объявлен устаревшим и будет заменен на **Get-AzBatchSupportImage** в версии 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1449">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb73b-1450">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb73b-1450">Az.Compute</span></span>
* <span data-ttu-id="cb73b-1451">В командлеты New-AzVM и New-AzVmss добавлены параметры Priority, EvictionPolicy и MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1451">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="cb73b-1452">Исправлены предупреждающее сообщение для командлетов Add-AzVMAdditionalUnattendContent и Add-AzVMSshPublicKey и справочная документация по ним.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1452">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="cb73b-1453">Для Set-AzVMDiskEncryptionExtension исправлено исключение -skipVmBackup для виртуальных машин Linux с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1453">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="cb73b-1454">Исправлена ошибка при изменении параметров шифрования в Set-AzVMDiskEncryptionExtension, реализован двухэтапный сценарий.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1454">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb73b-1455">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb73b-1455">Az.DataFactory</span></span>
* <span data-ttu-id="cb73b-1456">Добавлены команды CRUD для потока данных Фабрики данных Azure версии 2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow и Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1456">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="cb73b-1457">Добавлены команды действий для сеанса отладки потока данных Фабрики данных Azure версии 2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand и Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1457">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="cb73b-1458">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.2.0.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1458">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb73b-1459">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb73b-1459">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb73b-1460">Проверка учетной записи исправлена так, чтобы учетные записи, содержащие знак "-", можно было передавать без домена.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1460">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="cb73b-1461">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="cb73b-1461">Az.HealthcareApis</span></span>
* <span data-ttu-id="cb73b-1462">Версия PowerShell обновлена до 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1462">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="cb73b-1463">Версия пакета SDK обновлена до 1.0.2.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1463">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="cb73b-1464">В тестах обновлены ссылки на новую версию пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1464">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="cb73b-1465">Вложенная выходная структура заменена на плоскую.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1465">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cb73b-1466">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cb73b-1466">Az.IotHub</span></span>
* <span data-ttu-id="cb73b-1467">Добавлен новый источник маршрутизации DigitalTwinChangeEvents.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1467">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="cb73b-1468">Исправлены незначительные ошибки: Get-AzIothub не возвращает subscriptionId.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1468">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb73b-1469">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb73b-1469">Az.Monitor</span></span>
* <span data-ttu-id="cb73b-1470">Добавлены новые получатели групп действий: -ItsmReceiver, -VoiceReceiver, -ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1470">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="cb73b-1471">Для получателей включите общую схему оповещений.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1471">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="cb73b-1472">Это не касается получателей SMS, push-уведомлений приложения Azure, ITSM и голосовых сообщений.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1472">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="cb73b-1473">Веб-перехватчики теперь поддерживают аутентификацию Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1473">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb73b-1474">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb73b-1474">Az.Network</span></span>
* <span data-ttu-id="cb73b-1475">Добавлен новый командлет Get-AzAvailableServiceAlias, позволяющий получить псевдонимы для политик конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1475">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="cb73b-1476">В подключениях шлюза виртуальной сети появилась возможность добавлять селекторы трафика.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1476">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="cb73b-1477">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1477">New cmdlets added:</span></span>
        - <span data-ttu-id="cb73b-1478">New-AzureRmTrafficSelectorPolicy.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1478">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="cb73b-1479">В командлеты добавлены необязательные параметры -TrafficSelectorPolicies, -New-AzureRmVirtualNetworkGatewayConnection, -Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1479">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="cb73b-1480">В конфигурациях правил сетевой безопасности добавлена поддержка протоколов ESP и AH.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1480">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="cb73b-1481">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1481">Updated cmdlets:</span></span>
        - <span data-ttu-id="cb73b-1482">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1482">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="cb73b-1483">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1483">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="cb73b-1484">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1484">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="cb73b-1485">Улучшена обработка исключений в командлетах Cortex.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1485">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="cb73b-1486">Выпущены новые поколения и номера SKU VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1486">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="cb73b-1487">Представлены новые поколения VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1487">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="cb73b-1488">Представлены новые номера SKU VirtualNetworkGateways с высокой пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1488">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="cb73b-1489">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="cb73b-1489">Az.RedisCache</span></span>
* <span data-ttu-id="cb73b-1490">В справочную документацию по Set-AzRedisCache добавлены недостающие значения для параметра -Size.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1490">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb73b-1491">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb73b-1491">Az.Sql</span></span>
* <span data-ttu-id="cb73b-1492">Добавлена возможность назначать администратора Active Directory в Управляемом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1492">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb73b-1493">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb73b-1493">Az.Storage</span></span>
* <span data-ttu-id="cb73b-1494">Клиентская библиотека службы хранилища Azure обновлена до версии 11.1.0.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1494">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="cb73b-1495">NextPageLink теперь позволяет получить список контейнеров с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1495">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="cb73b-1496">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="cb73b-1496">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="cb73b-1497">NextPageLink теперь позволяет получить список учетных записей хранения из подписки.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1497">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="cb73b-1498">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb73b-1498">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="cb73b-1499">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="cb73b-1499">Az.StorageSync</span></span>
* <span data-ttu-id="cb73b-1500">Исправлена проблема 9810 с Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1500">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb73b-1501">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb73b-1501">Az.Websites</span></span>
* <span data-ttu-id="cb73b-1502">Обновление плана службы приложений с помощью Set-AzWebApp приводило к сбою приложения.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1502">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="cb73b-1503">2.7.0 — сентябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1503">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="cb73b-1504">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb73b-1504">Az.ApiManagement</span></span>
* <span data-ttu-id="cb73b-1505">В справочной документации по командлету Set-AzApiManagementPolicy обновлено описание параметра -Format.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1505">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="cb73b-1506">Из справочной документации удалены ссылки на нерекомендуемый командлет Update-AzApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1506">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="cb73b-1507">Вместо него следует использовать командлет Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1507">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb73b-1508">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb73b-1508">Az.Automation</span></span>
* <span data-ttu-id="cb73b-1509">В справочной документации по командлету Register-AzAutomationDscNode исправлена опечатка в примере.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1509">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="cb73b-1510">Добавлено уточнение об ограничениях ОС для командлета Register-AzAutomationDSCNode.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1510">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="cb73b-1511">Исправлено исключение пустой ссылки для параметра -Wait в командлете Start-AzAutomationRunbook.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1511">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb73b-1512">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb73b-1512">Az.Compute</span></span>
* <span data-ttu-id="cb73b-1513">Добавлен параметр UploadSizeInBytes для командлета New-AzDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1513">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="cb73b-1514">Добавлен добавочный параметр для командлета New-AzSnapshotConfig.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1514">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="cb73b-1515">Для виртуальной машины добавлены такие функции с низким приоритетом:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1515">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="cb73b-1516">Для командлета New-AzVMConfig добавлены параметры MaxPrice, EvictionPolicy и Priority.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1516">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="cb73b-1517">Для командлетов New-AzVmssConfig, Update-AzVM и Update-AzVmss добавлен параметр MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1517">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="cb73b-1518">Для командлета Get-AzAvailabilitySet устранена проблема со ссылкой на виртуальную машину, когда в нем перечисляются все группы доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1518">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="cb73b-1519">Исправлено исключение NULL для командлета Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1519">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="cb73b-1520">Исправлен метод поиска VHD для относительной конечной позиции.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1520">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="cb73b-1521">Устранена проблема с UltraSSD для командлетов New-AzVM и Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1521">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb73b-1522">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb73b-1522">Az.DataFactory</span></span>
* <span data-ttu-id="cb73b-1523">Добавлены 3 новые команды для ADF версии 2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription и Get-AzDataFactoryV2TriggerSubscriptionStatus.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1523">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="cb73b-1524">Пакет SDK ADF для .NET обновлен до версии 4.1.3.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1524">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cb73b-1525">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cb73b-1525">Az.HDInsight</span></span>
* <span data-ttu-id="cb73b-1526">Укажите критические изменения.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1526">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cb73b-1527">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cb73b-1527">Az.IotHub</span></span>
* <span data-ttu-id="cb73b-1528">Добавлена поддержка для вызова отработки отказа для IotHub в георегион аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1528">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="cb73b-1529">Добавлена поддержка для управления обогащением сообщений для IotHub.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1529">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="cb73b-1530">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1530">New cmdlets are:</span></span>
    - <span data-ttu-id="cb73b-1531">Add-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="cb73b-1531">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="cb73b-1532">Get-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="cb73b-1532">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="cb73b-1533">Remove-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="cb73b-1533">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="cb73b-1534">Set-AzIotHubMessageEnrichment.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1534">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb73b-1535">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb73b-1535">Az.Monitor</span></span>
* <span data-ttu-id="cb73b-1536">Указание на самую последнюю версию пакета SDK для монитора, т. е. 0.24.1-preview:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1536">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="cb73b-1537">В командлеты метрик добавлены некритические изменения, т. е. перечисление единиц поддерживает несколько новых значений.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1537">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="cb73b-1538">Эти командлеты доступны только для чтения, поэтому входные данные командлетов не будут изменены.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1538">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="cb73b-1539">Актуальная версия API запросов **ActionGroups** — **2019-06-01**. До этого была версия **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1539">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="cb73b-1540">Тесты сценария обновлены в соответствии с этим изменением.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1540">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="cb73b-1541">В конструкторы классов **EmailReceiver** и **WebhookReceiver** добавлен один новый обязательный аргумент — логическое значение с именем **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1541">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="cb73b-1542">Сейчас для него установлено значение **false**, чтобы скрыть это критическое изменение от командлетов.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1542">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="cb73b-1543">**Примечание**. Это временное изменение, которое должно быть подтверждено командой оповещения.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1543">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="cb73b-1544">Порядок аргументов для конструктора класса **Source** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1544">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="cb73b-1545">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1545">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="cb73b-1546">Порядок аргументов для конструктора класса **AlertingAction** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1546">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="cb73b-1547">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1547">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="cb73b-1548">Добавлена поддержка критериев динамического порога для оповещения метрики версии 2:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1548">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="cb73b-1549">New-AzMetricAlertRuleV2Criteria: теперь также позволяет создавать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1549">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="cb73b-1550">Add-AzMetricAlertRuleV2: теперь также позволяет принимать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1550">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="cb73b-1551">Добавлены усовершенствования в командлетах запланированных правил запросов (SQR).</span><span class="sxs-lookup"><span data-stu-id="cb73b-1551">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="cb73b-1552">Командлеты будут принимать параметр Location в обоих форматах: расположение (например, eastus) или отображаемое имя расположения (например, "восточная часть США").</span><span class="sxs-lookup"><span data-stu-id="cb73b-1552">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="cb73b-1553">Параметр Enabled проиллюстрирован в файлах справки надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1553">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="cb73b-1554">Добавлены примеры для необязательного параметра ActionGroup.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1554">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="cb73b-1555">Все файлы справки улучшены.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1555">Overall improved help files</span></span>
* <span data-ttu-id="cb73b-1556">Исправлена ошибка в определении типа области для командлета Set-AzActionRule.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1556">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb73b-1557">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb73b-1557">Az.Network</span></span>
* <span data-ttu-id="cb73b-1558">Исправлен неправильный пример в справочной документации по командлету New-AzApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1558">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="cb73b-1559">В справочную документацию по командлету Get-AzNetworkWatcherPacketCapture добавлено примечание, посвященное извлечению всех свойств для записи пакетов.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1559">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="cb73b-1560">В справочной документации по командлету Test-AzNetworkWatcherIPFlow исправлен пример: теперь он правильно перечисляет сетевые карты.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1560">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="cb73b-1561">Улучшен анализ облачных исключений для отображения дополнительных сведений (при их наличии).</span><span class="sxs-lookup"><span data-stu-id="cb73b-1561">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="cb73b-1562">Улучшен анализ облачных исключений для обработки дополнительного типа исключения SDK.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1562">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="cb73b-1563">Исправлено неправильное сопоставление моделей правил безопасности.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1563">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="cb73b-1564">Добавлены свойства сетевого интерфейса для компонента частного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1564">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="cb73b-1565">Для интерфейса PSNetworkInterface добавлено свойство PrivateEndpoint с типом PSResourceId.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1565">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="cb73b-1566">В PSNetworkInterfaceIPConfiguration добавлено свойство PrivateLinkConnectionProperties с типом PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1566">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="cb73b-1567">Добавлен новый класс модели: PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1567">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="cb73b-1568">Добавлен новый тип ApplicationRuleProtocolType "mssql" для ресурса Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1568">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="cb73b-1569">Поддержка многоканального подключения в Виртуальной глобальной сети:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1569">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="cb73b-1570">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="cb73b-1570">New cmdlets</span></span>
        - <span data-ttu-id="cb73b-1571">New-AzVpnSiteLink;</span><span class="sxs-lookup"><span data-stu-id="cb73b-1571">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="cb73b-1572">New-AzVpnSiteLinkConnection;</span><span class="sxs-lookup"><span data-stu-id="cb73b-1572">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="cb73b-1573">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1573">Updated cmdlet:</span></span>
        - <span data-ttu-id="cb73b-1574">New-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="cb73b-1574">New-VpnSite</span></span>
        - <span data-ttu-id="cb73b-1575">Update-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="cb73b-1575">Update-VpnSite</span></span>
        - <span data-ttu-id="cb73b-1576">New-VpnConnection;</span><span class="sxs-lookup"><span data-stu-id="cb73b-1576">New-VpnConnection</span></span>
        - <span data-ttu-id="cb73b-1577">Update-VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1577">Update-VpnConnection</span></span>
* <span data-ttu-id="cb73b-1578">Исправлены документы с некоторыми примерами PowerShell для использования командлетов AZ вместо командлетов AzureRM.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1578">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb73b-1579">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-1579">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb73b-1580">Для объекта AzureVMpolicy добавлен новый атрибут — ProtectedItemsCount.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1580">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="cb73b-1581">Добавлены тесты для политики виртуальной машины и восстановления исходной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1581">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb73b-1582">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb73b-1582">Az.Resources</span></span>
* <span data-ttu-id="cb73b-1583">Исправлена ошибка, при которой не удавалось вызвать командлет New-AzRoleAssignment без параметра Scope.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1583">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cb73b-1584">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cb73b-1584">Az.ServiceFabric</span></span>
* <span data-ttu-id="cb73b-1585">Исправлена опечатка в примере в справочной документации по командлету Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1585">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="cb73b-1586">Добавлены новые командлеты для управления приложениями и службами:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1586">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="cb73b-1587">New-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="cb73b-1587">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="cb73b-1588">New-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="cb73b-1588">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="cb73b-1589">New-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="cb73b-1589">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="cb73b-1590">New-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="cb73b-1590">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="cb73b-1591">Update-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="cb73b-1591">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="cb73b-1592">Get-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="cb73b-1592">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="cb73b-1593">Get-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="cb73b-1593">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="cb73b-1594">Get-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="cb73b-1594">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="cb73b-1595">Get-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="cb73b-1595">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="cb73b-1596">Remove-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="cb73b-1596">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="cb73b-1597">Remove-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="cb73b-1597">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="cb73b-1598">Remove-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="cb73b-1598">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="cb73b-1599">Remove-AzServiceFabricServic.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1599">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="cb73b-1600">Пакет SDK для Service Fabric обновлен до версии 1.2.0, в которой используется версия API 2019-03-01 поставщика ресурсов Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1600">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="cb73b-1601">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="cb73b-1601">Az.SignalR</span></span>
* <span data-ttu-id="cb73b-1602">Добавлены командлеты Update, Restart, CheckNameAvailability и GetUsage.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1602">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb73b-1603">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb73b-1603">Az.Sql</span></span>
* <span data-ttu-id="cb73b-1604">Обновлен пример в справочной документации по командлету Get-AzSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1604">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="cb73b-1605">Добавлен пример виртуального ядра для командлета создания эластичного пула (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="cb73b-1605">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="cb73b-1606">Удалена проверка свойства EmailAddresses и того, что свойство EmailAdmins правильное в случае, если свойство EmailAddresses пустое в командлетах Set-AzSqlServerAdvancedThreatProtectionPolicy и Set-AzSqlDatabaseAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1606">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="cb73b-1607">Теперь, если существует несколько параметров диагностики, включающих категорию аудита, параметры аудита сервера и базы данных удаляются.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1607">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="cb73b-1608">Исправлена проверка адресов электронной почты в нескольких командлетах оценки уязвимостей SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting и Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="cb73b-1608">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb73b-1609">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb73b-1609">Az.Storage</span></span>
* <span data-ttu-id="cb73b-1610">Обновлен пример в справочной документации по командлету Get-AzStorageAccountKey.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1610">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="cb73b-1611">Теперь при отправке и загрузке файла Azure в конечном файле сохраняются свойства SMB исходного файла (атрибуты файла, время создания файла, время последней записи файла).</span><span class="sxs-lookup"><span data-stu-id="cb73b-1611">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="cb73b-1612">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="cb73b-1612">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="cb73b-1613">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="cb73b-1613">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="cb73b-1614">Исправлена операция отправки блочного BLOB-объекта, в которой происходили сбои свойств и метаданных в контейнере с включенной ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1614">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="cb73b-1615">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cb73b-1615">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="cb73b-1616">Добавлена поддержка управления общими папками Azure в API плоскости управления с помощью таких командлетов:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1616">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="cb73b-1617">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="cb73b-1617">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="cb73b-1618">Get-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="cb73b-1618">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="cb73b-1619">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="cb73b-1619">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="cb73b-1620">Remove-AzRmStorageShare.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1620">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb73b-1621">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb73b-1621">Az.Websites</span></span>
* <span data-ttu-id="cb73b-1622">Устранена проблема, из-за которой теги webapp удалялись при переносе приложения в новый ASP.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1622">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="cb73b-1623">Теперь командлет Publish-AzureWebapp работает в Linux и Windows.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1623">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="cb73b-1624">Обновлен пример в справочной документации по командлету Get-AzWebAppPublishingProfile.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1624">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="cb73b-1625">2.6.0 — август 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1625">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="cb73b-1626">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="cb73b-1626">General</span></span>
* <span data-ttu-id="cb73b-1627">Исправлены опечатки в модулях.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1627">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cb73b-1628">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb73b-1628">Az.Accounts</span></span>
* <span data-ttu-id="cb73b-1629">Добавлена поддержка назначаемого пользователем удостоверения MSI при проверке подлинности в Функциях Azure (№ 9479).</span><span class="sxs-lookup"><span data-stu-id="cb73b-1629">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="cb73b-1630">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cb73b-1630">Az.Aks</span></span>
* <span data-ttu-id="cb73b-1631">Устранена проблема с выходными данными для Get-AzAks.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1631">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="cb73b-1632">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9847.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1632">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cb73b-1633">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb73b-1633">Az.ApiManagement</span></span>
* <span data-ttu-id="cb73b-1634">исправлена проблема https://github.com/Azure/azure-powershell/issues/9351.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1634">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="cb73b-1635">Обновлена версия NuGet для .NET, которая не накладывает ограничений на productId, apiId, groupId и userId.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1635">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="cb73b-1636">**Get-AzApiManagementProduct**. Добавлена поддержка запросов к продуктам с помощью API.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1636">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="cb73b-1637">**New-AzApiManagementApiRevision**. Устранена проблема, из-за которой не задавался параметр ApiRevisionDescription при создании новой редакции API https://github.com/Azure/azure-powershell/issues/9752.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1637">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="cb73b-1638">Исправлено написание имени модели c PsApiManagementOAuth2AuthrozationServer на PsApiManagementOAuth2AuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1638">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="cb73b-1639">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cb73b-1639">Az.Batch</span></span>
* <span data-ttu-id="cb73b-1640">Исправлена опечатка в написании Windows со строчной буквы в справочных сообщениях и документации.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1640">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cb73b-1641">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cb73b-1641">Az.Cdn</span></span>
* <span data-ttu-id="cb73b-1642">Исправлена опечатка во вспомогательном приложении модуля CDN.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1642">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb73b-1643">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb73b-1643">Az.Compute</span></span>
* <span data-ttu-id="cb73b-1644">Добавлен параметр VmssId в новый командлет Add New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1644">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="cb73b-1645">Добавлены параметры TerminateScheduledEvents и TerminateScheduledEventNotBeforeTimeoutInMinutes в New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1645">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="cb73b-1646">Добавлено свойство HyperVGeneration в объект образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1646">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="cb73b-1647">Добавлены компоненты Host и HostGroup.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1647">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="cb73b-1648">Новые командлеты:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="cb73b-1648">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="cb73b-1649">Параметр HostId добавлен в New-AzVMConfig и New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1649">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="cb73b-1650">Исправлен пример в документации по Invoke-AzVMRunCommand, в котором теперь используется правильное имя параметра.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1650">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="cb73b-1651">Исправлено описание VolumeType в справочной документации по Set-AzVMDiskEncryptionExtension и Set-AzVmssDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1651">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb73b-1652">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb73b-1652">Az.DataFactory</span></span>
* <span data-ttu-id="cb73b-1653">Исправлена опечатка в написании Windows со строчной буквы в документации по New-AzDataFactoryEncryptValue.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1653">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="cb73b-1654">Пакет SDK ADF для .NET обновлен до версии 4.1.2.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1654">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="cb73b-1655">Добавлены параметры DataProxyIntegrationRuntimeName, DataProxyStagingLinkedServiceName и DataProxyStagingPath в командлет Set-AzureRmDataFactoryV2IntegrationRuntime, что позволяет настраивать локальную среду выполнения интеграции в качестве прокси-сервера для Azure-SSIS Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1655">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="cb73b-1656">Обновлены PSTriggerRun для отображения активированных конвейеров, сообщений и свойств и PSActivityRun для отображения типа действия.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1656">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb73b-1657">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb73b-1657">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb73b-1658">Устранена проблема, при которой Get-DataLakeStoreDeletedItem переставал отвечать на запросы при возникновении ошибок или удаленных исключений.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1658">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cb73b-1659">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cb73b-1659">Az.EventHub</span></span>
* <span data-ttu-id="cb73b-1660">Исправлена проблема № 9658: опечатка в написании параметра VirtualNteworkRule у Set-AzEventHubNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1660">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="cb73b-1661">Исправлена проблема № 9558: в Set-AzEventHubNamespace используется PATCH вместо PUT.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1661">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="cb73b-1662">В командлет Set-AzEventHubNamespace добавлен параметр EnableKafka.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1662">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="cb73b-1663">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1663">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="cb73b-1664">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="cb73b-1664">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="cb73b-1665">Исправлено написание Azure со строчной буквы.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1665">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb73b-1666">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb73b-1666">Az.Monitor</span></span>
* <span data-ttu-id="cb73b-1667">Исправлены неправильные имена параметров в справочной документации.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1667">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb73b-1668">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb73b-1668">Az.Network</span></span>
* <span data-ttu-id="cb73b-1669">Обновлен New-AzPrivateLinkServiceIpConfig.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1669">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="cb73b-1670">Параметр PublicIpAddress объявлен нерекомендуемым, так как он не используется на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1670">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="cb73b-1671">Добавлен необязательный параметр Primary, указывающий, является ли текущая IP-конфигурация основной.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1671">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="cb73b-1672">Улучшена обработка исключений из-за ошибок запроса от пакета SDK. Устранена проблема, при которой исключения пакета SDK не обрабатывались правильно, из-за чего не отображались основные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1672">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="cb73b-1673">Настроена логика проверки для префикса IPv6 IP-адреса для проверки правильности длины префикса IPv6.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1673">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="cb73b-1674">Обновлен Get-AzVirtualNetworkSubnetConfig: добавлен набор параметров для получения по идентификатору ресурса подсети.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1674">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="cb73b-1675">Обновлено описание параметра Location для AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1675">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cb73b-1676">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cb73b-1676">Az.OperationalInsights</span></span>
* <span data-ttu-id="cb73b-1677">Обновлена документация по New-AzOperationalInsightsLinuxSyslogDataSource.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1677">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="cb73b-1678">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1678">Added example</span></span>
    - <span data-ttu-id="cb73b-1679">Обновлено описание параметра -Name.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1679">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="cb73b-1680">Добавлен пример для New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="cb73b-1680">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="cb73b-1681">Изменено описание параметра -Name для New-AzOperationalInsightsWindowsEventDataSource.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1681">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb73b-1682">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-1682">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb73b-1683">Обновлен Get-AzRecoveryServicesBackupJobDetail.md.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1683">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb73b-1684">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb73b-1684">Az.Resources</span></span>
* <span data-ttu-id="cb73b-1685">Добавлена поддержка новой версии API 2019-05-10 для Microsoft.Resource.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1685">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="cb73b-1686">Добавлена поддержка copy.count = 0 для переменных, ресурсов и свойств.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1686">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="cb73b-1687">Ресурсы, у которых condition = false или copy.count = 0, будут удаляться в полном режиме.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1687">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="cb73b-1688">В справочную документацию добавлен пример назначения политики на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1688">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="cb73b-1689">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cb73b-1689">Az.ServiceBus</span></span>
* <span data-ttu-id="cb73b-1690">Исправлена проблема № 9658: опечатка в написании параметра VirtualNetworkRule В Set-AzServiceBusNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1690">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="cb73b-1691">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1691">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="cb73b-1692">Добавлена новая команда Test-AzServiceBusNameAvailability для проверки доступности имени для очереди и раздела.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1692">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cb73b-1693">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cb73b-1693">Az.ServiceFabric</span></span>
* <span data-ttu-id="cb73b-1694">Устранены ошибки командлета для добавления типа узла:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1694">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="cb73b-1695">ошибка NullReferenceException, возникавшая, если у группы ресурсов были другие VMSS, не связанные с кластером Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1695">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="cb73b-1696">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8681.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1696">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="cb73b-1697">Исправлена ошибка, из-за которой командлет завершился сбоем, если virtualNetwork находилась не в той группе ресурсов, к которой относится кластер.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1697">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="cb73b-1698">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8407.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1698">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="cb73b-1699">Командлет Add-AzServiceFabricApplicationCertificate объявлен нерекомендуемым.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1699">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb73b-1700">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb73b-1700">Az.Sql</span></span>
* <span data-ttu-id="cb73b-1701">Обновление документации по старым командлетам аудита.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1701">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb73b-1702">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb73b-1702">Az.Storage</span></span>
* <span data-ttu-id="cb73b-1703">Обновлена справка по Get/Close-AzStorageFileHandle: в примеры добавлены сценарии использования командлетов и обновлено описание параметров.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1703">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="cb73b-1704">Добавлена поддержка StandardBlobTier в операции отправки BLOB-объекта и копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1704">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="cb73b-1705">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cb73b-1705">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="cb73b-1706">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="cb73b-1706">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="cb73b-1707">Добавлена поддержка приоритета восстановления в операцию копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1707">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="cb73b-1708">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="cb73b-1708">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb73b-1709">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb73b-1709">Az.Websites</span></span>
* <span data-ttu-id="cb73b-1710">Добавлены уточнение для параметра -AppSettings в Set-AzWebApp и Set-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1710">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="cb73b-1711">2.5.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1711">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb73b-1712">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb73b-1712">Az.Accounts</span></span>
* <span data-ttu-id="cb73b-1713">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1713">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="cb73b-1714">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="cb73b-1714">Az.ApplicationInsights</span></span>
* <span data-ttu-id="cb73b-1715">Исправлена опечатка в примере в документации по Remove-AzApplicationInsightsApiKey.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1715">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb73b-1716">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb73b-1716">Az.Automation</span></span>
* <span data-ttu-id="cb73b-1717">Исправлена опечатка в строке ресурса.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1717">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cb73b-1718">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-1718">Az.CognitiveServices</span></span>
* <span data-ttu-id="cb73b-1719">Добавлена поддержка NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1719">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb73b-1720">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb73b-1720">Az.Compute</span></span>
* <span data-ttu-id="cb73b-1721">Добавлены недостающие свойства (ComputerName, OsName, OsVersion и HyperVGeneration) для объекта представления экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1721">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="cb73b-1722">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="cb73b-1722">Az.ContainerRegistry</span></span>
* <span data-ttu-id="cb73b-1723">Исправлена опечатка в Remove-AzContainerRegistryReplication для параметра репликации.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1723">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="cb73b-1724">См. подробнее: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1724">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb73b-1725">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb73b-1725">Az.DataFactory</span></span>
* <span data-ttu-id="cb73b-1726">Пакет SDK для ADF .NET обновлен до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1726">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="cb73b-1727">Исправлена опечатка в документации по Get-AzDataFactoryV2PipelineRun.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1727">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cb73b-1728">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cb73b-1728">Az.EventHub</span></span>
* <span data-ttu-id="cb73b-1729">Добавлен новый командлет для создания маркера SAS: New-AzEventHubAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1729">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="cb73b-1730">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="cb73b-1730">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cb73b-1731">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb73b-1731">Az.KeyVault</span></span>
* <span data-ttu-id="cb73b-1732">Добавлена поддержка для настройки параметра KeySize в политиках сертификатов.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1732">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="cb73b-1733">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="cb73b-1733">Az.LogicApp</span></span>
* <span data-ttu-id="cb73b-1734">Get-AzIntegrationAccountMap теперь надлежащим образом выводит все типы сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1734">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="cb73b-1735">Добавлен новый параметр MapType для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1735">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="cb73b-1736">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-1736">Az.ManagedServices</span></span>
* <span data-ttu-id="cb73b-1737">Добавлена поддержка API версии 2019-06-01 (общедоступная).</span><span class="sxs-lookup"><span data-stu-id="cb73b-1737">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb73b-1738">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb73b-1738">Az.Network</span></span>
* <span data-ttu-id="cb73b-1739">Добавлена поддержка частной конечной точки и службы приватного канала.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1739">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="cb73b-1740">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="cb73b-1740">New cmdlets</span></span>
        - <span data-ttu-id="cb73b-1741">Set-AzPrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1741">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="cb73b-1742">Set-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1742">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="cb73b-1743">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1743">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="cb73b-1744">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1744">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="cb73b-1745">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1745">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="cb73b-1746">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1746">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="cb73b-1747">Test-AzPrivateLinkServiceVisibility.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1747">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="cb73b-1748">Get-AzAutoApprovedPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1748">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="cb73b-1749">Обновлены следующие команды для функции: Флаг PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies в подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1749">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="cb73b-1750">Обновлены командлеты New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1750">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="cb73b-1751">Добавлен необязательный параметр -PrivateEndpointNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к частной конечной точке в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1751">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="cb73b-1752">Добавлен необязательный параметр -PrivateLinkServiceNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к службе приватного канала в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1752">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="cb73b-1753">Параметр ServiceName командлета AzPrivateLinkService был переименован на Name с псевдонимом ServiceName для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1753">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="cb73b-1754">Включен протокол ICMP для настройки правил безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1754">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="cb73b-1755">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="cb73b-1755">Updated cmdlets</span></span>
        - <span data-ttu-id="cb73b-1756">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1756">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="cb73b-1757">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1757">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="cb73b-1758">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1758">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="cb73b-1759">Добавлен ConnectionProtocolType (Ikev1/Ikev2) в качестве настраиваемого параметра для командлета New-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1759">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="cb73b-1760">Добавлен PrivateIpAddressVersion в LoadBalancerFrontendIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1760">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="cb73b-1761">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1761">Updated cmdlet:</span></span>
        - <span data-ttu-id="cb73b-1762">New-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1762">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="cb73b-1763">Add-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1763">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="cb73b-1764">Set-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1764">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="cb73b-1765">Команда New-AzApplicationGatewayProbeConfig Шлюза приложений обновлена для поддержки настраиваемого порта в зонде.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1765">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="cb73b-1766">Обновлен командлет New-AzApplicationGatewayProbeConfig: добавлен необязательный параметр Port, который используется при проверке внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1766">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="cb73b-1767">Этот параметр применяется к номерам SKU Standard_V2 и WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1767">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cb73b-1768">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cb73b-1768">Az.OperationalInsights</span></span>
* <span data-ttu-id="cb73b-1769">Обновленная версия по умолчанию для сохраненных операций поиска имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1769">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="cb73b-1770">Исправлены ошибки при обработке регулярных выражений со значениями NULL в журналах.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1770">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb73b-1771">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-1771">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb73b-1772">Обновлен файл Get-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1772">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="cb73b-1773">Обновлен файл Get-AzRecoveryServicesBackupContainer.md.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1773">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="cb73b-1774">Обновлен файл Get-AzRecoveryServicesVault.md.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1774">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="cb73b-1775">Обновлен файл Wait-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1775">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="cb73b-1776">Обновлен файл Set-AzRecoveryServicesVaultContext.md.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1776">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="cb73b-1777">Обновлен файл Get-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1777">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="cb73b-1778">Обновлен файл Get-AzRecoveryServicesBackupRecoveryPoint.md.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1778">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="cb73b-1779">Обновлен файл Restore-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1779">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="cb73b-1780">Обновлен вызов службы для отмены регистрации контейнера в общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1780">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="cb73b-1781">Обновлен файл Set-AzRecoveryServicesAsrAlertSetting.md.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1781">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb73b-1782">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb73b-1782">Az.Resources</span></span>
- <span data-ttu-id="cb73b-1783">Удален отсутствующий командлет, который упоминается в документации по New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1783">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="cb73b-1784">Обновлены командлеты политик для использования новой версии API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1784">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="cb73b-1785">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cb73b-1785">Az.ServiceBus</span></span>
* <span data-ttu-id="cb73b-1786">Добавлен новый командлет для создания маркера SAS: New-AzServiceBusAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1786">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="cb73b-1787">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="cb73b-1787">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb73b-1788">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb73b-1788">Az.Sql</span></span>
* <span data-ttu-id="cb73b-1789">Исправлены отсутствующие примеры для командлета Set-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1789">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="cb73b-1790">Исправлены заданные повторяющиеся проверки для оценки наличия уязвимостей без указания адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1790">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="cb73b-1791">Исправлена незначительная опечатка в сообщении предупреждения.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1791">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb73b-1792">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb73b-1792">Az.Storage</span></span>
* <span data-ttu-id="cb73b-1793">Обновлен пример в справочной документации для использования командлетом Get-AzStorageAccount правильного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1793">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="cb73b-1794">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="cb73b-1794">Az.StorageSync</span></span>
* <span data-ttu-id="cb73b-1795">Добавлен командлет Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1795">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="cb73b-1796">Исправлена проблема № 9551, связанная с TierFilesOlderThanDays.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1796">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb73b-1797">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb73b-1797">Az.Websites</span></span>
* <span data-ttu-id="cb73b-1798">Исправлена ошибка, при которой некоторые свойства SiteConfig не возвращались Get-AzWebApp и Set-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1798">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="cb73b-1799">Добавлен новый параметр Location в Get-AzDeletedWebApp и Restore-AzDeletedWebApp.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1799">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="cb73b-1800">Исправлена ошибка, которая возникала при клонировании слотов веб-приложений с помощью командлета New-AzWebApp-IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1800">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="cb73b-1801">2.4.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1801">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb73b-1802">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb73b-1802">Az.Accounts</span></span>
* <span data-ttu-id="cb73b-1803">Добавлена поддержка командлетов профиля.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1803">Add support for profile cmdlets</span></span>
* <span data-ttu-id="cb73b-1804">Добавлена поддержка сред и плоскостей данных в созданных командлетах.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1804">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="cb73b-1805">Исправлена ошибка, когда в командлетах плоскости данных в Windows PowerShell в некоторых случаях использовалась неправильная конечная точка.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1805">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="cb73b-1806">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="cb73b-1806">Az.Advisor</span></span>
* <span data-ttu-id="cb73b-1807">Выпущена общедоступная версия Az.Advisor.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1807">GA release of Az.Advisor</span></span>
* <span data-ttu-id="cb73b-1808">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1808">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cb73b-1809">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb73b-1809">Az.ApiManagement</span></span>
* <span data-ttu-id="cb73b-1810">исправлена проблема https://github.com/Azure/azure-powershell/issues/8671.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1810">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="cb73b-1811">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="cb73b-1811">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="cb73b-1812">Добавлена поддержка запрашивания подписок по пользователю и продукту.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1812">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="cb73b-1813">Добавлена поддержка создания запросов с использованием области "/", "/apis", "/apis/echo-api".</span><span class="sxs-lookup"><span data-stu-id="cb73b-1813">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="cb73b-1814">Исправлены проблемы https://github.com/Azure/azure-powershell/issues/9307 и https://github.com/Azure/azure-powershell/issues/8432.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1814">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="cb73b-1815">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="cb73b-1815">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="cb73b-1816">Добавлена поддержка указания ApiVersion и ApiVersionSetId при импорте API-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1816">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb73b-1817">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb73b-1817">Az.Automation</span></span>
* <span data-ttu-id="cb73b-1818">Исправлена ошибка командлета Set-AzAutomationConnectionFieldValue при обработке строкового значения.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1818">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb73b-1819">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb73b-1819">Az.Compute</span></span>
* <span data-ttu-id="cb73b-1820">В New AzImageConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1820">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb73b-1821">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb73b-1821">Az.DataFactory</span></span>
* <span data-ttu-id="cb73b-1822">Обновление выходных данных командлетов ADF, предназначенных для получения числа выполнений действий, конвейеров и триггеров, для поддержки канала Select-Object.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1822">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="cb73b-1823">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="cb73b-1823">Az.EventGrid</span></span>
* <span data-ttu-id="cb73b-1824">Исправлена опечатка в документации по командлету New-AzEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1824">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cb73b-1825">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cb73b-1825">Az.IotHub</span></span>
* <span data-ttu-id="cb73b-1826">Добавлена поддержка повторного создания ключей политики авторизации.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1826">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb73b-1827">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb73b-1827">Az.Network</span></span>
* <span data-ttu-id="cb73b-1828">К тегам общедоступного IP-адреса добавлен тег RoutingPreference.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1828">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="cb73b-1829">Улучшены примеры для справочной документации по командлету Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1829">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cb73b-1830">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cb73b-1830">Az.PolicyInsights</span></span>
* <span data-ttu-id="cb73b-1831">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1831">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="cb73b-1832">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9446.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1832">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cb73b-1833">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cb73b-1833">Az.OperationalInsights</span></span>
* <span data-ttu-id="cb73b-1834">Исправленная модель источника данных CustomLog возвращена в командлет Get-AzOperationalInsightsDataSource.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1834">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb73b-1835">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-1835">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb73b-1836">Выпущено исправление для команды get-policy для виртуальных машин IaaS.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1836">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb73b-1837">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb73b-1837">Az.Resources</span></span>
    - <span data-ttu-id="cb73b-1838">Исправлен текст справки по параметру Get-AzPolicyState -Top.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1838">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="cb73b-1839">Добавлена поддержка разбиения по страницам на стороне клиента для Get-AzPolicyAlias.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1839">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="cb73b-1840">Добавлены новые параметры для Set-AzPolicyAssignment, -PolicyParameters и -PolicyParametersObject.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1840">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="cb73b-1841">Добавлен ряд обновлений документов и примеров для командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1841">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="cb73b-1842">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cb73b-1842">Az.ServiceBus</span></span>
* <span data-ttu-id="cb73b-1843">Исправление ошибки № 4938: командлет New-AzureRmServiceBusQueue возвращает ответ BadRequest (Недопустимый запрос) при задании значения MaxSizeInMegabytes.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1843">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb73b-1844">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb73b-1844">Az.Sql</span></span>
* <span data-ttu-id="cb73b-1845">Из выпуска предварительной версии в выпуск общедоступной версии добавлены командлеты группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1845">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="cb73b-1846">Поддержка аудита Azure SQL Server и баз данных с помощью новых командлетов:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1846">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="cb73b-1847">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="cb73b-1847">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="cb73b-1848">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="cb73b-1848">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="cb73b-1849">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="cb73b-1849">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="cb73b-1850">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="cb73b-1850">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="cb73b-1851">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="cb73b-1851">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="cb73b-1852">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="cb73b-1852">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="cb73b-1853">Из параметров оценки уязвимостей удалены ограничения, касающиеся электронной почты.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1853">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb73b-1854">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb73b-1854">Az.Storage</span></span>
* <span data-ttu-id="cb73b-1855">Два параметра в указанном ниже командлете — -IndexDocument и -ErrorDocument404Path, — которые ранее были обязательными, стали необязательными:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1855">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="cb73b-1856">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="cb73b-1856">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="cb73b-1857">Обновлена справка по командлету Get-AzStorageBlobContent: добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1857">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="cb73b-1858">При сбое выполнения командлета с ошибкой StorageException отображаются дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1858">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="cb73b-1859">Добавлена поддержка создания или обновления учетной записи хранения с использованием проверки подлинности AAD DS для службы "Файлы Azure".</span><span class="sxs-lookup"><span data-stu-id="cb73b-1859">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="cb73b-1860">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb73b-1860">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="cb73b-1861">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb73b-1861">Set-AzStorageAccount</span></span>
* <span data-ttu-id="cb73b-1862">Добавлена поддержка перечисления или закрытия дескрипторов файлов для общей папки, каталога файлов или файла:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1862">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="cb73b-1863">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="cb73b-1863">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="cb73b-1864">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="cb73b-1864">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="cb73b-1865">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="cb73b-1865">Az.StorageSync</span></span>
* <span data-ttu-id="cb73b-1866">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1866">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="cb73b-1867">2.3.2 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1867">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb73b-1868">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb73b-1868">Az.Accounts</span></span>
* <span data-ttu-id="cb73b-1869">Исправлена ошибка, связанная с использованием неправильного URL-адреса для вызовов функций.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1869">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="cb73b-1870">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8983.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1870">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="cb73b-1871">Устранена проблема с псевдонимами из AzureRM для командлетов Az.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1871">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="cb73b-1872">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1872">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="cb73b-1873">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1873">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb73b-1874">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb73b-1874">Az.Compute</span></span>
* <span data-ttu-id="cb73b-1875">Простые наборы параметров New-AzVm и New-AzVmss теперь принимают параметр ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1875">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="cb73b-1876">Исправлена опечатка в справочной документации по New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1876">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="cb73b-1877">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="cb73b-1877">Az.Dns</span></span>
* <span data-ttu-id="cb73b-1878">Исправлена опечатка в справочных примерах по использованию Set-AzDnsZone.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1878">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="cb73b-1879">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="cb73b-1879">Az.EventGrid</span></span>
* <span data-ttu-id="cb73b-1880">Обновлен для использования API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1880">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="cb73b-1881">Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1881">New cmdlets:</span></span>
    - <span data-ttu-id="cb73b-1882">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="cb73b-1882">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="cb73b-1883">Создает домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1883">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="cb73b-1884">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="cb73b-1884">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="cb73b-1885">Возвращает сведения о домене Сетки событий или список всех доменов Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1885">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="cb73b-1886">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="cb73b-1886">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="cb73b-1887">Удаляет домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1887">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="cb73b-1888">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="cb73b-1888">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="cb73b-1889">Повторно создает ключ общего доступа для домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1889">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="cb73b-1890">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="cb73b-1890">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="cb73b-1891">Возвращает ключи общего доступа, используемые для публикации событий в домене Сетки событий.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1891">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="cb73b-1892">New-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="cb73b-1892">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="cb73b-1893">Создает раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1893">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="cb73b-1894">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="cb73b-1894">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="cb73b-1895">Возвращает сведения о разделе домена Сетки событий или список всех разделов определенного домена Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1895">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="cb73b-1896">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="cb73b-1896">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="cb73b-1897">Удаляет раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1897">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="cb73b-1898">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1898">Updated cmdlets:</span></span>
    - <span data-ttu-id="cb73b-1899">New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="cb73b-1899">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="cb73b-1900">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для нового домена Сетки событий и раздела домена Сетки событий и позволяющие создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1900">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="cb73b-1901">Добавляют новые обязательные параметры для указания имени нового домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1901">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="cb73b-1902">Добавляют новые наборы параметров для доменов и разделов домена и позволяют повторно использовать существующие параметры (например, EndPointType, SubjectBeginsWith и т. д.).</span><span class="sxs-lookup"><span data-stu-id="cb73b-1902">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="cb73b-1903">Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1903">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="cb73b-1904">срока действия подписки на событие;</span><span class="sxs-lookup"><span data-stu-id="cb73b-1904">Event subscription expiration date,</span></span>
            - <span data-ttu-id="cb73b-1905">параметров расширенной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1905">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="cb73b-1906">Добавляют новое перечисление для ServiceBusQueue в качестве места назначения.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1906">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="cb73b-1907">Запрещают использование значение All в параметре -IncludedEventType и заменяют его следующим:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1907">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="cb73b-1908">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="cb73b-1908">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="cb73b-1909">Добавляют новые необязательные параметры (Top, ODataQuery и NextLink) для поддержки разбиения на страницы и фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1909">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="cb73b-1910">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="cb73b-1910">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="cb73b-1911">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для домена Сетки событий и раздела домена Сетки событий и позволяющие удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1911">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="cb73b-1912">Добавляют новые обязательные параметры для указания имени домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1912">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cb73b-1913">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cb73b-1913">Az.FrontDoor</span></span>
* <span data-ttu-id="cb73b-1914">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="cb73b-1914">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="cb73b-1915">Добавляет поддержку преобразований и новое значение оператора автозавершения (RegEx).</span><span class="sxs-lookup"><span data-stu-id="cb73b-1915">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="cb73b-1916">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="cb73b-1916">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="cb73b-1917">Добавляет новые значения автозавершения.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1917">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb73b-1918">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb73b-1918">Az.Network</span></span>
* <span data-ttu-id="cb73b-1919">Добавляет поддержку ресурса шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1919">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="cb73b-1920">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="cb73b-1920">New cmdlets</span></span>
        - <span data-ttu-id="cb73b-1921">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="cb73b-1921">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="cb73b-1922">Добавляет AvailablePrivateEndpointType.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1922">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="cb73b-1923">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="cb73b-1923">New cmdlets</span></span>
        - <span data-ttu-id="cb73b-1924">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="cb73b-1924">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="cb73b-1925">Добавляет PrivatePrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1925">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="cb73b-1926">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="cb73b-1926">New cmdlets</span></span>
        - <span data-ttu-id="cb73b-1927">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="cb73b-1927">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="cb73b-1928">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="cb73b-1928">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="cb73b-1929">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="cb73b-1929">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="cb73b-1930">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="cb73b-1930">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="cb73b-1931">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cb73b-1931">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="cb73b-1932">Добавляет PrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1932">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="cb73b-1933">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="cb73b-1933">New cmdlets</span></span>
        - <span data-ttu-id="cb73b-1934">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="cb73b-1934">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="cb73b-1935">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="cb73b-1935">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="cb73b-1936">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="cb73b-1936">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="cb73b-1937">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="cb73b-1937">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="cb73b-1938">Обновлены следующие команды для функции: флаг UseLocalAzureIpAddress для VPN-подключения.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1938">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="cb73b-1939">Обновлен командлет New-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1939">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="cb73b-1940">Обновлен командлет Set-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1940">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="cb73b-1941">В пиринг ExpressRoute добавлено поле только для чтения PeeredConnections.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1941">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="cb73b-1942">В ExpressRoute добавлено поле только для чтения GlobalReachEnabled.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1942">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="cb73b-1943">Добавлен атрибут в рамках критического изменения, отменяющего статус устаревшего поля AllowGlobalReach в модели ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1943">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="cb73b-1944">Исправлена проблема, связанная с ошибкой 8756, при использовании TargetListenerID с командлетами AzApplicationGatewayRedirectConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1944">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="cb73b-1945">Исправлена ошибка в New-AzApplicationGatewayPathRuleConfig, не позволявшая задавать набор правил повторного создания.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1945">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="cb73b-1946">Исправлено отображение VirtualNetworkTaps в NetworkInterfaceIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1946">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="cb73b-1947">Исправлены командлеты Cortex Get для отображения всех частей.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1947">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="cb73b-1948">Исправлено создание ссылок VirtualHub для ExpressRouteGateways и VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1948">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="cb73b-1949">В AzureFirewall и NatGateway добавлена поддержка Зон доступности.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1949">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="cb73b-1950">Добавлен командлет Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1950">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="cb73b-1951">Добавлена поддержка нескольких общедоступных IP-адресов для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1951">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="cb73b-1952">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="cb73b-1952">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="cb73b-1953">Добавлен параметр -PublicIpAddress, который принимает один или несколько объектов общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1953">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="cb73b-1954">Добавлен параметр -VirtualNetwork, который принимает объект виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1954">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="cb73b-1955">Добавлены методы AddPublicIpAddress и RemovePublicIpAddress для объекта брандмауэра. Они принимают объект общедоступного IP-адреса в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1955">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="cb73b-1956">Не рекомендуется использовать параметры -PublicIpName и -VirtualNetworkName.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1956">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="cb73b-1957">Обновлены следующие команды для функции: В параметрах проверки подлинности AAD VPN-клиента задан ресурс шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1957">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="cb73b-1958">Обновлен командлет New-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1958">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="cb73b-1959">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1959">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="cb73b-1960">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр-переключатель RemoveAadAuthentication для удаления в шлюзе параметров проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1960">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cb73b-1961">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cb73b-1961">Az.OperationalInsights</span></span>
* <span data-ttu-id="cb73b-1962">Добавлена поддержка SKU **pergb2018** в команде New-AzureRmOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1962">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb73b-1963">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb73b-1963">Az.Resources</span></span>
* <span data-ttu-id="cb73b-1964">Поддержка дополнительных вариантов экспорта шаблона.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1964">Support for additional Template Export options</span></span>
    - <span data-ttu-id="cb73b-1965">В Export-AzResourceGroup добавлен параметр -SkipResourceNameParameterization.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1965">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="cb73b-1966">В Export-AzResourceGroup добавлен параметр -SkipAllParameterization.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1966">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="cb73b-1967">В Export-AzResourceGroup добавлен параметр -Resource для фильтрации экспортированных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1967">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cb73b-1968">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cb73b-1968">Az.ServiceFabric</span></span>
* <span data-ttu-id="cb73b-1969">Исправлена ошибка, связанная с получением иногда неправильных отпечатков при добавлении сертификата ByExistingKeyVault.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1969">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb73b-1970">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb73b-1970">Az.Sql</span></span>
* <span data-ttu-id="cb73b-1971">Исправлен суффикс конечной точки хранилища службы "Расширенная защита от угроз Azure".</span><span class="sxs-lookup"><span data-stu-id="cb73b-1971">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="cb73b-1972">Исправлена ошибка, связанная с возможностью пакета "Расширенная защита данных" переопределять политику службы "Расширенная защита от угроз".</span><span class="sxs-lookup"><span data-stu-id="cb73b-1972">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="cb73b-1973">Новые командлеты для Management.Sql позволяют клиентам добавлять ключи TDE и задавать средство защиты TDE для управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1973">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="cb73b-1974">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cb73b-1974">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="cb73b-1975">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cb73b-1975">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="cb73b-1976">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cb73b-1976">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="cb73b-1977">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="cb73b-1977">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="cb73b-1978">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="cb73b-1978">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb73b-1979">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb73b-1979">Az.Storage</span></span>
* <span data-ttu-id="cb73b-1980">Поддержка класса Kind в FileStorage и значения Premium_ZRS в SkuName при создании учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1980">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="cb73b-1981">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb73b-1981">New-AzStorageAccount</span></span>
* <span data-ttu-id="cb73b-1982">Уточнено описание командлета неизменности BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1982">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="cb73b-1983">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="cb73b-1983">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb73b-1984">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb73b-1984">Az.Websites</span></span>
* <span data-ttu-id="cb73b-1985">Оптимизирует Get-AzWebAppCertificate для фильтрации по группе ресурсов на сервере, а не в клиенте.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1985">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="cb73b-1986">Добавляет параметр-переключатель - UseDisasterRecovery в Get AzWebAppSnapshot.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1986">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="cb73b-1987">2.2.0 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1987">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="cb73b-1988">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cb73b-1988">Az.Cdn</span></span>
* <span data-ttu-id="cb73b-1989">Обновлены командлеты для поддержки функции rulesEngine на основе API версии 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1989">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb73b-1990">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb73b-1990">Az.Compute</span></span>
* <span data-ttu-id="cb73b-1991">Добавлен параметр `NoWait`, который запускает операцию и немедленно возвращает значение еще до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1991">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="cb73b-1992">Обновлены командлеты:   Export-AzLogAnalyticRequestRateByInterval; Export-AzLogAnalyticThrottledRequest; Remove-AzVM; Remove-AzVMAccessExtension; Remove-AzVMAEMExtension; Remove-AzVMChefExtension; Remove-AzVMCustomScriptExtension; Remove-AzVMDiagnosticsExtension; Remove-AzVMDiskEncryptionExtension; Remove-AzVMDscExtension; Remove-AzVMSqlServerExtension; Restart-AzVM; Set-AzVM; Set-AzVMAccessExtension; Set-AzVMADDomainExtension; Set-AzVMAEMExtension; Set-AzVMBginfoExtension; Set-AzVMChefExtension; Set-AzVMCustomScriptExtension; Set-AzVMDiagnosticsExtension; Set-AzVMDscExtension; Set-AzVMExtension; Start-AzVM; Stop-AzVM; Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1992">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cb73b-1993">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cb73b-1993">Az.EventHub</span></span>
* <span data-ttu-id="cb73b-1994">Исправлена ошибка № 9231. Командлет Get-AzEventHubNamespace не возвращал теги.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1994">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="cb73b-1995">Исправлена ошибка № 9230. Командлет Get-AzEventHubNamespace возвращал значение ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1995">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb73b-1996">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb73b-1996">Az.Network</span></span>
* <span data-ttu-id="cb73b-1997">Обновлены параметры ResourceId и InputObject для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1997">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="cb73b-1998">Добавлены псевдонимы для параметров ResourceId и InputObject.</span><span class="sxs-lookup"><span data-stu-id="cb73b-1998">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cb73b-1999">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cb73b-1999">Az.PolicyInsights</span></span>
* <span data-ttu-id="cb73b-2000">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyEvent.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2000">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb73b-2001">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-2001">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb73b-2002">Минимальный срок хранения политики IaaSVM изменился с 1 до 7 дней.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2002">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="cb73b-2003">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cb73b-2003">Az.ServiceBus</span></span>
* <span data-ttu-id="cb73b-2004">Исправлена ошибка № 9182. Командлет Get-AzServiceBusNamespace возвращал ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2004">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cb73b-2005">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cb73b-2005">Az.ServiceFabric</span></span>
* <span data-ttu-id="cb73b-2006">Исправлена опечатка в сообщении об ошибке для командлета Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2006">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="cb73b-2007">Добавлен отсутствующий символ в командных строках Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2007">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb73b-2008">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb73b-2008">Az.Sql</span></span>
* <span data-ttu-id="cb73b-2009">Для командлета New-AzureSqlInstance добавлен параметр DnsZonePartner, обеспечивающий поддержку AutoDr для Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2009">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="cb73b-2010">Командлет Get-AzSqlDatabaseSecureConnectionPolicy объявлен неподдерживаемым.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2010">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="cb73b-2011">Командлеты обнаружения угроз переименованы в командлеты Расширенной защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2011">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="cb73b-2012">Параметры -StorageSizeInGB и -LicenseType командлета New-AzSqlInstance теперь необязательны.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2012">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb73b-2013">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb73b-2013">Az.Websites</span></span>
* <span data-ttu-id="cb73b-2014">Исправлены проблемы, когда удалялись теги при использовании Set-AzWebApp и Set-AzWebAppSlot со свойством -WebApp.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2014">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="cb73b-2015">2.1.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2015">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="cb73b-2016">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb73b-2016">Az.ApiManagement</span></span>
* <span data-ttu-id="cb73b-2017">Созданы командлеты для управления диагностикой в глобальной области и в области API.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2017">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="cb73b-2018">**Get-AzApiManagementDiagnostic** — получение диагностики, заданной глобально или на уровне области API.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2018">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="cb73b-2019">**New-AzApiManagementDiagnostic** — создание диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2019">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="cb73b-2020">**New-AzApiManagementHttpMessageDiagnostic** — создание параметра диагностики, для которого регистрируются заголовки и размер байтов тела.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2020">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="cb73b-2021">**New-AzApiManagementPipelineDiagnosticSetting** — создание параметров диагностики для сообщений HTTP, поступающих в шлюз или исходящих из него.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2021">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="cb73b-2022">**New-AzApiManagementSamplingSetting** — создание параметра выборки для запросов и ответов касательно диагностики.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2022">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="cb73b-2023">**Remove-AzApiManagementDiagnostic** — удаление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2023">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="cb73b-2024">**Set-AzApiManagementDiagnostic** — обновление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2024">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="cb73b-2025">Созданы командлеты для управления кэшем в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2025">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="cb73b-2026">**Get-AzApiManagementCache** — получение сведений о кэше, указанном идентификатором, или обо всех кэшах.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2026">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="cb73b-2027">**New-AzApiManagementCache** — создание кэша по умолчанию или кэша в определенном регионе Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2027">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="cb73b-2028">**Remove-AzApiManagementCache** — удаление кэша.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2028">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="cb73b-2029">**Update-AzApiManagementCache** — обновление кэша.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2029">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="cb73b-2030">Созданы командлеты для управления схемой API.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2030">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="cb73b-2031">**New-AzApiManagementSchema** — создание схемы для API.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2031">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="cb73b-2032">**Get-AzApiManagementSchema** — получение схем, настроенных в API.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2032">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="cb73b-2033">**Remove-AzApiManagementSchema** — удаление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2033">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="cb73b-2034">**Set-AzApiManagementSchema** — обновление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2034">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="cb73b-2035">Создан командлет для создания токена пользователя.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2035">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="cb73b-2036">**New-AzApiManagementUserToken** — создание токена пользователя, по умолчанию действительного в течение 8 часов. С помощью этого командлета можно создавать токен для пользователя GIT.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2036">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="cb73b-2037">Создан командлет для получения состояния сети.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2037">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="cb73b-2038">**Get-AzApiManagementNetworkStatus** — получение состояния подключения сети ресурсов, от которых зависит служба "Управление API".</span><span class="sxs-lookup"><span data-stu-id="cb73b-2038">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="cb73b-2039">Это полезно при развертывании службы ApiManagement в виртуальной сети и проверке того, не нарушена ли какая-либо из зависимостей.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2039">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="cb73b-2040">Обновлен командлет **New-AzApiManagement** для управления службой ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2040">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="cb73b-2041">Добавлена поддержка нового SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2041">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="cb73b-2042">Добавлена поддержка для включения флага EnableClientCertificate в SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2042">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="cb73b-2043">Новый командлет **New-AzApiManagementSslSetting** позволяет настраивать параметр TLS/SSL для сервера (Backend) и внешнего интерфейса (Frontend).</span><span class="sxs-lookup"><span data-stu-id="cb73b-2043">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="cb73b-2044">Его также можно использовать для настройки Ciphers как 3DES, в ServerProtocols как Http2 для внешнего интерфейса (Frontend) службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2044">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="cb73b-2045">Добавлена поддержка настройки имени узла DeveloperPortal в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2045">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="cb73b-2046">Обновлен командлет **Get-AzApiManagementSsoToken** для извлечения объекта PsApiManagement в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2046">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="cb73b-2047">Обновлен командлет для отображения встроенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2047">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="cb73b-2048">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Код ошибки: ValidationError. Сообщение об ошибке: "Некоторые поля содержат неправильные значения". Сведения об ошибке: [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="cb73b-2048">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="cb73b-2049">Обновлен командлет **Export-AzApiManagementApi** для экспортирования программных интерфейсов в формате OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2049">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="cb73b-2050">Обновлен командлет **Import-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="cb73b-2050">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="cb73b-2051">Для импортирования API из спецификации документа OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2051">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="cb73b-2052">Для переопределения свойства PsApiManagementSchema, указанного в любом документе (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="cb73b-2052">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="cb73b-2053">Для переопределения свойства ServiceUrl, указанного в любом документе.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2053">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="cb73b-2054">Обновлен командлет **Get-AzApiManagementPolicy** для возврата политики в формате, экранированном не для XML, с использованием rawxml.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2054">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="cb73b-2055">Обновлен командлет **Set-AzApiManagementPolicy**. Он принимает политику в формате, экранированном не для XML, с использованием rawxml и в формате, экранированном для XML, с использованием XML.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2055">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="cb73b-2056">Обновлен командлет **New-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="cb73b-2056">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="cb73b-2057">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2057">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="cb73b-2058">Для создания API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2058">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="cb73b-2059">Для клонирования API с использованием значений SourceApiId и SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2059">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="cb73b-2060">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2060">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="cb73b-2061">Обновлен командлет **Set-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="cb73b-2061">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="cb73b-2062">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2062">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="cb73b-2063">Для обновления API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2063">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="cb73b-2064">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2064">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="cb73b-2065">Обновлен командлет **New-AzApiManagementRevision**:</span><span class="sxs-lookup"><span data-stu-id="cb73b-2065">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="cb73b-2066">Для клонирования (копирования тегов, продуктов, операций и политик) существующей редакции с использованием SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2066">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="cb73b-2067">Новая редакция предполагает родительский идентификатор ApiId.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2067">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="cb73b-2068">Для предоставления ApiRevisionDescription.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2068">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="cb73b-2069">Для переопределения значения ServiceUrl при клонировании API.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2069">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="cb73b-2070">Обновлен командлет **New-AzApiManagementIdentityProvider**:</span><span class="sxs-lookup"><span data-stu-id="cb73b-2070">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="cb73b-2071">Для настройки AAD или AADB2C с Authority.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2071">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="cb73b-2072">Для установки политик SignupPolicy, SigninPolicy, ProfileEditingPolicy и PasswordResetPolicy.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2072">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="cb73b-2073">Обновлен командлет **New-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2073">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="cb73b-2074">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2074">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="cb73b-2075">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2075">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="cb73b-2076">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2076">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="cb73b-2077">Обновлен командлет **Set-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2077">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="cb73b-2078">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2078">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="cb73b-2079">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2079">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="cb73b-2080">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2080">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="cb73b-2081">Следующие командлеты обновлены, чтобы принимать значение ResourceId в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2081">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="cb73b-2082">New-AzApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2082">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="cb73b-2083">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="cb73b-2083">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="cb73b-2084">Get-AzApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2084">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="cb73b-2085">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="cb73b-2085">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="cb73b-2086">Get-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2086">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="cb73b-2087">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="cb73b-2087">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="cb73b-2088">Get-AzApiManagementAuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2088">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="cb73b-2089">Get-AzApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2089">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="cb73b-2090">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="cb73b-2090">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="cb73b-2091">Get-AzApiManagementCertificate.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2091">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="cb73b-2092">Remove-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2092">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="cb73b-2093">Remove-AzApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2093">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb73b-2094">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb73b-2094">Az.Automation</span></span>
* <span data-ttu-id="cb73b-2095">Обновлен командлет Get-AzAutomationJobOutputRecord для обработки значений в формате JSON и в виде текстовой записи.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2095">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="cb73b-2096">исправлена проблема https://github.com/Azure/azure-powershell/issues/7977.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2096">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="cb73b-2097">исправлена проблема https://github.com/Azure/azure-powershell/issues/8600.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2097">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="cb73b-2098">Поведение командлета Start-AzAutomationDscCompilationJob изменено так, чтобы сразу же запустить задание, а не ждать его завершения.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2098">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="cb73b-2099">исправлена проблема https://github.com/Azure/azure-powershell/issues/8347.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2099">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="cb73b-2100">Исправлен командлет Get-AzAutomationDscNode, возвращающий все узлы при использовании -Name.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2100">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="cb73b-2101">Теперь он возвращает только соответствующий узел.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2101">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb73b-2102">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb73b-2102">Az.Compute</span></span>
* <span data-ttu-id="cb73b-2103">Добавлены параметры ProtectFromScaleIn и ProtectFromScaleSetAction для командлета Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2103">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="cb73b-2104">Командлет New-AzVM с простым набором параметров теперь по умолчанию использует доступное расположение, если регион "восточная часть США" не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2104">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb73b-2105">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb73b-2105">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb73b-2106">Обновлен пакет SDK ADLS для использования httpclient. В инфраструктуру Azure интегрирована проверка плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2106">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb73b-2107">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb73b-2107">Az.Monitor</span></span>
* <span data-ttu-id="cb73b-2108">Исправлены неправильные имена параметров в справочных примерах.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2108">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb73b-2109">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb73b-2109">Az.Network</span></span>
* <span data-ttu-id="cb73b-2110">Добавлен флаг DisableBgpRoutePropagation для выходных данных действующей таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2110">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="cb73b-2111">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="cb73b-2111">Updated cmdlet:</span></span>
        - <span data-ttu-id="cb73b-2112">Get-AzEffectiveRouteTable.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2112">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="cb73b-2113">Исправлен двойной дефис в документации New-AzApplicationGatewayTrustedRootCertificate.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2113">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb73b-2114">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb73b-2114">Az.Resources</span></span>
* <span data-ttu-id="cb73b-2115">Добавлен новый командлет Get-AzureRmDenyAssignment для получения запрещающих назначений.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2115">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb73b-2116">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb73b-2116">Az.Sql</span></span>
* <span data-ttu-id="cb73b-2117">Командлеты Расширенной защиты от угроз переименованы на командлеты Расширенной защиты данных, и оценка уязвимости включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2117">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="cb73b-2118">2.0.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2118">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb73b-2119">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb73b-2119">Az.Accounts</span></span>
* <span data-ttu-id="cb73b-2120">Обновлена библиотека аутентификации для устранения проблем с ADFS при использовании аутентификации на основе имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2120">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cb73b-2121">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-2121">Az.CognitiveServices</span></span>
* <span data-ttu-id="cb73b-2122">Отображается только заявление об отказе Bing для служб Поиска Bing.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2122">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="cb73b-2123">Исправлена проблема с созданием учетной записи.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2123">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb73b-2124">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb73b-2124">Az.Compute</span></span>
* <span data-ttu-id="cb73b-2125">Функция группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2125">Proximity placement group feature.</span></span>
    - <span data-ttu-id="cb73b-2126">Добавлены следующие новые командлеты:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="cb73b-2126">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="cb73b-2127">Новый параметр ProximityPlacementGroupId будет добавлен в следующие командлеты:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="cb73b-2127">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="cb73b-2128">В командлет New-AzGalleryImageVersion добавлен параметр StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2128">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="cb73b-2129">TargetRegion в командлете New-AzGalleryImageVersion может содержать StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2129">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="cb73b-2130">Параметр-переключатель SkipShutdown добавлен в командлеты Stop-AzVM и Stop-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2130">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="cb73b-2131">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="cb73b-2131">Breaking changes</span></span>
    - <span data-ttu-id="cb73b-2132">Командлет SET-AzVMBootDiagnostics изменен на Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2132">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="cb73b-2133">Командлет Export-AzLogAnalyticThrottledRequests изменен на Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2133">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="cb73b-2134">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="cb73b-2134">Az.DeploymentManager</span></span>
* <span data-ttu-id="cb73b-2135">Первая общедоступная версия командлетов диспетчера развертывания Azure</span><span class="sxs-lookup"><span data-stu-id="cb73b-2135">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="cb73b-2136">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="cb73b-2136">Az.Dns</span></span>
* <span data-ttu-id="cb73b-2137">Автоматическое делегирование DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="cb73b-2137">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="cb73b-2138">Командлет для создания зоны DNS принимает имя родительской зоны в качестве дополнительного необязательного параметра.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2138">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="cb73b-2139">Он добавляет записи NS в родительской зоне для созданной дочерней зоны.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2139">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cb73b-2140">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cb73b-2140">Az.FrontDoor</span></span>
* <span data-ttu-id="cb73b-2141">Первая общедоступная версия командлетов Azure FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2141">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="cb73b-2142">Переименованы командлеты WAF для включения Waf.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2142">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="cb73b-2143">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cb73b-2143">Az.HDInsight</span></span>
* <span data-ttu-id="cb73b-2144">Удалены два командлета:</span><span class="sxs-lookup"><span data-stu-id="cb73b-2144">Removed two cmdlets:</span></span>
    - <span data-ttu-id="cb73b-2145">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="cb73b-2145">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="cb73b-2146">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="cb73b-2146">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="cb73b-2147">Добавлен новый командлет Set-AzHDInsightGatewayCredential для замены Grant-AzHDInsightHttpServicesAccess.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2147">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="cb73b-2148">Обновлен командлет Get-AzHDInsightJobOutput для различения ролей читателя и оператора HDInsight:</span><span class="sxs-lookup"><span data-stu-id="cb73b-2148">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="cb73b-2149">Пользователям с ролью читателя не нужно указывать параметр DefaultStorageAccountKey явным образом, иначе возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2149">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="cb73b-2150">На пользователей с ролью оператора HDInsight это не повлияет.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2150">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb73b-2151">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb73b-2151">Az.Monitor</span></span>
* <span data-ttu-id="cb73b-2152">Новые командлеты для API SQR (запланированное правило запросов)</span><span class="sxs-lookup"><span data-stu-id="cb73b-2152">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="cb73b-2153">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="cb73b-2153">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="cb73b-2154">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="cb73b-2154">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="cb73b-2155">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="cb73b-2155">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="cb73b-2156">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="cb73b-2156">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="cb73b-2157">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="cb73b-2157">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="cb73b-2158">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="cb73b-2158">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="cb73b-2159">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cb73b-2159">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="cb73b-2160">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cb73b-2160">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="cb73b-2161">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cb73b-2161">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="cb73b-2162">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cb73b-2162">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="cb73b-2163">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cb73b-2163">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="cb73b-2164">См. подробнее об [API SQR](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules).</span><span class="sxs-lookup"><span data-stu-id="cb73b-2164">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="cb73b-2165">Обновлен файл Az.Monitor.md для включения командлетов для правила генерации оповещений на основе метрик GenV2(не классическая версия).</span><span class="sxs-lookup"><span data-stu-id="cb73b-2165">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb73b-2166">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb73b-2166">Az.Network</span></span>
* <span data-ttu-id="cb73b-2167">Добавлена поддержка для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2167">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="cb73b-2168">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="cb73b-2168">New cmdlets</span></span>
        - <span data-ttu-id="cb73b-2169">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="cb73b-2169">New-AzNatGateway</span></span>
        - <span data-ttu-id="cb73b-2170">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="cb73b-2170">Get-AzNatGateway</span></span>
        - <span data-ttu-id="cb73b-2171">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="cb73b-2171">Set-AzNatGateway</span></span>
        - <span data-ttu-id="cb73b-2172">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="cb73b-2172">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="cb73b-2173">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="cb73b-2173">Updated cmdlets</span></span>
        - <span data-ttu-id="cb73b-2174">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="cb73b-2174">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="cb73b-2175">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="cb73b-2175">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="cb73b-2176">Обновлены следующие команды для функции: Настройка и удаление пользовательских маршрутов через шлюз в Бруклине.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2176">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="cb73b-2177">Обновлен командлет New-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2177">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="cb73b-2178">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2178">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cb73b-2179">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cb73b-2179">Az.PolicyInsights</span></span>
* <span data-ttu-id="cb73b-2180">Добавлена поддержка сведений об оценке политики запросов.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2180">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="cb73b-2181">Добавлен параметр -Expand в командлет Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2181">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="cb73b-2182">Добавлена поддержка -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2182">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb73b-2183">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-2183">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb73b-2184">Добавлена поддержка перекрестной подписки на Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2184">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="cb73b-2185">Добавлена возможность отмечать предстоящие критически важные изменения для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2185">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="cb73b-2186">Исправлены план восстановления и план действий для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2186">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="cb73b-2187">Исправлено сетевое сопоставление обновления Azure Site Recovery (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="cb73b-2187">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="cb73b-2188">Исправлено направление защиты обновления Azure Site Recovery для управляемых дисков (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="cb73b-2188">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="cb73b-2189">Добавлены другие незначительные исправления.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2189">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="cb73b-2190">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="cb73b-2190">Az.Relay</span></span>
* <span data-ttu-id="cb73b-2191">Исправлены опечатки в сообщениях для клиентов.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2191">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="cb73b-2192">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cb73b-2192">Az.ServiceBus</span></span>
* <span data-ttu-id="cb73b-2193">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2193">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb73b-2194">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb73b-2194">Az.Storage</span></span>
* <span data-ttu-id="cb73b-2195">Выполнено обновление клиентской библиотеки хранилища до версии 10.0.1 (пространство имен всех объектов из этого пакета SDK изменено с Microsoft.WindowsAzure.Storage. *на Microsoft.Azure.Storage*).</span><span class="sxs-lookup"><span data-stu-id="cb73b-2195">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="cb73b-2196">Выполнено обновление до Microsoft.Azure.Management.Storage версии 11.0.0 для включения поддержки нового API версии 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2196">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="cb73b-2197">Значение свойства Kind по умолчанию в учетной записи хранения изменено со Storage на StorageV2.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2197">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="cb73b-2198">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb73b-2198">New-AzStorageAccount</span></span>
* <span data-ttu-id="cb73b-2199">Изменено значение Sku.Name в выходных данных командлета учетной записи хранения в соответствии со значением Sku.Name во входных данных путем добавления _ (например, StandardLRS изменено на Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="cb73b-2199">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="cb73b-2200">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb73b-2200">New-AzStorageAccount</span></span>
    - <span data-ttu-id="cb73b-2201">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb73b-2201">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="cb73b-2202">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb73b-2202">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb73b-2203">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb73b-2203">Az.Websites</span></span>
* <span data-ttu-id="cb73b-2204">Свойство Kind теперь будет задаваться объектам PSSite, возвращаемым командлетом Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2204">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="cb73b-2205">Get-AzWebApp\*Metrics и Get-AzAppServicePlanMetrics считаются нерекомендуемыми.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2205">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="cb73b-2206">1.8.0 — апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2206">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cb73b-2207">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="cb73b-2207">Highlights since the last major release</span></span>
* <span data-ttu-id="cb73b-2208">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2208">General availability of `Az` module</span></span>
* <span data-ttu-id="cb73b-2209">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="cb73b-2209">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="cb73b-2210">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="cb73b-2210">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="cb73b-2211">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2211">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="cb73b-2212">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2212">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="cb73b-2213">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2213">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="cb73b-2214">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="cb73b-2214">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cb73b-2215">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb73b-2215">Az.Accounts</span></span>
* <span data-ttu-id="cb73b-2216">Обновлен командлет Uninstall-AzureRm для правильного удаления модулей в Mac.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2216">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="cb73b-2217">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cb73b-2217">Az.Batch</span></span>
* <span data-ttu-id="cb73b-2218">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2218">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cb73b-2219">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cb73b-2219">Az.Cdn</span></span>
* <span data-ttu-id="cb73b-2220">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2220">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cb73b-2221">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-2221">Az.CognitiveServices</span></span>
* <span data-ttu-id="cb73b-2222">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2222">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb73b-2223">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb73b-2223">Az.Compute</span></span>
* <span data-ttu-id="cb73b-2224">Устранена проблема с установкой AEM, если в идентификаторах ресурсов дисков группа ресурсов указана в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2224">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="cb73b-2225">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2225">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cb73b-2226">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2226">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb73b-2227">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb73b-2227">Az.DataFactory</span></span>
* <span data-ttu-id="cb73b-2228">Добавлены свойства SsisProperties, если NodeCount не имеет значения NULL для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2228">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb73b-2229">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb73b-2229">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb73b-2230">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2230">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="cb73b-2231">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="cb73b-2231">Az.EventGrid</span></span>
* <span data-ttu-id="cb73b-2232">Обновлен текст справки для конечной точки, указывающий, что необходимо создать ресурсы, прежде чем использовать командлеты для создания или обновления подписки на события.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2232">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cb73b-2233">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cb73b-2233">Az.EventHub</span></span>
* <span data-ttu-id="cb73b-2234">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2234">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cb73b-2235">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cb73b-2235">Az.HDInsight</span></span>
* <span data-ttu-id="cb73b-2236">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2236">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cb73b-2237">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cb73b-2237">Az.IotHub</span></span>
* <span data-ttu-id="cb73b-2238">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2238">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cb73b-2239">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb73b-2239">Az.KeyVault</span></span>
* <span data-ttu-id="cb73b-2240">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2240">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cb73b-2241">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2241">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="cb73b-2242">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="cb73b-2242">Az.MachineLearning</span></span>
* <span data-ttu-id="cb73b-2243">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2243">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="cb73b-2244">Az.Media</span><span class="sxs-lookup"><span data-stu-id="cb73b-2244">Az.Media</span></span>
* <span data-ttu-id="cb73b-2245">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2245">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb73b-2246">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb73b-2246">Az.Monitor</span></span>
  * <span data-ttu-id="cb73b-2247">Добавлены новые командлеты для правила генерации оповещений на основе метрик GenV2 (не классических).</span><span class="sxs-lookup"><span data-stu-id="cb73b-2247">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="cb73b-2248">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="cb73b-2248">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="cb73b-2249">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="cb73b-2249">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="cb73b-2250">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="cb73b-2250">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="cb73b-2251">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="cb73b-2251">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="cb73b-2252">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="cb73b-2252">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="cb73b-2253">Обновлен пакет SDK Monitor до предварительной версии 0.22.0.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2253">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb73b-2254">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb73b-2254">Az.Network</span></span>
* <span data-ttu-id="cb73b-2255">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2255">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cb73b-2256">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2256">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="cb73b-2257">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="cb73b-2257">Az.NotificationHubs</span></span>
* <span data-ttu-id="cb73b-2258">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2258">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cb73b-2259">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cb73b-2259">Az.OperationalInsights</span></span>
* <span data-ttu-id="cb73b-2260">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2260">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="cb73b-2261">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="cb73b-2261">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="cb73b-2262">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2262">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb73b-2263">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-2263">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb73b-2264">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2264">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cb73b-2265">Обновлен табличный формат для SQL на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2265">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="cb73b-2266">Добавлен альтернативный метод для получения расположения в Общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2266">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="cb73b-2267">Обновлено значение ScheduleRunDays в объекте SchedulePolicy в соответствии с часовым поясом.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2267">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="cb73b-2268">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="cb73b-2268">Az.RedisCache</span></span>
* <span data-ttu-id="cb73b-2269">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2269">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb73b-2270">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb73b-2270">Az.Resources</span></span>
* <span data-ttu-id="cb73b-2271">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2271">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb73b-2272">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb73b-2272">Az.Sql</span></span>
* <span data-ttu-id="cb73b-2273">Заменена зависимость от пакета SDK монитора на обычный код.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2273">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="cb73b-2274">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2274">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cb73b-2275">Улучшен процесс классификации нескольких столбцов.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2275">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="cb73b-2276">Добавлены свойства SKU (имя, семейство, производительность SKU) в отклике Get-AzSqlServerServiceObjective, а также по умолчанию задан табличный формат.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2276">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="cb73b-2277">C помощью Get-AzSqlServerServiceObjective теперь можно получать список доступных целевых служб по расположению без необходимости заранее размещать сервер в регионе.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2277">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="cb73b-2278">Поддерживается параметр часового пояса при создании Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2278">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="cb73b-2279">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2279">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb73b-2280">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb73b-2280">Az.Websites</span></span>
* <span data-ttu-id="cb73b-2281">Исправлены командлеты Set-AzWebApp и Set-AzWebAppSlot, которые теперь не удаляют теги при выполнении.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2281">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="cb73b-2282">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2282">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cb73b-2283">Обновлен пакет SDK веб-узлов.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2283">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="cb73b-2284">Удалено свойство AdminSiteName из PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2284">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="cb73b-2285">1.7.0 —апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2285">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cb73b-2286">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="cb73b-2286">Highlights since the last major release</span></span>
* <span data-ttu-id="cb73b-2287">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2287">General availability of `Az` module</span></span>
* <span data-ttu-id="cb73b-2288">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="cb73b-2288">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="cb73b-2289">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="cb73b-2289">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="cb73b-2290">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2290">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="cb73b-2291">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2291">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="cb73b-2292">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2292">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="cb73b-2293">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="cb73b-2293">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cb73b-2294">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb73b-2294">Az.Accounts</span></span>
* <span data-ttu-id="cb73b-2295">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметр AzureAnalysisServicesEndpointResourceId.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2295">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="cb73b-2296">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-2296">Az.AnalysisServices</span></span>
* <span data-ttu-id="cb73b-2297">Использование ServiceClient в командлетах плоскости данных и удаление исходной логики проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2297">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="cb73b-2298">Add-AzureASAccount используется как оболочка для Connect-AzAccount во избежание критических изменений.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2298">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb73b-2299">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb73b-2299">Az.Automation</span></span>
* <span data-ttu-id="cb73b-2300">Исправлена ошибка командлета New-AzAutomationSoftwareUpdateConfiguration, связанная с включением.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2300">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="cb73b-2301">Теперь параметры IncludedKbNumber и IncludedPackageNameMask должны работать нормально.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2301">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="cb73b-2302">Исправлена ошибка динамической группы управления обновлениями службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2302">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb73b-2303">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb73b-2303">Az.Compute</span></span>
* <span data-ttu-id="cb73b-2304">В командлеты New-AzDiskConfig и New-AzSnapshotConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2304">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="cb73b-2305">Теперь можно создавать виртуальные машину на основе образов из коллекции от других клиентов.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2305">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="cb73b-2306">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="cb73b-2306">Az.ContainerInstance</span></span>
* <span data-ttu-id="cb73b-2307">Исправлена проблема в параметре -Command командлета New-AzContainerGroup, из-за которой в конце добавлялся пустой аргумент.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2307">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb73b-2308">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb73b-2308">Az.DataFactory</span></span>
* <span data-ttu-id="cb73b-2309">Пакет SDK для ADF .NET обновлен до версии 3.0.2.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2309">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="cb73b-2310">Командлет Set-AzDataFactoryV2 обновлен с помощью дополнительных параметров для настроек, связанных с RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2310">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb73b-2311">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb73b-2311">Az.Resources</span></span>
* <span data-ttu-id="cb73b-2312">Улучшена обработка поставщиков Get-AzResource при предоставлении параметров -ResourceId или -ResourceGroupName, -Name и -ResourceType.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2312">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="cb73b-2313">Улучшена обработка ошибок в командлетах Test-AzDeployment и Test-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2313">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="cb73b-2314">Теперь ошибки, возникающие за пределами проверки развертывания, обрабатываются и включаются в выходные данные команды.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2314">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="cb73b-2315">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2315">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="cb73b-2316">Добавлен параметр-переключатель -IgnoreDynamicParameters, с помощью которого можно настроить командлеты развертывания так, чтобы они пропускали запросы в сценариях скриптов и заданий.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2316">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="cb73b-2317">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2317">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb73b-2318">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb73b-2318">Az.Sql</span></span>
* <span data-ttu-id="cb73b-2319">Поддержка классификации данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2319">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb73b-2320">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb73b-2320">Az.Storage</span></span>
* <span data-ttu-id="cb73b-2321">Подробные сообщения об ошибке передаются при создании контекста хранилища с помощью параметра -UseConnectedAccount, но без входа в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2321">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="cb73b-2322">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="cb73b-2322">New-AzStorageContext</span></span>
* <span data-ttu-id="cb73b-2323">Поддержка свойств службы управления BLOB-объектов в указанной учетной записи хранения с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2323">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="cb73b-2324">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="cb73b-2324">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="cb73b-2325">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="cb73b-2325">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="cb73b-2326">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cb73b-2326">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="cb73b-2327">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cb73b-2327">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="cb73b-2328">Поддержка параметра -AsJob в командлетах для отправки и скачивания больших двоичных объектов и файлов.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2328">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="cb73b-2329">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cb73b-2329">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="cb73b-2330">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cb73b-2330">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="cb73b-2331">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="cb73b-2331">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="cb73b-2332">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="cb73b-2332">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="cb73b-2333">1.6.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2333">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cb73b-2334">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="cb73b-2334">Highlights since the last major release</span></span>
* <span data-ttu-id="cb73b-2335">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2335">General availability of `Az` module</span></span>
* <span data-ttu-id="cb73b-2336">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="cb73b-2336">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="cb73b-2337">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="cb73b-2337">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="cb73b-2338">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2338">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="cb73b-2339">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2339">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="cb73b-2340">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2340">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="cb73b-2341">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="cb73b-2341">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb73b-2342">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb73b-2342">Az.Automation</span></span>
* <span data-ttu-id="cb73b-2343">В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:</span><span class="sxs-lookup"><span data-stu-id="cb73b-2343">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="cb73b-2344">динамическое группирование;</span><span class="sxs-lookup"><span data-stu-id="cb73b-2344">Dynamic grouping</span></span>
    * <span data-ttu-id="cb73b-2345">скрипты предварительного или последующего выполнения;</span><span class="sxs-lookup"><span data-stu-id="cb73b-2345">Pre-Post script</span></span>
    * <span data-ttu-id="cb73b-2346">параметр перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2346">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb73b-2347">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb73b-2347">Az.Compute</span></span>
* <span data-ttu-id="cb73b-2348">Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2348">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="cb73b-2349">Обновление клиентской библиотеки вычислений до версии 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2349">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cb73b-2350">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb73b-2350">Az.KeyVault</span></span>
* <span data-ttu-id="cb73b-2351">Добавлена поддержка подстановочных знаков в командлетах KeyVault.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2351">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb73b-2352">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb73b-2352">Az.Network</span></span>
* <span data-ttu-id="cb73b-2353">Добавлена поддержка анализа угроз для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2353">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="cb73b-2354">Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2354">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb73b-2355">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-2355">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb73b-2356">В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2356">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="cb73b-2357">Добавлена поддержка канала для отмены регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2357">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb73b-2358">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb73b-2358">Az.Resources</span></span>
* <span data-ttu-id="cb73b-2359">Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2359">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="cb73b-2360">Обновлены учетные данные, используемые при общих вызовах к ARM.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2360">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb73b-2361">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb73b-2361">Az.Sql</span></span>
* <span data-ttu-id="cb73b-2362">Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2362">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb73b-2363">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb73b-2363">Az.Storage</span></span>
* <span data-ttu-id="cb73b-2364">Поддержка получения, настройки и удаления политики управления в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2364">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="cb73b-2365">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="cb73b-2365">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="cb73b-2366">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="cb73b-2366">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="cb73b-2367">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="cb73b-2367">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="cb73b-2368">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="cb73b-2368">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="cb73b-2369">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="cb73b-2369">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="cb73b-2370">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="cb73b-2370">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb73b-2371">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb73b-2371">Az.Websites</span></span>
* <span data-ttu-id="cb73b-2372">Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2372">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="cb73b-2373">1.5.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2373">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb73b-2374">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb73b-2374">Az.Accounts</span></span>
* <span data-ttu-id="cb73b-2375">Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2375">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="cb73b-2376">Обновлены примеры для Connect AzAccount.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2376">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb73b-2377">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb73b-2377">Az.Automation</span></span>
* <span data-ttu-id="cb73b-2378">Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2378">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="cb73b-2379">Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2379">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="cb73b-2380">Теперь он возвращает все узлы.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2380">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cb73b-2381">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cb73b-2381">Az.Cdn</span></span>
* <span data-ttu-id="cb73b-2382">Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2382">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb73b-2383">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb73b-2383">Az.Compute</span></span>
* <span data-ttu-id="cb73b-2384">Добавлена поддержка подстановочных знаков в командлетах Get.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2384">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb73b-2385">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb73b-2385">Az.DataFactory</span></span>
* <span data-ttu-id="cb73b-2386">Обновлен пакет SDK для ADF .NET до версии 3.0.1.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2386">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="cb73b-2387">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="cb73b-2387">Az.LogicApp</span></span>
* <span data-ttu-id="cb73b-2388">Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2388">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb73b-2389">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb73b-2389">Az.Network</span></span>
* <span data-ttu-id="cb73b-2390">Добавлена поддержка подстановочных знаков в командлетах Network.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2390">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb73b-2391">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-2391">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb73b-2392">Добавлена поддержка SQL Server на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2392">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="cb73b-2393">Обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="cb73b-2393">SDK Update</span></span>
* <span data-ttu-id="cb73b-2394">Удалена проверка VMappContainer в Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2394">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="cb73b-2395">Добавлены параметры Name и ServerName для Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2395">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb73b-2396">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb73b-2396">Az.Resources</span></span>
* <span data-ttu-id="cb73b-2397">Добавлен параметр `-TemplateObject` в командлеты для развертывания.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2397">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="cb73b-2398">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2398">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="cb73b-2399">Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2399">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="cb73b-2400">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2400">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="cb73b-2401">Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2401">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="cb73b-2402">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2402">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb73b-2403">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb73b-2403">Az.Sql</span></span>
* <span data-ttu-id="cb73b-2404">Обновление AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2404">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="cb73b-2405">Исправлено поведение для пограничного случая при создании параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2405">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb73b-2406">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb73b-2406">Az.Storage</span></span>
* <span data-ttu-id="cb73b-2407">Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2407">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="cb73b-2408">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2408">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="cb73b-2409">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-2409">Az.AnalysisServices</span></span>
* <span data-ttu-id="cb73b-2410">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2410">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb73b-2411">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb73b-2411">Az.Automation</span></span>
* <span data-ttu-id="cb73b-2412">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2412">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="cb73b-2413">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2413">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="cb73b-2414">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2414">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cb73b-2415">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-2415">Az.CognitiveServices</span></span>
* <span data-ttu-id="cb73b-2416">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2416">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb73b-2417">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb73b-2417">Az.Compute</span></span>
* <span data-ttu-id="cb73b-2418">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2418">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="cb73b-2419">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2419">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="cb73b-2420">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2420">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="cb73b-2421">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2421">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb73b-2422">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb73b-2422">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb73b-2423">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2423">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cb73b-2424">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cb73b-2424">Az.EventHub</span></span>
* <span data-ttu-id="cb73b-2425">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2425">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cb73b-2426">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb73b-2426">Az.KeyVault</span></span>
* <span data-ttu-id="cb73b-2427">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2427">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="cb73b-2428">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="cb73b-2428">Az.LogicApp</span></span>
* <span data-ttu-id="cb73b-2429">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2429">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="cb73b-2430">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2430">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="cb73b-2431">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="cb73b-2431">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="cb73b-2432">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="cb73b-2432">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="cb73b-2433">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="cb73b-2433">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="cb73b-2434">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="cb73b-2434">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="cb73b-2435">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2435">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="cb73b-2436">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="cb73b-2436">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="cb73b-2437">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="cb73b-2437">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="cb73b-2438">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="cb73b-2438">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="cb73b-2439">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="cb73b-2439">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="cb73b-2440">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2440">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="cb73b-2441">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2441">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb73b-2442">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb73b-2442">Az.Monitor</span></span>
* <span data-ttu-id="cb73b-2443">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2443">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb73b-2444">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb73b-2444">Az.Network</span></span>
* <span data-ttu-id="cb73b-2445">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2445">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cb73b-2446">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cb73b-2446">Az.OperationalInsights</span></span>
* <span data-ttu-id="cb73b-2447">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2447">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="cb73b-2448">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2448">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="cb73b-2449">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2449">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb73b-2450">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb73b-2450">Az.Resources</span></span>
* <span data-ttu-id="cb73b-2451">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2451">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="cb73b-2452">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2452">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="cb73b-2453">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2453">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="cb73b-2454">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2454">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb73b-2455">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb73b-2455">Az.Sql</span></span>
* <span data-ttu-id="cb73b-2456">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2456">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="cb73b-2457">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2457">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb73b-2458">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb73b-2458">Az.Websites</span></span>
* <span data-ttu-id="cb73b-2459">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2459">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="cb73b-2460">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2460">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb73b-2461">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb73b-2461">Az.Accounts</span></span>
* <span data-ttu-id="cb73b-2462">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="cb73b-2462">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="cb73b-2463">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-2463">Az.AnalysisServices</span></span>
<span data-ttu-id="cb73b-2464">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2464">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb73b-2465">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb73b-2465">Az.Compute</span></span>
* <span data-ttu-id="cb73b-2466">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2466">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="cb73b-2467">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2467">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="cb73b-2468">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2468">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb73b-2469">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-2469">Az.RecoveryServices</span></span>
<span data-ttu-id="cb73b-2470">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2470">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb73b-2471">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb73b-2471">Az.Resources</span></span>
* <span data-ttu-id="cb73b-2472">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2472">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="cb73b-2473">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2473">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="cb73b-2474">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2474">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="cb73b-2475">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2475">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb73b-2476">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb73b-2476">Az.Sql</span></span>
* <span data-ttu-id="cb73b-2477">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2477">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="cb73b-2478">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2478">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="cb73b-2479">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2479">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="cb73b-2480">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2480">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb73b-2481">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb73b-2481">Az.Accounts</span></span>
* <span data-ttu-id="cb73b-2482">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2482">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="cb73b-2483">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-2483">Az.AnalysisServices</span></span>
* <span data-ttu-id="cb73b-2484">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2484">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb73b-2485">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-2485">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb73b-2486">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2486">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="cb73b-2487">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2487">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb73b-2488">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb73b-2488">Az.Accounts</span></span>
* <span data-ttu-id="cb73b-2489">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2489">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="cb73b-2490">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2490">Update incorrect online help URLs</span></span>
* <span data-ttu-id="cb73b-2491">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2491">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="cb73b-2492">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cb73b-2492">Az.Aks</span></span>
* <span data-ttu-id="cb73b-2493">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2493">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb73b-2494">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb73b-2494">Az.Automation</span></span>
* <span data-ttu-id="cb73b-2495">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2495">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="cb73b-2496">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2496">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cb73b-2497">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cb73b-2497">Az.Cdn</span></span>
* <span data-ttu-id="cb73b-2498">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2498">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb73b-2499">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb73b-2499">Az.Compute</span></span>
* <span data-ttu-id="cb73b-2500">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2500">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="cb73b-2501">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2501">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="cb73b-2502">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2502">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="cb73b-2503">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="cb73b-2503">Az.ContainerRegistry</span></span>
* <span data-ttu-id="cb73b-2504">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2504">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb73b-2505">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb73b-2505">Az.DataFactory</span></span>
* <span data-ttu-id="cb73b-2506">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2506">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb73b-2507">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb73b-2507">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb73b-2508">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2508">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="cb73b-2509">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2509">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="cb73b-2510">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2510">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cb73b-2511">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cb73b-2511">Az.IotHub</span></span>
* <span data-ttu-id="cb73b-2512">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2512">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cb73b-2513">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb73b-2513">Az.KeyVault</span></span>
* <span data-ttu-id="cb73b-2514">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2514">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb73b-2515">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb73b-2515">Az.Network</span></span>
* <span data-ttu-id="cb73b-2516">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2516">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb73b-2517">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb73b-2517">Az.Resources</span></span>
* <span data-ttu-id="cb73b-2518">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2518">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="cb73b-2519">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2519">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="cb73b-2520">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2520">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="cb73b-2521">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2521">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="cb73b-2522">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2522">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="cb73b-2523">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2523">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="cb73b-2524">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2524">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cb73b-2525">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cb73b-2525">Az.ServiceFabric</span></span>
* <span data-ttu-id="cb73b-2526">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2526">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="cb73b-2527">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2527">Fix some error messages.</span></span>
* <span data-ttu-id="cb73b-2528">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2528">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="cb73b-2529">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2529">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="cb73b-2530">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="cb73b-2530">Az.SignalR</span></span>
* <span data-ttu-id="cb73b-2531">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2531">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb73b-2532">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb73b-2532">Az.Sql</span></span>
* <span data-ttu-id="cb73b-2533">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2533">Update incorrect online help URLs</span></span>
* <span data-ttu-id="cb73b-2534">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2534">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="cb73b-2535">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2535">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="cb73b-2536">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2536">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb73b-2537">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb73b-2537">Az.Storage</span></span>
* <span data-ttu-id="cb73b-2538">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2538">Update incorrect online help URLs</span></span>
* <span data-ttu-id="cb73b-2539">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2539">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="cb73b-2540">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="cb73b-2540">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="cb73b-2541">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="cb73b-2541">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="cb73b-2542">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="cb73b-2542">Az.TrafficManager</span></span>
* <span data-ttu-id="cb73b-2543">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2543">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb73b-2544">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb73b-2544">Az.Websites</span></span>
* <span data-ttu-id="cb73b-2545">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2545">Update incorrect online help URLs</span></span>
* <span data-ttu-id="cb73b-2546">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2546">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="cb73b-2547">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2547">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="cb73b-2548">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2548">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb73b-2549">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb73b-2549">Az.Accounts</span></span>
* <span data-ttu-id="cb73b-2550">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2550">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb73b-2551">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb73b-2551">Az.Compute</span></span>
* <span data-ttu-id="cb73b-2552">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2552">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="cb73b-2553">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2553">Updated the description of ID in help files</span></span>
* <span data-ttu-id="cb73b-2554">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2554">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb73b-2555">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb73b-2555">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb73b-2556">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2556">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="cb73b-2557">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2557">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="cb73b-2558">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="cb73b-2558">Az.EventGrid</span></span>
* <span data-ttu-id="cb73b-2559">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2559">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="cb73b-2560">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2560">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="cb73b-2561">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="cb73b-2561">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="cb73b-2562">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="cb73b-2562">Event Time-To-Live,</span></span>
        - <span data-ttu-id="cb73b-2563">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="cb73b-2563">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="cb73b-2564">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2564">Dead letter endpoint.</span></span>
    - <span data-ttu-id="cb73b-2565">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="cb73b-2565">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="cb73b-2566">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="cb73b-2566">Event Time-To-Live,</span></span>
        - <span data-ttu-id="cb73b-2567">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="cb73b-2567">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="cb73b-2568">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2568">Dead letter endpoint.</span></span>
* <span data-ttu-id="cb73b-2569">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2569">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="cb73b-2570">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2570">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cb73b-2571">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cb73b-2571">Az.IotHub</span></span>
* <span data-ttu-id="cb73b-2572">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2572">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="cb73b-2573">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="cb73b-2573">Az.LogicApp</span></span>
* <span data-ttu-id="cb73b-2574">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2574">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb73b-2575">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb73b-2575">Az.Resources</span></span>
* <span data-ttu-id="cb73b-2576">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="cb73b-2576">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="cb73b-2577">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2577">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="cb73b-2578">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2578">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="cb73b-2579">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2579">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="cb73b-2580">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="cb73b-2580">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="cb73b-2581">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2581">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="cb73b-2582">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="cb73b-2582">Az.SignalR</span></span>
* <span data-ttu-id="cb73b-2583">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2583">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb73b-2584">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb73b-2584">Az.Sql</span></span>
* <span data-ttu-id="cb73b-2585">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2585">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb73b-2586">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb73b-2586">Az.Storage</span></span>
* <span data-ttu-id="cb73b-2587">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2587">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="cb73b-2588">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="cb73b-2588">New-AzStorageContext</span></span>
* <span data-ttu-id="cb73b-2589">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2589">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="cb73b-2590">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="cb73b-2590">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb73b-2591">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb73b-2591">Az.Websites</span></span>
* <span data-ttu-id="cb73b-2592">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="cb73b-2592">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="cb73b-2593">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2593">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="cb73b-2594">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2594">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="cb73b-2595">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="cb73b-2595">General</span></span>

- <span data-ttu-id="cb73b-2596">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2596">General Availability of Az Module</span></span>
- <span data-ttu-id="cb73b-2597">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2597">Online help for each module</span></span>
- <span data-ttu-id="cb73b-2598">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="cb73b-2598">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="cb73b-2599">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="cb73b-2599">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="cb73b-2600">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb73b-2600">Az.Accounts</span></span>
- <span data-ttu-id="cb73b-2601">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2601">Changed from Az.Profile</span></span>
- <span data-ttu-id="cb73b-2602">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2602">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="cb73b-2603">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb73b-2603">Az.ApiManagement</span></span>
- <span data-ttu-id="cb73b-2604">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2604">Fixes for #7002</span></span>
- <span data-ttu-id="cb73b-2605">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="cb73b-2605">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="cb73b-2606">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cb73b-2606">Az.Batch</span></span>
- <span data-ttu-id="cb73b-2607">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2607">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="cb73b-2608">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2608">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="cb73b-2609">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="cb73b-2609">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="cb73b-2610">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="cb73b-2610">Az.Billing</span></span>
- <span data-ttu-id="cb73b-2611">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="cb73b-2611">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="cb73b-2612">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-2612">Az.CognitivServices</span></span>
- <span data-ttu-id="cb73b-2613">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2613">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="cb73b-2614">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2614">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="cb73b-2615">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="cb73b-2615">Az.ContainerInstance</span></span>
- <span data-ttu-id="cb73b-2616">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2616">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="cb73b-2617">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="cb73b-2617">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="cb73b-2618">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="cb73b-2618">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="cb73b-2619">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb73b-2619">Az.DataLakeStore</span></span>
- <span data-ttu-id="cb73b-2620">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="cb73b-2620">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="cb73b-2621">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb73b-2621">Az.Monitor</span></span>
- <span data-ttu-id="cb73b-2622">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="cb73b-2622">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="cb73b-2623">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb73b-2623">Az.KeyVault</span></span>
- <span data-ttu-id="cb73b-2624">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="cb73b-2624">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="cb73b-2625">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="cb73b-2625">Az.MachineLearning</span></span>
- <span data-ttu-id="cb73b-2626">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="cb73b-2626">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="cb73b-2627">Az.Media</span><span class="sxs-lookup"><span data-stu-id="cb73b-2627">Az.Media</span></span>
- <span data-ttu-id="cb73b-2628">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="cb73b-2628">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="cb73b-2629">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb73b-2629">Az.Network</span></span>
<span data-ttu-id="cb73b-2630">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="cb73b-2630">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="cb73b-2631">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="cb73b-2631">New cmdlets added:</span></span>
        - <span data-ttu-id="cb73b-2632">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb73b-2632">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cb73b-2633">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb73b-2633">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cb73b-2634">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb73b-2634">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cb73b-2635">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb73b-2635">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cb73b-2636">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb73b-2636">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cb73b-2637">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="cb73b-2637">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="cb73b-2638">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="cb73b-2638">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="cb73b-2639">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb73b-2639">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="cb73b-2640">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb73b-2640">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="cb73b-2641">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb73b-2641">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="cb73b-2642">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="cb73b-2642">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="cb73b-2643">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="cb73b-2643">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="cb73b-2644">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cb73b-2644">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="cb73b-2645">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="cb73b-2645">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="cb73b-2646">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2646">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="cb73b-2647">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="cb73b-2647">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="cb73b-2648">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cb73b-2648">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="cb73b-2649">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cb73b-2649">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="cb73b-2650">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cb73b-2650">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="cb73b-2651">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="cb73b-2651">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="cb73b-2652">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="cb73b-2652">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="cb73b-2653">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cb73b-2653">Az.OperationalInsights</span></span>
- <span data-ttu-id="cb73b-2654">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="cb73b-2654">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="cb73b-2655">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="cb73b-2655">Az.Profile</span></span>
- <span data-ttu-id="cb73b-2656">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2656">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="cb73b-2657">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-2657">Az.RecoveryServices</span></span>
- <span data-ttu-id="cb73b-2658">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="cb73b-2658">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="cb73b-2659">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb73b-2659">Az.Resources</span></span>
- <span data-ttu-id="cb73b-2660">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="cb73b-2660">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="cb73b-2661">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cb73b-2661">Az.ServiceFabric</span></span>
- <span data-ttu-id="cb73b-2662">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="cb73b-2662">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="cb73b-2663">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="cb73b-2663">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="cb73b-2664">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="cb73b-2664">Az.SIgnalR</span></span>
- <span data-ttu-id="cb73b-2665">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="cb73b-2665">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="cb73b-2666">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb73b-2666">Az.Sql</span></span>
- <span data-ttu-id="cb73b-2667">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="cb73b-2667">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="cb73b-2668">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="cb73b-2668">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="cb73b-2669">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="cb73b-2669">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="cb73b-2670">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb73b-2670">Az.Storage</span></span>
- <span data-ttu-id="cb73b-2671">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="cb73b-2671">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="cb73b-2672">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb73b-2672">Az.Websites</span></span>
- <span data-ttu-id="cb73b-2673">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="cb73b-2673">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="cb73b-2674">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2674">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="cb73b-2675">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="cb73b-2675">General</span></span>

* <span data-ttu-id="cb73b-2676">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="cb73b-2676">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="cb73b-2677">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb73b-2677">Az.Compute</span></span>

* <span data-ttu-id="cb73b-2678">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2678">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="cb73b-2679">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb73b-2679">Az.DataLakeStore</span></span>

* <span data-ttu-id="cb73b-2680">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="cb73b-2680">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="cb73b-2681">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cb73b-2681">Az.FrontDoor</span></span>

* <span data-ttu-id="cb73b-2682">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="cb73b-2682">Fixed some broken links</span></span>
    - <span data-ttu-id="cb73b-2683">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2683">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="cb73b-2684">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2684">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="cb73b-2685">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-2685">Az.RecoveryServices</span></span>

* <span data-ttu-id="cb73b-2686">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2686">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="cb73b-2687">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2687">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="cb73b-2688">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb73b-2688">Az.Resources</span></span>

* <span data-ttu-id="cb73b-2689">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2689">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="cb73b-2690">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2690">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="cb73b-2691">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb73b-2691">Az.Sql</span></span>

* <span data-ttu-id="cb73b-2692">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="cb73b-2692">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="cb73b-2693">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2693">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="cb73b-2694">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2694">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="cb73b-2695">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb73b-2695">Az.Storage</span></span>

* <span data-ttu-id="cb73b-2696">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb73b-2696">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="cb73b-2697">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="cb73b-2697">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="cb73b-2698">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="cb73b-2698">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="cb73b-2699">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="cb73b-2699">Support Static Website configuration</span></span>
    - <span data-ttu-id="cb73b-2700">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="cb73b-2700">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="cb73b-2701">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="cb73b-2701">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="cb73b-2702">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb73b-2702">Az.Websites</span></span>

* <span data-ttu-id="cb73b-2703">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cb73b-2703">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="cb73b-2704">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2704">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="cb73b-2705">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2705">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="cb73b-2706">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2706">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="cb73b-2707">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb73b-2707">Az.ApiManagement</span></span>
* <span data-ttu-id="cb73b-2708">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2708">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="cb73b-2709">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb73b-2709">Az.Automation</span></span>
* <span data-ttu-id="cb73b-2710">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2710">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="cb73b-2711">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2711">Added Update Management cmdlets</span></span>
* <span data-ttu-id="cb73b-2712">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2712">Added Source Control cmdlets</span></span>
* <span data-ttu-id="cb73b-2713">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2713">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="cb73b-2714">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2714">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="cb73b-2715">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb73b-2715">Az.Compute</span></span>
* <span data-ttu-id="cb73b-2716">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2716">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="cb73b-2717">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2717">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="cb73b-2718">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="cb73b-2718">Az.ContainerInstance</span></span>
* <span data-ttu-id="cb73b-2719">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2719">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="cb73b-2720">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="cb73b-2720">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="cb73b-2721">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2721">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="cb73b-2722">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb73b-2722">Az.Network</span></span>
* <span data-ttu-id="cb73b-2723">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2723">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="cb73b-2724">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2724">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="cb73b-2725">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2725">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="cb73b-2726">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2726">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="cb73b-2727">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="cb73b-2727">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="cb73b-2728">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2728">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="cb73b-2729">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2729">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="cb73b-2730">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="cb73b-2730">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="cb73b-2731">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2731">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="cb73b-2732">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2732">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="cb73b-2733">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="cb73b-2733">Az.Relay</span></span>
* <span data-ttu-id="cb73b-2734">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2734">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="cb73b-2735">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb73b-2735">Az.Resources</span></span>
* <span data-ttu-id="cb73b-2736">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2736">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="cb73b-2737">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2737">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="cb73b-2738">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2738">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="cb73b-2739">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cb73b-2739">Az.ServiceFabric</span></span>
* <span data-ttu-id="cb73b-2740">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2740">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="cb73b-2741">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb73b-2741">Az.Sql</span></span>
* <span data-ttu-id="cb73b-2742">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2742">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="cb73b-2743">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2743">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="cb73b-2744">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2744">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="cb73b-2745">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2745">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="cb73b-2746">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2746">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="cb73b-2747">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2747">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="cb73b-2748">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2748">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="cb73b-2749">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2749">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="cb73b-2750">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2750">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="cb73b-2751">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2751">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="cb73b-2752">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2752">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="cb73b-2753">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2753">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="cb73b-2754">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2754">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="cb73b-2755">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2755">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="cb73b-2756">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2756">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="cb73b-2757">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2757">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="cb73b-2758">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2758">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="cb73b-2759">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2759">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="cb73b-2760">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="cb73b-2760">General</span></span>
* <span data-ttu-id="cb73b-2761">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="cb73b-2761">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="cb73b-2762">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="cb73b-2762">Az.Profile</span></span>
* <span data-ttu-id="cb73b-2763">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2763">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="cb73b-2764">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="cb73b-2764">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="cb73b-2765">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="cb73b-2765">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="cb73b-2766">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2766">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="cb73b-2767">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2767">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="cb73b-2768">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2768">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="cb73b-2769">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="cb73b-2769">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="cb73b-2770">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-2770">Az.CognitiveServices</span></span>
* <span data-ttu-id="cb73b-2771">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2771">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb73b-2772">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb73b-2772">Az.Compute</span></span>
* <span data-ttu-id="cb73b-2773">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="cb73b-2773">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="cb73b-2774">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="cb73b-2774">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="cb73b-2775">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2775">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb73b-2776">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb73b-2776">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb73b-2777">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2777">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="cb73b-2778">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2778">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="cb73b-2779">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="cb73b-2779">Az.Insights</span></span>
* <span data-ttu-id="cb73b-2780">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="cb73b-2780">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="cb73b-2781">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="cb73b-2781">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="cb73b-2782">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="cb73b-2782">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="cb73b-2783">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2783">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb73b-2784">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb73b-2784">Az.Network</span></span>
* <span data-ttu-id="cb73b-2785">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="cb73b-2785">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="cb73b-2786">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="cb73b-2786">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="cb73b-2787">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="cb73b-2787">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="cb73b-2788">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="cb73b-2788">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="cb73b-2789">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="cb73b-2789">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="cb73b-2790">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="cb73b-2790">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="cb73b-2791">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="cb73b-2791">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cb73b-2792">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cb73b-2792">Az.PolicyInsights</span></span>
* <span data-ttu-id="cb73b-2793">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2793">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb73b-2794">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb73b-2794">Az.Resources</span></span>
* <span data-ttu-id="cb73b-2795">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2795">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="cb73b-2796">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="cb73b-2796">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="cb73b-2797">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cb73b-2797">Az.ServiceBus</span></span>
* <span data-ttu-id="cb73b-2798">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2798">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cb73b-2799">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cb73b-2799">Az.ServiceFabric</span></span>
* <span data-ttu-id="cb73b-2800">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2800">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="cb73b-2801">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="cb73b-2801">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="cb73b-2802">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="cb73b-2802">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="cb73b-2803">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="cb73b-2803">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="cb73b-2804">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2804">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="cb73b-2805">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2805">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="cb73b-2806">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="cb73b-2806">Az.Profile</span></span>
* <span data-ttu-id="cb73b-2807">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="cb73b-2807">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="cb73b-2808">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2808">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb73b-2809">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb73b-2809">Az.Compute</span></span>
* <span data-ttu-id="cb73b-2810">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="cb73b-2810">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="cb73b-2811">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2811">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb73b-2812">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb73b-2812">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb73b-2813">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="cb73b-2813">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="cb73b-2814">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2814">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="cb73b-2815">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2815">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="cb73b-2816">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2816">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="cb73b-2817">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2817">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb73b-2818">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb73b-2818">Az.Network</span></span>
* <span data-ttu-id="cb73b-2819">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2819">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="cb73b-2820">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2820">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb73b-2821">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb73b-2821">Az.Resources</span></span>
* <span data-ttu-id="cb73b-2822">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2822">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="cb73b-2823">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2823">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="cb73b-2824">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2824">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="cb73b-2825">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="cb73b-2825">Azure.Storage</span></span>
* <span data-ttu-id="cb73b-2826">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2826">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="cb73b-2827">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="cb73b-2827">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="cb73b-2828">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="cb73b-2828">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="cb73b-2829">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2829">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="cb73b-2830">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="cb73b-2830">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cb73b-2831">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cb73b-2831">Az.CognitiveServices</span></span>
* <span data-ttu-id="cb73b-2832">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2832">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb73b-2833">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb73b-2833">Az.Compute</span></span>
* <span data-ttu-id="cb73b-2834">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="cb73b-2834">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="cb73b-2835">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2835">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="cb73b-2836">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2836">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="cb73b-2837">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="cb73b-2837">Az.DataFactoryV2</span></span>
* <span data-ttu-id="cb73b-2838">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2838">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb73b-2839">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb73b-2839">Az.Network</span></span>
* <span data-ttu-id="cb73b-2840">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2840">Added NetworkProfile functionality.</span></span> <span data-ttu-id="cb73b-2841">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="cb73b-2841">new cmdlets added</span></span>
    - <span data-ttu-id="cb73b-2842">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cb73b-2842">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="cb73b-2843">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cb73b-2843">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="cb73b-2844">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cb73b-2844">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="cb73b-2845">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cb73b-2845">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="cb73b-2846">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="cb73b-2846">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="cb73b-2847">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="cb73b-2847">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="cb73b-2848">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2848">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="cb73b-2849">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="cb73b-2849">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="cb73b-2850">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="cb73b-2850">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="cb73b-2851">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="cb73b-2851">Az.RedisCache</span></span>
* <span data-ttu-id="cb73b-2852">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2852">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="cb73b-2853">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2853">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb73b-2854">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb73b-2854">Az.Resources</span></span>
* <span data-ttu-id="cb73b-2855">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cb73b-2855">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="cb73b-2856">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="cb73b-2856">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb73b-2857">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb73b-2857">Az.Sql</span></span>
* <span data-ttu-id="cb73b-2858">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2858">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb73b-2859">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb73b-2859">Az.Websites</span></span>
* <span data-ttu-id="cb73b-2860">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="cb73b-2860">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="cb73b-2861">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="cb73b-2861">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="cb73b-2862">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="cb73b-2862">0.2.0 - September 2018</span></span>
 <span data-ttu-id="cb73b-2863">Начальный выпуск</span><span class="sxs-lookup"><span data-stu-id="cb73b-2863">Initial Release</span></span>
