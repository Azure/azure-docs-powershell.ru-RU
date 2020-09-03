---
title: Заметки о выпуске Azure PowerShell
description: Узнайте обо всех последних обновлениях модулей Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 86413b426db1b17349c6256f9c70f542c6a62a2f
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "89242297"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="82d40-103">Заметки о выпуске Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="82d40-103">Azure PowerShell release notes</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="82d40-104">4.5.0 — август 2020 г.</span><span class="sxs-lookup"><span data-stu-id="82d40-104">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="82d40-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="82d40-105">Az.Accounts</span></span>
* <span data-ttu-id="82d40-106">Командлет Connect-AzAccount теперь принимает параметр MaxContextPopulation (№ 9865).</span><span class="sxs-lookup"><span data-stu-id="82d40-106">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="82d40-107">Версия SubscriptionClient обновлена до 2019-06-01 и поддерживает отображение доменов арендаторов (№ 9838).</span><span class="sxs-lookup"><span data-stu-id="82d40-107">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="82d40-108">Добавлена поддержка домашнего арендатора и сведений managedBy арендатора для подписки.</span><span class="sxs-lookup"><span data-stu-id="82d40-108">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="82d40-109">Исправлено имя модуля и сведения о версии в данных телеметрии.</span><span class="sxs-lookup"><span data-stu-id="82d40-109">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="82d40-110">Исправлено поведение SqlDatabaseDnsSuffix и ServiceManagementUrl, когда конечная точка метаданных среды возвращает несовместимое значение.</span><span class="sxs-lookup"><span data-stu-id="82d40-110">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="82d40-111">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="82d40-111">Az.Aks</span></span>
* <span data-ttu-id="82d40-112">Параметр ClientIdAndSecret замен на ServicePrincipalIdAndSecret и задан в виде псевдонима (№ 12381).</span><span class="sxs-lookup"><span data-stu-id="82d40-112">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="82d40-113">Командлеты Get-AzAks, New-AzAks, Remove-AzAks, Set-AzAks заменены на Get-AzAksCluster, New-AzAksCluster, Remove-AzAksCluster, Set-AzAksCluster. Исходные командлеты заданы в виде псевдонимов (№ 12373).</span><span class="sxs-lookup"><span data-stu-id="82d40-113">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="82d40-114">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="82d40-114">Az.ApiManagement</span></span>
* <span data-ttu-id="82d40-115">Добавлен новый командлет Add-AzApiManagementApiToGateway.</span><span class="sxs-lookup"><span data-stu-id="82d40-115">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="82d40-116">Добавлен новый командлет Get-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="82d40-116">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="82d40-117">Добавлен новый командлет Get-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="82d40-117">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="82d40-118">Добавлен новый командлет Get-AzApiManagementGatewayKey.</span><span class="sxs-lookup"><span data-stu-id="82d40-118">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="82d40-119">Добавлен новый командлет New-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="82d40-119">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="82d40-120">Добавлен новый командлет New-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="82d40-120">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="82d40-121">Добавлен новый командлет New-AzApiManagementResourceLocationObject.</span><span class="sxs-lookup"><span data-stu-id="82d40-121">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="82d40-122">Добавлен новый командлет Remove-AzApiManagementApiFromGateway.</span><span class="sxs-lookup"><span data-stu-id="82d40-122">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="82d40-123">Добавлен новый командлет Remove-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="82d40-123">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="82d40-124">Добавлен новый командлет Remove-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="82d40-124">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="82d40-125">Добавлен новый командлет Update-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="82d40-125">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="82d40-126">Добавлен новый необязательный параметр [-GatewayId] в командлет Get-AzApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="82d40-126">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="82d40-127">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="82d40-127">Az.CognitiveServices</span></span>
* <span data-ttu-id="82d40-128">Задано явное использование действия "Отклонить" в качестве действия NetworkRules по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="82d40-128">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="82d40-129">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="82d40-129">Az.FrontDoor</span></span>
* <span data-ttu-id="82d40-130">Исправлена проблема, связанная с возникновением исключения при попытке Enum.Parse привести значение NULL к значениям перечисления Enabled или Disabled (№ 12344).</span><span class="sxs-lookup"><span data-stu-id="82d40-130">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="82d40-131">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="82d40-131">Az.HDInsight</span></span>
* <span data-ttu-id="82d40-132">Добавлена поддержка создания кластера с функцией шифрования передаваемых данных.</span><span class="sxs-lookup"><span data-stu-id="82d40-132">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="82d40-133">Добавлен новый параметр EncryptionInTransit в командлет New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="82d40-133">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="82d40-134">Добавлен новый параметр EncryptionInTransit в командлет New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="82d40-134">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="82d40-135">Добавлена поддержка создания кластера с функцией приватного канала:</span><span class="sxs-lookup"><span data-stu-id="82d40-135">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="82d40-136">Добавлен новый параметр PublicNetworkAccessType и OutboundPublicNetworkAccessType в командлет New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="82d40-136">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="82d40-137">Добавлен новый параметр PublicNetworkAccessType и OutboundPublicNetworkAccessType в командлет New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="82d40-137">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="82d40-138">Реализовано возвращение сведений о виртуальной сети при вызове New-AzHDInsightCluster или Get-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="82d40-138">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82d40-139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82d40-139">Az.Network</span></span>
* <span data-ttu-id="82d40-140">Включена поддержка параметра AddressPrefixType в Remove-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="82d40-140">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="82d40-141">Реализованы некритические изменения: функциональность PeerAddressType для частного пиринга в Remove-AzExpressRouteCircutPeeringConfig.</span><span class="sxs-lookup"><span data-stu-id="82d40-141">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="82d40-142">Код изменен для игнорирования регистра в параметрах AddressPrefixType и PeerAddressType.</span><span class="sxs-lookup"><span data-stu-id="82d40-142">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="82d40-143">Изменено сообщение с предупреждением для New-AzLoadBalancerFrontendIpConfig, New-AzPublicIpAddress и New-AzPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="82d40-143">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="82d40-144">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="82d40-144">Az.OperationalInsights</span></span>
* <span data-ttu-id="82d40-145">Добавлен параметр -ForceDelete для Remove-AzOperationalInsightsworkspace.</span><span class="sxs-lookup"><span data-stu-id="82d40-145">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="82d40-146">Добавлен новый командлет Get-AzOperationalInsightsDeletedWorkspace.</span><span class="sxs-lookup"><span data-stu-id="82d40-146">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="82d40-147">Добавлен новый командлет Restore-AzOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="82d40-147">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="82d40-148">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="82d40-148">Az.RecoveryServices</span></span>
* <span data-ttu-id="82d40-149">Улучшена работа с обнаружением контейнеров и элементов Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="82d40-149">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="82d40-150">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82d40-150">Az.Resources</span></span>
* <span data-ttu-id="82d40-151">Добавлены свойства Condition, ConditionVersion и Description в New-AzRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="82d40-151">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="82d40-152">Это касается всех соответствующих изменений моделей данных.</span><span class="sxs-lookup"><span data-stu-id="82d40-152">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="82d40-153">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82d40-153">Az.Sql</span></span>
* <span data-ttu-id="82d40-154">Исправлена ошибка, связанная с потенциальным игнорированием регистра имени сервера в New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="82d40-154">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="82d40-155">Исправлена ошибка, из-за которой возвращалось неправильное имя существующей базы данных в New-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="82d40-155">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="82d40-156">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="82d40-156">Az.Storage</span></span>
* <span data-ttu-id="82d40-157">Добавлена поддержка создания маркера SAS контейнера и BLOB-объекта с новым разрешением x,t.</span><span class="sxs-lookup"><span data-stu-id="82d40-157">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="82d40-158">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="82d40-158">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="82d40-159">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="82d40-159">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="82d40-160">Добавлена поддержка создания маркера SAS учетной записи с новым разрешением x,t,f.</span><span class="sxs-lookup"><span data-stu-id="82d40-160">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="82d40-161">New-AzStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="82d40-161">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="82d40-162">Добавлена поддержка получения данных об использовании одной общей папки.</span><span class="sxs-lookup"><span data-stu-id="82d40-162">Supported get single file share usage</span></span>
    - <span data-ttu-id="82d40-163">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="82d40-163">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="82d40-164">4.4.0 — июль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="82d40-164">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="82d40-165">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="82d40-165">Az.Accounts</span></span>
* <span data-ttu-id="82d40-166">Добавлен новый командлет Invoke-AzRestMethod.</span><span class="sxs-lookup"><span data-stu-id="82d40-166">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="82d40-167">Устранена неполадка, из-за которой могли возникать ошибки с проверкой подлинности в сценариях с несколькими процессами, такими как выполнение нескольких командлетов Azure PowerShell с помощью Start-Job [№ 9448].</span><span class="sxs-lookup"><span data-stu-id="82d40-167">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="82d40-168">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="82d40-168">Az.Aks</span></span>
* <span data-ttu-id="82d40-169">Исправлена ошибка, из-за которой Get-AzAks выводит не все кластеры [ №12296].</span><span class="sxs-lookup"><span data-stu-id="82d40-169">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="82d40-170">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="82d40-170">Az.AnalysisServices</span></span>
* <span data-ttu-id="82d40-171">Удалена ссылка на проект для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="82d40-171">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="82d40-172">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="82d40-172">Az.Automation</span></span>
* <span data-ttu-id="82d40-173">Исправлена ошибка, из-за которой строка с escape-символами не преобразовывалась в объект JSON.</span><span class="sxs-lookup"><span data-stu-id="82d40-173">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82d40-174">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82d40-174">Az.Compute</span></span>
* <span data-ttu-id="82d40-175">Добавлено предупреждение, которое отображается при использовании New-AzVmss, если версия образа не является последней.</span><span class="sxs-lookup"><span data-stu-id="82d40-175">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="82d40-176">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="82d40-176">Az.DataFactory</span></span>
* <span data-ttu-id="82d40-177">Добавлены глобальные параметры в Фабрику данных.</span><span class="sxs-lookup"><span data-stu-id="82d40-177">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="82d40-178">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="82d40-178">Az.EventGrid</span></span>
* <span data-ttu-id="82d40-179">Обновлен модуль для использования API версии 2020-06-01.</span><span class="sxs-lookup"><span data-stu-id="82d40-179">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="82d40-180">Добавлены новые возможности:</span><span class="sxs-lookup"><span data-stu-id="82d40-180">Added new features:</span></span>
    - <span data-ttu-id="82d40-181">сопоставление входных данных;</span><span class="sxs-lookup"><span data-stu-id="82d40-181">Input mapping</span></span>
    - <span data-ttu-id="82d40-182">схема доставки событий;</span><span class="sxs-lookup"><span data-stu-id="82d40-182">Event Delivery Schema</span></span>
    - <span data-ttu-id="82d40-183">Приватный канал</span><span class="sxs-lookup"><span data-stu-id="82d40-183">Private Link</span></span>
    - <span data-ttu-id="82d40-184">схема событий облака (версия 1.0);</span><span class="sxs-lookup"><span data-stu-id="82d40-184">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="82d40-185">раздел служебной шины как назначение;</span><span class="sxs-lookup"><span data-stu-id="82d40-185">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="82d40-186">функция Azure как назначение;</span><span class="sxs-lookup"><span data-stu-id="82d40-186">Azure Function As Destination</span></span>
    - <span data-ttu-id="82d40-187">пакетная обработка данных веб-перехватчика;</span><span class="sxs-lookup"><span data-stu-id="82d40-187">WebHook Batching</span></span>
    - <span data-ttu-id="82d40-188">безопасный веб-перехватчик (поддержка AAD);</span><span class="sxs-lookup"><span data-stu-id="82d40-188">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="82d40-189">фильтрация IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="82d40-189">IpFiltering</span></span>
* <span data-ttu-id="82d40-190">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="82d40-190">Updated cmdlets:</span></span>
    - <span data-ttu-id="82d40-191">New-AzEventGridSubscription или Update-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="82d40-191">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="82d40-192">Добавлены новые необязательные параметры для поддержки пакетной обработки данных веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="82d40-192">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="82d40-193">Добавлены новые необязательные параметры для поддержки безопасного веб-перехватчика с использованием AAD.</span><span class="sxs-lookup"><span data-stu-id="82d40-193">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="82d40-194">Добавлено новое перечисление для параметра EndpointType, чтобы обеспечить поддержку функции Azure и раздела служебной шины в качестве назначения.</span><span class="sxs-lookup"><span data-stu-id="82d40-194">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="82d40-195">Добавлен новый необязательный параметр для схемы доставки.</span><span class="sxs-lookup"><span data-stu-id="82d40-195">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="82d40-196">New-AzEventGridTopic или Update-AzEventGridTopic и New-AzEventGridDomain или Update-AzEventGridDomain:</span><span class="sxs-lookup"><span data-stu-id="82d40-196">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="82d40-197">Добавлены новые необязательные параметры для поддержки фильтрации IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="82d40-197">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="82d40-198">New-AzEventGridTopic или New-AzEventGridDomain:</span><span class="sxs-lookup"><span data-stu-id="82d40-198">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="82d40-199">Добавлены новые необязательные параметры для поддержки сопоставления входных данных.</span><span class="sxs-lookup"><span data-stu-id="82d40-199">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="82d40-200">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="82d40-200">Az.FrontDoor</span></span>
* <span data-ttu-id="82d40-201">Обновлен модуль для использования API версии 2020-05-01.</span><span class="sxs-lookup"><span data-stu-id="82d40-201">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="82d40-202">Включена поддержка Приватного канала для ресурсов службы хранилища, Key Vault и службы веб-приложений.</span><span class="sxs-lookup"><span data-stu-id="82d40-202">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="82d40-203">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="82d40-203">Az.HDInsight</span></span>
* <span data-ttu-id="82d40-204">Включена поддержка создания кластера с хранилищем ADLS 1-го и 2-го поколения в национальных облаках.</span><span class="sxs-lookup"><span data-stu-id="82d40-204">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="82d40-205">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="82d40-205">Az.Monitor</span></span>
* <span data-ttu-id="82d40-206">Исправлена ошибка с Get-AzDiagnosticSetting, связанная с присвоением значения NULL метрикам или журналам [№ 12272].</span><span class="sxs-lookup"><span data-stu-id="82d40-206">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82d40-207">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82d40-207">Az.Network</span></span>
* <span data-ttu-id="82d40-208">Исправлены ошибки с переключением параметров для подключения виртуальной сети концентратора к глобальной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="82d40-208">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="82d40-209">Добавлены новые командлеты для сайтов сетевых виртуальных модулей Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-209">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="82d40-210">Get-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="82d40-210">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="82d40-211">New-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="82d40-211">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="82d40-212">Remove-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="82d40-212">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="82d40-213">Update-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="82d40-213">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="82d40-214">New-AzOffice365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="82d40-214">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="82d40-215">Добавлены новые командлеты для сетевого виртуального модуля Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-215">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="82d40-216">Get-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="82d40-216">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="82d40-217">New-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="82d40-217">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="82d40-218">Remove-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="82d40-218">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="82d40-219">Update-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="82d40-219">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="82d40-220">Get-AzNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="82d40-220">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="82d40-221">New-AzVirtualApplianceSkuProperty</span><span class="sxs-lookup"><span data-stu-id="82d40-221">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="82d40-222">Общие командлеты для Шлюза приложений, подключенного к Приватному каналу.</span><span class="sxs-lookup"><span data-stu-id="82d40-222">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="82d40-223">Общие командлеты для службы синхронизации хранилища, подключенной к Приватному каналу.</span><span class="sxs-lookup"><span data-stu-id="82d40-223">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="82d40-224">Общие командлеты для службы SignalR, подключенной к Приватному каналу.</span><span class="sxs-lookup"><span data-stu-id="82d40-224">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="82d40-225">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="82d40-225">Az.RecoveryServices</span></span>
* <span data-ttu-id="82d40-226">Удалена ссылка на проект для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="82d40-226">Removed project reference to Authentication</span></span>
* <span data-ttu-id="82d40-227">В Azure Backup представлена более точная справка по командлетам.</span><span class="sxs-lookup"><span data-stu-id="82d40-227">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="82d40-228">В Azure Backup включена поддержка выборки заданий агента MAB с помощью командлета Get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="82d40-228">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="82d40-229">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82d40-229">Az.Resources</span></span>
* <span data-ttu-id="82d40-230">Обновлен командлет Save-AzResourceGroupDeploymentTemplate для использования пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="82d40-230">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="82d40-231">Добавлен командлет Unregister-AzResourceProvider.</span><span class="sxs-lookup"><span data-stu-id="82d40-231">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="82d40-232">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82d40-232">Az.Sql</span></span>
* <span data-ttu-id="82d40-233">Включена поддержка субъекта-службы и гостевых пользователей для командлета Set-AzSqlInstanceActiveDirectoryAdministrator.</span><span class="sxs-lookup"><span data-stu-id="82d40-233">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="82d40-234">Исправлена ошибка в командлетах классификации данных.</span><span class="sxs-lookup"><span data-stu-id="82d40-234">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="82d40-235">Включена поддержка отработки отказа Управляемого экземпляра SQL Azure. Invoke-AzSqlInstanceFailover</span><span class="sxs-lookup"><span data-stu-id="82d40-235">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="82d40-236">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="82d40-236">Az.Storage</span></span>
* <span data-ttu-id="82d40-237">Исправлена ошибка, из-за которой в некоторых командлетах плоскости данных не добавлялся объект UserAgent.</span><span class="sxs-lookup"><span data-stu-id="82d40-237">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="82d40-238">Включена поддержка создания и обновления учетной записи хранения с использованием MinimumTlsVersion и AllowBlobPublicAccess.</span><span class="sxs-lookup"><span data-stu-id="82d40-238">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="82d40-239">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="82d40-239">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="82d40-240">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="82d40-240">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="82d40-241">Включена поддержка включения и отключения управления версиями в службе BLOB-объектов учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="82d40-241">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="82d40-242">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="82d40-242">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="82d40-243">Включена поддержка вывода списка BLOB-объектов с данными о версиях BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="82d40-243">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="82d40-244">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="82d40-244">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="82d40-245">Включена поддержка получения или удаления одного моментального снимка BLOB-объекта или версии BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="82d40-245">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="82d40-246">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="82d40-246">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="82d40-247">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="82d40-247">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="82d40-248">Включена поддержка конвейера на основе BLOB-объекта, созданного с помощью Azure.Storage.Blobs версии 12.</span><span class="sxs-lookup"><span data-stu-id="82d40-248">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="82d40-249">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="82d40-249">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="82d40-250">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="82d40-250">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="82d40-251">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="82d40-251">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="82d40-252">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="82d40-252">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="82d40-253">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="82d40-253">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="82d40-254">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="82d40-254">Az.StorageSync</span></span>
* <span data-ttu-id="82d40-255">Добавлена новая версия пакета SDK StorageSync, предназначенная для API версии 2020-03-01.</span><span class="sxs-lookup"><span data-stu-id="82d40-255">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="82d40-256">Добавлен командлет для обновления службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="82d40-256">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="82d40-257">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="82d40-257">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="82d40-258">Добавлены классы IncomingTrafficPolicy и IncomingTrafficPolicy в командлеты службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="82d40-258">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="82d40-259">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="82d40-259">Az.Websites</span></span>
* <span data-ttu-id="82d40-260">Включена поддержка выполнения операций для слотов, которые находятся не в той же группе ресурсов, что и план службы приложений.</span><span class="sxs-lookup"><span data-stu-id="82d40-260">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="82d40-261">4.3.0 — июнь 2020 года</span><span class="sxs-lookup"><span data-stu-id="82d40-261">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="82d40-262">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="82d40-262">Az.Accounts</span></span>
* <span data-ttu-id="82d40-263">Включена поддержка обнаружения параметров среды по умолчанию и добавления окружения с помощью командлета Add-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="82d40-263">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="82d40-264">Обновлены предварительно загруженные сборки [№ 12024], [№ 11976].</span><span class="sxs-lookup"><span data-stu-id="82d40-264">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="82d40-265">Обновлена сборка Azure.Core.</span><span class="sxs-lookup"><span data-stu-id="82d40-265">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="82d40-266">Исправлена ошибка, из-за которой выполнение Connect-AzAccount может завершаться сбоем при многопоточном выполнении [№ 11201].</span><span class="sxs-lookup"><span data-stu-id="82d40-266">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="82d40-267">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="82d40-267">Az.Aks</span></span>
* <span data-ttu-id="82d40-268">Заменено использование старого [API AccessProfile](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) вызовами API [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) и [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials).</span><span class="sxs-lookup"><span data-stu-id="82d40-268">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="82d40-269">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="82d40-269">Az.Batch</span></span>
* <span data-ttu-id="82d40-270">Изменена версия SDK для Microsoft.Azure.Management.Batch для Az.Batch на 11.0.0.</span><span class="sxs-lookup"><span data-stu-id="82d40-270">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="82d40-271">Включена возможность задать удостоверение BatchAccount в командлете New-AzBatchAccount.</span><span class="sxs-lookup"><span data-stu-id="82d40-271">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="82d40-272">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="82d40-272">Az.CognitiveServices</span></span>
* <span data-ttu-id="82d40-273">Включена поддержка отображения возможностей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="82d40-273">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="82d40-274">Включена поддержка изменения PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="82d40-274">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82d40-275">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82d40-275">Az.Compute</span></span>
* <span data-ttu-id="82d40-276">Добавлен параметр SimulateEviction в командлеты Set-AzVM и Set-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="82d40-276">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="82d40-277">Добавлен фрагмент Premium_LRS в средство заполнения аргументов параметра StorageAccountType для командлета New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="82d40-277">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="82d40-278">Добавлены подсостояния для VMCustomScriptExtension [№ 11297].</span><span class="sxs-lookup"><span data-stu-id="82d40-278">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="82d40-279">Добавлен фрагмент Delete в средство заполнения аргументов параметра EvictionPolicy для командлетов New-AzVM и New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="82d40-279">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="82d40-280">Исправлено имя нового расширения виртуальной машины для SAP.</span><span class="sxs-lookup"><span data-stu-id="82d40-280">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="82d40-281">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="82d40-281">Az.DataFactory</span></span>
* <span data-ttu-id="82d40-282">Обновлен пакет SDK ADF для .NET до версии 4.9.0.</span><span class="sxs-lookup"><span data-stu-id="82d40-282">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="82d40-283">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="82d40-283">Az.EventHub</span></span>
* <span data-ttu-id="82d40-284">Добавлены параметры управляемого удостоверения для командлетов New-AzEventHubNamespace и Set-AzEventHubNamespace.</span><span class="sxs-lookup"><span data-stu-id="82d40-284">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="82d40-285">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="82d40-285">Az.Functions</span></span>
* <span data-ttu-id="82d40-286">Включена поддержка создания приложений-функций PowerShell 7.0 и Java 11.</span><span class="sxs-lookup"><span data-stu-id="82d40-286">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="82d40-287">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="82d40-287">Az.HDInsight</span></span>
* <span data-ttu-id="82d40-288">Включена поддержка перечисления узлов и перезагрузка отдельных узлов кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="82d40-288">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="82d40-289">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="82d40-289">Az.HealthcareApis</span></span>
* <span data-ttu-id="82d40-290">Обновлен пакет SDK до версии 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="82d40-290">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="82d40-291">Включена поддержка параметров экспорта и управляемого удостоверения.</span><span class="sxs-lookup"><span data-stu-id="82d40-291">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="82d40-292">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="82d40-292">Az.Monitor</span></span>
* <span data-ttu-id="82d40-293">Исправлен входной параметр объекта для Set-AzActivityLogAlert.</span><span class="sxs-lookup"><span data-stu-id="82d40-293">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="82d40-294">Исправлен параметр InputObject для Set-AzActionGroup [№ 10868].</span><span class="sxs-lookup"><span data-stu-id="82d40-294">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82d40-295">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82d40-295">Az.Network</span></span>
* <span data-ttu-id="82d40-296">Включена поддержка параметра AddressPrefixType в Remove-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="82d40-296">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="82d40-297">Добавлены новые командлеты для политики Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-297">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="82d40-298">New-AzFirewallPolicyDnsSetting</span><span class="sxs-lookup"><span data-stu-id="82d40-298">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="82d40-299">Включена поддержка полного доменного имени назначения в правилах сети для политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="82d40-299">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="82d40-300">Включена поддержка операций серверного пула адресов:</span><span class="sxs-lookup"><span data-stu-id="82d40-300">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="82d40-301">New-AzLoadBalancerBackendAddressConfig</span><span class="sxs-lookup"><span data-stu-id="82d40-301">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="82d40-302">New-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="82d40-302">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="82d40-303">Set-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="82d40-303">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="82d40-304">Remove-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="82d40-304">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="82d40-305">Get-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="82d40-305">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="82d40-306">Добавлена проверка имени для New-AzIpGroup.</span><span class="sxs-lookup"><span data-stu-id="82d40-306">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="82d40-307">Добавлены новые командлеты для политики Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-307">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="82d40-308">New-AzFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="82d40-308">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="82d40-309">Обновлены следующие команды для функции: Включена возможность настройки и удаления пользовательских DNS-серверов в шлюзе VPN P2S виртуальной глобальной сети.</span><span class="sxs-lookup"><span data-stu-id="82d40-309">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="82d40-310">Обновлен командлет New-AzP2sVpnGateway: добавлен необязательный параметр -CustomDnsServer, чтобы пользователи могли указывать свои DNS-серверы для настройки в шлюзе VPN P2S для использования клиентами с подключением "точка — сеть".</span><span class="sxs-lookup"><span data-stu-id="82d40-310">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="82d40-311">Обновлен командлет Update-AzP2sVpnGateway: добавлен необязательный параметр -CustomDnsServer, чтобы пользователи могли указывать свои DNS-серверы для настройки в шлюзе VPN P2S для использования клиентами с подключением "точка — сеть".</span><span class="sxs-lookup"><span data-stu-id="82d40-311">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="82d40-312">Обновлен командлет Update-AzVpnGateway:</span><span class="sxs-lookup"><span data-stu-id="82d40-312">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="82d40-313">добавлен необязательный параметр -BgpPeeringAddress, чтобы клиенты могли указывать пользовательские маршруты BGP для настройки в шлюзе VPN.</span><span class="sxs-lookup"><span data-stu-id="82d40-313">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="82d40-314">Добавлен новый командлет для сброса состояния маршрутизации ресурса VirtualHub:</span><span class="sxs-lookup"><span data-stu-id="82d40-314">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="82d40-315">Reset-AzHubRouter</span><span class="sxs-lookup"><span data-stu-id="82d40-315">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="82d40-316">Следующие обновления основаны на последнем изменении Swagger для политики брандмауэра:</span><span class="sxs-lookup"><span data-stu-id="82d40-316">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="82d40-317">изменены имена для RuleGroup, RuleCollectionGroup и RuleType;</span><span class="sxs-lookup"><span data-stu-id="82d40-317">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="82d40-318">включена поддержка коллекций правил NAT политики брандмауэра для поддержки нескольких коллекций правил NAT.</span><span class="sxs-lookup"><span data-stu-id="82d40-318">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="82d40-319">[Критическое изменение] Добавлен обязательный параметр SourceIpGroup для командлетов New-AzFirewallPolicyApplicationRule и New-AzFirewallPolicyNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="82d40-319">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="82d40-320">[Критическое изменение] Параметр SourceAddress для командлета New-AzFirewallPolicyApplicationRule сделан обязательным.</span><span class="sxs-lookup"><span data-stu-id="82d40-320">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="82d40-321">[Критическое изменение] Параметр SourceAddress для командлета New-AzFirewallPolicyApplicationRule сделан обязательным.</span><span class="sxs-lookup"><span data-stu-id="82d40-321">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="82d40-322">[Критическое изменение] Удалены обязательные параметры: TranslatedAddress и TranslatedPort для командлета New-AzFirewallPolicyNatRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="82d40-322">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="82d40-323">Добавлены новые командлеты для поддержки Приватного канала в Шлюзе приложений:</span><span class="sxs-lookup"><span data-stu-id="82d40-323">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="82d40-324">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="82d40-324">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="82d40-325">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="82d40-325">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="82d40-326">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="82d40-326">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="82d40-327">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="82d40-327">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="82d40-328">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="82d40-328">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="82d40-329">New-AzApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="82d40-329">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="82d40-330">Добавлены новые командлеты для дочернего ресурса HubRouteTables VirtualHub:</span><span class="sxs-lookup"><span data-stu-id="82d40-330">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="82d40-331">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="82d40-331">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="82d40-332">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="82d40-332">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="82d40-333">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="82d40-333">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="82d40-334">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="82d40-334">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="82d40-335">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="82d40-335">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="82d40-336">Обновлены существующие командлеты для включения поддержки необязательного входного параметра RoutingConfiguration для настраиваемой маршрутизации в виртуальной глобальной сети.</span><span class="sxs-lookup"><span data-stu-id="82d40-336">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="82d40-337">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="82d40-337">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="82d40-338">Set-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="82d40-338">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="82d40-339">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="82d40-339">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="82d40-340">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="82d40-340">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="82d40-341">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="82d40-341">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="82d40-342">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="82d40-342">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="82d40-343">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="82d40-343">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="82d40-344">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="82d40-344">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="82d40-345">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="82d40-345">Az.OperationalInsights</span></span>
* <span data-ttu-id="82d40-346">Исправлена ошибка, из-за которой PSWorkspace не реализует IOperationalInsightsWorkspace [№ 12135].</span><span class="sxs-lookup"><span data-stu-id="82d40-346">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="82d40-347">Добавлено значение pergb2018 в действительный набор значений параметра Sku в командлете Set-AzOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="82d40-347">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="82d40-348">Добавлен псевдоним FunctionParameters для параметра FunctionParameter:</span><span class="sxs-lookup"><span data-stu-id="82d40-348">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="82d40-349">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="82d40-349">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="82d40-350">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="82d40-350">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="82d40-351">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="82d40-351">Az.RecoveryServices</span></span>
* <span data-ttu-id="82d40-352">Включена поддержка выборки элементов MAB в Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="82d40-352">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="82d40-353">Включена поддержка типа диска StandardSSD_LRS в Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="82d40-353">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="82d40-354">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82d40-354">Az.Resources</span></span>
* <span data-ttu-id="82d40-355">Добавлены параметры UsageLocation, GivenName, Surname, AccountEnabled, MailNickname, Mail для PSADUser [№ 10526], [№ 10497].</span><span class="sxs-lookup"><span data-stu-id="82d40-355">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="82d40-356">Исправлена ошибка, из-за которой параметр -Mail не работает в командлете Get-AzADUser [№ 11981].</span><span class="sxs-lookup"><span data-stu-id="82d40-356">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="82d40-357">Добавлен параметр -ExcludeChangeType в командлеты Get-AzDeploymentWhatIfResult и Get-AzResourceGroupDeploymentWhatIfResult.</span><span class="sxs-lookup"><span data-stu-id="82d40-357">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="82d40-358">Добавлен параметр -WhatIfExcludeChangeType в командлеты New-AzDeployment и New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="82d40-358">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="82d40-359">Обновлены командлеты Test-Az\*Deployment для отображения улучшенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="82d40-359">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="82d40-360">Исправлено справочное сообщение для параметра -Name в командлетах создания развертывания и командлетах What-If.</span><span class="sxs-lookup"><span data-stu-id="82d40-360">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="82d40-361">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82d40-361">Az.Sql</span></span>
* <span data-ttu-id="82d40-362">Включена поддержка субъекта-службы для командлета настройки администратора Azure Active Directory SQL Server.</span><span class="sxs-lookup"><span data-stu-id="82d40-362">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="82d40-363">Исправлена ошибка синхронизации в командлетах классификации данных.</span><span class="sxs-lookup"><span data-stu-id="82d40-363">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="82d40-364">Включена поддержка поиска пользователей по адресу электронной почты в командлете Set-AzSqlServerActiveDirectoryAdministrator [№ 12192].</span><span class="sxs-lookup"><span data-stu-id="82d40-364">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="82d40-365">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="82d40-365">Az.Storage</span></span>
* <span data-ttu-id="82d40-366">Включена поддержка создания учетной записи хранения с помощью RequireInfrastructureEncryption.</span><span class="sxs-lookup"><span data-stu-id="82d40-366">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="82d40-367">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="82d40-367">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="82d40-368">Перемещена логика загрузки Azure.Core в Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="82d40-368">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="82d40-369">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="82d40-369">Az.Websites</span></span>
* <span data-ttu-id="82d40-370">В командлет Restore-AzDeletedWebApp добавлена защитная мера при удалении созданного веб-приложения, если восстановление завершилось сбоем.</span><span class="sxs-lookup"><span data-stu-id="82d40-370">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="82d40-371">Добавлены параметры SourceWebApp.Location для командлетов New-AzWebApp и New-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="82d40-371">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="82d40-372">Исправлена ошибка, препятствующая изменению параметров контейнера в командлетах Set-AzWebApp и Set-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="82d40-372">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="82d40-373">Исправлена ошибка получения SiteConfig, когда параметр -Name не указан для командлета Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="82d40-373">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="82d40-374">Включена поддержка создания приложений ASP для Linux.</span><span class="sxs-lookup"><span data-stu-id="82d40-374">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="82d40-375">Добавлены исключения для клонирования в группах ресурсов.</span><span class="sxs-lookup"><span data-stu-id="82d40-375">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="82d40-376">4.2.0 — июнь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="82d40-376">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="82d40-377">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="82d40-377">Az.Accounts</span></span>
* <span data-ttu-id="82d40-378">Исправлена проблема, из-за которой модуль Az мог пропускать журналы в заданиях службы автоматизации или PowerShell [№ 11492].</span><span class="sxs-lookup"><span data-stu-id="82d40-378">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="82d40-379">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="82d40-379">Az.AnalysisServices</span></span>
* <span data-ttu-id="82d40-380">Обновлена версия сборки командлетов плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="82d40-380">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="82d40-381">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="82d40-381">Az.ApiManagement</span></span>
* <span data-ttu-id="82d40-382">Обновлена версия сборки командлетов управления службами.</span><span class="sxs-lookup"><span data-stu-id="82d40-382">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="82d40-383">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="82d40-383">Az.Billing</span></span>
* <span data-ttu-id="82d40-384">Обновлена версия сборки командлетов потребления.</span><span class="sxs-lookup"><span data-stu-id="82d40-384">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="82d40-385">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="82d40-385">Az.CognitiveServices</span></span>
* <span data-ttu-id="82d40-386">Реализована поддержка элементов управления PrivateEndpoint и PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="82d40-386">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="82d40-387">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="82d40-387">Az.DataFactory</span></span>
* <span data-ttu-id="82d40-388">Обновлена версия сборки командлетов фабрики данных версии 2.</span><span class="sxs-lookup"><span data-stu-id="82d40-388">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="82d40-389">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="82d40-389">Az.DataShare</span></span>
* <span data-ttu-id="82d40-390">Вышла общедоступная версия модуля Az.DataShare.</span><span class="sxs-lookup"><span data-stu-id="82d40-390">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="82d40-391">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="82d40-391">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="82d40-392">Вышла общедоступная версия модуля Az.DesktopVirtualization.</span><span class="sxs-lookup"><span data-stu-id="82d40-392">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="82d40-393">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="82d40-393">Az.OperationalInsights</span></span>
* <span data-ttu-id="82d40-394">Пакет SDK обновлен до версии 0.21.0.</span><span class="sxs-lookup"><span data-stu-id="82d40-394">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="82d40-395">Добавлены дополнительные параметры в следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="82d40-395">Added optional parameters to</span></span> 
    - <span data-ttu-id="82d40-396">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="82d40-396">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="82d40-397">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="82d40-397">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="82d40-398">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="82d40-398">Az.PolicyInsights</span></span>
