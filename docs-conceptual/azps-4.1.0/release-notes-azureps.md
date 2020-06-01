---
title: Заметки о выпуске Azure PowerShell
description: Узнайте обо всех последних обновлениях модулей Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: 60827fe7b4f8c351655046e3711660cdf7ce0513
ms.sourcegitcommit: 10ec909100a70acec94d42f6084e7bf0342c6854
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/19/2020
ms.locfileid: "83631070"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="27133-103">Заметки о выпуске Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="27133-103">Azure PowerShell release notes</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="27133-104">4.1.0 — май 2020 г.</span><span class="sxs-lookup"><span data-stu-id="27133-104">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="27133-105">Основные сведения о новых возможностях с момента последнего выпуска</span><span class="sxs-lookup"><span data-stu-id="27133-105">Highlights since the last release</span></span>
* <span data-ttu-id="27133-106">Поддерживаемые версии PowerShell: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="27133-106">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="27133-107">Вышла общедоступная версия модуля Az.Functions.</span><span class="sxs-lookup"><span data-stu-id="27133-107">General availability of Az.Functions</span></span> 
* <span data-ttu-id="27133-108">Состоялся основной выпуск Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources и Az.Storage.</span><span class="sxs-lookup"><span data-stu-id="27133-108">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="27133-109">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27133-109">Az.Accounts</span></span>
* <span data-ttu-id="27133-110">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметры AzureSynapseAnalyticsEndpointResourceId и AzureSynapseAnalyticsEndpointSuffix.</span><span class="sxs-lookup"><span data-stu-id="27133-110">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="27133-111">В Az.Accounts добавлены сборки, связанные с Azure.Core. Добавлена поддержка Windows PowerShell 5.1, PowerShell Core 6.2.4 и PowerShell 7+.</span><span class="sxs-lookup"><span data-stu-id="27133-111">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="27133-112">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="27133-112">Az.Aks</span></span>
* <span data-ttu-id="27133-113">Версия API обновлена до 2019-10-01.</span><span class="sxs-lookup"><span data-stu-id="27133-113">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="27133-114">Добавлена возможность создания контейнера Windows в службе Azure Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="27133-114">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="27133-115">Добавлены новые командлеты: New-AzAksNodePool, Update-AzAksNodePool, Remove-AzAksNodePool, Get-AzAksNodePool, Install-AzAksKubectl, Get-AzAksVersion.</span><span class="sxs-lookup"><span data-stu-id="27133-115">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="27133-116">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="27133-116">Az.ApiManagement</span></span>
* <span data-ttu-id="27133-117">В New-AzApiManagement и Set-AzApiManagement параметр -AssignIdentity переименован в -SystemAssignedIdentity.</span><span class="sxs-lookup"><span data-stu-id="27133-117">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="27133-118">В New-AzApiManagement и Set-AzApiManagement добавлен новый параметр -UserAssignedIdentity <строка[]>.</span><span class="sxs-lookup"><span data-stu-id="27133-118">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="27133-119">Командлет Get-AzApiManagementProperty переименован в Get-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="27133-119">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="27133-120">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="27133-120">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="27133-121">Командлет New-AzApiManagementProperty переименован в New-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="27133-121">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="27133-122">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="27133-122">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="27133-123">Командлет Set-AzApiManagementProperty переименован в Set-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="27133-123">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="27133-124">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="27133-124">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="27133-125">Командлет Remove-AzApiManagementProperty переименован в Remove-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="27133-125">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="27133-126">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="27133-126">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="27133-127">Добавлен новый командлет Get-AzApiManagementAuthorizationServerClientSecret, а Get-AzApiManagementAuthorizationServer теперь не возвращает секрет клиента.</span><span class="sxs-lookup"><span data-stu-id="27133-127">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="27133-128">Добавлен новый командлет Get-AzApiManagementNamedValueSecretValue, а Get-AzApiManagementNamedValue теперь не возвращает значение секрета.</span><span class="sxs-lookup"><span data-stu-id="27133-128">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="27133-129">Добавлен новый командлет Get-AzApiManagementOpenIdConnectProviderClientSecret, а Get-AzApiManagementOpenIdConnectProvider теперь не возвращает секрет клиента.</span><span class="sxs-lookup"><span data-stu-id="27133-129">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="27133-130">Добавлен новый командлет Get-AzApiManagementSubscriptionKey, а Get-AzApiManagementSubscription теперь не возвращает ключи подписки.</span><span class="sxs-lookup"><span data-stu-id="27133-130">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="27133-131">Добавлен новый командлет Get-AzApiManagementTenantAccessSecret, а Get-AzApiManagementTenantAccess теперь не возвращает ключи.</span><span class="sxs-lookup"><span data-stu-id="27133-131">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="27133-132">Добавлен новый командлет Get-AzApiManagementTenantGitAccessSecret, а Get-AzApiManagementTenantGitAccess теперь не возвращает ключи.</span><span class="sxs-lookup"><span data-stu-id="27133-132">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="27133-133">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="27133-133">Az.ApplicationInsights</span></span>
* <span data-ttu-id="27133-134">В New-AzApplicationInsights добавлены параметры RetentionInDays, PublicNetworkAccessForIngestion и PublicNetworkAccessForQuery.</span><span class="sxs-lookup"><span data-stu-id="27133-134">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="27133-135">Создан командлет Update-AzApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="27133-135">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="27133-136">Созданы командлеты для связанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="27133-136">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="27133-137">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="27133-137">Az.Batch</span></span>
* <span data-ttu-id="27133-138">В командлеты Az.Batch добавлена поддержка пакетов SDK Microsoft.Azure.Batch версии 13.0.0 и SDK Microsoft.Azure.Management.Batch версии 9.0.0.</span><span class="sxs-lookup"><span data-stu-id="27133-138">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="27133-139">Теперь в New-AzBatchCertificate можно выбрать тип добавляемого сертификата с помощью нового параметра -CertificateKind.</span><span class="sxs-lookup"><span data-stu-id="27133-139">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="27133-140">В PSApplication удалено свойство ApplicationPackages.</span><span class="sxs-lookup"><span data-stu-id="27133-140">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="27133-141">Отдельные пакеты в приложении теперь можно извлечь с помощью Get-AzBatchApplicationPackage.</span><span class="sxs-lookup"><span data-stu-id="27133-141">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="27133-142">Пример: Get-AzBatchApplication -AccountName моя_учетная_запись -ResourceGroupName моя_группа_ресурсов -ApplicationId мое_приложение.</span><span class="sxs-lookup"><span data-stu-id="27133-142">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="27133-143">При создании пула с помощью New-AzBatchPool свойство VirtualMachineImageId элемента PSImageReference теперь может ссылаться только на образ из Общей коллекции образов.</span><span class="sxs-lookup"><span data-stu-id="27133-143">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="27133-144">При создании пула с помощью New-AzBatchPool пул можно подготовить без общедоступного IP-адреса, используя новое свойство PublicIPAddressConfiguration элемента PSNetworkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="27133-144">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="27133-145">Свойство PublicIPs элемента PSNetworkConfiguration было передано элементу PSPublicIPAddressConfiguration.</span><span class="sxs-lookup"><span data-stu-id="27133-145">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="27133-146">Это свойство можно указать, только если параметру IPAddressProvisioningType присвоено значение UserManaged.</span><span class="sxs-lookup"><span data-stu-id="27133-146">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27133-147">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27133-147">Az.Compute</span></span>
* <span data-ttu-id="27133-148">В командлет Update-AzVM добавлен параметр HostId.</span><span class="sxs-lookup"><span data-stu-id="27133-148">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="27133-149">Обновлена справочная документация по командлетам New-AzVMConfig, New-AzVmssConfig, Update-AzVmss, Set-AzVMOperatingSystem и Set-AzVmssOsProfile.</span><span class="sxs-lookup"><span data-stu-id="27133-149">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="27133-150">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="27133-150">Breaking changes</span></span>
    - <span data-ttu-id="27133-151">Параметр FilterExpression удален из командлета Get-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="27133-151">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="27133-152">Параметр AssignIdentity удален из командлетов New-AzVmssConfig, New-AzVMConfig и Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="27133-152">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="27133-153">Параметр AutomaticRepairMaxInstanceRepairsPercent удален из командлетов New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="27133-153">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="27133-154">Свойства AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus и VirtualMachineScaleSetsColocationStatus удалены из ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="27133-154">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="27133-155">Свойство MaxInstanceRepairsPercent удалено из AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="27133-155">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="27133-156">Типы AvailabilitySets, VirtualMachines и VirtualMachineScaleSets изменены с IList<SubResource> на IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="27133-156">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="27133-157">Уточнено описание командлета Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="27133-157">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="27133-158">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27133-158">Az.DataFactory</span></span>
* <span data-ttu-id="27133-159">Добавлена поддержка операций CRUD для свойств среды выполнения потока данных в управляемой среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="27133-159">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="27133-160">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="27133-160">Az.FrontDoor</span></span>
* <span data-ttu-id="27133-161">Добавлены новые командлеты для создания, обновления, извлечения и удаления объекта обработчика правил Front Door.</span><span class="sxs-lookup"><span data-stu-id="27133-161">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="27133-162">Добавлены вспомогательные командлеты для создания объекта обработчика правил Front Door.</span><span class="sxs-lookup"><span data-stu-id="27133-162">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="27133-163">Добавлена ссылка обработчика правил на объект правила маршрутизации Front Door.</span><span class="sxs-lookup"><span data-stu-id="27133-163">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="27133-164">Добавлены параметры Приватного канала на серверный объект Front Door.</span><span class="sxs-lookup"><span data-stu-id="27133-164">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="27133-165">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="27133-165">Az.Functions</span></span>
* <span data-ttu-id="27133-166">Вышла общедоступная версия модуля Az.Functions.</span><span class="sxs-lookup"><span data-stu-id="27133-166">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="27133-167">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="27133-167">Az.HDInsight</span></span>
* <span data-ttu-id="27133-168">Добавлена поддержка шифрования управляемых клиентом ключей.</span><span class="sxs-lookup"><span data-stu-id="27133-168">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="27133-169">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="27133-169">Az.HealthcareApis</span></span>
* <span data-ttu-id="27133-170">Политики доступа для текущего субъекта теперь не используются по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="27133-170">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="27133-171">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="27133-171">Az.IotHub</span></span>
* <span data-ttu-id="27133-172">Добавлен командлет для вызова запроса в центре Интернета вещей для получения данных с помощью SQL-подобного языка.</span><span class="sxs-lookup"><span data-stu-id="27133-172">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="27133-173">Устранена проблема, когда с помощью Add-AzIotHubDevice не удавалось создать устройство с поддержкой IoT Edge без дочерних устройств (№ 11597).</span><span class="sxs-lookup"><span data-stu-id="27133-173">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="27133-174">Добавлен командлет для создания маркера SAS для Центра Интернета вещей, устройства или модуля.</span><span class="sxs-lookup"><span data-stu-id="27133-174">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="27133-175">Добавлен командлет для вызова запроса метрик конфигурации.</span><span class="sxs-lookup"><span data-stu-id="27133-175">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="27133-176">Появилась возможность управлять автоматическим развертыванием IoT Edge в большом масштабе.</span><span class="sxs-lookup"><span data-stu-id="27133-176">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="27133-177">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="27133-177">New cmdlets are:</span></span>
    - <span data-ttu-id="27133-178">Add-AzIotHubDeployment;</span><span class="sxs-lookup"><span data-stu-id="27133-178">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="27133-179">Get-AzIotHubDeployment;</span><span class="sxs-lookup"><span data-stu-id="27133-179">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="27133-180">Remove-AzIotHubDeployment;</span><span class="sxs-lookup"><span data-stu-id="27133-180">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="27133-181">Set-AzIotHubDeployment.</span><span class="sxs-lookup"><span data-stu-id="27133-181">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="27133-182">Добавлен командлет для вызова запроса метрик развертывания IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="27133-182">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="27133-183">Добавлен командлет для применения содержимого конфигурации к указанному пограничному устройству.</span><span class="sxs-lookup"><span data-stu-id="27133-183">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="27133-184">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27133-184">Az.KeyVault</span></span>
* <span data-ttu-id="27133-185">Удалены два псевдонима: New-AzKeyVaultCertificateAdministratorDetails и New-AzKeyVaultCertificateOrganizationDetails.</span><span class="sxs-lookup"><span data-stu-id="27133-185">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="27133-186">При создании хранилища ключей обратимое удаление включено по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="27133-186">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="27133-187">Можно задать правила сети, чтобы при создании хранилища ключей управлять доступом из определенных сетевых расположений.</span><span class="sxs-lookup"><span data-stu-id="27133-187">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="27133-188">Добавлена возможность создания собственных ключей (BYOK).</span><span class="sxs-lookup"><span data-stu-id="27133-188">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="27133-189">С помощью Add-AzKeyVaultKey теперь можно создавать ключ обмена ключами.</span><span class="sxs-lookup"><span data-stu-id="27133-189">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="27133-190">С помощью Get-AzKeyVaultKey можно скачать открытый ключ в формате PEM.</span><span class="sxs-lookup"><span data-stu-id="27133-190">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="27133-191">Обновлен раздел KeyOps справочной документации по Add-AzKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="27133-191">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27133-192">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27133-192">Az.Monitor</span></span>
* <span data-ttu-id="27133-193">Исправлена ошибка Set-AzDiagnosticSettings, когда политика хранения не применялась ко всем категориям (№ 11589).</span><span class="sxs-lookup"><span data-stu-id="27133-193">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="27133-194">Добавлена поддержка критериев доступности веб-теста для оповещения метрики версии 2.</span><span class="sxs-lookup"><span data-stu-id="27133-194">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="27133-195">В New-AzMetricAlertRuleV2Criteria добавлена возможность создавать критерии доступности веб-теста.</span><span class="sxs-lookup"><span data-stu-id="27133-195">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="27133-196">Add-AzMetricAlertRuleV2 теперь поддерживает новые критерии доступности веб-теста.</span><span class="sxs-lookup"><span data-stu-id="27133-196">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="27133-197">В PSLogProfile исправлено избыточное определение RetentionPolicy (№ 7608).</span><span class="sxs-lookup"><span data-stu-id="27133-197">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="27133-198">В PSEventData удалены избыточные определения свойств (№ 11353).</span><span class="sxs-lookup"><span data-stu-id="27133-198">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="27133-199">Командлет Get-AzLog переименован в Get-AzActivityLog.</span><span class="sxs-lookup"><span data-stu-id="27133-199">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27133-200">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27133-200">Az.Network</span></span>
* <span data-ttu-id="27133-201">Добавлен атрибут критического изменения, сообщающий о том, что поведение зоны по умолчанию будет изменено.</span><span class="sxs-lookup"><span data-stu-id="27133-201">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="27133-202">New-AzPublicIpAddress;</span><span class="sxs-lookup"><span data-stu-id="27133-202">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="27133-203">New-AzPublicIpPrefix;</span><span class="sxs-lookup"><span data-stu-id="27133-203">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="27133-204">New-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="27133-204">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="27133-205">Добавлена поддержка нового ресурса верхнего уровня SecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="27133-205">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="27133-206">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="27133-206">New cmdlets added:</span></span>
        - <span data-ttu-id="27133-207">New-AzSecurityPartnerProvider;</span><span class="sxs-lookup"><span data-stu-id="27133-207">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="27133-208">Remove-AzSecurityPartnerProvider;</span><span class="sxs-lookup"><span data-stu-id="27133-208">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="27133-209">Get-AzSecurityPartnerProvider;</span><span class="sxs-lookup"><span data-stu-id="27133-209">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="27133-210">Set-AzSecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="27133-210">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="27133-211">В PSPrivateLinkResource добавлен параметр RequiredZoneNames, а в PSPrivateEndpointConnection — GroupId.</span><span class="sxs-lookup"><span data-stu-id="27133-211">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="27133-212">Исправлен неправильный тип параметра SuccessThresholdRoundTripTimeMs для New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.</span><span class="sxs-lookup"><span data-stu-id="27133-212">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="27133-213">В командлетах VirtualWan аргументу AllowVnetToVnetTraffic теперь по умолчанию присвоено значение True.</span><span class="sxs-lookup"><span data-stu-id="27133-213">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="27133-214">New-AzVirtualWan;</span><span class="sxs-lookup"><span data-stu-id="27133-214">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="27133-215">Update-AzVirtualWan.</span><span class="sxs-lookup"><span data-stu-id="27133-215">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="27133-216">Добавлены новые командлеты для поддержки группы зон DNS для частной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="27133-216">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="27133-217">New-AzPrivateDnsZoneConfig;</span><span class="sxs-lookup"><span data-stu-id="27133-217">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="27133-218">Get-AzPrivateDnsZoneGroup;</span><span class="sxs-lookup"><span data-stu-id="27133-218">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="27133-219">New-AzPrivateDnsZoneGroup;</span><span class="sxs-lookup"><span data-stu-id="27133-219">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="27133-220">Set-AzPrivateDnsZoneGroup;</span><span class="sxs-lookup"><span data-stu-id="27133-220">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="27133-221">Remove-AzPrivateDnsZoneGroup.</span><span class="sxs-lookup"><span data-stu-id="27133-221">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="27133-222">В AzureFirewall добавлены параметры DNSEnableProxy, DNSRequireProxyForNetworkRules и DNSServers.</span><span class="sxs-lookup"><span data-stu-id="27133-222">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="27133-223">В AzureFirewall добавлены параметры EnableDnsProxy, DnsProxyNotRequiredForNetworkRule и DnsServer.</span><span class="sxs-lookup"><span data-stu-id="27133-223">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="27133-224">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="27133-224">Updated cmdlet:</span></span>
        - <span data-ttu-id="27133-225">New-AzFirewall.</span><span class="sxs-lookup"><span data-stu-id="27133-225">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="27133-226">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="27133-226">Az.OperationalInsights</span></span>
* <span data-ttu-id="27133-227">Обновлен устаревший код для использования новых пакетов SDK.</span><span class="sxs-lookup"><span data-stu-id="27133-227">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="27133-228">Из-за устаревших API-интерфейсов удалены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="27133-228">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="27133-229">Get-AzOperationalInsightsSavedSearchResult (псевдоним Get-AzOperationalInsightsSavedSearchResults);</span><span class="sxs-lookup"><span data-stu-id="27133-229">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="27133-230">Get-AzOperationalInsightsSearchResult (псевдоним Get-AzOperationalInsightsSearchResults);</span><span class="sxs-lookup"><span data-stu-id="27133-230">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="27133-231">Get-AzOperationalInsightsLinkTarget (псевдоним Get-AzOperationalInsightsLinkTargets).</span><span class="sxs-lookup"><span data-stu-id="27133-231">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="27133-232">В Set-AzOperationalInsightsWorkspace и New-AzOperationalInsightsWorkspace добавлены новые параметры.</span><span class="sxs-lookup"><span data-stu-id="27133-232">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="27133-233">Созданы командлеты для связанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="27133-233">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="27133-234">Созданы командлеты для кластеров и связанной службы.</span><span class="sxs-lookup"><span data-stu-id="27133-234">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27133-235">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27133-235">Az.RecoveryServices</span></span>
* <span data-ttu-id="27133-236">В Azure Site Recovery добавлена поддержка защиты поставщика Azure для групп размещения виртуальных машин Azure близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="27133-236">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="27133-237">В Azure Site Recovery добавлена поддержка репликации из зоны в зону.</span><span class="sxs-lookup"><span data-stu-id="27133-237">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="27133-238">В Azure Backup добавлена поддержка долгосрочного хранения для точек восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="27133-238">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="27133-239">В выходные данные командлета Get-AzRecoveryServicesBackupItem добавлены свойства исключения диска, добавленного в Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="27133-239">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="27133-240">Добавлена частная конечная точка для файла учетных данных хранилища для службы Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="27133-240">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="27133-241">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27133-241">Az.Resources</span></span>
* <span data-ttu-id="27133-242">Добавлено предупреждение о задержке представления при создании определения роли.</span><span class="sxs-lookup"><span data-stu-id="27133-242">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="27133-243">Командлеты политики теперь выводят строго типизированные объекты.</span><span class="sxs-lookup"><span data-stu-id="27133-243">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="27133-244">Из командлета Get-AzResourceLock удален параметр -TenantLevel (№ 11335).</span><span class="sxs-lookup"><span data-stu-id="27133-244">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="27133-245">Исправлена ошибка с Remove-AzResourceGroup -Id ResourceId (№ 9882).</span><span class="sxs-lookup"><span data-stu-id="27133-245">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="27133-246">Добавлен новый командлет для получения результатов анализа гипотетических вариантов из шаблона ARM в области группы ресурсов: Get-AzDeploymentResourceGroupWhatIfResult.</span><span class="sxs-lookup"><span data-stu-id="27133-246">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="27133-247">Добавлен новый командлет для получения результатов анализа гипотетических вариантов из шаблона ARM в области подписки: Get-AzDeploymentWhatIfResult.</span><span class="sxs-lookup"><span data-stu-id="27133-247">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="27133-248">Alias: Get-AzSubscriptionDeploymentWhatIf.</span><span class="sxs-lookup"><span data-stu-id="27133-248">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="27133-249">Переопределены параметры -WhatIf и -Confirm для New-AzDeployment и New-AzResourceGroupDeployment для использования результатов анализа гипотетических вариантов из шаблона ARM.</span><span class="sxs-lookup"><span data-stu-id="27133-249">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="27133-250">В командлеты развертывания добавлено сообщение об устаревании для параметра ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="27133-250">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="27133-251">Добавлена возможность отображения улучшенных сообщений об ошибках при развертывании.</span><span class="sxs-lookup"><span data-stu-id="27133-251">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="27133-252">Добавлена возможность регистрации correlationId для сбоев развертывания.</span><span class="sxs-lookup"><span data-stu-id="27133-252">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="27133-253">В выходные данные скрипта развертывания добавлено свойство error.</span><span class="sxs-lookup"><span data-stu-id="27133-253">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="27133-254">Пакет NuGet Microsoft.Azure.Management.ResourceManager обновлен до версии 3.7.1-preview.</span><span class="sxs-lookup"><span data-stu-id="27133-254">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="27133-255">Удаленные определенные тестовые случаи как свойство error в DeploymentValidateResult были изменены на доступные только для чтения из пакета NuGet версии 3.7.1-preview.</span><span class="sxs-lookup"><span data-stu-id="27133-255">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="27133-256">Добавлен GenericResourceExpanded из пакета SDK ResourceManager версии 3.7.1-preview.</span><span class="sxs-lookup"><span data-stu-id="27133-256">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="27133-257">Добавлена поддержка тегов для всех командлетов Get для развертывания, а также для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="27133-257">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="27133-258">New-AzDeployment;</span><span class="sxs-lookup"><span data-stu-id="27133-258">'New-AzDeployment'</span></span>
    - <span data-ttu-id="27133-259">New-AzManagementGroupDeployment;</span><span class="sxs-lookup"><span data-stu-id="27133-259">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="27133-260">New-AzResourceGroupDeployment;</span><span class="sxs-lookup"><span data-stu-id="27133-260">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="27133-261">New-AzTenantDeployment.</span><span class="sxs-lookup"><span data-stu-id="27133-261">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="27133-262">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="27133-262">Az.ServiceFabric</span></span>
* <span data-ttu-id="27133-263">Исправлена ошибка при добавлении сертификата с помощью параметра -SecretIdentifier, когда возвращался неправильный отпечаток сертификата.</span><span class="sxs-lookup"><span data-stu-id="27133-263">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="27133-264">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27133-264">Az.Sql</span></span>
* <span data-ttu-id="27133-265">Оптимизирована работа следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="27133-265">Enhance performance of:</span></span>
    - <span data-ttu-id="27133-266">Set-AzSqlDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="27133-266">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="27133-267">Set-AzSqlInstanceDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="27133-267">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="27133-268">Remove-AzSqlDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="27133-268">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="27133-269">Remove-AzSqlInstanceDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="27133-269">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="27133-270">Enable-AzSqlDatabaseSensitivityRecommendation;</span><span class="sxs-lookup"><span data-stu-id="27133-270">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="27133-271">Enable-AzSqlInstanceDatabaseSensitivityRecommendation;</span><span class="sxs-lookup"><span data-stu-id="27133-271">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="27133-272">Disable-AzSqlDatabaseSensitivityRecommendation;</span><span class="sxs-lookup"><span data-stu-id="27133-272">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="27133-273">Disable-AzSqlInstanceDatabaseSensitivityRecommendation.</span><span class="sxs-lookup"><span data-stu-id="27133-273">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="27133-274">Удалена проверка на стороне клиента параметра RetentionDays из командлета Set-AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="27133-274">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="27133-275">Добавлен аудит учетной записи хранения в виртуальной сети. Исправлена ошибка при создании роли участника данных BLOB-объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="27133-275">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27133-276">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27133-276">Az.Storage</span></span>
* <span data-ttu-id="27133-277">В командлет Get-AzStorageAccount добавлен параметр -AsJob.</span><span class="sxs-lookup"><span data-stu-id="27133-277">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="27133-278">Параметр KeyVersion теперь является необязательным при изменении учетной записи хранения с помощью KeyvaultEncryption, что обеспечивает поддержку автоматической смены ключа.</span><span class="sxs-lookup"><span data-stu-id="27133-278">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="27133-279">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27133-279">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="27133-280">Исправлена ошибка при удалении каталога файлов Azure с конвейером.</span><span class="sxs-lookup"><span data-stu-id="27133-280">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="27133-281">Remove-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="27133-281">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="27133-282">Исправлена ошибка 9880. Значение DefaultAction для NetWorkRule приведено в соответствие со Swagger.</span><span class="sxs-lookup"><span data-stu-id="27133-282">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="27133-283">Update-AzStorageAccountNetworkRuleSet;</span><span class="sxs-lookup"><span data-stu-id="27133-283">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="27133-284">Get-AzStorageAccountNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="27133-284">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="27133-285">Исправлена ошибка 11624. При добавлении NetworkRules дублирующиеся правила пропускаются, чтобы не происходил сбой сервера.</span><span class="sxs-lookup"><span data-stu-id="27133-285">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="27133-286">Add-AzStorageAccountNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="27133-286">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="27133-287">Версия пакета SDK Microsoft.Azure.Cosmos.Table обновлена до 1.0.7.</span><span class="sxs-lookup"><span data-stu-id="27133-287">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="27133-288">Добавлено предупреждающее сообщение, напоминающее пользователю о необходимости повторного вывода списка с помощью ContinuationToken, когда в списке элементов Data Lake 2-го поколения возвращается только часть элементов.</span><span class="sxs-lookup"><span data-stu-id="27133-288">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="27133-289">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="27133-289">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="27133-290">Добавлена возможность создания или изменения учетной записи хранения с использованием проверки подлинности Active Directory для Файлов Azure.</span><span class="sxs-lookup"><span data-stu-id="27133-290">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="27133-291">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27133-291">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="27133-292">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27133-292">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="27133-293">Добавлена возможность создания и просмотра ключей Kerberos учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="27133-293">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="27133-294">New-AzStorageAccountKey;</span><span class="sxs-lookup"><span data-stu-id="27133-294">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="27133-295">Get-AzStorageAccountKey.</span><span class="sxs-lookup"><span data-stu-id="27133-295">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="27133-296">Добавлена возможность отработки отказа для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="27133-296">Supported failover Storage account</span></span>
    - <span data-ttu-id="27133-297">Invoke-AzStorageAccountFailover.</span><span class="sxs-lookup"><span data-stu-id="27133-297">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="27133-298">Обновлена справка по Get-AzStorageBlobCopyState.</span><span class="sxs-lookup"><span data-stu-id="27133-298">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="27133-299">Обновлена справка по Get-AzStorageFileCopyState и Start-AzStorageBlobCopy.</span><span class="sxs-lookup"><span data-stu-id="27133-299">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="27133-300">Появилась интегрированная клиентская библиотека хранилища версии 12 для командлетов очередей и файлов.</span><span class="sxs-lookup"><span data-stu-id="27133-300">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="27133-301">Тип выходных данных изменен с CloudFile на AzureStorageFile. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="27133-301">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="27133-302">Get-AzStorageFile;</span><span class="sxs-lookup"><span data-stu-id="27133-302">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="27133-303">Remove-AzStorageFile;</span><span class="sxs-lookup"><span data-stu-id="27133-303">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="27133-304">Get-AzStorageFileContent;</span><span class="sxs-lookup"><span data-stu-id="27133-304">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="27133-305">Set-AzStorageFileContent;</span><span class="sxs-lookup"><span data-stu-id="27133-305">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="27133-306">Start-AzStorageFileCopy.</span><span class="sxs-lookup"><span data-stu-id="27133-306">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="27133-307">Тип выходных данных изменен с CloudFileDirectory на AzureStorageFileDirectory. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="27133-307">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="27133-308">New-AzStorageDirectory;</span><span class="sxs-lookup"><span data-stu-id="27133-308">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="27133-309">Remove-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="27133-309">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="27133-310">Тип выходных данных изменен с CloudFileShare на AzureStorageFileShare. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="27133-310">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="27133-311">Get-AzStorageShare;</span><span class="sxs-lookup"><span data-stu-id="27133-311">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="27133-312">New-AzStorageShare;</span><span class="sxs-lookup"><span data-stu-id="27133-312">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="27133-313">Remove-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="27133-313">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="27133-314">Тип выходных данных изменен с FileShareProperties на AzureStorageFileShare. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="27133-314">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="27133-315">Set-AzStorageShareQuota.</span><span class="sxs-lookup"><span data-stu-id="27133-315">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="27133-316">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="27133-316">Az.TrafficManager</span></span>