* <span data-ttu-id="82d40-399">Исправлен пример 3 для командлета Start-AzPolicyComplianceScan.</span><span class="sxs-lookup"><span data-stu-id="82d40-399">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="82d40-400">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="82d40-400">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="82d40-401">Обновлена версия сборки командлетов PowerBI.</span><span class="sxs-lookup"><span data-stu-id="82d40-401">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="82d40-402">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="82d40-402">Az.PrivateDns</span></span>
* <span data-ttu-id="82d40-403">Исправлено форматирование строки с подробными выходными данными командлета Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="82d40-403">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="82d40-404">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="82d40-404">Az.RecoveryServices</span></span>
* <span data-ttu-id="82d40-405">Реализована поддержка Azure Site Recovery для создания плана восстановления и репликации между зонами из входного XML-файла.</span><span class="sxs-lookup"><span data-stu-id="82d40-405">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="82d40-406">Обновлена версия сборки командлетов SiteRecovery и Backup.</span><span class="sxs-lookup"><span data-stu-id="82d40-406">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="82d40-407">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82d40-407">Az.Resources</span></span>
* <span data-ttu-id="82d40-408">Добавлен параметр Tail в командлеты Get-AzDeploymentScriptLog и Save-AzDeploymentScriptLog.</span><span class="sxs-lookup"><span data-stu-id="82d40-408">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="82d40-409">Отформатировано свойство Output и включено в отображаемые выходные данные командлета Get-AzDeploymentScript.</span><span class="sxs-lookup"><span data-stu-id="82d40-409">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="82d40-410">Параметр -DeploymentScriptInputObject переименован в -DeploymentScriptObject.</span><span class="sxs-lookup"><span data-stu-id="82d40-410">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="82d40-411">Исправлена ошибка с отсутствующими именами файлов или целевых объектов в сообщениях командлетов.</span><span class="sxs-lookup"><span data-stu-id="82d40-411">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="82d40-412">Обновлена версия сборки командлетов диспетчера ресурсов и обработчика тегов.</span><span class="sxs-lookup"><span data-stu-id="82d40-412">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="82d40-413">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82d40-413">Az.Sql</span></span>
* <span data-ttu-id="82d40-414">Добавлен параметр UsePrivateLinkConnection в командлеты New-AzSqlSyncGroup, Update-AzSqlSyncGroup, New-AzSqlSyncMember и Update-AzSqlSyncMember.</span><span class="sxs-lookup"><span data-stu-id="82d40-414">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="82d40-415">Добавлен параметр SyncMemberAzureDatabaseResourceId в командлеты New-AzSqlSyncMember и Update-AzSqlSyncMember.</span><span class="sxs-lookup"><span data-stu-id="82d40-415">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="82d40-416">Реализована поддержка поиска гостевых пользователей в командлете для настройки администратора Active Directory в SQL Server Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-416">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="82d40-417">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="82d40-417">Az.Storage</span></span>
* <span data-ttu-id="82d40-418">Обновлена версия сборки командлетов плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="82d40-418">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="82d40-419">4.1.0 — май 2020 г.</span><span class="sxs-lookup"><span data-stu-id="82d40-419">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="82d40-420">Основные сведения о новых возможностях с момента последнего выпуска</span><span class="sxs-lookup"><span data-stu-id="82d40-420">Highlights since the last release</span></span>
* <span data-ttu-id="82d40-421">Поддерживаемые версии PowerShell: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="82d40-421">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="82d40-422">Вышла общедоступная версия модуля Az.Functions.</span><span class="sxs-lookup"><span data-stu-id="82d40-422">General availability of Az.Functions</span></span> 
* <span data-ttu-id="82d40-423">Состоялся основной выпуск Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources и Az.Storage.</span><span class="sxs-lookup"><span data-stu-id="82d40-423">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="82d40-424">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="82d40-424">Az.Accounts</span></span>
* <span data-ttu-id="82d40-425">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметры AzureSynapseAnalyticsEndpointResourceId и AzureSynapseAnalyticsEndpointSuffix.</span><span class="sxs-lookup"><span data-stu-id="82d40-425">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="82d40-426">В Az.Accounts добавлены сборки, связанные с Azure.Core. Добавлена поддержка Windows PowerShell 5.1, PowerShell Core 6.2.4 и PowerShell 7+.</span><span class="sxs-lookup"><span data-stu-id="82d40-426">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="82d40-427">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="82d40-427">Az.Aks</span></span>
* <span data-ttu-id="82d40-428">Версия API обновлена до 2019-10-01.</span><span class="sxs-lookup"><span data-stu-id="82d40-428">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="82d40-429">Добавлена возможность создания контейнера Windows в службе Azure Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="82d40-429">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="82d40-430">Добавлены новые командлеты: New-AzAksNodePool, Update-AzAksNodePool, Remove-AzAksNodePool, Get-AzAksNodePool, Install-AzAksKubectl, Get-AzAksVersion.</span><span class="sxs-lookup"><span data-stu-id="82d40-430">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="82d40-431">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="82d40-431">Az.ApiManagement</span></span>
* <span data-ttu-id="82d40-432">В New-AzApiManagement и Set-AzApiManagement параметр -AssignIdentity переименован в -SystemAssignedIdentity.</span><span class="sxs-lookup"><span data-stu-id="82d40-432">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="82d40-433">В New-AzApiManagement и Set-AzApiManagement добавлен новый параметр -UserAssignedIdentity <строка[]>.</span><span class="sxs-lookup"><span data-stu-id="82d40-433">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="82d40-434">Командлет Get-AzApiManagementProperty переименован в Get-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="82d40-434">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="82d40-435">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="82d40-435">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="82d40-436">Командлет New-AzApiManagementProperty переименован в New-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="82d40-436">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="82d40-437">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="82d40-437">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="82d40-438">Командлет Set-AzApiManagementProperty переименован в Set-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="82d40-438">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="82d40-439">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="82d40-439">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="82d40-440">Командлет Remove-AzApiManagementProperty переименован в Remove-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="82d40-440">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="82d40-441">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="82d40-441">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="82d40-442">Добавлен новый командлет Get-AzApiManagementAuthorizationServerClientSecret, а Get-AzApiManagementAuthorizationServer теперь не возвращает секрет клиента.</span><span class="sxs-lookup"><span data-stu-id="82d40-442">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="82d40-443">Добавлен новый командлет Get-AzApiManagementNamedValueSecretValue, а Get-AzApiManagementNamedValue теперь не возвращает значение секрета.</span><span class="sxs-lookup"><span data-stu-id="82d40-443">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="82d40-444">Добавлен новый командлет Get-AzApiManagementOpenIdConnectProviderClientSecret, а Get-AzApiManagementOpenIdConnectProvider теперь не возвращает секрет клиента.</span><span class="sxs-lookup"><span data-stu-id="82d40-444">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="82d40-445">Добавлен новый командлет Get-AzApiManagementSubscriptionKey, а Get-AzApiManagementSubscription теперь не возвращает ключи подписки.</span><span class="sxs-lookup"><span data-stu-id="82d40-445">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="82d40-446">Добавлен новый командлет Get-AzApiManagementTenantAccessSecret, а Get-AzApiManagementTenantAccess теперь не возвращает ключи.</span><span class="sxs-lookup"><span data-stu-id="82d40-446">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="82d40-447">Добавлен новый командлет Get-AzApiManagementTenantGitAccessSecret, а Get-AzApiManagementTenantGitAccess теперь не возвращает ключи.</span><span class="sxs-lookup"><span data-stu-id="82d40-447">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="82d40-448">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="82d40-448">Az.ApplicationInsights</span></span>
* <span data-ttu-id="82d40-449">В New-AzApplicationInsights добавлены параметры RetentionInDays, PublicNetworkAccessForIngestion и PublicNetworkAccessForQuery.</span><span class="sxs-lookup"><span data-stu-id="82d40-449">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="82d40-450">Создан командлет Update-AzApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="82d40-450">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="82d40-451">Созданы командлеты для связанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="82d40-451">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="82d40-452">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="82d40-452">Az.Batch</span></span>
* <span data-ttu-id="82d40-453">В командлеты Az.Batch добавлена поддержка пакетов SDK Microsoft.Azure.Batch версии 13.0.0 и SDK Microsoft.Azure.Management.Batch версии 9.0.0.</span><span class="sxs-lookup"><span data-stu-id="82d40-453">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="82d40-454">Теперь в New-AzBatchCertificate можно выбрать тип добавляемого сертификата с помощью нового параметра -CertificateKind.</span><span class="sxs-lookup"><span data-stu-id="82d40-454">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="82d40-455">В PSApplication удалено свойство ApplicationPackages.</span><span class="sxs-lookup"><span data-stu-id="82d40-455">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="82d40-456">Отдельные пакеты в приложении теперь можно извлечь с помощью Get-AzBatchApplicationPackage.</span><span class="sxs-lookup"><span data-stu-id="82d40-456">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="82d40-457">Пример: Get-AzBatchApplication -AccountName моя_учетная_запись -ResourceGroupName моя_группа_ресурсов -ApplicationId мое_приложение.</span><span class="sxs-lookup"><span data-stu-id="82d40-457">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="82d40-458">При создании пула с помощью New-AzBatchPool свойство VirtualMachineImageId элемента PSImageReference теперь может ссылаться только на образ из Общей коллекции образов.</span><span class="sxs-lookup"><span data-stu-id="82d40-458">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="82d40-459">При создании пула с помощью New-AzBatchPool пул можно подготовить без общедоступного IP-адреса, используя новое свойство PublicIPAddressConfiguration элемента PSNetworkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="82d40-459">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="82d40-460">Свойство PublicIPs элемента PSNetworkConfiguration было передано элементу PSPublicIPAddressConfiguration.</span><span class="sxs-lookup"><span data-stu-id="82d40-460">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="82d40-461">Это свойство можно указать, только если параметру IPAddressProvisioningType присвоено значение UserManaged.</span><span class="sxs-lookup"><span data-stu-id="82d40-461">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82d40-462">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82d40-462">Az.Compute</span></span>
* <span data-ttu-id="82d40-463">В командлет Update-AzVM добавлен параметр HostId.</span><span class="sxs-lookup"><span data-stu-id="82d40-463">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="82d40-464">Обновлена справочная документация по командлетам New-AzVMConfig, New-AzVmssConfig, Update-AzVmss, Set-AzVMOperatingSystem и Set-AzVmssOsProfile.</span><span class="sxs-lookup"><span data-stu-id="82d40-464">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="82d40-465">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="82d40-465">Breaking changes</span></span>
    - <span data-ttu-id="82d40-466">Параметр FilterExpression удален из командлета Get-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="82d40-466">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="82d40-467">Параметр AssignIdentity удален из командлетов New-AzVmssConfig, New-AzVMConfig и Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="82d40-467">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="82d40-468">Параметр AutomaticRepairMaxInstanceRepairsPercent удален из командлетов New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="82d40-468">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="82d40-469">Свойства AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus и VirtualMachineScaleSetsColocationStatus удалены из ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="82d40-469">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="82d40-470">Свойство MaxInstanceRepairsPercent удалено из AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="82d40-470">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="82d40-471">Типы AvailabilitySets, VirtualMachines и VirtualMachineScaleSets изменены с IList<SubResource> на IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="82d40-471">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="82d40-472">Уточнено описание командлета Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="82d40-472">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="82d40-473">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="82d40-473">Az.DataFactory</span></span>
* <span data-ttu-id="82d40-474">Добавлена поддержка операций CRUD для свойств среды выполнения потока данных в управляемой среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="82d40-474">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="82d40-475">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="82d40-475">Az.FrontDoor</span></span>
* <span data-ttu-id="82d40-476">Добавлены новые командлеты для создания, обновления, извлечения и удаления объекта обработчика правил Front Door.</span><span class="sxs-lookup"><span data-stu-id="82d40-476">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="82d40-477">Добавлены вспомогательные командлеты для создания объекта обработчика правил Front Door.</span><span class="sxs-lookup"><span data-stu-id="82d40-477">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="82d40-478">Добавлена ссылка обработчика правил на объект правила маршрутизации Front Door.</span><span class="sxs-lookup"><span data-stu-id="82d40-478">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="82d40-479">Добавлены параметры Приватного канала на серверный объект Front Door.</span><span class="sxs-lookup"><span data-stu-id="82d40-479">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="82d40-480">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="82d40-480">Az.Functions</span></span>
* <span data-ttu-id="82d40-481">Вышла общедоступная версия модуля Az.Functions.</span><span class="sxs-lookup"><span data-stu-id="82d40-481">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="82d40-482">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="82d40-482">Az.HDInsight</span></span>
* <span data-ttu-id="82d40-483">Добавлена поддержка шифрования управляемых клиентом ключей.</span><span class="sxs-lookup"><span data-stu-id="82d40-483">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="82d40-484">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="82d40-484">Az.HealthcareApis</span></span>
* <span data-ttu-id="82d40-485">Политики доступа для текущего субъекта теперь не используются по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="82d40-485">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="82d40-486">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="82d40-486">Az.IotHub</span></span>
* <span data-ttu-id="82d40-487">Добавлен командлет для вызова запроса в центре Интернета вещей для получения данных с помощью SQL-подобного языка.</span><span class="sxs-lookup"><span data-stu-id="82d40-487">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="82d40-488">Устранена проблема, когда с помощью Add-AzIotHubDevice не удавалось создать устройство с поддержкой IoT Edge без дочерних устройств (№ 11597).</span><span class="sxs-lookup"><span data-stu-id="82d40-488">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="82d40-489">Добавлен командлет для создания маркера SAS для Центра Интернета вещей, устройства или модуля.</span><span class="sxs-lookup"><span data-stu-id="82d40-489">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="82d40-490">Добавлен командлет для вызова запроса метрик конфигурации.</span><span class="sxs-lookup"><span data-stu-id="82d40-490">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="82d40-491">Появилась возможность управлять автоматическим развертыванием IoT Edge в большом масштабе.</span><span class="sxs-lookup"><span data-stu-id="82d40-491">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="82d40-492">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="82d40-492">New cmdlets are:</span></span>
    - <span data-ttu-id="82d40-493">Add-AzIotHubDeployment;</span><span class="sxs-lookup"><span data-stu-id="82d40-493">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="82d40-494">Get-AzIotHubDeployment;</span><span class="sxs-lookup"><span data-stu-id="82d40-494">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="82d40-495">Remove-AzIotHubDeployment;</span><span class="sxs-lookup"><span data-stu-id="82d40-495">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="82d40-496">Set-AzIotHubDeployment.</span><span class="sxs-lookup"><span data-stu-id="82d40-496">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="82d40-497">Добавлен командлет для вызова запроса метрик развертывания IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="82d40-497">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="82d40-498">Добавлен командлет для применения содержимого конфигурации к указанному пограничному устройству.</span><span class="sxs-lookup"><span data-stu-id="82d40-498">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="82d40-499">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="82d40-499">Az.KeyVault</span></span>
* <span data-ttu-id="82d40-500">Удалены два псевдонима: New-AzKeyVaultCertificateAdministratorDetails и New-AzKeyVaultCertificateOrganizationDetails.</span><span class="sxs-lookup"><span data-stu-id="82d40-500">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="82d40-501">При создании хранилища ключей обратимое удаление включено по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="82d40-501">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="82d40-502">Можно задать правила сети, чтобы при создании хранилища ключей управлять доступом из определенных сетевых расположений.</span><span class="sxs-lookup"><span data-stu-id="82d40-502">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="82d40-503">Добавлена возможность создания собственных ключей (BYOK).</span><span class="sxs-lookup"><span data-stu-id="82d40-503">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="82d40-504">С помощью Add-AzKeyVaultKey теперь можно создавать ключ обмена ключами.</span><span class="sxs-lookup"><span data-stu-id="82d40-504">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="82d40-505">С помощью Get-AzKeyVaultKey можно скачать открытый ключ в формате PEM.</span><span class="sxs-lookup"><span data-stu-id="82d40-505">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="82d40-506">Обновлен раздел KeyOps справочной документации по Add-AzKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="82d40-506">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="82d40-507">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="82d40-507">Az.Monitor</span></span>
* <span data-ttu-id="82d40-508">Исправлена ошибка Set-AzDiagnosticSettings, когда политика хранения не применялась ко всем категориям (№ 11589).</span><span class="sxs-lookup"><span data-stu-id="82d40-508">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="82d40-509">Добавлена поддержка критериев доступности веб-теста для оповещения метрики версии 2.</span><span class="sxs-lookup"><span data-stu-id="82d40-509">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="82d40-510">В New-AzMetricAlertRuleV2Criteria добавлена возможность создавать критерии доступности веб-теста.</span><span class="sxs-lookup"><span data-stu-id="82d40-510">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="82d40-511">Add-AzMetricAlertRuleV2 теперь поддерживает новые критерии доступности веб-теста.</span><span class="sxs-lookup"><span data-stu-id="82d40-511">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="82d40-512">В PSLogProfile исправлено избыточное определение RetentionPolicy (№ 7608).</span><span class="sxs-lookup"><span data-stu-id="82d40-512">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="82d40-513">В PSEventData удалены избыточные определения свойств (№ 11353).</span><span class="sxs-lookup"><span data-stu-id="82d40-513">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="82d40-514">Командлет Get-AzLog переименован в Get-AzActivityLog.</span><span class="sxs-lookup"><span data-stu-id="82d40-514">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82d40-515">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82d40-515">Az.Network</span></span>
* <span data-ttu-id="82d40-516">Добавлен атрибут критического изменения, сообщающий о том, что поведение зоны по умолчанию будет изменено.</span><span class="sxs-lookup"><span data-stu-id="82d40-516">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="82d40-517">New-AzPublicIpAddress;</span><span class="sxs-lookup"><span data-stu-id="82d40-517">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="82d40-518">New-AzPublicIpPrefix;</span><span class="sxs-lookup"><span data-stu-id="82d40-518">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="82d40-519">New-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="82d40-519">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="82d40-520">Добавлена поддержка нового ресурса верхнего уровня SecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="82d40-520">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="82d40-521">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="82d40-521">New cmdlets added:</span></span>
        - <span data-ttu-id="82d40-522">New-AzSecurityPartnerProvider;</span><span class="sxs-lookup"><span data-stu-id="82d40-522">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="82d40-523">Remove-AzSecurityPartnerProvider;</span><span class="sxs-lookup"><span data-stu-id="82d40-523">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="82d40-524">Get-AzSecurityPartnerProvider;</span><span class="sxs-lookup"><span data-stu-id="82d40-524">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="82d40-525">Set-AzSecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="82d40-525">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="82d40-526">В PSPrivateLinkResource добавлен параметр RequiredZoneNames, а в PSPrivateEndpointConnection — GroupId.</span><span class="sxs-lookup"><span data-stu-id="82d40-526">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="82d40-527">Исправлен неправильный тип параметра SuccessThresholdRoundTripTimeMs для New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.</span><span class="sxs-lookup"><span data-stu-id="82d40-527">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="82d40-528">В командлетах VirtualWan аргументу AllowVnetToVnetTraffic теперь по умолчанию присвоено значение True.</span><span class="sxs-lookup"><span data-stu-id="82d40-528">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="82d40-529">New-AzVirtualWan;</span><span class="sxs-lookup"><span data-stu-id="82d40-529">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="82d40-530">Update-AzVirtualWan.</span><span class="sxs-lookup"><span data-stu-id="82d40-530">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="82d40-531">Добавлены новые командлеты для поддержки группы зон DNS для частной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="82d40-531">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="82d40-532">New-AzPrivateDnsZoneConfig;</span><span class="sxs-lookup"><span data-stu-id="82d40-532">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="82d40-533">Get-AzPrivateDnsZoneGroup;</span><span class="sxs-lookup"><span data-stu-id="82d40-533">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="82d40-534">New-AzPrivateDnsZoneGroup;</span><span class="sxs-lookup"><span data-stu-id="82d40-534">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="82d40-535">Set-AzPrivateDnsZoneGroup;</span><span class="sxs-lookup"><span data-stu-id="82d40-535">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="82d40-536">Remove-AzPrivateDnsZoneGroup.</span><span class="sxs-lookup"><span data-stu-id="82d40-536">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="82d40-537">В AzureFirewall добавлены параметры DNSEnableProxy, DNSRequireProxyForNetworkRules и DNSServers.</span><span class="sxs-lookup"><span data-stu-id="82d40-537">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="82d40-538">В AzureFirewall добавлены параметры EnableDnsProxy, DnsProxyNotRequiredForNetworkRule и DnsServer.</span><span class="sxs-lookup"><span data-stu-id="82d40-538">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="82d40-539">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="82d40-539">Updated cmdlet:</span></span>
        - <span data-ttu-id="82d40-540">New-AzFirewall.</span><span class="sxs-lookup"><span data-stu-id="82d40-540">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="82d40-541">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="82d40-541">Az.OperationalInsights</span></span>
* <span data-ttu-id="82d40-542">Обновлен устаревший код для использования новых пакетов SDK.</span><span class="sxs-lookup"><span data-stu-id="82d40-542">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="82d40-543">Из-за устаревших API-интерфейсов удалены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="82d40-543">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="82d40-544">Get-AzOperationalInsightsSavedSearchResult (псевдоним Get-AzOperationalInsightsSavedSearchResults);</span><span class="sxs-lookup"><span data-stu-id="82d40-544">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="82d40-545">Get-AzOperationalInsightsSearchResult (псевдоним Get-AzOperationalInsightsSearchResults);</span><span class="sxs-lookup"><span data-stu-id="82d40-545">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="82d40-546">Get-AzOperationalInsightsLinkTarget (псевдоним Get-AzOperationalInsightsLinkTargets).</span><span class="sxs-lookup"><span data-stu-id="82d40-546">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="82d40-547">В Set-AzOperationalInsightsWorkspace и New-AzOperationalInsightsWorkspace добавлены новые параметры.</span><span class="sxs-lookup"><span data-stu-id="82d40-547">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="82d40-548">Созданы командлеты для связанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="82d40-548">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="82d40-549">Созданы командлеты для кластеров и связанной службы.</span><span class="sxs-lookup"><span data-stu-id="82d40-549">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="82d40-550">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="82d40-550">Az.RecoveryServices</span></span>
* <span data-ttu-id="82d40-551">В Azure Site Recovery добавлена поддержка защиты поставщика Azure для групп размещения виртуальных машин Azure близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="82d40-551">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="82d40-552">В Azure Site Recovery добавлена поддержка репликации из зоны в зону.</span><span class="sxs-lookup"><span data-stu-id="82d40-552">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="82d40-553">В Azure Backup добавлена поддержка долгосрочного хранения для точек восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-553">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="82d40-554">В выходные данные командлета Get-AzRecoveryServicesBackupItem добавлены свойства исключения диска, добавленного в Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="82d40-554">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="82d40-555">Добавлена частная конечная точка для файла учетных данных хранилища для службы Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="82d40-555">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="82d40-556">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82d40-556">Az.Resources</span></span>
* <span data-ttu-id="82d40-557">Добавлено предупреждение о задержке представления при создании определения роли.</span><span class="sxs-lookup"><span data-stu-id="82d40-557">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="82d40-558">Командлеты политики теперь выводят строго типизированные объекты.</span><span class="sxs-lookup"><span data-stu-id="82d40-558">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="82d40-559">Из командлета Get-AzResourceLock удален параметр -TenantLevel (№ 11335).</span><span class="sxs-lookup"><span data-stu-id="82d40-559">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="82d40-560">Исправлена ошибка с Remove-AzResourceGroup -Id ResourceId (№ 9882).</span><span class="sxs-lookup"><span data-stu-id="82d40-560">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="82d40-561">Добавлен новый командлет для получения результатов анализа гипотетических вариантов из шаблона ARM в области группы ресурсов: Get-AzDeploymentResourceGroupWhatIfResult.</span><span class="sxs-lookup"><span data-stu-id="82d40-561">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="82d40-562">Добавлен новый командлет для получения результатов анализа гипотетических вариантов из шаблона ARM в области подписки: Get-AzDeploymentWhatIfResult.</span><span class="sxs-lookup"><span data-stu-id="82d40-562">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="82d40-563">Alias: Get-AzSubscriptionDeploymentWhatIf.</span><span class="sxs-lookup"><span data-stu-id="82d40-563">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="82d40-564">Переопределены параметры -WhatIf и -Confirm для New-AzDeployment и New-AzResourceGroupDeployment для использования результатов анализа гипотетических вариантов из шаблона ARM.</span><span class="sxs-lookup"><span data-stu-id="82d40-564">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="82d40-565">В командлеты развертывания добавлено сообщение об устаревании для параметра ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="82d40-565">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="82d40-566">Добавлена возможность отображения улучшенных сообщений об ошибках при развертывании.</span><span class="sxs-lookup"><span data-stu-id="82d40-566">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="82d40-567">Добавлена возможность регистрации correlationId для сбоев развертывания.</span><span class="sxs-lookup"><span data-stu-id="82d40-567">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="82d40-568">В выходные данные скрипта развертывания добавлено свойство error.</span><span class="sxs-lookup"><span data-stu-id="82d40-568">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="82d40-569">Пакет NuGet Microsoft.Azure.Management.ResourceManager обновлен до версии 3.7.1-preview.</span><span class="sxs-lookup"><span data-stu-id="82d40-569">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="82d40-570">Удаленные определенные тестовые случаи как свойство error в DeploymentValidateResult были изменены на доступные только для чтения из пакета NuGet версии 3.7.1-preview.</span><span class="sxs-lookup"><span data-stu-id="82d40-570">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="82d40-571">Добавлен GenericResourceExpanded из пакета SDK ResourceManager версии 3.7.1-preview.</span><span class="sxs-lookup"><span data-stu-id="82d40-571">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="82d40-572">Добавлена поддержка тегов для всех командлетов Get для развертывания, а также для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="82d40-572">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="82d40-573">New-AzDeployment;</span><span class="sxs-lookup"><span data-stu-id="82d40-573">'New-AzDeployment'</span></span>
    - <span data-ttu-id="82d40-574">New-AzManagementGroupDeployment;</span><span class="sxs-lookup"><span data-stu-id="82d40-574">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="82d40-575">New-AzResourceGroupDeployment;</span><span class="sxs-lookup"><span data-stu-id="82d40-575">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="82d40-576">New-AzTenantDeployment.</span><span class="sxs-lookup"><span data-stu-id="82d40-576">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="82d40-577">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="82d40-577">Az.ServiceFabric</span></span>
* <span data-ttu-id="82d40-578">Исправлена ошибка при добавлении сертификата с помощью параметра -SecretIdentifier, когда возвращался неправильный отпечаток сертификата.</span><span class="sxs-lookup"><span data-stu-id="82d40-578">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="82d40-579">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82d40-579">Az.Sql</span></span>
* <span data-ttu-id="82d40-580">Оптимизирована работа следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="82d40-580">Enhance performance of:</span></span>
    - <span data-ttu-id="82d40-581">Set-AzSqlDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="82d40-581">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="82d40-582">Set-AzSqlInstanceDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="82d40-582">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="82d40-583">Remove-AzSqlDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="82d40-583">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="82d40-584">Remove-AzSqlInstanceDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="82d40-584">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="82d40-585">Enable-AzSqlDatabaseSensitivityRecommendation;</span><span class="sxs-lookup"><span data-stu-id="82d40-585">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="82d40-586">Enable-AzSqlInstanceDatabaseSensitivityRecommendation;</span><span class="sxs-lookup"><span data-stu-id="82d40-586">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="82d40-587">Disable-AzSqlDatabaseSensitivityRecommendation;</span><span class="sxs-lookup"><span data-stu-id="82d40-587">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="82d40-588">Disable-AzSqlInstanceDatabaseSensitivityRecommendation.</span><span class="sxs-lookup"><span data-stu-id="82d40-588">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="82d40-589">Удалена проверка на стороне клиента параметра RetentionDays из командлета Set-AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="82d40-589">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="82d40-590">Добавлен аудит учетной записи хранения в виртуальной сети. Исправлена ошибка при создании роли участника данных BLOB-объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="82d40-590">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="82d40-591">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="82d40-591">Az.Storage</span></span>
* <span data-ttu-id="82d40-592">В командлет Get-AzStorageAccount добавлен параметр -AsJob.</span><span class="sxs-lookup"><span data-stu-id="82d40-592">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="82d40-593">Параметр KeyVersion теперь является необязательным при изменении учетной записи хранения с помощью KeyvaultEncryption, что обеспечивает поддержку автоматической смены ключа.</span><span class="sxs-lookup"><span data-stu-id="82d40-593">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="82d40-594">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="82d40-594">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="82d40-595">Исправлена ошибка при удалении каталога файлов Azure с конвейером.</span><span class="sxs-lookup"><span data-stu-id="82d40-595">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="82d40-596">Remove-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="82d40-596">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="82d40-597">Исправлена ошибка 9880. Значение DefaultAction для NetWorkRule приведено в соответствие со Swagger.</span><span class="sxs-lookup"><span data-stu-id="82d40-597">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="82d40-598">Update-AzStorageAccountNetworkRuleSet;</span><span class="sxs-lookup"><span data-stu-id="82d40-598">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="82d40-599">Get-AzStorageAccountNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="82d40-599">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="82d40-600">Исправлена ошибка 11624. При добавлении NetworkRules дублирующиеся правила пропускаются, чтобы не происходил сбой сервера.</span><span class="sxs-lookup"><span data-stu-id="82d40-600">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="82d40-601">Add-AzStorageAccountNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="82d40-601">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="82d40-602">Версия пакета SDK Microsoft.Azure.Cosmos.Table обновлена до 1.0.7.</span><span class="sxs-lookup"><span data-stu-id="82d40-602">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="82d40-603">Добавлено предупреждающее сообщение, напоминающее пользователю о необходимости повторного вывода списка с помощью ContinuationToken, когда в списке элементов Data Lake 2-го поколения возвращается только часть элементов.</span><span class="sxs-lookup"><span data-stu-id="82d40-603">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="82d40-604">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="82d40-604">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="82d40-605">Добавлена возможность создания или изменения учетной записи хранения с использованием проверки подлинности Active Directory для Файлов Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-605">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="82d40-606">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="82d40-606">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="82d40-607">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="82d40-607">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="82d40-608">Добавлена возможность создания и просмотра ключей Kerberos учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="82d40-608">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="82d40-609">New-AzStorageAccountKey;</span><span class="sxs-lookup"><span data-stu-id="82d40-609">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="82d40-610">Get-AzStorageAccountKey.</span><span class="sxs-lookup"><span data-stu-id="82d40-610">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="82d40-611">Добавлена возможность отработки отказа для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="82d40-611">Supported failover Storage account</span></span>
    - <span data-ttu-id="82d40-612">Invoke-AzStorageAccountFailover.</span><span class="sxs-lookup"><span data-stu-id="82d40-612">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="82d40-613">Обновлена справка по Get-AzStorageBlobCopyState.</span><span class="sxs-lookup"><span data-stu-id="82d40-613">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="82d40-614">Обновлена справка по Get-AzStorageFileCopyState и Start-AzStorageBlobCopy.</span><span class="sxs-lookup"><span data-stu-id="82d40-614">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="82d40-615">Появилась интегрированная клиентская библиотека хранилища версии 12 для командлетов очередей и файлов.</span><span class="sxs-lookup"><span data-stu-id="82d40-615">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="82d40-616">Тип выходных данных изменен с CloudFile на AzureStorageFile. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="82d40-616">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="82d40-617">Get-AzStorageFile;</span><span class="sxs-lookup"><span data-stu-id="82d40-617">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="82d40-618">Remove-AzStorageFile;</span><span class="sxs-lookup"><span data-stu-id="82d40-618">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="82d40-619">Get-AzStorageFileContent;</span><span class="sxs-lookup"><span data-stu-id="82d40-619">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="82d40-620">Set-AzStorageFileContent;</span><span class="sxs-lookup"><span data-stu-id="82d40-620">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="82d40-621">Start-AzStorageFileCopy.</span><span class="sxs-lookup"><span data-stu-id="82d40-621">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="82d40-622">Тип выходных данных изменен с CloudFileDirectory на AzureStorageFileDirectory. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="82d40-622">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="82d40-623">New-AzStorageDirectory;</span><span class="sxs-lookup"><span data-stu-id="82d40-623">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="82d40-624">Remove-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="82d40-624">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="82d40-625">Тип выходных данных изменен с CloudFileShare на AzureStorageFileShare. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="82d40-625">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="82d40-626">Get-AzStorageShare;</span><span class="sxs-lookup"><span data-stu-id="82d40-626">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="82d40-627">New-AzStorageShare;</span><span class="sxs-lookup"><span data-stu-id="82d40-627">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="82d40-628">Remove-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="82d40-628">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="82d40-629">Тип выходных данных изменен с FileShareProperties на AzureStorageFileShare. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="82d40-629">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="82d40-630">Set-AzStorageShareQuota.</span><span class="sxs-lookup"><span data-stu-id="82d40-630">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="82d40-631">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="82d40-631">Az.TrafficManager</span></span>
* <span data-ttu-id="82d40-632">Исправлено неправильное имя профиля в подробных выходных данных DisableAzureTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="82d40-632">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="82d40-633">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="82d40-633">Az.Websites</span></span>
* <span data-ttu-id="82d40-634">Исправлена опечатка в справке по Update-AzWebAppAccessRestrictionConfig.</span><span class="sxs-lookup"><span data-stu-id="82d40-634">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="82d40-635">3.8.0 — апрель 2020 г.</span><span class="sxs-lookup"><span data-stu-id="82d40-635">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="82d40-636">Основные сведения о новых возможностях с момента последнего выпуска</span><span class="sxs-lookup"><span data-stu-id="82d40-636">Highlights since the last release</span></span>
* <span data-ttu-id="82d40-637">Версии PowerShell, которые поддерживает Az.Storage: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="82d40-637">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="82d40-638">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="82d40-638">Az.Accounts</span></span>
* <span data-ttu-id="82d40-639">Обновлен URL-адрес опроса Azure PowerShell в Resolve-AzError [11507].</span><span class="sxs-lookup"><span data-stu-id="82d40-639">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="82d40-640">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="82d40-640">Az.ApiManagement</span></span>
* <span data-ttu-id="82d40-641">Добавлено уведомление о критическом изменении для изменения выходных данных командлетов, выполняющих действия с файлами в Azure, в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="82d40-641">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="82d40-642">Обновлена документация для Set-AzApiManagementGroup с указанием параметра GroupId.</span><span class="sxs-lookup"><span data-stu-id="82d40-642">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="82d40-643">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="82d40-643">Az.Cdn</span></span>
* <span data-ttu-id="82d40-644">Исправлено отображение ценовой категории (SKU), связанной с ChinaCDN.</span><span class="sxs-lookup"><span data-stu-id="82d40-644">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="82d40-645">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="82d40-645">Az.CognitiveServices</span></span>
* <span data-ttu-id="82d40-646">Включена поддержка Identity, Encryption, UserOwnedStorage.</span><span class="sxs-lookup"><span data-stu-id="82d40-646">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82d40-647">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82d40-647">Az.Compute</span></span>
* <span data-ttu-id="82d40-648">Добавлен командлет Set-AzVmssOrchestrationServiceState.</span><span class="sxs-lookup"><span data-stu-id="82d40-648">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="82d40-649">Get-AzVmss с параметром -InstanceView отображает состояния OrchestrationService.</span><span class="sxs-lookup"><span data-stu-id="82d40-649">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="82d40-650">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="82d40-650">Az.IotHub</span></span>
* <span data-ttu-id="82d40-651">Реализовано управление конфигурацией двойника устройства Интернета вещей. Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="82d40-651">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="82d40-652">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="82d40-652">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="82d40-653">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="82d40-653">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="82d40-654">Добавлен командлет для вызова прямого метода на устройстве в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="82d40-654">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="82d40-655">Реализовано управление конфигурацией двойника модуля устройства Интернета вещей. Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="82d40-655">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="82d40-656">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="82d40-656">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="82d40-657">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="82d40-657">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="82d40-658">Реализовано управление конфигурацией автоматического управления устройствами в центре Интернета вещей в большом масштабе.</span><span class="sxs-lookup"><span data-stu-id="82d40-658">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="82d40-659">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="82d40-659">New cmdlets are:</span></span>
    - <span data-ttu-id="82d40-660">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="82d40-660">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="82d40-661">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="82d40-661">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="82d40-662">Remove-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="82d40-662">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="82d40-663">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="82d40-663">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="82d40-664">Добавлен командлет для вызова метода периферийного модуля в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="82d40-664">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="82d40-665">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="82d40-665">Az.KeyVault</span></span>