* <span data-ttu-id="27133-317">Исправлено неправильное имя профиля в подробных выходных данных DisableAzureTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="27133-317">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27133-318">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27133-318">Az.Websites</span></span>
* <span data-ttu-id="27133-319">Исправлена опечатка в справке по Update-AzWebAppAccessRestrictionConfig.</span><span class="sxs-lookup"><span data-stu-id="27133-319">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="27133-320">3.8.0 — апрель 2020 г.</span><span class="sxs-lookup"><span data-stu-id="27133-320">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="27133-321">Основные сведения о новых возможностях с момента последнего выпуска</span><span class="sxs-lookup"><span data-stu-id="27133-321">Highlights since the last release</span></span>
* <span data-ttu-id="27133-322">Версии PowerShell, которые поддерживает Az.Storage: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="27133-322">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="27133-323">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27133-323">Az.Accounts</span></span>
* <span data-ttu-id="27133-324">Обновлен URL-адрес опроса Azure PowerShell в Resolve-AzError [11507].</span><span class="sxs-lookup"><span data-stu-id="27133-324">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="27133-325">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="27133-325">Az.ApiManagement</span></span>
* <span data-ttu-id="27133-326">Добавлено уведомление о критическом изменении для изменения выходных данных командлетов, выполняющих действия с файлами в Azure, в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="27133-326">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="27133-327">Обновлена документация для Set-AzApiManagementGroup с указанием параметра GroupId.</span><span class="sxs-lookup"><span data-stu-id="27133-327">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="27133-328">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="27133-328">Az.Cdn</span></span>
* <span data-ttu-id="27133-329">Исправлено отображение ценовой категории (SKU), связанной с ChinaCDN.</span><span class="sxs-lookup"><span data-stu-id="27133-329">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="27133-330">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="27133-330">Az.CognitiveServices</span></span>
* <span data-ttu-id="27133-331">Включена поддержка Identity, Encryption, UserOwnedStorage.</span><span class="sxs-lookup"><span data-stu-id="27133-331">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27133-332">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27133-332">Az.Compute</span></span>
* <span data-ttu-id="27133-333">Добавлен командлет Set-AzVmssOrchestrationServiceState.</span><span class="sxs-lookup"><span data-stu-id="27133-333">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="27133-334">Get-AzVmss с параметром -InstanceView отображает состояния OrchestrationService.</span><span class="sxs-lookup"><span data-stu-id="27133-334">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="27133-335">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="27133-335">Az.IotHub</span></span>
* <span data-ttu-id="27133-336">Реализовано управление конфигурацией двойника устройства Интернета вещей. Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="27133-336">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="27133-337">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="27133-337">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="27133-338">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="27133-338">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="27133-339">Добавлен командлет для вызова прямого метода на устройстве в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="27133-339">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="27133-340">Реализовано управление конфигурацией двойника модуля устройства Интернета вещей. Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="27133-340">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="27133-341">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="27133-341">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="27133-342">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="27133-342">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="27133-343">Реализовано управление конфигурацией автоматического управления устройствами в центре Интернета вещей в большом масштабе.</span><span class="sxs-lookup"><span data-stu-id="27133-343">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="27133-344">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="27133-344">New cmdlets are:</span></span>
    - <span data-ttu-id="27133-345">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="27133-345">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="27133-346">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="27133-346">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="27133-347">Remove-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="27133-347">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="27133-348">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="27133-348">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="27133-349">Добавлен командлет для вызова метода периферийного модуля в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="27133-349">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="27133-350">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27133-350">Az.KeyVault</span></span>
* <span data-ttu-id="27133-351">Добавлен новый командлет Update-AzKeyVault, который может включать защиту от обратимого удаления и очистки в хранилище.</span><span class="sxs-lookup"><span data-stu-id="27133-351">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="27133-352">Включена поддержка Microsoft.PowerShell.SecretManagement [11178].</span><span class="sxs-lookup"><span data-stu-id="27133-352">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="27133-353">Исправлена ошибка в примерах Remove-AzKeyVaultManagedStorageSasDefinition [11479].</span><span class="sxs-lookup"><span data-stu-id="27133-353">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="27133-354">Включена поддержка частной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="27133-354">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="27133-355">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="27133-355">Az.Maintenance</span></span>
* <span data-ttu-id="27133-356">Опубликована версия выпуска командлетов обслуживания для общедоступной версии.</span><span class="sxs-lookup"><span data-stu-id="27133-356">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27133-357">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27133-357">Az.Monitor</span></span>
* <span data-ttu-id="27133-358">Добавлены командлеты для области приватных каналов:</span><span class="sxs-lookup"><span data-stu-id="27133-358">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="27133-359">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="27133-359">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="27133-360">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="27133-360">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="27133-361">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="27133-361">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="27133-362">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="27133-362">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="27133-363">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="27133-363">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="27133-364">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="27133-364">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="27133-365">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="27133-365">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27133-366">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27133-366">Az.Network</span></span>
* <span data-ttu-id="27133-367">Обновлены командлеты для включения подключения на частном IP-адресе для шлюза виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="27133-367">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="27133-368">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="27133-368">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="27133-369">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="27133-369">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="27133-370">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="27133-370">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="27133-371">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="27133-371">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="27133-372">Обновлены командлеты для включения шлюзов LocalNetworkGateways и сайтов VpnSites на основе FQDN:</span><span class="sxs-lookup"><span data-stu-id="27133-372">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="27133-373">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="27133-373">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="27133-374">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="27133-374">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="27133-375">Включена поддержка семейства адресов IPv6 в ExpressRouteCircuitConnectionConfig (Global Reach).</span><span class="sxs-lookup"><span data-stu-id="27133-375">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="27133-376">Добавлен командлет Set-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="27133-376">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="27133-377">Позволяет выполнять настройку всех существующих свойств, включая IPv6CircuitConnectionProperties.</span><span class="sxs-lookup"><span data-stu-id="27133-377">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="27133-378">Обновлен командлет Add-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="27133-378">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="27133-379">Добавлен еще один необязательный параметр AddressPrefixType для указания семейства адресов префикса адреса.</span><span class="sxs-lookup"><span data-stu-id="27133-379">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="27133-380">Обновлены командлеты для включения параметра времени ожидания для обнаружения неиспользуемых одноранговых узлов (DPD) в подключениях шлюзов виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="27133-380">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="27133-381">New-AzVirtualNetworkGatewayConnection;</span><span class="sxs-lookup"><span data-stu-id="27133-381">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="27133-382">Set-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="27133-382">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="27133-383">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="27133-383">Az.PolicyInsights</span></span>
* <span data-ttu-id="27133-384">Добавлен командлет Start-AzPolicyComplianceScan для запуска проверок соответствия политикам.</span><span class="sxs-lookup"><span data-stu-id="27133-384">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="27133-385">Добавлены версии определения политики, определения набора и назначения в выходные данные командлета Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="27133-385">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="27133-386">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="27133-386">Az.ServiceFabric</span></span>
* <span data-ttu-id="27133-387">Улучшено форматирование и наглядность кода в примерах New-AzServiceFabricCluster.</span><span class="sxs-lookup"><span data-stu-id="27133-387">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="27133-388">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27133-388">Az.Sql</span></span>
* <span data-ttu-id="27133-389">Добавлены командлеты Get-AzSqlInstanceOperation и Stop-AzSqlInstanceOperation.</span><span class="sxs-lookup"><span data-stu-id="27133-389">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="27133-390">Включен аудит учетной записи хранения в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="27133-390">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27133-391">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27133-391">Az.Storage</span></span>
* <span data-ttu-id="27133-392">Добавлено уведомление о критическом изменении для изменения выходных данных командлетов, выполняющих действия с файлами в Azure, в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="27133-392">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="27133-393">Включена поддержка новых имен SKU StandardGZRS, StandardRAGZRS при создании или обновлении учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="27133-393">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="27133-394">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27133-394">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="27133-395">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27133-395">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="27133-396">Добавлена поддержка DataLake 2-го поколения.</span><span class="sxs-lookup"><span data-stu-id="27133-396">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="27133-397">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="27133-397">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="27133-398">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="27133-398">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="27133-399">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="27133-399">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="27133-400">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="27133-400">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="27133-401">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="27133-401">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="27133-402">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="27133-402">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="27133-403">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="27133-403">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="27133-404">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="27133-404">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="27133-405">0.10.0-preview — апрель 2020 г.</span><span class="sxs-lookup"><span data-stu-id="27133-405">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="27133-406">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="27133-406">General</span></span>
* <span data-ttu-id="27133-407">Модуль Az стали доступными в предварительной версии в Azure Stack Hub.</span><span class="sxs-lookup"><span data-stu-id="27133-407">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="27133-408">Это обеспечивает кросс-платформенную совместимость с Linux и macOs.</span><span class="sxs-lookup"><span data-stu-id="27133-408">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="27133-409">Azure Stack Hub теперь поддерживает PowerShell Core с модулями Az (см. [дополнительные сведения](https://aka.ms/az4AzureStack))</span><span class="sxs-lookup"><span data-stu-id="27133-409">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="27133-410">Модули Az поддерживают профиль 2019-03-01-hybrid:</span><span class="sxs-lookup"><span data-stu-id="27133-410">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="27133-411">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="27133-411">Az.Billing</span></span>
  - <span data-ttu-id="27133-412">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27133-412">Az.Compute</span></span>
  - <span data-ttu-id="27133-413">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="27133-413">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="27133-414">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="27133-414">Az.EventHub</span></span>
  - <span data-ttu-id="27133-415">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="27133-415">Az.IotHub</span></span>
  - <span data-ttu-id="27133-416">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27133-416">Az.KeyVault</span></span>
  - <span data-ttu-id="27133-417">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27133-417">Az.Monitor</span></span>
  - <span data-ttu-id="27133-418">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27133-418">Az.Network</span></span>
  - <span data-ttu-id="27133-419">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27133-419">Az.Resources</span></span>
  - <span data-ttu-id="27133-420">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27133-420">Az.Storage</span></span>
  - <span data-ttu-id="27133-421">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27133-421">Az.Websites</span></span>
* <span data-ttu-id="27133-422">В PowerShell появились три новых модуля Az, которые работают с Azure Stack Hub: Az.Databox, Az.IotHub и Az.EventHub.</span><span class="sxs-lookup"><span data-stu-id="27133-422">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="27133-423">Команды остаются прежними же за исключением незначительных изменений, таких как изменение AzureRM на Az.</span><span class="sxs-lookup"><span data-stu-id="27133-423">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="27133-424">См. обновленную ссылку на документацию по [PowerShell для Azure Stack Hub](https://aka.ms/InstallASHPowerShell)</span><span class="sxs-lookup"><span data-stu-id="27133-424">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="27133-425">3.7.0 — март 2020 г.</span><span class="sxs-lookup"><span data-stu-id="27133-425">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27133-426">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27133-426">Az.Accounts</span></span>
* <span data-ttu-id="27133-427">Исправлено исключение NullReferenceException командлетов Get-AzTenant/Get-AzDefault/Set-AzDefault, если вход не выполнен [10292]</span><span class="sxs-lookup"><span data-stu-id="27133-427">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27133-428">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27133-428">Az.Compute</span></span>
* <span data-ttu-id="27133-429">Добавлены следующие параметры к командлету New-AzDiskConfig:</span><span class="sxs-lookup"><span data-stu-id="27133-429">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="27133-430">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="27133-430">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="27133-431">Разрешено свойство Encryption для параметра Target командлета New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="27133-431">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="27133-432">Исправлена проблема с tempDisk для командлетов Set-AzVmss -Reimage и Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="27133-432">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="27133-433">[11354]</span><span class="sxs-lookup"><span data-stu-id="27133-433">[#11354]</span></span>
* <span data-ttu-id="27133-434">Добавлена поддержка нового расширения SAP для указанных ниже командлетов</span><span class="sxs-lookup"><span data-stu-id="27133-434">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="27133-435">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="27133-435">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="27133-436">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="27133-436">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="27133-437">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="27133-437">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="27133-438">Update-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="27133-438">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="27133-439">Исправлены ошибки в примерах справки</span><span class="sxs-lookup"><span data-stu-id="27133-439">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="27133-440">Показано точное строковое значение в табличном формате для свойства PowerState виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="27133-440">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="27133-441">New-AzVmssConfig: исправлена сериализация свойства AutomaticRepairs, если параметр SinglePlacementGroup отключен.</span><span class="sxs-lookup"><span data-stu-id="27133-441">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="27133-442">[11257]</span><span class="sxs-lookup"><span data-stu-id="27133-442">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27133-443">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27133-443">Az.DataFactory</span></span>
* <span data-ttu-id="27133-444">Пакет SDK ADF для .NET обновлен до версии 4.8.0.</span><span class="sxs-lookup"><span data-stu-id="27133-444">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="27133-445">Добавлены необязательные параметры для команды Invoke-AzDataFactoryV2Pipeline для поддержки повторного запуска.</span><span class="sxs-lookup"><span data-stu-id="27133-445">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="27133-446">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27133-446">Az.DataLakeStore</span></span>
* <span data-ttu-id="27133-447">Добавлено описание критического изменения для Export-AzDataLakeStoreItem и Import-AzDataLakeStoreItem.</span><span class="sxs-lookup"><span data-stu-id="27133-447">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="27133-448">Добавлен параметр кодирования байтов для New-AzDataLakeStoreItem, Add-AzDAtaLakeStoreItemContent и Get-AzDAtaLakeStoreItemContent.</span><span class="sxs-lookup"><span data-stu-id="27133-448">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="27133-449">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="27133-449">Az.HDInsight</span></span>
* <span data-ttu-id="27133-450">Добавлена поддержка указания минимальной поддерживаемой версии TLS при создании кластера.</span><span class="sxs-lookup"><span data-stu-id="27133-450">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="27133-451">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="27133-451">Az.IotHub</span></span>
* <span data-ttu-id="27133-452">Добавлена поддержка для управления распределенными параметрами на отдельных устройствах.</span><span class="sxs-lookup"><span data-stu-id="27133-452">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="27133-453">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="27133-453">New Cmdlets are:</span></span>
    - <span data-ttu-id="27133-454">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="27133-454">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="27133-455">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="27133-455">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="27133-456">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27133-456">Az.KeyVault</span></span>
* <span data-ttu-id="27133-457">Добавлены атрибуты критических изменений для New-AzKeyVault.</span><span class="sxs-lookup"><span data-stu-id="27133-457">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27133-458">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27133-458">Az.Monitor</span></span>
* <span data-ttu-id="27133-459">Обновлена документация для New-AzScheduledQueryRuleLogMetricTrigger.</span><span class="sxs-lookup"><span data-stu-id="27133-459">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27133-460">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27133-460">Az.Network</span></span>
* <span data-ttu-id="27133-461">Обновлены командлеты для поддержки подключений VirtualHubVnetConnections между клиентами</span><span class="sxs-lookup"><span data-stu-id="27133-461">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="27133-462">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="27133-462">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="27133-463">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="27133-463">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="27133-464">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="27133-464">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="27133-465">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="27133-465">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="27133-466">Удалена зависимость пакета SDK для управления SQL.</span><span class="sxs-lookup"><span data-stu-id="27133-466">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="27133-467">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="27133-467">Az.PolicyInsights</span></span>
* <span data-ttu-id="27133-468">Улучшены сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="27133-468">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27133-469">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27133-469">Az.RecoveryServices</span></span>
* <span data-ttu-id="27133-470">В Azure Site Recovery реализована поддержка повторной защиты и обновлены свойства зашифрованных виртуальных машин диска Azure.</span><span class="sxs-lookup"><span data-stu-id="27133-470">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="27133-471">Добавлена возможность мониторинг аварийного восстановления для свойств VmwareToAzure в Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="27133-471">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="27133-472">В Azure Backup реализована поддержка повторного обновления политики для элементов с ошибками.</span><span class="sxs-lookup"><span data-stu-id="27133-472">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="27133-473">В Azure Backup реализована поддержка параметров исключения диска во время резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="27133-473">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="27133-474">В Azure Backup реализована поддержка восстановления нескольких файлов или папок в AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="27133-474">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="27133-475">В Azure Backup реализована поддержка указанной пользователем группы Resourcegroup при обновлении политики IaasVM.</span><span class="sxs-lookup"><span data-stu-id="27133-475">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="27133-476">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27133-476">Az.Resources</span></span>
* <span data-ttu-id="27133-477">Исправлена команда Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType для использования фактической версии apiVersion ресурсов (а не версии apiVersion по умолчанию) [11267].</span><span class="sxs-lookup"><span data-stu-id="27133-477">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="27133-478">Добавлена возможность регистрации correlationId для сценариев с ошибками.</span><span class="sxs-lookup"><span data-stu-id="27133-478">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="27133-479">Незначительно изменена документация по Get-AzResourceLock.</span><span class="sxs-lookup"><span data-stu-id="27133-479">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="27133-480">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="27133-480">Added example.</span></span>
* <span data-ttu-id="27133-481">Экранирована одинарная кавычка в значении параметра Get-AzADUser [11317].</span><span class="sxs-lookup"><span data-stu-id="27133-481">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="27133-482">Добавлены новые командлеты для сценариев развертывания (Get-AzDeploymentScript, Get-AzDeploymentScriptLog, Save-AzDeploymentScriptLog, Remove-AzDeploymentScript).</span><span class="sxs-lookup"><span data-stu-id="27133-482">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="27133-483">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27133-483">Az.Sql</span></span>
* <span data-ttu-id="27133-484">Добавлен параметр вторичной реплики для чтения для командлета Invoke-AzSqlDatabaseFailover.</span><span class="sxs-lookup"><span data-stu-id="27133-484">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="27133-485">Добавлен командлет Disable-AzSqlServerActiveDirectoryOnlyAuthentication.</span><span class="sxs-lookup"><span data-stu-id="27133-485">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="27133-486">Сохранен приоритет конфиденциальности при классификации столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="27133-486">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="27133-487">Az.Support</span><span class="sxs-lookup"><span data-stu-id="27133-487">Az.Support</span></span>
* <span data-ttu-id="27133-488">Модуль Az.Support стал общедоступным.</span><span class="sxs-lookup"><span data-stu-id="27133-488">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27133-489">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27133-489">Az.Websites</span></span>
* <span data-ttu-id="27133-490">Реализована поддержка работы с правилами маршрутизации трафика веб-приложения через указанные ниже командлеты</span><span class="sxs-lookup"><span data-stu-id="27133-490">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="27133-491">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="27133-491">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="27133-492">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="27133-492">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="27133-493">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="27133-493">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="27133-494">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="27133-494">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="27133-495">3.6.1 — март 2020 г.</span><span class="sxs-lookup"><span data-stu-id="27133-495">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27133-496">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27133-496">Az.Accounts</span></span>
* <span data-ttu-id="27133-497">Открытие страницы опроса Azure PowerShell в Send-Feedback [11020].</span><span class="sxs-lookup"><span data-stu-id="27133-497">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="27133-498">Отображение URL-адреса опроса Azure PowerShell в Resolve-Error [11021].</span><span class="sxs-lookup"><span data-stu-id="27133-498">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="27133-499">Добавлена версия Az в UserAgent.</span><span class="sxs-lookup"><span data-stu-id="27133-499">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="27133-500">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="27133-500">Az.ApiManagement</span></span>
* <span data-ttu-id="27133-501">Включена поддержка получения и настройки личного домена в конечной точке DeveloperPortal [11007].</span><span class="sxs-lookup"><span data-stu-id="27133-501">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="27133-502">Export-AzApiManagementApi: включена поддержка скачивания определения API в формате JSON [9987].</span><span class="sxs-lookup"><span data-stu-id="27133-502">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="27133-503">Import-AzApiManagementApi: включена поддержка импорта определения OpenApi 3.0 из документа JSON.</span><span class="sxs-lookup"><span data-stu-id="27133-503">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="27133-504">New-AzApiManagementIdentityProvider и Set-AzApiManagementIdentityProvider: включена поддержка настройки входа арендатора для поставщика AAD B2C [9784].</span><span class="sxs-lookup"><span data-stu-id="27133-504">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="27133-505">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27133-505">Az.DataLakeStore</span></span>
* <span data-ttu-id="27133-506">Добавлена ссылка на System.Buffers явным образом в CSPROJ и PSD1.</span><span class="sxs-lookup"><span data-stu-id="27133-506">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="27133-507">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="27133-507">Az.IotHub</span></span>
* <span data-ttu-id="27133-508">Добавлена возможность управления устройствами в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="27133-508">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="27133-509">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="27133-509">New Cmdlets are:</span></span>
    - <span data-ttu-id="27133-510">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="27133-510">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="27133-511">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="27133-511">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="27133-512">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="27133-512">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="27133-513">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="27133-513">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="27133-514">Включена поддержка управления модулями в целевом устройстве Интернета вещей в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="27133-514">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="27133-515">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="27133-515">New Cmdlets are:</span></span>
    - <span data-ttu-id="27133-516">Add-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="27133-516">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="27133-517">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="27133-517">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="27133-518">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="27133-518">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="27133-519">Set-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="27133-519">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="27133-520">Добавлен командлет для получения строки подключения целевого устройства Интернета вещей в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="27133-520">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="27133-521">Добавлен командлет для получения строки подключения модуля на целевом устройстве Интернета вещей в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="27133-521">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="27133-522">Включена поддержка для получения или настройки родительского устройства для устройства Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="27133-522">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="27133-523">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="27133-523">New Cmdlets are:</span></span>
    - <span data-ttu-id="27133-524">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="27133-524">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="27133-525">Set-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="27133-525">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="27133-526">Включена поддержка управления связью "родители — потомки" устройства.</span><span class="sxs-lookup"><span data-stu-id="27133-526">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27133-527">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27133-527">Az.Monitor</span></span>
* <span data-ttu-id="27133-528">Исправлено выходное значение для Get-AzMetricDefinition [9714].</span><span class="sxs-lookup"><span data-stu-id="27133-528">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27133-529">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27133-529">Az.Network</span></span>
* <span data-ttu-id="27133-530">Обновлен пакет SDK для управления SQL.</span><span class="sxs-lookup"><span data-stu-id="27133-530">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="27133-531">Исправлена проблема с разницей в именовании в классе PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="27133-531">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="27133-532">Сопоставление ActionsRequired с ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="27133-532">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="27133-533">Добавление PublicNetworkAccess в команды New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="27133-533">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="27133-534">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27133-534">Az.Resources</span></span>
* <span data-ttu-id="27133-535">Исправлена ошибка пустой ссылки в Get-AzRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="27133-535">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="27133-536">Параметры -Force и -PassThru помечены необязательными в Remove-AzADGroup [10849].</span><span class="sxs-lookup"><span data-stu-id="27133-536">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="27133-537">Исправлена ошибка, из-за которой MailNickname не возвращается в Remove-AzADGroup [11167].</span><span class="sxs-lookup"><span data-stu-id="27133-537">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="27133-538">Исправлена ошибка, из-за которой операция канала Remove-AzADGroup не работает [11171].</span><span class="sxs-lookup"><span data-stu-id="27133-538">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="27133-539">Исправлена ошибка с пустой ссылкой в GetAzureRoleAssignmentCommand.</span><span class="sxs-lookup"><span data-stu-id="27133-539">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="27133-540">Добавлено критическое изменение атрибутов для будущих изменений командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="27133-540">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="27133-541">Обновлена команда Get-AzResourceGroup для выполнения фильтрации тегов группы ресурсов на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="27133-541">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="27133-542">Расширены командлеты Tag для включения поддержки параметра -ResourceId.</span><span class="sxs-lookup"><span data-stu-id="27133-542">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="27133-543">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="27133-543">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="27133-544">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="27133-544">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="27133-545">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="27133-545">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="27133-546">Добавлен новый командлет Tag.</span><span class="sxs-lookup"><span data-stu-id="27133-546">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="27133-547">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="27133-547">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="27133-548">Предоставляется ScopedDeployment из пакета SDK 3.3.0.</span><span class="sxs-lookup"><span data-stu-id="27133-548">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="27133-549">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27133-549">Az.Sql</span></span>
* <span data-ttu-id="27133-550">Добавление PublicNetworkAccess в команды New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="27133-550">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="27133-551">Включена поддержка конфигурации резервного копирования долгосрочного хранения для управляемых баз данных.</span><span class="sxs-lookup"><span data-stu-id="27133-551">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="27133-552">Получение или настройка политики LTR в управляемой базе данных.</span><span class="sxs-lookup"><span data-stu-id="27133-552">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="27133-553">Получение резервных копий LTR по управляемой базе данных, управляемому экземпляру или расположению.</span><span class="sxs-lookup"><span data-stu-id="27133-553">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="27133-554">Удаление резервной копии LTR.</span><span class="sxs-lookup"><span data-stu-id="27133-554">Remove an LTR backup</span></span>
    - <span data-ttu-id="27133-555">Восстановление резервной копии LTR для создания новой управляемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="27133-555">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="27133-556">Добавление MinimalTlsVersion в New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="27133-556">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="27133-557">Добавление MinimalTlsVersion в New-AzSqlInstance и Set-AzSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="27133-557">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="27133-558">Обновлена версия пакета SDK для SQL для Az.Network.</span><span class="sxs-lookup"><span data-stu-id="27133-558">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27133-559">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27133-559">Az.Storage</span></span>
* <span data-ttu-id="27133-560">Включена поддержка AllowProtectedAppendWrite в ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="27133-560">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="27133-561">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="27133-561">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="27133-562">Добавлено предупреждение о критическом изменении для изменения типа AzureStorageTable в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="27133-562">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="27133-563">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="27133-563">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="27133-564">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="27133-564">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27133-565">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27133-565">Az.Websites</span></span>
* <span data-ttu-id="27133-566">Добавлен параметр Tag для New-AzAppServicePlan и Set-AzAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="27133-566">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="27133-567">Завершение выполнения командлета, если при добавлении личного домена на веб-сайт возникает исключение.</span><span class="sxs-lookup"><span data-stu-id="27133-567">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="27133-568">Включена поддержка выполнения операций для Служб приложений, которые находятся не в той же группе ресурсов, что и план службы приложений.</span><span class="sxs-lookup"><span data-stu-id="27133-568">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="27133-569">Применение ограничения доступа к WebApp/Function в разных группах ресурсов.</span><span class="sxs-lookup"><span data-stu-id="27133-569">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="27133-570">Исправлена ошибка с указанием пользовательских имен узлов для WebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="27133-570">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="27133-571">3.5.0 — февраль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="27133-571">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="27133-572">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="27133-572">Highlights since the last major release</span></span>
* <span data-ttu-id="27133-573">Обновлены данные телеметрии на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="27133-573">Updated client side telemetry.</span></span>
* <span data-ttu-id="27133-574">В Az.IotHub добавлены командлеты для управления устройствами.</span><span class="sxs-lookup"><span data-stu-id="27133-574">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="27133-575">В Az.SqlVirtualMachine добавлены командлеты для прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="27133-575">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="27133-576">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27133-576">Az.Accounts</span></span>
* <span data-ttu-id="27133-577">В данные телеметрии на стороне клиента добавлены такие сведения, как идентификатор подписки, идентификатор арендатора и время выполнения.</span><span class="sxs-lookup"><span data-stu-id="27133-577">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="27133-578">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="27133-578">Az.Automation</span></span>
* <span data-ttu-id="27133-579">Исправлена опечатка в примере 1 в справочной документации по New-AzAutomationSoftwareUpdateConfiguration.</span><span class="sxs-lookup"><span data-stu-id="27133-579">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="27133-580">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="27133-580">Az.CognitiveServices</span></span>
* <span data-ttu-id="27133-581">Обновлен пакет SDK до версии 7.0.</span><span class="sxs-lookup"><span data-stu-id="27133-581">Updated SDK to 7.0</span></span>
* <span data-ttu-id="27133-582">Улучшено сообщение об ошибке, которое появляется, если ответы сервера не содержат текст.</span><span class="sxs-lookup"><span data-stu-id="27133-582">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27133-583">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27133-583">Az.Compute</span></span>
* <span data-ttu-id="27133-584">Разрешено использовать пустое значение для ProximityPlacementGroupId во время обновления.</span><span class="sxs-lookup"><span data-stu-id="27133-584">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="27133-585">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="27133-585">Az.FrontDoor</span></span>
* <span data-ttu-id="27133-586">Добавлен командлет для получения определений управляемых правил, которые могут использоваться в WAF.</span><span class="sxs-lookup"><span data-stu-id="27133-586">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="27133-587">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="27133-587">Az.IotHub</span></span>
* <span data-ttu-id="27133-588">Добавлена возможность управления устройствами в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="27133-588">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="27133-589">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="27133-589">New Cmdlets are:</span></span>
    - <span data-ttu-id="27133-590">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="27133-590">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="27133-591">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="27133-591">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="27133-592">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="27133-592">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="27133-593">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="27133-593">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="27133-594">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27133-594">Az.KeyVault</span></span>
* <span data-ttu-id="27133-595">Устранен дублирующийся текст для Add-AzKeyVaultKey.md.</span><span class="sxs-lookup"><span data-stu-id="27133-595">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27133-596">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27133-596">Az.Monitor</span></span>
* <span data-ttu-id="27133-597">Исправлено описание командлета Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="27133-597">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="27133-598">В команду New-AzMetricAlertRuleV2 добавлен новый параметр ActionGroupId.</span><span class="sxs-lookup"><span data-stu-id="27133-598">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="27133-599">Пользователь может предоставить ActionGroupId(string) или ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="27133-599">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27133-600">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27133-600">Az.Network</span></span>
* <span data-ttu-id="27133-601">Добавлен еще один параметр -EnableProxyProtocol для командлета New-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="27133-601">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="27133-602">Исправлен пример FilterData в Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="27133-602">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="27133-603">Добавлен пример Packet Capture для всех внутренних и внешних пакетов в Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="27133-603">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="27133-604">Добавлена поддерживаемая политика Брандмауэра Azure в брандмауэрах виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="27133-604">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="27133-605">Новые командлеты не добавлены.</span><span class="sxs-lookup"><span data-stu-id="27133-605">No new cmdlets are added.</span></span> <span data-ttu-id="27133-606">Снято ограничение политики брандмауэра в брандмауэрах виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="27133-606">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27133-607">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27133-607">Az.RecoveryServices</span></span>
* <span data-ttu-id="27133-608">Добавлена возможность восстановления в виде файлов для Баз данных SQL.</span><span class="sxs-lookup"><span data-stu-id="27133-608">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="27133-609">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27133-609">Az.Resources</span></span>
* <span data-ttu-id="27133-610">Выполнен рефакторинг командлетов развертывания шаблона.</span><span class="sxs-lookup"><span data-stu-id="27133-610">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="27133-611">Добавлены новые командлеты для управления развертываниями в группе управления: \*-AzManagementGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="27133-611">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="27133-612">Добавлены новые командлеты для управления развертываниями в области арендатора: \*-AzTenantDeployment.</span><span class="sxs-lookup"><span data-stu-id="27133-612">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="27133-613">Выполнен рефакторинг командлетов \*-AzDeployment для работы в области подписки.</span><span class="sxs-lookup"><span data-stu-id="27133-613">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="27133-614">Созданы псевдонимы \*-AzSubscriptionDeployment для командлетов \*-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="27133-614">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="27133-615">Исправлен командлет Update-AzADApplication, когда параметр AvailableToOtherTenants не задан.</span><span class="sxs-lookup"><span data-stu-id="27133-615">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="27133-616">Удален набор параметров ApplicationObjectWithoutCredentialParameterSet, чтобы предотвратить возникновение AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="27133-616">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="27133-617">Повторно созданы файлы справки.</span><span class="sxs-lookup"><span data-stu-id="27133-617">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="27133-618">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27133-618">Az.Sql</span></span>
* <span data-ttu-id="27133-619">Добавлена возможность восстановления точки во времени между подписками в Управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="27133-619">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="27133-620">Добавлена возможность изменения существующего поколения оборудования Управляемого экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="27133-620">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="27133-621">Исправлены примеры справки Update-AzSqlServerVulnerabilityAssessmentSetting: выходные данные параметра и свойства — EmailAdmins.</span><span class="sxs-lookup"><span data-stu-id="27133-621">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="27133-622">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="27133-622">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="27133-623">Добавлены командлеты для прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="27133-623">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="27133-624">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="27133-624">Az.StorageSync</span></span>
* <span data-ttu-id="27133-625">В командлете Invoke-AzStorageSyncCompatibilityCheck обновлены поддерживаемые наборы символов.</span><span class="sxs-lookup"><span data-stu-id="27133-625">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="27133-626">3.4.0 — февраль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="27133-626">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="27133-627">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="27133-627">Highlights since the last major release</span></span>
* <span data-ttu-id="27133-628">Выпущена первоначальная версия 0.1.0 Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="27133-628">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="27133-629">Добавлена поддержка Az.Network ConnectionMonitor V2</span><span class="sxs-lookup"><span data-stu-id="27133-629">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="27133-630">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27133-630">Az.Accounts</span></span>
* <span data-ttu-id="27133-631">Отключить автоматическое сохранение контекста, если AzureRmContext.json недоступен</span><span class="sxs-lookup"><span data-stu-id="27133-631">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="27133-632">Обновление ссылки на Azure Powershell Common до предварительной версии 1.3.5</span><span class="sxs-lookup"><span data-stu-id="27133-632">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="27133-633">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="27133-633">Az.ApiManagement</span></span>
* <span data-ttu-id="27133-634">**Get-AzApiManagementApiSchema** Исправлено получение схемы Open-API, связанной с API https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="27133-634">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="27133-635">**New-AzApiManagementProduct**\* и **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="27133-635">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="27133-636">Исправить документацию для https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="27133-636">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="27133-637">**Set-AzApiManagementApi** Добавлен пример, показывающий, как обновить ServiceUrl с помощью командлета</span><span class="sxs-lookup"><span data-stu-id="27133-637">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27133-638">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27133-638">Az.Compute</span></span>
* <span data-ttu-id="27133-639">Ограничение числа состояний виртуальных машин до 100, чтобы избежать регулирования при выполнении Get-AzVM-Status без имени виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="27133-639">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="27133-640">Добавление обновления командлета -AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="27133-640">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="27133-641">Добавление параметров EncryptionType и DiskEncryptionSetId в следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="27133-641">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="27133-642">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="27133-642">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="27133-643">Добавление параметра ColocationStatus в командлет Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="27133-643">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27133-644">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27133-644">Az.DataFactory</span></span>
* <span data-ttu-id="27133-645">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.7.0.</span><span class="sxs-lookup"><span data-stu-id="27133-645">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="27133-646">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="27133-646">Az.DeploymentManager</span></span>
* <span data-ttu-id="27133-647">Добавляет операции LIST для ресурсов</span><span class="sxs-lookup"><span data-stu-id="27133-647">Adds LIST operations for resources</span></span>
* <span data-ttu-id="27133-648">Добавляет возможность выполнения операций на этапах Проверки работоспособности</span><span class="sxs-lookup"><span data-stu-id="27133-648">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="27133-649">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="27133-649">Az.HDInsight</span></span>
* <span data-ttu-id="27133-650">Исправление ошибки в документе New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="27133-650">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="27133-651">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27133-651">Az.KeyVault</span></span>
* <span data-ttu-id="27133-652">Добавление Псевдонимов имени в атрибут VaultName, чтобы Remove-AzureKeyVault соответствовал New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="27133-652">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27133-653">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27133-653">Az.Network</span></span>
* <span data-ttu-id="27133-654">В Set-AzNetworkWatcherConfigFlowLog.md добавлен новый пример для демонстрации сценария отключения Аналитики трафика.</span><span class="sxs-lookup"><span data-stu-id="27133-654">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="27133-655">Добавление поддержки назначения IP-конфигурации для брандмауэра Azure — выделенная подсеть и общедоступный IP-адрес, которые брандмауэр будет использовать для управления трафиком</span><span class="sxs-lookup"><span data-stu-id="27133-655">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="27133-656">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="27133-656">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="27133-657">добавлен параметр — ManagementPublicIpAddress (необязательный), который принимает объект общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="27133-657">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="27133-658">Добавлен метод SetManagementIpConfiguration для объекта брандмауэра — в качестве входных данных требуется подсеть и общедоступный IP-адрес — имя подсети должно быть "AzureFirewallManagementSubnet"</span><span class="sxs-lookup"><span data-stu-id="27133-658">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="27133-659">Исправлены примеры Get-AzNetworkSecurityGroup для отображения примеров для группы безопасности сети (NSG) вместо сетевых интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="27133-659">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="27133-660">Исправлена опечатка в команде New-AzVpnSite, которая препятствовала завершению параметра идентификатором ресурса.</span><span class="sxs-lookup"><span data-stu-id="27133-660">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="27133-661">Добавлена поддержка конфигурации в наборе действий для правил подстановки URL-адресов в шлюзе приложения.</span><span class="sxs-lookup"><span data-stu-id="27133-661">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="27133-662">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="27133-662">New cmdlets added:</span></span>
        - <span data-ttu-id="27133-663">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="27133-663">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="27133-664">В следующие командлеты добавлен необязательный параметр — UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="27133-664">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="27133-665">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="27133-665">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="27133-666">Добавление поддержки для ресурсов NetworkWatcher ConnectionMonitor версии 2</span><span class="sxs-lookup"><span data-stu-id="27133-666">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="27133-667">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="27133-667">Az.PolicyInsights</span></span>
* <span data-ttu-id="27133-668">Поддержка оценки соответствия до определения того, какой ресурс нужно исправить</span><span class="sxs-lookup"><span data-stu-id="27133-668">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="27133-669">Добавление параметра "—ResourceDiscoverMode" в Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="27133-669">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="27133-670">Добавление командлета Get-AzPolicyMetadata для получения ресурсов метаданных политики</span><span class="sxs-lookup"><span data-stu-id="27133-670">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="27133-671">Get-AzPolicyState и Get-AzPolicyStateSummary обновлены для API версии 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="27133-671">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27133-672">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27133-672">Az.RecoveryServices</span></span>
* <span data-ttu-id="27133-673">Поддержка Azure Site Recovery для удаления реплицированного диска.</span><span class="sxs-lookup"><span data-stu-id="27133-673">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="27133-674">В Azure Backup добавлена ​​поддержка добавления тегов при создании Хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="27133-674">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="27133-675">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27133-675">Az.Resources</span></span>
* <span data-ttu-id="27133-676">Сделайте команду "Область" необязательной в командлетах \*—AzPolicyAssignment с настройкой по умолчанию для контекстной подписки</span><span class="sxs-lookup"><span data-stu-id="27133-676">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="27133-677">Добавление примеров создания ADServicePrincipal с паролем и ключом учетных данных</span><span class="sxs-lookup"><span data-stu-id="27133-677">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="27133-678">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27133-678">Az.Sql</span></span>
<span data-ttu-id="27133-679">Исправление командлета New-AzSqlDatabaseSecondary, чтобы проверить существование PartnerDatabaseName, а не DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="27133-679">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27133-680">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27133-680">Az.Storage</span></span>
* <span data-ttu-id="27133-681">Поддержка набора шифрования типа ключа таблиц и очередей в создании учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="27133-681">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="27133-682">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27133-682">New-AzStorageAccount</span></span>
* <span data-ttu-id="27133-683">Представление RequestId, если StorageException не имеет ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="27133-683">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="27133-684">Исправление примера 6 командлета Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="27133-684">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27133-685">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27133-685">Az.Websites</span></span>
* <span data-ttu-id="27133-686">Set-AzWebapp и Set-AzWebappSlot поддерживают свойства AlwaysOn, MinTls и FtpsState</span><span class="sxs-lookup"><span data-stu-id="27133-686">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="27133-687">Устранение проблемы, при которой параметр HttpsOnly с одновременным изменением AppservicePlan с помощью одной команды Set-AzWebApp сбрасывал значение HttpsOnly до значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="27133-687">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="27133-688">3.3.0 — январь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="27133-688">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27133-689">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27133-689">Az.Accounts</span></span>
* <span data-ttu-id="27133-690">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment: теперь они принимают параметры AzureAttestationServiceEndpointResourceId и AzureAttestationServiceEndpointSuffix.</span><span class="sxs-lookup"><span data-stu-id="27133-690">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="27133-691">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="27133-691">Az.Cdn</span></span>
* <span data-ttu-id="27133-692">Теперь в командлете New-AzCdnEndpoint отображаются сведения из сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="27133-692">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27133-693">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27133-693">Az.Compute</span></span>
* <span data-ttu-id="27133-694">Командлет Set-AzVMCustomScriptExtension исправлен для виртуальной машины с управляемым диском ОС без профиля ОС.</span><span class="sxs-lookup"><span data-stu-id="27133-694">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="27133-695">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="27133-695">Az.ContainerInstance</span></span>
* <span data-ttu-id="27133-696">Исправлены имена параметров, используемые в примере командлета New-AzContainerGroup.</span><span class="sxs-lookup"><span data-stu-id="27133-696">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="27133-697">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="27133-697">Az.DataBoxEdge</span></span>
* <span data-ttu-id="27133-698">Добавлен командлет Get-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="27133-698">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="27133-699">получение контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="27133-699">Get the Edge Storage Container</span></span>
* <span data-ttu-id="27133-700">Добавлен командлет New-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="27133-700">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="27133-701">создание контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="27133-701">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="27133-702">Добавлен командлет Remove-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="27133-702">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="27133-703">удаление контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="27133-703">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="27133-704">Добавлен командлет Invoke-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="27133-704">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="27133-705">вызов действия для обновления данных в контейнере хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="27133-705">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="27133-706">Добавлен командлет Get-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="27133-706">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="27133-707">получение учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="27133-707">Get the Edge Storage Account</span></span>
* <span data-ttu-id="27133-708">Добавлен командлет New-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="27133-708">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="27133-709">создание учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="27133-709">Create new Edge Storage Account</span></span>
* <span data-ttu-id="27133-710">Добавлен командлет Remove-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="27133-710">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="27133-711">удаление учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="27133-711">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="27133-712">Вызов командлета Invoke-AzDataBoxEdgeShare:</span><span class="sxs-lookup"><span data-stu-id="27133-712">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="27133-713">вызов действия для обновления данных в общей папке.</span><span class="sxs-lookup"><span data-stu-id="27133-713">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="27133-714">Добавлен командлет Set-AzDataBoxEdgeStorageAccountCredential:</span><span class="sxs-lookup"><span data-stu-id="27133-714">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="27133-715">установка учетных данных для учетной записи хранилища Azure Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="27133-715">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27133-716">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27133-716">Az.DataFactory</span></span>
* <span data-ttu-id="27133-717">Добавлены свойства AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId и VersionStatus для командлета Get-AzDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="27133-717">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="27133-718">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.6.0.</span><span class="sxs-lookup"><span data-stu-id="27133-718">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="27133-719">Для командлета Set-AzureRmDataFactoryV2IntegrationRuntime добавлен параметр PublicIPs, позволяющий включить создание среды Azure-SSIS IR со статическими общедоступными IP-адресами.</span><span class="sxs-lookup"><span data-stu-id="27133-719">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="27133-720">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="27133-720">Az.DevTestLabs</span></span>
* <span data-ttu-id="27133-721">Удалена недействительная ссылка в файле Get-AzDtlAllowedVMSizesPolicy.md.</span><span class="sxs-lookup"><span data-stu-id="27133-721">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="27133-722">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="27133-722">Az.EventHub</span></span>
* <span data-ttu-id="27133-723">Устранена проблема № 10634: исправлена ссылка на пустой объект для удаления пространства имен концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="27133-723">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="27133-724">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="27133-724">Az.HDInsight</span></span>
* <span data-ttu-id="27133-725">Устранена ошибка в файле Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="27133-725">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="27133-726">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="27133-726">Az.MachineLearning</span></span>
* <span data-ttu-id="27133-727">Вычислительная среда Машинного обучения больше недоступна, поэтому удалены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="27133-727">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="27133-728">Get-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="27133-728">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="27133-729">Get-AzMlOpClusterKey;</span><span class="sxs-lookup"><span data-stu-id="27133-729">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="27133-730">New-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="27133-730">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="27133-731">Remove-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="27133-731">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="27133-732">Set-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="27133-732">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="27133-733">Test-AzMlOpClusterSystemServicesUpdateAvailability;</span><span class="sxs-lookup"><span data-stu-id="27133-733">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="27133-734">Update-AzMlOpClusterSystemService.</span><span class="sxs-lookup"><span data-stu-id="27133-734">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27133-735">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27133-735">Az.Network</span></span>
* <span data-ttu-id="27133-736">Обновлена зависимость Microsoft.Azure.Management.Sql от предварительной версии 1.36 до предварительной версии 1.37.</span><span class="sxs-lookup"><span data-stu-id="27133-736">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27133-737">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27133-737">Az.RecoveryServices</span></span>
* <span data-ttu-id="27133-738">Добавлена поддержка Azure Site Recovery для виртуальных машин с управляемым диском, зашифрованных при хранении с помощью управляемых клиентом ключей, при восстановлении из Azure в поставщике Azure.</span><span class="sxs-lookup"><span data-stu-id="27133-738">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="27133-739">Добавлена поддержка Azure Site Recovery для необязательного ввода идентификатора набора шифрования диска при включении защиты в рамках восстановления из VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="27133-739">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="27133-740">Добавлена поддержка Azure Site Recovery для необязательного ввода идентификатора набора шифрования диска на уровне диска при включении защиты в рамках восстановления из VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="27133-740">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="27133-741">Добавлена поддержка Azure Site Recovery для обновления элемента, защищенного репликацией, путем сопоставления набора шифрования диска при восстановлении из HyperV в Azure.</span><span class="sxs-lookup"><span data-stu-id="27133-741">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="27133-742">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27133-742">Az.Resources</span></span>
* <span data-ttu-id="27133-743">Исправлена ошибка в справочном документе о командлете Remove-AzTag.</span><span class="sxs-lookup"><span data-stu-id="27133-743">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="27133-744">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27133-744">Az.Sql</span></span>
* <span data-ttu-id="27133-745">Исправлена функция основных командлетов установки оценки уязвимостей: теперь она позволяет работать с базой данных master для базы данных Azure и ограничить ее в системных базах данных управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="27133-745">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="27133-746">Устранена ошибка, возникающая при создании группы отработки отказа экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="27133-746">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="27133-747">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="27133-747">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="27133-748">Добавлен новый допустимый тип лицензии: DR (аварийное восстановление).</span><span class="sxs-lookup"><span data-stu-id="27133-748">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27133-749">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27133-749">Az.Storage</span></span>
* <span data-ttu-id="27133-750">Добавлено предупреждающее сообщение о критическом изменении значения DefaultAction в следующем выпуске:</span><span class="sxs-lookup"><span data-stu-id="27133-750">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="27133-751">Update-AzStorageAccountNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="27133-751">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="27133-752">Включена поддержка получения времени последней синхронизации учетной записи хранения путем выполнения командлета Get-AzureRmStorageAccount с параметром -IncludeGeoReplicationStats:</span><span class="sxs-lookup"><span data-stu-id="27133-752">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="27133-753">Get-AzureRmStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="27133-753">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="27133-754">3.2.0 — декабрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="27133-754">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="27133-755">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="27133-755">General</span></span>
* <span data-ttu-id="27133-756">Обновление ссылок в .psd1 для использования относительного пути для всех модулей.</span><span class="sxs-lookup"><span data-stu-id="27133-756">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="27133-757">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27133-757">Az.Accounts</span></span>
* <span data-ttu-id="27133-758">Установка правильного параметра UserAgent для телеметрии на стороне клиента для Az 4.0 (предварительная версия).</span><span class="sxs-lookup"><span data-stu-id="27133-758">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="27133-759">Отображение понятного пользователю сообщения об ошибке, если в Az 4.0 (предварительная версия) не указан контекст.</span><span class="sxs-lookup"><span data-stu-id="27133-759">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="27133-760">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="27133-760">Az.Batch</span></span>
* <span data-ttu-id="27133-761">Исправлена проблема [№ 10602](https://github.com/Azure/azure-powershell/issues/10602), из-за которой использование командлета **New-AzBatchPool** приводило к неправильной отправке VirtualMachineConfiguration.ContainerConfiguration или VirtualMachineConfiguration.DataDisks на сервер.</span><span class="sxs-lookup"><span data-stu-id="27133-761">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27133-762">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27133-762">Az.DataFactory</span></span>
* <span data-ttu-id="27133-763">Обновление пакета SDK Фабрики данных для .NET до версии 4.5.0.</span><span class="sxs-lookup"><span data-stu-id="27133-763">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="27133-764">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="27133-764">Az.FrontDoor</span></span>
* <span data-ttu-id="27133-765">Включена поддержка исключений управляемых правил WAF.</span><span class="sxs-lookup"><span data-stu-id="27133-765">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="27133-766">Добавление SocketAddr в список автозавершения.</span><span class="sxs-lookup"><span data-stu-id="27133-766">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="27133-767">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="27133-767">Az.HealthcareApis</span></span>
* <span data-ttu-id="27133-768">Обработка исключений.</span><span class="sxs-lookup"><span data-stu-id="27133-768">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="27133-769">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27133-769">Az.KeyVault</span></span>
* <span data-ttu-id="27133-770">Исправлена ошибка при получении доступа к значению, которое может быть не задано.</span><span class="sxs-lookup"><span data-stu-id="27133-770">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="27133-771">Управление сертификатами шифрования на основе эллиптических кривых.</span><span class="sxs-lookup"><span data-stu-id="27133-771">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="27133-772">Включена возможность указания кривой для политик сертификатов.</span><span class="sxs-lookup"><span data-stu-id="27133-772">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27133-773">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27133-773">Az.Monitor</span></span>
* <span data-ttu-id="27133-774">Добавление необязательного аргумента в команду добавления параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="27133-774">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="27133-775">Существующий аргумент switch указывает на то, что экспорт в Log Analytics должен выполняться в фиксированную схему</span><span class="sxs-lookup"><span data-stu-id="27133-775">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="27133-776">(выделенный тип данных).</span><span class="sxs-lookup"><span data-stu-id="27133-776">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27133-777">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27133-777">Az.Network</span></span>
* <span data-ttu-id="27133-778">В приложении AzureFirewall, NAT и сетевых правилах включена поддержка IpGroups.</span><span class="sxs-lookup"><span data-stu-id="27133-778">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="27133-779">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27133-779">Az.Resources</span></span>
* <span data-ttu-id="27133-780">Устранена проблема, из-за которой при развертывании шаблона не удавалось считать его параметр, если имя параметра конфликтовало с именем встроенного параметра.</span><span class="sxs-lookup"><span data-stu-id="27133-780">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="27133-781">Обновлены командлеты политики для использования новой версии API 2019-09-01 с поддержкой группирования в определениях наборов политик.</span><span class="sxs-lookup"><span data-stu-id="27133-781">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="27133-782">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27133-782">Az.Sql</span></span>
* <span data-ttu-id="27133-783">Обновлена функция автоматического создания расширенного хранилища для службы оценки уязвимостей в учетной записи StorageV2.</span><span class="sxs-lookup"><span data-stu-id="27133-783">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27133-784">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27133-784">Az.Storage</span></span>
* <span data-ttu-id="27133-785">Включена поддержка создания маркера SAS на основе удостоверения контейнера и большого двоичного объекта с аутентификацией Oauth на основе контекста службы хранилища:</span><span class="sxs-lookup"><span data-stu-id="27133-785">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="27133-786">New-AzStorageContainerSASToken;</span><span class="sxs-lookup"><span data-stu-id="27133-786">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="27133-787">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="27133-787">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="27133-788">Отозвана поддержка ключей делегирования пользователя учетной записи хранения, а также всех маркеров SAS удостоверения:</span><span class="sxs-lookup"><span data-stu-id="27133-788">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="27133-789">Revoke-AzStorageAccountUserDelegationKeys.</span><span class="sxs-lookup"><span data-stu-id="27133-789">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="27133-790">Выполнено обновление до Microsoft.Azure.Management.Storage версии 14.2.0 для включения поддержки нового API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="27133-790">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="27133-791">Включена поддержка QuotaGiB (квота общего ресурса в ГиБ) для значений свыше 5120 в командлетах для работы с общими папками в плоскости управления и добавлен псевдоним Quota для параметра QuotaGiB.</span><span class="sxs-lookup"><span data-stu-id="27133-791">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="27133-792">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="27133-792">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="27133-793">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="27133-793">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="27133-794">Добавлен псевдоним QuotaGiB для параметра Quota:</span><span class="sxs-lookup"><span data-stu-id="27133-794">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="27133-795">Set-AzStorageShareQuota.</span><span class="sxs-lookup"><span data-stu-id="27133-795">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="27133-796">Устранена проблема, из-за которой при использовании AzStorageContainerAcl могла очищаться хранимая политика доступа:</span><span class="sxs-lookup"><span data-stu-id="27133-796">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="27133-797">Set-AzStorageContainerAcl.</span><span class="sxs-lookup"><span data-stu-id="27133-797">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="27133-798">Версия 3.1.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="27133-798">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="27133-799">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="27133-799">Highlights since the last major release</span></span>
* <span data-ttu-id="27133-800">Выпуск Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="27133-800">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="27133-801">Выпуск Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="27133-801">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27133-802">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27133-802">Az.Compute</span></span>
* <span data-ttu-id="27133-803">Функция повторного применения виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="27133-803">VM Reapply feature</span></span>
    - <span data-ttu-id="27133-804">Добавлен параметр повторного применения в командлет Set-AzVM.</span><span class="sxs-lookup"><span data-stu-id="27133-804">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="27133-805">Функция AutomaticRepairs масштабируемого набора виртуальных машин:</span><span class="sxs-lookup"><span data-stu-id="27133-805">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="27133-806">Добавлены параметры EnableAutomaticRepair, AutomaticRepairGracePeriod и AutomaticRepairMaxInstanceRepairsPercent в следующие командлеты:   New-AzVmssConfig Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="27133-806">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="27133-807">Включена поддержка образа из коллекции разных клиентов для New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="27133-807">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="27133-808">Добавлен фрагмент Spot в средство заполнения аргументов параметра Priority в командлетах New-AzVM, New-AzVMConfig и New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="27133-808">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="27133-809">Добавлены параметры DiskIOPSReadWrite и DiskMBpsReadWrite в командлет Add-AzVmssDataDisk.</span><span class="sxs-lookup"><span data-stu-id="27133-809">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="27133-810">Изменен параметр SourceImageId командлета New-AzGalleryImageVersion на необязательный.</span><span class="sxs-lookup"><span data-stu-id="27133-810">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="27133-811">Добавлены параметры OSDiskImage и DataDiskImage в командлет New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="27133-811">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="27133-812">Добавлен параметр HyperVGeneration в командлет New-AzGalleryImageDefinition.</span><span class="sxs-lookup"><span data-stu-id="27133-812">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="27133-813">Добавлены параметры SkipExtensionsOnOverprovisionedVMs в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="27133-813">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="27133-814">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="27133-814">Az.DataBoxEdge</span></span>
* <span data-ttu-id="27133-815">Добавлен командлет `Get-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="27133-815">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="27133-816">Получение заказа.</span><span class="sxs-lookup"><span data-stu-id="27133-816">Get the Order</span></span>
* <span data-ttu-id="27133-817">Добавлен командлет `New-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="27133-817">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="27133-818">Создание заказа.</span><span class="sxs-lookup"><span data-stu-id="27133-818">Create new Order</span></span>
* <span data-ttu-id="27133-819">Добавлен командлет `Remove-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="27133-819">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="27133-820">Удаление заказа.</span><span class="sxs-lookup"><span data-stu-id="27133-820">Remove the Order</span></span>
* <span data-ttu-id="27133-821">Изменен командлет `New-AzDataBoxEdgeShare`.</span><span class="sxs-lookup"><span data-stu-id="27133-821">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="27133-822">Создание локальной общей папки.</span><span class="sxs-lookup"><span data-stu-id="27133-822">Now creates Local Share</span></span>
* <span data-ttu-id="27133-823">Добавлен командлет `Set-AzDataBoxEdgeRole`.</span><span class="sxs-lookup"><span data-stu-id="27133-823">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="27133-824">Сопоставление IotRole с общей папкой.</span><span class="sxs-lookup"><span data-stu-id="27133-824">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="27133-825">Добавлен командлет `Invoke-AzDataBoxEdgeDevice`.</span><span class="sxs-lookup"><span data-stu-id="27133-825">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="27133-826">Вызов проверки обновлений, скачивание обновления, установка обновления на устройстве.</span><span class="sxs-lookup"><span data-stu-id="27133-826">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="27133-827">Добавлен командлет `Get-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="27133-827">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="27133-828">Получение сведений о триггерах.</span><span class="sxs-lookup"><span data-stu-id="27133-828">Gets the information about Triggers</span></span>
* <span data-ttu-id="27133-829">Добавлен командлет `New-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="27133-829">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="27133-830">Создание триггеров.</span><span class="sxs-lookup"><span data-stu-id="27133-830">Create new Triggers</span></span>
* <span data-ttu-id="27133-831">Добавлен командлет `Remove-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="27133-831">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="27133-832">Удаление триггеров.</span><span class="sxs-lookup"><span data-stu-id="27133-832">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27133-833">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27133-833">Az.DataFactory</span></span>
* <span data-ttu-id="27133-834">Обновление пакета SDK Фабрики данных для .NET до версии 4.4.0.</span><span class="sxs-lookup"><span data-stu-id="27133-834">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="27133-835">Добавлен параметр ExpressCustomSetup в командлет Set-AzureRmDataFactoryV2IntegrationRuntime для включения конфигураций установки и сторонних компонентов без использования настраиваемого скрипта установки.</span><span class="sxs-lookup"><span data-stu-id="27133-835">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="27133-836">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27133-836">Az.DataLakeStore</span></span>
* <span data-ttu-id="27133-837">Обновлена документация по Get-AzDataLakeStoreDeletedItem и Restore-AzDataLakeStoreDeletedItem.</span><span class="sxs-lookup"><span data-stu-id="27133-837">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="27133-838">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="27133-838">Az.EventHub</span></span>
* <span data-ttu-id="27133-839">Исправлена проблема № 10301. Исправлен формат даты маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="27133-839">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="27133-840">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="27133-840">Az.FrontDoor</span></span>
* <span data-ttu-id="27133-841">Добавлен параметр MinimumTlsVersion в Enable-AzFrontDoorCustomDomainHttps и New-AzFrontDoorFrontendEndpointObject.</span><span class="sxs-lookup"><span data-stu-id="27133-841">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="27133-842">Добавлены параметры HealthProbeMethod и EnabledState в New-AzFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="27133-842">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="27133-843">Добавлен новый командлет для создания объекта BackendPoolsSettings для передачи при создании и обновлении Front Door.</span><span class="sxs-lookup"><span data-stu-id="27133-843">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="27133-844">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="27133-844">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27133-845">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27133-845">Az.Network</span></span>
* <span data-ttu-id="27133-846">Изменены примеры параметра FilterData Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="27133-846">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="27133-847">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="27133-847">Az.PrivateDns</span></span>
* <span data-ttu-id="27133-848">Пакет SDK PrivateDns для .NET обновлен до версии 1.0.0</span><span class="sxs-lookup"><span data-stu-id="27133-848">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27133-849">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27133-849">Az.RecoveryServices</span></span>
* <span data-ttu-id="27133-850">Включена поддержка Azure Site Recovery для выбора типа диска при включении защиты.</span><span class="sxs-lookup"><span data-stu-id="27133-850">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="27133-851">Внесено исправление Azure Site Recovery для изменения действия плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="27133-851">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="27133-852">Включена поддержка восстановления SQL Azure Backup для принятия баз данных файлового потока.</span><span class="sxs-lookup"><span data-stu-id="27133-852">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="27133-853">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="27133-853">Az.RedisCache</span></span>
* <span data-ttu-id="27133-854">Добавлен параметр MinimumTlsVersion в командлеты New-AzRedisCache и Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="27133-854">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="27133-855">Кроме того, добавлен параметр MinimumTlsVersion в выходные данные командлета Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="27133-855">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="27133-856">Добавлена проверка параметра -Size для командлетов Set-AzRedisCache и New-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="27133-856">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="27133-857">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27133-857">Az.Resources</span></span>
- <span data-ttu-id="27133-858">Обновлены командлеты политики для использования новой версии API 2019-06-01 с новым свойством EnforcementMode в назначении политики.</span><span class="sxs-lookup"><span data-stu-id="27133-858">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="27133-859">Обновлен пример справки по созданию определения политики</span><span class="sxs-lookup"><span data-stu-id="27133-859">Updated create policy definition help example</span></span>
- <span data-ttu-id="27133-860">Исправлена ошибка с параметром -ServicePrincipalName командлета Remove-AZADServicePrincipal с возвратом пустой ссылки, если имя субъекта службы не найдено.</span><span class="sxs-lookup"><span data-stu-id="27133-860">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="27133-861">Исправлена ошибка с New-AZADServicePrincipal с возвратом пустой ссылки, если у клиента нет подписки.</span><span class="sxs-lookup"><span data-stu-id="27133-861">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="27133-862">Изменен командлет New-AzAdServicePrincipal для добавления учетных данных только для связанного приложения.</span><span class="sxs-lookup"><span data-stu-id="27133-862">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="27133-863">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27133-863">Az.Sql</span></span>
* <span data-ttu-id="27133-864">Добавлена поддержка ReadReplicaCount для базы данных.</span><span class="sxs-lookup"><span data-stu-id="27133-864">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="27133-865">Исправлена ошибка с Set-AzSqlDatabase, если избыточность в пределах зоны не настроена.</span><span class="sxs-lookup"><span data-stu-id="27133-865">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="27133-866">Версия 3.0.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="27133-866">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="27133-867">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="27133-867">General</span></span>
* <span data-ttu-id="27133-868">Выпущена версия Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="27133-868">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="27133-869">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27133-869">Az.Accounts</span></span>
* <span data-ttu-id="27133-870">Добавлено сообщение об устаревании для псевдонима "Resolve-Error".</span><span class="sxs-lookup"><span data-stu-id="27133-870">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="27133-871">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="27133-871">Az.Advisor</span></span>
* <span data-ttu-id="27133-872">Добавлена новая категория Operational Excellence (Эффективность работы) в командлет Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="27133-872">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="27133-873">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="27133-873">Az.Batch</span></span>
* <span data-ttu-id="27133-874">`CoreQuota` в `BatchAccountContext` переименован в `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="27133-874">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="27133-875">Также появился новый `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="27133-875">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="27133-876">Это влияет на **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="27133-876">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="27133-877">Параметр **New-AzBatchTask** `-ResourceFile` теперь принимает коллекцию объектов `PSResourceFile`, которые можно создать с помощью нового командлета **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="27133-877">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="27133-878">Новый командлет **New-AzBatchResourceFile**, который помогает создавать объекты `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="27133-878">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="27133-879">Их можно передавать в **New-AzBatchTask** в параметре `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="27133-879">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="27133-880">Это позволяет поддерживать два новых типа файлов ресурсов, которые дополняют существующий метод `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="27133-880">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="27133-881">Файлы ресурсов на основе `AutoStorageContainerName` скачивают весь контейнер автоматического хранения в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="27133-881">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="27133-882">Файлы ресурсов на основе `StorageContainerUrl` скачивают указанный в URL-адресе контейнер в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="27133-882">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="27133-883">Удалено свойство `ApplicationPackages` в `PSApplication`, который возвращается из **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="27133-883">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="27133-884">Отдельные пакеты в приложении теперь можно извлечь с помощью **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="27133-884">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="27133-885">Например: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="27133-885">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="27133-886">`ApplicationId` переименован в `ApplicationName` для **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** и **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="27133-886">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="27133-887">Теперь `ApplicationId` является псевдонимом для `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="27133-887">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="27133-888">Добавлено новое свойство `PSWindowsUserConfiguration` в `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="27133-888">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="27133-889">`Version` переименован в `Name` для `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="27133-889">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="27133-890">`BlobSource` переименован в `HttpUrl` для `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="27133-890">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="27133-891">Удалено свойство `OSDisk` из `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="27133-891">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="27133-892">Удалена операция **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="27133-892">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="27133-893">Больше она не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="27133-893">This operation is no longer supported.</span></span>
* <span data-ttu-id="27133-894">Удалено `TargetOSVersion` из `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="27133-894">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="27133-895">`CurrentOSVersion` переименован в `OSVersion` для `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="27133-895">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="27133-896">Удалено `DataEgressGiB` и `DataIngressGiB` из `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="27133-896">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="27133-897">Операция **Get-AzBatchNodeAgentSku** удалена и заменена на **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="27133-897">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="27133-898">**Get-AzBatchSupportedImage** возвращает те же данные, что и **Get-AzBatchNodeAgentSku**, но в более удобном формате.</span><span class="sxs-lookup"><span data-stu-id="27133-898">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="27133-899">Также возвращаются новые непроверенные образы.</span><span class="sxs-lookup"><span data-stu-id="27133-899">New non-verified images are also now returned.</span></span> <span data-ttu-id="27133-900">Включается и дополнительная информация о `Capabilities` и `BatchSupportEndOfLife` для каждого образа.</span><span class="sxs-lookup"><span data-stu-id="27133-900">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="27133-901">Добавлена возможность монтировать файловые системы на каждом узле пула с помощью нового параметра `MountConfiguration` в **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="27133-901">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="27133-902">Теперь поддерживаются правила безопасности сети, которые блокируют сетевой доступ к пулу по исходящему порту трафика.</span><span class="sxs-lookup"><span data-stu-id="27133-902">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="27133-903">Это выполняется с помощью свойства `SourcePortRanges` для `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="27133-903">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="27133-904">Что касается выполнения контейнеров, пакетная служба теперь поддерживает выполнение задачи в рабочей папке контейнера или рабочей папке задачи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="27133-904">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="27133-905">Выбор зависит от параметра `WorkingDirectory` в `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="27133-905">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="27133-906">Добавлена возможность указать коллекцию общедоступных IP-адресов для `PSNetworkConfiguration` с помощью нового свойства `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="27133-906">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="27133-907">Это гарантирует, что узлы в пуле будут иметь IP-адреса из списка, предоставленного пользователем.</span><span class="sxs-lookup"><span data-stu-id="27133-907">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="27133-908">Если значение не задано, по умолчанию для `WaitForSuccess` в `PSSTartTask` используется значение `$True` (ранее `$False`).</span><span class="sxs-lookup"><span data-stu-id="27133-908">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="27133-909">Если значение не задано, по умолчанию для `Scope` в `PSAutoUserSpecification` используется значение `Pool` (ранее `Task` для Windows или `Pool` для Linux).</span><span class="sxs-lookup"><span data-stu-id="27133-909">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="27133-910">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="27133-910">Az.Cdn</span></span>
* <span data-ttu-id="27133-911">Добавлены UrlRewriteAction и CacheKeyQueryStringAction в RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="27133-911">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="27133-912">Исправлено несколько ошибок, таких как отсутствующий входной параметр Selector в командлете New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="27133-912">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27133-913">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27133-913">Az.Compute</span></span>
* <span data-ttu-id="27133-914">Функция набора шифрования диска</span><span class="sxs-lookup"><span data-stu-id="27133-914">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="27133-915">Новые командлеты:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="27133-915">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="27133-916">Добавлен параметр ProximityPlacementGroupId в следующие командлеты:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="27133-916">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="27133-917">Параметры DiskEncryptionSetId и EncryptionType добавлены в следующие командлеты:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="27133-917">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="27133-918">Добавлен параметр PublicIPAddressVersion в New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="27133-918">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="27133-919">FileUris для расширения пользовательских скриптов теперь будет защищенным, а не общедоступным параметром</span><span class="sxs-lookup"><span data-stu-id="27133-919">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="27133-920">Добавлено ScaleInPolicy в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="27133-920">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="27133-921">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="27133-921">Breaking changes</span></span>
    - <span data-ttu-id="27133-922">Параметр UploadSizeInBytes применяется теперь вместо DiskSizeGB для New-AzDiskConfig, если CreateOption имеет значение Upload</span><span class="sxs-lookup"><span data-stu-id="27133-922">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="27133-923">PublishingProfile.Source.ManagedImage.Id заменяется на StorageProfile.Source.Id в объекте GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="27133-923">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27133-924">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27133-924">Az.DataFactory</span></span>
* <span data-ttu-id="27133-925">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.3.0.</span><span class="sxs-lookup"><span data-stu-id="27133-925">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="27133-926">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27133-926">Az.DataLakeStore</span></span>
* <span data-ttu-id="27133-927">Обновлен пакет SDK для ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), включает следующие исправления</span><span class="sxs-lookup"><span data-stu-id="27133-927">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="27133-928">Не создается исключение при невозможности десериализовать значение времени создания для записи в корзине или каталоге.</span><span class="sxs-lookup"><span data-stu-id="27133-928">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="27133-929">Предоставляется параметр для времени ожидания запроса в adlsclient</span><span class="sxs-lookup"><span data-stu-id="27133-929">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="27133-930">Исправлена передача исходного значения syncflag для восстановления badoffset</span><span class="sxs-lookup"><span data-stu-id="27133-930">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="27133-931">Исправлена операция EnumerateDirectory, чтобы она извлекала токен продолжения после проверки ответа</span><span class="sxs-lookup"><span data-stu-id="27133-931">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="27133-932">Исправлена ошибка объединения</span><span class="sxs-lookup"><span data-stu-id="27133-932">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="27133-933">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="27133-933">Az.FrontDoor</span></span>
* <span data-ttu-id="27133-934">Исправлены разные опечатки в разных частях модуля</span><span class="sxs-lookup"><span data-stu-id="27133-934">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="27133-935">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="27133-935">Az.HDInsight</span></span>
* <span data-ttu-id="27133-936">Исправлена ошибка, из-за которой клиент получал сообщение об ошибке 'Not a valid Base-64 string' (Не является допустимой строкой Base64) при выполнении Get-AzHDInsightCluster для получения кластера с хранилищем ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="27133-936">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="27133-937">Добавлен параметр с именем ApplicationId в три командлета Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig и New-AzHDInsightCluster, чтобы клиент мог предоставить идентификатор приложения субъекта-службы для доступа к Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="27133-937">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="27133-938">Для Microsoft.Azure.Management.HDInsight изменена версия с 2.1.0 на 5.1.0</span><span class="sxs-lookup"><span data-stu-id="27133-938">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="27133-939">Удалены пять командлетов:</span><span class="sxs-lookup"><span data-stu-id="27133-939">Removed five cmdlets:</span></span>
    - <span data-ttu-id="27133-940">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="27133-940">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="27133-941">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="27133-941">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="27133-942">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="27133-942">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="27133-943">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="27133-943">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="27133-944">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="27133-944">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="27133-945">Добавлены три командлета:</span><span class="sxs-lookup"><span data-stu-id="27133-945">Added three cmdlets:</span></span>
    - <span data-ttu-id="27133-946">Get-AzHDInsightMonitoring заменяет собой Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="27133-946">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="27133-947">Enable-AzHDInsightMonitoring заменяет собой Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="27133-947">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="27133-948">Disable-AzHDInsightMonitoring заменяет собой Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="27133-948">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="27133-949">Исправлен командлет Get-AzHDInsightProperties, чтобы он поддерживал получение сведений о возможностях из определенного расположения.</span><span class="sxs-lookup"><span data-stu-id="27133-949">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="27133-950">Удалены наборы параметров ("Spark1", "Spark2") из Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="27133-950">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="27133-951">Добавлены примеры в справочные документы по командлету Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="27133-951">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="27133-952">Изменен тип выходных данных для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="27133-952">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="27133-953">Для Get-AzHDInsightProperties тип выходных данных изменен с CapabilitiesResponse на AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="27133-953">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="27133-954">Для Remove-AzHDInsightCluster тип выходных данных изменен с ClusterGetResponse на bool.</span><span class="sxs-lookup"><span data-stu-id="27133-954">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="27133-955">Для Set-AzHDInsightGatewaySettings тип выходных данных изменен с HttpConnectivitySettings на GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="27133-955">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="27133-956">Добавлены несколько условий для проверки сценариев.</span><span class="sxs-lookup"><span data-stu-id="27133-956">Added some scenario test cases.</span></span>
* <span data-ttu-id="27133-957">Удалены несколько псевдонимов: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="27133-957">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="27133-958">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="27133-958">Az.IotHub</span></span>
* <span data-ttu-id="27133-959">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="27133-959">Breaking changes:</span></span>
    - <span data-ttu-id="27133-960">Командлет Add-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="27133-960">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="27133-961">Удален набор параметров __AllParameterSets для командлета Add-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="27133-961">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="27133-962">Командлет Get-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="27133-962">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="27133-963">Удален набор параметров __AllParameterSets для командлета Get-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="27133-963">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="27133-964">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties.</span><span class="sxs-lookup"><span data-stu-id="27133-964">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="27133-965">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties.</span><span class="sxs-lookup"><span data-stu-id="27133-965">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="27133-966">Командлет New-AzIotHubExportDevice больше не поддерживает псевдоним New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="27133-966">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="27133-967">Командлет New-AzIotHubImportDevice больше не поддерживает псевдоним New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="27133-967">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="27133-968">Командлет Remove-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="27133-968">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="27133-969">Удален набор параметров __AllParameterSets для командлета Remove-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="27133-969">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="27133-970">Командлет Set-AzIotHub теперь не поддерживает параметр OperationsMonitoringProperties и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="27133-970">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="27133-971">Удален набор параметров UpdateOperationsMonitoringProperties для командлета Set-AzIotHub.</span><span class="sxs-lookup"><span data-stu-id="27133-971">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27133-972">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27133-972">Az.RecoveryServices</span></span>
* <span data-ttu-id="27133-973">Azure Site Recovery поддерживает настройку сетевых ресурсов, например групп безопасности сети, общедоступных IP-адресов и внутренних подсистем балансировки нагрузки из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="27133-973">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="27133-974">Azure Site Recovery поддерживает запись на управляемый диск из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="27133-974">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="27133-975">Azure Site Recovery поддерживает сокращение NIC из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="27133-975">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="27133-976">Azure Site Recovery поддерживает ускорение сети NIC из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="27133-976">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="27133-977">Azure Site Recovery поддерживает автоматическое обновление агента из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="27133-977">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="27133-978">Azure Site Recovery поддерживает стандартный SSD-накопитель из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="27133-978">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="27133-979">Azure Site Recovery поддерживает двухпроходное шифрование диска Azure из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="27133-979">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="27133-980">Azure Site Recovery поддерживает новый добавленный диск из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="27133-980">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="27133-981">Добавлена функция SoftDelete для виртуальных машин и соответствующие тесты</span><span class="sxs-lookup"><span data-stu-id="27133-981">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="27133-982">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27133-982">Az.Resources</span></span>
* <span data-ttu-id="27133-983">Обновлена сборка зависимостей Microsoft.Extensions.Caching.Memory с версии 1.1.1 до 2.2</span><span class="sxs-lookup"><span data-stu-id="27133-983">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27133-984">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27133-984">Az.Network</span></span>
* <span data-ttu-id="27133-985">Изменены все командлеты для PrivateEndpointConnection, чтобы они поддерживали универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="27133-985">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="27133-986">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="27133-986">Updated cmdlet:</span></span>
        - <span data-ttu-id="27133-987">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="27133-987">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="27133-988">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="27133-988">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="27133-989">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="27133-989">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="27133-990">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="27133-990">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="27133-991">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="27133-991">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="27133-992">Добавлен новый командлет для PrivateLinkResource, который поддерживает универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="27133-992">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="27133-993">Новый командлет</span><span class="sxs-lookup"><span data-stu-id="27133-993">New cmdlet:</span></span>
        - <span data-ttu-id="27133-994">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="27133-994">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="27133-995">Добавлены новые поля и параметр для протокола прокси версии 2.</span><span class="sxs-lookup"><span data-stu-id="27133-995">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="27133-996">Добавлено свойство EnableProxyProtocol в PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="27133-996">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="27133-997">Добавлено свойство LinkIdentifier в PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="27133-997">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="27133-998">Обновлен New-AzPrivateLinkService для поддержки нового необязательного параметра EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="27133-998">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="27133-999">Исправлено описание параметра в справочной документации по командлету New-AzApplicationGatewaySku.</span><span class="sxs-lookup"><span data-stu-id="27133-999">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="27133-1000">Новые командлеты для поддержки политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="27133-1000">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="27133-1001">Добавлена поддержка дочерних ресурсов RouteTables для VirtualHub</span><span class="sxs-lookup"><span data-stu-id="27133-1001">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="27133-1002">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="27133-1002">New cmdlets added:</span></span>
        - <span data-ttu-id="27133-1003">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="27133-1003">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="27133-1004">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="27133-1004">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="27133-1005">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="27133-1005">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="27133-1006">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="27133-1006">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="27133-1007">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="27133-1007">Set-AzVirtualHub</span></span>
* <span data-ttu-id="27133-1008">Добавлена поддержка новых свойств SKU для VirtualHub и VirtualWANType в VirtualWan</span><span class="sxs-lookup"><span data-stu-id="27133-1008">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="27133-1009">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="27133-1009">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="27133-1010">New-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="27133-1010">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="27133-1011">Update-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="27133-1011">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="27133-1012">New-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="27133-1012">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="27133-1013">Update-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="27133-1013">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="27133-1014">Добавлена поддержка свойства EnableInternetSecurity для HubVnetConnection, VpnConnection и ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="27133-1014">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="27133-1015">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="27133-1015">New cmdlets added:</span></span>
        - <span data-ttu-id="27133-1016">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="27133-1016">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="27133-1017">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="27133-1017">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="27133-1018">New-AzureRmVirtualHubVnetConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="27133-1018">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="27133-1019">New-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="27133-1019">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="27133-1020">Update-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="27133-1020">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="27133-1021">New-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="27133-1021">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="27133-1022">Set-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="27133-1022">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="27133-1023">Добавлена поддержка настройки политики верхнего уровня WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="27133-1023">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="27133-1024">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="27133-1024">New cmdlets added:</span></span>
        - <span data-ttu-id="27133-1025">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="27133-1025">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="27133-1026">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="27133-1026">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="27133-1027">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="27133-1027">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="27133-1028">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="27133-1028">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="27133-1029">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="27133-1029">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="27133-1030">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="27133-1030">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="27133-1031">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="27133-1031">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="27133-1032">New-AzApplicationGatewayFirewallPolicy: добавлены параметры PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="27133-1032">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="27133-1033">Добавлена поддержка оператора Geo-Match для CustomRule</span><span class="sxs-lookup"><span data-stu-id="27133-1033">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="27133-1034">Добавлен параметр GeoMatch в оператор для FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="27133-1034">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="27133-1035">Добавлена поддержка политики брандмауэра perListener и perSite</span><span class="sxs-lookup"><span data-stu-id="27133-1035">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="27133-1036">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="27133-1036">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="27133-1037">New-AzApplicationGatewayHttpListener: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="27133-1037">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="27133-1038">New-AzApplicationGatewayPathRuleConfig: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="27133-1038">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="27133-1039">Исправлен учет регистра для требуемой подсети с именем AzureBastionSubnet в PSBastion</span><span class="sxs-lookup"><span data-stu-id="27133-1039">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="27133-1040">Поддержка полного доменного имени назначения в правилах сети и преобразованного полного доменного имени в правилах NAT для брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="27133-1040">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="27133-1041">Добавлена поддержка ресурсов верхнего уровня RouteTables для IpGroup</span><span class="sxs-lookup"><span data-stu-id="27133-1041">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="27133-1042">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="27133-1042">New cmdlets added:</span></span>
        - <span data-ttu-id="27133-1043">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="27133-1043">New-AzIpGroup</span></span>
        - <span data-ttu-id="27133-1044">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="27133-1044">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="27133-1045">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="27133-1045">Get-AzIpGroup</span></span>
        - <span data-ttu-id="27133-1046">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="27133-1046">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="27133-1047">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="27133-1047">Az.ServiceFabric</span></span>
* <span data-ttu-id="27133-1048">Удален командлет Add-AzServiceFabricApplicationCertificate, так как соответствующий сценарий выполняется командлетом Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="27133-1048">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="27133-1049">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27133-1049">Az.Sql</span></span>
* <span data-ttu-id="27133-1050">Добавлена поддержка восстановления удаленных баз данных в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="27133-1050">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="27133-1051">Из кода удалены старые командлеты аудита.</span><span class="sxs-lookup"><span data-stu-id="27133-1051">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="27133-1052">Удалены нерекомендуемые псевдонимы:</span><span class="sxs-lookup"><span data-stu-id="27133-1052">Removed deprecated aliases:</span></span>
* <span data-ttu-id="27133-1053">Get-AzSqlDatabaseIndexRecommendations (вместо него используйте Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="27133-1053">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="27133-1054">Get-AzSqlDatabaseRestorePoints (вместо него используйте Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="27133-1054">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="27133-1055">Удален командлет Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="27133-1055">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="27133-1056">Удалены псевдонимы для нерекомендуемых командлетов параметров оценки уязвимостей</span><span class="sxs-lookup"><span data-stu-id="27133-1056">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="27133-1057">Командлеты расширенного обнаружения угроз объявлены устаревшими</span><span class="sxs-lookup"><span data-stu-id="27133-1057">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="27133-1058">Добавлены командлеты для отключения и включения рекомендаций о конфиденциальности для столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="27133-1058">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27133-1059">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27133-1059">Az.Storage</span></span>
* <span data-ttu-id="27133-1060">Поддержка включения большой общей папки при создании или обновлении учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="27133-1060">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="27133-1061">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27133-1061">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="27133-1062">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27133-1062">Set-AzStorageAccount</span></span>
* <span data-ttu-id="27133-1063">При закрытии или получении маркера файла пропускается проверка того, является ли входной путь файлом или каталогом, чтобы избежать сбоев при получении объектов в состоянии DeletePending.</span><span class="sxs-lookup"><span data-stu-id="27133-1063">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="27133-1064">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="27133-1064">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="27133-1065">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="27133-1065">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="27133-1066">2.8.0 — октябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="27133-1066">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="27133-1067">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="27133-1067">General</span></span>
* <span data-ttu-id="27133-1068">Выпуск Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="27133-1068">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="27133-1069">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27133-1069">Az.Accounts</span></span>
* <span data-ttu-id="27133-1070">Обновление телеметрии и перезаписи URL-адресов для созданных модулей, исправление для модульных тестов Windows.</span><span class="sxs-lookup"><span data-stu-id="27133-1070">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="27133-1071">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="27133-1071">Az.ApiManagement</span></span>
* <span data-ttu-id="27133-1072">**Set-AzApiManagementApi** — в ApiVersionSet добавлена поддержка обновления API.</span><span class="sxs-lookup"><span data-stu-id="27133-1072">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="27133-1073">исправлена проблема https://github.com/Azure/azure-powershell/issues/10068.</span><span class="sxs-lookup"><span data-stu-id="27133-1073">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="27133-1074">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="27133-1074">Az.Automation</span></span>
* <span data-ttu-id="27133-1075">Исправлен командлет New-AzureAutomationSoftwareUpdateConfiguration для параметра перезагрузки Linux.</span><span class="sxs-lookup"><span data-stu-id="27133-1075">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="27133-1076">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="27133-1076">Az.Batch</span></span>
* <span data-ttu-id="27133-1077">Командлет **Get-AzBatchNodeAgentSku** объявлен устаревшим и будет заменен на **Get-AzBatchSupportImage** в версии 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="27133-1077">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27133-1078">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27133-1078">Az.Compute</span></span>
* <span data-ttu-id="27133-1079">В командлеты New-AzVM и New-AzVmss добавлены параметры Priority, EvictionPolicy и MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="27133-1079">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="27133-1080">Исправлены предупреждающее сообщение для командлетов Add-AzVMAdditionalUnattendContent и Add-AzVMSshPublicKey и справочная документация по ним.</span><span class="sxs-lookup"><span data-stu-id="27133-1080">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="27133-1081">Для Set-AzVMDiskEncryptionExtension исправлено исключение -skipVmBackup для виртуальных машин Linux с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="27133-1081">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="27133-1082">Исправлена ошибка при изменении параметров шифрования в Set-AzVMDiskEncryptionExtension, реализован двухэтапный сценарий.</span><span class="sxs-lookup"><span data-stu-id="27133-1082">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27133-1083">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27133-1083">Az.DataFactory</span></span>
* <span data-ttu-id="27133-1084">Добавлены команды CRUD для потока данных Фабрики данных Azure версии 2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow и Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="27133-1084">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="27133-1085">Добавлены команды действий для сеанса отладки потока данных Фабрики данных Azure версии 2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand и Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="27133-1085">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="27133-1086">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.2.0.</span><span class="sxs-lookup"><span data-stu-id="27133-1086">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="27133-1087">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27133-1087">Az.DataLakeStore</span></span>
* <span data-ttu-id="27133-1088">Проверка учетной записи исправлена так, чтобы учетные записи, содержащие знак "-", можно было передавать без домена.</span><span class="sxs-lookup"><span data-stu-id="27133-1088">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="27133-1089">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="27133-1089">Az.HealthcareApis</span></span>
* <span data-ttu-id="27133-1090">Версия PowerShell обновлена до 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="27133-1090">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="27133-1091">Версия пакета SDK обновлена до 1.0.2.</span><span class="sxs-lookup"><span data-stu-id="27133-1091">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="27133-1092">В тестах обновлены ссылки на новую версию пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="27133-1092">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="27133-1093">Вложенная выходная структура заменена на плоскую.</span><span class="sxs-lookup"><span data-stu-id="27133-1093">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="27133-1094">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="27133-1094">Az.IotHub</span></span>
* <span data-ttu-id="27133-1095">Добавлен новый источник маршрутизации DigitalTwinChangeEvents.</span><span class="sxs-lookup"><span data-stu-id="27133-1095">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="27133-1096">Исправлены незначительные ошибки: Get-AzIothub не возвращает subscriptionId.</span><span class="sxs-lookup"><span data-stu-id="27133-1096">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27133-1097">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27133-1097">Az.Monitor</span></span>
* <span data-ttu-id="27133-1098">Добавлены новые получатели групп действий: -ItsmReceiver, -VoiceReceiver, -ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver.</span><span class="sxs-lookup"><span data-stu-id="27133-1098">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="27133-1099">Для получателей включите общую схему оповещений.</span><span class="sxs-lookup"><span data-stu-id="27133-1099">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="27133-1100">Это не касается получателей SMS, push-уведомлений приложения Azure, ITSM и голосовых сообщений.</span><span class="sxs-lookup"><span data-stu-id="27133-1100">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="27133-1101">Веб-перехватчики теперь поддерживают аутентификацию Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="27133-1101">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27133-1102">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27133-1102">Az.Network</span></span>
* <span data-ttu-id="27133-1103">Добавлен новый командлет Get-AzAvailableServiceAlias, позволяющий получить псевдонимы для политик конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="27133-1103">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="27133-1104">В подключениях шлюза виртуальной сети появилась возможность добавлять селекторы трафика.</span><span class="sxs-lookup"><span data-stu-id="27133-1104">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="27133-1105">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="27133-1105">New cmdlets added:</span></span>
        - <span data-ttu-id="27133-1106">New-AzureRmTrafficSelectorPolicy.</span><span class="sxs-lookup"><span data-stu-id="27133-1106">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="27133-1107">В командлеты добавлены необязательные параметры -TrafficSelectorPolicies, -New-AzureRmVirtualNetworkGatewayConnection, -Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="27133-1107">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="27133-1108">В конфигурациях правил сетевой безопасности добавлена поддержка протоколов ESP и AH.</span><span class="sxs-lookup"><span data-stu-id="27133-1108">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="27133-1109">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="27133-1109">Updated cmdlets:</span></span>
        - <span data-ttu-id="27133-1110">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="27133-1110">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="27133-1111">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="27133-1111">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="27133-1112">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="27133-1112">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="27133-1113">Улучшена обработка исключений в командлетах Cortex.</span><span class="sxs-lookup"><span data-stu-id="27133-1113">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="27133-1114">Выпущены новые поколения и номера SKU VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="27133-1114">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="27133-1115">Представлены новые поколения VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="27133-1115">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="27133-1116">Представлены новые номера SKU VirtualNetworkGateways с высокой пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="27133-1116">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="27133-1117">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="27133-1117">Az.RedisCache</span></span>
* <span data-ttu-id="27133-1118">В справочную документацию по Set-AzRedisCache добавлены недостающие значения для параметра -Size.</span><span class="sxs-lookup"><span data-stu-id="27133-1118">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="27133-1119">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27133-1119">Az.Sql</span></span>
* <span data-ttu-id="27133-1120">Добавлена возможность назначать администратора Active Directory в Управляемом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="27133-1120">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27133-1121">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27133-1121">Az.Storage</span></span>
* <span data-ttu-id="27133-1122">Клиентская библиотека службы хранилища Azure обновлена до версии 11.1.0.</span><span class="sxs-lookup"><span data-stu-id="27133-1122">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="27133-1123">NextPageLink теперь позволяет получить список контейнеров с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="27133-1123">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="27133-1124">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="27133-1124">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="27133-1125">NextPageLink теперь позволяет получить список учетных записей хранения из подписки.</span><span class="sxs-lookup"><span data-stu-id="27133-1125">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="27133-1126">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27133-1126">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="27133-1127">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="27133-1127">Az.StorageSync</span></span>
* <span data-ttu-id="27133-1128">Исправлена проблема 9810 с Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="27133-1128">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27133-1129">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27133-1129">Az.Websites</span></span>
* <span data-ttu-id="27133-1130">Обновление плана службы приложений с помощью Set-AzWebApp приводило к сбою приложения.</span><span class="sxs-lookup"><span data-stu-id="27133-1130">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="27133-1131">2.7.0 — сентябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="27133-1131">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="27133-1132">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="27133-1132">Az.ApiManagement</span></span>
* <span data-ttu-id="27133-1133">В справочной документации по командлету Set-AzApiManagementPolicy обновлено описание параметра -Format.</span><span class="sxs-lookup"><span data-stu-id="27133-1133">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="27133-1134">Из справочной документации удалены ссылки на нерекомендуемый командлет Update-AzApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="27133-1134">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="27133-1135">Вместо него следует использовать командлет Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="27133-1135">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="27133-1136">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="27133-1136">Az.Automation</span></span>
* <span data-ttu-id="27133-1137">В справочной документации по командлету Register-AzAutomationDscNode исправлена опечатка в примере.</span><span class="sxs-lookup"><span data-stu-id="27133-1137">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="27133-1138">Добавлено уточнение об ограничениях ОС для командлета Register-AzAutomationDSCNode.</span><span class="sxs-lookup"><span data-stu-id="27133-1138">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="27133-1139">Исправлено исключение пустой ссылки для параметра -Wait в командлете Start-AzAutomationRunbook.</span><span class="sxs-lookup"><span data-stu-id="27133-1139">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27133-1140">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27133-1140">Az.Compute</span></span>
* <span data-ttu-id="27133-1141">Добавлен параметр UploadSizeInBytes для командлета New-AzDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="27133-1141">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="27133-1142">Добавлен добавочный параметр для командлета New-AzSnapshotConfig.</span><span class="sxs-lookup"><span data-stu-id="27133-1142">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="27133-1143">Для виртуальной машины добавлены такие функции с низким приоритетом:</span><span class="sxs-lookup"><span data-stu-id="27133-1143">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="27133-1144">Для командлета New-AzVMConfig добавлены параметры MaxPrice, EvictionPolicy и Priority.</span><span class="sxs-lookup"><span data-stu-id="27133-1144">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="27133-1145">Для командлетов New-AzVmssConfig, Update-AzVM и Update-AzVmss добавлен параметр MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="27133-1145">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="27133-1146">Для командлета Get-AzAvailabilitySet устранена проблема со ссылкой на виртуальную машину, когда в нем перечисляются все группы доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="27133-1146">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="27133-1147">Исправлено исключение NULL для командлета Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="27133-1147">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="27133-1148">Исправлен метод поиска VHD для относительной конечной позиции.</span><span class="sxs-lookup"><span data-stu-id="27133-1148">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="27133-1149">Устранена проблема с UltraSSD для командлетов New-AzVM и Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="27133-1149">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27133-1150">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27133-1150">Az.DataFactory</span></span>
* <span data-ttu-id="27133-1151">Добавлены 3 новые команды для ADF версии 2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription и Get-AzDataFactoryV2TriggerSubscriptionStatus.</span><span class="sxs-lookup"><span data-stu-id="27133-1151">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="27133-1152">Пакет SDK ADF для .NET обновлен до версии 4.1.3.</span><span class="sxs-lookup"><span data-stu-id="27133-1152">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="27133-1153">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="27133-1153">Az.HDInsight</span></span>
* <span data-ttu-id="27133-1154">Укажите критические изменения.</span><span class="sxs-lookup"><span data-stu-id="27133-1154">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="27133-1155">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="27133-1155">Az.IotHub</span></span>
* <span data-ttu-id="27133-1156">Добавлена поддержка для вызова отработки отказа для IotHub в георегион аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="27133-1156">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="27133-1157">Добавлена поддержка для управления обогащением сообщений для IotHub.</span><span class="sxs-lookup"><span data-stu-id="27133-1157">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="27133-1158">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="27133-1158">New cmdlets are:</span></span>
    - <span data-ttu-id="27133-1159">Add-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="27133-1159">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="27133-1160">Get-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="27133-1160">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="27133-1161">Remove-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="27133-1161">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="27133-1162">Set-AzIotHubMessageEnrichment.</span><span class="sxs-lookup"><span data-stu-id="27133-1162">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27133-1163">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27133-1163">Az.Monitor</span></span>
* <span data-ttu-id="27133-1164">Указание на самую последнюю версию пакета SDK для монитора, т. е. 0.24.1-preview:</span><span class="sxs-lookup"><span data-stu-id="27133-1164">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="27133-1165">В командлеты метрик добавлены некритические изменения, т. е. перечисление единиц поддерживает несколько новых значений.</span><span class="sxs-lookup"><span data-stu-id="27133-1165">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="27133-1166">Эти командлеты доступны только для чтения, поэтому входные данные командлетов не будут изменены.</span><span class="sxs-lookup"><span data-stu-id="27133-1166">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="27133-1167">Актуальная версия API запросов **ActionGroups** — **2019-06-01**. До этого была версия **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="27133-1167">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="27133-1168">Тесты сценария обновлены в соответствии с этим изменением.</span><span class="sxs-lookup"><span data-stu-id="27133-1168">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="27133-1169">В конструкторы классов **EmailReceiver** и **WebhookReceiver** добавлен один новый обязательный аргумент — логическое значение с именем **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="27133-1169">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="27133-1170">Сейчас для него установлено значение **false**, чтобы скрыть это критическое изменение от командлетов.</span><span class="sxs-lookup"><span data-stu-id="27133-1170">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="27133-1171">**Примечание**. Это временное изменение, которое должно быть подтверждено командой оповещения.</span><span class="sxs-lookup"><span data-stu-id="27133-1171">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="27133-1172">Порядок аргументов для конструктора класса **Source** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="27133-1172">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="27133-1173">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="27133-1173">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="27133-1174">Порядок аргументов для конструктора класса **AlertingAction** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="27133-1174">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="27133-1175">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="27133-1175">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="27133-1176">Добавлена поддержка критериев динамического порога для оповещения метрики версии 2:</span><span class="sxs-lookup"><span data-stu-id="27133-1176">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="27133-1177">New-AzMetricAlertRuleV2Criteria: теперь также позволяет создавать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="27133-1177">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="27133-1178">Add-AzMetricAlertRuleV2: теперь также позволяет принимать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="27133-1178">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="27133-1179">Добавлены усовершенствования в командлетах запланированных правил запросов (SQR).</span><span class="sxs-lookup"><span data-stu-id="27133-1179">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="27133-1180">Командлеты будут принимать параметр Location в обоих форматах: расположение (например, eastus) или отображаемое имя расположения (например, "восточная часть США").</span><span class="sxs-lookup"><span data-stu-id="27133-1180">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="27133-1181">Параметр Enabled проиллюстрирован в файлах справки надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="27133-1181">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="27133-1182">Добавлены примеры для необязательного параметра ActionGroup.</span><span class="sxs-lookup"><span data-stu-id="27133-1182">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="27133-1183">Все файлы справки улучшены.</span><span class="sxs-lookup"><span data-stu-id="27133-1183">Overall improved help files</span></span>
* <span data-ttu-id="27133-1184">Исправлена ошибка в определении типа области для командлета Set-AzActionRule.</span><span class="sxs-lookup"><span data-stu-id="27133-1184">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27133-1185">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27133-1185">Az.Network</span></span>
* <span data-ttu-id="27133-1186">Исправлен неправильный пример в справочной документации по командлету New-AzApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="27133-1186">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="27133-1187">В справочную документацию по командлету Get-AzNetworkWatcherPacketCapture добавлено примечание, посвященное извлечению всех свойств для записи пакетов.</span><span class="sxs-lookup"><span data-stu-id="27133-1187">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="27133-1188">В справочной документации по командлету Test-AzNetworkWatcherIPFlow исправлен пример: теперь он правильно перечисляет сетевые карты.</span><span class="sxs-lookup"><span data-stu-id="27133-1188">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="27133-1189">Улучшен анализ облачных исключений для отображения дополнительных сведений (при их наличии).</span><span class="sxs-lookup"><span data-stu-id="27133-1189">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="27133-1190">Улучшен анализ облачных исключений для обработки дополнительного типа исключения SDK.</span><span class="sxs-lookup"><span data-stu-id="27133-1190">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="27133-1191">Исправлено неправильное сопоставление моделей правил безопасности.</span><span class="sxs-lookup"><span data-stu-id="27133-1191">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="27133-1192">Добавлены свойства сетевого интерфейса для компонента частного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="27133-1192">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="27133-1193">Для интерфейса PSNetworkInterface добавлено свойство PrivateEndpoint с типом PSResourceId.</span><span class="sxs-lookup"><span data-stu-id="27133-1193">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="27133-1194">В PSNetworkInterfaceIPConfiguration добавлено свойство PrivateLinkConnectionProperties с типом PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="27133-1194">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="27133-1195">Добавлен новый класс модели: PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="27133-1195">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="27133-1196">Добавлен новый тип ApplicationRuleProtocolType "mssql" для ресурса Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="27133-1196">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="27133-1197">Поддержка многоканального подключения в Виртуальной глобальной сети:</span><span class="sxs-lookup"><span data-stu-id="27133-1197">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="27133-1198">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="27133-1198">New cmdlets</span></span>
        - <span data-ttu-id="27133-1199">New-AzVpnSiteLink;</span><span class="sxs-lookup"><span data-stu-id="27133-1199">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="27133-1200">New-AzVpnSiteLinkConnection;</span><span class="sxs-lookup"><span data-stu-id="27133-1200">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="27133-1201">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="27133-1201">Updated cmdlet:</span></span>
        - <span data-ttu-id="27133-1202">New-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="27133-1202">New-VpnSite</span></span>
        - <span data-ttu-id="27133-1203">Update-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="27133-1203">Update-VpnSite</span></span>
        - <span data-ttu-id="27133-1204">New-VpnConnection;</span><span class="sxs-lookup"><span data-stu-id="27133-1204">New-VpnConnection</span></span>
        - <span data-ttu-id="27133-1205">Update-VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="27133-1205">Update-VpnConnection</span></span>
* <span data-ttu-id="27133-1206">Исправлены документы с некоторыми примерами PowerShell для использования командлетов AZ вместо командлетов AzureRM.</span><span class="sxs-lookup"><span data-stu-id="27133-1206">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27133-1207">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27133-1207">Az.RecoveryServices</span></span>
* <span data-ttu-id="27133-1208">Для объекта AzureVMpolicy добавлен новый атрибут — ProtectedItemsCount.</span><span class="sxs-lookup"><span data-stu-id="27133-1208">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="27133-1209">Добавлены тесты для политики виртуальной машины и восстановления исходной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="27133-1209">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="27133-1210">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27133-1210">Az.Resources</span></span>
* <span data-ttu-id="27133-1211">Исправлена ошибка, при которой не удавалось вызвать командлет New-AzRoleAssignment без параметра Scope.</span><span class="sxs-lookup"><span data-stu-id="27133-1211">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="27133-1212">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="27133-1212">Az.ServiceFabric</span></span>
* <span data-ttu-id="27133-1213">Исправлена опечатка в примере в справочной документации по командлету Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="27133-1213">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="27133-1214">Добавлены новые командлеты для управления приложениями и службами:</span><span class="sxs-lookup"><span data-stu-id="27133-1214">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="27133-1215">New-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="27133-1215">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="27133-1216">New-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="27133-1216">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="27133-1217">New-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="27133-1217">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="27133-1218">New-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="27133-1218">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="27133-1219">Update-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="27133-1219">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="27133-1220">Get-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="27133-1220">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="27133-1221">Get-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="27133-1221">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="27133-1222">Get-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="27133-1222">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="27133-1223">Get-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="27133-1223">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="27133-1224">Remove-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="27133-1224">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="27133-1225">Remove-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="27133-1225">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="27133-1226">Remove-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="27133-1226">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="27133-1227">Remove-AzServiceFabricServic.</span><span class="sxs-lookup"><span data-stu-id="27133-1227">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="27133-1228">Пакет SDK для Service Fabric обновлен до версии 1.2.0, в которой используется версия API 2019-03-01 поставщика ресурсов Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="27133-1228">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="27133-1229">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="27133-1229">Az.SignalR</span></span>
* <span data-ttu-id="27133-1230">Добавлены командлеты Update, Restart, CheckNameAvailability и GetUsage.</span><span class="sxs-lookup"><span data-stu-id="27133-1230">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="27133-1231">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27133-1231">Az.Sql</span></span>
* <span data-ttu-id="27133-1232">Обновлен пример в справочной документации по командлету Get-AzSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="27133-1232">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="27133-1233">Добавлен пример виртуального ядра для командлета создания эластичного пула (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="27133-1233">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="27133-1234">Удалена проверка свойства EmailAddresses и того, что свойство EmailAdmins правильное в случае, если свойство EmailAddresses пустое в командлетах Set-AzSqlServerAdvancedThreatProtectionPolicy и Set-AzSqlDatabaseAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="27133-1234">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="27133-1235">Теперь, если существует несколько параметров диагностики, включающих категорию аудита, параметры аудита сервера и базы данных удаляются.</span><span class="sxs-lookup"><span data-stu-id="27133-1235">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="27133-1236">Исправлена проверка адресов электронной почты в нескольких командлетах оценки уязвимостей SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting и Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="27133-1236">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27133-1237">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27133-1237">Az.Storage</span></span>
* <span data-ttu-id="27133-1238">Обновлен пример в справочной документации по командлету Get-AzStorageAccountKey.</span><span class="sxs-lookup"><span data-stu-id="27133-1238">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="27133-1239">Теперь при отправке и загрузке файла Azure в конечном файле сохраняются свойства SMB исходного файла (атрибуты файла, время создания файла, время последней записи файла).</span><span class="sxs-lookup"><span data-stu-id="27133-1239">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="27133-1240">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="27133-1240">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="27133-1241">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="27133-1241">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="27133-1242">Исправлена операция отправки блочного BLOB-объекта, в которой происходили сбои свойств и метаданных в контейнере с включенной ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="27133-1242">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="27133-1243">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="27133-1243">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="27133-1244">Добавлена поддержка управления общими папками Azure в API плоскости управления с помощью таких командлетов:</span><span class="sxs-lookup"><span data-stu-id="27133-1244">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="27133-1245">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="27133-1245">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="27133-1246">Get-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="27133-1246">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="27133-1247">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="27133-1247">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="27133-1248">Remove-AzRmStorageShare.</span><span class="sxs-lookup"><span data-stu-id="27133-1248">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27133-1249">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27133-1249">Az.Websites</span></span>
* <span data-ttu-id="27133-1250">Устранена проблема, из-за которой теги webapp удалялись при переносе приложения в новый ASP.</span><span class="sxs-lookup"><span data-stu-id="27133-1250">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="27133-1251">Теперь командлет Publish-AzureWebapp работает в Linux и Windows.</span><span class="sxs-lookup"><span data-stu-id="27133-1251">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="27133-1252">Обновлен пример в справочной документации по командлету Get-AzWebAppPublishingProfile.</span><span class="sxs-lookup"><span data-stu-id="27133-1252">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="27133-1253">2.6.0 — август 2019 г.</span><span class="sxs-lookup"><span data-stu-id="27133-1253">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="27133-1254">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="27133-1254">General</span></span>
* <span data-ttu-id="27133-1255">Исправлены опечатки в модулях.</span><span class="sxs-lookup"><span data-stu-id="27133-1255">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="27133-1256">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27133-1256">Az.Accounts</span></span>
* <span data-ttu-id="27133-1257">Добавлена поддержка назначаемого пользователем удостоверения MSI при проверке подлинности в Функциях Azure (№ 9479).</span><span class="sxs-lookup"><span data-stu-id="27133-1257">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="27133-1258">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="27133-1258">Az.Aks</span></span>
* <span data-ttu-id="27133-1259">Устранена проблема с выходными данными для Get-AzAks.</span><span class="sxs-lookup"><span data-stu-id="27133-1259">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="27133-1260">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9847.</span><span class="sxs-lookup"><span data-stu-id="27133-1260">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="27133-1261">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="27133-1261">Az.ApiManagement</span></span>
* <span data-ttu-id="27133-1262">исправлена проблема https://github.com/Azure/azure-powershell/issues/9351.</span><span class="sxs-lookup"><span data-stu-id="27133-1262">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="27133-1263">Обновлена версия NuGet для .NET, которая не накладывает ограничений на productId, apiId, groupId и userId.</span><span class="sxs-lookup"><span data-stu-id="27133-1263">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="27133-1264">**Get-AzApiManagementProduct**. Добавлена поддержка запросов к продуктам с помощью API.</span><span class="sxs-lookup"><span data-stu-id="27133-1264">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="27133-1265">**New-AzApiManagementApiRevision**. Устранена проблема, из-за которой не задавался параметр ApiRevisionDescription при создании новой редакции API https://github.com/Azure/azure-powershell/issues/9752.</span><span class="sxs-lookup"><span data-stu-id="27133-1265">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="27133-1266">Исправлено написание имени модели c PsApiManagementOAuth2AuthrozationServer на PsApiManagementOAuth2AuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="27133-1266">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="27133-1267">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="27133-1267">Az.Batch</span></span>
* <span data-ttu-id="27133-1268">Исправлена опечатка в написании Windows со строчной буквы в справочных сообщениях и документации.</span><span class="sxs-lookup"><span data-stu-id="27133-1268">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="27133-1269">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="27133-1269">Az.Cdn</span></span>
* <span data-ttu-id="27133-1270">Исправлена опечатка во вспомогательном приложении модуля CDN.</span><span class="sxs-lookup"><span data-stu-id="27133-1270">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27133-1271">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27133-1271">Az.Compute</span></span>
* <span data-ttu-id="27133-1272">Добавлен параметр VmssId в новый командлет Add New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="27133-1272">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="27133-1273">Добавлены параметры TerminateScheduledEvents и TerminateScheduledEventNotBeforeTimeoutInMinutes в New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="27133-1273">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="27133-1274">Добавлено свойство HyperVGeneration в объект образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="27133-1274">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="27133-1275">Добавлены компоненты Host и HostGroup.</span><span class="sxs-lookup"><span data-stu-id="27133-1275">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="27133-1276">Новые командлеты:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="27133-1276">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="27133-1277">Параметр HostId добавлен в New-AzVMConfig и New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="27133-1277">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="27133-1278">Исправлен пример в документации по Invoke-AzVMRunCommand, в котором теперь используется правильное имя параметра.</span><span class="sxs-lookup"><span data-stu-id="27133-1278">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="27133-1279">Исправлено описание VolumeType в справочной документации по Set-AzVMDiskEncryptionExtension и Set-AzVmssDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="27133-1279">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27133-1280">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27133-1280">Az.DataFactory</span></span>
* <span data-ttu-id="27133-1281">Исправлена опечатка в написании Windows со строчной буквы в документации по New-AzDataFactoryEncryptValue.</span><span class="sxs-lookup"><span data-stu-id="27133-1281">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="27133-1282">Пакет SDK ADF для .NET обновлен до версии 4.1.2.</span><span class="sxs-lookup"><span data-stu-id="27133-1282">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="27133-1283">Добавлены параметры DataProxyIntegrationRuntimeName, DataProxyStagingLinkedServiceName и DataProxyStagingPath в командлет Set-AzureRmDataFactoryV2IntegrationRuntime, что позволяет настраивать локальную среду выполнения интеграции в качестве прокси-сервера для Azure-SSIS Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="27133-1283">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="27133-1284">Обновлены PSTriggerRun для отображения активированных конвейеров, сообщений и свойств и PSActivityRun для отображения типа действия.</span><span class="sxs-lookup"><span data-stu-id="27133-1284">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="27133-1285">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27133-1285">Az.DataLakeStore</span></span>
* <span data-ttu-id="27133-1286">Устранена проблема, при которой Get-DataLakeStoreDeletedItem переставал отвечать на запросы при возникновении ошибок или удаленных исключений.</span><span class="sxs-lookup"><span data-stu-id="27133-1286">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="27133-1287">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="27133-1287">Az.EventHub</span></span>
* <span data-ttu-id="27133-1288">Исправлена проблема № 9658: опечатка в написании параметра VirtualNteworkRule у Set-AzEventHubNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="27133-1288">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="27133-1289">Исправлена проблема № 9558: в Set-AzEventHubNamespace используется PATCH вместо PUT.</span><span class="sxs-lookup"><span data-stu-id="27133-1289">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="27133-1290">В командлет Set-AzEventHubNamespace добавлен параметр EnableKafka.</span><span class="sxs-lookup"><span data-stu-id="27133-1290">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="27133-1291">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="27133-1291">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="27133-1292">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="27133-1292">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="27133-1293">Исправлено написание Azure со строчной буквы.</span><span class="sxs-lookup"><span data-stu-id="27133-1293">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27133-1294">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27133-1294">Az.Monitor</span></span>
* <span data-ttu-id="27133-1295">Исправлены неправильные имена параметров в справочной документации.</span><span class="sxs-lookup"><span data-stu-id="27133-1295">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27133-1296">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27133-1296">Az.Network</span></span>
* <span data-ttu-id="27133-1297">Обновлен New-AzPrivateLinkServiceIpConfig.</span><span class="sxs-lookup"><span data-stu-id="27133-1297">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="27133-1298">Параметр PublicIpAddress объявлен нерекомендуемым, так как он не используется на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="27133-1298">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="27133-1299">Добавлен необязательный параметр Primary, указывающий, является ли текущая IP-конфигурация основной.</span><span class="sxs-lookup"><span data-stu-id="27133-1299">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="27133-1300">Улучшена обработка исключений из-за ошибок запроса от пакета SDK. Устранена проблема, при которой исключения пакета SDK не обрабатывались правильно, из-за чего не отображались основные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="27133-1300">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="27133-1301">Настроена логика проверки для префикса IPv6 IP-адреса для проверки правильности длины префикса IPv6.</span><span class="sxs-lookup"><span data-stu-id="27133-1301">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="27133-1302">Обновлен Get-AzVirtualNetworkSubnetConfig: добавлен набор параметров для получения по идентификатору ресурса подсети.</span><span class="sxs-lookup"><span data-stu-id="27133-1302">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="27133-1303">Обновлено описание параметра Location для AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="27133-1303">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="27133-1304">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="27133-1304">Az.OperationalInsights</span></span>
* <span data-ttu-id="27133-1305">Обновлена документация по New-AzOperationalInsightsLinuxSyslogDataSource.</span><span class="sxs-lookup"><span data-stu-id="27133-1305">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="27133-1306">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="27133-1306">Added example</span></span>
    - <span data-ttu-id="27133-1307">Обновлено описание параметра -Name.</span><span class="sxs-lookup"><span data-stu-id="27133-1307">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="27133-1308">Добавлен пример для New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="27133-1308">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="27133-1309">Изменено описание параметра -Name для New-AzOperationalInsightsWindowsEventDataSource.</span><span class="sxs-lookup"><span data-stu-id="27133-1309">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27133-1310">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27133-1310">Az.RecoveryServices</span></span>
* <span data-ttu-id="27133-1311">Обновлен Get-AzRecoveryServicesBackupJobDetail.md.</span><span class="sxs-lookup"><span data-stu-id="27133-1311">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="27133-1312">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27133-1312">Az.Resources</span></span>
* <span data-ttu-id="27133-1313">Добавлена поддержка новой версии API 2019-05-10 для Microsoft.Resource.</span><span class="sxs-lookup"><span data-stu-id="27133-1313">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="27133-1314">Добавлена поддержка copy.count = 0 для переменных, ресурсов и свойств.</span><span class="sxs-lookup"><span data-stu-id="27133-1314">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="27133-1315">Ресурсы, у которых condition = false или copy.count = 0, будут удаляться в полном режиме.</span><span class="sxs-lookup"><span data-stu-id="27133-1315">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="27133-1316">В справочную документацию добавлен пример назначения политики на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="27133-1316">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="27133-1317">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="27133-1317">Az.ServiceBus</span></span>
* <span data-ttu-id="27133-1318">Исправлена проблема № 9658: опечатка в написании параметра VirtualNetworkRule В Set-AzServiceBusNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="27133-1318">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="27133-1319">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="27133-1319">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="27133-1320">Добавлена новая команда Test-AzServiceBusNameAvailability для проверки доступности имени для очереди и раздела.</span><span class="sxs-lookup"><span data-stu-id="27133-1320">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="27133-1321">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="27133-1321">Az.ServiceFabric</span></span>
* <span data-ttu-id="27133-1322">Устранены ошибки командлета для добавления типа узла:</span><span class="sxs-lookup"><span data-stu-id="27133-1322">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="27133-1323">ошибка NullReferenceException, возникавшая, если у группы ресурсов были другие VMSS, не связанные с кластером Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="27133-1323">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="27133-1324">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8681.</span><span class="sxs-lookup"><span data-stu-id="27133-1324">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="27133-1325">Исправлена ошибка, из-за которой командлет завершился сбоем, если virtualNetwork находилась не в той группе ресурсов, к которой относится кластер.</span><span class="sxs-lookup"><span data-stu-id="27133-1325">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="27133-1326">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8407.</span><span class="sxs-lookup"><span data-stu-id="27133-1326">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="27133-1327">Командлет Add-AzServiceFabricApplicationCertificate объявлен нерекомендуемым.</span><span class="sxs-lookup"><span data-stu-id="27133-1327">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="27133-1328">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27133-1328">Az.Sql</span></span>
* <span data-ttu-id="27133-1329">Обновление документации по старым командлетам аудита.</span><span class="sxs-lookup"><span data-stu-id="27133-1329">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27133-1330">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27133-1330">Az.Storage</span></span>
* <span data-ttu-id="27133-1331">Обновлена справка по Get/Close-AzStorageFileHandle: в примеры добавлены сценарии использования командлетов и обновлено описание параметров.</span><span class="sxs-lookup"><span data-stu-id="27133-1331">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="27133-1332">Добавлена поддержка StandardBlobTier в операции отправки BLOB-объекта и копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="27133-1332">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="27133-1333">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="27133-1333">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="27133-1334">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="27133-1334">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="27133-1335">Добавлена поддержка приоритета восстановления в операцию копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="27133-1335">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="27133-1336">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="27133-1336">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27133-1337">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27133-1337">Az.Websites</span></span>
* <span data-ttu-id="27133-1338">Добавлены уточнение для параметра -AppSettings в Set-AzWebApp и Set-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="27133-1338">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="27133-1339">2.5.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="27133-1339">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27133-1340">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27133-1340">Az.Accounts</span></span>
* <span data-ttu-id="27133-1341">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="27133-1341">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="27133-1342">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="27133-1342">Az.ApplicationInsights</span></span>
* <span data-ttu-id="27133-1343">Исправлена опечатка в примере в документации по Remove-AzApplicationInsightsApiKey.</span><span class="sxs-lookup"><span data-stu-id="27133-1343">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="27133-1344">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="27133-1344">Az.Automation</span></span>
* <span data-ttu-id="27133-1345">Исправлена опечатка в строке ресурса.</span><span class="sxs-lookup"><span data-stu-id="27133-1345">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="27133-1346">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="27133-1346">Az.CognitiveServices</span></span>
* <span data-ttu-id="27133-1347">Добавлена поддержка NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="27133-1347">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27133-1348">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27133-1348">Az.Compute</span></span>
* <span data-ttu-id="27133-1349">Добавлены недостающие свойства (ComputerName, OsName, OsVersion и HyperVGeneration) для объекта представления экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="27133-1349">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="27133-1350">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="27133-1350">Az.ContainerRegistry</span></span>
* <span data-ttu-id="27133-1351">Исправлена опечатка в Remove-AzContainerRegistryReplication для параметра репликации.</span><span class="sxs-lookup"><span data-stu-id="27133-1351">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="27133-1352">См. подробнее: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="27133-1352">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27133-1353">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27133-1353">Az.DataFactory</span></span>
* <span data-ttu-id="27133-1354">Пакет SDK для ADF .NET обновлен до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="27133-1354">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="27133-1355">Исправлена опечатка в документации по Get-AzDataFactoryV2PipelineRun.</span><span class="sxs-lookup"><span data-stu-id="27133-1355">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="27133-1356">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="27133-1356">Az.EventHub</span></span>
* <span data-ttu-id="27133-1357">Добавлен новый командлет для создания маркера SAS: New-AzEventHubAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="27133-1357">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="27133-1358">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="27133-1358">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="27133-1359">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27133-1359">Az.KeyVault</span></span>
* <span data-ttu-id="27133-1360">Добавлена поддержка для настройки параметра KeySize в политиках сертификатов.</span><span class="sxs-lookup"><span data-stu-id="27133-1360">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="27133-1361">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="27133-1361">Az.LogicApp</span></span>
* <span data-ttu-id="27133-1362">Get-AzIntegrationAccountMap теперь надлежащим образом выводит все типы сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="27133-1362">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="27133-1363">Добавлен новый параметр MapType для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="27133-1363">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="27133-1364">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="27133-1364">Az.ManagedServices</span></span>
* <span data-ttu-id="27133-1365">Добавлена поддержка API версии 2019-06-01 (общедоступная).</span><span class="sxs-lookup"><span data-stu-id="27133-1365">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27133-1366">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27133-1366">Az.Network</span></span>
* <span data-ttu-id="27133-1367">Добавлена поддержка частной конечной точки и службы приватного канала.</span><span class="sxs-lookup"><span data-stu-id="27133-1367">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="27133-1368">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="27133-1368">New cmdlets</span></span>
        - <span data-ttu-id="27133-1369">Set-AzPrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="27133-1369">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="27133-1370">Set-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="27133-1370">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="27133-1371">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="27133-1371">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="27133-1372">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="27133-1372">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="27133-1373">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="27133-1373">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="27133-1374">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="27133-1374">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="27133-1375">Test-AzPrivateLinkServiceVisibility.</span><span class="sxs-lookup"><span data-stu-id="27133-1375">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="27133-1376">Get-AzAutoApprovedPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="27133-1376">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="27133-1377">Обновлены следующие команды для функции: Флаг PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies в подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="27133-1377">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="27133-1378">Обновлены командлеты New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig.</span><span class="sxs-lookup"><span data-stu-id="27133-1378">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="27133-1379">Добавлен необязательный параметр -PrivateEndpointNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к частной конечной точке в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="27133-1379">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="27133-1380">Добавлен необязательный параметр -PrivateLinkServiceNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к службе приватного канала в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="27133-1380">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="27133-1381">Параметр ServiceName командлета AzPrivateLinkService был переименован на Name с псевдонимом ServiceName для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="27133-1381">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="27133-1382">Включен протокол ICMP для настройки правил безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="27133-1382">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="27133-1383">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="27133-1383">Updated cmdlets</span></span>
        - <span data-ttu-id="27133-1384">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="27133-1384">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="27133-1385">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="27133-1385">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="27133-1386">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="27133-1386">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="27133-1387">Добавлен ConnectionProtocolType (Ikev1/Ikev2) в качестве настраиваемого параметра для командлета New-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="27133-1387">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="27133-1388">Добавлен PrivateIpAddressVersion в LoadBalancerFrontendIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="27133-1388">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="27133-1389">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="27133-1389">Updated cmdlet:</span></span>
        - <span data-ttu-id="27133-1390">New-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="27133-1390">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="27133-1391">Add-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="27133-1391">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="27133-1392">Set-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="27133-1392">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="27133-1393">Команда New-AzApplicationGatewayProbeConfig Шлюза приложений обновлена для поддержки настраиваемого порта в зонде.</span><span class="sxs-lookup"><span data-stu-id="27133-1393">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="27133-1394">Обновлен командлет New-AzApplicationGatewayProbeConfig: добавлен необязательный параметр Port, который используется при проверке внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="27133-1394">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="27133-1395">Этот параметр применяется к номерам SKU Standard_V2 и WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="27133-1395">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="27133-1396">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="27133-1396">Az.OperationalInsights</span></span>
* <span data-ttu-id="27133-1397">Обновленная версия по умолчанию для сохраненных операций поиска имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="27133-1397">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="27133-1398">Исправлены ошибки при обработке регулярных выражений со значениями NULL в журналах.</span><span class="sxs-lookup"><span data-stu-id="27133-1398">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27133-1399">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27133-1399">Az.RecoveryServices</span></span>
* <span data-ttu-id="27133-1400">Обновлен файл Get-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="27133-1400">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="27133-1401">Обновлен файл Get-AzRecoveryServicesBackupContainer.md.</span><span class="sxs-lookup"><span data-stu-id="27133-1401">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="27133-1402">Обновлен файл Get-AzRecoveryServicesVault.md.</span><span class="sxs-lookup"><span data-stu-id="27133-1402">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="27133-1403">Обновлен файл Wait-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="27133-1403">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="27133-1404">Обновлен файл Set-AzRecoveryServicesVaultContext.md.</span><span class="sxs-lookup"><span data-stu-id="27133-1404">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="27133-1405">Обновлен файл Get-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="27133-1405">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="27133-1406">Обновлен файл Get-AzRecoveryServicesBackupRecoveryPoint.md.</span><span class="sxs-lookup"><span data-stu-id="27133-1406">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="27133-1407">Обновлен файл Restore-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="27133-1407">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="27133-1408">Обновлен вызов службы для отмены регистрации контейнера в общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="27133-1408">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="27133-1409">Обновлен файл Set-AzRecoveryServicesAsrAlertSetting.md.</span><span class="sxs-lookup"><span data-stu-id="27133-1409">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="27133-1410">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27133-1410">Az.Resources</span></span>
- <span data-ttu-id="27133-1411">Удален отсутствующий командлет, который упоминается в документации по New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="27133-1411">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="27133-1412">Обновлены командлеты политик для использования новой версии API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="27133-1412">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="27133-1413">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="27133-1413">Az.ServiceBus</span></span>
* <span data-ttu-id="27133-1414">Добавлен новый командлет для создания маркера SAS: New-AzServiceBusAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="27133-1414">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="27133-1415">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="27133-1415">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="27133-1416">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27133-1416">Az.Sql</span></span>
* <span data-ttu-id="27133-1417">Исправлены отсутствующие примеры для командлета Set-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="27133-1417">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="27133-1418">Исправлены заданные повторяющиеся проверки для оценки наличия уязвимостей без указания адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="27133-1418">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="27133-1419">Исправлена незначительная опечатка в сообщении предупреждения.</span><span class="sxs-lookup"><span data-stu-id="27133-1419">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27133-1420">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27133-1420">Az.Storage</span></span>
* <span data-ttu-id="27133-1421">Обновлен пример в справочной документации для использования командлетом Get-AzStorageAccount правильного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="27133-1421">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="27133-1422">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="27133-1422">Az.StorageSync</span></span>
* <span data-ttu-id="27133-1423">Добавлен командлет Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="27133-1423">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="27133-1424">Исправлена проблема № 9551, связанная с TierFilesOlderThanDays.</span><span class="sxs-lookup"><span data-stu-id="27133-1424">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27133-1425">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27133-1425">Az.Websites</span></span>
* <span data-ttu-id="27133-1426">Исправлена ошибка, при которой некоторые свойства SiteConfig не возвращались Get-AzWebApp и Set-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="27133-1426">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="27133-1427">Добавлен новый параметр Location в Get-AzDeletedWebApp и Restore-AzDeletedWebApp.</span><span class="sxs-lookup"><span data-stu-id="27133-1427">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="27133-1428">Исправлена ошибка, которая возникала при клонировании слотов веб-приложений с помощью командлета New-AzWebApp-IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="27133-1428">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="27133-1429">2.4.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="27133-1429">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27133-1430">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27133-1430">Az.Accounts</span></span>
* <span data-ttu-id="27133-1431">Добавлена поддержка командлетов профиля.</span><span class="sxs-lookup"><span data-stu-id="27133-1431">Add support for profile cmdlets</span></span>
* <span data-ttu-id="27133-1432">Добавлена поддержка сред и плоскостей данных в созданных командлетах.</span><span class="sxs-lookup"><span data-stu-id="27133-1432">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="27133-1433">Исправлена ошибка, когда в командлетах плоскости данных в Windows PowerShell в некоторых случаях использовалась неправильная конечная точка.</span><span class="sxs-lookup"><span data-stu-id="27133-1433">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="27133-1434">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="27133-1434">Az.Advisor</span></span>
* <span data-ttu-id="27133-1435">Выпущена общедоступная версия Az.Advisor.</span><span class="sxs-lookup"><span data-stu-id="27133-1435">GA release of Az.Advisor</span></span>
* <span data-ttu-id="27133-1436">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="27133-1436">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="27133-1437">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="27133-1437">Az.ApiManagement</span></span>
* <span data-ttu-id="27133-1438">исправлена проблема https://github.com/Azure/azure-powershell/issues/8671.</span><span class="sxs-lookup"><span data-stu-id="27133-1438">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="27133-1439">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="27133-1439">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="27133-1440">Добавлена поддержка запрашивания подписок по пользователю и продукту.</span><span class="sxs-lookup"><span data-stu-id="27133-1440">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="27133-1441">Добавлена поддержка создания запросов с использованием области "/", "/apis", "/apis/echo-api".</span><span class="sxs-lookup"><span data-stu-id="27133-1441">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="27133-1442">Исправлены проблемы https://github.com/Azure/azure-powershell/issues/9307 и https://github.com/Azure/azure-powershell/issues/8432.</span><span class="sxs-lookup"><span data-stu-id="27133-1442">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="27133-1443">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="27133-1443">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="27133-1444">Добавлена поддержка указания ApiVersion и ApiVersionSetId при импорте API-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="27133-1444">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="27133-1445">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="27133-1445">Az.Automation</span></span>
* <span data-ttu-id="27133-1446">Исправлена ошибка командлета Set-AzAutomationConnectionFieldValue при обработке строкового значения.</span><span class="sxs-lookup"><span data-stu-id="27133-1446">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27133-1447">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27133-1447">Az.Compute</span></span>
* <span data-ttu-id="27133-1448">В New AzImageConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="27133-1448">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27133-1449">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27133-1449">Az.DataFactory</span></span>
* <span data-ttu-id="27133-1450">Обновление выходных данных командлетов ADF, предназначенных для получения числа выполнений действий, конвейеров и триггеров, для поддержки канала Select-Object.</span><span class="sxs-lookup"><span data-stu-id="27133-1450">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="27133-1451">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="27133-1451">Az.EventGrid</span></span>
* <span data-ttu-id="27133-1452">Исправлена опечатка в документации по командлету New-AzEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="27133-1452">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="27133-1453">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="27133-1453">Az.IotHub</span></span>
* <span data-ttu-id="27133-1454">Добавлена поддержка повторного создания ключей политики авторизации.</span><span class="sxs-lookup"><span data-stu-id="27133-1454">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27133-1455">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27133-1455">Az.Network</span></span>
* <span data-ttu-id="27133-1456">К тегам общедоступного IP-адреса добавлен тег RoutingPreference.</span><span class="sxs-lookup"><span data-stu-id="27133-1456">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="27133-1457">Улучшены примеры для справочной документации по командлету Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="27133-1457">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="27133-1458">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="27133-1458">Az.PolicyInsights</span></span>
* <span data-ttu-id="27133-1459">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="27133-1459">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="27133-1460">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9446.</span><span class="sxs-lookup"><span data-stu-id="27133-1460">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="27133-1461">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="27133-1461">Az.OperationalInsights</span></span>
* <span data-ttu-id="27133-1462">Исправленная модель источника данных CustomLog возвращена в командлет Get-AzOperationalInsightsDataSource.</span><span class="sxs-lookup"><span data-stu-id="27133-1462">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27133-1463">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27133-1463">Az.RecoveryServices</span></span>
* <span data-ttu-id="27133-1464">Выпущено исправление для команды get-policy для виртуальных машин IaaS.</span><span class="sxs-lookup"><span data-stu-id="27133-1464">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="27133-1465">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27133-1465">Az.Resources</span></span>
    - <span data-ttu-id="27133-1466">Исправлен текст справки по параметру Get-AzPolicyState -Top.</span><span class="sxs-lookup"><span data-stu-id="27133-1466">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="27133-1467">Добавлена поддержка разбиения по страницам на стороне клиента для Get-AzPolicyAlias.</span><span class="sxs-lookup"><span data-stu-id="27133-1467">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="27133-1468">Добавлены новые параметры для Set-AzPolicyAssignment, -PolicyParameters и -PolicyParametersObject.</span><span class="sxs-lookup"><span data-stu-id="27133-1468">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="27133-1469">Добавлен ряд обновлений документов и примеров для командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="27133-1469">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="27133-1470">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="27133-1470">Az.ServiceBus</span></span>
* <span data-ttu-id="27133-1471">Исправление ошибки № 4938: командлет New-AzureRmServiceBusQueue возвращает ответ BadRequest (Недопустимый запрос) при задании значения MaxSizeInMegabytes.</span><span class="sxs-lookup"><span data-stu-id="27133-1471">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="27133-1472">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27133-1472">Az.Sql</span></span>
* <span data-ttu-id="27133-1473">Из выпуска предварительной версии в выпуск общедоступной версии добавлены командлеты группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="27133-1473">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="27133-1474">Поддержка аудита Azure SQL Server и баз данных с помощью новых командлетов:</span><span class="sxs-lookup"><span data-stu-id="27133-1474">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="27133-1475">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="27133-1475">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="27133-1476">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="27133-1476">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="27133-1477">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="27133-1477">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="27133-1478">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="27133-1478">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="27133-1479">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="27133-1479">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="27133-1480">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="27133-1480">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="27133-1481">Из параметров оценки уязвимостей удалены ограничения, касающиеся электронной почты.</span><span class="sxs-lookup"><span data-stu-id="27133-1481">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27133-1482">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27133-1482">Az.Storage</span></span>
* <span data-ttu-id="27133-1483">Два параметра в указанном ниже командлете — -IndexDocument и -ErrorDocument404Path, — которые ранее были обязательными, стали необязательными:</span><span class="sxs-lookup"><span data-stu-id="27133-1483">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="27133-1484">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="27133-1484">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="27133-1485">Обновлена справка по командлету Get-AzStorageBlobContent: добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="27133-1485">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="27133-1486">При сбое выполнения командлета с ошибкой StorageException отображаются дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="27133-1486">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="27133-1487">Добавлена поддержка создания или обновления учетной записи хранения с использованием проверки подлинности AAD DS для службы "Файлы Azure".</span><span class="sxs-lookup"><span data-stu-id="27133-1487">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="27133-1488">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27133-1488">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="27133-1489">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27133-1489">Set-AzStorageAccount</span></span>
* <span data-ttu-id="27133-1490">Добавлена поддержка перечисления или закрытия дескрипторов файлов для общей папки, каталога файлов или файла:</span><span class="sxs-lookup"><span data-stu-id="27133-1490">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="27133-1491">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="27133-1491">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="27133-1492">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="27133-1492">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="27133-1493">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="27133-1493">Az.StorageSync</span></span>
* <span data-ttu-id="27133-1494">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="27133-1494">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="27133-1495">2.3.2 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="27133-1495">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27133-1496">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27133-1496">Az.Accounts</span></span>
* <span data-ttu-id="27133-1497">Исправлена ошибка, связанная с использованием неправильного URL-адреса для вызовов функций.</span><span class="sxs-lookup"><span data-stu-id="27133-1497">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="27133-1498">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8983.</span><span class="sxs-lookup"><span data-stu-id="27133-1498">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="27133-1499">Устранена проблема с псевдонимами из AzureRM для командлетов Az.</span><span class="sxs-lookup"><span data-stu-id="27133-1499">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="27133-1500">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="27133-1500">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="27133-1501">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest.</span><span class="sxs-lookup"><span data-stu-id="27133-1501">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27133-1502">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27133-1502">Az.Compute</span></span>
* <span data-ttu-id="27133-1503">Простые наборы параметров New-AzVm и New-AzVmss теперь принимают параметр ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="27133-1503">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="27133-1504">Исправлена опечатка в справочной документации по New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="27133-1504">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="27133-1505">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="27133-1505">Az.Dns</span></span>
* <span data-ttu-id="27133-1506">Исправлена опечатка в справочных примерах по использованию Set-AzDnsZone.</span><span class="sxs-lookup"><span data-stu-id="27133-1506">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="27133-1507">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="27133-1507">Az.EventGrid</span></span>
* <span data-ttu-id="27133-1508">Обновлен для использования API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="27133-1508">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="27133-1509">Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="27133-1509">New cmdlets:</span></span>
    - <span data-ttu-id="27133-1510">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="27133-1510">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="27133-1511">Создает домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="27133-1511">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="27133-1512">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="27133-1512">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="27133-1513">Возвращает сведения о домене Сетки событий или список всех доменов Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="27133-1513">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="27133-1514">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="27133-1514">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="27133-1515">Удаляет домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="27133-1515">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="27133-1516">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="27133-1516">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="27133-1517">Повторно создает ключ общего доступа для домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="27133-1517">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="27133-1518">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="27133-1518">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="27133-1519">Возвращает ключи общего доступа, используемые для публикации событий в домене Сетки событий.</span><span class="sxs-lookup"><span data-stu-id="27133-1519">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="27133-1520">New-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="27133-1520">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="27133-1521">Создает раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="27133-1521">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="27133-1522">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="27133-1522">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="27133-1523">Возвращает сведения о разделе домена Сетки событий или список всех разделов определенного домена Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="27133-1523">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="27133-1524">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="27133-1524">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="27133-1525">Удаляет раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="27133-1525">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="27133-1526">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="27133-1526">Updated cmdlets:</span></span>
    - <span data-ttu-id="27133-1527">New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="27133-1527">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="27133-1528">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для нового домена Сетки событий и раздела домена Сетки событий и позволяющие создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="27133-1528">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="27133-1529">Добавляют новые обязательные параметры для указания имени нового домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="27133-1529">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="27133-1530">Добавляют новые наборы параметров для доменов и разделов домена и позволяют повторно использовать существующие параметры (например, EndPointType, SubjectBeginsWith и т. д.).</span><span class="sxs-lookup"><span data-stu-id="27133-1530">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="27133-1531">Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="27133-1531">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="27133-1532">срока действия подписки на событие;</span><span class="sxs-lookup"><span data-stu-id="27133-1532">Event subscription expiration date,</span></span>
            - <span data-ttu-id="27133-1533">параметров расширенной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="27133-1533">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="27133-1534">Добавляют новое перечисление для ServiceBusQueue в качестве места назначения.</span><span class="sxs-lookup"><span data-stu-id="27133-1534">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="27133-1535">Запрещают использование значение All в параметре -IncludedEventType и заменяют его следующим:</span><span class="sxs-lookup"><span data-stu-id="27133-1535">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="27133-1536">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="27133-1536">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="27133-1537">Добавляют новые необязательные параметры (Top, ODataQuery и NextLink) для поддержки разбиения на страницы и фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="27133-1537">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="27133-1538">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="27133-1538">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="27133-1539">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для домена Сетки событий и раздела домена Сетки событий и позволяющие удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="27133-1539">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="27133-1540">Добавляют новые обязательные параметры для указания имени домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="27133-1540">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="27133-1541">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="27133-1541">Az.FrontDoor</span></span>
* <span data-ttu-id="27133-1542">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="27133-1542">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="27133-1543">Добавляет поддержку преобразований и новое значение оператора автозавершения (RegEx).</span><span class="sxs-lookup"><span data-stu-id="27133-1543">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="27133-1544">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="27133-1544">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="27133-1545">Добавляет новые значения автозавершения.</span><span class="sxs-lookup"><span data-stu-id="27133-1545">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27133-1546">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27133-1546">Az.Network</span></span>
* <span data-ttu-id="27133-1547">Добавляет поддержку ресурса шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="27133-1547">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="27133-1548">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="27133-1548">New cmdlets</span></span>
        - <span data-ttu-id="27133-1549">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="27133-1549">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="27133-1550">Добавляет AvailablePrivateEndpointType.</span><span class="sxs-lookup"><span data-stu-id="27133-1550">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="27133-1551">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="27133-1551">New cmdlets</span></span>
        - <span data-ttu-id="27133-1552">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="27133-1552">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="27133-1553">Добавляет PrivatePrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="27133-1553">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="27133-1554">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="27133-1554">New cmdlets</span></span>
        - <span data-ttu-id="27133-1555">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="27133-1555">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="27133-1556">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="27133-1556">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="27133-1557">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="27133-1557">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="27133-1558">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="27133-1558">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="27133-1559">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="27133-1559">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="27133-1560">Добавляет PrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="27133-1560">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="27133-1561">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="27133-1561">New cmdlets</span></span>
        - <span data-ttu-id="27133-1562">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="27133-1562">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="27133-1563">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="27133-1563">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="27133-1564">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="27133-1564">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="27133-1565">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="27133-1565">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="27133-1566">Обновлены следующие команды для функции: флаг UseLocalAzureIpAddress для VPN-подключения.</span><span class="sxs-lookup"><span data-stu-id="27133-1566">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="27133-1567">Обновлен командлет New-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="27133-1567">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="27133-1568">Обновлен командлет Set-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="27133-1568">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="27133-1569">В пиринг ExpressRoute добавлено поле только для чтения PeeredConnections.</span><span class="sxs-lookup"><span data-stu-id="27133-1569">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="27133-1570">В ExpressRoute добавлено поле только для чтения GlobalReachEnabled.</span><span class="sxs-lookup"><span data-stu-id="27133-1570">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="27133-1571">Добавлен атрибут в рамках критического изменения, отменяющего статус устаревшего поля AllowGlobalReach в модели ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="27133-1571">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="27133-1572">Исправлена проблема, связанная с ошибкой 8756, при использовании TargetListenerID с командлетами AzApplicationGatewayRedirectConfiguration.</span><span class="sxs-lookup"><span data-stu-id="27133-1572">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="27133-1573">Исправлена ошибка в New-AzApplicationGatewayPathRuleConfig, не позволявшая задавать набор правил повторного создания.</span><span class="sxs-lookup"><span data-stu-id="27133-1573">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="27133-1574">Исправлено отображение VirtualNetworkTaps в NetworkInterfaceIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="27133-1574">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="27133-1575">Исправлены командлеты Cortex Get для отображения всех частей.</span><span class="sxs-lookup"><span data-stu-id="27133-1575">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="27133-1576">Исправлено создание ссылок VirtualHub для ExpressRouteGateways и VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="27133-1576">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="27133-1577">В AzureFirewall и NatGateway добавлена поддержка Зон доступности.</span><span class="sxs-lookup"><span data-stu-id="27133-1577">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="27133-1578">Добавлен командлет Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="27133-1578">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="27133-1579">Добавлена поддержка нескольких общедоступных IP-адресов для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="27133-1579">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="27133-1580">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="27133-1580">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="27133-1581">Добавлен параметр -PublicIpAddress, который принимает один или несколько объектов общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="27133-1581">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="27133-1582">Добавлен параметр -VirtualNetwork, который принимает объект виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="27133-1582">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="27133-1583">Добавлены методы AddPublicIpAddress и RemovePublicIpAddress для объекта брандмауэра. Они принимают объект общедоступного IP-адреса в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="27133-1583">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="27133-1584">Не рекомендуется использовать параметры -PublicIpName и -VirtualNetworkName.</span><span class="sxs-lookup"><span data-stu-id="27133-1584">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="27133-1585">Обновлены следующие команды для функции: В параметрах проверки подлинности AAD VPN-клиента задан ресурс шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="27133-1585">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="27133-1586">Обновлен командлет New-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="27133-1586">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="27133-1587">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="27133-1587">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="27133-1588">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр-переключатель RemoveAadAuthentication для удаления в шлюзе параметров проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="27133-1588">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="27133-1589">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="27133-1589">Az.OperationalInsights</span></span>
* <span data-ttu-id="27133-1590">Добавлена поддержка SKU **pergb2018** в команде New-AzureRmOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="27133-1590">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="27133-1591">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27133-1591">Az.Resources</span></span>
* <span data-ttu-id="27133-1592">Поддержка дополнительных вариантов экспорта шаблона.</span><span class="sxs-lookup"><span data-stu-id="27133-1592">Support for additional Template Export options</span></span>
    - <span data-ttu-id="27133-1593">В Export-AzResourceGroup добавлен параметр -SkipResourceNameParameterization.</span><span class="sxs-lookup"><span data-stu-id="27133-1593">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="27133-1594">В Export-AzResourceGroup добавлен параметр -SkipAllParameterization.</span><span class="sxs-lookup"><span data-stu-id="27133-1594">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="27133-1595">В Export-AzResourceGroup добавлен параметр -Resource для фильтрации экспортированных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="27133-1595">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="27133-1596">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="27133-1596">Az.ServiceFabric</span></span>
* <span data-ttu-id="27133-1597">Исправлена ошибка, связанная с получением иногда неправильных отпечатков при добавлении сертификата ByExistingKeyVault.</span><span class="sxs-lookup"><span data-stu-id="27133-1597">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="27133-1598">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27133-1598">Az.Sql</span></span>
* <span data-ttu-id="27133-1599">Исправлен суффикс конечной точки хранилища службы "Расширенная защита от угроз Azure".</span><span class="sxs-lookup"><span data-stu-id="27133-1599">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="27133-1600">Исправлена ошибка, связанная с возможностью пакета "Расширенная защита данных" переопределять политику службы "Расширенная защита от угроз".</span><span class="sxs-lookup"><span data-stu-id="27133-1600">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="27133-1601">Новые командлеты для Management.Sql позволяют клиентам добавлять ключи TDE и задавать средство защиты TDE для управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="27133-1601">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="27133-1602">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="27133-1602">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="27133-1603">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="27133-1603">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="27133-1604">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="27133-1604">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="27133-1605">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="27133-1605">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="27133-1606">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="27133-1606">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27133-1607">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27133-1607">Az.Storage</span></span>
* <span data-ttu-id="27133-1608">Поддержка класса Kind в FileStorage и значения Premium_ZRS в SkuName при создании учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="27133-1608">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="27133-1609">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27133-1609">New-AzStorageAccount</span></span>
* <span data-ttu-id="27133-1610">Уточнено описание командлета неизменности BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="27133-1610">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="27133-1611">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="27133-1611">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27133-1612">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27133-1612">Az.Websites</span></span>
* <span data-ttu-id="27133-1613">Оптимизирует Get-AzWebAppCertificate для фильтрации по группе ресурсов на сервере, а не в клиенте.</span><span class="sxs-lookup"><span data-stu-id="27133-1613">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="27133-1614">Добавляет параметр-переключатель - UseDisasterRecovery в Get AzWebAppSnapshot.</span><span class="sxs-lookup"><span data-stu-id="27133-1614">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="27133-1615">2.2.0 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="27133-1615">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="27133-1616">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="27133-1616">Az.Cdn</span></span>
* <span data-ttu-id="27133-1617">Обновлены командлеты для поддержки функции rulesEngine на основе API версии 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="27133-1617">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27133-1618">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27133-1618">Az.Compute</span></span>
* <span data-ttu-id="27133-1619">Добавлен параметр `NoWait`, который запускает операцию и немедленно возвращает значение еще до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="27133-1619">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="27133-1620">Обновлены командлеты:   Export-AzLogAnalyticRequestRateByInterval; Export-AzLogAnalyticThrottledRequest; Remove-AzVM; Remove-AzVMAccessExtension; Remove-AzVMAEMExtension; Remove-AzVMChefExtension; Remove-AzVMCustomScriptExtension; Remove-AzVMDiagnosticsExtension; Remove-AzVMDiskEncryptionExtension; Remove-AzVMDscExtension; Remove-AzVMSqlServerExtension; Restart-AzVM; Set-AzVM; Set-AzVMAccessExtension; Set-AzVMADDomainExtension; Set-AzVMAEMExtension; Set-AzVMBginfoExtension; Set-AzVMChefExtension; Set-AzVMCustomScriptExtension; Set-AzVMDiagnosticsExtension; Set-AzVMDscExtension; Set-AzVMExtension; Start-AzVM; Stop-AzVM; Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="27133-1620">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="27133-1621">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="27133-1621">Az.EventHub</span></span>
* <span data-ttu-id="27133-1622">Исправлена ошибка № 9231. Командлет Get-AzEventHubNamespace не возвращал теги.</span><span class="sxs-lookup"><span data-stu-id="27133-1622">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="27133-1623">Исправлена ошибка № 9230. Командлет Get-AzEventHubNamespace возвращал значение ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="27133-1623">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27133-1624">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27133-1624">Az.Network</span></span>
* <span data-ttu-id="27133-1625">Обновлены параметры ResourceId и InputObject для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="27133-1625">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="27133-1626">Добавлены псевдонимы для параметров ResourceId и InputObject.</span><span class="sxs-lookup"><span data-stu-id="27133-1626">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="27133-1627">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="27133-1627">Az.PolicyInsights</span></span>
* <span data-ttu-id="27133-1628">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyEvent.</span><span class="sxs-lookup"><span data-stu-id="27133-1628">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27133-1629">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27133-1629">Az.RecoveryServices</span></span>
* <span data-ttu-id="27133-1630">Минимальный срок хранения политики IaaSVM изменился с 1 до 7 дней.</span><span class="sxs-lookup"><span data-stu-id="27133-1630">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="27133-1631">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="27133-1631">Az.ServiceBus</span></span>
* <span data-ttu-id="27133-1632">Исправлена ошибка № 9182. Командлет Get-AzServiceBusNamespace возвращал ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="27133-1632">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="27133-1633">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="27133-1633">Az.ServiceFabric</span></span>
* <span data-ttu-id="27133-1634">Исправлена опечатка в сообщении об ошибке для командлета Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="27133-1634">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="27133-1635">Добавлен отсутствующий символ в командных строках Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="27133-1635">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="27133-1636">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27133-1636">Az.Sql</span></span>
* <span data-ttu-id="27133-1637">Для командлета New-AzureSqlInstance добавлен параметр DnsZonePartner, обеспечивающий поддержку AutoDr для Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="27133-1637">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="27133-1638">Командлет Get-AzSqlDatabaseSecureConnectionPolicy объявлен неподдерживаемым.</span><span class="sxs-lookup"><span data-stu-id="27133-1638">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="27133-1639">Командлеты обнаружения угроз переименованы в командлеты Расширенной защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="27133-1639">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="27133-1640">Параметры -StorageSizeInGB и -LicenseType командлета New-AzSqlInstance теперь необязательны.</span><span class="sxs-lookup"><span data-stu-id="27133-1640">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27133-1641">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27133-1641">Az.Websites</span></span>
* <span data-ttu-id="27133-1642">Исправлены проблемы, когда удалялись теги при использовании Set-AzWebApp и Set-AzWebAppSlot со свойством -WebApp.</span><span class="sxs-lookup"><span data-stu-id="27133-1642">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="27133-1643">2.1.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="27133-1643">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="27133-1644">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="27133-1644">Az.ApiManagement</span></span>
* <span data-ttu-id="27133-1645">Созданы командлеты для управления диагностикой в глобальной области и в области API.</span><span class="sxs-lookup"><span data-stu-id="27133-1645">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="27133-1646">**Get-AzApiManagementDiagnostic** — получение диагностики, заданной глобально или на уровне области API.</span><span class="sxs-lookup"><span data-stu-id="27133-1646">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="27133-1647">**New-AzApiManagementDiagnostic** — создание диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="27133-1647">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="27133-1648">**New-AzApiManagementHttpMessageDiagnostic** — создание параметра диагностики, для которого регистрируются заголовки и размер байтов тела.</span><span class="sxs-lookup"><span data-stu-id="27133-1648">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="27133-1649">**New-AzApiManagementPipelineDiagnosticSetting** — создание параметров диагностики для сообщений HTTP, поступающих в шлюз или исходящих из него.</span><span class="sxs-lookup"><span data-stu-id="27133-1649">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="27133-1650">**New-AzApiManagementSamplingSetting** — создание параметра выборки для запросов и ответов касательно диагностики.</span><span class="sxs-lookup"><span data-stu-id="27133-1650">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="27133-1651">**Remove-AzApiManagementDiagnostic** — удаление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="27133-1651">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="27133-1652">**Set-AzApiManagementDiagnostic** — обновление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="27133-1652">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="27133-1653">Созданы командлеты для управления кэшем в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="27133-1653">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="27133-1654">**Get-AzApiManagementCache** — получение сведений о кэше, указанном идентификатором, или обо всех кэшах.</span><span class="sxs-lookup"><span data-stu-id="27133-1654">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="27133-1655">**New-AzApiManagementCache** — создание кэша по умолчанию или кэша в определенном регионе Azure.</span><span class="sxs-lookup"><span data-stu-id="27133-1655">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="27133-1656">**Remove-AzApiManagementCache** — удаление кэша.</span><span class="sxs-lookup"><span data-stu-id="27133-1656">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="27133-1657">**Update-AzApiManagementCache** — обновление кэша.</span><span class="sxs-lookup"><span data-stu-id="27133-1657">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="27133-1658">Созданы командлеты для управления схемой API.</span><span class="sxs-lookup"><span data-stu-id="27133-1658">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="27133-1659">**New-AzApiManagementSchema** — создание схемы для API.</span><span class="sxs-lookup"><span data-stu-id="27133-1659">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="27133-1660">**Get-AzApiManagementSchema** — получение схем, настроенных в API.</span><span class="sxs-lookup"><span data-stu-id="27133-1660">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="27133-1661">**Remove-AzApiManagementSchema** — удаление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="27133-1661">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="27133-1662">**Set-AzApiManagementSchema** — обновление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="27133-1662">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="27133-1663">Создан командлет для создания токена пользователя.</span><span class="sxs-lookup"><span data-stu-id="27133-1663">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="27133-1664">**New-AzApiManagementUserToken** — создание токена пользователя, по умолчанию действительного в течение 8 часов. С помощью этого командлета можно создавать токен для пользователя GIT.</span><span class="sxs-lookup"><span data-stu-id="27133-1664">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="27133-1665">Создан командлет для получения состояния сети.</span><span class="sxs-lookup"><span data-stu-id="27133-1665">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="27133-1666">**Get-AzApiManagementNetworkStatus** — получение состояния подключения сети ресурсов, от которых зависит служба "Управление API".</span><span class="sxs-lookup"><span data-stu-id="27133-1666">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="27133-1667">Это полезно при развертывании службы ApiManagement в виртуальной сети и проверке того, не нарушена ли какая-либо из зависимостей.</span><span class="sxs-lookup"><span data-stu-id="27133-1667">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="27133-1668">Обновлен командлет **New-AzApiManagement** для управления службой ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="27133-1668">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="27133-1669">Добавлена поддержка нового SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="27133-1669">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="27133-1670">Добавлена поддержка для включения флага EnableClientCertificate в SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="27133-1670">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="27133-1671">Новый командлет **New-AzApiManagementSslSetting** позволяет настраивать параметр TLS/SSL для сервера (Backend) и внешнего интерфейса (Frontend).</span><span class="sxs-lookup"><span data-stu-id="27133-1671">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="27133-1672">Его также можно использовать для настройки Ciphers как 3DES, в ServerProtocols как Http2 для внешнего интерфейса (Frontend) службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="27133-1672">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="27133-1673">Добавлена поддержка настройки имени узла DeveloperPortal в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="27133-1673">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="27133-1674">Обновлен командлет **Get-AzApiManagementSsoToken** для извлечения объекта PsApiManagement в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="27133-1674">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="27133-1675">Обновлен командлет для отображения встроенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="27133-1675">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="27133-1676">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Код ошибки: ValidationError. Сообщение об ошибке: "Некоторые поля содержат неправильные значения". Сведения об ошибке: [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="27133-1676">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="27133-1677">Обновлен командлет **Export-AzApiManagementApi** для экспортирования программных интерфейсов в формате OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="27133-1677">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="27133-1678">Обновлен командлет **Import-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="27133-1678">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="27133-1679">Для импортирования API из спецификации документа OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="27133-1679">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="27133-1680">Для переопределения свойства PsApiManagementSchema, указанного в любом документе (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="27133-1680">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="27133-1681">Для переопределения свойства ServiceUrl, указанного в любом документе.</span><span class="sxs-lookup"><span data-stu-id="27133-1681">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="27133-1682">Обновлен командлет **Get-AzApiManagementPolicy** для возврата политики в формате, экранированном не для XML, с использованием rawxml.</span><span class="sxs-lookup"><span data-stu-id="27133-1682">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="27133-1683">Обновлен командлет **Set-AzApiManagementPolicy**. Он принимает политику в формате, экранированном не для XML, с использованием rawxml и в формате, экранированном для XML, с использованием XML.</span><span class="sxs-lookup"><span data-stu-id="27133-1683">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="27133-1684">Обновлен командлет **New-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="27133-1684">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="27133-1685">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="27133-1685">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="27133-1686">Для создания API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="27133-1686">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="27133-1687">Для клонирования API с использованием значений SourceApiId и SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="27133-1687">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="27133-1688">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="27133-1688">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="27133-1689">Обновлен командлет **Set-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="27133-1689">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="27133-1690">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="27133-1690">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="27133-1691">Для обновления API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="27133-1691">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="27133-1692">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="27133-1692">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="27133-1693">Обновлен командлет **New-AzApiManagementRevision**:</span><span class="sxs-lookup"><span data-stu-id="27133-1693">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="27133-1694">Для клонирования (копирования тегов, продуктов, операций и политик) существующей редакции с использованием SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="27133-1694">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="27133-1695">Новая редакция предполагает родительский идентификатор ApiId.</span><span class="sxs-lookup"><span data-stu-id="27133-1695">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="27133-1696">Для предоставления ApiRevisionDescription.</span><span class="sxs-lookup"><span data-stu-id="27133-1696">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="27133-1697">Для переопределения значения ServiceUrl при клонировании API.</span><span class="sxs-lookup"><span data-stu-id="27133-1697">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="27133-1698">Обновлен командлет **New-AzApiManagementIdentityProvider**:</span><span class="sxs-lookup"><span data-stu-id="27133-1698">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="27133-1699">Для настройки AAD или AADB2C с Authority.</span><span class="sxs-lookup"><span data-stu-id="27133-1699">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="27133-1700">Для установки политик SignupPolicy, SigninPolicy, ProfileEditingPolicy и PasswordResetPolicy.</span><span class="sxs-lookup"><span data-stu-id="27133-1700">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="27133-1701">Обновлен командлет **New-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="27133-1701">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="27133-1702">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="27133-1702">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="27133-1703">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="27133-1703">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="27133-1704">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="27133-1704">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="27133-1705">Обновлен командлет **Set-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="27133-1705">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="27133-1706">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="27133-1706">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="27133-1707">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="27133-1707">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="27133-1708">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="27133-1708">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="27133-1709">Следующие командлеты обновлены, чтобы принимать значение ResourceId в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="27133-1709">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="27133-1710">New-AzApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="27133-1710">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="27133-1711">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="27133-1711">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="27133-1712">Get-AzApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="27133-1712">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="27133-1713">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="27133-1713">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="27133-1714">Get-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="27133-1714">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="27133-1715">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="27133-1715">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="27133-1716">Get-AzApiManagementAuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="27133-1716">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="27133-1717">Get-AzApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="27133-1717">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="27133-1718">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="27133-1718">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="27133-1719">Get-AzApiManagementCertificate.</span><span class="sxs-lookup"><span data-stu-id="27133-1719">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="27133-1720">Remove-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="27133-1720">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="27133-1721">Remove-AzApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="27133-1721">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="27133-1722">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="27133-1722">Az.Automation</span></span>
* <span data-ttu-id="27133-1723">Обновлен командлет Get-AzAutomationJobOutputRecord для обработки значений в формате JSON и в виде текстовой записи.</span><span class="sxs-lookup"><span data-stu-id="27133-1723">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="27133-1724">исправлена проблема https://github.com/Azure/azure-powershell/issues/7977.</span><span class="sxs-lookup"><span data-stu-id="27133-1724">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="27133-1725">исправлена проблема https://github.com/Azure/azure-powershell/issues/8600.</span><span class="sxs-lookup"><span data-stu-id="27133-1725">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="27133-1726">Поведение командлета Start-AzAutomationDscCompilationJob изменено так, чтобы сразу же запустить задание, а не ждать его завершения.</span><span class="sxs-lookup"><span data-stu-id="27133-1726">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="27133-1727">исправлена проблема https://github.com/Azure/azure-powershell/issues/8347.</span><span class="sxs-lookup"><span data-stu-id="27133-1727">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="27133-1728">Исправлен командлет Get-AzAutomationDscNode, возвращающий все узлы при использовании -Name.</span><span class="sxs-lookup"><span data-stu-id="27133-1728">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="27133-1729">Теперь он возвращает только соответствующий узел.</span><span class="sxs-lookup"><span data-stu-id="27133-1729">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27133-1730">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27133-1730">Az.Compute</span></span>
* <span data-ttu-id="27133-1731">Добавлены параметры ProtectFromScaleIn и ProtectFromScaleSetAction для командлета Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="27133-1731">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="27133-1732">Командлет New-AzVM с простым набором параметров теперь по умолчанию использует доступное расположение, если регион "восточная часть США" не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="27133-1732">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="27133-1733">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27133-1733">Az.DataLakeStore</span></span>
* <span data-ttu-id="27133-1734">Обновлен пакет SDK ADLS для использования httpclient. В инфраструктуру Azure интегрирована проверка плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="27133-1734">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27133-1735">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27133-1735">Az.Monitor</span></span>
* <span data-ttu-id="27133-1736">Исправлены неправильные имена параметров в справочных примерах.</span><span class="sxs-lookup"><span data-stu-id="27133-1736">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27133-1737">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27133-1737">Az.Network</span></span>
* <span data-ttu-id="27133-1738">Добавлен флаг DisableBgpRoutePropagation для выходных данных действующей таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="27133-1738">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="27133-1739">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="27133-1739">Updated cmdlet:</span></span>
        - <span data-ttu-id="27133-1740">Get-AzEffectiveRouteTable.</span><span class="sxs-lookup"><span data-stu-id="27133-1740">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="27133-1741">Исправлен двойной дефис в документации New-AzApplicationGatewayTrustedRootCertificate.</span><span class="sxs-lookup"><span data-stu-id="27133-1741">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="27133-1742">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27133-1742">Az.Resources</span></span>
* <span data-ttu-id="27133-1743">Добавлен новый командлет Get-AzureRmDenyAssignment для получения запрещающих назначений.</span><span class="sxs-lookup"><span data-stu-id="27133-1743">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="27133-1744">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27133-1744">Az.Sql</span></span>
* <span data-ttu-id="27133-1745">Командлеты Расширенной защиты от угроз переименованы на командлеты Расширенной защиты данных, и оценка уязвимости включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="27133-1745">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="27133-1746">2.0.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="27133-1746">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27133-1747">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27133-1747">Az.Accounts</span></span>
* <span data-ttu-id="27133-1748">Обновлена библиотека аутентификации для устранения проблем с ADFS при использовании аутентификации на основе имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="27133-1748">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="27133-1749">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="27133-1749">Az.CognitiveServices</span></span>
* <span data-ttu-id="27133-1750">Отображается только заявление об отказе Bing для служб Поиска Bing.</span><span class="sxs-lookup"><span data-stu-id="27133-1750">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="27133-1751">Исправлена проблема с созданием учетной записи.</span><span class="sxs-lookup"><span data-stu-id="27133-1751">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27133-1752">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27133-1752">Az.Compute</span></span>
* <span data-ttu-id="27133-1753">Функция группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="27133-1753">Proximity placement group feature.</span></span>
    - <span data-ttu-id="27133-1754">Добавлены следующие новые командлеты:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="27133-1754">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="27133-1755">Новый параметр ProximityPlacementGroupId будет добавлен в следующие командлеты:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="27133-1755">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="27133-1756">В командлет New-AzGalleryImageVersion добавлен параметр StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="27133-1756">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="27133-1757">TargetRegion в командлете New-AzGalleryImageVersion может содержать StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="27133-1757">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="27133-1758">Параметр-переключатель SkipShutdown добавлен в командлеты Stop-AzVM и Stop-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="27133-1758">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="27133-1759">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="27133-1759">Breaking changes</span></span>
    - <span data-ttu-id="27133-1760">Командлет SET-AzVMBootDiagnostics изменен на Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="27133-1760">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="27133-1761">Командлет Export-AzLogAnalyticThrottledRequests изменен на Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="27133-1761">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="27133-1762">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="27133-1762">Az.DeploymentManager</span></span>
* <span data-ttu-id="27133-1763">Первая общедоступная версия командлетов диспетчера развертывания Azure</span><span class="sxs-lookup"><span data-stu-id="27133-1763">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="27133-1764">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="27133-1764">Az.Dns</span></span>
* <span data-ttu-id="27133-1765">Автоматическое делегирование DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="27133-1765">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="27133-1766">Командлет для создания зоны DNS принимает имя родительской зоны в качестве дополнительного необязательного параметра.</span><span class="sxs-lookup"><span data-stu-id="27133-1766">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="27133-1767">Он добавляет записи NS в родительской зоне для созданной дочерней зоны.</span><span class="sxs-lookup"><span data-stu-id="27133-1767">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="27133-1768">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="27133-1768">Az.FrontDoor</span></span>
* <span data-ttu-id="27133-1769">Первая общедоступная версия командлетов Azure FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="27133-1769">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="27133-1770">Переименованы командлеты WAF для включения Waf.</span><span class="sxs-lookup"><span data-stu-id="27133-1770">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="27133-1771">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="27133-1771">Az.HDInsight</span></span>
* <span data-ttu-id="27133-1772">Удалены два командлета:</span><span class="sxs-lookup"><span data-stu-id="27133-1772">Removed two cmdlets:</span></span>
    - <span data-ttu-id="27133-1773">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="27133-1773">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="27133-1774">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="27133-1774">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="27133-1775">Добавлен новый командлет Set-AzHDInsightGatewayCredential для замены Grant-AzHDInsightHttpServicesAccess.</span><span class="sxs-lookup"><span data-stu-id="27133-1775">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="27133-1776">Обновлен командлет Get-AzHDInsightJobOutput для различения ролей читателя и оператора HDInsight:</span><span class="sxs-lookup"><span data-stu-id="27133-1776">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="27133-1777">Пользователям с ролью читателя не нужно указывать параметр DefaultStorageAccountKey явным образом, иначе возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="27133-1777">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="27133-1778">На пользователей с ролью оператора HDInsight это не повлияет.</span><span class="sxs-lookup"><span data-stu-id="27133-1778">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27133-1779">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27133-1779">Az.Monitor</span></span>
* <span data-ttu-id="27133-1780">Новые командлеты для API SQR (запланированное правило запросов)</span><span class="sxs-lookup"><span data-stu-id="27133-1780">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="27133-1781">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="27133-1781">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="27133-1782">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="27133-1782">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="27133-1783">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="27133-1783">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="27133-1784">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="27133-1784">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="27133-1785">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="27133-1785">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="27133-1786">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="27133-1786">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="27133-1787">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="27133-1787">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="27133-1788">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="27133-1788">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="27133-1789">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="27133-1789">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="27133-1790">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="27133-1790">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="27133-1791">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="27133-1791">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="27133-1792">См. подробнее об [API SQR](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules).</span><span class="sxs-lookup"><span data-stu-id="27133-1792">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="27133-1793">Обновлен файл Az.Monitor.md для включения командлетов для правила генерации оповещений на основе метрик GenV2(не классическая версия).</span><span class="sxs-lookup"><span data-stu-id="27133-1793">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27133-1794">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27133-1794">Az.Network</span></span>
* <span data-ttu-id="27133-1795">Добавлена поддержка для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="27133-1795">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="27133-1796">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="27133-1796">New cmdlets</span></span>
        - <span data-ttu-id="27133-1797">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="27133-1797">New-AzNatGateway</span></span>
        - <span data-ttu-id="27133-1798">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="27133-1798">Get-AzNatGateway</span></span>
        - <span data-ttu-id="27133-1799">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="27133-1799">Set-AzNatGateway</span></span>
        - <span data-ttu-id="27133-1800">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="27133-1800">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="27133-1801">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="27133-1801">Updated cmdlets</span></span>
        - <span data-ttu-id="27133-1802">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="27133-1802">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="27133-1803">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="27133-1803">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="27133-1804">Обновлены следующие команды для функции: Настройка и удаление пользовательских маршрутов через шлюз в Бруклине.</span><span class="sxs-lookup"><span data-stu-id="27133-1804">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="27133-1805">Обновлен командлет New-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="27133-1805">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="27133-1806">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="27133-1806">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="27133-1807">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="27133-1807">Az.PolicyInsights</span></span>
* <span data-ttu-id="27133-1808">Добавлена поддержка сведений об оценке политики запросов.</span><span class="sxs-lookup"><span data-stu-id="27133-1808">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="27133-1809">Добавлен параметр -Expand в командлет Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="27133-1809">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="27133-1810">Добавлена поддержка -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="27133-1810">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27133-1811">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27133-1811">Az.RecoveryServices</span></span>
* <span data-ttu-id="27133-1812">Добавлена поддержка перекрестной подписки на Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="27133-1812">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="27133-1813">Добавлена возможность отмечать предстоящие критически важные изменения для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="27133-1813">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="27133-1814">Исправлены план восстановления и план действий для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="27133-1814">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="27133-1815">Исправлено сетевое сопоставление обновления Azure Site Recovery (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="27133-1815">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="27133-1816">Исправлено направление защиты обновления Azure Site Recovery для управляемых дисков (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="27133-1816">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="27133-1817">Добавлены другие незначительные исправления.</span><span class="sxs-lookup"><span data-stu-id="27133-1817">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="27133-1818">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="27133-1818">Az.Relay</span></span>
* <span data-ttu-id="27133-1819">Исправлены опечатки в сообщениях для клиентов.</span><span class="sxs-lookup"><span data-stu-id="27133-1819">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="27133-1820">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="27133-1820">Az.ServiceBus</span></span>
* <span data-ttu-id="27133-1821">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="27133-1821">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27133-1822">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27133-1822">Az.Storage</span></span>
* <span data-ttu-id="27133-1823">Выполнено обновление клиентской библиотеки хранилища до версии 10.0.1 (пространство имен всех объектов из этого пакета SDK изменено с Microsoft.WindowsAzure.Storage. *на Microsoft.Azure.Storage*).</span><span class="sxs-lookup"><span data-stu-id="27133-1823">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="27133-1824">Выполнено обновление до Microsoft.Azure.Management.Storage версии 11.0.0 для включения поддержки нового API версии 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="27133-1824">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="27133-1825">Значение свойства Kind по умолчанию в учетной записи хранения изменено со Storage на StorageV2.</span><span class="sxs-lookup"><span data-stu-id="27133-1825">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="27133-1826">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27133-1826">New-AzStorageAccount</span></span>
* <span data-ttu-id="27133-1827">Изменено значение Sku.Name в выходных данных командлета учетной записи хранения в соответствии со значением Sku.Name во входных данных путем добавления _ (например, StandardLRS изменено на Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="27133-1827">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="27133-1828">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27133-1828">New-AzStorageAccount</span></span>
    - <span data-ttu-id="27133-1829">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27133-1829">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="27133-1830">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27133-1830">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27133-1831">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27133-1831">Az.Websites</span></span>
* <span data-ttu-id="27133-1832">Свойство Kind теперь будет задаваться объектам PSSite, возвращаемым командлетом Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="27133-1832">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="27133-1833">Get-AzWebApp\*Metrics и Get-AzAppServicePlanMetrics считаются нерекомендуемыми.</span><span class="sxs-lookup"><span data-stu-id="27133-1833">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="27133-1834">1.8.0 — апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="27133-1834">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="27133-1835">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="27133-1835">Highlights since the last major release</span></span>
* <span data-ttu-id="27133-1836">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="27133-1836">General availability of `Az` module</span></span>
* <span data-ttu-id="27133-1837">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="27133-1837">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="27133-1838">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="27133-1838">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="27133-1839">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="27133-1839">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="27133-1840">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="27133-1840">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="27133-1841">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="27133-1841">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="27133-1842">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="27133-1842">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="27133-1843">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27133-1843">Az.Accounts</span></span>
* <span data-ttu-id="27133-1844">Обновлен командлет Uninstall-AzureRm для правильного удаления модулей в Mac.</span><span class="sxs-lookup"><span data-stu-id="27133-1844">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="27133-1845">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="27133-1845">Az.Batch</span></span>
* <span data-ttu-id="27133-1846">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="27133-1846">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="27133-1847">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="27133-1847">Az.Cdn</span></span>
* <span data-ttu-id="27133-1848">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="27133-1848">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="27133-1849">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="27133-1849">Az.CognitiveServices</span></span>
* <span data-ttu-id="27133-1850">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="27133-1850">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27133-1851">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27133-1851">Az.Compute</span></span>
* <span data-ttu-id="27133-1852">Устранена проблема с установкой AEM, если в идентификаторах ресурсов дисков группа ресурсов указана в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="27133-1852">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="27133-1853">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="27133-1853">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="27133-1854">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="27133-1854">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27133-1855">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27133-1855">Az.DataFactory</span></span>
* <span data-ttu-id="27133-1856">Добавлены свойства SsisProperties, если NodeCount не имеет значения NULL для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="27133-1856">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="27133-1857">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27133-1857">Az.DataLakeStore</span></span>
* <span data-ttu-id="27133-1858">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="27133-1858">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="27133-1859">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="27133-1859">Az.EventGrid</span></span>
* <span data-ttu-id="27133-1860">Обновлен текст справки для конечной точки, указывающий, что необходимо создать ресурсы, прежде чем использовать командлеты для создания или обновления подписки на события.</span><span class="sxs-lookup"><span data-stu-id="27133-1860">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="27133-1861">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="27133-1861">Az.EventHub</span></span>
* <span data-ttu-id="27133-1862">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="27133-1862">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="27133-1863">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="27133-1863">Az.HDInsight</span></span>
* <span data-ttu-id="27133-1864">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="27133-1864">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="27133-1865">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="27133-1865">Az.IotHub</span></span>
* <span data-ttu-id="27133-1866">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="27133-1866">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="27133-1867">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27133-1867">Az.KeyVault</span></span>
* <span data-ttu-id="27133-1868">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="27133-1868">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="27133-1869">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="27133-1869">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="27133-1870">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="27133-1870">Az.MachineLearning</span></span>
* <span data-ttu-id="27133-1871">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="27133-1871">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="27133-1872">Az.Media</span><span class="sxs-lookup"><span data-stu-id="27133-1872">Az.Media</span></span>
* <span data-ttu-id="27133-1873">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="27133-1873">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27133-1874">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27133-1874">Az.Monitor</span></span>
  * <span data-ttu-id="27133-1875">Добавлены новые командлеты для правила генерации оповещений на основе метрик GenV2 (не классических).</span><span class="sxs-lookup"><span data-stu-id="27133-1875">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="27133-1876">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="27133-1876">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="27133-1877">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="27133-1877">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="27133-1878">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="27133-1878">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="27133-1879">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="27133-1879">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="27133-1880">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="27133-1880">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="27133-1881">Обновлен пакет SDK Monitor до предварительной версии 0.22.0.</span><span class="sxs-lookup"><span data-stu-id="27133-1881">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27133-1882">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27133-1882">Az.Network</span></span>
* <span data-ttu-id="27133-1883">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="27133-1883">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="27133-1884">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="27133-1884">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="27133-1885">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="27133-1885">Az.NotificationHubs</span></span>
* <span data-ttu-id="27133-1886">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="27133-1886">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="27133-1887">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="27133-1887">Az.OperationalInsights</span></span>
* <span data-ttu-id="27133-1888">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="27133-1888">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="27133-1889">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="27133-1889">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="27133-1890">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="27133-1890">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27133-1891">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27133-1891">Az.RecoveryServices</span></span>
* <span data-ttu-id="27133-1892">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="27133-1892">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="27133-1893">Обновлен табличный формат для SQL на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="27133-1893">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="27133-1894">Добавлен альтернативный метод для получения расположения в Общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="27133-1894">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="27133-1895">Обновлено значение ScheduleRunDays в объекте SchedulePolicy в соответствии с часовым поясом.</span><span class="sxs-lookup"><span data-stu-id="27133-1895">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="27133-1896">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="27133-1896">Az.RedisCache</span></span>
* <span data-ttu-id="27133-1897">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="27133-1897">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="27133-1898">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27133-1898">Az.Resources</span></span>
* <span data-ttu-id="27133-1899">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="27133-1899">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="27133-1900">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27133-1900">Az.Sql</span></span>
* <span data-ttu-id="27133-1901">Заменена зависимость от пакета SDK монитора на обычный код.</span><span class="sxs-lookup"><span data-stu-id="27133-1901">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="27133-1902">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="27133-1902">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="27133-1903">Улучшен процесс классификации нескольких столбцов.</span><span class="sxs-lookup"><span data-stu-id="27133-1903">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="27133-1904">Добавлены свойства SKU (имя, семейство, производительность SKU) в отклике Get-AzSqlServerServiceObjective, а также по умолчанию задан табличный формат.</span><span class="sxs-lookup"><span data-stu-id="27133-1904">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="27133-1905">C помощью Get-AzSqlServerServiceObjective теперь можно получать список доступных целевых служб по расположению без необходимости заранее размещать сервер в регионе.</span><span class="sxs-lookup"><span data-stu-id="27133-1905">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="27133-1906">Поддерживается параметр часового пояса при создании Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="27133-1906">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="27133-1907">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="27133-1907">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27133-1908">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27133-1908">Az.Websites</span></span>
* <span data-ttu-id="27133-1909">Исправлены командлеты Set-AzWebApp и Set-AzWebAppSlot, которые теперь не удаляют теги при выполнении.</span><span class="sxs-lookup"><span data-stu-id="27133-1909">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="27133-1910">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="27133-1910">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="27133-1911">Обновлен пакет SDK веб-узлов.</span><span class="sxs-lookup"><span data-stu-id="27133-1911">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="27133-1912">Удалено свойство AdminSiteName из PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="27133-1912">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="27133-1913">1.7.0 —апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="27133-1913">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="27133-1914">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="27133-1914">Highlights since the last major release</span></span>
* <span data-ttu-id="27133-1915">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="27133-1915">General availability of `Az` module</span></span>
* <span data-ttu-id="27133-1916">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="27133-1916">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="27133-1917">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="27133-1917">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="27133-1918">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="27133-1918">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="27133-1919">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="27133-1919">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="27133-1920">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="27133-1920">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="27133-1921">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="27133-1921">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="27133-1922">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27133-1922">Az.Accounts</span></span>
* <span data-ttu-id="27133-1923">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметр AzureAnalysisServicesEndpointResourceId.</span><span class="sxs-lookup"><span data-stu-id="27133-1923">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="27133-1924">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="27133-1924">Az.AnalysisServices</span></span>
* <span data-ttu-id="27133-1925">Использование ServiceClient в командлетах плоскости данных и удаление исходной логики проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="27133-1925">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="27133-1926">Add-AzureASAccount используется как оболочка для Connect-AzAccount во избежание критических изменений.</span><span class="sxs-lookup"><span data-stu-id="27133-1926">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="27133-1927">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="27133-1927">Az.Automation</span></span>
* <span data-ttu-id="27133-1928">Исправлена ошибка командлета New-AzAutomationSoftwareUpdateConfiguration, связанная с включением.</span><span class="sxs-lookup"><span data-stu-id="27133-1928">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="27133-1929">Теперь параметры IncludedKbNumber и IncludedPackageNameMask должны работать нормально.</span><span class="sxs-lookup"><span data-stu-id="27133-1929">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="27133-1930">Исправлена ошибка динамической группы управления обновлениями службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="27133-1930">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27133-1931">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27133-1931">Az.Compute</span></span>
* <span data-ttu-id="27133-1932">В командлеты New-AzDiskConfig и New-AzSnapshotConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="27133-1932">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="27133-1933">Теперь можно создавать виртуальные машину на основе образов из коллекции от других клиентов.</span><span class="sxs-lookup"><span data-stu-id="27133-1933">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="27133-1934">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="27133-1934">Az.ContainerInstance</span></span>
* <span data-ttu-id="27133-1935">Исправлена проблема в параметре -Command командлета New-AzContainerGroup, из-за которой в конце добавлялся пустой аргумент.</span><span class="sxs-lookup"><span data-stu-id="27133-1935">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27133-1936">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27133-1936">Az.DataFactory</span></span>
* <span data-ttu-id="27133-1937">Пакет SDK для ADF .NET обновлен до версии 3.0.2.</span><span class="sxs-lookup"><span data-stu-id="27133-1937">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="27133-1938">Командлет Set-AzDataFactoryV2 обновлен с помощью дополнительных параметров для настроек, связанных с RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="27133-1938">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="27133-1939">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27133-1939">Az.Resources</span></span>
* <span data-ttu-id="27133-1940">Улучшена обработка поставщиков Get-AzResource при предоставлении параметров -ResourceId или -ResourceGroupName, -Name и -ResourceType.</span><span class="sxs-lookup"><span data-stu-id="27133-1940">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="27133-1941">Улучшена обработка ошибок в командлетах Test-AzDeployment и Test-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="27133-1941">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="27133-1942">Теперь ошибки, возникающие за пределами проверки развертывания, обрабатываются и включаются в выходные данные команды.</span><span class="sxs-lookup"><span data-stu-id="27133-1942">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="27133-1943">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="27133-1943">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="27133-1944">Добавлен параметр-переключатель -IgnoreDynamicParameters, с помощью которого можно настроить командлеты развертывания так, чтобы они пропускали запросы в сценариях скриптов и заданий.</span><span class="sxs-lookup"><span data-stu-id="27133-1944">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="27133-1945">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="27133-1945">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="27133-1946">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27133-1946">Az.Sql</span></span>
* <span data-ttu-id="27133-1947">Поддержка классификации данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="27133-1947">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27133-1948">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27133-1948">Az.Storage</span></span>
* <span data-ttu-id="27133-1949">Подробные сообщения об ошибке передаются при создании контекста хранилища с помощью параметра -UseConnectedAccount, но без входа в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="27133-1949">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="27133-1950">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="27133-1950">New-AzStorageContext</span></span>
* <span data-ttu-id="27133-1951">Поддержка свойств службы управления BLOB-объектов в указанной учетной записи хранения с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="27133-1951">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="27133-1952">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="27133-1952">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="27133-1953">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="27133-1953">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="27133-1954">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="27133-1954">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="27133-1955">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="27133-1955">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="27133-1956">Поддержка параметра -AsJob в командлетах для отправки и скачивания больших двоичных объектов и файлов.</span><span class="sxs-lookup"><span data-stu-id="27133-1956">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="27133-1957">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="27133-1957">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="27133-1958">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="27133-1958">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="27133-1959">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="27133-1959">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="27133-1960">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="27133-1960">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="27133-1961">1.6.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="27133-1961">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="27133-1962">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="27133-1962">Highlights since the last major release</span></span>
* <span data-ttu-id="27133-1963">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="27133-1963">General availability of `Az` module</span></span>
* <span data-ttu-id="27133-1964">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="27133-1964">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="27133-1965">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="27133-1965">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="27133-1966">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="27133-1966">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="27133-1967">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="27133-1967">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="27133-1968">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="27133-1968">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="27133-1969">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="27133-1969">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="27133-1970">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="27133-1970">Az.Automation</span></span>
* <span data-ttu-id="27133-1971">В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:</span><span class="sxs-lookup"><span data-stu-id="27133-1971">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="27133-1972">динамическое группирование;</span><span class="sxs-lookup"><span data-stu-id="27133-1972">Dynamic grouping</span></span>
    * <span data-ttu-id="27133-1973">скрипты предварительного или последующего выполнения;</span><span class="sxs-lookup"><span data-stu-id="27133-1973">Pre-Post script</span></span>
    * <span data-ttu-id="27133-1974">параметр перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="27133-1974">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27133-1975">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27133-1975">Az.Compute</span></span>
* <span data-ttu-id="27133-1976">Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.</span><span class="sxs-lookup"><span data-stu-id="27133-1976">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="27133-1977">Обновление клиентской библиотеки вычислений до версии 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="27133-1977">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="27133-1978">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27133-1978">Az.KeyVault</span></span>
* <span data-ttu-id="27133-1979">Добавлена поддержка подстановочных знаков в командлетах KeyVault.</span><span class="sxs-lookup"><span data-stu-id="27133-1979">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27133-1980">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27133-1980">Az.Network</span></span>
* <span data-ttu-id="27133-1981">Добавлена поддержка анализа угроз для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="27133-1981">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="27133-1982">Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="27133-1982">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27133-1983">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27133-1983">Az.RecoveryServices</span></span>
* <span data-ttu-id="27133-1984">В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.</span><span class="sxs-lookup"><span data-stu-id="27133-1984">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="27133-1985">Добавлена поддержка канала для отмены регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="27133-1985">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="27133-1986">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27133-1986">Az.Resources</span></span>
* <span data-ttu-id="27133-1987">Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="27133-1987">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="27133-1988">Обновлены учетные данные, используемые при общих вызовах к ARM.</span><span class="sxs-lookup"><span data-stu-id="27133-1988">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="27133-1989">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27133-1989">Az.Sql</span></span>
* <span data-ttu-id="27133-1990">Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="27133-1990">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27133-1991">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27133-1991">Az.Storage</span></span>
* <span data-ttu-id="27133-1992">Поддержка получения, настройки и удаления политики управления в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="27133-1992">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="27133-1993">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="27133-1993">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="27133-1994">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="27133-1994">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="27133-1995">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="27133-1995">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="27133-1996">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="27133-1996">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="27133-1997">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="27133-1997">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="27133-1998">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="27133-1998">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27133-1999">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27133-1999">Az.Websites</span></span>
* <span data-ttu-id="27133-2000">Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="27133-2000">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="27133-2001">1.5.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="27133-2001">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27133-2002">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27133-2002">Az.Accounts</span></span>
* <span data-ttu-id="27133-2003">Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.</span><span class="sxs-lookup"><span data-stu-id="27133-2003">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="27133-2004">Обновлены примеры для Connect AzAccount.</span><span class="sxs-lookup"><span data-stu-id="27133-2004">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="27133-2005">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="27133-2005">Az.Automation</span></span>
* <span data-ttu-id="27133-2006">Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="27133-2006">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="27133-2007">Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов.</span><span class="sxs-lookup"><span data-stu-id="27133-2007">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="27133-2008">Теперь он возвращает все узлы.</span><span class="sxs-lookup"><span data-stu-id="27133-2008">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="27133-2009">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="27133-2009">Az.Cdn</span></span>
* <span data-ttu-id="27133-2010">Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.</span><span class="sxs-lookup"><span data-stu-id="27133-2010">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27133-2011">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27133-2011">Az.Compute</span></span>
* <span data-ttu-id="27133-2012">Добавлена поддержка подстановочных знаков в командлетах Get.</span><span class="sxs-lookup"><span data-stu-id="27133-2012">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27133-2013">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27133-2013">Az.DataFactory</span></span>
* <span data-ttu-id="27133-2014">Обновлен пакет SDK для ADF .NET до версии 3.0.1.</span><span class="sxs-lookup"><span data-stu-id="27133-2014">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="27133-2015">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="27133-2015">Az.LogicApp</span></span>
* <span data-ttu-id="27133-2016">Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.</span><span class="sxs-lookup"><span data-stu-id="27133-2016">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27133-2017">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27133-2017">Az.Network</span></span>
* <span data-ttu-id="27133-2018">Добавлена поддержка подстановочных знаков в командлетах Network.</span><span class="sxs-lookup"><span data-stu-id="27133-2018">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27133-2019">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27133-2019">Az.RecoveryServices</span></span>
* <span data-ttu-id="27133-2020">Добавлена поддержка SQL Server на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="27133-2020">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="27133-2021">Обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="27133-2021">SDK Update</span></span>
* <span data-ttu-id="27133-2022">Удалена проверка VMappContainer в Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="27133-2022">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="27133-2023">Добавлены параметры Name и ServerName для Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="27133-2023">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="27133-2024">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27133-2024">Az.Resources</span></span>
* <span data-ttu-id="27133-2025">Добавлен параметр `-TemplateObject` в командлеты для развертывания.</span><span class="sxs-lookup"><span data-stu-id="27133-2025">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="27133-2026">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.</span><span class="sxs-lookup"><span data-stu-id="27133-2026">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="27133-2027">Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="27133-2027">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="27133-2028">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.</span><span class="sxs-lookup"><span data-stu-id="27133-2028">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="27133-2029">Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="27133-2029">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="27133-2030">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.</span><span class="sxs-lookup"><span data-stu-id="27133-2030">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="27133-2031">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27133-2031">Az.Sql</span></span>
* <span data-ttu-id="27133-2032">Обновление AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="27133-2032">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="27133-2033">Исправлено поведение для пограничного случая при создании параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="27133-2033">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27133-2034">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27133-2034">Az.Storage</span></span>
* <span data-ttu-id="27133-2035">Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="27133-2035">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="27133-2036">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="27133-2036">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="27133-2037">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="27133-2037">Az.AnalysisServices</span></span>
* <span data-ttu-id="27133-2038">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="27133-2038">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="27133-2039">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="27133-2039">Az.Automation</span></span>
* <span data-ttu-id="27133-2040">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="27133-2040">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="27133-2041">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="27133-2041">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="27133-2042">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="27133-2042">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="27133-2043">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="27133-2043">Az.CognitiveServices</span></span>
* <span data-ttu-id="27133-2044">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="27133-2044">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27133-2045">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27133-2045">Az.Compute</span></span>
* <span data-ttu-id="27133-2046">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="27133-2046">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="27133-2047">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="27133-2047">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="27133-2048">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="27133-2048">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="27133-2049">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="27133-2049">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="27133-2050">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27133-2050">Az.DataLakeStore</span></span>
* <span data-ttu-id="27133-2051">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="27133-2051">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="27133-2052">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="27133-2052">Az.EventHub</span></span>
* <span data-ttu-id="27133-2053">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="27133-2053">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="27133-2054">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27133-2054">Az.KeyVault</span></span>
* <span data-ttu-id="27133-2055">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="27133-2055">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="27133-2056">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="27133-2056">Az.LogicApp</span></span>
* <span data-ttu-id="27133-2057">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="27133-2057">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="27133-2058">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="27133-2058">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="27133-2059">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="27133-2059">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="27133-2060">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="27133-2060">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="27133-2061">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="27133-2061">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="27133-2062">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="27133-2062">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="27133-2063">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="27133-2063">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="27133-2064">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="27133-2064">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="27133-2065">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="27133-2065">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="27133-2066">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="27133-2066">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="27133-2067">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="27133-2067">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="27133-2068">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="27133-2068">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="27133-2069">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="27133-2069">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27133-2070">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27133-2070">Az.Monitor</span></span>
* <span data-ttu-id="27133-2071">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="27133-2071">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27133-2072">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27133-2072">Az.Network</span></span>
* <span data-ttu-id="27133-2073">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="27133-2073">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="27133-2074">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="27133-2074">Az.OperationalInsights</span></span>
* <span data-ttu-id="27133-2075">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="27133-2075">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="27133-2076">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="27133-2076">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="27133-2077">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="27133-2077">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="27133-2078">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27133-2078">Az.Resources</span></span>
* <span data-ttu-id="27133-2079">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="27133-2079">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="27133-2080">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="27133-2080">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="27133-2081">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="27133-2081">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="27133-2082">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="27133-2082">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="27133-2083">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27133-2083">Az.Sql</span></span>
* <span data-ttu-id="27133-2084">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="27133-2084">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="27133-2085">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="27133-2085">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27133-2086">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27133-2086">Az.Websites</span></span>
* <span data-ttu-id="27133-2087">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="27133-2087">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="27133-2088">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="27133-2088">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27133-2089">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27133-2089">Az.Accounts</span></span>
* <span data-ttu-id="27133-2090">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="27133-2090">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="27133-2091">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="27133-2091">Az.AnalysisServices</span></span>
<span data-ttu-id="27133-2092">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="27133-2092">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27133-2093">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27133-2093">Az.Compute</span></span>
* <span data-ttu-id="27133-2094">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="27133-2094">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="27133-2095">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="27133-2095">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="27133-2096">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="27133-2096">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27133-2097">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27133-2097">Az.RecoveryServices</span></span>
<span data-ttu-id="27133-2098">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="27133-2098">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="27133-2099">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27133-2099">Az.Resources</span></span>
* <span data-ttu-id="27133-2100">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="27133-2100">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="27133-2101">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="27133-2101">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="27133-2102">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="27133-2102">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="27133-2103">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="27133-2103">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="27133-2104">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27133-2104">Az.Sql</span></span>
* <span data-ttu-id="27133-2105">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="27133-2105">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="27133-2106">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="27133-2106">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="27133-2107">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="27133-2107">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="27133-2108">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="27133-2108">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27133-2109">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27133-2109">Az.Accounts</span></span>
* <span data-ttu-id="27133-2110">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="27133-2110">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="27133-2111">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="27133-2111">Az.AnalysisServices</span></span>
* <span data-ttu-id="27133-2112">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="27133-2112">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27133-2113">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27133-2113">Az.RecoveryServices</span></span>
* <span data-ttu-id="27133-2114">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="27133-2114">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="27133-2115">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="27133-2115">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27133-2116">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27133-2116">Az.Accounts</span></span>
* <span data-ttu-id="27133-2117">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="27133-2117">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="27133-2118">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="27133-2118">Update incorrect online help URLs</span></span>
* <span data-ttu-id="27133-2119">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="27133-2119">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="27133-2120">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="27133-2120">Az.Aks</span></span>
* <span data-ttu-id="27133-2121">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="27133-2121">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="27133-2122">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="27133-2122">Az.Automation</span></span>
* <span data-ttu-id="27133-2123">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="27133-2123">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="27133-2124">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="27133-2124">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="27133-2125">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="27133-2125">Az.Cdn</span></span>
* <span data-ttu-id="27133-2126">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="27133-2126">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27133-2127">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27133-2127">Az.Compute</span></span>
* <span data-ttu-id="27133-2128">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="27133-2128">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="27133-2129">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="27133-2129">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="27133-2130">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="27133-2130">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="27133-2131">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="27133-2131">Az.ContainerRegistry</span></span>
* <span data-ttu-id="27133-2132">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="27133-2132">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27133-2133">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27133-2133">Az.DataFactory</span></span>
* <span data-ttu-id="27133-2134">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="27133-2134">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="27133-2135">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27133-2135">Az.DataLakeStore</span></span>
* <span data-ttu-id="27133-2136">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="27133-2136">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="27133-2137">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="27133-2137">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="27133-2138">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="27133-2138">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="27133-2139">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="27133-2139">Az.IotHub</span></span>
* <span data-ttu-id="27133-2140">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="27133-2140">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="27133-2141">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27133-2141">Az.KeyVault</span></span>
* <span data-ttu-id="27133-2142">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="27133-2142">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27133-2143">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27133-2143">Az.Network</span></span>
* <span data-ttu-id="27133-2144">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="27133-2144">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="27133-2145">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27133-2145">Az.Resources</span></span>
* <span data-ttu-id="27133-2146">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="27133-2146">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="27133-2147">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="27133-2147">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="27133-2148">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="27133-2148">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="27133-2149">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="27133-2149">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="27133-2150">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="27133-2150">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="27133-2151">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="27133-2151">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="27133-2152">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="27133-2152">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="27133-2153">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="27133-2153">Az.ServiceFabric</span></span>
* <span data-ttu-id="27133-2154">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="27133-2154">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="27133-2155">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="27133-2155">Fix some error messages.</span></span>
* <span data-ttu-id="27133-2156">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="27133-2156">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="27133-2157">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="27133-2157">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="27133-2158">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="27133-2158">Az.SignalR</span></span>
* <span data-ttu-id="27133-2159">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="27133-2159">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="27133-2160">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27133-2160">Az.Sql</span></span>
* <span data-ttu-id="27133-2161">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="27133-2161">Update incorrect online help URLs</span></span>
* <span data-ttu-id="27133-2162">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="27133-2162">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="27133-2163">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="27133-2163">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="27133-2164">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="27133-2164">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27133-2165">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27133-2165">Az.Storage</span></span>
* <span data-ttu-id="27133-2166">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="27133-2166">Update incorrect online help URLs</span></span>
* <span data-ttu-id="27133-2167">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="27133-2167">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="27133-2168">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="27133-2168">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="27133-2169">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="27133-2169">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="27133-2170">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="27133-2170">Az.TrafficManager</span></span>
* <span data-ttu-id="27133-2171">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="27133-2171">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27133-2172">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27133-2172">Az.Websites</span></span>
* <span data-ttu-id="27133-2173">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="27133-2173">Update incorrect online help URLs</span></span>
* <span data-ttu-id="27133-2174">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="27133-2174">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="27133-2175">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="27133-2175">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="27133-2176">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="27133-2176">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27133-2177">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27133-2177">Az.Accounts</span></span>
* <span data-ttu-id="27133-2178">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="27133-2178">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27133-2179">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27133-2179">Az.Compute</span></span>
* <span data-ttu-id="27133-2180">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="27133-2180">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="27133-2181">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="27133-2181">Updated the description of ID in help files</span></span>
* <span data-ttu-id="27133-2182">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="27133-2182">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="27133-2183">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27133-2183">Az.DataLakeStore</span></span>
* <span data-ttu-id="27133-2184">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="27133-2184">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="27133-2185">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="27133-2185">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="27133-2186">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="27133-2186">Az.EventGrid</span></span>
* <span data-ttu-id="27133-2187">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="27133-2187">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="27133-2188">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="27133-2188">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="27133-2189">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="27133-2189">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="27133-2190">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="27133-2190">Event Time-To-Live,</span></span>
        - <span data-ttu-id="27133-2191">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="27133-2191">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="27133-2192">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="27133-2192">Dead letter endpoint.</span></span>
    - <span data-ttu-id="27133-2193">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="27133-2193">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="27133-2194">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="27133-2194">Event Time-To-Live,</span></span>
        - <span data-ttu-id="27133-2195">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="27133-2195">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="27133-2196">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="27133-2196">Dead letter endpoint.</span></span>
* <span data-ttu-id="27133-2197">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="27133-2197">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="27133-2198">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="27133-2198">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="27133-2199">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="27133-2199">Az.IotHub</span></span>
* <span data-ttu-id="27133-2200">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="27133-2200">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="27133-2201">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="27133-2201">Az.LogicApp</span></span>
* <span data-ttu-id="27133-2202">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="27133-2202">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="27133-2203">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27133-2203">Az.Resources</span></span>
* <span data-ttu-id="27133-2204">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="27133-2204">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="27133-2205">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="27133-2205">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="27133-2206">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="27133-2206">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="27133-2207">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="27133-2207">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="27133-2208">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="27133-2208">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="27133-2209">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="27133-2209">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="27133-2210">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="27133-2210">Az.SignalR</span></span>
* <span data-ttu-id="27133-2211">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="27133-2211">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="27133-2212">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27133-2212">Az.Sql</span></span>
* <span data-ttu-id="27133-2213">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="27133-2213">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27133-2214">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27133-2214">Az.Storage</span></span>
* <span data-ttu-id="27133-2215">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="27133-2215">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="27133-2216">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="27133-2216">New-AzStorageContext</span></span>
* <span data-ttu-id="27133-2217">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="27133-2217">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="27133-2218">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="27133-2218">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27133-2219">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27133-2219">Az.Websites</span></span>
* <span data-ttu-id="27133-2220">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="27133-2220">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="27133-2221">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="27133-2221">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="27133-2222">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="27133-2222">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="27133-2223">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="27133-2223">General</span></span>

- <span data-ttu-id="27133-2224">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="27133-2224">General Availability of Az Module</span></span>
- <span data-ttu-id="27133-2225">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="27133-2225">Online help for each module</span></span>
- <span data-ttu-id="27133-2226">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="27133-2226">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="27133-2227">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="27133-2227">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="27133-2228">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27133-2228">Az.Accounts</span></span>
- <span data-ttu-id="27133-2229">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="27133-2229">Changed from Az.Profile</span></span>
- <span data-ttu-id="27133-2230">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="27133-2230">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="27133-2231">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="27133-2231">Az.ApiManagement</span></span>
- <span data-ttu-id="27133-2232">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="27133-2232">Fixes for #7002</span></span>
- <span data-ttu-id="27133-2233">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="27133-2233">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="27133-2234">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="27133-2234">Az.Batch</span></span>
- <span data-ttu-id="27133-2235">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="27133-2235">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="27133-2236">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="27133-2236">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="27133-2237">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="27133-2237">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="27133-2238">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="27133-2238">Az.Billing</span></span>
- <span data-ttu-id="27133-2239">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="27133-2239">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="27133-2240">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="27133-2240">Az.CognitivServices</span></span>
- <span data-ttu-id="27133-2241">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="27133-2241">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="27133-2242">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="27133-2242">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="27133-2243">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="27133-2243">Az.ContainerInstance</span></span>
- <span data-ttu-id="27133-2244">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="27133-2244">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="27133-2245">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="27133-2245">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="27133-2246">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="27133-2246">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="27133-2247">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27133-2247">Az.DataLakeStore</span></span>
- <span data-ttu-id="27133-2248">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="27133-2248">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="27133-2249">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27133-2249">Az.Monitor</span></span>
- <span data-ttu-id="27133-2250">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="27133-2250">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="27133-2251">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27133-2251">Az.KeyVault</span></span>
- <span data-ttu-id="27133-2252">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="27133-2252">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="27133-2253">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="27133-2253">Az.MachineLearning</span></span>
- <span data-ttu-id="27133-2254">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="27133-2254">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="27133-2255">Az.Media</span><span class="sxs-lookup"><span data-stu-id="27133-2255">Az.Media</span></span>
- <span data-ttu-id="27133-2256">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="27133-2256">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="27133-2257">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27133-2257">Az.Network</span></span>
<span data-ttu-id="27133-2258">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="27133-2258">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="27133-2259">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="27133-2259">New cmdlets added:</span></span>
        - <span data-ttu-id="27133-2260">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="27133-2260">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="27133-2261">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="27133-2261">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="27133-2262">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="27133-2262">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="27133-2263">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="27133-2263">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="27133-2264">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="27133-2264">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="27133-2265">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="27133-2265">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="27133-2266">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="27133-2266">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="27133-2267">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="27133-2267">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="27133-2268">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="27133-2268">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="27133-2269">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="27133-2269">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="27133-2270">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="27133-2270">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="27133-2271">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="27133-2271">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="27133-2272">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="27133-2272">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="27133-2273">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="27133-2273">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="27133-2274">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="27133-2274">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="27133-2275">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="27133-2275">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="27133-2276">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="27133-2276">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="27133-2277">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="27133-2277">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="27133-2278">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="27133-2278">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="27133-2279">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="27133-2279">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="27133-2280">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="27133-2280">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="27133-2281">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="27133-2281">Az.OperationalInsights</span></span>
- <span data-ttu-id="27133-2282">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="27133-2282">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="27133-2283">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="27133-2283">Az.Profile</span></span>
- <span data-ttu-id="27133-2284">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="27133-2284">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="27133-2285">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27133-2285">Az.RecoveryServices</span></span>
- <span data-ttu-id="27133-2286">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="27133-2286">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="27133-2287">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27133-2287">Az.Resources</span></span>
- <span data-ttu-id="27133-2288">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="27133-2288">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="27133-2289">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="27133-2289">Az.ServiceFabric</span></span>
- <span data-ttu-id="27133-2290">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="27133-2290">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="27133-2291">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="27133-2291">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="27133-2292">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="27133-2292">Az.SIgnalR</span></span>
- <span data-ttu-id="27133-2293">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="27133-2293">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="27133-2294">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27133-2294">Az.Sql</span></span>
- <span data-ttu-id="27133-2295">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="27133-2295">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="27133-2296">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="27133-2296">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="27133-2297">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="27133-2297">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="27133-2298">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27133-2298">Az.Storage</span></span>
- <span data-ttu-id="27133-2299">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="27133-2299">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="27133-2300">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27133-2300">Az.Websites</span></span>
- <span data-ttu-id="27133-2301">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="27133-2301">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="27133-2302">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="27133-2302">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="27133-2303">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="27133-2303">General</span></span>

* <span data-ttu-id="27133-2304">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="27133-2304">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="27133-2305">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27133-2305">Az.Compute</span></span>

* <span data-ttu-id="27133-2306">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="27133-2306">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="27133-2307">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27133-2307">Az.DataLakeStore</span></span>

* <span data-ttu-id="27133-2308">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="27133-2308">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="27133-2309">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="27133-2309">Az.FrontDoor</span></span>

* <span data-ttu-id="27133-2310">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="27133-2310">Fixed some broken links</span></span>
    - <span data-ttu-id="27133-2311">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="27133-2311">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="27133-2312">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="27133-2312">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="27133-2313">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27133-2313">Az.RecoveryServices</span></span>

* <span data-ttu-id="27133-2314">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="27133-2314">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="27133-2315">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="27133-2315">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="27133-2316">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27133-2316">Az.Resources</span></span>

* <span data-ttu-id="27133-2317">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="27133-2317">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="27133-2318">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="27133-2318">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="27133-2319">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27133-2319">Az.Sql</span></span>

* <span data-ttu-id="27133-2320">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="27133-2320">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="27133-2321">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="27133-2321">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="27133-2322">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="27133-2322">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="27133-2323">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27133-2323">Az.Storage</span></span>

* <span data-ttu-id="27133-2324">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27133-2324">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="27133-2325">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="27133-2325">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="27133-2326">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="27133-2326">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="27133-2327">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="27133-2327">Support Static Website configuration</span></span>
    - <span data-ttu-id="27133-2328">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="27133-2328">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="27133-2329">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="27133-2329">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="27133-2330">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27133-2330">Az.Websites</span></span>

* <span data-ttu-id="27133-2331">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="27133-2331">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="27133-2332">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="27133-2332">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="27133-2333">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="27133-2333">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="27133-2334">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="27133-2334">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="27133-2335">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="27133-2335">Az.ApiManagement</span></span>
* <span data-ttu-id="27133-2336">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="27133-2336">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="27133-2337">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="27133-2337">Az.Automation</span></span>
* <span data-ttu-id="27133-2338">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="27133-2338">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="27133-2339">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="27133-2339">Added Update Management cmdlets</span></span>
* <span data-ttu-id="27133-2340">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="27133-2340">Added Source Control cmdlets</span></span>
* <span data-ttu-id="27133-2341">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="27133-2341">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="27133-2342">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="27133-2342">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="27133-2343">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27133-2343">Az.Compute</span></span>
* <span data-ttu-id="27133-2344">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="27133-2344">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="27133-2345">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="27133-2345">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="27133-2346">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="27133-2346">Az.ContainerInstance</span></span>
* <span data-ttu-id="27133-2347">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="27133-2347">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="27133-2348">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="27133-2348">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="27133-2349">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="27133-2349">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="27133-2350">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27133-2350">Az.Network</span></span>
* <span data-ttu-id="27133-2351">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="27133-2351">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="27133-2352">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="27133-2352">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="27133-2353">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="27133-2353">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="27133-2354">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="27133-2354">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="27133-2355">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="27133-2355">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="27133-2356">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="27133-2356">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="27133-2357">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="27133-2357">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="27133-2358">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="27133-2358">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="27133-2359">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="27133-2359">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="27133-2360">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="27133-2360">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="27133-2361">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="27133-2361">Az.Relay</span></span>
* <span data-ttu-id="27133-2362">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="27133-2362">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="27133-2363">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27133-2363">Az.Resources</span></span>
* <span data-ttu-id="27133-2364">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="27133-2364">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="27133-2365">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="27133-2365">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="27133-2366">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="27133-2366">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="27133-2367">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="27133-2367">Az.ServiceFabric</span></span>
* <span data-ttu-id="27133-2368">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="27133-2368">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="27133-2369">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27133-2369">Az.Sql</span></span>
* <span data-ttu-id="27133-2370">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="27133-2370">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="27133-2371">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="27133-2371">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="27133-2372">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="27133-2372">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="27133-2373">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="27133-2373">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="27133-2374">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="27133-2374">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="27133-2375">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="27133-2375">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="27133-2376">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="27133-2376">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="27133-2377">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="27133-2377">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="27133-2378">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="27133-2378">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="27133-2379">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="27133-2379">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="27133-2380">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="27133-2380">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="27133-2381">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="27133-2381">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="27133-2382">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="27133-2382">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="27133-2383">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="27133-2383">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="27133-2384">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="27133-2384">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="27133-2385">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="27133-2385">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="27133-2386">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="27133-2386">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="27133-2387">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="27133-2387">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="27133-2388">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="27133-2388">General</span></span>
* <span data-ttu-id="27133-2389">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="27133-2389">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="27133-2390">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="27133-2390">Az.Profile</span></span>
* <span data-ttu-id="27133-2391">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="27133-2391">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="27133-2392">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="27133-2392">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="27133-2393">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="27133-2393">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="27133-2394">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="27133-2394">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="27133-2395">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="27133-2395">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="27133-2396">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="27133-2396">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="27133-2397">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="27133-2397">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="27133-2398">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="27133-2398">Az.CognitiveServices</span></span>
* <span data-ttu-id="27133-2399">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="27133-2399">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27133-2400">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27133-2400">Az.Compute</span></span>
* <span data-ttu-id="27133-2401">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="27133-2401">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="27133-2402">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="27133-2402">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="27133-2403">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="27133-2403">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="27133-2404">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27133-2404">Az.DataLakeStore</span></span>
* <span data-ttu-id="27133-2405">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="27133-2405">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="27133-2406">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="27133-2406">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="27133-2407">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="27133-2407">Az.Insights</span></span>
* <span data-ttu-id="27133-2408">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="27133-2408">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="27133-2409">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="27133-2409">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="27133-2410">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="27133-2410">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="27133-2411">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="27133-2411">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27133-2412">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27133-2412">Az.Network</span></span>
* <span data-ttu-id="27133-2413">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="27133-2413">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="27133-2414">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="27133-2414">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="27133-2415">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="27133-2415">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="27133-2416">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="27133-2416">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="27133-2417">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="27133-2417">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="27133-2418">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="27133-2418">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="27133-2419">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="27133-2419">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="27133-2420">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="27133-2420">Az.PolicyInsights</span></span>
* <span data-ttu-id="27133-2421">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="27133-2421">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="27133-2422">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27133-2422">Az.Resources</span></span>
* <span data-ttu-id="27133-2423">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="27133-2423">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="27133-2424">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="27133-2424">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="27133-2425">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="27133-2425">Az.ServiceBus</span></span>
* <span data-ttu-id="27133-2426">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="27133-2426">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="27133-2427">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="27133-2427">Az.ServiceFabric</span></span>
* <span data-ttu-id="27133-2428">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="27133-2428">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="27133-2429">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="27133-2429">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="27133-2430">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="27133-2430">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="27133-2431">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="27133-2431">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="27133-2432">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="27133-2432">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="27133-2433">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="27133-2433">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="27133-2434">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="27133-2434">Az.Profile</span></span>
* <span data-ttu-id="27133-2435">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="27133-2435">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="27133-2436">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="27133-2436">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27133-2437">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27133-2437">Az.Compute</span></span>
* <span data-ttu-id="27133-2438">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="27133-2438">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="27133-2439">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="27133-2439">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="27133-2440">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27133-2440">Az.DataLakeStore</span></span>
* <span data-ttu-id="27133-2441">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="27133-2441">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="27133-2442">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="27133-2442">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="27133-2443">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="27133-2443">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="27133-2444">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="27133-2444">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="27133-2445">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="27133-2445">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27133-2446">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27133-2446">Az.Network</span></span>
* <span data-ttu-id="27133-2447">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="27133-2447">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="27133-2448">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="27133-2448">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="27133-2449">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27133-2449">Az.Resources</span></span>
* <span data-ttu-id="27133-2450">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="27133-2450">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="27133-2451">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="27133-2451">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="27133-2452">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="27133-2452">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="27133-2453">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="27133-2453">Azure.Storage</span></span>
* <span data-ttu-id="27133-2454">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="27133-2454">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="27133-2455">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="27133-2455">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="27133-2456">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="27133-2456">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="27133-2457">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="27133-2457">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="27133-2458">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="27133-2458">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="27133-2459">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="27133-2459">Az.CognitiveServices</span></span>
* <span data-ttu-id="27133-2460">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="27133-2460">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27133-2461">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27133-2461">Az.Compute</span></span>
* <span data-ttu-id="27133-2462">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="27133-2462">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="27133-2463">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="27133-2463">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="27133-2464">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="27133-2464">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="27133-2465">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="27133-2465">Az.DataFactoryV2</span></span>
* <span data-ttu-id="27133-2466">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="27133-2466">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27133-2467">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27133-2467">Az.Network</span></span>
* <span data-ttu-id="27133-2468">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="27133-2468">Added NetworkProfile functionality.</span></span> <span data-ttu-id="27133-2469">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="27133-2469">new cmdlets added</span></span>
    - <span data-ttu-id="27133-2470">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="27133-2470">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="27133-2471">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="27133-2471">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="27133-2472">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="27133-2472">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="27133-2473">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="27133-2473">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="27133-2474">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="27133-2474">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="27133-2475">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="27133-2475">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="27133-2476">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="27133-2476">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="27133-2477">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="27133-2477">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="27133-2478">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="27133-2478">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="27133-2479">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="27133-2479">Az.RedisCache</span></span>
* <span data-ttu-id="27133-2480">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="27133-2480">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="27133-2481">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="27133-2481">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="27133-2482">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27133-2482">Az.Resources</span></span>
* <span data-ttu-id="27133-2483">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="27133-2483">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="27133-2484">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="27133-2484">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="27133-2485">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27133-2485">Az.Sql</span></span>
* <span data-ttu-id="27133-2486">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="27133-2486">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27133-2487">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27133-2487">Az.Websites</span></span>
* <span data-ttu-id="27133-2488">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="27133-2488">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="27133-2489">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="27133-2489">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="27133-2490">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="27133-2490">0.2.0 - September 2018</span></span>
 <span data-ttu-id="27133-2491">Начальный выпуск</span><span class="sxs-lookup"><span data-stu-id="27133-2491">Initial Release</span></span>