* <span data-ttu-id="82d40-666">Добавлен новый командлет Update-AzKeyVault, который может включать защиту от обратимого удаления и очистки в хранилище.</span><span class="sxs-lookup"><span data-stu-id="82d40-666">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="82d40-667">Включена поддержка Microsoft.PowerShell.SecretManagement [11178].</span><span class="sxs-lookup"><span data-stu-id="82d40-667">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="82d40-668">Исправлена ошибка в примерах Remove-AzKeyVaultManagedStorageSasDefinition [11479].</span><span class="sxs-lookup"><span data-stu-id="82d40-668">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="82d40-669">Включена поддержка частной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="82d40-669">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="82d40-670">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="82d40-670">Az.Maintenance</span></span>
* <span data-ttu-id="82d40-671">Опубликована версия выпуска командлетов обслуживания для общедоступной версии.</span><span class="sxs-lookup"><span data-stu-id="82d40-671">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="82d40-672">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="82d40-672">Az.Monitor</span></span>
* <span data-ttu-id="82d40-673">Добавлены командлеты для области приватных каналов:</span><span class="sxs-lookup"><span data-stu-id="82d40-673">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="82d40-674">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="82d40-674">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="82d40-675">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="82d40-675">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="82d40-676">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="82d40-676">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="82d40-677">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="82d40-677">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="82d40-678">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="82d40-678">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="82d40-679">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="82d40-679">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="82d40-680">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="82d40-680">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82d40-681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82d40-681">Az.Network</span></span>
* <span data-ttu-id="82d40-682">Обновлены командлеты для включения подключения на частном IP-адресе для шлюза виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="82d40-682">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="82d40-683">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="82d40-683">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="82d40-684">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="82d40-684">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="82d40-685">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="82d40-685">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="82d40-686">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="82d40-686">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="82d40-687">Обновлены командлеты для включения шлюзов LocalNetworkGateways и сайтов VpnSites на основе FQDN:</span><span class="sxs-lookup"><span data-stu-id="82d40-687">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="82d40-688">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="82d40-688">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="82d40-689">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="82d40-689">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="82d40-690">Включена поддержка семейства адресов IPv6 в ExpressRouteCircuitConnectionConfig (Global Reach).</span><span class="sxs-lookup"><span data-stu-id="82d40-690">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="82d40-691">Добавлен командлет Set-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="82d40-691">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="82d40-692">Позволяет выполнять настройку всех существующих свойств, включая IPv6CircuitConnectionProperties.</span><span class="sxs-lookup"><span data-stu-id="82d40-692">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="82d40-693">Обновлен командлет Add-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="82d40-693">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="82d40-694">Добавлен еще один необязательный параметр AddressPrefixType для указания семейства адресов префикса адреса.</span><span class="sxs-lookup"><span data-stu-id="82d40-694">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="82d40-695">Обновлены командлеты для включения параметра времени ожидания для обнаружения неиспользуемых одноранговых узлов (DPD) в подключениях шлюзов виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="82d40-695">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="82d40-696">New-AzVirtualNetworkGatewayConnection;</span><span class="sxs-lookup"><span data-stu-id="82d40-696">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="82d40-697">Set-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="82d40-697">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="82d40-698">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="82d40-698">Az.PolicyInsights</span></span>
* <span data-ttu-id="82d40-699">Добавлен командлет Start-AzPolicyComplianceScan для запуска проверок соответствия политикам.</span><span class="sxs-lookup"><span data-stu-id="82d40-699">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="82d40-700">Добавлены версии определения политики, определения набора и назначения в выходные данные командлета Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="82d40-700">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="82d40-701">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="82d40-701">Az.ServiceFabric</span></span>
* <span data-ttu-id="82d40-702">Улучшено форматирование и наглядность кода в примерах New-AzServiceFabricCluster.</span><span class="sxs-lookup"><span data-stu-id="82d40-702">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="82d40-703">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82d40-703">Az.Sql</span></span>
* <span data-ttu-id="82d40-704">Добавлены командлеты Get-AzSqlInstanceOperation и Stop-AzSqlInstanceOperation.</span><span class="sxs-lookup"><span data-stu-id="82d40-704">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="82d40-705">Включен аудит учетной записи хранения в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="82d40-705">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="82d40-706">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="82d40-706">Az.Storage</span></span>
* <span data-ttu-id="82d40-707">Добавлено уведомление о критическом изменении для изменения выходных данных командлетов, выполняющих действия с файлами в Azure, в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="82d40-707">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="82d40-708">Включена поддержка новых имен SKU StandardGZRS, StandardRAGZRS при создании или обновлении учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="82d40-708">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="82d40-709">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="82d40-709">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="82d40-710">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="82d40-710">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="82d40-711">Добавлена поддержка DataLake 2-го поколения.</span><span class="sxs-lookup"><span data-stu-id="82d40-711">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="82d40-712">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="82d40-712">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="82d40-713">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="82d40-713">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="82d40-714">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="82d40-714">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="82d40-715">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="82d40-715">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="82d40-716">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="82d40-716">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="82d40-717">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="82d40-717">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="82d40-718">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="82d40-718">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="82d40-719">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="82d40-719">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="82d40-720">0.10.0-preview — апрель 2020 г.</span><span class="sxs-lookup"><span data-stu-id="82d40-720">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="82d40-721">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="82d40-721">General</span></span>
* <span data-ttu-id="82d40-722">Модуль Az стали доступными в предварительной версии в Azure Stack Hub.</span><span class="sxs-lookup"><span data-stu-id="82d40-722">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="82d40-723">Это обеспечивает кросс-платформенную совместимость с Linux и macOs.</span><span class="sxs-lookup"><span data-stu-id="82d40-723">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="82d40-724">Azure Stack Hub теперь поддерживает PowerShell Core с модулями Az (см. [дополнительные сведения](https://aka.ms/az4AzureStack))</span><span class="sxs-lookup"><span data-stu-id="82d40-724">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="82d40-725">Модули Az поддерживают профиль 2019-03-01-hybrid:</span><span class="sxs-lookup"><span data-stu-id="82d40-725">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="82d40-726">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="82d40-726">Az.Billing</span></span>
  - <span data-ttu-id="82d40-727">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82d40-727">Az.Compute</span></span>
  - <span data-ttu-id="82d40-728">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="82d40-728">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="82d40-729">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="82d40-729">Az.EventHub</span></span>
  - <span data-ttu-id="82d40-730">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="82d40-730">Az.IotHub</span></span>
  - <span data-ttu-id="82d40-731">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="82d40-731">Az.KeyVault</span></span>
  - <span data-ttu-id="82d40-732">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="82d40-732">Az.Monitor</span></span>
  - <span data-ttu-id="82d40-733">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82d40-733">Az.Network</span></span>
  - <span data-ttu-id="82d40-734">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82d40-734">Az.Resources</span></span>
  - <span data-ttu-id="82d40-735">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="82d40-735">Az.Storage</span></span>
  - <span data-ttu-id="82d40-736">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="82d40-736">Az.Websites</span></span>
* <span data-ttu-id="82d40-737">В PowerShell появились три новых модуля Az, которые работают с Azure Stack Hub: Az.Databox, Az.IotHub и Az.EventHub.</span><span class="sxs-lookup"><span data-stu-id="82d40-737">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="82d40-738">Команды остаются прежними же за исключением незначительных изменений, таких как изменение AzureRM на Az.</span><span class="sxs-lookup"><span data-stu-id="82d40-738">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="82d40-739">См. обновленную ссылку на документацию по [PowerShell для Azure Stack Hub](https://aka.ms/InstallASHPowerShell)</span><span class="sxs-lookup"><span data-stu-id="82d40-739">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="82d40-740">3.7.0 — март 2020 г.</span><span class="sxs-lookup"><span data-stu-id="82d40-740">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="82d40-741">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="82d40-741">Az.Accounts</span></span>
* <span data-ttu-id="82d40-742">Исправлено исключение NullReferenceException командлетов Get-AzTenant/Get-AzDefault/Set-AzDefault, если вход не выполнен [10292]</span><span class="sxs-lookup"><span data-stu-id="82d40-742">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82d40-743">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82d40-743">Az.Compute</span></span>
* <span data-ttu-id="82d40-744">Добавлены следующие параметры к командлету New-AzDiskConfig:</span><span class="sxs-lookup"><span data-stu-id="82d40-744">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="82d40-745">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="82d40-745">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="82d40-746">Разрешено свойство Encryption для параметра Target командлета New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="82d40-746">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="82d40-747">Исправлена проблема с tempDisk для командлетов Set-AzVmss -Reimage и Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="82d40-747">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="82d40-748">[11354]</span><span class="sxs-lookup"><span data-stu-id="82d40-748">[#11354]</span></span>
* <span data-ttu-id="82d40-749">Добавлена поддержка нового расширения SAP для указанных ниже командлетов</span><span class="sxs-lookup"><span data-stu-id="82d40-749">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="82d40-750">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="82d40-750">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="82d40-751">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="82d40-751">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="82d40-752">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="82d40-752">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="82d40-753">Update-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="82d40-753">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="82d40-754">Исправлены ошибки в примерах справки</span><span class="sxs-lookup"><span data-stu-id="82d40-754">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="82d40-755">Показано точное строковое значение в табличном формате для свойства PowerState виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="82d40-755">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="82d40-756">New-AzVmssConfig: исправлена сериализация свойства AutomaticRepairs, если параметр SinglePlacementGroup отключен.</span><span class="sxs-lookup"><span data-stu-id="82d40-756">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="82d40-757">[11257]</span><span class="sxs-lookup"><span data-stu-id="82d40-757">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="82d40-758">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="82d40-758">Az.DataFactory</span></span>
* <span data-ttu-id="82d40-759">Пакет SDK ADF для .NET обновлен до версии 4.8.0.</span><span class="sxs-lookup"><span data-stu-id="82d40-759">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="82d40-760">Добавлены необязательные параметры для команды Invoke-AzDataFactoryV2Pipeline для поддержки повторного запуска.</span><span class="sxs-lookup"><span data-stu-id="82d40-760">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="82d40-761">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="82d40-761">Az.DataLakeStore</span></span>
* <span data-ttu-id="82d40-762">Добавлено описание критического изменения для Export-AzDataLakeStoreItem и Import-AzDataLakeStoreItem.</span><span class="sxs-lookup"><span data-stu-id="82d40-762">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="82d40-763">Добавлен параметр кодирования байтов для New-AzDataLakeStoreItem, Add-AzDAtaLakeStoreItemContent и Get-AzDAtaLakeStoreItemContent.</span><span class="sxs-lookup"><span data-stu-id="82d40-763">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="82d40-764">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="82d40-764">Az.HDInsight</span></span>
* <span data-ttu-id="82d40-765">Добавлена поддержка указания минимальной поддерживаемой версии TLS при создании кластера.</span><span class="sxs-lookup"><span data-stu-id="82d40-765">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="82d40-766">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="82d40-766">Az.IotHub</span></span>
* <span data-ttu-id="82d40-767">Добавлена поддержка для управления распределенными параметрами на отдельных устройствах.</span><span class="sxs-lookup"><span data-stu-id="82d40-767">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="82d40-768">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="82d40-768">New Cmdlets are:</span></span>
    - <span data-ttu-id="82d40-769">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="82d40-769">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="82d40-770">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="82d40-770">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="82d40-771">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="82d40-771">Az.KeyVault</span></span>
* <span data-ttu-id="82d40-772">Добавлены атрибуты критических изменений для New-AzKeyVault.</span><span class="sxs-lookup"><span data-stu-id="82d40-772">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="82d40-773">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="82d40-773">Az.Monitor</span></span>
* <span data-ttu-id="82d40-774">Обновлена документация для New-AzScheduledQueryRuleLogMetricTrigger.</span><span class="sxs-lookup"><span data-stu-id="82d40-774">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82d40-775">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82d40-775">Az.Network</span></span>
* <span data-ttu-id="82d40-776">Обновлены командлеты для поддержки подключений VirtualHubVnetConnections между клиентами</span><span class="sxs-lookup"><span data-stu-id="82d40-776">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="82d40-777">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="82d40-777">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="82d40-778">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="82d40-778">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="82d40-779">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="82d40-779">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="82d40-780">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="82d40-780">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="82d40-781">Удалена зависимость пакета SDK для управления SQL.</span><span class="sxs-lookup"><span data-stu-id="82d40-781">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="82d40-782">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="82d40-782">Az.PolicyInsights</span></span>
* <span data-ttu-id="82d40-783">Улучшены сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="82d40-783">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="82d40-784">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="82d40-784">Az.RecoveryServices</span></span>
* <span data-ttu-id="82d40-785">В Azure Site Recovery реализована поддержка повторной защиты и обновлены свойства зашифрованных виртуальных машин диска Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-785">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="82d40-786">Добавлена возможность мониторинг аварийного восстановления для свойств VmwareToAzure в Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="82d40-786">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="82d40-787">В Azure Backup реализована поддержка повторного обновления политики для элементов с ошибками.</span><span class="sxs-lookup"><span data-stu-id="82d40-787">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="82d40-788">В Azure Backup реализована поддержка параметров исключения диска во время резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="82d40-788">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="82d40-789">В Azure Backup реализована поддержка восстановления нескольких файлов или папок в AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="82d40-789">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="82d40-790">В Azure Backup реализована поддержка указанной пользователем группы Resourcegroup при обновлении политики IaasVM.</span><span class="sxs-lookup"><span data-stu-id="82d40-790">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="82d40-791">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82d40-791">Az.Resources</span></span>
* <span data-ttu-id="82d40-792">Исправлена команда Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType для использования фактической версии apiVersion ресурсов (а не версии apiVersion по умолчанию) [11267].</span><span class="sxs-lookup"><span data-stu-id="82d40-792">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="82d40-793">Добавлена возможность регистрации correlationId для сценариев с ошибками.</span><span class="sxs-lookup"><span data-stu-id="82d40-793">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="82d40-794">Незначительно изменена документация по Get-AzResourceLock.</span><span class="sxs-lookup"><span data-stu-id="82d40-794">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="82d40-795">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="82d40-795">Added example.</span></span>
* <span data-ttu-id="82d40-796">Экранирована одинарная кавычка в значении параметра Get-AzADUser [11317].</span><span class="sxs-lookup"><span data-stu-id="82d40-796">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="82d40-797">Добавлены новые командлеты для сценариев развертывания (Get-AzDeploymentScript, Get-AzDeploymentScriptLog, Save-AzDeploymentScriptLog, Remove-AzDeploymentScript).</span><span class="sxs-lookup"><span data-stu-id="82d40-797">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="82d40-798">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82d40-798">Az.Sql</span></span>
* <span data-ttu-id="82d40-799">Добавлен параметр вторичной реплики для чтения для командлета Invoke-AzSqlDatabaseFailover.</span><span class="sxs-lookup"><span data-stu-id="82d40-799">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="82d40-800">Добавлен командлет Disable-AzSqlServerActiveDirectoryOnlyAuthentication.</span><span class="sxs-lookup"><span data-stu-id="82d40-800">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="82d40-801">Сохранен приоритет конфиденциальности при классификации столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="82d40-801">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="82d40-802">Az.Support</span><span class="sxs-lookup"><span data-stu-id="82d40-802">Az.Support</span></span>
* <span data-ttu-id="82d40-803">Модуль Az.Support стал общедоступным.</span><span class="sxs-lookup"><span data-stu-id="82d40-803">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="82d40-804">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="82d40-804">Az.Websites</span></span>
* <span data-ttu-id="82d40-805">Реализована поддержка работы с правилами маршрутизации трафика веб-приложения через указанные ниже командлеты</span><span class="sxs-lookup"><span data-stu-id="82d40-805">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="82d40-806">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="82d40-806">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="82d40-807">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="82d40-807">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="82d40-808">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="82d40-808">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="82d40-809">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="82d40-809">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="82d40-810">3.6.1 — март 2020 г.</span><span class="sxs-lookup"><span data-stu-id="82d40-810">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="82d40-811">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="82d40-811">Az.Accounts</span></span>
* <span data-ttu-id="82d40-812">Открытие страницы опроса Azure PowerShell в Send-Feedback [11020].</span><span class="sxs-lookup"><span data-stu-id="82d40-812">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="82d40-813">Отображение URL-адреса опроса Azure PowerShell в Resolve-Error [11021].</span><span class="sxs-lookup"><span data-stu-id="82d40-813">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="82d40-814">Добавлена версия Az в UserAgent.</span><span class="sxs-lookup"><span data-stu-id="82d40-814">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="82d40-815">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="82d40-815">Az.ApiManagement</span></span>
* <span data-ttu-id="82d40-816">Включена поддержка получения и настройки личного домена в конечной точке DeveloperPortal [11007].</span><span class="sxs-lookup"><span data-stu-id="82d40-816">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="82d40-817">Export-AzApiManagementApi: включена поддержка скачивания определения API в формате JSON [9987].</span><span class="sxs-lookup"><span data-stu-id="82d40-817">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="82d40-818">Import-AzApiManagementApi: включена поддержка импорта определения OpenApi 3.0 из документа JSON.</span><span class="sxs-lookup"><span data-stu-id="82d40-818">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="82d40-819">New-AzApiManagementIdentityProvider и Set-AzApiManagementIdentityProvider: включена поддержка настройки входа арендатора для поставщика AAD B2C [9784].</span><span class="sxs-lookup"><span data-stu-id="82d40-819">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="82d40-820">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="82d40-820">Az.DataLakeStore</span></span>
* <span data-ttu-id="82d40-821">Добавлена ссылка на System.Buffers явным образом в CSPROJ и PSD1.</span><span class="sxs-lookup"><span data-stu-id="82d40-821">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="82d40-822">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="82d40-822">Az.IotHub</span></span>
* <span data-ttu-id="82d40-823">Добавлена возможность управления устройствами в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="82d40-823">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="82d40-824">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="82d40-824">New Cmdlets are:</span></span>
    - <span data-ttu-id="82d40-825">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="82d40-825">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="82d40-826">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="82d40-826">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="82d40-827">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="82d40-827">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="82d40-828">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="82d40-828">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="82d40-829">Включена поддержка управления модулями в целевом устройстве Интернета вещей в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="82d40-829">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="82d40-830">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="82d40-830">New Cmdlets are:</span></span>
    - <span data-ttu-id="82d40-831">Add-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="82d40-831">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="82d40-832">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="82d40-832">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="82d40-833">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="82d40-833">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="82d40-834">Set-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="82d40-834">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="82d40-835">Добавлен командлет для получения строки подключения целевого устройства Интернета вещей в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="82d40-835">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="82d40-836">Добавлен командлет для получения строки подключения модуля на целевом устройстве Интернета вещей в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="82d40-836">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="82d40-837">Включена поддержка для получения или настройки родительского устройства для устройства Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="82d40-837">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="82d40-838">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="82d40-838">New Cmdlets are:</span></span>
    - <span data-ttu-id="82d40-839">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="82d40-839">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="82d40-840">Set-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="82d40-840">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="82d40-841">Включена поддержка управления связью "родители — потомки" устройства.</span><span class="sxs-lookup"><span data-stu-id="82d40-841">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="82d40-842">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="82d40-842">Az.Monitor</span></span>
* <span data-ttu-id="82d40-843">Исправлено выходное значение для Get-AzMetricDefinition [9714].</span><span class="sxs-lookup"><span data-stu-id="82d40-843">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82d40-844">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82d40-844">Az.Network</span></span>
* <span data-ttu-id="82d40-845">Обновлен пакет SDK для управления SQL.</span><span class="sxs-lookup"><span data-stu-id="82d40-845">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="82d40-846">Исправлена проблема с разницей в именовании в классе PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="82d40-846">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="82d40-847">Сопоставление ActionsRequired с ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="82d40-847">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="82d40-848">Добавление PublicNetworkAccess в команды New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="82d40-848">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="82d40-849">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82d40-849">Az.Resources</span></span>
* <span data-ttu-id="82d40-850">Исправлена ошибка пустой ссылки в Get-AzRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="82d40-850">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="82d40-851">Параметры -Force и -PassThru помечены необязательными в Remove-AzADGroup [10849].</span><span class="sxs-lookup"><span data-stu-id="82d40-851">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="82d40-852">Исправлена ошибка, из-за которой MailNickname не возвращается в Remove-AzADGroup [11167].</span><span class="sxs-lookup"><span data-stu-id="82d40-852">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="82d40-853">Исправлена ошибка, из-за которой операция канала Remove-AzADGroup не работает [11171].</span><span class="sxs-lookup"><span data-stu-id="82d40-853">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="82d40-854">Исправлена ошибка с пустой ссылкой в GetAzureRoleAssignmentCommand.</span><span class="sxs-lookup"><span data-stu-id="82d40-854">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="82d40-855">Добавлено критическое изменение атрибутов для будущих изменений командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="82d40-855">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="82d40-856">Обновлена команда Get-AzResourceGroup для выполнения фильтрации тегов группы ресурсов на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="82d40-856">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="82d40-857">Расширены командлеты Tag для включения поддержки параметра -ResourceId.</span><span class="sxs-lookup"><span data-stu-id="82d40-857">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="82d40-858">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="82d40-858">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="82d40-859">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="82d40-859">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="82d40-860">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="82d40-860">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="82d40-861">Добавлен новый командлет Tag.</span><span class="sxs-lookup"><span data-stu-id="82d40-861">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="82d40-862">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="82d40-862">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="82d40-863">Предоставляется ScopedDeployment из пакета SDK 3.3.0.</span><span class="sxs-lookup"><span data-stu-id="82d40-863">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="82d40-864">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82d40-864">Az.Sql</span></span>
* <span data-ttu-id="82d40-865">Добавление PublicNetworkAccess в команды New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="82d40-865">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="82d40-866">Включена поддержка конфигурации резервного копирования долгосрочного хранения для управляемых баз данных.</span><span class="sxs-lookup"><span data-stu-id="82d40-866">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="82d40-867">Получение или настройка политики LTR в управляемой базе данных.</span><span class="sxs-lookup"><span data-stu-id="82d40-867">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="82d40-868">Получение резервных копий LTR по управляемой базе данных, управляемому экземпляру или расположению.</span><span class="sxs-lookup"><span data-stu-id="82d40-868">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="82d40-869">Удаление резервной копии LTR.</span><span class="sxs-lookup"><span data-stu-id="82d40-869">Remove an LTR backup</span></span>
    - <span data-ttu-id="82d40-870">Восстановление резервной копии LTR для создания новой управляемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="82d40-870">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="82d40-871">Добавление MinimalTlsVersion в New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="82d40-871">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="82d40-872">Добавление MinimalTlsVersion в New-AzSqlInstance и Set-AzSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="82d40-872">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="82d40-873">Обновлена версия пакета SDK для SQL для Az.Network.</span><span class="sxs-lookup"><span data-stu-id="82d40-873">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="82d40-874">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="82d40-874">Az.Storage</span></span>
* <span data-ttu-id="82d40-875">Включена поддержка AllowProtectedAppendWrite в ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="82d40-875">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="82d40-876">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="82d40-876">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="82d40-877">Добавлено предупреждение о критическом изменении для изменения типа AzureStorageTable в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="82d40-877">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="82d40-878">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="82d40-878">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="82d40-879">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="82d40-879">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="82d40-880">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="82d40-880">Az.Websites</span></span>
* <span data-ttu-id="82d40-881">Добавлен параметр Tag для New-AzAppServicePlan и Set-AzAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="82d40-881">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="82d40-882">Завершение выполнения командлета, если при добавлении личного домена на веб-сайт возникает исключение.</span><span class="sxs-lookup"><span data-stu-id="82d40-882">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="82d40-883">Включена поддержка выполнения операций для Служб приложений, которые находятся не в той же группе ресурсов, что и план службы приложений.</span><span class="sxs-lookup"><span data-stu-id="82d40-883">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="82d40-884">Применение ограничения доступа к WebApp/Function в разных группах ресурсов.</span><span class="sxs-lookup"><span data-stu-id="82d40-884">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="82d40-885">Исправлена ошибка с указанием пользовательских имен узлов для WebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="82d40-885">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="82d40-886">3.5.0 — февраль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="82d40-886">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="82d40-887">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="82d40-887">Highlights since the last major release</span></span>
* <span data-ttu-id="82d40-888">Обновлены данные телеметрии на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="82d40-888">Updated client side telemetry.</span></span>
* <span data-ttu-id="82d40-889">В Az.IotHub добавлены командлеты для управления устройствами.</span><span class="sxs-lookup"><span data-stu-id="82d40-889">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="82d40-890">В Az.SqlVirtualMachine добавлены командлеты для прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="82d40-890">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="82d40-891">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="82d40-891">Az.Accounts</span></span>
* <span data-ttu-id="82d40-892">В данные телеметрии на стороне клиента добавлены такие сведения, как идентификатор подписки, идентификатор арендатора и время выполнения.</span><span class="sxs-lookup"><span data-stu-id="82d40-892">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="82d40-893">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="82d40-893">Az.Automation</span></span>
* <span data-ttu-id="82d40-894">Исправлена опечатка в примере 1 в справочной документации по New-AzAutomationSoftwareUpdateConfiguration.</span><span class="sxs-lookup"><span data-stu-id="82d40-894">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="82d40-895">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="82d40-895">Az.CognitiveServices</span></span>
* <span data-ttu-id="82d40-896">Обновлен пакет SDK до версии 7.0.</span><span class="sxs-lookup"><span data-stu-id="82d40-896">Updated SDK to 7.0</span></span>
* <span data-ttu-id="82d40-897">Улучшено сообщение об ошибке, которое появляется, если ответы сервера не содержат текст.</span><span class="sxs-lookup"><span data-stu-id="82d40-897">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82d40-898">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82d40-898">Az.Compute</span></span>
* <span data-ttu-id="82d40-899">Разрешено использовать пустое значение для ProximityPlacementGroupId во время обновления.</span><span class="sxs-lookup"><span data-stu-id="82d40-899">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="82d40-900">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="82d40-900">Az.FrontDoor</span></span>
* <span data-ttu-id="82d40-901">Добавлен командлет для получения определений управляемых правил, которые могут использоваться в WAF.</span><span class="sxs-lookup"><span data-stu-id="82d40-901">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="82d40-902">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="82d40-902">Az.IotHub</span></span>
* <span data-ttu-id="82d40-903">Добавлена возможность управления устройствами в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="82d40-903">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="82d40-904">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="82d40-904">New Cmdlets are:</span></span>
    - <span data-ttu-id="82d40-905">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="82d40-905">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="82d40-906">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="82d40-906">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="82d40-907">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="82d40-907">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="82d40-908">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="82d40-908">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="82d40-909">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="82d40-909">Az.KeyVault</span></span>
* <span data-ttu-id="82d40-910">Устранен дублирующийся текст для Add-AzKeyVaultKey.md.</span><span class="sxs-lookup"><span data-stu-id="82d40-910">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="82d40-911">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="82d40-911">Az.Monitor</span></span>
* <span data-ttu-id="82d40-912">Исправлено описание командлета Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="82d40-912">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="82d40-913">В команду New-AzMetricAlertRuleV2 добавлен новый параметр ActionGroupId.</span><span class="sxs-lookup"><span data-stu-id="82d40-913">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="82d40-914">Пользователь может предоставить ActionGroupId(string) или ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="82d40-914">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82d40-915">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82d40-915">Az.Network</span></span>
* <span data-ttu-id="82d40-916">Добавлен еще один параметр -EnableProxyProtocol для командлета New-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="82d40-916">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="82d40-917">Исправлен пример FilterData в Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="82d40-917">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="82d40-918">Добавлен пример Packet Capture для всех внутренних и внешних пакетов в Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="82d40-918">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="82d40-919">Добавлена поддерживаемая политика Брандмауэра Azure в брандмауэрах виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="82d40-919">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="82d40-920">Новые командлеты не добавлены.</span><span class="sxs-lookup"><span data-stu-id="82d40-920">No new cmdlets are added.</span></span> <span data-ttu-id="82d40-921">Снято ограничение политики брандмауэра в брандмауэрах виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="82d40-921">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="82d40-922">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="82d40-922">Az.RecoveryServices</span></span>
* <span data-ttu-id="82d40-923">Добавлена возможность восстановления в виде файлов для Баз данных SQL.</span><span class="sxs-lookup"><span data-stu-id="82d40-923">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="82d40-924">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82d40-924">Az.Resources</span></span>
* <span data-ttu-id="82d40-925">Выполнен рефакторинг командлетов развертывания шаблона.</span><span class="sxs-lookup"><span data-stu-id="82d40-925">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="82d40-926">Добавлены новые командлеты для управления развертываниями в группе управления: \*-AzManagementGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="82d40-926">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="82d40-927">Добавлены новые командлеты для управления развертываниями в области арендатора: \*-AzTenantDeployment.</span><span class="sxs-lookup"><span data-stu-id="82d40-927">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="82d40-928">Выполнен рефакторинг командлетов \*-AzDeployment для работы в области подписки.</span><span class="sxs-lookup"><span data-stu-id="82d40-928">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="82d40-929">Созданы псевдонимы \*-AzSubscriptionDeployment для командлетов \*-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="82d40-929">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="82d40-930">Исправлен командлет Update-AzADApplication, когда параметр AvailableToOtherTenants не задан.</span><span class="sxs-lookup"><span data-stu-id="82d40-930">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="82d40-931">Удален набор параметров ApplicationObjectWithoutCredentialParameterSet, чтобы предотвратить возникновение AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="82d40-931">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="82d40-932">Повторно созданы файлы справки.</span><span class="sxs-lookup"><span data-stu-id="82d40-932">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="82d40-933">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82d40-933">Az.Sql</span></span>
* <span data-ttu-id="82d40-934">Добавлена возможность восстановления точки во времени между подписками в Управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="82d40-934">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="82d40-935">Добавлена возможность изменения существующего поколения оборудования Управляемого экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="82d40-935">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="82d40-936">Исправлены примеры справки Update-AzSqlServerVulnerabilityAssessmentSetting: выходные данные параметра и свойства — EmailAdmins.</span><span class="sxs-lookup"><span data-stu-id="82d40-936">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="82d40-937">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="82d40-937">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="82d40-938">Добавлены командлеты для прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="82d40-938">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="82d40-939">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="82d40-939">Az.StorageSync</span></span>
* <span data-ttu-id="82d40-940">В командлете Invoke-AzStorageSyncCompatibilityCheck обновлены поддерживаемые наборы символов.</span><span class="sxs-lookup"><span data-stu-id="82d40-940">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="82d40-941">3.4.0 — февраль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="82d40-941">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="82d40-942">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="82d40-942">Highlights since the last major release</span></span>
* <span data-ttu-id="82d40-943">Выпущена первоначальная версия 0.1.0 Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="82d40-943">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="82d40-944">Добавлена поддержка Az.Network ConnectionMonitor V2</span><span class="sxs-lookup"><span data-stu-id="82d40-944">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="82d40-945">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="82d40-945">Az.Accounts</span></span>
* <span data-ttu-id="82d40-946">Отключить автоматическое сохранение контекста, если AzureRmContext.json недоступен</span><span class="sxs-lookup"><span data-stu-id="82d40-946">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="82d40-947">Обновление ссылки на Azure Powershell Common до предварительной версии 1.3.5</span><span class="sxs-lookup"><span data-stu-id="82d40-947">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="82d40-948">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="82d40-948">Az.ApiManagement</span></span>
* <span data-ttu-id="82d40-949">**Get-AzApiManagementApiSchema** Исправлено получение схемы Open-API, связанной с API https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="82d40-949">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="82d40-950">**New-AzApiManagementProduct**\* и **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="82d40-950">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="82d40-951">Исправить документацию для https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="82d40-951">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="82d40-952">**Set-AzApiManagementApi** Добавлен пример, показывающий, как обновить ServiceUrl с помощью командлета</span><span class="sxs-lookup"><span data-stu-id="82d40-952">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82d40-953">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82d40-953">Az.Compute</span></span>
* <span data-ttu-id="82d40-954">Ограничение числа состояний виртуальных машин до 100, чтобы избежать регулирования при выполнении Get-AzVM-Status без имени виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="82d40-954">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="82d40-955">Добавление обновления командлета -AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="82d40-955">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="82d40-956">Добавление параметров EncryptionType и DiskEncryptionSetId в следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="82d40-956">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="82d40-957">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="82d40-957">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="82d40-958">Добавление параметра ColocationStatus в командлет Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="82d40-958">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="82d40-959">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="82d40-959">Az.DataFactory</span></span>
* <span data-ttu-id="82d40-960">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.7.0.</span><span class="sxs-lookup"><span data-stu-id="82d40-960">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="82d40-961">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="82d40-961">Az.DeploymentManager</span></span>
* <span data-ttu-id="82d40-962">Добавляет операции LIST для ресурсов</span><span class="sxs-lookup"><span data-stu-id="82d40-962">Adds LIST operations for resources</span></span>
* <span data-ttu-id="82d40-963">Добавляет возможность выполнения операций на этапах Проверки работоспособности</span><span class="sxs-lookup"><span data-stu-id="82d40-963">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="82d40-964">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="82d40-964">Az.HDInsight</span></span>
* <span data-ttu-id="82d40-965">Исправление ошибки в документе New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="82d40-965">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="82d40-966">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="82d40-966">Az.KeyVault</span></span>
* <span data-ttu-id="82d40-967">Добавление Псевдонимов имени в атрибут VaultName, чтобы Remove-AzureKeyVault соответствовал New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="82d40-967">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82d40-968">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82d40-968">Az.Network</span></span>
* <span data-ttu-id="82d40-969">В Set-AzNetworkWatcherConfigFlowLog.md добавлен новый пример для демонстрации сценария отключения Аналитики трафика.</span><span class="sxs-lookup"><span data-stu-id="82d40-969">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="82d40-970">Добавление поддержки назначения IP-конфигурации для брандмауэра Azure — выделенная подсеть и общедоступный IP-адрес, которые брандмауэр будет использовать для управления трафиком</span><span class="sxs-lookup"><span data-stu-id="82d40-970">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="82d40-971">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="82d40-971">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="82d40-972">добавлен параметр — ManagementPublicIpAddress (необязательный), который принимает объект общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="82d40-972">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="82d40-973">Добавлен метод SetManagementIpConfiguration для объекта брандмауэра — в качестве входных данных требуется подсеть и общедоступный IP-адрес — имя подсети должно быть "AzureFirewallManagementSubnet"</span><span class="sxs-lookup"><span data-stu-id="82d40-973">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="82d40-974">Исправлены примеры Get-AzNetworkSecurityGroup для отображения примеров для группы безопасности сети (NSG) вместо сетевых интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="82d40-974">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="82d40-975">Исправлена опечатка в команде New-AzVpnSite, которая препятствовала завершению параметра идентификатором ресурса.</span><span class="sxs-lookup"><span data-stu-id="82d40-975">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="82d40-976">Добавлена поддержка конфигурации в наборе действий для правил подстановки URL-адресов в шлюзе приложения.</span><span class="sxs-lookup"><span data-stu-id="82d40-976">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="82d40-977">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="82d40-977">New cmdlets added:</span></span>
        - <span data-ttu-id="82d40-978">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="82d40-978">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="82d40-979">В следующие командлеты добавлен необязательный параметр — UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="82d40-979">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="82d40-980">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="82d40-980">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="82d40-981">Добавление поддержки для ресурсов NetworkWatcher ConnectionMonitor версии 2</span><span class="sxs-lookup"><span data-stu-id="82d40-981">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="82d40-982">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="82d40-982">Az.PolicyInsights</span></span>
* <span data-ttu-id="82d40-983">Поддержка оценки соответствия до определения того, какой ресурс нужно исправить</span><span class="sxs-lookup"><span data-stu-id="82d40-983">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="82d40-984">Добавление параметра "—ResourceDiscoverMode" в Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="82d40-984">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="82d40-985">Добавление командлета Get-AzPolicyMetadata для получения ресурсов метаданных политики</span><span class="sxs-lookup"><span data-stu-id="82d40-985">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="82d40-986">Get-AzPolicyState и Get-AzPolicyStateSummary обновлены для API версии 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="82d40-986">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="82d40-987">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="82d40-987">Az.RecoveryServices</span></span>
* <span data-ttu-id="82d40-988">Поддержка Azure Site Recovery для удаления реплицированного диска.</span><span class="sxs-lookup"><span data-stu-id="82d40-988">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="82d40-989">В Azure Backup добавлена ​​поддержка добавления тегов при создании Хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="82d40-989">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="82d40-990">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82d40-990">Az.Resources</span></span>
* <span data-ttu-id="82d40-991">Сделайте команду "Область" необязательной в командлетах \*—AzPolicyAssignment с настройкой по умолчанию для контекстной подписки</span><span class="sxs-lookup"><span data-stu-id="82d40-991">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="82d40-992">Добавление примеров создания ADServicePrincipal с паролем и ключом учетных данных</span><span class="sxs-lookup"><span data-stu-id="82d40-992">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="82d40-993">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82d40-993">Az.Sql</span></span>
<span data-ttu-id="82d40-994">Исправление командлета New-AzSqlDatabaseSecondary, чтобы проверить существование PartnerDatabaseName, а не DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="82d40-994">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="82d40-995">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="82d40-995">Az.Storage</span></span>
* <span data-ttu-id="82d40-996">Поддержка набора шифрования типа ключа таблиц и очередей в создании учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="82d40-996">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="82d40-997">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="82d40-997">New-AzStorageAccount</span></span>
* <span data-ttu-id="82d40-998">Представление RequestId, если StorageException не имеет ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="82d40-998">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="82d40-999">Исправление примера 6 командлета Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="82d40-999">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="82d40-1000">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="82d40-1000">Az.Websites</span></span>
* <span data-ttu-id="82d40-1001">Set-AzWebapp и Set-AzWebappSlot поддерживают свойства AlwaysOn, MinTls и FtpsState</span><span class="sxs-lookup"><span data-stu-id="82d40-1001">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="82d40-1002">Устранение проблемы, при которой параметр HttpsOnly с одновременным изменением AppservicePlan с помощью одной команды Set-AzWebApp сбрасывал значение HttpsOnly до значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="82d40-1002">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="82d40-1003">3.3.0 — январь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="82d40-1003">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="82d40-1004">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="82d40-1004">Az.Accounts</span></span>
* <span data-ttu-id="82d40-1005">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment: теперь они принимают параметры AzureAttestationServiceEndpointResourceId и AzureAttestationServiceEndpointSuffix.</span><span class="sxs-lookup"><span data-stu-id="82d40-1005">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="82d40-1006">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="82d40-1006">Az.Cdn</span></span>
* <span data-ttu-id="82d40-1007">Теперь в командлете New-AzCdnEndpoint отображаются сведения из сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="82d40-1007">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82d40-1008">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82d40-1008">Az.Compute</span></span>
* <span data-ttu-id="82d40-1009">Командлет Set-AzVMCustomScriptExtension исправлен для виртуальной машины с управляемым диском ОС без профиля ОС.</span><span class="sxs-lookup"><span data-stu-id="82d40-1009">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="82d40-1010">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="82d40-1010">Az.ContainerInstance</span></span>
* <span data-ttu-id="82d40-1011">Исправлены имена параметров, используемые в примере командлета New-AzContainerGroup.</span><span class="sxs-lookup"><span data-stu-id="82d40-1011">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="82d40-1012">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="82d40-1012">Az.DataBoxEdge</span></span>
* <span data-ttu-id="82d40-1013">Добавлен командлет Get-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="82d40-1013">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="82d40-1014">получение контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="82d40-1014">Get the Edge Storage Container</span></span>
* <span data-ttu-id="82d40-1015">Добавлен командлет New-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="82d40-1015">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="82d40-1016">создание контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="82d40-1016">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="82d40-1017">Добавлен командлет Remove-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="82d40-1017">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="82d40-1018">удаление контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="82d40-1018">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="82d40-1019">Добавлен командлет Invoke-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="82d40-1019">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="82d40-1020">вызов действия для обновления данных в контейнере хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="82d40-1020">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="82d40-1021">Добавлен командлет Get-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="82d40-1021">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="82d40-1022">получение учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="82d40-1022">Get the Edge Storage Account</span></span>
* <span data-ttu-id="82d40-1023">Добавлен командлет New-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="82d40-1023">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="82d40-1024">создание учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="82d40-1024">Create new Edge Storage Account</span></span>
* <span data-ttu-id="82d40-1025">Добавлен командлет Remove-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="82d40-1025">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="82d40-1026">удаление учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="82d40-1026">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="82d40-1027">Вызов командлета Invoke-AzDataBoxEdgeShare:</span><span class="sxs-lookup"><span data-stu-id="82d40-1027">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="82d40-1028">вызов действия для обновления данных в общей папке.</span><span class="sxs-lookup"><span data-stu-id="82d40-1028">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="82d40-1029">Добавлен командлет Set-AzDataBoxEdgeStorageAccountCredential:</span><span class="sxs-lookup"><span data-stu-id="82d40-1029">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="82d40-1030">установка учетных данных для учетной записи хранилища Azure Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="82d40-1030">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="82d40-1031">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="82d40-1031">Az.DataFactory</span></span>
* <span data-ttu-id="82d40-1032">Добавлены свойства AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId и VersionStatus для командлета Get-AzDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="82d40-1032">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="82d40-1033">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.6.0.</span><span class="sxs-lookup"><span data-stu-id="82d40-1033">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="82d40-1034">Для командлета Set-AzureRmDataFactoryV2IntegrationRuntime добавлен параметр PublicIPs, позволяющий включить создание среды Azure-SSIS IR со статическими общедоступными IP-адресами.</span><span class="sxs-lookup"><span data-stu-id="82d40-1034">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="82d40-1035">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="82d40-1035">Az.DevTestLabs</span></span>
* <span data-ttu-id="82d40-1036">Удалена недействительная ссылка в файле Get-AzDtlAllowedVMSizesPolicy.md.</span><span class="sxs-lookup"><span data-stu-id="82d40-1036">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="82d40-1037">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="82d40-1037">Az.EventHub</span></span>
* <span data-ttu-id="82d40-1038">Устранена проблема № 10634: исправлена ссылка на пустой объект для удаления пространства имен концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="82d40-1038">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="82d40-1039">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="82d40-1039">Az.HDInsight</span></span>
* <span data-ttu-id="82d40-1040">Устранена ошибка в файле Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="82d40-1040">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="82d40-1041">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="82d40-1041">Az.MachineLearning</span></span>
* <span data-ttu-id="82d40-1042">Вычислительная среда Машинного обучения больше недоступна, поэтому удалены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="82d40-1042">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="82d40-1043">Get-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="82d40-1043">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="82d40-1044">Get-AzMlOpClusterKey;</span><span class="sxs-lookup"><span data-stu-id="82d40-1044">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="82d40-1045">New-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="82d40-1045">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="82d40-1046">Remove-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="82d40-1046">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="82d40-1047">Set-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="82d40-1047">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="82d40-1048">Test-AzMlOpClusterSystemServicesUpdateAvailability;</span><span class="sxs-lookup"><span data-stu-id="82d40-1048">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="82d40-1049">Update-AzMlOpClusterSystemService.</span><span class="sxs-lookup"><span data-stu-id="82d40-1049">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82d40-1050">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82d40-1050">Az.Network</span></span>
* <span data-ttu-id="82d40-1051">Обновлена зависимость Microsoft.Azure.Management.Sql от предварительной версии 1.36 до предварительной версии 1.37.</span><span class="sxs-lookup"><span data-stu-id="82d40-1051">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="82d40-1052">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="82d40-1052">Az.RecoveryServices</span></span>
* <span data-ttu-id="82d40-1053">Добавлена поддержка Azure Site Recovery для виртуальных машин с управляемым диском, зашифрованных при хранении с помощью управляемых клиентом ключей, при восстановлении из Azure в поставщике Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-1053">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="82d40-1054">Добавлена поддержка Azure Site Recovery для необязательного ввода идентификатора набора шифрования диска при включении защиты в рамках восстановления из VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-1054">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="82d40-1055">Добавлена поддержка Azure Site Recovery для необязательного ввода идентификатора набора шифрования диска на уровне диска при включении защиты в рамках восстановления из VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-1055">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="82d40-1056">Добавлена поддержка Azure Site Recovery для обновления элемента, защищенного репликацией, путем сопоставления набора шифрования диска при восстановлении из HyperV в Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-1056">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="82d40-1057">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82d40-1057">Az.Resources</span></span>
* <span data-ttu-id="82d40-1058">Исправлена ошибка в справочном документе о командлете Remove-AzTag.</span><span class="sxs-lookup"><span data-stu-id="82d40-1058">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="82d40-1059">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82d40-1059">Az.Sql</span></span>
* <span data-ttu-id="82d40-1060">Исправлена функция основных командлетов установки оценки уязвимостей: теперь она позволяет работать с базой данных master для базы данных Azure и ограничить ее в системных базах данных управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="82d40-1060">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="82d40-1061">Устранена ошибка, возникающая при создании группы отработки отказа экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="82d40-1061">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="82d40-1062">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="82d40-1062">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="82d40-1063">Добавлен новый допустимый тип лицензии: DR (аварийное восстановление).</span><span class="sxs-lookup"><span data-stu-id="82d40-1063">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="82d40-1064">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="82d40-1064">Az.Storage</span></span>
* <span data-ttu-id="82d40-1065">Добавлено предупреждающее сообщение о критическом изменении значения DefaultAction в следующем выпуске:</span><span class="sxs-lookup"><span data-stu-id="82d40-1065">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="82d40-1066">Update-AzStorageAccountNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="82d40-1066">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="82d40-1067">Включена поддержка получения времени последней синхронизации учетной записи хранения путем выполнения командлета Get-AzureRmStorageAccount с параметром -IncludeGeoReplicationStats:</span><span class="sxs-lookup"><span data-stu-id="82d40-1067">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="82d40-1068">Get-AzureRmStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="82d40-1068">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="82d40-1069">3.2.0 — декабрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="82d40-1069">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="82d40-1070">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="82d40-1070">General</span></span>
* <span data-ttu-id="82d40-1071">Обновление ссылок в .psd1 для использования относительного пути для всех модулей.</span><span class="sxs-lookup"><span data-stu-id="82d40-1071">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="82d40-1072">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="82d40-1072">Az.Accounts</span></span>
* <span data-ttu-id="82d40-1073">Установка правильного параметра UserAgent для телеметрии на стороне клиента для Az 4.0 (предварительная версия).</span><span class="sxs-lookup"><span data-stu-id="82d40-1073">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="82d40-1074">Отображение понятного пользователю сообщения об ошибке, если в Az 4.0 (предварительная версия) не указан контекст.</span><span class="sxs-lookup"><span data-stu-id="82d40-1074">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="82d40-1075">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="82d40-1075">Az.Batch</span></span>
* <span data-ttu-id="82d40-1076">Исправлена проблема [№ 10602](https://github.com/Azure/azure-powershell/issues/10602), из-за которой использование командлета **New-AzBatchPool** приводило к неправильной отправке VirtualMachineConfiguration.ContainerConfiguration или VirtualMachineConfiguration.DataDisks на сервер.</span><span class="sxs-lookup"><span data-stu-id="82d40-1076">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="82d40-1077">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="82d40-1077">Az.DataFactory</span></span>
* <span data-ttu-id="82d40-1078">Обновление пакета SDK Фабрики данных для .NET до версии 4.5.0.</span><span class="sxs-lookup"><span data-stu-id="82d40-1078">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="82d40-1079">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="82d40-1079">Az.FrontDoor</span></span>
* <span data-ttu-id="82d40-1080">Включена поддержка исключений управляемых правил WAF.</span><span class="sxs-lookup"><span data-stu-id="82d40-1080">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="82d40-1081">Добавление SocketAddr в список автозавершения.</span><span class="sxs-lookup"><span data-stu-id="82d40-1081">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="82d40-1082">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="82d40-1082">Az.HealthcareApis</span></span>
* <span data-ttu-id="82d40-1083">Обработка исключений.</span><span class="sxs-lookup"><span data-stu-id="82d40-1083">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="82d40-1084">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="82d40-1084">Az.KeyVault</span></span>
* <span data-ttu-id="82d40-1085">Исправлена ошибка при получении доступа к значению, которое может быть не задано.</span><span class="sxs-lookup"><span data-stu-id="82d40-1085">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="82d40-1086">Управление сертификатами шифрования на основе эллиптических кривых.</span><span class="sxs-lookup"><span data-stu-id="82d40-1086">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="82d40-1087">Включена возможность указания кривой для политик сертификатов.</span><span class="sxs-lookup"><span data-stu-id="82d40-1087">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="82d40-1088">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="82d40-1088">Az.Monitor</span></span>
* <span data-ttu-id="82d40-1089">Добавление необязательного аргумента в команду добавления параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="82d40-1089">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="82d40-1090">Существующий аргумент switch указывает на то, что экспорт в Log Analytics должен выполняться в фиксированную схему</span><span class="sxs-lookup"><span data-stu-id="82d40-1090">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="82d40-1091">(выделенный тип данных).</span><span class="sxs-lookup"><span data-stu-id="82d40-1091">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82d40-1092">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82d40-1092">Az.Network</span></span>
* <span data-ttu-id="82d40-1093">В приложении AzureFirewall, NAT и сетевых правилах включена поддержка IpGroups.</span><span class="sxs-lookup"><span data-stu-id="82d40-1093">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="82d40-1094">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82d40-1094">Az.Resources</span></span>
* <span data-ttu-id="82d40-1095">Устранена проблема, из-за которой при развертывании шаблона не удавалось считать его параметр, если имя параметра конфликтовало с именем встроенного параметра.</span><span class="sxs-lookup"><span data-stu-id="82d40-1095">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="82d40-1096">Обновлены командлеты политики для использования новой версии API 2019-09-01 с поддержкой группирования в определениях наборов политик.</span><span class="sxs-lookup"><span data-stu-id="82d40-1096">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="82d40-1097">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82d40-1097">Az.Sql</span></span>
* <span data-ttu-id="82d40-1098">Обновлена функция автоматического создания расширенного хранилища для службы оценки уязвимостей в учетной записи StorageV2.</span><span class="sxs-lookup"><span data-stu-id="82d40-1098">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="82d40-1099">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="82d40-1099">Az.Storage</span></span>
* <span data-ttu-id="82d40-1100">Включена поддержка создания маркера SAS на основе удостоверения контейнера и большого двоичного объекта с аутентификацией Oauth на основе контекста службы хранилища:</span><span class="sxs-lookup"><span data-stu-id="82d40-1100">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="82d40-1101">New-AzStorageContainerSASToken;</span><span class="sxs-lookup"><span data-stu-id="82d40-1101">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="82d40-1102">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="82d40-1102">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="82d40-1103">Отозвана поддержка ключей делегирования пользователя учетной записи хранения, а также всех маркеров SAS удостоверения:</span><span class="sxs-lookup"><span data-stu-id="82d40-1103">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="82d40-1104">Revoke-AzStorageAccountUserDelegationKeys.</span><span class="sxs-lookup"><span data-stu-id="82d40-1104">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="82d40-1105">Выполнено обновление до Microsoft.Azure.Management.Storage версии 14.2.0 для включения поддержки нового API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="82d40-1105">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="82d40-1106">Включена поддержка QuotaGiB (квота общего ресурса в ГиБ) для значений свыше 5120 в командлетах для работы с общими папками в плоскости управления и добавлен псевдоним Quota для параметра QuotaGiB.</span><span class="sxs-lookup"><span data-stu-id="82d40-1106">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="82d40-1107">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="82d40-1107">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="82d40-1108">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="82d40-1108">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="82d40-1109">Добавлен псевдоним QuotaGiB для параметра Quota:</span><span class="sxs-lookup"><span data-stu-id="82d40-1109">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="82d40-1110">Set-AzStorageShareQuota.</span><span class="sxs-lookup"><span data-stu-id="82d40-1110">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="82d40-1111">Устранена проблема, из-за которой при использовании AzStorageContainerAcl могла очищаться хранимая политика доступа:</span><span class="sxs-lookup"><span data-stu-id="82d40-1111">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="82d40-1112">Set-AzStorageContainerAcl.</span><span class="sxs-lookup"><span data-stu-id="82d40-1112">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="82d40-1113">Версия 3.1.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="82d40-1113">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="82d40-1114">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="82d40-1114">Highlights since the last major release</span></span>
* <span data-ttu-id="82d40-1115">Выпуск Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="82d40-1115">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="82d40-1116">Выпуск Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="82d40-1116">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82d40-1117">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82d40-1117">Az.Compute</span></span>
* <span data-ttu-id="82d40-1118">Функция повторного применения виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="82d40-1118">VM Reapply feature</span></span>
    - <span data-ttu-id="82d40-1119">Добавлен параметр повторного применения в командлет Set-AzVM.</span><span class="sxs-lookup"><span data-stu-id="82d40-1119">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="82d40-1120">Функция AutomaticRepairs масштабируемого набора виртуальных машин:</span><span class="sxs-lookup"><span data-stu-id="82d40-1120">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="82d40-1121">Добавлены параметры EnableAutomaticRepair, AutomaticRepairGracePeriod и AutomaticRepairMaxInstanceRepairsPercent в следующие командлеты:   New-AzVmssConfig Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="82d40-1121">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="82d40-1122">Включена поддержка образа из коллекции разных клиентов для New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="82d40-1122">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="82d40-1123">Добавлен фрагмент Spot в средство заполнения аргументов параметра Priority в командлетах New-AzVM, New-AzVMConfig и New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="82d40-1123">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="82d40-1124">Добавлены параметры DiskIOPSReadWrite и DiskMBpsReadWrite в командлет Add-AzVmssDataDisk.</span><span class="sxs-lookup"><span data-stu-id="82d40-1124">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="82d40-1125">Изменен параметр SourceImageId командлета New-AzGalleryImageVersion на необязательный.</span><span class="sxs-lookup"><span data-stu-id="82d40-1125">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="82d40-1126">Добавлены параметры OSDiskImage и DataDiskImage в командлет New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="82d40-1126">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="82d40-1127">Добавлен параметр HyperVGeneration в командлет New-AzGalleryImageDefinition.</span><span class="sxs-lookup"><span data-stu-id="82d40-1127">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="82d40-1128">Добавлены параметры SkipExtensionsOnOverprovisionedVMs в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="82d40-1128">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="82d40-1129">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="82d40-1129">Az.DataBoxEdge</span></span>
* <span data-ttu-id="82d40-1130">Добавлен командлет `Get-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="82d40-1130">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="82d40-1131">Получение заказа.</span><span class="sxs-lookup"><span data-stu-id="82d40-1131">Get the Order</span></span>
* <span data-ttu-id="82d40-1132">Добавлен командлет `New-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="82d40-1132">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="82d40-1133">Создание заказа.</span><span class="sxs-lookup"><span data-stu-id="82d40-1133">Create new Order</span></span>
* <span data-ttu-id="82d40-1134">Добавлен командлет `Remove-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="82d40-1134">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="82d40-1135">Удаление заказа.</span><span class="sxs-lookup"><span data-stu-id="82d40-1135">Remove the Order</span></span>
* <span data-ttu-id="82d40-1136">Изменен командлет `New-AzDataBoxEdgeShare`.</span><span class="sxs-lookup"><span data-stu-id="82d40-1136">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="82d40-1137">Создание локальной общей папки.</span><span class="sxs-lookup"><span data-stu-id="82d40-1137">Now creates Local Share</span></span>
* <span data-ttu-id="82d40-1138">Добавлен командлет `Set-AzDataBoxEdgeRole`.</span><span class="sxs-lookup"><span data-stu-id="82d40-1138">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="82d40-1139">Сопоставление IotRole с общей папкой.</span><span class="sxs-lookup"><span data-stu-id="82d40-1139">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="82d40-1140">Добавлен командлет `Invoke-AzDataBoxEdgeDevice`.</span><span class="sxs-lookup"><span data-stu-id="82d40-1140">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="82d40-1141">Вызов проверки обновлений, скачивание обновления, установка обновления на устройстве.</span><span class="sxs-lookup"><span data-stu-id="82d40-1141">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="82d40-1142">Добавлен командлет `Get-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="82d40-1142">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="82d40-1143">Получение сведений о триггерах.</span><span class="sxs-lookup"><span data-stu-id="82d40-1143">Gets the information about Triggers</span></span>
* <span data-ttu-id="82d40-1144">Добавлен командлет `New-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="82d40-1144">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="82d40-1145">Создание триггеров.</span><span class="sxs-lookup"><span data-stu-id="82d40-1145">Create new Triggers</span></span>
* <span data-ttu-id="82d40-1146">Добавлен командлет `Remove-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="82d40-1146">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="82d40-1147">Удаление триггеров.</span><span class="sxs-lookup"><span data-stu-id="82d40-1147">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="82d40-1148">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="82d40-1148">Az.DataFactory</span></span>
* <span data-ttu-id="82d40-1149">Обновление пакета SDK Фабрики данных для .NET до версии 4.4.0.</span><span class="sxs-lookup"><span data-stu-id="82d40-1149">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="82d40-1150">Добавлен параметр ExpressCustomSetup в командлет Set-AzureRmDataFactoryV2IntegrationRuntime для включения конфигураций установки и сторонних компонентов без использования настраиваемого скрипта установки.</span><span class="sxs-lookup"><span data-stu-id="82d40-1150">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="82d40-1151">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="82d40-1151">Az.DataLakeStore</span></span>
* <span data-ttu-id="82d40-1152">Обновлена документация по Get-AzDataLakeStoreDeletedItem и Restore-AzDataLakeStoreDeletedItem.</span><span class="sxs-lookup"><span data-stu-id="82d40-1152">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="82d40-1153">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="82d40-1153">Az.EventHub</span></span>
* <span data-ttu-id="82d40-1154">Исправлена проблема № 10301. Исправлен формат даты маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="82d40-1154">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="82d40-1155">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="82d40-1155">Az.FrontDoor</span></span>
* <span data-ttu-id="82d40-1156">Добавлен параметр MinimumTlsVersion в Enable-AzFrontDoorCustomDomainHttps и New-AzFrontDoorFrontendEndpointObject.</span><span class="sxs-lookup"><span data-stu-id="82d40-1156">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="82d40-1157">Добавлены параметры HealthProbeMethod и EnabledState в New-AzFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="82d40-1157">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="82d40-1158">Добавлен новый командлет для создания объекта BackendPoolsSettings для передачи при создании и обновлении Front Door.</span><span class="sxs-lookup"><span data-stu-id="82d40-1158">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="82d40-1159">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="82d40-1159">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82d40-1160">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82d40-1160">Az.Network</span></span>
* <span data-ttu-id="82d40-1161">Изменены примеры параметра FilterData Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="82d40-1161">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="82d40-1162">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="82d40-1162">Az.PrivateDns</span></span>
* <span data-ttu-id="82d40-1163">Пакет SDK PrivateDns для .NET обновлен до версии 1.0.0</span><span class="sxs-lookup"><span data-stu-id="82d40-1163">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="82d40-1164">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="82d40-1164">Az.RecoveryServices</span></span>
* <span data-ttu-id="82d40-1165">Включена поддержка Azure Site Recovery для выбора типа диска при включении защиты.</span><span class="sxs-lookup"><span data-stu-id="82d40-1165">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="82d40-1166">Внесено исправление Azure Site Recovery для изменения действия плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="82d40-1166">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="82d40-1167">Включена поддержка восстановления SQL Azure Backup для принятия баз данных файлового потока.</span><span class="sxs-lookup"><span data-stu-id="82d40-1167">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="82d40-1168">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="82d40-1168">Az.RedisCache</span></span>
* <span data-ttu-id="82d40-1169">Добавлен параметр MinimumTlsVersion в командлеты New-AzRedisCache и Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="82d40-1169">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="82d40-1170">Кроме того, добавлен параметр MinimumTlsVersion в выходные данные командлета Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="82d40-1170">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="82d40-1171">Добавлена проверка параметра -Size для командлетов Set-AzRedisCache и New-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="82d40-1171">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="82d40-1172">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82d40-1172">Az.Resources</span></span>
- <span data-ttu-id="82d40-1173">Обновлены командлеты политики для использования новой версии API 2019-06-01 с новым свойством EnforcementMode в назначении политики.</span><span class="sxs-lookup"><span data-stu-id="82d40-1173">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="82d40-1174">Обновлен пример справки по созданию определения политики</span><span class="sxs-lookup"><span data-stu-id="82d40-1174">Updated create policy definition help example</span></span>
- <span data-ttu-id="82d40-1175">Исправлена ошибка с параметром -ServicePrincipalName командлета Remove-AZADServicePrincipal с возвратом пустой ссылки, если имя субъекта службы не найдено.</span><span class="sxs-lookup"><span data-stu-id="82d40-1175">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="82d40-1176">Исправлена ошибка с New-AZADServicePrincipal с возвратом пустой ссылки, если у клиента нет подписки.</span><span class="sxs-lookup"><span data-stu-id="82d40-1176">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="82d40-1177">Изменен командлет New-AzAdServicePrincipal для добавления учетных данных только для связанного приложения.</span><span class="sxs-lookup"><span data-stu-id="82d40-1177">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="82d40-1178">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82d40-1178">Az.Sql</span></span>
* <span data-ttu-id="82d40-1179">Добавлена поддержка ReadReplicaCount для базы данных.</span><span class="sxs-lookup"><span data-stu-id="82d40-1179">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="82d40-1180">Исправлена ошибка с Set-AzSqlDatabase, если избыточность в пределах зоны не настроена.</span><span class="sxs-lookup"><span data-stu-id="82d40-1180">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="82d40-1181">Версия 3.0.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="82d40-1181">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="82d40-1182">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="82d40-1182">General</span></span>
* <span data-ttu-id="82d40-1183">Выпущена версия Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="82d40-1183">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="82d40-1184">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="82d40-1184">Az.Accounts</span></span>
* <span data-ttu-id="82d40-1185">Добавлено сообщение об устаревании для псевдонима "Resolve-Error".</span><span class="sxs-lookup"><span data-stu-id="82d40-1185">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="82d40-1186">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="82d40-1186">Az.Advisor</span></span>
* <span data-ttu-id="82d40-1187">Добавлена новая категория Operational Excellence (Эффективность работы) в командлет Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="82d40-1187">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="82d40-1188">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="82d40-1188">Az.Batch</span></span>
* <span data-ttu-id="82d40-1189">`CoreQuota` в `BatchAccountContext` переименован в `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="82d40-1189">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="82d40-1190">Также появился новый `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="82d40-1190">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="82d40-1191">Это влияет на **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="82d40-1191">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="82d40-1192">Параметр **New-AzBatchTask** `-ResourceFile` теперь принимает коллекцию объектов `PSResourceFile`, которые можно создать с помощью нового командлета **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="82d40-1192">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="82d40-1193">Новый командлет **New-AzBatchResourceFile**, который помогает создавать объекты `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="82d40-1193">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="82d40-1194">Их можно передавать в **New-AzBatchTask** в параметре `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="82d40-1194">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="82d40-1195">Это позволяет поддерживать два новых типа файлов ресурсов, которые дополняют существующий метод `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="82d40-1195">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="82d40-1196">Файлы ресурсов на основе `AutoStorageContainerName` скачивают весь контейнер автоматического хранения в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="82d40-1196">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="82d40-1197">Файлы ресурсов на основе `StorageContainerUrl` скачивают указанный в URL-адресе контейнер в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="82d40-1197">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="82d40-1198">Удалено свойство `ApplicationPackages` в `PSApplication`, который возвращается из **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="82d40-1198">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="82d40-1199">Отдельные пакеты в приложении теперь можно извлечь с помощью **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="82d40-1199">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="82d40-1200">Например: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="82d40-1200">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="82d40-1201">`ApplicationId` переименован в `ApplicationName` для **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** и **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="82d40-1201">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="82d40-1202">Теперь `ApplicationId` является псевдонимом для `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="82d40-1202">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="82d40-1203">Добавлено новое свойство `PSWindowsUserConfiguration` в `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="82d40-1203">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="82d40-1204">`Version` переименован в `Name` для `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="82d40-1204">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="82d40-1205">`BlobSource` переименован в `HttpUrl` для `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="82d40-1205">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="82d40-1206">Удалено свойство `OSDisk` из `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="82d40-1206">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="82d40-1207">Удалена операция **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="82d40-1207">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="82d40-1208">Больше она не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="82d40-1208">This operation is no longer supported.</span></span>
* <span data-ttu-id="82d40-1209">Удалено `TargetOSVersion` из `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="82d40-1209">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="82d40-1210">`CurrentOSVersion` переименован в `OSVersion` для `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="82d40-1210">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="82d40-1211">Удалено `DataEgressGiB` и `DataIngressGiB` из `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="82d40-1211">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="82d40-1212">Операция **Get-AzBatchNodeAgentSku** удалена и заменена на **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="82d40-1212">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="82d40-1213">**Get-AzBatchSupportedImage** возвращает те же данные, что и **Get-AzBatchNodeAgentSku**, но в более удобном формате.</span><span class="sxs-lookup"><span data-stu-id="82d40-1213">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="82d40-1214">Также возвращаются новые непроверенные образы.</span><span class="sxs-lookup"><span data-stu-id="82d40-1214">New non-verified images are also now returned.</span></span> <span data-ttu-id="82d40-1215">Включается и дополнительная информация о `Capabilities` и `BatchSupportEndOfLife` для каждого образа.</span><span class="sxs-lookup"><span data-stu-id="82d40-1215">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="82d40-1216">Добавлена возможность монтировать файловые системы на каждом узле пула с помощью нового параметра `MountConfiguration` в **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="82d40-1216">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="82d40-1217">Теперь поддерживаются правила безопасности сети, которые блокируют сетевой доступ к пулу по исходящему порту трафика.</span><span class="sxs-lookup"><span data-stu-id="82d40-1217">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="82d40-1218">Это выполняется с помощью свойства `SourcePortRanges` для `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="82d40-1218">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="82d40-1219">Что касается выполнения контейнеров, пакетная служба теперь поддерживает выполнение задачи в рабочей папке контейнера или рабочей папке задачи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="82d40-1219">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="82d40-1220">Выбор зависит от параметра `WorkingDirectory` в `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="82d40-1220">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="82d40-1221">Добавлена возможность указать коллекцию общедоступных IP-адресов для `PSNetworkConfiguration` с помощью нового свойства `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="82d40-1221">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="82d40-1222">Это гарантирует, что узлы в пуле будут иметь IP-адреса из списка, предоставленного пользователем.</span><span class="sxs-lookup"><span data-stu-id="82d40-1222">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="82d40-1223">Если значение не задано, по умолчанию для `WaitForSuccess` в `PSSTartTask` используется значение `$True` (ранее `$False`).</span><span class="sxs-lookup"><span data-stu-id="82d40-1223">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="82d40-1224">Если значение не задано, по умолчанию для `Scope` в `PSAutoUserSpecification` используется значение `Pool` (ранее `Task` для Windows или `Pool` для Linux).</span><span class="sxs-lookup"><span data-stu-id="82d40-1224">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="82d40-1225">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="82d40-1225">Az.Cdn</span></span>
* <span data-ttu-id="82d40-1226">Добавлены UrlRewriteAction и CacheKeyQueryStringAction в RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="82d40-1226">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="82d40-1227">Исправлено несколько ошибок, таких как отсутствующий входной параметр Selector в командлете New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="82d40-1227">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82d40-1228">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82d40-1228">Az.Compute</span></span>
* <span data-ttu-id="82d40-1229">Функция набора шифрования диска</span><span class="sxs-lookup"><span data-stu-id="82d40-1229">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="82d40-1230">Новые командлеты:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="82d40-1230">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="82d40-1231">Добавлен параметр ProximityPlacementGroupId в следующие командлеты:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="82d40-1231">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="82d40-1232">Параметры DiskEncryptionSetId и EncryptionType добавлены в следующие командлеты:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="82d40-1232">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="82d40-1233">Добавлен параметр PublicIPAddressVersion в New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="82d40-1233">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="82d40-1234">FileUris для расширения пользовательских скриптов теперь будет защищенным, а не общедоступным параметром</span><span class="sxs-lookup"><span data-stu-id="82d40-1234">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="82d40-1235">Добавлено ScaleInPolicy в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="82d40-1235">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="82d40-1236">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="82d40-1236">Breaking changes</span></span>
    - <span data-ttu-id="82d40-1237">Параметр UploadSizeInBytes применяется теперь вместо DiskSizeGB для New-AzDiskConfig, если CreateOption имеет значение Upload</span><span class="sxs-lookup"><span data-stu-id="82d40-1237">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="82d40-1238">PublishingProfile.Source.ManagedImage.Id заменяется на StorageProfile.Source.Id в объекте GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="82d40-1238">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="82d40-1239">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="82d40-1239">Az.DataFactory</span></span>
* <span data-ttu-id="82d40-1240">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.3.0.</span><span class="sxs-lookup"><span data-stu-id="82d40-1240">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="82d40-1241">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="82d40-1241">Az.DataLakeStore</span></span>
* <span data-ttu-id="82d40-1242">Обновлен пакет SDK для ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), включает следующие исправления</span><span class="sxs-lookup"><span data-stu-id="82d40-1242">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="82d40-1243">Не создается исключение при невозможности десериализовать значение времени создания для записи в корзине или каталоге.</span><span class="sxs-lookup"><span data-stu-id="82d40-1243">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="82d40-1244">Предоставляется параметр для времени ожидания запроса в adlsclient</span><span class="sxs-lookup"><span data-stu-id="82d40-1244">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="82d40-1245">Исправлена передача исходного значения syncflag для восстановления badoffset</span><span class="sxs-lookup"><span data-stu-id="82d40-1245">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="82d40-1246">Исправлена операция EnumerateDirectory, чтобы она извлекала токен продолжения после проверки ответа</span><span class="sxs-lookup"><span data-stu-id="82d40-1246">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="82d40-1247">Исправлена ошибка объединения</span><span class="sxs-lookup"><span data-stu-id="82d40-1247">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="82d40-1248">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="82d40-1248">Az.FrontDoor</span></span>
* <span data-ttu-id="82d40-1249">Исправлены разные опечатки в разных частях модуля</span><span class="sxs-lookup"><span data-stu-id="82d40-1249">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="82d40-1250">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="82d40-1250">Az.HDInsight</span></span>
* <span data-ttu-id="82d40-1251">Исправлена ошибка, из-за которой клиент получал сообщение об ошибке 'Not a valid Base-64 string' (Не является допустимой строкой Base64) при выполнении Get-AzHDInsightCluster для получения кластера с хранилищем ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="82d40-1251">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="82d40-1252">Добавлен параметр с именем ApplicationId в три командлета Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig и New-AzHDInsightCluster, чтобы клиент мог предоставить идентификатор приложения субъекта-службы для доступа к Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="82d40-1252">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="82d40-1253">Для Microsoft.Azure.Management.HDInsight изменена версия с 2.1.0 на 5.1.0</span><span class="sxs-lookup"><span data-stu-id="82d40-1253">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="82d40-1254">Удалены пять командлетов:</span><span class="sxs-lookup"><span data-stu-id="82d40-1254">Removed five cmdlets:</span></span>
    - <span data-ttu-id="82d40-1255">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="82d40-1255">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="82d40-1256">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="82d40-1256">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="82d40-1257">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="82d40-1257">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="82d40-1258">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="82d40-1258">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="82d40-1259">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="82d40-1259">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="82d40-1260">Добавлены три командлета:</span><span class="sxs-lookup"><span data-stu-id="82d40-1260">Added three cmdlets:</span></span>
    - <span data-ttu-id="82d40-1261">Get-AzHDInsightMonitoring заменяет собой Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="82d40-1261">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="82d40-1262">Enable-AzHDInsightMonitoring заменяет собой Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="82d40-1262">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="82d40-1263">Disable-AzHDInsightMonitoring заменяет собой Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="82d40-1263">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="82d40-1264">Исправлен командлет Get-AzHDInsightProperties, чтобы он поддерживал получение сведений о возможностях из определенного расположения.</span><span class="sxs-lookup"><span data-stu-id="82d40-1264">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="82d40-1265">Удалены наборы параметров ("Spark1", "Spark2") из Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="82d40-1265">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="82d40-1266">Добавлены примеры в справочные документы по командлету Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="82d40-1266">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="82d40-1267">Изменен тип выходных данных для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="82d40-1267">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="82d40-1268">Для Get-AzHDInsightProperties тип выходных данных изменен с CapabilitiesResponse на AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="82d40-1268">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="82d40-1269">Для Remove-AzHDInsightCluster тип выходных данных изменен с ClusterGetResponse на bool.</span><span class="sxs-lookup"><span data-stu-id="82d40-1269">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="82d40-1270">Для Set-AzHDInsightGatewaySettings тип выходных данных изменен с HttpConnectivitySettings на GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="82d40-1270">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="82d40-1271">Добавлены несколько условий для проверки сценариев.</span><span class="sxs-lookup"><span data-stu-id="82d40-1271">Added some scenario test cases.</span></span>
* <span data-ttu-id="82d40-1272">Удалены несколько псевдонимов: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="82d40-1272">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="82d40-1273">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="82d40-1273">Az.IotHub</span></span>
* <span data-ttu-id="82d40-1274">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="82d40-1274">Breaking changes:</span></span>
    - <span data-ttu-id="82d40-1275">Командлет Add-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="82d40-1275">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="82d40-1276">Удален набор параметров __AllParameterSets для командлета Add-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="82d40-1276">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="82d40-1277">Командлет Get-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="82d40-1277">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="82d40-1278">Удален набор параметров __AllParameterSets для командлета Get-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="82d40-1278">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="82d40-1279">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties.</span><span class="sxs-lookup"><span data-stu-id="82d40-1279">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="82d40-1280">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties.</span><span class="sxs-lookup"><span data-stu-id="82d40-1280">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="82d40-1281">Командлет New-AzIotHubExportDevice больше не поддерживает псевдоним New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="82d40-1281">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="82d40-1282">Командлет New-AzIotHubImportDevice больше не поддерживает псевдоним New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="82d40-1282">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="82d40-1283">Командлет Remove-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="82d40-1283">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="82d40-1284">Удален набор параметров __AllParameterSets для командлета Remove-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="82d40-1284">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="82d40-1285">Командлет Set-AzIotHub теперь не поддерживает параметр OperationsMonitoringProperties и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="82d40-1285">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="82d40-1286">Удален набор параметров UpdateOperationsMonitoringProperties для командлета Set-AzIotHub.</span><span class="sxs-lookup"><span data-stu-id="82d40-1286">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="82d40-1287">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="82d40-1287">Az.RecoveryServices</span></span>
* <span data-ttu-id="82d40-1288">Azure Site Recovery поддерживает настройку сетевых ресурсов, например групп безопасности сети, общедоступных IP-адресов и внутренних подсистем балансировки нагрузки из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-1288">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="82d40-1289">Azure Site Recovery поддерживает запись на управляемый диск из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-1289">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="82d40-1290">Azure Site Recovery поддерживает сокращение NIC из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-1290">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="82d40-1291">Azure Site Recovery поддерживает ускорение сети NIC из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-1291">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="82d40-1292">Azure Site Recovery поддерживает автоматическое обновление агента из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-1292">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="82d40-1293">Azure Site Recovery поддерживает стандартный SSD-накопитель из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-1293">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="82d40-1294">Azure Site Recovery поддерживает двухпроходное шифрование диска Azure из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-1294">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="82d40-1295">Azure Site Recovery поддерживает новый добавленный диск из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-1295">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="82d40-1296">Добавлена функция SoftDelete для виртуальных машин и соответствующие тесты</span><span class="sxs-lookup"><span data-stu-id="82d40-1296">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="82d40-1297">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82d40-1297">Az.Resources</span></span>
* <span data-ttu-id="82d40-1298">Обновлена сборка зависимостей Microsoft.Extensions.Caching.Memory с версии 1.1.1 до 2.2</span><span class="sxs-lookup"><span data-stu-id="82d40-1298">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82d40-1299">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82d40-1299">Az.Network</span></span>
* <span data-ttu-id="82d40-1300">Изменены все командлеты для PrivateEndpointConnection, чтобы они поддерживали универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="82d40-1300">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="82d40-1301">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="82d40-1301">Updated cmdlet:</span></span>
        - <span data-ttu-id="82d40-1302">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="82d40-1302">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="82d40-1303">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="82d40-1303">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="82d40-1304">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="82d40-1304">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="82d40-1305">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="82d40-1305">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="82d40-1306">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="82d40-1306">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="82d40-1307">Добавлен новый командлет для PrivateLinkResource, который поддерживает универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="82d40-1307">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="82d40-1308">Новый командлет</span><span class="sxs-lookup"><span data-stu-id="82d40-1308">New cmdlet:</span></span>
        - <span data-ttu-id="82d40-1309">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="82d40-1309">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="82d40-1310">Добавлены новые поля и параметр для протокола прокси версии 2.</span><span class="sxs-lookup"><span data-stu-id="82d40-1310">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="82d40-1311">Добавлено свойство EnableProxyProtocol в PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="82d40-1311">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="82d40-1312">Добавлено свойство LinkIdentifier в PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="82d40-1312">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="82d40-1313">Обновлен New-AzPrivateLinkService для поддержки нового необязательного параметра EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="82d40-1313">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="82d40-1314">Исправлено описание параметра в справочной документации по командлету New-AzApplicationGatewaySku.</span><span class="sxs-lookup"><span data-stu-id="82d40-1314">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="82d40-1315">Новые командлеты для поддержки политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="82d40-1315">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="82d40-1316">Добавлена поддержка дочерних ресурсов RouteTables для VirtualHub</span><span class="sxs-lookup"><span data-stu-id="82d40-1316">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="82d40-1317">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="82d40-1317">New cmdlets added:</span></span>
        - <span data-ttu-id="82d40-1318">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="82d40-1318">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="82d40-1319">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="82d40-1319">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="82d40-1320">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="82d40-1320">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="82d40-1321">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="82d40-1321">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="82d40-1322">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="82d40-1322">Set-AzVirtualHub</span></span>
* <span data-ttu-id="82d40-1323">Добавлена поддержка новых свойств SKU для VirtualHub и VirtualWANType в VirtualWan</span><span class="sxs-lookup"><span data-stu-id="82d40-1323">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="82d40-1324">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="82d40-1324">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="82d40-1325">New-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="82d40-1325">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="82d40-1326">Update-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="82d40-1326">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="82d40-1327">New-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="82d40-1327">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="82d40-1328">Update-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="82d40-1328">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="82d40-1329">Добавлена поддержка свойства EnableInternetSecurity для HubVnetConnection, VpnConnection и ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="82d40-1329">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="82d40-1330">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="82d40-1330">New cmdlets added:</span></span>
        - <span data-ttu-id="82d40-1331">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="82d40-1331">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="82d40-1332">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="82d40-1332">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="82d40-1333">New-AzureRmVirtualHubVnetConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="82d40-1333">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="82d40-1334">New-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="82d40-1334">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="82d40-1335">Update-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="82d40-1335">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="82d40-1336">New-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="82d40-1336">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="82d40-1337">Set-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="82d40-1337">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="82d40-1338">Добавлена поддержка настройки политики верхнего уровня WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="82d40-1338">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="82d40-1339">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="82d40-1339">New cmdlets added:</span></span>
        - <span data-ttu-id="82d40-1340">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="82d40-1340">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="82d40-1341">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="82d40-1341">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="82d40-1342">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="82d40-1342">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="82d40-1343">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="82d40-1343">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="82d40-1344">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="82d40-1344">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="82d40-1345">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="82d40-1345">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="82d40-1346">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="82d40-1346">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="82d40-1347">New-AzApplicationGatewayFirewallPolicy: добавлены параметры PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="82d40-1347">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="82d40-1348">Добавлена поддержка оператора Geo-Match для CustomRule</span><span class="sxs-lookup"><span data-stu-id="82d40-1348">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="82d40-1349">Добавлен параметр GeoMatch в оператор для FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="82d40-1349">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="82d40-1350">Добавлена поддержка политики брандмауэра perListener и perSite</span><span class="sxs-lookup"><span data-stu-id="82d40-1350">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="82d40-1351">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="82d40-1351">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="82d40-1352">New-AzApplicationGatewayHttpListener: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="82d40-1352">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="82d40-1353">New-AzApplicationGatewayPathRuleConfig: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="82d40-1353">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="82d40-1354">Исправлен учет регистра для требуемой подсети с именем AzureBastionSubnet в PSBastion</span><span class="sxs-lookup"><span data-stu-id="82d40-1354">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="82d40-1355">Поддержка полного доменного имени назначения в правилах сети и преобразованного полного доменного имени в правилах NAT для брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="82d40-1355">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="82d40-1356">Добавлена поддержка ресурсов верхнего уровня RouteTables для IpGroup</span><span class="sxs-lookup"><span data-stu-id="82d40-1356">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="82d40-1357">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="82d40-1357">New cmdlets added:</span></span>
        - <span data-ttu-id="82d40-1358">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="82d40-1358">New-AzIpGroup</span></span>
        - <span data-ttu-id="82d40-1359">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="82d40-1359">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="82d40-1360">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="82d40-1360">Get-AzIpGroup</span></span>
        - <span data-ttu-id="82d40-1361">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="82d40-1361">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="82d40-1362">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="82d40-1362">Az.ServiceFabric</span></span>
* <span data-ttu-id="82d40-1363">Удален командлет Add-AzServiceFabricApplicationCertificate, так как соответствующий сценарий выполняется командлетом Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="82d40-1363">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="82d40-1364">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82d40-1364">Az.Sql</span></span>
* <span data-ttu-id="82d40-1365">Добавлена поддержка восстановления удаленных баз данных в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="82d40-1365">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="82d40-1366">Из кода удалены старые командлеты аудита.</span><span class="sxs-lookup"><span data-stu-id="82d40-1366">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="82d40-1367">Удалены нерекомендуемые псевдонимы:</span><span class="sxs-lookup"><span data-stu-id="82d40-1367">Removed deprecated aliases:</span></span>
* <span data-ttu-id="82d40-1368">Get-AzSqlDatabaseIndexRecommendations (вместо него используйте Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="82d40-1368">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="82d40-1369">Get-AzSqlDatabaseRestorePoints (вместо него используйте Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="82d40-1369">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="82d40-1370">Удален командлет Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="82d40-1370">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="82d40-1371">Удалены псевдонимы для нерекомендуемых командлетов параметров оценки уязвимостей</span><span class="sxs-lookup"><span data-stu-id="82d40-1371">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="82d40-1372">Командлеты расширенного обнаружения угроз объявлены устаревшими</span><span class="sxs-lookup"><span data-stu-id="82d40-1372">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="82d40-1373">Добавлены командлеты для отключения и включения рекомендаций о конфиденциальности для столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="82d40-1373">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="82d40-1374">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="82d40-1374">Az.Storage</span></span>
* <span data-ttu-id="82d40-1375">Поддержка включения большой общей папки при создании или обновлении учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="82d40-1375">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="82d40-1376">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="82d40-1376">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="82d40-1377">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="82d40-1377">Set-AzStorageAccount</span></span>
* <span data-ttu-id="82d40-1378">При закрытии или получении маркера файла пропускается проверка того, является ли входной путь файлом или каталогом, чтобы избежать сбоев при получении объектов в состоянии DeletePending.</span><span class="sxs-lookup"><span data-stu-id="82d40-1378">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="82d40-1379">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="82d40-1379">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="82d40-1380">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="82d40-1380">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="82d40-1381">2.8.0 — октябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="82d40-1381">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="82d40-1382">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="82d40-1382">General</span></span>
* <span data-ttu-id="82d40-1383">Выпуск Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="82d40-1383">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="82d40-1384">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="82d40-1384">Az.Accounts</span></span>
* <span data-ttu-id="82d40-1385">Обновление телеметрии и перезаписи URL-адресов для созданных модулей, исправление для модульных тестов Windows.</span><span class="sxs-lookup"><span data-stu-id="82d40-1385">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="82d40-1386">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="82d40-1386">Az.ApiManagement</span></span>
* <span data-ttu-id="82d40-1387">**Set-AzApiManagementApi** — в ApiVersionSet добавлена поддержка обновления API.</span><span class="sxs-lookup"><span data-stu-id="82d40-1387">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="82d40-1388">исправлена проблема https://github.com/Azure/azure-powershell/issues/10068.</span><span class="sxs-lookup"><span data-stu-id="82d40-1388">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="82d40-1389">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="82d40-1389">Az.Automation</span></span>
* <span data-ttu-id="82d40-1390">Исправлен командлет New-AzureAutomationSoftwareUpdateConfiguration для параметра перезагрузки Linux.</span><span class="sxs-lookup"><span data-stu-id="82d40-1390">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="82d40-1391">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="82d40-1391">Az.Batch</span></span>
* <span data-ttu-id="82d40-1392">Командлет **Get-AzBatchNodeAgentSku** объявлен устаревшим и будет заменен на **Get-AzBatchSupportImage** в версии 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="82d40-1392">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82d40-1393">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82d40-1393">Az.Compute</span></span>
* <span data-ttu-id="82d40-1394">В командлеты New-AzVM и New-AzVmss добавлены параметры Priority, EvictionPolicy и MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="82d40-1394">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="82d40-1395">Исправлены предупреждающее сообщение для командлетов Add-AzVMAdditionalUnattendContent и Add-AzVMSshPublicKey и справочная документация по ним.</span><span class="sxs-lookup"><span data-stu-id="82d40-1395">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="82d40-1396">Для Set-AzVMDiskEncryptionExtension исправлено исключение -skipVmBackup для виртуальных машин Linux с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="82d40-1396">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="82d40-1397">Исправлена ошибка при изменении параметров шифрования в Set-AzVMDiskEncryptionExtension, реализован двухэтапный сценарий.</span><span class="sxs-lookup"><span data-stu-id="82d40-1397">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="82d40-1398">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="82d40-1398">Az.DataFactory</span></span>
* <span data-ttu-id="82d40-1399">Добавлены команды CRUD для потока данных Фабрики данных Azure версии 2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow и Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="82d40-1399">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="82d40-1400">Добавлены команды действий для сеанса отладки потока данных Фабрики данных Azure версии 2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand и Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="82d40-1400">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="82d40-1401">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.2.0.</span><span class="sxs-lookup"><span data-stu-id="82d40-1401">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="82d40-1402">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="82d40-1402">Az.DataLakeStore</span></span>
* <span data-ttu-id="82d40-1403">Проверка учетной записи исправлена так, чтобы учетные записи, содержащие знак "-", можно было передавать без домена.</span><span class="sxs-lookup"><span data-stu-id="82d40-1403">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="82d40-1404">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="82d40-1404">Az.HealthcareApis</span></span>
* <span data-ttu-id="82d40-1405">Версия PowerShell обновлена до 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="82d40-1405">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="82d40-1406">Версия пакета SDK обновлена до 1.0.2.</span><span class="sxs-lookup"><span data-stu-id="82d40-1406">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="82d40-1407">В тестах обновлены ссылки на новую версию пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="82d40-1407">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="82d40-1408">Вложенная выходная структура заменена на плоскую.</span><span class="sxs-lookup"><span data-stu-id="82d40-1408">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="82d40-1409">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="82d40-1409">Az.IotHub</span></span>
* <span data-ttu-id="82d40-1410">Добавлен новый источник маршрутизации DigitalTwinChangeEvents.</span><span class="sxs-lookup"><span data-stu-id="82d40-1410">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="82d40-1411">Исправлены незначительные ошибки: Get-AzIothub не возвращает subscriptionId.</span><span class="sxs-lookup"><span data-stu-id="82d40-1411">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="82d40-1412">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="82d40-1412">Az.Monitor</span></span>
* <span data-ttu-id="82d40-1413">Добавлены новые получатели групп действий: -ItsmReceiver, -VoiceReceiver, -ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver.</span><span class="sxs-lookup"><span data-stu-id="82d40-1413">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="82d40-1414">Для получателей включите общую схему оповещений.</span><span class="sxs-lookup"><span data-stu-id="82d40-1414">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="82d40-1415">Это не касается получателей SMS, push-уведомлений приложения Azure, ITSM и голосовых сообщений.</span><span class="sxs-lookup"><span data-stu-id="82d40-1415">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="82d40-1416">Веб-перехватчики теперь поддерживают аутентификацию Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="82d40-1416">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82d40-1417">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82d40-1417">Az.Network</span></span>
* <span data-ttu-id="82d40-1418">Добавлен новый командлет Get-AzAvailableServiceAlias, позволяющий получить псевдонимы для политик конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="82d40-1418">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="82d40-1419">В подключениях шлюза виртуальной сети появилась возможность добавлять селекторы трафика.</span><span class="sxs-lookup"><span data-stu-id="82d40-1419">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="82d40-1420">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="82d40-1420">New cmdlets added:</span></span>
        - <span data-ttu-id="82d40-1421">New-AzureRmTrafficSelectorPolicy.</span><span class="sxs-lookup"><span data-stu-id="82d40-1421">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="82d40-1422">В командлеты добавлены необязательные параметры -TrafficSelectorPolicies, -New-AzureRmVirtualNetworkGatewayConnection, -Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="82d40-1422">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="82d40-1423">В конфигурациях правил сетевой безопасности добавлена поддержка протоколов ESP и AH.</span><span class="sxs-lookup"><span data-stu-id="82d40-1423">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="82d40-1424">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="82d40-1424">Updated cmdlets:</span></span>
        - <span data-ttu-id="82d40-1425">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="82d40-1425">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="82d40-1426">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="82d40-1426">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="82d40-1427">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="82d40-1427">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="82d40-1428">Улучшена обработка исключений в командлетах Cortex.</span><span class="sxs-lookup"><span data-stu-id="82d40-1428">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="82d40-1429">Выпущены новые поколения и номера SKU VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="82d40-1429">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="82d40-1430">Представлены новые поколения VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="82d40-1430">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="82d40-1431">Представлены новые номера SKU VirtualNetworkGateways с высокой пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="82d40-1431">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="82d40-1432">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="82d40-1432">Az.RedisCache</span></span>
* <span data-ttu-id="82d40-1433">В справочную документацию по Set-AzRedisCache добавлены недостающие значения для параметра -Size.</span><span class="sxs-lookup"><span data-stu-id="82d40-1433">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="82d40-1434">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82d40-1434">Az.Sql</span></span>
* <span data-ttu-id="82d40-1435">Добавлена возможность назначать администратора Active Directory в Управляемом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="82d40-1435">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="82d40-1436">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="82d40-1436">Az.Storage</span></span>
* <span data-ttu-id="82d40-1437">Клиентская библиотека службы хранилища Azure обновлена до версии 11.1.0.</span><span class="sxs-lookup"><span data-stu-id="82d40-1437">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="82d40-1438">NextPageLink теперь позволяет получить список контейнеров с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="82d40-1438">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="82d40-1439">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="82d40-1439">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="82d40-1440">NextPageLink теперь позволяет получить список учетных записей хранения из подписки.</span><span class="sxs-lookup"><span data-stu-id="82d40-1440">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="82d40-1441">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="82d40-1441">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="82d40-1442">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="82d40-1442">Az.StorageSync</span></span>
* <span data-ttu-id="82d40-1443">Исправлена проблема 9810 с Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="82d40-1443">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="82d40-1444">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="82d40-1444">Az.Websites</span></span>
* <span data-ttu-id="82d40-1445">Обновление плана службы приложений с помощью Set-AzWebApp приводило к сбою приложения.</span><span class="sxs-lookup"><span data-stu-id="82d40-1445">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="82d40-1446">2.7.0 — сентябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="82d40-1446">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="82d40-1447">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="82d40-1447">Az.ApiManagement</span></span>
* <span data-ttu-id="82d40-1448">В справочной документации по командлету Set-AzApiManagementPolicy обновлено описание параметра -Format.</span><span class="sxs-lookup"><span data-stu-id="82d40-1448">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="82d40-1449">Из справочной документации удалены ссылки на нерекомендуемый командлет Update-AzApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="82d40-1449">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="82d40-1450">Вместо него следует использовать командлет Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="82d40-1450">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="82d40-1451">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="82d40-1451">Az.Automation</span></span>
* <span data-ttu-id="82d40-1452">В справочной документации по командлету Register-AzAutomationDscNode исправлена опечатка в примере.</span><span class="sxs-lookup"><span data-stu-id="82d40-1452">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="82d40-1453">Добавлено уточнение об ограничениях ОС для командлета Register-AzAutomationDSCNode.</span><span class="sxs-lookup"><span data-stu-id="82d40-1453">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="82d40-1454">Исправлено исключение пустой ссылки для параметра -Wait в командлете Start-AzAutomationRunbook.</span><span class="sxs-lookup"><span data-stu-id="82d40-1454">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82d40-1455">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82d40-1455">Az.Compute</span></span>
* <span data-ttu-id="82d40-1456">Добавлен параметр UploadSizeInBytes для командлета New-AzDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="82d40-1456">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="82d40-1457">Добавлен добавочный параметр для командлета New-AzSnapshotConfig.</span><span class="sxs-lookup"><span data-stu-id="82d40-1457">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="82d40-1458">Для виртуальной машины добавлены такие функции с низким приоритетом:</span><span class="sxs-lookup"><span data-stu-id="82d40-1458">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="82d40-1459">Для командлета New-AzVMConfig добавлены параметры MaxPrice, EvictionPolicy и Priority.</span><span class="sxs-lookup"><span data-stu-id="82d40-1459">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="82d40-1460">Для командлетов New-AzVmssConfig, Update-AzVM и Update-AzVmss добавлен параметр MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="82d40-1460">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="82d40-1461">Для командлета Get-AzAvailabilitySet устранена проблема со ссылкой на виртуальную машину, когда в нем перечисляются все группы доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="82d40-1461">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="82d40-1462">Исправлено исключение NULL для командлета Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="82d40-1462">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="82d40-1463">Исправлен метод поиска VHD для относительной конечной позиции.</span><span class="sxs-lookup"><span data-stu-id="82d40-1463">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="82d40-1464">Устранена проблема с UltraSSD для командлетов New-AzVM и Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="82d40-1464">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="82d40-1465">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="82d40-1465">Az.DataFactory</span></span>
* <span data-ttu-id="82d40-1466">Добавлены 3 новые команды для ADF версии 2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription и Get-AzDataFactoryV2TriggerSubscriptionStatus.</span><span class="sxs-lookup"><span data-stu-id="82d40-1466">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="82d40-1467">Пакет SDK ADF для .NET обновлен до версии 4.1.3.</span><span class="sxs-lookup"><span data-stu-id="82d40-1467">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="82d40-1468">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="82d40-1468">Az.HDInsight</span></span>
* <span data-ttu-id="82d40-1469">Укажите критические изменения.</span><span class="sxs-lookup"><span data-stu-id="82d40-1469">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="82d40-1470">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="82d40-1470">Az.IotHub</span></span>
* <span data-ttu-id="82d40-1471">Добавлена поддержка для вызова отработки отказа для IotHub в георегион аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="82d40-1471">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="82d40-1472">Добавлена поддержка для управления обогащением сообщений для IotHub.</span><span class="sxs-lookup"><span data-stu-id="82d40-1472">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="82d40-1473">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="82d40-1473">New cmdlets are:</span></span>
    - <span data-ttu-id="82d40-1474">Add-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="82d40-1474">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="82d40-1475">Get-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="82d40-1475">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="82d40-1476">Remove-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="82d40-1476">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="82d40-1477">Set-AzIotHubMessageEnrichment.</span><span class="sxs-lookup"><span data-stu-id="82d40-1477">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="82d40-1478">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="82d40-1478">Az.Monitor</span></span>
* <span data-ttu-id="82d40-1479">Указание на самую последнюю версию пакета SDK для монитора, т. е. 0.24.1-preview:</span><span class="sxs-lookup"><span data-stu-id="82d40-1479">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="82d40-1480">В командлеты метрик добавлены некритические изменения, т. е. перечисление единиц поддерживает несколько новых значений.</span><span class="sxs-lookup"><span data-stu-id="82d40-1480">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="82d40-1481">Эти командлеты доступны только для чтения, поэтому входные данные командлетов не будут изменены.</span><span class="sxs-lookup"><span data-stu-id="82d40-1481">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="82d40-1482">Актуальная версия API запросов **ActionGroups** — **2019-06-01**. До этого была версия **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="82d40-1482">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="82d40-1483">Тесты сценария обновлены в соответствии с этим изменением.</span><span class="sxs-lookup"><span data-stu-id="82d40-1483">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="82d40-1484">В конструкторы классов **EmailReceiver** и **WebhookReceiver** добавлен один новый обязательный аргумент — логическое значение с именем **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="82d40-1484">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="82d40-1485">Сейчас для него установлено значение **false**, чтобы скрыть это критическое изменение от командлетов.</span><span class="sxs-lookup"><span data-stu-id="82d40-1485">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="82d40-1486">**Примечание**. Это временное изменение, которое должно быть подтверждено командой оповещения.</span><span class="sxs-lookup"><span data-stu-id="82d40-1486">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="82d40-1487">Порядок аргументов для конструктора класса **Source** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="82d40-1487">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="82d40-1488">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="82d40-1488">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="82d40-1489">Порядок аргументов для конструктора класса **AlertingAction** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="82d40-1489">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="82d40-1490">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="82d40-1490">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="82d40-1491">Добавлена поддержка критериев динамического порога для оповещения метрики версии 2:</span><span class="sxs-lookup"><span data-stu-id="82d40-1491">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="82d40-1492">New-AzMetricAlertRuleV2Criteria: теперь также позволяет создавать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="82d40-1492">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="82d40-1493">Add-AzMetricAlertRuleV2: теперь также позволяет принимать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="82d40-1493">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="82d40-1494">Добавлены усовершенствования в командлетах запланированных правил запросов (SQR).</span><span class="sxs-lookup"><span data-stu-id="82d40-1494">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="82d40-1495">Командлеты будут принимать параметр Location в обоих форматах: расположение (например, eastus) или отображаемое имя расположения (например, "восточная часть США").</span><span class="sxs-lookup"><span data-stu-id="82d40-1495">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="82d40-1496">Параметр Enabled проиллюстрирован в файлах справки надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="82d40-1496">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="82d40-1497">Добавлены примеры для необязательного параметра ActionGroup.</span><span class="sxs-lookup"><span data-stu-id="82d40-1497">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="82d40-1498">Все файлы справки улучшены.</span><span class="sxs-lookup"><span data-stu-id="82d40-1498">Overall improved help files</span></span>
* <span data-ttu-id="82d40-1499">Исправлена ошибка в определении типа области для командлета Set-AzActionRule.</span><span class="sxs-lookup"><span data-stu-id="82d40-1499">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82d40-1500">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82d40-1500">Az.Network</span></span>
* <span data-ttu-id="82d40-1501">Исправлен неправильный пример в справочной документации по командлету New-AzApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="82d40-1501">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="82d40-1502">В справочную документацию по командлету Get-AzNetworkWatcherPacketCapture добавлено примечание, посвященное извлечению всех свойств для записи пакетов.</span><span class="sxs-lookup"><span data-stu-id="82d40-1502">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="82d40-1503">В справочной документации по командлету Test-AzNetworkWatcherIPFlow исправлен пример: теперь он правильно перечисляет сетевые карты.</span><span class="sxs-lookup"><span data-stu-id="82d40-1503">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="82d40-1504">Улучшен анализ облачных исключений для отображения дополнительных сведений (при их наличии).</span><span class="sxs-lookup"><span data-stu-id="82d40-1504">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="82d40-1505">Улучшен анализ облачных исключений для обработки дополнительного типа исключения SDK.</span><span class="sxs-lookup"><span data-stu-id="82d40-1505">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="82d40-1506">Исправлено неправильное сопоставление моделей правил безопасности.</span><span class="sxs-lookup"><span data-stu-id="82d40-1506">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="82d40-1507">Добавлены свойства сетевого интерфейса для компонента частного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="82d40-1507">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="82d40-1508">Для интерфейса PSNetworkInterface добавлено свойство PrivateEndpoint с типом PSResourceId.</span><span class="sxs-lookup"><span data-stu-id="82d40-1508">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="82d40-1509">В PSNetworkInterfaceIPConfiguration добавлено свойство PrivateLinkConnectionProperties с типом PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="82d40-1509">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="82d40-1510">Добавлен новый класс модели: PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="82d40-1510">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="82d40-1511">Добавлен новый тип ApplicationRuleProtocolType "mssql" для ресурса Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-1511">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="82d40-1512">Поддержка многоканального подключения в Виртуальной глобальной сети:</span><span class="sxs-lookup"><span data-stu-id="82d40-1512">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="82d40-1513">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="82d40-1513">New cmdlets</span></span>
        - <span data-ttu-id="82d40-1514">New-AzVpnSiteLink;</span><span class="sxs-lookup"><span data-stu-id="82d40-1514">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="82d40-1515">New-AzVpnSiteLinkConnection;</span><span class="sxs-lookup"><span data-stu-id="82d40-1515">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="82d40-1516">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="82d40-1516">Updated cmdlet:</span></span>
        - <span data-ttu-id="82d40-1517">New-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="82d40-1517">New-VpnSite</span></span>
        - <span data-ttu-id="82d40-1518">Update-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="82d40-1518">Update-VpnSite</span></span>
        - <span data-ttu-id="82d40-1519">New-VpnConnection;</span><span class="sxs-lookup"><span data-stu-id="82d40-1519">New-VpnConnection</span></span>
        - <span data-ttu-id="82d40-1520">Update-VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="82d40-1520">Update-VpnConnection</span></span>
* <span data-ttu-id="82d40-1521">Исправлены документы с некоторыми примерами PowerShell для использования командлетов AZ вместо командлетов AzureRM.</span><span class="sxs-lookup"><span data-stu-id="82d40-1521">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="82d40-1522">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="82d40-1522">Az.RecoveryServices</span></span>
* <span data-ttu-id="82d40-1523">Для объекта AzureVMpolicy добавлен новый атрибут — ProtectedItemsCount.</span><span class="sxs-lookup"><span data-stu-id="82d40-1523">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="82d40-1524">Добавлены тесты для политики виртуальной машины и восстановления исходной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="82d40-1524">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="82d40-1525">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82d40-1525">Az.Resources</span></span>
* <span data-ttu-id="82d40-1526">Исправлена ошибка, при которой не удавалось вызвать командлет New-AzRoleAssignment без параметра Scope.</span><span class="sxs-lookup"><span data-stu-id="82d40-1526">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="82d40-1527">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="82d40-1527">Az.ServiceFabric</span></span>
* <span data-ttu-id="82d40-1528">Исправлена опечатка в примере в справочной документации по командлету Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="82d40-1528">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="82d40-1529">Добавлены новые командлеты для управления приложениями и службами:</span><span class="sxs-lookup"><span data-stu-id="82d40-1529">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="82d40-1530">New-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="82d40-1530">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="82d40-1531">New-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="82d40-1531">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="82d40-1532">New-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="82d40-1532">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="82d40-1533">New-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="82d40-1533">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="82d40-1534">Update-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="82d40-1534">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="82d40-1535">Get-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="82d40-1535">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="82d40-1536">Get-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="82d40-1536">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="82d40-1537">Get-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="82d40-1537">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="82d40-1538">Get-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="82d40-1538">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="82d40-1539">Remove-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="82d40-1539">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="82d40-1540">Remove-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="82d40-1540">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="82d40-1541">Remove-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="82d40-1541">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="82d40-1542">Remove-AzServiceFabricServic.</span><span class="sxs-lookup"><span data-stu-id="82d40-1542">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="82d40-1543">Пакет SDK для Service Fabric обновлен до версии 1.2.0, в которой используется версия API 2019-03-01 поставщика ресурсов Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="82d40-1543">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="82d40-1544">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="82d40-1544">Az.SignalR</span></span>
* <span data-ttu-id="82d40-1545">Добавлены командлеты Update, Restart, CheckNameAvailability и GetUsage.</span><span class="sxs-lookup"><span data-stu-id="82d40-1545">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="82d40-1546">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82d40-1546">Az.Sql</span></span>
* <span data-ttu-id="82d40-1547">Обновлен пример в справочной документации по командлету Get-AzSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="82d40-1547">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="82d40-1548">Добавлен пример виртуального ядра для командлета создания эластичного пула (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="82d40-1548">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="82d40-1549">Удалена проверка свойства EmailAddresses и того, что свойство EmailAdmins правильное в случае, если свойство EmailAddresses пустое в командлетах Set-AzSqlServerAdvancedThreatProtectionPolicy и Set-AzSqlDatabaseAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="82d40-1549">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="82d40-1550">Теперь, если существует несколько параметров диагностики, включающих категорию аудита, параметры аудита сервера и базы данных удаляются.</span><span class="sxs-lookup"><span data-stu-id="82d40-1550">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="82d40-1551">Исправлена проверка адресов электронной почты в нескольких командлетах оценки уязвимостей SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting и Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="82d40-1551">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="82d40-1552">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="82d40-1552">Az.Storage</span></span>
* <span data-ttu-id="82d40-1553">Обновлен пример в справочной документации по командлету Get-AzStorageAccountKey.</span><span class="sxs-lookup"><span data-stu-id="82d40-1553">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="82d40-1554">Теперь при отправке и загрузке файла Azure в конечном файле сохраняются свойства SMB исходного файла (атрибуты файла, время создания файла, время последней записи файла).</span><span class="sxs-lookup"><span data-stu-id="82d40-1554">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="82d40-1555">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="82d40-1555">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="82d40-1556">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="82d40-1556">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="82d40-1557">Исправлена операция отправки блочного BLOB-объекта, в которой происходили сбои свойств и метаданных в контейнере с включенной ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="82d40-1557">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="82d40-1558">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="82d40-1558">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="82d40-1559">Добавлена поддержка управления общими папками Azure в API плоскости управления с помощью таких командлетов:</span><span class="sxs-lookup"><span data-stu-id="82d40-1559">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="82d40-1560">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="82d40-1560">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="82d40-1561">Get-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="82d40-1561">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="82d40-1562">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="82d40-1562">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="82d40-1563">Remove-AzRmStorageShare.</span><span class="sxs-lookup"><span data-stu-id="82d40-1563">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="82d40-1564">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="82d40-1564">Az.Websites</span></span>
* <span data-ttu-id="82d40-1565">Устранена проблема, из-за которой теги webapp удалялись при переносе приложения в новый ASP.</span><span class="sxs-lookup"><span data-stu-id="82d40-1565">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="82d40-1566">Теперь командлет Publish-AzureWebapp работает в Linux и Windows.</span><span class="sxs-lookup"><span data-stu-id="82d40-1566">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="82d40-1567">Обновлен пример в справочной документации по командлету Get-AzWebAppPublishingProfile.</span><span class="sxs-lookup"><span data-stu-id="82d40-1567">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="82d40-1568">2.6.0 — август 2019 г.</span><span class="sxs-lookup"><span data-stu-id="82d40-1568">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="82d40-1569">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="82d40-1569">General</span></span>
* <span data-ttu-id="82d40-1570">Исправлены опечатки в модулях.</span><span class="sxs-lookup"><span data-stu-id="82d40-1570">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="82d40-1571">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="82d40-1571">Az.Accounts</span></span>
* <span data-ttu-id="82d40-1572">Добавлена поддержка назначаемого пользователем удостоверения MSI при проверке подлинности в Функциях Azure (№ 9479).</span><span class="sxs-lookup"><span data-stu-id="82d40-1572">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="82d40-1573">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="82d40-1573">Az.Aks</span></span>
* <span data-ttu-id="82d40-1574">Устранена проблема с выходными данными для Get-AzAks.</span><span class="sxs-lookup"><span data-stu-id="82d40-1574">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="82d40-1575">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9847.</span><span class="sxs-lookup"><span data-stu-id="82d40-1575">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="82d40-1576">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="82d40-1576">Az.ApiManagement</span></span>
* <span data-ttu-id="82d40-1577">исправлена проблема https://github.com/Azure/azure-powershell/issues/9351.</span><span class="sxs-lookup"><span data-stu-id="82d40-1577">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="82d40-1578">Обновлена версия NuGet для .NET, которая не накладывает ограничений на productId, apiId, groupId и userId.</span><span class="sxs-lookup"><span data-stu-id="82d40-1578">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="82d40-1579">**Get-AzApiManagementProduct**. Добавлена поддержка запросов к продуктам с помощью API.</span><span class="sxs-lookup"><span data-stu-id="82d40-1579">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="82d40-1580">**New-AzApiManagementApiRevision**. Устранена проблема, из-за которой не задавался параметр ApiRevisionDescription при создании новой редакции API https://github.com/Azure/azure-powershell/issues/9752.</span><span class="sxs-lookup"><span data-stu-id="82d40-1580">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="82d40-1581">Исправлено написание имени модели c PsApiManagementOAuth2AuthrozationServer на PsApiManagementOAuth2AuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="82d40-1581">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="82d40-1582">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="82d40-1582">Az.Batch</span></span>
* <span data-ttu-id="82d40-1583">Исправлена опечатка в написании Windows со строчной буквы в справочных сообщениях и документации.</span><span class="sxs-lookup"><span data-stu-id="82d40-1583">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="82d40-1584">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="82d40-1584">Az.Cdn</span></span>
* <span data-ttu-id="82d40-1585">Исправлена опечатка во вспомогательном приложении модуля CDN.</span><span class="sxs-lookup"><span data-stu-id="82d40-1585">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82d40-1586">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82d40-1586">Az.Compute</span></span>
* <span data-ttu-id="82d40-1587">Добавлен параметр VmssId в новый командлет Add New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="82d40-1587">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="82d40-1588">Добавлены параметры TerminateScheduledEvents и TerminateScheduledEventNotBeforeTimeoutInMinutes в New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="82d40-1588">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="82d40-1589">Добавлено свойство HyperVGeneration в объект образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="82d40-1589">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="82d40-1590">Добавлены компоненты Host и HostGroup.</span><span class="sxs-lookup"><span data-stu-id="82d40-1590">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="82d40-1591">Новые командлеты:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="82d40-1591">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="82d40-1592">Параметр HostId добавлен в New-AzVMConfig и New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="82d40-1592">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="82d40-1593">Исправлен пример в документации по Invoke-AzVMRunCommand, в котором теперь используется правильное имя параметра.</span><span class="sxs-lookup"><span data-stu-id="82d40-1593">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="82d40-1594">Исправлено описание VolumeType в справочной документации по Set-AzVMDiskEncryptionExtension и Set-AzVmssDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="82d40-1594">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="82d40-1595">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="82d40-1595">Az.DataFactory</span></span>
* <span data-ttu-id="82d40-1596">Исправлена опечатка в написании Windows со строчной буквы в документации по New-AzDataFactoryEncryptValue.</span><span class="sxs-lookup"><span data-stu-id="82d40-1596">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="82d40-1597">Пакет SDK ADF для .NET обновлен до версии 4.1.2.</span><span class="sxs-lookup"><span data-stu-id="82d40-1597">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="82d40-1598">Добавлены параметры DataProxyIntegrationRuntimeName, DataProxyStagingLinkedServiceName и DataProxyStagingPath в командлет Set-AzureRmDataFactoryV2IntegrationRuntime, что позволяет настраивать локальную среду выполнения интеграции в качестве прокси-сервера для Azure-SSIS Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="82d40-1598">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="82d40-1599">Обновлены PSTriggerRun для отображения активированных конвейеров, сообщений и свойств и PSActivityRun для отображения типа действия.</span><span class="sxs-lookup"><span data-stu-id="82d40-1599">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="82d40-1600">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="82d40-1600">Az.DataLakeStore</span></span>
* <span data-ttu-id="82d40-1601">Устранена проблема, при которой Get-DataLakeStoreDeletedItem переставал отвечать на запросы при возникновении ошибок или удаленных исключений.</span><span class="sxs-lookup"><span data-stu-id="82d40-1601">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="82d40-1602">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="82d40-1602">Az.EventHub</span></span>
* <span data-ttu-id="82d40-1603">Исправлена проблема № 9658: опечатка в написании параметра VirtualNteworkRule у Set-AzEventHubNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="82d40-1603">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="82d40-1604">Исправлена проблема № 9558: в Set-AzEventHubNamespace используется PATCH вместо PUT.</span><span class="sxs-lookup"><span data-stu-id="82d40-1604">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="82d40-1605">В командлет Set-AzEventHubNamespace добавлен параметр EnableKafka.</span><span class="sxs-lookup"><span data-stu-id="82d40-1605">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="82d40-1606">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="82d40-1606">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="82d40-1607">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="82d40-1607">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="82d40-1608">Исправлено написание Azure со строчной буквы.</span><span class="sxs-lookup"><span data-stu-id="82d40-1608">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="82d40-1609">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="82d40-1609">Az.Monitor</span></span>
* <span data-ttu-id="82d40-1610">Исправлены неправильные имена параметров в справочной документации.</span><span class="sxs-lookup"><span data-stu-id="82d40-1610">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82d40-1611">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82d40-1611">Az.Network</span></span>
* <span data-ttu-id="82d40-1612">Обновлен New-AzPrivateLinkServiceIpConfig.</span><span class="sxs-lookup"><span data-stu-id="82d40-1612">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="82d40-1613">Параметр PublicIpAddress объявлен нерекомендуемым, так как он не используется на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="82d40-1613">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="82d40-1614">Добавлен необязательный параметр Primary, указывающий, является ли текущая IP-конфигурация основной.</span><span class="sxs-lookup"><span data-stu-id="82d40-1614">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="82d40-1615">Улучшена обработка исключений из-за ошибок запроса от пакета SDK. Устранена проблема, при которой исключения пакета SDK не обрабатывались правильно, из-за чего не отображались основные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="82d40-1615">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="82d40-1616">Настроена логика проверки для префикса IPv6 IP-адреса для проверки правильности длины префикса IPv6.</span><span class="sxs-lookup"><span data-stu-id="82d40-1616">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="82d40-1617">Обновлен Get-AzVirtualNetworkSubnetConfig: добавлен набор параметров для получения по идентификатору ресурса подсети.</span><span class="sxs-lookup"><span data-stu-id="82d40-1617">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="82d40-1618">Обновлено описание параметра Location для AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="82d40-1618">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="82d40-1619">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="82d40-1619">Az.OperationalInsights</span></span>
* <span data-ttu-id="82d40-1620">Обновлена документация по New-AzOperationalInsightsLinuxSyslogDataSource.</span><span class="sxs-lookup"><span data-stu-id="82d40-1620">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="82d40-1621">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="82d40-1621">Added example</span></span>
    - <span data-ttu-id="82d40-1622">Обновлено описание параметра -Name.</span><span class="sxs-lookup"><span data-stu-id="82d40-1622">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="82d40-1623">Добавлен пример для New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="82d40-1623">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="82d40-1624">Изменено описание параметра -Name для New-AzOperationalInsightsWindowsEventDataSource.</span><span class="sxs-lookup"><span data-stu-id="82d40-1624">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="82d40-1625">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="82d40-1625">Az.RecoveryServices</span></span>
* <span data-ttu-id="82d40-1626">Обновлен Get-AzRecoveryServicesBackupJobDetail.md.</span><span class="sxs-lookup"><span data-stu-id="82d40-1626">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="82d40-1627">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82d40-1627">Az.Resources</span></span>
* <span data-ttu-id="82d40-1628">Добавлена поддержка новой версии API 2019-05-10 для Microsoft.Resource.</span><span class="sxs-lookup"><span data-stu-id="82d40-1628">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="82d40-1629">Добавлена поддержка copy.count = 0 для переменных, ресурсов и свойств.</span><span class="sxs-lookup"><span data-stu-id="82d40-1629">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="82d40-1630">Ресурсы, у которых condition = false или copy.count = 0, будут удаляться в полном режиме.</span><span class="sxs-lookup"><span data-stu-id="82d40-1630">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="82d40-1631">В справочную документацию добавлен пример назначения политики на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="82d40-1631">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="82d40-1632">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="82d40-1632">Az.ServiceBus</span></span>
* <span data-ttu-id="82d40-1633">Исправлена проблема № 9658: опечатка в написании параметра VirtualNetworkRule В Set-AzServiceBusNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="82d40-1633">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="82d40-1634">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="82d40-1634">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="82d40-1635">Добавлена новая команда Test-AzServiceBusNameAvailability для проверки доступности имени для очереди и раздела.</span><span class="sxs-lookup"><span data-stu-id="82d40-1635">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="82d40-1636">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="82d40-1636">Az.ServiceFabric</span></span>
* <span data-ttu-id="82d40-1637">Устранены ошибки командлета для добавления типа узла:</span><span class="sxs-lookup"><span data-stu-id="82d40-1637">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="82d40-1638">ошибка NullReferenceException, возникавшая, если у группы ресурсов были другие VMSS, не связанные с кластером Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="82d40-1638">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="82d40-1639">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8681.</span><span class="sxs-lookup"><span data-stu-id="82d40-1639">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="82d40-1640">Исправлена ошибка, из-за которой командлет завершился сбоем, если virtualNetwork находилась не в той группе ресурсов, к которой относится кластер.</span><span class="sxs-lookup"><span data-stu-id="82d40-1640">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="82d40-1641">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8407.</span><span class="sxs-lookup"><span data-stu-id="82d40-1641">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="82d40-1642">Командлет Add-AzServiceFabricApplicationCertificate объявлен нерекомендуемым.</span><span class="sxs-lookup"><span data-stu-id="82d40-1642">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="82d40-1643">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82d40-1643">Az.Sql</span></span>
* <span data-ttu-id="82d40-1644">Обновление документации по старым командлетам аудита.</span><span class="sxs-lookup"><span data-stu-id="82d40-1644">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="82d40-1645">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="82d40-1645">Az.Storage</span></span>
* <span data-ttu-id="82d40-1646">Обновлена справка по Get/Close-AzStorageFileHandle: в примеры добавлены сценарии использования командлетов и обновлено описание параметров.</span><span class="sxs-lookup"><span data-stu-id="82d40-1646">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="82d40-1647">Добавлена поддержка StandardBlobTier в операции отправки BLOB-объекта и копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="82d40-1647">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="82d40-1648">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="82d40-1648">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="82d40-1649">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="82d40-1649">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="82d40-1650">Добавлена поддержка приоритета восстановления в операцию копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="82d40-1650">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="82d40-1651">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="82d40-1651">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="82d40-1652">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="82d40-1652">Az.Websites</span></span>
* <span data-ttu-id="82d40-1653">Добавлены уточнение для параметра -AppSettings в Set-AzWebApp и Set-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="82d40-1653">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="82d40-1654">2.5.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="82d40-1654">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="82d40-1655">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="82d40-1655">Az.Accounts</span></span>
* <span data-ttu-id="82d40-1656">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="82d40-1656">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="82d40-1657">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="82d40-1657">Az.ApplicationInsights</span></span>
* <span data-ttu-id="82d40-1658">Исправлена опечатка в примере в документации по Remove-AzApplicationInsightsApiKey.</span><span class="sxs-lookup"><span data-stu-id="82d40-1658">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="82d40-1659">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="82d40-1659">Az.Automation</span></span>
* <span data-ttu-id="82d40-1660">Исправлена опечатка в строке ресурса.</span><span class="sxs-lookup"><span data-stu-id="82d40-1660">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="82d40-1661">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="82d40-1661">Az.CognitiveServices</span></span>
* <span data-ttu-id="82d40-1662">Добавлена поддержка NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="82d40-1662">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82d40-1663">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82d40-1663">Az.Compute</span></span>
* <span data-ttu-id="82d40-1664">Добавлены недостающие свойства (ComputerName, OsName, OsVersion и HyperVGeneration) для объекта представления экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="82d40-1664">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="82d40-1665">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="82d40-1665">Az.ContainerRegistry</span></span>
* <span data-ttu-id="82d40-1666">Исправлена опечатка в Remove-AzContainerRegistryReplication для параметра репликации.</span><span class="sxs-lookup"><span data-stu-id="82d40-1666">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="82d40-1667">См. подробнее: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="82d40-1667">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="82d40-1668">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="82d40-1668">Az.DataFactory</span></span>
* <span data-ttu-id="82d40-1669">Пакет SDK для ADF .NET обновлен до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="82d40-1669">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="82d40-1670">Исправлена опечатка в документации по Get-AzDataFactoryV2PipelineRun.</span><span class="sxs-lookup"><span data-stu-id="82d40-1670">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="82d40-1671">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="82d40-1671">Az.EventHub</span></span>
* <span data-ttu-id="82d40-1672">Добавлен новый командлет для создания маркера SAS: New-AzEventHubAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="82d40-1672">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="82d40-1673">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="82d40-1673">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="82d40-1674">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="82d40-1674">Az.KeyVault</span></span>
* <span data-ttu-id="82d40-1675">Добавлена поддержка для настройки параметра KeySize в политиках сертификатов.</span><span class="sxs-lookup"><span data-stu-id="82d40-1675">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="82d40-1676">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="82d40-1676">Az.LogicApp</span></span>
* <span data-ttu-id="82d40-1677">Get-AzIntegrationAccountMap теперь надлежащим образом выводит все типы сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="82d40-1677">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="82d40-1678">Добавлен новый параметр MapType для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="82d40-1678">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="82d40-1679">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="82d40-1679">Az.ManagedServices</span></span>
* <span data-ttu-id="82d40-1680">Добавлена поддержка API версии 2019-06-01 (общедоступная).</span><span class="sxs-lookup"><span data-stu-id="82d40-1680">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82d40-1681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82d40-1681">Az.Network</span></span>
* <span data-ttu-id="82d40-1682">Добавлена поддержка частной конечной точки и службы приватного канала.</span><span class="sxs-lookup"><span data-stu-id="82d40-1682">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="82d40-1683">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="82d40-1683">New cmdlets</span></span>
        - <span data-ttu-id="82d40-1684">Set-AzPrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="82d40-1684">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="82d40-1685">Set-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="82d40-1685">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="82d40-1686">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="82d40-1686">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="82d40-1687">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="82d40-1687">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="82d40-1688">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="82d40-1688">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="82d40-1689">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="82d40-1689">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="82d40-1690">Test-AzPrivateLinkServiceVisibility.</span><span class="sxs-lookup"><span data-stu-id="82d40-1690">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="82d40-1691">Get-AzAutoApprovedPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="82d40-1691">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="82d40-1692">Обновлены следующие команды для функции: Флаг PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies в подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="82d40-1692">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="82d40-1693">Обновлены командлеты New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig.</span><span class="sxs-lookup"><span data-stu-id="82d40-1693">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="82d40-1694">Добавлен необязательный параметр -PrivateEndpointNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к частной конечной точке в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="82d40-1694">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="82d40-1695">Добавлен необязательный параметр -PrivateLinkServiceNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к службе приватного канала в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="82d40-1695">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="82d40-1696">Параметр ServiceName командлета AzPrivateLinkService был переименован на Name с псевдонимом ServiceName для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="82d40-1696">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="82d40-1697">Включен протокол ICMP для настройки правил безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="82d40-1697">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="82d40-1698">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="82d40-1698">Updated cmdlets</span></span>
        - <span data-ttu-id="82d40-1699">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="82d40-1699">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="82d40-1700">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="82d40-1700">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="82d40-1701">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="82d40-1701">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="82d40-1702">Добавлен ConnectionProtocolType (Ikev1/Ikev2) в качестве настраиваемого параметра для командлета New-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="82d40-1702">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="82d40-1703">Добавлен PrivateIpAddressVersion в LoadBalancerFrontendIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="82d40-1703">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="82d40-1704">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="82d40-1704">Updated cmdlet:</span></span>
        - <span data-ttu-id="82d40-1705">New-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="82d40-1705">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="82d40-1706">Add-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="82d40-1706">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="82d40-1707">Set-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="82d40-1707">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="82d40-1708">Команда New-AzApplicationGatewayProbeConfig Шлюза приложений обновлена для поддержки настраиваемого порта в зонде.</span><span class="sxs-lookup"><span data-stu-id="82d40-1708">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="82d40-1709">Обновлен командлет New-AzApplicationGatewayProbeConfig: добавлен необязательный параметр Port, который используется при проверке внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="82d40-1709">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="82d40-1710">Этот параметр применяется к номерам SKU Standard_V2 и WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="82d40-1710">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="82d40-1711">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="82d40-1711">Az.OperationalInsights</span></span>
* <span data-ttu-id="82d40-1712">Обновленная версия по умолчанию для сохраненных операций поиска имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="82d40-1712">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="82d40-1713">Исправлены ошибки при обработке регулярных выражений со значениями NULL в журналах.</span><span class="sxs-lookup"><span data-stu-id="82d40-1713">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="82d40-1714">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="82d40-1714">Az.RecoveryServices</span></span>
* <span data-ttu-id="82d40-1715">Обновлен файл Get-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="82d40-1715">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="82d40-1716">Обновлен файл Get-AzRecoveryServicesBackupContainer.md.</span><span class="sxs-lookup"><span data-stu-id="82d40-1716">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="82d40-1717">Обновлен файл Get-AzRecoveryServicesVault.md.</span><span class="sxs-lookup"><span data-stu-id="82d40-1717">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="82d40-1718">Обновлен файл Wait-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="82d40-1718">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="82d40-1719">Обновлен файл Set-AzRecoveryServicesVaultContext.md.</span><span class="sxs-lookup"><span data-stu-id="82d40-1719">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="82d40-1720">Обновлен файл Get-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="82d40-1720">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="82d40-1721">Обновлен файл Get-AzRecoveryServicesBackupRecoveryPoint.md.</span><span class="sxs-lookup"><span data-stu-id="82d40-1721">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="82d40-1722">Обновлен файл Restore-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="82d40-1722">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="82d40-1723">Обновлен вызов службы для отмены регистрации контейнера в общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-1723">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="82d40-1724">Обновлен файл Set-AzRecoveryServicesAsrAlertSetting.md.</span><span class="sxs-lookup"><span data-stu-id="82d40-1724">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="82d40-1725">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82d40-1725">Az.Resources</span></span>
- <span data-ttu-id="82d40-1726">Удален отсутствующий командлет, который упоминается в документации по New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="82d40-1726">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="82d40-1727">Обновлены командлеты политик для использования новой версии API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="82d40-1727">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="82d40-1728">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="82d40-1728">Az.ServiceBus</span></span>
* <span data-ttu-id="82d40-1729">Добавлен новый командлет для создания маркера SAS: New-AzServiceBusAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="82d40-1729">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="82d40-1730">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="82d40-1730">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="82d40-1731">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82d40-1731">Az.Sql</span></span>
* <span data-ttu-id="82d40-1732">Исправлены отсутствующие примеры для командлета Set-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="82d40-1732">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="82d40-1733">Исправлены заданные повторяющиеся проверки для оценки наличия уязвимостей без указания адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="82d40-1733">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="82d40-1734">Исправлена незначительная опечатка в сообщении предупреждения.</span><span class="sxs-lookup"><span data-stu-id="82d40-1734">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="82d40-1735">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="82d40-1735">Az.Storage</span></span>
* <span data-ttu-id="82d40-1736">Обновлен пример в справочной документации для использования командлетом Get-AzStorageAccount правильного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="82d40-1736">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="82d40-1737">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="82d40-1737">Az.StorageSync</span></span>
* <span data-ttu-id="82d40-1738">Добавлен командлет Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="82d40-1738">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="82d40-1739">Исправлена проблема № 9551, связанная с TierFilesOlderThanDays.</span><span class="sxs-lookup"><span data-stu-id="82d40-1739">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="82d40-1740">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="82d40-1740">Az.Websites</span></span>
* <span data-ttu-id="82d40-1741">Исправлена ошибка, при которой некоторые свойства SiteConfig не возвращались Get-AzWebApp и Set-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="82d40-1741">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="82d40-1742">Добавлен новый параметр Location в Get-AzDeletedWebApp и Restore-AzDeletedWebApp.</span><span class="sxs-lookup"><span data-stu-id="82d40-1742">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="82d40-1743">Исправлена ошибка, которая возникала при клонировании слотов веб-приложений с помощью командлета New-AzWebApp-IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="82d40-1743">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="82d40-1744">2.4.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="82d40-1744">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="82d40-1745">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="82d40-1745">Az.Accounts</span></span>
* <span data-ttu-id="82d40-1746">Добавлена поддержка командлетов профиля.</span><span class="sxs-lookup"><span data-stu-id="82d40-1746">Add support for profile cmdlets</span></span>
* <span data-ttu-id="82d40-1747">Добавлена поддержка сред и плоскостей данных в созданных командлетах.</span><span class="sxs-lookup"><span data-stu-id="82d40-1747">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="82d40-1748">Исправлена ошибка, когда в командлетах плоскости данных в Windows PowerShell в некоторых случаях использовалась неправильная конечная точка.</span><span class="sxs-lookup"><span data-stu-id="82d40-1748">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="82d40-1749">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="82d40-1749">Az.Advisor</span></span>
* <span data-ttu-id="82d40-1750">Выпущена общедоступная версия Az.Advisor.</span><span class="sxs-lookup"><span data-stu-id="82d40-1750">GA release of Az.Advisor</span></span>
* <span data-ttu-id="82d40-1751">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="82d40-1751">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="82d40-1752">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="82d40-1752">Az.ApiManagement</span></span>
* <span data-ttu-id="82d40-1753">исправлена проблема https://github.com/Azure/azure-powershell/issues/8671.</span><span class="sxs-lookup"><span data-stu-id="82d40-1753">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="82d40-1754">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="82d40-1754">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="82d40-1755">Добавлена поддержка запрашивания подписок по пользователю и продукту.</span><span class="sxs-lookup"><span data-stu-id="82d40-1755">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="82d40-1756">Добавлена поддержка создания запросов с использованием области "/", "/apis", "/apis/echo-api".</span><span class="sxs-lookup"><span data-stu-id="82d40-1756">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="82d40-1757">Исправлены проблемы https://github.com/Azure/azure-powershell/issues/9307 и https://github.com/Azure/azure-powershell/issues/8432.</span><span class="sxs-lookup"><span data-stu-id="82d40-1757">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="82d40-1758">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="82d40-1758">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="82d40-1759">Добавлена поддержка указания ApiVersion и ApiVersionSetId при импорте API-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="82d40-1759">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="82d40-1760">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="82d40-1760">Az.Automation</span></span>
* <span data-ttu-id="82d40-1761">Исправлена ошибка командлета Set-AzAutomationConnectionFieldValue при обработке строкового значения.</span><span class="sxs-lookup"><span data-stu-id="82d40-1761">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82d40-1762">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82d40-1762">Az.Compute</span></span>
* <span data-ttu-id="82d40-1763">В New AzImageConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="82d40-1763">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="82d40-1764">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="82d40-1764">Az.DataFactory</span></span>
* <span data-ttu-id="82d40-1765">Обновление выходных данных командлетов ADF, предназначенных для получения числа выполнений действий, конвейеров и триггеров, для поддержки канала Select-Object.</span><span class="sxs-lookup"><span data-stu-id="82d40-1765">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="82d40-1766">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="82d40-1766">Az.EventGrid</span></span>
* <span data-ttu-id="82d40-1767">Исправлена опечатка в документации по командлету New-AzEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="82d40-1767">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="82d40-1768">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="82d40-1768">Az.IotHub</span></span>
* <span data-ttu-id="82d40-1769">Добавлена поддержка повторного создания ключей политики авторизации.</span><span class="sxs-lookup"><span data-stu-id="82d40-1769">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82d40-1770">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82d40-1770">Az.Network</span></span>
* <span data-ttu-id="82d40-1771">К тегам общедоступного IP-адреса добавлен тег RoutingPreference.</span><span class="sxs-lookup"><span data-stu-id="82d40-1771">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="82d40-1772">Улучшены примеры для справочной документации по командлету Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="82d40-1772">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="82d40-1773">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="82d40-1773">Az.PolicyInsights</span></span>
* <span data-ttu-id="82d40-1774">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="82d40-1774">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="82d40-1775">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9446.</span><span class="sxs-lookup"><span data-stu-id="82d40-1775">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="82d40-1776">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="82d40-1776">Az.OperationalInsights</span></span>
* <span data-ttu-id="82d40-1777">Исправленная модель источника данных CustomLog возвращена в командлет Get-AzOperationalInsightsDataSource.</span><span class="sxs-lookup"><span data-stu-id="82d40-1777">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="82d40-1778">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="82d40-1778">Az.RecoveryServices</span></span>
* <span data-ttu-id="82d40-1779">Выпущено исправление для команды get-policy для виртуальных машин IaaS.</span><span class="sxs-lookup"><span data-stu-id="82d40-1779">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="82d40-1780">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82d40-1780">Az.Resources</span></span>
    - <span data-ttu-id="82d40-1781">Исправлен текст справки по параметру Get-AzPolicyState -Top.</span><span class="sxs-lookup"><span data-stu-id="82d40-1781">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="82d40-1782">Добавлена поддержка разбиения по страницам на стороне клиента для Get-AzPolicyAlias.</span><span class="sxs-lookup"><span data-stu-id="82d40-1782">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="82d40-1783">Добавлены новые параметры для Set-AzPolicyAssignment, -PolicyParameters и -PolicyParametersObject.</span><span class="sxs-lookup"><span data-stu-id="82d40-1783">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="82d40-1784">Добавлен ряд обновлений документов и примеров для командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="82d40-1784">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="82d40-1785">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="82d40-1785">Az.ServiceBus</span></span>
* <span data-ttu-id="82d40-1786">Исправление ошибки № 4938: командлет New-AzureRmServiceBusQueue возвращает ответ BadRequest (Недопустимый запрос) при задании значения MaxSizeInMegabytes.</span><span class="sxs-lookup"><span data-stu-id="82d40-1786">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="82d40-1787">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82d40-1787">Az.Sql</span></span>
* <span data-ttu-id="82d40-1788">Из выпуска предварительной версии в выпуск общедоступной версии добавлены командлеты группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="82d40-1788">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="82d40-1789">Поддержка аудита Azure SQL Server и баз данных с помощью новых командлетов:</span><span class="sxs-lookup"><span data-stu-id="82d40-1789">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="82d40-1790">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="82d40-1790">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="82d40-1791">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="82d40-1791">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="82d40-1792">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="82d40-1792">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="82d40-1793">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="82d40-1793">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="82d40-1794">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="82d40-1794">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="82d40-1795">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="82d40-1795">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="82d40-1796">Из параметров оценки уязвимостей удалены ограничения, касающиеся электронной почты.</span><span class="sxs-lookup"><span data-stu-id="82d40-1796">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="82d40-1797">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="82d40-1797">Az.Storage</span></span>
* <span data-ttu-id="82d40-1798">Два параметра в указанном ниже командлете — -IndexDocument и -ErrorDocument404Path, — которые ранее были обязательными, стали необязательными:</span><span class="sxs-lookup"><span data-stu-id="82d40-1798">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="82d40-1799">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="82d40-1799">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="82d40-1800">Обновлена справка по командлету Get-AzStorageBlobContent: добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="82d40-1800">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="82d40-1801">При сбое выполнения командлета с ошибкой StorageException отображаются дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="82d40-1801">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="82d40-1802">Добавлена поддержка создания или обновления учетной записи хранения с использованием проверки подлинности AAD DS для службы "Файлы Azure".</span><span class="sxs-lookup"><span data-stu-id="82d40-1802">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="82d40-1803">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="82d40-1803">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="82d40-1804">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="82d40-1804">Set-AzStorageAccount</span></span>
* <span data-ttu-id="82d40-1805">Добавлена поддержка перечисления или закрытия дескрипторов файлов для общей папки, каталога файлов или файла:</span><span class="sxs-lookup"><span data-stu-id="82d40-1805">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="82d40-1806">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="82d40-1806">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="82d40-1807">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="82d40-1807">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="82d40-1808">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="82d40-1808">Az.StorageSync</span></span>
* <span data-ttu-id="82d40-1809">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="82d40-1809">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="82d40-1810">2.3.2 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="82d40-1810">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="82d40-1811">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="82d40-1811">Az.Accounts</span></span>
* <span data-ttu-id="82d40-1812">Исправлена ошибка, связанная с использованием неправильного URL-адреса для вызовов функций.</span><span class="sxs-lookup"><span data-stu-id="82d40-1812">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="82d40-1813">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8983.</span><span class="sxs-lookup"><span data-stu-id="82d40-1813">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="82d40-1814">Устранена проблема с псевдонимами из AzureRM для командлетов Az.</span><span class="sxs-lookup"><span data-stu-id="82d40-1814">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="82d40-1815">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="82d40-1815">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="82d40-1816">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest.</span><span class="sxs-lookup"><span data-stu-id="82d40-1816">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82d40-1817">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82d40-1817">Az.Compute</span></span>
* <span data-ttu-id="82d40-1818">Простые наборы параметров New-AzVm и New-AzVmss теперь принимают параметр ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="82d40-1818">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="82d40-1819">Исправлена опечатка в справочной документации по New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="82d40-1819">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="82d40-1820">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="82d40-1820">Az.Dns</span></span>
* <span data-ttu-id="82d40-1821">Исправлена опечатка в справочных примерах по использованию Set-AzDnsZone.</span><span class="sxs-lookup"><span data-stu-id="82d40-1821">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="82d40-1822">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="82d40-1822">Az.EventGrid</span></span>
* <span data-ttu-id="82d40-1823">Обновлен для использования API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="82d40-1823">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="82d40-1824">Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="82d40-1824">New cmdlets:</span></span>
    - <span data-ttu-id="82d40-1825">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="82d40-1825">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="82d40-1826">Создает домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-1826">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="82d40-1827">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="82d40-1827">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="82d40-1828">Возвращает сведения о домене Сетки событий или список всех доменов Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-1828">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="82d40-1829">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="82d40-1829">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="82d40-1830">Удаляет домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-1830">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="82d40-1831">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="82d40-1831">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="82d40-1832">Повторно создает ключ общего доступа для домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-1832">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="82d40-1833">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="82d40-1833">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="82d40-1834">Возвращает ключи общего доступа, используемые для публикации событий в домене Сетки событий.</span><span class="sxs-lookup"><span data-stu-id="82d40-1834">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="82d40-1835">New-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="82d40-1835">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="82d40-1836">Создает раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-1836">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="82d40-1837">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="82d40-1837">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="82d40-1838">Возвращает сведения о разделе домена Сетки событий или список всех разделов определенного домена Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-1838">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="82d40-1839">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="82d40-1839">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="82d40-1840">Удаляет раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-1840">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="82d40-1841">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="82d40-1841">Updated cmdlets:</span></span>
    - <span data-ttu-id="82d40-1842">New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="82d40-1842">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="82d40-1843">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для нового домена Сетки событий и раздела домена Сетки событий и позволяющие создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="82d40-1843">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="82d40-1844">Добавляют новые обязательные параметры для указания имени нового домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="82d40-1844">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="82d40-1845">Добавляют новые наборы параметров для доменов и разделов домена и позволяют повторно использовать существующие параметры (например, EndPointType, SubjectBeginsWith и т. д.).</span><span class="sxs-lookup"><span data-stu-id="82d40-1845">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="82d40-1846">Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="82d40-1846">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="82d40-1847">срока действия подписки на событие;</span><span class="sxs-lookup"><span data-stu-id="82d40-1847">Event subscription expiration date,</span></span>
            - <span data-ttu-id="82d40-1848">параметров расширенной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="82d40-1848">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="82d40-1849">Добавляют новое перечисление для ServiceBusQueue в качестве места назначения.</span><span class="sxs-lookup"><span data-stu-id="82d40-1849">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="82d40-1850">Запрещают использование значение All в параметре -IncludedEventType и заменяют его следующим:</span><span class="sxs-lookup"><span data-stu-id="82d40-1850">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="82d40-1851">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="82d40-1851">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="82d40-1852">Добавляют новые необязательные параметры (Top, ODataQuery и NextLink) для поддержки разбиения на страницы и фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="82d40-1852">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="82d40-1853">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="82d40-1853">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="82d40-1854">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для домена Сетки событий и раздела домена Сетки событий и позволяющие удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="82d40-1854">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="82d40-1855">Добавляют новые обязательные параметры для указания имени домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="82d40-1855">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="82d40-1856">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="82d40-1856">Az.FrontDoor</span></span>
* <span data-ttu-id="82d40-1857">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="82d40-1857">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="82d40-1858">Добавляет поддержку преобразований и новое значение оператора автозавершения (RegEx).</span><span class="sxs-lookup"><span data-stu-id="82d40-1858">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="82d40-1859">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="82d40-1859">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="82d40-1860">Добавляет новые значения автозавершения.</span><span class="sxs-lookup"><span data-stu-id="82d40-1860">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82d40-1861">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82d40-1861">Az.Network</span></span>
* <span data-ttu-id="82d40-1862">Добавляет поддержку ресурса шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="82d40-1862">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="82d40-1863">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="82d40-1863">New cmdlets</span></span>
        - <span data-ttu-id="82d40-1864">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="82d40-1864">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="82d40-1865">Добавляет AvailablePrivateEndpointType.</span><span class="sxs-lookup"><span data-stu-id="82d40-1865">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="82d40-1866">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="82d40-1866">New cmdlets</span></span>
        - <span data-ttu-id="82d40-1867">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="82d40-1867">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="82d40-1868">Добавляет PrivatePrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="82d40-1868">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="82d40-1869">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="82d40-1869">New cmdlets</span></span>
        - <span data-ttu-id="82d40-1870">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="82d40-1870">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="82d40-1871">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="82d40-1871">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="82d40-1872">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="82d40-1872">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="82d40-1873">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="82d40-1873">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="82d40-1874">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="82d40-1874">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="82d40-1875">Добавляет PrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="82d40-1875">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="82d40-1876">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="82d40-1876">New cmdlets</span></span>
        - <span data-ttu-id="82d40-1877">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="82d40-1877">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="82d40-1878">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="82d40-1878">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="82d40-1879">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="82d40-1879">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="82d40-1880">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="82d40-1880">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="82d40-1881">Обновлены следующие команды для функции: флаг UseLocalAzureIpAddress для VPN-подключения.</span><span class="sxs-lookup"><span data-stu-id="82d40-1881">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="82d40-1882">Обновлен командлет New-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="82d40-1882">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="82d40-1883">Обновлен командлет Set-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="82d40-1883">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="82d40-1884">В пиринг ExpressRoute добавлено поле только для чтения PeeredConnections.</span><span class="sxs-lookup"><span data-stu-id="82d40-1884">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="82d40-1885">В ExpressRoute добавлено поле только для чтения GlobalReachEnabled.</span><span class="sxs-lookup"><span data-stu-id="82d40-1885">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="82d40-1886">Добавлен атрибут в рамках критического изменения, отменяющего статус устаревшего поля AllowGlobalReach в модели ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="82d40-1886">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="82d40-1887">Исправлена проблема, связанная с ошибкой 8756, при использовании TargetListenerID с командлетами AzApplicationGatewayRedirectConfiguration.</span><span class="sxs-lookup"><span data-stu-id="82d40-1887">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="82d40-1888">Исправлена ошибка в New-AzApplicationGatewayPathRuleConfig, не позволявшая задавать набор правил повторного создания.</span><span class="sxs-lookup"><span data-stu-id="82d40-1888">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="82d40-1889">Исправлено отображение VirtualNetworkTaps в NetworkInterfaceIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="82d40-1889">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="82d40-1890">Исправлены командлеты Cortex Get для отображения всех частей.</span><span class="sxs-lookup"><span data-stu-id="82d40-1890">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="82d40-1891">Исправлено создание ссылок VirtualHub для ExpressRouteGateways и VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="82d40-1891">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="82d40-1892">В AzureFirewall и NatGateway добавлена поддержка Зон доступности.</span><span class="sxs-lookup"><span data-stu-id="82d40-1892">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="82d40-1893">Добавлен командлет Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="82d40-1893">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="82d40-1894">Добавлена поддержка нескольких общедоступных IP-адресов для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-1894">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="82d40-1895">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="82d40-1895">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="82d40-1896">Добавлен параметр -PublicIpAddress, который принимает один или несколько объектов общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="82d40-1896">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="82d40-1897">Добавлен параметр -VirtualNetwork, который принимает объект виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="82d40-1897">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="82d40-1898">Добавлены методы AddPublicIpAddress и RemovePublicIpAddress для объекта брандмауэра. Они принимают объект общедоступного IP-адреса в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="82d40-1898">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="82d40-1899">Не рекомендуется использовать параметры -PublicIpName и -VirtualNetworkName.</span><span class="sxs-lookup"><span data-stu-id="82d40-1899">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="82d40-1900">Обновлены следующие команды для функции: В параметрах проверки подлинности AAD VPN-клиента задан ресурс шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="82d40-1900">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="82d40-1901">Обновлен командлет New-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="82d40-1901">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="82d40-1902">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="82d40-1902">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="82d40-1903">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр-переключатель RemoveAadAuthentication для удаления в шлюзе параметров проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="82d40-1903">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="82d40-1904">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="82d40-1904">Az.OperationalInsights</span></span>
* <span data-ttu-id="82d40-1905">Добавлена поддержка SKU **pergb2018** в команде New-AzureRmOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="82d40-1905">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="82d40-1906">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82d40-1906">Az.Resources</span></span>
* <span data-ttu-id="82d40-1907">Поддержка дополнительных вариантов экспорта шаблона.</span><span class="sxs-lookup"><span data-stu-id="82d40-1907">Support for additional Template Export options</span></span>
    - <span data-ttu-id="82d40-1908">В Export-AzResourceGroup добавлен параметр -SkipResourceNameParameterization.</span><span class="sxs-lookup"><span data-stu-id="82d40-1908">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="82d40-1909">В Export-AzResourceGroup добавлен параметр -SkipAllParameterization.</span><span class="sxs-lookup"><span data-stu-id="82d40-1909">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="82d40-1910">В Export-AzResourceGroup добавлен параметр -Resource для фильтрации экспортированных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="82d40-1910">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="82d40-1911">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="82d40-1911">Az.ServiceFabric</span></span>
* <span data-ttu-id="82d40-1912">Исправлена ошибка, связанная с получением иногда неправильных отпечатков при добавлении сертификата ByExistingKeyVault.</span><span class="sxs-lookup"><span data-stu-id="82d40-1912">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="82d40-1913">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82d40-1913">Az.Sql</span></span>
* <span data-ttu-id="82d40-1914">Исправлен суффикс конечной точки хранилища службы "Расширенная защита от угроз Azure".</span><span class="sxs-lookup"><span data-stu-id="82d40-1914">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="82d40-1915">Исправлена ошибка, связанная с возможностью пакета "Расширенная защита данных" переопределять политику службы "Расширенная защита от угроз".</span><span class="sxs-lookup"><span data-stu-id="82d40-1915">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="82d40-1916">Новые командлеты для Management.Sql позволяют клиентам добавлять ключи TDE и задавать средство защиты TDE для управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="82d40-1916">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="82d40-1917">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="82d40-1917">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="82d40-1918">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="82d40-1918">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="82d40-1919">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="82d40-1919">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="82d40-1920">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="82d40-1920">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="82d40-1921">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="82d40-1921">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="82d40-1922">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="82d40-1922">Az.Storage</span></span>
* <span data-ttu-id="82d40-1923">Поддержка класса Kind в FileStorage и значения Premium_ZRS в SkuName при создании учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="82d40-1923">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="82d40-1924">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="82d40-1924">New-AzStorageAccount</span></span>
* <span data-ttu-id="82d40-1925">Уточнено описание командлета неизменности BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="82d40-1925">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="82d40-1926">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="82d40-1926">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="82d40-1927">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="82d40-1927">Az.Websites</span></span>
* <span data-ttu-id="82d40-1928">Оптимизирует Get-AzWebAppCertificate для фильтрации по группе ресурсов на сервере, а не в клиенте.</span><span class="sxs-lookup"><span data-stu-id="82d40-1928">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="82d40-1929">Добавляет параметр-переключатель - UseDisasterRecovery в Get AzWebAppSnapshot.</span><span class="sxs-lookup"><span data-stu-id="82d40-1929">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="82d40-1930">2.2.0 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="82d40-1930">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="82d40-1931">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="82d40-1931">Az.Cdn</span></span>
* <span data-ttu-id="82d40-1932">Обновлены командлеты для поддержки функции rulesEngine на основе API версии 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="82d40-1932">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82d40-1933">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82d40-1933">Az.Compute</span></span>
* <span data-ttu-id="82d40-1934">Добавлен параметр `NoWait`, который запускает операцию и немедленно возвращает значение еще до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="82d40-1934">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="82d40-1935">Обновлены командлеты:   Export-AzLogAnalyticRequestRateByInterval; Export-AzLogAnalyticThrottledRequest; Remove-AzVM; Remove-AzVMAccessExtension; Remove-AzVMAEMExtension; Remove-AzVMChefExtension; Remove-AzVMCustomScriptExtension; Remove-AzVMDiagnosticsExtension; Remove-AzVMDiskEncryptionExtension; Remove-AzVMDscExtension; Remove-AzVMSqlServerExtension; Restart-AzVM; Set-AzVM; Set-AzVMAccessExtension; Set-AzVMADDomainExtension; Set-AzVMAEMExtension; Set-AzVMBginfoExtension; Set-AzVMChefExtension; Set-AzVMCustomScriptExtension; Set-AzVMDiagnosticsExtension; Set-AzVMDscExtension; Set-AzVMExtension; Start-AzVM; Stop-AzVM; Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="82d40-1935">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="82d40-1936">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="82d40-1936">Az.EventHub</span></span>
* <span data-ttu-id="82d40-1937">Исправлена ошибка № 9231. Командлет Get-AzEventHubNamespace не возвращал теги.</span><span class="sxs-lookup"><span data-stu-id="82d40-1937">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="82d40-1938">Исправлена ошибка № 9230. Командлет Get-AzEventHubNamespace возвращал значение ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="82d40-1938">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82d40-1939">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82d40-1939">Az.Network</span></span>
* <span data-ttu-id="82d40-1940">Обновлены параметры ResourceId и InputObject для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="82d40-1940">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="82d40-1941">Добавлены псевдонимы для параметров ResourceId и InputObject.</span><span class="sxs-lookup"><span data-stu-id="82d40-1941">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="82d40-1942">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="82d40-1942">Az.PolicyInsights</span></span>
* <span data-ttu-id="82d40-1943">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyEvent.</span><span class="sxs-lookup"><span data-stu-id="82d40-1943">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="82d40-1944">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="82d40-1944">Az.RecoveryServices</span></span>
* <span data-ttu-id="82d40-1945">Минимальный срок хранения политики IaaSVM изменился с 1 до 7 дней.</span><span class="sxs-lookup"><span data-stu-id="82d40-1945">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="82d40-1946">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="82d40-1946">Az.ServiceBus</span></span>
* <span data-ttu-id="82d40-1947">Исправлена ошибка № 9182. Командлет Get-AzServiceBusNamespace возвращал ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="82d40-1947">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="82d40-1948">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="82d40-1948">Az.ServiceFabric</span></span>
* <span data-ttu-id="82d40-1949">Исправлена опечатка в сообщении об ошибке для командлета Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="82d40-1949">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="82d40-1950">Добавлен отсутствующий символ в командных строках Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="82d40-1950">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="82d40-1951">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82d40-1951">Az.Sql</span></span>
* <span data-ttu-id="82d40-1952">Для командлета New-AzureSqlInstance добавлен параметр DnsZonePartner, обеспечивающий поддержку AutoDr для Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="82d40-1952">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="82d40-1953">Командлет Get-AzSqlDatabaseSecureConnectionPolicy объявлен неподдерживаемым.</span><span class="sxs-lookup"><span data-stu-id="82d40-1953">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="82d40-1954">Командлеты обнаружения угроз переименованы в командлеты Расширенной защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="82d40-1954">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="82d40-1955">Параметры -StorageSizeInGB и -LicenseType командлета New-AzSqlInstance теперь необязательны.</span><span class="sxs-lookup"><span data-stu-id="82d40-1955">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="82d40-1956">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="82d40-1956">Az.Websites</span></span>
* <span data-ttu-id="82d40-1957">Исправлены проблемы, когда удалялись теги при использовании Set-AzWebApp и Set-AzWebAppSlot со свойством -WebApp.</span><span class="sxs-lookup"><span data-stu-id="82d40-1957">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="82d40-1958">2.1.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="82d40-1958">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="82d40-1959">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="82d40-1959">Az.ApiManagement</span></span>
* <span data-ttu-id="82d40-1960">Созданы командлеты для управления диагностикой в глобальной области и в области API.</span><span class="sxs-lookup"><span data-stu-id="82d40-1960">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="82d40-1961">**Get-AzApiManagementDiagnostic** — получение диагностики, заданной глобально или на уровне области API.</span><span class="sxs-lookup"><span data-stu-id="82d40-1961">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="82d40-1962">**New-AzApiManagementDiagnostic** — создание диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="82d40-1962">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="82d40-1963">**New-AzApiManagementHttpMessageDiagnostic** — создание параметра диагностики, для которого регистрируются заголовки и размер байтов тела.</span><span class="sxs-lookup"><span data-stu-id="82d40-1963">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="82d40-1964">**New-AzApiManagementPipelineDiagnosticSetting** — создание параметров диагностики для сообщений HTTP, поступающих в шлюз или исходящих из него.</span><span class="sxs-lookup"><span data-stu-id="82d40-1964">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="82d40-1965">**New-AzApiManagementSamplingSetting** — создание параметра выборки для запросов и ответов касательно диагностики.</span><span class="sxs-lookup"><span data-stu-id="82d40-1965">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="82d40-1966">**Remove-AzApiManagementDiagnostic** — удаление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="82d40-1966">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="82d40-1967">**Set-AzApiManagementDiagnostic** — обновление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="82d40-1967">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="82d40-1968">Созданы командлеты для управления кэшем в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="82d40-1968">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="82d40-1969">**Get-AzApiManagementCache** — получение сведений о кэше, указанном идентификатором, или обо всех кэшах.</span><span class="sxs-lookup"><span data-stu-id="82d40-1969">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="82d40-1970">**New-AzApiManagementCache** — создание кэша по умолчанию или кэша в определенном регионе Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-1970">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="82d40-1971">**Remove-AzApiManagementCache** — удаление кэша.</span><span class="sxs-lookup"><span data-stu-id="82d40-1971">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="82d40-1972">**Update-AzApiManagementCache** — обновление кэша.</span><span class="sxs-lookup"><span data-stu-id="82d40-1972">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="82d40-1973">Созданы командлеты для управления схемой API.</span><span class="sxs-lookup"><span data-stu-id="82d40-1973">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="82d40-1974">**New-AzApiManagementSchema** — создание схемы для API.</span><span class="sxs-lookup"><span data-stu-id="82d40-1974">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="82d40-1975">**Get-AzApiManagementSchema** — получение схем, настроенных в API.</span><span class="sxs-lookup"><span data-stu-id="82d40-1975">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="82d40-1976">**Remove-AzApiManagementSchema** — удаление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="82d40-1976">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="82d40-1977">**Set-AzApiManagementSchema** — обновление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="82d40-1977">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="82d40-1978">Создан командлет для создания токена пользователя.</span><span class="sxs-lookup"><span data-stu-id="82d40-1978">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="82d40-1979">**New-AzApiManagementUserToken** — создание токена пользователя, по умолчанию действительного в течение 8 часов. С помощью этого командлета можно создавать токен для пользователя GIT.</span><span class="sxs-lookup"><span data-stu-id="82d40-1979">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="82d40-1980">Создан командлет для получения состояния сети.</span><span class="sxs-lookup"><span data-stu-id="82d40-1980">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="82d40-1981">**Get-AzApiManagementNetworkStatus** — получение состояния подключения сети ресурсов, от которых зависит служба "Управление API".</span><span class="sxs-lookup"><span data-stu-id="82d40-1981">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="82d40-1982">Это полезно при развертывании службы ApiManagement в виртуальной сети и проверке того, не нарушена ли какая-либо из зависимостей.</span><span class="sxs-lookup"><span data-stu-id="82d40-1982">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="82d40-1983">Обновлен командлет **New-AzApiManagement** для управления службой ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="82d40-1983">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="82d40-1984">Добавлена поддержка нового SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="82d40-1984">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="82d40-1985">Добавлена поддержка для включения флага EnableClientCertificate в SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="82d40-1985">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="82d40-1986">Новый командлет **New-AzApiManagementSslSetting** позволяет настраивать параметр TLS/SSL для сервера (Backend) и внешнего интерфейса (Frontend).</span><span class="sxs-lookup"><span data-stu-id="82d40-1986">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="82d40-1987">Его также можно использовать для настройки Ciphers как 3DES, в ServerProtocols как Http2 для внешнего интерфейса (Frontend) службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="82d40-1987">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="82d40-1988">Добавлена поддержка настройки имени узла DeveloperPortal в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="82d40-1988">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="82d40-1989">Обновлен командлет **Get-AzApiManagementSsoToken** для извлечения объекта PsApiManagement в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="82d40-1989">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="82d40-1990">Обновлен командлет для отображения встроенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="82d40-1990">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="82d40-1991">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Код ошибки: ValidationError. Сообщение об ошибке: "Некоторые поля содержат неправильные значения". Сведения об ошибке: [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="82d40-1991">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="82d40-1992">Обновлен командлет **Export-AzApiManagementApi** для экспортирования программных интерфейсов в формате OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="82d40-1992">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="82d40-1993">Обновлен командлет **Import-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="82d40-1993">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="82d40-1994">Для импортирования API из спецификации документа OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="82d40-1994">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="82d40-1995">Для переопределения свойства PsApiManagementSchema, указанного в любом документе (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="82d40-1995">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="82d40-1996">Для переопределения свойства ServiceUrl, указанного в любом документе.</span><span class="sxs-lookup"><span data-stu-id="82d40-1996">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="82d40-1997">Обновлен командлет **Get-AzApiManagementPolicy** для возврата политики в формате, экранированном не для XML, с использованием rawxml.</span><span class="sxs-lookup"><span data-stu-id="82d40-1997">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="82d40-1998">Обновлен командлет **Set-AzApiManagementPolicy**. Он принимает политику в формате, экранированном не для XML, с использованием rawxml и в формате, экранированном для XML, с использованием XML.</span><span class="sxs-lookup"><span data-stu-id="82d40-1998">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="82d40-1999">Обновлен командлет **New-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="82d40-1999">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="82d40-2000">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="82d40-2000">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="82d40-2001">Для создания API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="82d40-2001">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="82d40-2002">Для клонирования API с использованием значений SourceApiId и SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="82d40-2002">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="82d40-2003">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="82d40-2003">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="82d40-2004">Обновлен командлет **Set-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="82d40-2004">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="82d40-2005">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="82d40-2005">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="82d40-2006">Для обновления API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="82d40-2006">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="82d40-2007">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="82d40-2007">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="82d40-2008">Обновлен командлет **New-AzApiManagementRevision**:</span><span class="sxs-lookup"><span data-stu-id="82d40-2008">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="82d40-2009">Для клонирования (копирования тегов, продуктов, операций и политик) существующей редакции с использованием SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="82d40-2009">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="82d40-2010">Новая редакция предполагает родительский идентификатор ApiId.</span><span class="sxs-lookup"><span data-stu-id="82d40-2010">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="82d40-2011">Для предоставления ApiRevisionDescription.</span><span class="sxs-lookup"><span data-stu-id="82d40-2011">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="82d40-2012">Для переопределения значения ServiceUrl при клонировании API.</span><span class="sxs-lookup"><span data-stu-id="82d40-2012">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="82d40-2013">Обновлен командлет **New-AzApiManagementIdentityProvider**:</span><span class="sxs-lookup"><span data-stu-id="82d40-2013">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="82d40-2014">Для настройки AAD или AADB2C с Authority.</span><span class="sxs-lookup"><span data-stu-id="82d40-2014">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="82d40-2015">Для установки политик SignupPolicy, SigninPolicy, ProfileEditingPolicy и PasswordResetPolicy.</span><span class="sxs-lookup"><span data-stu-id="82d40-2015">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="82d40-2016">Обновлен командлет **New-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="82d40-2016">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="82d40-2017">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="82d40-2017">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="82d40-2018">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="82d40-2018">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="82d40-2019">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="82d40-2019">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="82d40-2020">Обновлен командлет **Set-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="82d40-2020">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="82d40-2021">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="82d40-2021">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="82d40-2022">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="82d40-2022">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="82d40-2023">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="82d40-2023">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="82d40-2024">Следующие командлеты обновлены, чтобы принимать значение ResourceId в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="82d40-2024">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="82d40-2025">New-AzApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="82d40-2025">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="82d40-2026">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="82d40-2026">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="82d40-2027">Get-AzApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="82d40-2027">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="82d40-2028">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="82d40-2028">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="82d40-2029">Get-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="82d40-2029">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="82d40-2030">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="82d40-2030">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="82d40-2031">Get-AzApiManagementAuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="82d40-2031">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="82d40-2032">Get-AzApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="82d40-2032">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="82d40-2033">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="82d40-2033">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="82d40-2034">Get-AzApiManagementCertificate.</span><span class="sxs-lookup"><span data-stu-id="82d40-2034">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="82d40-2035">Remove-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="82d40-2035">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="82d40-2036">Remove-AzApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="82d40-2036">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="82d40-2037">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="82d40-2037">Az.Automation</span></span>
* <span data-ttu-id="82d40-2038">Обновлен командлет Get-AzAutomationJobOutputRecord для обработки значений в формате JSON и в виде текстовой записи.</span><span class="sxs-lookup"><span data-stu-id="82d40-2038">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="82d40-2039">исправлена проблема https://github.com/Azure/azure-powershell/issues/7977.</span><span class="sxs-lookup"><span data-stu-id="82d40-2039">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="82d40-2040">исправлена проблема https://github.com/Azure/azure-powershell/issues/8600.</span><span class="sxs-lookup"><span data-stu-id="82d40-2040">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="82d40-2041">Поведение командлета Start-AzAutomationDscCompilationJob изменено так, чтобы сразу же запустить задание, а не ждать его завершения.</span><span class="sxs-lookup"><span data-stu-id="82d40-2041">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="82d40-2042">исправлена проблема https://github.com/Azure/azure-powershell/issues/8347.</span><span class="sxs-lookup"><span data-stu-id="82d40-2042">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="82d40-2043">Исправлен командлет Get-AzAutomationDscNode, возвращающий все узлы при использовании -Name.</span><span class="sxs-lookup"><span data-stu-id="82d40-2043">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="82d40-2044">Теперь он возвращает только соответствующий узел.</span><span class="sxs-lookup"><span data-stu-id="82d40-2044">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82d40-2045">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82d40-2045">Az.Compute</span></span>
* <span data-ttu-id="82d40-2046">Добавлены параметры ProtectFromScaleIn и ProtectFromScaleSetAction для командлета Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="82d40-2046">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="82d40-2047">Командлет New-AzVM с простым набором параметров теперь по умолчанию использует доступное расположение, если регион "восточная часть США" не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="82d40-2047">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="82d40-2048">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="82d40-2048">Az.DataLakeStore</span></span>
* <span data-ttu-id="82d40-2049">Обновлен пакет SDK ADLS для использования httpclient. В инфраструктуру Azure интегрирована проверка плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="82d40-2049">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="82d40-2050">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="82d40-2050">Az.Monitor</span></span>
* <span data-ttu-id="82d40-2051">Исправлены неправильные имена параметров в справочных примерах.</span><span class="sxs-lookup"><span data-stu-id="82d40-2051">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82d40-2052">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82d40-2052">Az.Network</span></span>
* <span data-ttu-id="82d40-2053">Добавлен флаг DisableBgpRoutePropagation для выходных данных действующей таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="82d40-2053">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="82d40-2054">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="82d40-2054">Updated cmdlet:</span></span>
        - <span data-ttu-id="82d40-2055">Get-AzEffectiveRouteTable.</span><span class="sxs-lookup"><span data-stu-id="82d40-2055">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="82d40-2056">Исправлен двойной дефис в документации New-AzApplicationGatewayTrustedRootCertificate.</span><span class="sxs-lookup"><span data-stu-id="82d40-2056">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="82d40-2057">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82d40-2057">Az.Resources</span></span>
* <span data-ttu-id="82d40-2058">Добавлен новый командлет Get-AzureRmDenyAssignment для получения запрещающих назначений.</span><span class="sxs-lookup"><span data-stu-id="82d40-2058">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="82d40-2059">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82d40-2059">Az.Sql</span></span>
* <span data-ttu-id="82d40-2060">Командлеты Расширенной защиты от угроз переименованы на командлеты Расширенной защиты данных, и оценка уязвимости включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="82d40-2060">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="82d40-2061">2.0.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="82d40-2061">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="82d40-2062">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="82d40-2062">Az.Accounts</span></span>
* <span data-ttu-id="82d40-2063">Обновлена библиотека аутентификации для устранения проблем с ADFS при использовании аутентификации на основе имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="82d40-2063">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="82d40-2064">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="82d40-2064">Az.CognitiveServices</span></span>
* <span data-ttu-id="82d40-2065">Отображается только заявление об отказе Bing для служб Поиска Bing.</span><span class="sxs-lookup"><span data-stu-id="82d40-2065">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="82d40-2066">Исправлена проблема с созданием учетной записи.</span><span class="sxs-lookup"><span data-stu-id="82d40-2066">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82d40-2067">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82d40-2067">Az.Compute</span></span>
* <span data-ttu-id="82d40-2068">Функция группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="82d40-2068">Proximity placement group feature.</span></span>
    - <span data-ttu-id="82d40-2069">Добавлены следующие новые командлеты:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="82d40-2069">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="82d40-2070">Новый параметр ProximityPlacementGroupId будет добавлен в следующие командлеты:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="82d40-2070">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="82d40-2071">В командлет New-AzGalleryImageVersion добавлен параметр StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="82d40-2071">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="82d40-2072">TargetRegion в командлете New-AzGalleryImageVersion может содержать StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="82d40-2072">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="82d40-2073">Параметр-переключатель SkipShutdown добавлен в командлеты Stop-AzVM и Stop-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="82d40-2073">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="82d40-2074">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="82d40-2074">Breaking changes</span></span>
    - <span data-ttu-id="82d40-2075">Командлет SET-AzVMBootDiagnostics изменен на Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="82d40-2075">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="82d40-2076">Командлет Export-AzLogAnalyticThrottledRequests изменен на Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="82d40-2076">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="82d40-2077">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="82d40-2077">Az.DeploymentManager</span></span>
* <span data-ttu-id="82d40-2078">Первая общедоступная версия командлетов диспетчера развертывания Azure</span><span class="sxs-lookup"><span data-stu-id="82d40-2078">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="82d40-2079">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="82d40-2079">Az.Dns</span></span>
* <span data-ttu-id="82d40-2080">Автоматическое делегирование DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="82d40-2080">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="82d40-2081">Командлет для создания зоны DNS принимает имя родительской зоны в качестве дополнительного необязательного параметра.</span><span class="sxs-lookup"><span data-stu-id="82d40-2081">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="82d40-2082">Он добавляет записи NS в родительской зоне для созданной дочерней зоны.</span><span class="sxs-lookup"><span data-stu-id="82d40-2082">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="82d40-2083">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="82d40-2083">Az.FrontDoor</span></span>
* <span data-ttu-id="82d40-2084">Первая общедоступная версия командлетов Azure FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="82d40-2084">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="82d40-2085">Переименованы командлеты WAF для включения Waf.</span><span class="sxs-lookup"><span data-stu-id="82d40-2085">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="82d40-2086">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="82d40-2086">Az.HDInsight</span></span>
* <span data-ttu-id="82d40-2087">Удалены два командлета:</span><span class="sxs-lookup"><span data-stu-id="82d40-2087">Removed two cmdlets:</span></span>
    - <span data-ttu-id="82d40-2088">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="82d40-2088">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="82d40-2089">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="82d40-2089">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="82d40-2090">Добавлен новый командлет Set-AzHDInsightGatewayCredential для замены Grant-AzHDInsightHttpServicesAccess.</span><span class="sxs-lookup"><span data-stu-id="82d40-2090">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="82d40-2091">Обновлен командлет Get-AzHDInsightJobOutput для различения ролей читателя и оператора HDInsight:</span><span class="sxs-lookup"><span data-stu-id="82d40-2091">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="82d40-2092">Пользователям с ролью читателя не нужно указывать параметр DefaultStorageAccountKey явным образом, иначе возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="82d40-2092">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="82d40-2093">На пользователей с ролью оператора HDInsight это не повлияет.</span><span class="sxs-lookup"><span data-stu-id="82d40-2093">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="82d40-2094">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="82d40-2094">Az.Monitor</span></span>
* <span data-ttu-id="82d40-2095">Новые командлеты для API SQR (запланированное правило запросов)</span><span class="sxs-lookup"><span data-stu-id="82d40-2095">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="82d40-2096">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="82d40-2096">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="82d40-2097">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="82d40-2097">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="82d40-2098">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="82d40-2098">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="82d40-2099">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="82d40-2099">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="82d40-2100">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="82d40-2100">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="82d40-2101">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="82d40-2101">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="82d40-2102">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="82d40-2102">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="82d40-2103">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="82d40-2103">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="82d40-2104">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="82d40-2104">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="82d40-2105">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="82d40-2105">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="82d40-2106">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="82d40-2106">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="82d40-2107">См. подробнее об [API SQR](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules).</span><span class="sxs-lookup"><span data-stu-id="82d40-2107">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="82d40-2108">Обновлен файл Az.Monitor.md для включения командлетов для правила генерации оповещений на основе метрик GenV2(не классическая версия).</span><span class="sxs-lookup"><span data-stu-id="82d40-2108">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82d40-2109">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82d40-2109">Az.Network</span></span>
* <span data-ttu-id="82d40-2110">Добавлена поддержка для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="82d40-2110">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="82d40-2111">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="82d40-2111">New cmdlets</span></span>
        - <span data-ttu-id="82d40-2112">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="82d40-2112">New-AzNatGateway</span></span>
        - <span data-ttu-id="82d40-2113">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="82d40-2113">Get-AzNatGateway</span></span>
        - <span data-ttu-id="82d40-2114">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="82d40-2114">Set-AzNatGateway</span></span>
        - <span data-ttu-id="82d40-2115">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="82d40-2115">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="82d40-2116">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="82d40-2116">Updated cmdlets</span></span>
        - <span data-ttu-id="82d40-2117">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="82d40-2117">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="82d40-2118">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="82d40-2118">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="82d40-2119">Обновлены следующие команды для функции: Настройка и удаление пользовательских маршрутов через шлюз в Бруклине.</span><span class="sxs-lookup"><span data-stu-id="82d40-2119">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="82d40-2120">Обновлен командлет New-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="82d40-2120">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="82d40-2121">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="82d40-2121">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="82d40-2122">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="82d40-2122">Az.PolicyInsights</span></span>
* <span data-ttu-id="82d40-2123">Добавлена поддержка сведений об оценке политики запросов.</span><span class="sxs-lookup"><span data-stu-id="82d40-2123">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="82d40-2124">Добавлен параметр -Expand в командлет Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="82d40-2124">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="82d40-2125">Добавлена поддержка -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="82d40-2125">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="82d40-2126">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="82d40-2126">Az.RecoveryServices</span></span>
* <span data-ttu-id="82d40-2127">Добавлена поддержка перекрестной подписки на Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="82d40-2127">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="82d40-2128">Добавлена возможность отмечать предстоящие критически важные изменения для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="82d40-2128">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="82d40-2129">Исправлены план восстановления и план действий для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="82d40-2129">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="82d40-2130">Исправлено сетевое сопоставление обновления Azure Site Recovery (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="82d40-2130">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="82d40-2131">Исправлено направление защиты обновления Azure Site Recovery для управляемых дисков (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="82d40-2131">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="82d40-2132">Добавлены другие незначительные исправления.</span><span class="sxs-lookup"><span data-stu-id="82d40-2132">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="82d40-2133">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="82d40-2133">Az.Relay</span></span>
* <span data-ttu-id="82d40-2134">Исправлены опечатки в сообщениях для клиентов.</span><span class="sxs-lookup"><span data-stu-id="82d40-2134">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="82d40-2135">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="82d40-2135">Az.ServiceBus</span></span>
* <span data-ttu-id="82d40-2136">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="82d40-2136">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="82d40-2137">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="82d40-2137">Az.Storage</span></span>
* <span data-ttu-id="82d40-2138">Выполнено обновление клиентской библиотеки хранилища до версии 10.0.1 (пространство имен всех объектов из этого пакета SDK изменено с Microsoft.WindowsAzure.Storage. *на Microsoft.Azure.Storage*).</span><span class="sxs-lookup"><span data-stu-id="82d40-2138">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="82d40-2139">Выполнено обновление до Microsoft.Azure.Management.Storage версии 11.0.0 для включения поддержки нового API версии 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="82d40-2139">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="82d40-2140">Значение свойства Kind по умолчанию в учетной записи хранения изменено со Storage на StorageV2.</span><span class="sxs-lookup"><span data-stu-id="82d40-2140">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="82d40-2141">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="82d40-2141">New-AzStorageAccount</span></span>
* <span data-ttu-id="82d40-2142">Изменено значение Sku.Name в выходных данных командлета учетной записи хранения в соответствии со значением Sku.Name во входных данных путем добавления _ (например, StandardLRS изменено на Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="82d40-2142">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="82d40-2143">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="82d40-2143">New-AzStorageAccount</span></span>
    - <span data-ttu-id="82d40-2144">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="82d40-2144">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="82d40-2145">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="82d40-2145">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="82d40-2146">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="82d40-2146">Az.Websites</span></span>
* <span data-ttu-id="82d40-2147">Свойство Kind теперь будет задаваться объектам PSSite, возвращаемым командлетом Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="82d40-2147">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="82d40-2148">Get-AzWebApp\*Metrics и Get-AzAppServicePlanMetrics считаются нерекомендуемыми.</span><span class="sxs-lookup"><span data-stu-id="82d40-2148">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="82d40-2149">1.8.0 — апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="82d40-2149">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="82d40-2150">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="82d40-2150">Highlights since the last major release</span></span>
* <span data-ttu-id="82d40-2151">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="82d40-2151">General availability of `Az` module</span></span>
* <span data-ttu-id="82d40-2152">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="82d40-2152">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="82d40-2153">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="82d40-2153">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="82d40-2154">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="82d40-2154">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="82d40-2155">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="82d40-2155">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="82d40-2156">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="82d40-2156">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="82d40-2157">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="82d40-2157">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="82d40-2158">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="82d40-2158">Az.Accounts</span></span>
* <span data-ttu-id="82d40-2159">Обновлен командлет Uninstall-AzureRm для правильного удаления модулей в Mac.</span><span class="sxs-lookup"><span data-stu-id="82d40-2159">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="82d40-2160">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="82d40-2160">Az.Batch</span></span>
* <span data-ttu-id="82d40-2161">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="82d40-2161">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="82d40-2162">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="82d40-2162">Az.Cdn</span></span>
* <span data-ttu-id="82d40-2163">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="82d40-2163">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="82d40-2164">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="82d40-2164">Az.CognitiveServices</span></span>
* <span data-ttu-id="82d40-2165">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="82d40-2165">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82d40-2166">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82d40-2166">Az.Compute</span></span>
* <span data-ttu-id="82d40-2167">Устранена проблема с установкой AEM, если в идентификаторах ресурсов дисков группа ресурсов указана в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="82d40-2167">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="82d40-2168">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="82d40-2168">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="82d40-2169">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="82d40-2169">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="82d40-2170">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="82d40-2170">Az.DataFactory</span></span>
* <span data-ttu-id="82d40-2171">Добавлены свойства SsisProperties, если NodeCount не имеет значения NULL для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="82d40-2171">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="82d40-2172">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="82d40-2172">Az.DataLakeStore</span></span>
* <span data-ttu-id="82d40-2173">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="82d40-2173">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="82d40-2174">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="82d40-2174">Az.EventGrid</span></span>
* <span data-ttu-id="82d40-2175">Обновлен текст справки для конечной точки, указывающий, что необходимо создать ресурсы, прежде чем использовать командлеты для создания или обновления подписки на события.</span><span class="sxs-lookup"><span data-stu-id="82d40-2175">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="82d40-2176">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="82d40-2176">Az.EventHub</span></span>
* <span data-ttu-id="82d40-2177">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="82d40-2177">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="82d40-2178">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="82d40-2178">Az.HDInsight</span></span>
* <span data-ttu-id="82d40-2179">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="82d40-2179">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="82d40-2180">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="82d40-2180">Az.IotHub</span></span>
* <span data-ttu-id="82d40-2181">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="82d40-2181">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="82d40-2182">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="82d40-2182">Az.KeyVault</span></span>
* <span data-ttu-id="82d40-2183">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="82d40-2183">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="82d40-2184">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="82d40-2184">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="82d40-2185">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="82d40-2185">Az.MachineLearning</span></span>
* <span data-ttu-id="82d40-2186">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="82d40-2186">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="82d40-2187">Az.Media</span><span class="sxs-lookup"><span data-stu-id="82d40-2187">Az.Media</span></span>
* <span data-ttu-id="82d40-2188">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="82d40-2188">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="82d40-2189">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="82d40-2189">Az.Monitor</span></span>
  * <span data-ttu-id="82d40-2190">Добавлены новые командлеты для правила генерации оповещений на основе метрик GenV2 (не классических).</span><span class="sxs-lookup"><span data-stu-id="82d40-2190">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="82d40-2191">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="82d40-2191">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="82d40-2192">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="82d40-2192">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="82d40-2193">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="82d40-2193">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="82d40-2194">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="82d40-2194">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="82d40-2195">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="82d40-2195">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="82d40-2196">Обновлен пакет SDK Monitor до предварительной версии 0.22.0.</span><span class="sxs-lookup"><span data-stu-id="82d40-2196">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82d40-2197">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82d40-2197">Az.Network</span></span>
* <span data-ttu-id="82d40-2198">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="82d40-2198">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="82d40-2199">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="82d40-2199">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="82d40-2200">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="82d40-2200">Az.NotificationHubs</span></span>
* <span data-ttu-id="82d40-2201">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="82d40-2201">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="82d40-2202">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="82d40-2202">Az.OperationalInsights</span></span>
* <span data-ttu-id="82d40-2203">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="82d40-2203">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="82d40-2204">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="82d40-2204">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="82d40-2205">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="82d40-2205">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="82d40-2206">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="82d40-2206">Az.RecoveryServices</span></span>
* <span data-ttu-id="82d40-2207">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="82d40-2207">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="82d40-2208">Обновлен табличный формат для SQL на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-2208">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="82d40-2209">Добавлен альтернативный метод для получения расположения в Общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-2209">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="82d40-2210">Обновлено значение ScheduleRunDays в объекте SchedulePolicy в соответствии с часовым поясом.</span><span class="sxs-lookup"><span data-stu-id="82d40-2210">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="82d40-2211">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="82d40-2211">Az.RedisCache</span></span>
* <span data-ttu-id="82d40-2212">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="82d40-2212">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="82d40-2213">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82d40-2213">Az.Resources</span></span>
* <span data-ttu-id="82d40-2214">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="82d40-2214">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="82d40-2215">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82d40-2215">Az.Sql</span></span>
* <span data-ttu-id="82d40-2216">Заменена зависимость от пакета SDK монитора на обычный код.</span><span class="sxs-lookup"><span data-stu-id="82d40-2216">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="82d40-2217">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="82d40-2217">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="82d40-2218">Улучшен процесс классификации нескольких столбцов.</span><span class="sxs-lookup"><span data-stu-id="82d40-2218">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="82d40-2219">Добавлены свойства SKU (имя, семейство, производительность SKU) в отклике Get-AzSqlServerServiceObjective, а также по умолчанию задан табличный формат.</span><span class="sxs-lookup"><span data-stu-id="82d40-2219">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="82d40-2220">C помощью Get-AzSqlServerServiceObjective теперь можно получать список доступных целевых служб по расположению без необходимости заранее размещать сервер в регионе.</span><span class="sxs-lookup"><span data-stu-id="82d40-2220">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="82d40-2221">Поддерживается параметр часового пояса при создании Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="82d40-2221">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="82d40-2222">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="82d40-2222">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="82d40-2223">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="82d40-2223">Az.Websites</span></span>
* <span data-ttu-id="82d40-2224">Исправлены командлеты Set-AzWebApp и Set-AzWebAppSlot, которые теперь не удаляют теги при выполнении.</span><span class="sxs-lookup"><span data-stu-id="82d40-2224">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="82d40-2225">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="82d40-2225">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="82d40-2226">Обновлен пакет SDK веб-узлов.</span><span class="sxs-lookup"><span data-stu-id="82d40-2226">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="82d40-2227">Удалено свойство AdminSiteName из PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="82d40-2227">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="82d40-2228">1.7.0 —апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="82d40-2228">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="82d40-2229">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="82d40-2229">Highlights since the last major release</span></span>
* <span data-ttu-id="82d40-2230">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="82d40-2230">General availability of `Az` module</span></span>
* <span data-ttu-id="82d40-2231">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="82d40-2231">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="82d40-2232">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="82d40-2232">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="82d40-2233">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="82d40-2233">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="82d40-2234">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="82d40-2234">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="82d40-2235">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="82d40-2235">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="82d40-2236">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="82d40-2236">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="82d40-2237">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="82d40-2237">Az.Accounts</span></span>
* <span data-ttu-id="82d40-2238">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметр AzureAnalysisServicesEndpointResourceId.</span><span class="sxs-lookup"><span data-stu-id="82d40-2238">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="82d40-2239">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="82d40-2239">Az.AnalysisServices</span></span>
* <span data-ttu-id="82d40-2240">Использование ServiceClient в командлетах плоскости данных и удаление исходной логики проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="82d40-2240">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="82d40-2241">Add-AzureASAccount используется как оболочка для Connect-AzAccount во избежание критических изменений.</span><span class="sxs-lookup"><span data-stu-id="82d40-2241">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="82d40-2242">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="82d40-2242">Az.Automation</span></span>
* <span data-ttu-id="82d40-2243">Исправлена ошибка командлета New-AzAutomationSoftwareUpdateConfiguration, связанная с включением.</span><span class="sxs-lookup"><span data-stu-id="82d40-2243">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="82d40-2244">Теперь параметры IncludedKbNumber и IncludedPackageNameMask должны работать нормально.</span><span class="sxs-lookup"><span data-stu-id="82d40-2244">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="82d40-2245">Исправлена ошибка динамической группы управления обновлениями службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-2245">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82d40-2246">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82d40-2246">Az.Compute</span></span>
* <span data-ttu-id="82d40-2247">В командлеты New-AzDiskConfig и New-AzSnapshotConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="82d40-2247">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="82d40-2248">Теперь можно создавать виртуальные машину на основе образов из коллекции от других клиентов.</span><span class="sxs-lookup"><span data-stu-id="82d40-2248">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="82d40-2249">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="82d40-2249">Az.ContainerInstance</span></span>
* <span data-ttu-id="82d40-2250">Исправлена проблема в параметре -Command командлета New-AzContainerGroup, из-за которой в конце добавлялся пустой аргумент.</span><span class="sxs-lookup"><span data-stu-id="82d40-2250">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="82d40-2251">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="82d40-2251">Az.DataFactory</span></span>
* <span data-ttu-id="82d40-2252">Пакет SDK для ADF .NET обновлен до версии 3.0.2.</span><span class="sxs-lookup"><span data-stu-id="82d40-2252">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="82d40-2253">Командлет Set-AzDataFactoryV2 обновлен с помощью дополнительных параметров для настроек, связанных с RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="82d40-2253">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="82d40-2254">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82d40-2254">Az.Resources</span></span>
* <span data-ttu-id="82d40-2255">Улучшена обработка поставщиков Get-AzResource при предоставлении параметров -ResourceId или -ResourceGroupName, -Name и -ResourceType.</span><span class="sxs-lookup"><span data-stu-id="82d40-2255">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="82d40-2256">Улучшена обработка ошибок в командлетах Test-AzDeployment и Test-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="82d40-2256">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="82d40-2257">Теперь ошибки, возникающие за пределами проверки развертывания, обрабатываются и включаются в выходные данные команды.</span><span class="sxs-lookup"><span data-stu-id="82d40-2257">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="82d40-2258">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="82d40-2258">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="82d40-2259">Добавлен параметр-переключатель -IgnoreDynamicParameters, с помощью которого можно настроить командлеты развертывания так, чтобы они пропускали запросы в сценариях скриптов и заданий.</span><span class="sxs-lookup"><span data-stu-id="82d40-2259">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="82d40-2260">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="82d40-2260">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="82d40-2261">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82d40-2261">Az.Sql</span></span>
* <span data-ttu-id="82d40-2262">Поддержка классификации данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="82d40-2262">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="82d40-2263">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="82d40-2263">Az.Storage</span></span>
* <span data-ttu-id="82d40-2264">Подробные сообщения об ошибке передаются при создании контекста хранилища с помощью параметра -UseConnectedAccount, но без входа в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-2264">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="82d40-2265">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="82d40-2265">New-AzStorageContext</span></span>
* <span data-ttu-id="82d40-2266">Поддержка свойств службы управления BLOB-объектов в указанной учетной записи хранения с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="82d40-2266">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="82d40-2267">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="82d40-2267">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="82d40-2268">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="82d40-2268">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="82d40-2269">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="82d40-2269">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="82d40-2270">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="82d40-2270">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="82d40-2271">Поддержка параметра -AsJob в командлетах для отправки и скачивания больших двоичных объектов и файлов.</span><span class="sxs-lookup"><span data-stu-id="82d40-2271">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="82d40-2272">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="82d40-2272">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="82d40-2273">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="82d40-2273">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="82d40-2274">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="82d40-2274">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="82d40-2275">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="82d40-2275">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="82d40-2276">1.6.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="82d40-2276">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="82d40-2277">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="82d40-2277">Highlights since the last major release</span></span>
* <span data-ttu-id="82d40-2278">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="82d40-2278">General availability of `Az` module</span></span>
* <span data-ttu-id="82d40-2279">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="82d40-2279">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="82d40-2280">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="82d40-2280">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="82d40-2281">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="82d40-2281">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="82d40-2282">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="82d40-2282">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="82d40-2283">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="82d40-2283">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="82d40-2284">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="82d40-2284">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="82d40-2285">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="82d40-2285">Az.Automation</span></span>
* <span data-ttu-id="82d40-2286">В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:</span><span class="sxs-lookup"><span data-stu-id="82d40-2286">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="82d40-2287">динамическое группирование;</span><span class="sxs-lookup"><span data-stu-id="82d40-2287">Dynamic grouping</span></span>
    * <span data-ttu-id="82d40-2288">скрипты предварительного или последующего выполнения;</span><span class="sxs-lookup"><span data-stu-id="82d40-2288">Pre-Post script</span></span>
    * <span data-ttu-id="82d40-2289">параметр перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="82d40-2289">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82d40-2290">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82d40-2290">Az.Compute</span></span>
* <span data-ttu-id="82d40-2291">Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.</span><span class="sxs-lookup"><span data-stu-id="82d40-2291">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="82d40-2292">Обновление клиентской библиотеки вычислений до версии 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="82d40-2292">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="82d40-2293">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="82d40-2293">Az.KeyVault</span></span>
* <span data-ttu-id="82d40-2294">Добавлена поддержка подстановочных знаков в командлетах KeyVault.</span><span class="sxs-lookup"><span data-stu-id="82d40-2294">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82d40-2295">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82d40-2295">Az.Network</span></span>
* <span data-ttu-id="82d40-2296">Добавлена поддержка анализа угроз для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-2296">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="82d40-2297">Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="82d40-2297">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="82d40-2298">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="82d40-2298">Az.RecoveryServices</span></span>
* <span data-ttu-id="82d40-2299">В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.</span><span class="sxs-lookup"><span data-stu-id="82d40-2299">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="82d40-2300">Добавлена поддержка канала для отмены регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="82d40-2300">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="82d40-2301">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82d40-2301">Az.Resources</span></span>
* <span data-ttu-id="82d40-2302">Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="82d40-2302">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="82d40-2303">Обновлены учетные данные, используемые при общих вызовах к ARM.</span><span class="sxs-lookup"><span data-stu-id="82d40-2303">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="82d40-2304">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82d40-2304">Az.Sql</span></span>
* <span data-ttu-id="82d40-2305">Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="82d40-2305">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="82d40-2306">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="82d40-2306">Az.Storage</span></span>
* <span data-ttu-id="82d40-2307">Поддержка получения, настройки и удаления политики управления в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="82d40-2307">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="82d40-2308">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="82d40-2308">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="82d40-2309">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="82d40-2309">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="82d40-2310">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="82d40-2310">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="82d40-2311">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="82d40-2311">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="82d40-2312">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="82d40-2312">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="82d40-2313">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="82d40-2313">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="82d40-2314">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="82d40-2314">Az.Websites</span></span>
* <span data-ttu-id="82d40-2315">Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="82d40-2315">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="82d40-2316">1.5.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="82d40-2316">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="82d40-2317">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="82d40-2317">Az.Accounts</span></span>
* <span data-ttu-id="82d40-2318">Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.</span><span class="sxs-lookup"><span data-stu-id="82d40-2318">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="82d40-2319">Обновлены примеры для Connect AzAccount.</span><span class="sxs-lookup"><span data-stu-id="82d40-2319">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="82d40-2320">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="82d40-2320">Az.Automation</span></span>
* <span data-ttu-id="82d40-2321">Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-2321">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="82d40-2322">Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов.</span><span class="sxs-lookup"><span data-stu-id="82d40-2322">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="82d40-2323">Теперь он возвращает все узлы.</span><span class="sxs-lookup"><span data-stu-id="82d40-2323">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="82d40-2324">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="82d40-2324">Az.Cdn</span></span>
* <span data-ttu-id="82d40-2325">Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.</span><span class="sxs-lookup"><span data-stu-id="82d40-2325">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82d40-2326">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82d40-2326">Az.Compute</span></span>
* <span data-ttu-id="82d40-2327">Добавлена поддержка подстановочных знаков в командлетах Get.</span><span class="sxs-lookup"><span data-stu-id="82d40-2327">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="82d40-2328">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="82d40-2328">Az.DataFactory</span></span>
* <span data-ttu-id="82d40-2329">Обновлен пакет SDK для ADF .NET до версии 3.0.1.</span><span class="sxs-lookup"><span data-stu-id="82d40-2329">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="82d40-2330">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="82d40-2330">Az.LogicApp</span></span>
* <span data-ttu-id="82d40-2331">Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.</span><span class="sxs-lookup"><span data-stu-id="82d40-2331">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82d40-2332">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82d40-2332">Az.Network</span></span>
* <span data-ttu-id="82d40-2333">Добавлена поддержка подстановочных знаков в командлетах Network.</span><span class="sxs-lookup"><span data-stu-id="82d40-2333">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="82d40-2334">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="82d40-2334">Az.RecoveryServices</span></span>
* <span data-ttu-id="82d40-2335">Добавлена поддержка SQL Server на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-2335">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="82d40-2336">Обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="82d40-2336">SDK Update</span></span>
* <span data-ttu-id="82d40-2337">Удалена проверка VMappContainer в Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="82d40-2337">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="82d40-2338">Добавлены параметры Name и ServerName для Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="82d40-2338">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="82d40-2339">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82d40-2339">Az.Resources</span></span>
* <span data-ttu-id="82d40-2340">Добавлен параметр `-TemplateObject` в командлеты для развертывания.</span><span class="sxs-lookup"><span data-stu-id="82d40-2340">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="82d40-2341">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.</span><span class="sxs-lookup"><span data-stu-id="82d40-2341">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="82d40-2342">Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="82d40-2342">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="82d40-2343">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.</span><span class="sxs-lookup"><span data-stu-id="82d40-2343">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="82d40-2344">Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="82d40-2344">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="82d40-2345">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.</span><span class="sxs-lookup"><span data-stu-id="82d40-2345">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="82d40-2346">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82d40-2346">Az.Sql</span></span>
* <span data-ttu-id="82d40-2347">Обновление AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="82d40-2347">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="82d40-2348">Исправлено поведение для пограничного случая при создании параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="82d40-2348">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="82d40-2349">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="82d40-2349">Az.Storage</span></span>
* <span data-ttu-id="82d40-2350">Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="82d40-2350">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="82d40-2351">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="82d40-2351">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="82d40-2352">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="82d40-2352">Az.AnalysisServices</span></span>
* <span data-ttu-id="82d40-2353">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="82d40-2353">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="82d40-2354">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="82d40-2354">Az.Automation</span></span>
* <span data-ttu-id="82d40-2355">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="82d40-2355">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="82d40-2356">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="82d40-2356">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="82d40-2357">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="82d40-2357">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="82d40-2358">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="82d40-2358">Az.CognitiveServices</span></span>
* <span data-ttu-id="82d40-2359">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="82d40-2359">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82d40-2360">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82d40-2360">Az.Compute</span></span>
* <span data-ttu-id="82d40-2361">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="82d40-2361">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="82d40-2362">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="82d40-2362">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="82d40-2363">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="82d40-2363">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="82d40-2364">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="82d40-2364">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="82d40-2365">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="82d40-2365">Az.DataLakeStore</span></span>
* <span data-ttu-id="82d40-2366">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="82d40-2366">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="82d40-2367">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="82d40-2367">Az.EventHub</span></span>
* <span data-ttu-id="82d40-2368">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="82d40-2368">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="82d40-2369">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="82d40-2369">Az.KeyVault</span></span>
* <span data-ttu-id="82d40-2370">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="82d40-2370">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="82d40-2371">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="82d40-2371">Az.LogicApp</span></span>
* <span data-ttu-id="82d40-2372">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="82d40-2372">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="82d40-2373">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="82d40-2373">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="82d40-2374">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="82d40-2374">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="82d40-2375">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="82d40-2375">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="82d40-2376">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="82d40-2376">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="82d40-2377">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="82d40-2377">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="82d40-2378">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="82d40-2378">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="82d40-2379">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="82d40-2379">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="82d40-2380">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="82d40-2380">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="82d40-2381">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="82d40-2381">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="82d40-2382">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="82d40-2382">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="82d40-2383">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="82d40-2383">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="82d40-2384">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="82d40-2384">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="82d40-2385">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="82d40-2385">Az.Monitor</span></span>
* <span data-ttu-id="82d40-2386">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="82d40-2386">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82d40-2387">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82d40-2387">Az.Network</span></span>
* <span data-ttu-id="82d40-2388">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="82d40-2388">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="82d40-2389">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="82d40-2389">Az.OperationalInsights</span></span>
* <span data-ttu-id="82d40-2390">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="82d40-2390">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="82d40-2391">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="82d40-2391">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="82d40-2392">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="82d40-2392">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="82d40-2393">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82d40-2393">Az.Resources</span></span>
* <span data-ttu-id="82d40-2394">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="82d40-2394">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="82d40-2395">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="82d40-2395">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="82d40-2396">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="82d40-2396">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="82d40-2397">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="82d40-2397">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="82d40-2398">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82d40-2398">Az.Sql</span></span>
* <span data-ttu-id="82d40-2399">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="82d40-2399">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="82d40-2400">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="82d40-2400">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="82d40-2401">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="82d40-2401">Az.Websites</span></span>
* <span data-ttu-id="82d40-2402">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="82d40-2402">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="82d40-2403">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="82d40-2403">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="82d40-2404">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="82d40-2404">Az.Accounts</span></span>
* <span data-ttu-id="82d40-2405">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="82d40-2405">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="82d40-2406">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="82d40-2406">Az.AnalysisServices</span></span>
<span data-ttu-id="82d40-2407">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="82d40-2407">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82d40-2408">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82d40-2408">Az.Compute</span></span>
* <span data-ttu-id="82d40-2409">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="82d40-2409">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="82d40-2410">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="82d40-2410">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="82d40-2411">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="82d40-2411">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="82d40-2412">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="82d40-2412">Az.RecoveryServices</span></span>
<span data-ttu-id="82d40-2413">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="82d40-2413">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="82d40-2414">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82d40-2414">Az.Resources</span></span>
* <span data-ttu-id="82d40-2415">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="82d40-2415">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="82d40-2416">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="82d40-2416">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="82d40-2417">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="82d40-2417">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="82d40-2418">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="82d40-2418">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="82d40-2419">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82d40-2419">Az.Sql</span></span>
* <span data-ttu-id="82d40-2420">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="82d40-2420">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="82d40-2421">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-2421">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="82d40-2422">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="82d40-2422">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="82d40-2423">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="82d40-2423">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="82d40-2424">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="82d40-2424">Az.Accounts</span></span>
* <span data-ttu-id="82d40-2425">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="82d40-2425">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="82d40-2426">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="82d40-2426">Az.AnalysisServices</span></span>
* <span data-ttu-id="82d40-2427">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="82d40-2427">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="82d40-2428">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="82d40-2428">Az.RecoveryServices</span></span>
* <span data-ttu-id="82d40-2429">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="82d40-2429">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="82d40-2430">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="82d40-2430">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="82d40-2431">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="82d40-2431">Az.Accounts</span></span>
* <span data-ttu-id="82d40-2432">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="82d40-2432">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="82d40-2433">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="82d40-2433">Update incorrect online help URLs</span></span>
* <span data-ttu-id="82d40-2434">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="82d40-2434">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="82d40-2435">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="82d40-2435">Az.Aks</span></span>
* <span data-ttu-id="82d40-2436">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="82d40-2436">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="82d40-2437">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="82d40-2437">Az.Automation</span></span>
* <span data-ttu-id="82d40-2438">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="82d40-2438">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="82d40-2439">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="82d40-2439">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="82d40-2440">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="82d40-2440">Az.Cdn</span></span>
* <span data-ttu-id="82d40-2441">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="82d40-2441">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82d40-2442">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82d40-2442">Az.Compute</span></span>
* <span data-ttu-id="82d40-2443">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="82d40-2443">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="82d40-2444">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="82d40-2444">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="82d40-2445">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="82d40-2445">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="82d40-2446">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="82d40-2446">Az.ContainerRegistry</span></span>
* <span data-ttu-id="82d40-2447">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="82d40-2447">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="82d40-2448">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="82d40-2448">Az.DataFactory</span></span>
* <span data-ttu-id="82d40-2449">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="82d40-2449">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="82d40-2450">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="82d40-2450">Az.DataLakeStore</span></span>
* <span data-ttu-id="82d40-2451">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="82d40-2451">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="82d40-2452">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="82d40-2452">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="82d40-2453">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="82d40-2453">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="82d40-2454">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="82d40-2454">Az.IotHub</span></span>
* <span data-ttu-id="82d40-2455">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="82d40-2455">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="82d40-2456">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="82d40-2456">Az.KeyVault</span></span>
* <span data-ttu-id="82d40-2457">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="82d40-2457">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82d40-2458">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82d40-2458">Az.Network</span></span>
* <span data-ttu-id="82d40-2459">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="82d40-2459">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="82d40-2460">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82d40-2460">Az.Resources</span></span>
* <span data-ttu-id="82d40-2461">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="82d40-2461">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="82d40-2462">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="82d40-2462">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="82d40-2463">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="82d40-2463">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="82d40-2464">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="82d40-2464">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="82d40-2465">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="82d40-2465">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="82d40-2466">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="82d40-2466">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="82d40-2467">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="82d40-2467">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="82d40-2468">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="82d40-2468">Az.ServiceFabric</span></span>
* <span data-ttu-id="82d40-2469">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="82d40-2469">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="82d40-2470">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="82d40-2470">Fix some error messages.</span></span>
* <span data-ttu-id="82d40-2471">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="82d40-2471">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="82d40-2472">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="82d40-2472">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="82d40-2473">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="82d40-2473">Az.SignalR</span></span>
* <span data-ttu-id="82d40-2474">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="82d40-2474">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="82d40-2475">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82d40-2475">Az.Sql</span></span>
* <span data-ttu-id="82d40-2476">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="82d40-2476">Update incorrect online help URLs</span></span>
* <span data-ttu-id="82d40-2477">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="82d40-2477">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="82d40-2478">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="82d40-2478">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="82d40-2479">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="82d40-2479">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="82d40-2480">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="82d40-2480">Az.Storage</span></span>
* <span data-ttu-id="82d40-2481">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="82d40-2481">Update incorrect online help URLs</span></span>
* <span data-ttu-id="82d40-2482">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="82d40-2482">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="82d40-2483">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="82d40-2483">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="82d40-2484">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="82d40-2484">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="82d40-2485">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="82d40-2485">Az.TrafficManager</span></span>
* <span data-ttu-id="82d40-2486">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="82d40-2486">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="82d40-2487">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="82d40-2487">Az.Websites</span></span>
* <span data-ttu-id="82d40-2488">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="82d40-2488">Update incorrect online help URLs</span></span>
* <span data-ttu-id="82d40-2489">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="82d40-2489">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="82d40-2490">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="82d40-2490">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="82d40-2491">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="82d40-2491">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="82d40-2492">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="82d40-2492">Az.Accounts</span></span>
* <span data-ttu-id="82d40-2493">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="82d40-2493">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82d40-2494">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82d40-2494">Az.Compute</span></span>
* <span data-ttu-id="82d40-2495">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="82d40-2495">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="82d40-2496">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="82d40-2496">Updated the description of ID in help files</span></span>
* <span data-ttu-id="82d40-2497">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="82d40-2497">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="82d40-2498">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="82d40-2498">Az.DataLakeStore</span></span>
* <span data-ttu-id="82d40-2499">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="82d40-2499">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="82d40-2500">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="82d40-2500">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="82d40-2501">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="82d40-2501">Az.EventGrid</span></span>
* <span data-ttu-id="82d40-2502">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="82d40-2502">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="82d40-2503">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="82d40-2503">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="82d40-2504">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="82d40-2504">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="82d40-2505">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="82d40-2505">Event Time-To-Live,</span></span>
        - <span data-ttu-id="82d40-2506">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="82d40-2506">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="82d40-2507">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="82d40-2507">Dead letter endpoint.</span></span>
    - <span data-ttu-id="82d40-2508">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="82d40-2508">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="82d40-2509">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="82d40-2509">Event Time-To-Live,</span></span>
        - <span data-ttu-id="82d40-2510">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="82d40-2510">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="82d40-2511">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="82d40-2511">Dead letter endpoint.</span></span>
* <span data-ttu-id="82d40-2512">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="82d40-2512">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="82d40-2513">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="82d40-2513">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="82d40-2514">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="82d40-2514">Az.IotHub</span></span>
* <span data-ttu-id="82d40-2515">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="82d40-2515">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="82d40-2516">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="82d40-2516">Az.LogicApp</span></span>
* <span data-ttu-id="82d40-2517">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="82d40-2517">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="82d40-2518">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82d40-2518">Az.Resources</span></span>
* <span data-ttu-id="82d40-2519">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="82d40-2519">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="82d40-2520">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="82d40-2520">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="82d40-2521">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="82d40-2521">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="82d40-2522">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="82d40-2522">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="82d40-2523">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="82d40-2523">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="82d40-2524">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="82d40-2524">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="82d40-2525">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="82d40-2525">Az.SignalR</span></span>
* <span data-ttu-id="82d40-2526">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="82d40-2526">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="82d40-2527">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82d40-2527">Az.Sql</span></span>
* <span data-ttu-id="82d40-2528">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="82d40-2528">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="82d40-2529">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="82d40-2529">Az.Storage</span></span>
* <span data-ttu-id="82d40-2530">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="82d40-2530">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="82d40-2531">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="82d40-2531">New-AzStorageContext</span></span>
* <span data-ttu-id="82d40-2532">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="82d40-2532">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="82d40-2533">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="82d40-2533">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="82d40-2534">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="82d40-2534">Az.Websites</span></span>
* <span data-ttu-id="82d40-2535">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="82d40-2535">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="82d40-2536">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="82d40-2536">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="82d40-2537">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="82d40-2537">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="82d40-2538">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="82d40-2538">General</span></span>

- <span data-ttu-id="82d40-2539">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="82d40-2539">General Availability of Az Module</span></span>
- <span data-ttu-id="82d40-2540">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="82d40-2540">Online help for each module</span></span>
- <span data-ttu-id="82d40-2541">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="82d40-2541">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="82d40-2542">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="82d40-2542">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="82d40-2543">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="82d40-2543">Az.Accounts</span></span>
- <span data-ttu-id="82d40-2544">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="82d40-2544">Changed from Az.Profile</span></span>
- <span data-ttu-id="82d40-2545">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="82d40-2545">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="82d40-2546">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="82d40-2546">Az.ApiManagement</span></span>
- <span data-ttu-id="82d40-2547">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="82d40-2547">Fixes for #7002</span></span>
- <span data-ttu-id="82d40-2548">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="82d40-2548">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="82d40-2549">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="82d40-2549">Az.Batch</span></span>
- <span data-ttu-id="82d40-2550">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="82d40-2550">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="82d40-2551">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="82d40-2551">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="82d40-2552">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="82d40-2552">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="82d40-2553">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="82d40-2553">Az.Billing</span></span>
- <span data-ttu-id="82d40-2554">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="82d40-2554">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="82d40-2555">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="82d40-2555">Az.CognitivServices</span></span>
- <span data-ttu-id="82d40-2556">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="82d40-2556">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="82d40-2557">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="82d40-2557">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="82d40-2558">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="82d40-2558">Az.ContainerInstance</span></span>
- <span data-ttu-id="82d40-2559">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="82d40-2559">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="82d40-2560">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="82d40-2560">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="82d40-2561">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="82d40-2561">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="82d40-2562">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="82d40-2562">Az.DataLakeStore</span></span>
- <span data-ttu-id="82d40-2563">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="82d40-2563">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="82d40-2564">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="82d40-2564">Az.Monitor</span></span>
- <span data-ttu-id="82d40-2565">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="82d40-2565">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="82d40-2566">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="82d40-2566">Az.KeyVault</span></span>
- <span data-ttu-id="82d40-2567">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="82d40-2567">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="82d40-2568">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="82d40-2568">Az.MachineLearning</span></span>
- <span data-ttu-id="82d40-2569">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="82d40-2569">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="82d40-2570">Az.Media</span><span class="sxs-lookup"><span data-stu-id="82d40-2570">Az.Media</span></span>
- <span data-ttu-id="82d40-2571">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="82d40-2571">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="82d40-2572">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82d40-2572">Az.Network</span></span>
<span data-ttu-id="82d40-2573">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="82d40-2573">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="82d40-2574">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="82d40-2574">New cmdlets added:</span></span>
        - <span data-ttu-id="82d40-2575">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="82d40-2575">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="82d40-2576">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="82d40-2576">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="82d40-2577">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="82d40-2577">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="82d40-2578">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="82d40-2578">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="82d40-2579">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="82d40-2579">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="82d40-2580">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="82d40-2580">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="82d40-2581">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="82d40-2581">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="82d40-2582">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="82d40-2582">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="82d40-2583">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="82d40-2583">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="82d40-2584">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="82d40-2584">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="82d40-2585">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="82d40-2585">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="82d40-2586">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="82d40-2586">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="82d40-2587">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="82d40-2587">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="82d40-2588">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="82d40-2588">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="82d40-2589">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="82d40-2589">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="82d40-2590">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="82d40-2590">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="82d40-2591">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="82d40-2591">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="82d40-2592">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="82d40-2592">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="82d40-2593">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="82d40-2593">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="82d40-2594">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="82d40-2594">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="82d40-2595">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="82d40-2595">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="82d40-2596">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="82d40-2596">Az.OperationalInsights</span></span>
- <span data-ttu-id="82d40-2597">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="82d40-2597">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="82d40-2598">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="82d40-2598">Az.Profile</span></span>
- <span data-ttu-id="82d40-2599">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="82d40-2599">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="82d40-2600">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="82d40-2600">Az.RecoveryServices</span></span>
- <span data-ttu-id="82d40-2601">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="82d40-2601">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="82d40-2602">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82d40-2602">Az.Resources</span></span>
- <span data-ttu-id="82d40-2603">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="82d40-2603">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="82d40-2604">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="82d40-2604">Az.ServiceFabric</span></span>
- <span data-ttu-id="82d40-2605">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="82d40-2605">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="82d40-2606">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="82d40-2606">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="82d40-2607">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="82d40-2607">Az.SIgnalR</span></span>
- <span data-ttu-id="82d40-2608">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="82d40-2608">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="82d40-2609">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82d40-2609">Az.Sql</span></span>
- <span data-ttu-id="82d40-2610">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="82d40-2610">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="82d40-2611">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="82d40-2611">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="82d40-2612">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="82d40-2612">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="82d40-2613">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="82d40-2613">Az.Storage</span></span>
- <span data-ttu-id="82d40-2614">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="82d40-2614">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="82d40-2615">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="82d40-2615">Az.Websites</span></span>
- <span data-ttu-id="82d40-2616">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="82d40-2616">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="82d40-2617">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="82d40-2617">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="82d40-2618">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="82d40-2618">General</span></span>

* <span data-ttu-id="82d40-2619">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="82d40-2619">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="82d40-2620">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82d40-2620">Az.Compute</span></span>

* <span data-ttu-id="82d40-2621">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="82d40-2621">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="82d40-2622">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="82d40-2622">Az.DataLakeStore</span></span>

* <span data-ttu-id="82d40-2623">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="82d40-2623">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="82d40-2624">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="82d40-2624">Az.FrontDoor</span></span>

* <span data-ttu-id="82d40-2625">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="82d40-2625">Fixed some broken links</span></span>
    - <span data-ttu-id="82d40-2626">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="82d40-2626">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="82d40-2627">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="82d40-2627">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="82d40-2628">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="82d40-2628">Az.RecoveryServices</span></span>

* <span data-ttu-id="82d40-2629">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-2629">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="82d40-2630">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="82d40-2630">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="82d40-2631">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82d40-2631">Az.Resources</span></span>

* <span data-ttu-id="82d40-2632">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="82d40-2632">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="82d40-2633">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="82d40-2633">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="82d40-2634">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82d40-2634">Az.Sql</span></span>

* <span data-ttu-id="82d40-2635">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="82d40-2635">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="82d40-2636">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="82d40-2636">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="82d40-2637">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="82d40-2637">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="82d40-2638">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="82d40-2638">Az.Storage</span></span>

* <span data-ttu-id="82d40-2639">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="82d40-2639">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="82d40-2640">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="82d40-2640">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="82d40-2641">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="82d40-2641">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="82d40-2642">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="82d40-2642">Support Static Website configuration</span></span>
    - <span data-ttu-id="82d40-2643">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="82d40-2643">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="82d40-2644">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="82d40-2644">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="82d40-2645">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="82d40-2645">Az.Websites</span></span>

* <span data-ttu-id="82d40-2646">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="82d40-2646">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="82d40-2647">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="82d40-2647">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="82d40-2648">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-2648">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="82d40-2649">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="82d40-2649">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="82d40-2650">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="82d40-2650">Az.ApiManagement</span></span>
* <span data-ttu-id="82d40-2651">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="82d40-2651">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="82d40-2652">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="82d40-2652">Az.Automation</span></span>
* <span data-ttu-id="82d40-2653">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="82d40-2653">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="82d40-2654">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="82d40-2654">Added Update Management cmdlets</span></span>
* <span data-ttu-id="82d40-2655">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="82d40-2655">Added Source Control cmdlets</span></span>
* <span data-ttu-id="82d40-2656">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="82d40-2656">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="82d40-2657">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="82d40-2657">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="82d40-2658">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82d40-2658">Az.Compute</span></span>
* <span data-ttu-id="82d40-2659">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="82d40-2659">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="82d40-2660">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="82d40-2660">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="82d40-2661">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="82d40-2661">Az.ContainerInstance</span></span>
* <span data-ttu-id="82d40-2662">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="82d40-2662">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="82d40-2663">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="82d40-2663">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="82d40-2664">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="82d40-2664">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="82d40-2665">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82d40-2665">Az.Network</span></span>
* <span data-ttu-id="82d40-2666">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="82d40-2666">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="82d40-2667">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-2667">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="82d40-2668">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="82d40-2668">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="82d40-2669">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="82d40-2669">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="82d40-2670">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="82d40-2670">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="82d40-2671">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="82d40-2671">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="82d40-2672">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="82d40-2672">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="82d40-2673">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="82d40-2673">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="82d40-2674">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="82d40-2674">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="82d40-2675">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="82d40-2675">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="82d40-2676">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="82d40-2676">Az.Relay</span></span>
* <span data-ttu-id="82d40-2677">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="82d40-2677">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="82d40-2678">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82d40-2678">Az.Resources</span></span>
* <span data-ttu-id="82d40-2679">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="82d40-2679">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="82d40-2680">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="82d40-2680">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="82d40-2681">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="82d40-2681">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="82d40-2682">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="82d40-2682">Az.ServiceFabric</span></span>
* <span data-ttu-id="82d40-2683">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="82d40-2683">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="82d40-2684">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82d40-2684">Az.Sql</span></span>
* <span data-ttu-id="82d40-2685">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-2685">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="82d40-2686">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="82d40-2686">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="82d40-2687">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="82d40-2687">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="82d40-2688">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="82d40-2688">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="82d40-2689">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="82d40-2689">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="82d40-2690">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="82d40-2690">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="82d40-2691">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="82d40-2691">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="82d40-2692">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="82d40-2692">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="82d40-2693">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="82d40-2693">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="82d40-2694">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="82d40-2694">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="82d40-2695">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="82d40-2695">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="82d40-2696">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="82d40-2696">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="82d40-2697">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="82d40-2697">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="82d40-2698">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="82d40-2698">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="82d40-2699">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="82d40-2699">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="82d40-2700">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="82d40-2700">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="82d40-2701">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="82d40-2701">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="82d40-2702">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="82d40-2702">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="82d40-2703">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="82d40-2703">General</span></span>
* <span data-ttu-id="82d40-2704">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="82d40-2704">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="82d40-2705">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="82d40-2705">Az.Profile</span></span>
* <span data-ttu-id="82d40-2706">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="82d40-2706">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="82d40-2707">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="82d40-2707">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="82d40-2708">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="82d40-2708">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="82d40-2709">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="82d40-2709">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="82d40-2710">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="82d40-2710">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="82d40-2711">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="82d40-2711">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="82d40-2712">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="82d40-2712">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="82d40-2713">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="82d40-2713">Az.CognitiveServices</span></span>
* <span data-ttu-id="82d40-2714">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="82d40-2714">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82d40-2715">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82d40-2715">Az.Compute</span></span>
* <span data-ttu-id="82d40-2716">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="82d40-2716">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="82d40-2717">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="82d40-2717">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="82d40-2718">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="82d40-2718">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="82d40-2719">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="82d40-2719">Az.DataLakeStore</span></span>
* <span data-ttu-id="82d40-2720">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="82d40-2720">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="82d40-2721">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="82d40-2721">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="82d40-2722">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="82d40-2722">Az.Insights</span></span>
* <span data-ttu-id="82d40-2723">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="82d40-2723">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="82d40-2724">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="82d40-2724">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="82d40-2725">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="82d40-2725">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="82d40-2726">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="82d40-2726">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82d40-2727">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82d40-2727">Az.Network</span></span>
* <span data-ttu-id="82d40-2728">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="82d40-2728">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="82d40-2729">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="82d40-2729">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="82d40-2730">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="82d40-2730">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="82d40-2731">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="82d40-2731">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="82d40-2732">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="82d40-2732">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="82d40-2733">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="82d40-2733">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="82d40-2734">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="82d40-2734">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="82d40-2735">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="82d40-2735">Az.PolicyInsights</span></span>
* <span data-ttu-id="82d40-2736">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="82d40-2736">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="82d40-2737">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82d40-2737">Az.Resources</span></span>
* <span data-ttu-id="82d40-2738">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="82d40-2738">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="82d40-2739">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="82d40-2739">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="82d40-2740">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="82d40-2740">Az.ServiceBus</span></span>
* <span data-ttu-id="82d40-2741">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="82d40-2741">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="82d40-2742">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="82d40-2742">Az.ServiceFabric</span></span>
* <span data-ttu-id="82d40-2743">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="82d40-2743">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="82d40-2744">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="82d40-2744">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="82d40-2745">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="82d40-2745">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="82d40-2746">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="82d40-2746">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="82d40-2747">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="82d40-2747">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="82d40-2748">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="82d40-2748">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="82d40-2749">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="82d40-2749">Az.Profile</span></span>
* <span data-ttu-id="82d40-2750">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="82d40-2750">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="82d40-2751">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="82d40-2751">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82d40-2752">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82d40-2752">Az.Compute</span></span>
* <span data-ttu-id="82d40-2753">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="82d40-2753">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="82d40-2754">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="82d40-2754">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="82d40-2755">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="82d40-2755">Az.DataLakeStore</span></span>
* <span data-ttu-id="82d40-2756">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="82d40-2756">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="82d40-2757">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="82d40-2757">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="82d40-2758">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="82d40-2758">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="82d40-2759">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="82d40-2759">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="82d40-2760">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="82d40-2760">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82d40-2761">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82d40-2761">Az.Network</span></span>
* <span data-ttu-id="82d40-2762">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="82d40-2762">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="82d40-2763">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="82d40-2763">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="82d40-2764">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82d40-2764">Az.Resources</span></span>
* <span data-ttu-id="82d40-2765">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="82d40-2765">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="82d40-2766">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="82d40-2766">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="82d40-2767">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="82d40-2767">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="82d40-2768">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="82d40-2768">Azure.Storage</span></span>
* <span data-ttu-id="82d40-2769">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="82d40-2769">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="82d40-2770">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="82d40-2770">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="82d40-2771">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="82d40-2771">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="82d40-2772">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="82d40-2772">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="82d40-2773">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="82d40-2773">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="82d40-2774">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="82d40-2774">Az.CognitiveServices</span></span>
* <span data-ttu-id="82d40-2775">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="82d40-2775">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82d40-2776">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82d40-2776">Az.Compute</span></span>
* <span data-ttu-id="82d40-2777">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="82d40-2777">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="82d40-2778">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="82d40-2778">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="82d40-2779">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-2779">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="82d40-2780">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="82d40-2780">Az.DataFactoryV2</span></span>
* <span data-ttu-id="82d40-2781">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="82d40-2781">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82d40-2782">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82d40-2782">Az.Network</span></span>
* <span data-ttu-id="82d40-2783">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="82d40-2783">Added NetworkProfile functionality.</span></span> <span data-ttu-id="82d40-2784">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="82d40-2784">new cmdlets added</span></span>
    - <span data-ttu-id="82d40-2785">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="82d40-2785">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="82d40-2786">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="82d40-2786">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="82d40-2787">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="82d40-2787">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="82d40-2788">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="82d40-2788">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="82d40-2789">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="82d40-2789">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="82d40-2790">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="82d40-2790">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="82d40-2791">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="82d40-2791">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="82d40-2792">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="82d40-2792">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="82d40-2793">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="82d40-2793">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="82d40-2794">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="82d40-2794">Az.RedisCache</span></span>
* <span data-ttu-id="82d40-2795">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="82d40-2795">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="82d40-2796">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="82d40-2796">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="82d40-2797">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82d40-2797">Az.Resources</span></span>
* <span data-ttu-id="82d40-2798">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="82d40-2798">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="82d40-2799">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="82d40-2799">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="82d40-2800">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82d40-2800">Az.Sql</span></span>
* <span data-ttu-id="82d40-2801">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="82d40-2801">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="82d40-2802">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="82d40-2802">Az.Websites</span></span>
* <span data-ttu-id="82d40-2803">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="82d40-2803">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="82d40-2804">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="82d40-2804">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="82d40-2805">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="82d40-2805">0.2.0 - September 2018</span></span>
 <span data-ttu-id="82d40-2806">Начальный выпуск</span><span class="sxs-lookup"><span data-stu-id="82d40-2806">Initial Release</span></span>
