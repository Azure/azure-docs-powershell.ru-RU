---
title: Заметки о выпуске Azure PowerShell
description: Узнайте обо всех последних обновлениях модулей Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 0fe1d2360af5a05953a08eaf3b3eaf0bf5ddcda5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100012202"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="d29f3-103">Заметки о выпуске Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d29f3-103">Azure PowerShell release notes</span></span>

## <a name="550---february-2021"></a><span data-ttu-id="d29f3-104">5.5.0 — февраль 2021 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-104">5.5.0 - February 2021</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d29f3-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d29f3-105">Az.Accounts</span></span>
* <span data-ttu-id="d29f3-106">Отслежен код ошибки CloudError в исключении.</span><span class="sxs-lookup"><span data-stu-id="d29f3-106">Tracked CloudError code in exception</span></span>
* <span data-ttu-id="d29f3-107">Событие ContextCleared вызывается при выполнении Clear-AzContext.</span><span class="sxs-lookup"><span data-stu-id="d29f3-107">Raised 'ContextCleared' event when 'Clear-AzContext' was executed</span></span>

#### <a name="azaks"></a><span data-ttu-id="d29f3-108">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="d29f3-108">Az.Aks</span></span>
* <span data-ttu-id="d29f3-109">Уточнены сообщения об ошибках при сбое командлета.</span><span class="sxs-lookup"><span data-stu-id="d29f3-109">Refined error messages of cmdlet failure.</span></span>
* <span data-ttu-id="d29f3-110">Обновлена обработка исключений для использования связанных с Azure PowerShell исключений.</span><span class="sxs-lookup"><span data-stu-id="d29f3-110">Upgraded exception handling to use Azure PowerShell related exceptions.</span></span>
* <span data-ttu-id="d29f3-111">Исправлена проблема, из-за которой пользователь не мог использовать предоставленный субъект-службу для создания кластера Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="d29f3-111">Fixed the issue that user could not use provided service principal to create Kubernetes cluster.</span></span> <span data-ttu-id="d29f3-112">[№ 13938]</span><span class="sxs-lookup"><span data-stu-id="d29f3-112">[#13938]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d29f3-113">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d29f3-113">Az.Automation</span></span>
* <span data-ttu-id="d29f3-114">Исправлена проблема с обработкой PSCustomObject и Array.</span><span class="sxs-lookup"><span data-stu-id="d29f3-114">Fixed the issue of processing 'PSCustomObject' and 'Array'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d29f3-115">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-115">Az.Compute</span></span>
* <span data-ttu-id="d29f3-116">Добавлен параметр -EnableAutomaticUpgrade к командлетам Set-AzVmExtension и Add-AzVmssExtension.</span><span class="sxs-lookup"><span data-stu-id="d29f3-116">Added parameter '-EnableAutomaticUpgrade' to 'Set-AzVmExtension' and 'Add-AzVmssExtension'.</span></span>
* <span data-ttu-id="d29f3-117">Удален параметр FilterExpression из документации по командлету Get-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="d29f3-117">Removed FilterExpression parameter from 'Get-AzVMImage' cmdlet documentation.</span></span> 
* <span data-ttu-id="d29f3-118">Добавлено сообщение о прекращении поддержки в командлеты ContainerService:</span><span class="sxs-lookup"><span data-stu-id="d29f3-118">Added deprecation message to the ContainerService cmdlets:</span></span>
    - <span data-ttu-id="d29f3-119">Add-AzureRmContainerServiceAgentPoolProfileCommand;</span><span class="sxs-lookup"><span data-stu-id="d29f3-119">'Add-AzureRmContainerServiceAgentPoolProfileCommand'</span></span>
    - <span data-ttu-id="d29f3-120">Get-AzContainerService;</span><span class="sxs-lookup"><span data-stu-id="d29f3-120">'Get-AzContainerService'</span></span>
    - <span data-ttu-id="d29f3-121">New-AzContainerService;</span><span class="sxs-lookup"><span data-stu-id="d29f3-121">'New-AzContainerService'</span></span>
    - <span data-ttu-id="d29f3-122">New-AzContainerServiceConfig;</span><span class="sxs-lookup"><span data-stu-id="d29f3-122">'New-AzContainerServiceConfig'</span></span>
    - <span data-ttu-id="d29f3-123">Remove-AzContainerService;</span><span class="sxs-lookup"><span data-stu-id="d29f3-123">'Remove-AzContainerService'</span></span>
    - <span data-ttu-id="d29f3-124">Remove-AzContainerServiceAgentPoolProfile;</span><span class="sxs-lookup"><span data-stu-id="d29f3-124">'Remove-AzContainerServiceAgentPoolProfile'</span></span>
    - <span data-ttu-id="d29f3-125">Update-AzContainerService.</span><span class="sxs-lookup"><span data-stu-id="d29f3-125">'Update-AzContainerService'</span></span>
* <span data-ttu-id="d29f3-126">Добавлен параметр -BurstingEnabled к командлетам New-AzDiskConfig и New-AzDiskUpdateConfig.</span><span class="sxs-lookup"><span data-stu-id="d29f3-126">Added parameter '-BurstingEnabled' to 'New-AzDiskConfig' and 'New-AzDiskUpdateConfig'</span></span>
* <span data-ttu-id="d29f3-127">Добавлены параметры -GroupByApplicationId и -GroupByUserAgent к командлетам Export-AzLogAnalyticThrottledRequest и Export-AzLogAnalyticRequestRateByInterval.</span><span class="sxs-lookup"><span data-stu-id="d29f3-127">Added '-GroupByApplicationId' and '-GroupByUserAgent' parameters to the 'Export-AzLogAnalyticThrottledRequest' and 'Export-AzLogAnalyticRequestRateByInterval' cmdlets.</span></span>
* <span data-ttu-id="d29f3-128">Добавлен набор параметров VMParameterSet к командлету Get-AzVMExtension.</span><span class="sxs-lookup"><span data-stu-id="d29f3-128">Added 'VMParameterSet' parameter set to 'Get-AzVMExtension' cmdlet.</span></span> <span data-ttu-id="d29f3-129">В этот набор параметров добавлен параметр -VM.</span><span class="sxs-lookup"><span data-stu-id="d29f3-129">Added new parameter '-VM' to this parameter set.</span></span> 

#### <a name="azcontainerregistry"></a><span data-ttu-id="d29f3-130">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d29f3-130">Az.ContainerRegistry</span></span>
* <span data-ttu-id="d29f3-131">Добавлены командлеты для поддерживаемых операций репозитория, манифеста и тегов:</span><span class="sxs-lookup"><span data-stu-id="d29f3-131">Added cmdlets to supported repository, manifest, and tag operations:</span></span>
    - <span data-ttu-id="d29f3-132">Get-AzContainerRegistryRepository;</span><span class="sxs-lookup"><span data-stu-id="d29f3-132">'Get-AzContainerRegistryRepository'</span></span>
    - <span data-ttu-id="d29f3-133">Update-AzContainerRegistryRepository;</span><span class="sxs-lookup"><span data-stu-id="d29f3-133">'Update-AzContainerRegistryRepository'</span></span>
    - <span data-ttu-id="d29f3-134">Remove-AzContainerRegistryRepository;</span><span class="sxs-lookup"><span data-stu-id="d29f3-134">'Remove-AzContainerRegistryRepository'</span></span>
    - <span data-ttu-id="d29f3-135">Get-AzContainerRegistryManifest;</span><span class="sxs-lookup"><span data-stu-id="d29f3-135">'Get-AzContainerRegistryManifest'</span></span>
    - <span data-ttu-id="d29f3-136">Update-AzContainerRegistryManifest;</span><span class="sxs-lookup"><span data-stu-id="d29f3-136">'Update-AzContainerRegistryManifest'</span></span>
    - <span data-ttu-id="d29f3-137">Remove-AzContainerRegistryManifest;</span><span class="sxs-lookup"><span data-stu-id="d29f3-137">'Remove-AzContainerRegistryManifest'</span></span>
    - <span data-ttu-id="d29f3-138">Get-AzContainerRegistryTag;</span><span class="sxs-lookup"><span data-stu-id="d29f3-138">'Get-AzContainerRegistryTag'</span></span>
    - <span data-ttu-id="d29f3-139">Update-AzContainerRegistryTag;</span><span class="sxs-lookup"><span data-stu-id="d29f3-139">'Update-AzContainerRegistryTag'</span></span>
    - <span data-ttu-id="d29f3-140">Remove-AzContainerRegistryTag.</span><span class="sxs-lookup"><span data-stu-id="d29f3-140">'Remove-AzContainerRegistryTag'</span></span>

#### <a name="azdatabricks"></a><span data-ttu-id="d29f3-141">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="d29f3-141">Az.Databricks</span></span>
<span data-ttu-id="d29f3-142">Реализована поддержка -EnableNoPublicIP при создании рабочей области Databricks.</span><span class="sxs-lookup"><span data-stu-id="d29f3-142">Supported -EnableNoPublicIP when creating a Databricks workspace</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d29f3-143">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d29f3-143">Az.FrontDoor</span></span>
* <span data-ttu-id="d29f3-144">Добавлено свойство FrontDoorId.</span><span class="sxs-lookup"><span data-stu-id="d29f3-144">Added FrontDoorId to properties</span></span>
* <span data-ttu-id="d29f3-145">Добавлена поддержка исключений JSON и RequestBodyCheck в управляемые правила.</span><span class="sxs-lookup"><span data-stu-id="d29f3-145">Added JSON Exclusions and RequestBodyCheck support to managed rules</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d29f3-146">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d29f3-146">Az.HDInsight</span></span>
* <span data-ttu-id="d29f3-147">Добавлены новые параметры -EnableComputeIsolation и -ComputeIsolationHostSku к командлету New-AzHDInsightCluster для поддержки функции изоляции вычислительных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-147">Added new parameter '-EnableComputeIsolation' and '-ComputeIsolationHostSku' to the cmdlet 'New-AzHDInsightCluster' to support compute isolation feature</span></span>
* <span data-ttu-id="d29f3-148">Добавлены свойства ComputeIsolationProperties и ConnectivityEndpoints к классу AzureHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="d29f3-148">Added property 'ComputeIsolationProperties' and 'ConnectivityEndpoints' in the class AzureHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d29f3-149">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d29f3-149">Az.KeyVault</span></span>
* <span data-ttu-id="d29f3-150">Реализована поддержка указания типа ключа и имени кривой при импортировании ключей через собственный файл ключа (BYOK).</span><span class="sxs-lookup"><span data-stu-id="d29f3-150">Supported specifying key type and curve name when importing keys via a BYOK file</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d29f3-151">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d29f3-151">Az.Network</span></span>
* <span data-ttu-id="d29f3-152">Добавлены новые командлеты для замены старого имени продукта virtual router новым именем route server в будущем:</span><span class="sxs-lookup"><span data-stu-id="d29f3-152">Added new cmdlets to replace old product name 'virtual router' with new name 'route server' in the future.</span></span>
    - <span data-ttu-id="d29f3-153">New-AzRouteServer;</span><span class="sxs-lookup"><span data-stu-id="d29f3-153">'New-AzRouteServer'</span></span>
    - <span data-ttu-id="d29f3-154">Get-AzRouteServer;</span><span class="sxs-lookup"><span data-stu-id="d29f3-154">'Get-AzRouteServer'</span></span>
    - <span data-ttu-id="d29f3-155">Remove-AzRouteServer;</span><span class="sxs-lookup"><span data-stu-id="d29f3-155">'Remove-AzRouteServer'</span></span>
    - <span data-ttu-id="d29f3-156">Update-AzRouteServer;</span><span class="sxs-lookup"><span data-stu-id="d29f3-156">'Update-AzRouteServer'</span></span>
    - <span data-ttu-id="d29f3-157">Get-AzRouteServerPeer;</span><span class="sxs-lookup"><span data-stu-id="d29f3-157">'Get-AzRouteServerPeer'</span></span>
    - <span data-ttu-id="d29f3-158">Add-AzRouteServerPeer;</span><span class="sxs-lookup"><span data-stu-id="d29f3-158">'Add-AzRouteServerPeer'</span></span>
    - <span data-ttu-id="d29f3-159">Update-AzRouteServerPeer;</span><span class="sxs-lookup"><span data-stu-id="d29f3-159">'Update-AzRouteServerPeer'</span></span>
    - <span data-ttu-id="d29f3-160">Remove-AzRouteServerPeer.</span><span class="sxs-lookup"><span data-stu-id="d29f3-160">'Remove-AzRouteServerPeer'</span></span>
    - <span data-ttu-id="d29f3-161">Добавлено предупреждение с атрибутом отмены поддержки в старые командлеты.</span><span class="sxs-lookup"><span data-stu-id="d29f3-161">Added deprecation attribute warning to the old cmdlets.</span></span>
* <span data-ttu-id="d29f3-162">Исправлена ошибка в MacSecConfig ExpressRouteLink.</span><span class="sxs-lookup"><span data-stu-id="d29f3-162">Bug fix in ExpressRouteLink MacSecConfig.</span></span> <span data-ttu-id="d29f3-163">Добавлено новое свойство SciState в PSExpressRouteLinkMacSecConfig.</span><span class="sxs-lookup"><span data-stu-id="d29f3-163">Added new property 'SciState' to 'PSExpressRouteLinkMacSecConfig'</span></span>
* <span data-ttu-id="d29f3-164">Обновлен список форматов и представления таблиц форматов для Get-AzVirtualNetworkGatewayConnectionIkeSa.</span><span class="sxs-lookup"><span data-stu-id="d29f3-164">Updated format list and format table views for Get-AzVirtualNetworkGatewayConnectionIkeSa</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d29f3-165">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d29f3-165">Az.PolicyInsights</span></span>
* <span data-ttu-id="d29f3-166">Отменены изменения в PowerShell, которые привели к увеличению ограничения на строки запросов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-166">Retracted changes made in powershell that increased request row limit.</span></span> <span data-ttu-id="d29f3-167">Удалено неверное утверждение по поддержке разбиения на страницы.</span><span class="sxs-lookup"><span data-stu-id="d29f3-167">Removed incorrect statement of supporting paging</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d29f3-168">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-168">Az.RecoveryServices</span></span>
* <span data-ttu-id="d29f3-169">Изменены ограничения для проверки политики в соответствии с параметрами службы резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="d29f3-169">modified policy validation limits as per backup service.</span></span>
* <span data-ttu-id="d29f3-170">Добавлена избыточность между зонами для хранилищ Служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="d29f3-170">Added Zone Redundancy for Recovery Service Vaults.</span></span> 
* <span data-ttu-id="d29f3-171">Добавлена поддержка Site Recovery для группы размещения близкого взаимодействия для VMware в Azure и HyperV для поставщиков Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-171">Azure Site Recovery support for Proximity placement group for VMware to Azure and HyperV to Azure providers.</span></span>
* <span data-ttu-id="d29f3-172">Добавлена поддержка Azure Site Recovery для зоны доступности для VMware в Azure и HyperV для поставщиков Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-172">Azure Site Recovery support for Availability zone for VMware to Azure and HyperV to Azure providers.</span></span>
* <span data-ttu-id="d29f3-173">Добавлена поддержка Azure Site Recovery для UseManagedDisk для HyperV в поставщик Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-173">Azure Site Recovery support for UseManagedDisk for HyperV to Azure provider</span></span>

#### <a name="azresources"></a><span data-ttu-id="d29f3-174">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-174">Az.Resources</span></span>
* <span data-ttu-id="d29f3-175">Удален тип субъекта в командлетах New-AzRoleAssignment и Set-AzRoleAssignment, так как текущие сопоставления приводили к ошибкам в определенных сценариях.</span><span class="sxs-lookup"><span data-stu-id="d29f3-175">Removed principal type on New-AzRoleAssignment and Set-AzRoleAssignment because current mapping was breaking certain scenarios</span></span>

#### <a name="azsql"></a><span data-ttu-id="d29f3-176">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-176">Az.Sql</span></span>
* <span data-ttu-id="d29f3-177">Добавлен MaintenanceConfigurationId к командлетам New-AzSqlDatabase, Set-AzSqlDatabase, New-AzSqlElasticPool и Set-AzSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="d29f3-177">Added MaintenanceConfigurationId to 'New-AzSqlDatabase', 'Set-AzSqlDatabase', 'New-AzSqlElasticPool' and 'Set-AzSqlElasticPool'</span></span>
* <span data-ttu-id="d29f3-178">Исправлена регрессия в Set-AzSqlServerAudit при указании аргумента PredicateExpression.</span><span class="sxs-lookup"><span data-stu-id="d29f3-178">Fixed regression in 'Set-AzSqlServerAudit' when PredicateExpression argument is provided</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d29f3-179">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d29f3-179">Az.Storage</span></span>
* <span data-ttu-id="d29f3-180">Добавлены поддержка параметров RoutingPreference в операциях создания и обновления учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="d29f3-180">Supported RoutingPreference settings in create/update Storage account</span></span>
    - <span data-ttu-id="d29f3-181">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d29f3-181">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="d29f3-182">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d29f3-182">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="d29f3-183">Обновлена версия Azure.Storage.Blobs до 12.8.0.</span><span class="sxs-lookup"><span data-stu-id="d29f3-183">Upgraded Azure.Storage.Blobs to 12.8.0</span></span>
* <span data-ttu-id="d29f3-184">Обновлена версия Azure.Storage.Files.Shares до 12.6.0.</span><span class="sxs-lookup"><span data-stu-id="d29f3-184">Upgraded Azure.Storage.Files.Shares to 12.6.0</span></span>
* <span data-ttu-id="d29f3-185">Обновлена версия Azure.Storage.Files.DataLake до 12.6.0.</span><span class="sxs-lookup"><span data-stu-id="d29f3-185">Upgraded Azure.Storage.Files.DataLake to 12.6.0</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d29f3-186">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d29f3-186">Az.Websites</span></span>
* <span data-ttu-id="d29f3-187">Добавлена поддержка для импорта сертификатов хранилища ключей в WebApp.</span><span class="sxs-lookup"><span data-stu-id="d29f3-187">Added support for Importing a key vault certificate to WebApp.</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="d29f3-188">Благодарим наших участников сообщества</span><span class="sxs-lookup"><span data-stu-id="d29f3-188">Thanks to our community contributors</span></span>
* <span data-ttu-id="d29f3-189">@atul-ram, обновление Set-AzEventHub.md (№ 13921).</span><span class="sxs-lookup"><span data-stu-id="d29f3-189">@atul-ram, Update Set-AzEventHub.md (#13921)</span></span>
* <span data-ttu-id="d29f3-190">Кристоф Бергмайстер (Christoph Bergmeister) [MVP] (@bergmeister), Set-AzDataLakeGen2AclRecursive.md — исправление опечатки (directiry -> directory) (№ 14082).</span><span class="sxs-lookup"><span data-stu-id="d29f3-190">Christoph Bergmeister [MVP] (@bergmeister), Set-AzDataLakeGen2AclRecursive.md - Fix typo (directiry -> directory) (#14082)</span></span>
* <span data-ttu-id="d29f3-191">Александр Шмидт (Alexander Schmidt) (@devdeer-alex), исправлена неработающая ссылка на рекомендации по добавлению изменений (№ 14009).</span><span class="sxs-lookup"><span data-stu-id="d29f3-191">Alexander Schmidt (@devdeer-alex), Fixed broken link to contribution guidelines (#14009)</span></span>
* <span data-ttu-id="d29f3-192">@JiangYuchun, обновление Get-AzApplicationGatewayAuthenticationCertificate.md (№ 13972).</span><span class="sxs-lookup"><span data-stu-id="d29f3-192">@JiangYuchun, Update Get-AzApplicationGatewayAuthenticationCertificate.md (#13972)</span></span>
* <span data-ttu-id="d29f3-193">Себастиан Олсен (Sebastian Olsen) (@Spacebjorn), исправление примера команды (№ 13901).</span><span class="sxs-lookup"><span data-stu-id="d29f3-193">Sebastian Olsen (@Spacebjorn), Corrected example command (#13901)</span></span>

## <a name="540---january-2021"></a><span data-ttu-id="d29f3-194">5.4.0 — январь 2021 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-194">5.4.0 - January 2021</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d29f3-195">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d29f3-195">Az.Accounts</span></span>
* <span data-ttu-id="d29f3-196">Отображение правильного идентификатора запроса клиента в сообщении отладки [№ 13745].</span><span class="sxs-lookup"><span data-stu-id="d29f3-196">Shown correct client request id on debug message [#13745]</span></span>
* <span data-ttu-id="d29f3-197">Добавлен общий тип исключений Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d29f3-197">Added common Azure PowerShell exception type</span></span>
* <span data-ttu-id="d29f3-198">Поддерживаемый API хранилища 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="d29f3-198">Supported storage API 2019-06-01</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d29f3-199">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d29f3-199">Az.Automation</span></span>
* <span data-ttu-id="d29f3-200">Исправлена проблема, из-за которой описание не было заполнено для расписаний управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="d29f3-200">Fixed issue where description was not populated for update management schedules</span></span>

#### <a name="azcosmosdb"></a><span data-ttu-id="d29f3-201">Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="d29f3-201">Az.CosmosDB</span></span>
* <span data-ttu-id="d29f3-202">Выпущена общедоступная версия модуля Az.CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="d29f3-202">General availability of 'Az.CosmosDB' module</span></span>
* <span data-ttu-id="d29f3-203">Ограничено действие командлета New-AzCosmosDBAccount, чтобы выполнять вызовы обновления к существующим учетным записям базы данных.</span><span class="sxs-lookup"><span data-stu-id="d29f3-203">Restricting New-AzCosmosDBAccount cmdlet to make update calls to existing Database Accounts.</span></span>
* <span data-ttu-id="d29f3-204">Реализация AnalyticalStorageTTL в SqlContainer.</span><span class="sxs-lookup"><span data-stu-id="d29f3-204">Introducing AnalyticalStorageTTL in SqlContainer.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d29f3-205">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d29f3-205">Az.IotHub</span></span>
* <span data-ttu-id="d29f3-206">Исправлена регрессия, связанная с созданием маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="d29f3-206">Fixed a regression regarding SAS token generation</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d29f3-207">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d29f3-207">Az.KeyVault</span></span>
* <span data-ttu-id="d29f3-208">Исправлена проблема в модуле управления секретами.</span><span class="sxs-lookup"><span data-stu-id="d29f3-208">Fixed an issue in Secret Management module</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d29f3-209">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d29f3-209">Az.LogicApp</span></span>
* <span data-ttu-id="d29f3-210">Исправлена проблема, из-за которой Get-AzLogicAppTriggerHistory и Get-AzLogicAppRunAction получали только первую страницу результатов [№ 9141].</span><span class="sxs-lookup"><span data-stu-id="d29f3-210">Fixed issue that 'Get-AzLogicAppTriggerHistory' and 'Get-AzLogicAppRunAction' only retrieving the first page of results [#9141]</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d29f3-211">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d29f3-211">Az.Monitor</span></span>
* <span data-ttu-id="d29f3-212">Добавлены командлеты для правил сбора данных:</span><span class="sxs-lookup"><span data-stu-id="d29f3-212">Added cmdlets for data collection rules:</span></span> 
    - <span data-ttu-id="d29f3-213">Get-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="d29f3-213">'Get-AzDataCollectionRule'</span></span>
    - <span data-ttu-id="d29f3-214">New-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="d29f3-214">'New-AzDataCollectionRule'</span></span>
    - <span data-ttu-id="d29f3-215">Set-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="d29f3-215">'Set-AzDataCollectionRule'</span></span>
    - <span data-ttu-id="d29f3-216">Update-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="d29f3-216">'Update-AzDataCollectionRule'</span></span>
    - <span data-ttu-id="d29f3-217">Remove-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="d29f3-217">'Remove-AzDataCollectionRule'</span></span>
* <span data-ttu-id="d29f3-218">Добавлены командлеты для связей правил сбора данных:</span><span class="sxs-lookup"><span data-stu-id="d29f3-218">Added cmdlets for data collection rules associations</span></span>
    - <span data-ttu-id="d29f3-219">Get-AzDataCollectionRuleAssociation</span><span class="sxs-lookup"><span data-stu-id="d29f3-219">'Get-AzDataCollectionRuleAssociation'</span></span>
    - <span data-ttu-id="d29f3-220">New-AzDataCollectionRuleAssociation</span><span class="sxs-lookup"><span data-stu-id="d29f3-220">'New-AzDataCollectionRuleAssociation'</span></span>
    - <span data-ttu-id="d29f3-221">Remove-AzDataCollectionRuleAssociation</span><span class="sxs-lookup"><span data-stu-id="d29f3-221">'Remove-AzDataCollectionRuleAssociation'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d29f3-222">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d29f3-222">Az.Network</span></span>
* <span data-ttu-id="d29f3-223">Добавлены новые командлеты для CRUD VpnGatewayNATRule:</span><span class="sxs-lookup"><span data-stu-id="d29f3-223">Added new cmdlets for CRUD of VpnGatewayNATRule.</span></span>
    - <span data-ttu-id="d29f3-224">New-AzVpnGatewayNatRule;</span><span class="sxs-lookup"><span data-stu-id="d29f3-224">'New-AzVpnGatewayNatRule'</span></span>
    - <span data-ttu-id="d29f3-225">Update-AzVpnGatewayNatRule;</span><span class="sxs-lookup"><span data-stu-id="d29f3-225">'Update-AzVpnGatewayNatRule'</span></span>
    - <span data-ttu-id="d29f3-226">Get-AzVpnGatewayNatRule;</span><span class="sxs-lookup"><span data-stu-id="d29f3-226">'Get-AzVpnGatewayNatRule'</span></span>
    - <span data-ttu-id="d29f3-227">Remove-AzVpnGatewayNatRule.</span><span class="sxs-lookup"><span data-stu-id="d29f3-227">'Remove-AzVpnGatewayNatRule'</span></span>  
* <span data-ttu-id="d29f3-228">Обновлены командлеты, чтобы задать правило NATRule для ресурса VpnGateway и связать его с ресурсом VpnSiteLinkConnection:</span><span class="sxs-lookup"><span data-stu-id="d29f3-228">Updated cmdlets to set NATRule on VpnGateway resource and associate it with VpnSiteLinkConnection resource.</span></span>
    - <span data-ttu-id="d29f3-229">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="d29f3-229">'New-AzVpnGateway'</span></span>
    - <span data-ttu-id="d29f3-230">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="d29f3-230">'Update-AzVpnGateway'</span></span> 
    - <span data-ttu-id="d29f3-231">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="d29f3-231">'New-AzVpnSiteLinkConnection'</span></span>
* <span data-ttu-id="d29f3-232">Обновлены командлеты для включения ConnectionMode в подключениях шлюзов виртуальных сетей:</span><span class="sxs-lookup"><span data-stu-id="d29f3-232">Updated cmdlets to enable setting of ConnectionMode on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="d29f3-233">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d29f3-233">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="d29f3-234">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d29f3-234">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="d29f3-235">Обновлен командлет New-AzFirewallPolicyApplicationRule:</span><span class="sxs-lookup"><span data-stu-id="d29f3-235">Updated 'New-AzFirewallPolicyApplicationRule' cmdlet:</span></span>
    - <span data-ttu-id="d29f3-236">добавлен параметр TargetUrl;</span><span class="sxs-lookup"><span data-stu-id="d29f3-236">Added parameter TargetUrl</span></span>
    - <span data-ttu-id="d29f3-237">добавлен параметр TerminateTLS.</span><span class="sxs-lookup"><span data-stu-id="d29f3-237">Added parameter TerminateTLS</span></span>
* <span data-ttu-id="d29f3-238">Добавлены новые командлеты для расширенных функций Брандмауэра Azure:</span><span class="sxs-lookup"><span data-stu-id="d29f3-238">Added new cmdlets for Azure Firewall Premium Features</span></span>
    - <span data-ttu-id="d29f3-239">New-AzFirewallPolicyIntrusionDetection</span><span class="sxs-lookup"><span data-stu-id="d29f3-239">'New-AzFirewallPolicyIntrusionDetection'</span></span>
    - <span data-ttu-id="d29f3-240">New-AzFirewallPolicyIntrusionDetectionBypassTraffic</span><span class="sxs-lookup"><span data-stu-id="d29f3-240">'New-AzFirewallPolicyIntrusionDetectionBypassTraffic'</span></span>
    - <span data-ttu-id="d29f3-241">New-AzFirewallPolicyIntrusionDetectionSignatureOverride</span><span class="sxs-lookup"><span data-stu-id="d29f3-241">'New-AzFirewallPolicyIntrusionDetectionSignatureOverride'</span></span>
* <span data-ttu-id="d29f3-242">Обновлен командлет New-AzFirewallPolicy:</span><span class="sxs-lookup"><span data-stu-id="d29f3-242">Updated New-AzFirewallPolicy cmdlet:</span></span>
    - <span data-ttu-id="d29f3-243">добавлен параметр -SkuTier;</span><span class="sxs-lookup"><span data-stu-id="d29f3-243">Added parameter -SkuTier</span></span>
    - <span data-ttu-id="d29f3-244">добавлен параметр -Identity;</span><span class="sxs-lookup"><span data-stu-id="d29f3-244">Added parameter -Identity</span></span>
    - <span data-ttu-id="d29f3-245">добавлен параметр -UserAssignedIdentityId;</span><span class="sxs-lookup"><span data-stu-id="d29f3-245">Added parameter -UserAssignedIdentityId</span></span>
    - <span data-ttu-id="d29f3-246">добавлен параметр -IntrusionDetection;</span><span class="sxs-lookup"><span data-stu-id="d29f3-246">Added parameter -IntrusionDetection</span></span>
    - <span data-ttu-id="d29f3-247">добавлен параметр -TransportSecurityName;</span><span class="sxs-lookup"><span data-stu-id="d29f3-247">Added parameter -TransportSecurityName</span></span>
    - <span data-ttu-id="d29f3-248">добавлен параметр -TransportSecurityKeyVaultSecretId.</span><span class="sxs-lookup"><span data-stu-id="d29f3-248">Added parameter -TransportSecurityKeyVaultSecretId</span></span>
* <span data-ttu-id="d29f3-249">Добавлен новый командлет для сбора данных о сопоставлениях безопасности IKE для подключений шлюза виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="d29f3-249">Added new cmdlet to fetch IKE Security Associations for Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="d29f3-250">Get-AzVirtualNetworkGatewayConnectionIkeSa</span><span class="sxs-lookup"><span data-stu-id="d29f3-250">'Get-AzVirtualNetworkGatewayConnectionIkeSa'</span></span>
* <span data-ttu-id="d29f3-251">Добавлена поддержка множественной проверки подлинности для p2sVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="d29f3-251">Added multiple Authentication support for p2sVpnGateway</span></span>
    - <span data-ttu-id="d29f3-252">Обновлены командлеты New-AzVpnServerConfiguration и Update-AzVpnServerConfiguration, разрешающие настройку нескольких параметров проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="d29f3-252">Updated New-AzVpnServerConfiguration and Update-AzVpnServerConfiguration to allow multiple authentication parameters to be set.</span></span>
* <span data-ttu-id="d29f3-253">Обновлены командлеты New-AzVpnGateway и New-AzP2sVpnGateway:</span><span class="sxs-lookup"><span data-stu-id="d29f3-253">Updated 'New-AzVpnGateway' and 'New-AzP2sVpnGateway' cmdlet:</span></span>
    - <span data-ttu-id="d29f3-254">добавлен параметр EnableRoutingPreferenceInternetFlag.</span><span class="sxs-lookup"><span data-stu-id="d29f3-254">Added parameter EnableRoutingPreferenceInternetFlag</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d29f3-255">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-255">Az.RecoveryServices</span></span>
* <span data-ttu-id="d29f3-256">Добавлена функция восстановления между регионами.</span><span class="sxs-lookup"><span data-stu-id="d29f3-256">Added Cross Region Restore feature.</span></span>  
* <span data-ttu-id="d29f3-257">Заблокировано получение конфигурации рабочей нагрузки, когда целевой элемент является группой доступности.</span><span class="sxs-lookup"><span data-stu-id="d29f3-257">Blocked getting workload config when target item is an availability group.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d29f3-258">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-258">Az.Resources</span></span>
* <span data-ttu-id="d29f3-259">Включена поддержка параметра -QueryString в командлетах New-Az\*Deployments.</span><span class="sxs-lookup"><span data-stu-id="d29f3-259">Added support for -QueryString parameter in New-Az\*Deployments cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="d29f3-260">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-260">Az.Sql</span></span>
* <span data-ttu-id="d29f3-261">Командлет Start-AzSqlInstanceDatabaseLogReplay сделан синхронным и добавлен флаг -AsJob.</span><span class="sxs-lookup"><span data-stu-id="d29f3-261">Made 'Start-AzSqlInstanceDatabaseLogReplay' cmdlet synchronous, added -AsJob flag</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d29f3-262">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d29f3-262">Az.Storage</span></span>
* <span data-ttu-id="d29f3-263">Исправлена проблема, из-за которой ContinuationToken никогда не имеет значение NULL при использовании большого двоичного объекта списка с параметром -IncludeVersion.</span><span class="sxs-lookup"><span data-stu-id="d29f3-263">Fix ContinuationToken never null when list blob with -IncludeVersion</span></span>
    - <span data-ttu-id="d29f3-264">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="d29f3-264">'Get-AzStorageBlob'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d29f3-265">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d29f3-265">Az.Websites</span></span>
* <span data-ttu-id="d29f3-266">Включена поддержка управляемых сертификатов Службы приложений:</span><span class="sxs-lookup"><span data-stu-id="d29f3-266">Added support for App Service Managed certificates</span></span>
    - <span data-ttu-id="d29f3-267">New-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="d29f3-267">'New-AzWebAppCertificate'</span></span>
    - <span data-ttu-id="d29f3-268">Remove-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="d29f3-268">'Remove-AzWebAppCertificate'</span></span>
* <span data-ttu-id="d29f3-269">Исправлена проблема, из-за которой пароль Docker удалялся из appsettings в Set-AzWebApp и Set-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="d29f3-269">Fixed issue that causes Docker Password to be removed from appsettings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="d29f3-270">Благодарим наших участников сообщества</span><span class="sxs-lookup"><span data-stu-id="d29f3-270">Thanks to our community contributors</span></span>
* <span data-ttu-id="d29f3-271">Иван Акчеуров (Ivan Akcheurov) (@ivanakcheurov), обновление Set-AzSecurityWorkspaceSetting.md (№ 13877).</span><span class="sxs-lookup"><span data-stu-id="d29f3-271">Ivan Akcheurov (@ivanakcheurov), Update Set-AzSecurityWorkspaceSetting.md (#13877)</span></span>
* <span data-ttu-id="d29f3-272">@javiermarasco, пример обновления (№ 13837).</span><span class="sxs-lookup"><span data-stu-id="d29f3-272">@javiermarasco, Update example (#13837)</span></span>
* <span data-ttu-id="d29f3-273">@jhaprakash26, обновление Set-AzVirtualNetwork.md (№ 13857).</span><span class="sxs-lookup"><span data-stu-id="d29f3-273">@jhaprakash26, Update Set-AzVirtualNetwork.md (#13857)</span></span>
* <span data-ttu-id="d29f3-274">Майкл Холмс (Michael Holmes) (@MichaelHolmesWP), обновление New-AzStorageTableStoredAccessPolicy.md (№ 13871).</span><span class="sxs-lookup"><span data-stu-id="d29f3-274">Michael Holmes (@MichaelHolmesWP), Update New-AzStorageTableStoredAccessPolicy.md (#13871)</span></span>
* <span data-ttu-id="d29f3-275">Майкл Джеймс (Michael James) (@mikejwhat), настройка Get-AzLogicAppTriggerHistory и Get-AzLogicAppRunAction на возвращение более 30 результатов (№ 13846).</span><span class="sxs-lookup"><span data-stu-id="d29f3-275">Michael James (@mikejwhat), Allow Get-AzLogicAppTriggerHistory and Get-AzLogicAppRunAction to return more than 30 results (#13846)</span></span>
* <span data-ttu-id="d29f3-276">@Willem-J-an, исправление проблемы, из-за которой пароль Docker удалялся из appsettings в Set-AzWebApp(Slot) (№ 13866).</span><span class="sxs-lookup"><span data-stu-id="d29f3-276">@Willem-J-an, Fix bug causing Docker Password to be removed from appsettings in Set-AzWebApp(Slot) (#13866)</span></span>

## <a name="530---december-2020"></a><span data-ttu-id="d29f3-277">5.3.0 — декабрь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-277">5.3.0 - December 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d29f3-278">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d29f3-278">Az.Accounts</span></span>
* <span data-ttu-id="d29f3-279">Исправлена проблема, из-за которой прокси-сервер HTTP не учитывался в Windows PowerShell [№ 13647].</span><span class="sxs-lookup"><span data-stu-id="d29f3-279">Fixed the issue that Http proxy is not respected in Windows PowerShell [#13647]</span></span>
* <span data-ttu-id="d29f3-280">Улучшен журнал отладки для длительных операций в созданных модулях.</span><span class="sxs-lookup"><span data-stu-id="d29f3-280">Improved debug log of long running operations in generated modules</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d29f3-281">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d29f3-281">Az.Automation</span></span>
* <span data-ttu-id="d29f3-282">Исправлена проблема, из-за которой упакованную строку PSObject не удавалось преобразовать в строку JSON с помощью параметров Start-AzAutomationRunbook [№ 13240].</span><span class="sxs-lookup"><span data-stu-id="d29f3-282">Fixed issue that parameters of 'Start-AzAutomationRunbook' cannot convert PSObject wrapped string to JSON string [#13240]</span></span>
* <span data-ttu-id="d29f3-283">Исправлено средство заполнения расположения для командлета New-AzAutomationUpdateManagementAzureQuery.</span><span class="sxs-lookup"><span data-stu-id="d29f3-283">Fixed location completer for New-AzAutomationUpdateManagementAzureQuery cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d29f3-284">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-284">Az.Compute</span></span>
* <span data-ttu-id="d29f3-285">В командлеты Get-AzVMDscExtensionStatus и Get-AzVMDscExtension добавлен новый параметр VM в новом наборе параметров VMParameterSet.</span><span class="sxs-lookup"><span data-stu-id="d29f3-285">New parameter 'VM' in new parameter set 'VMParameterSet' added to 'Get-AzVMDscExtensionStatus' and 'Get-AzVMDscExtension' cmdlets.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="d29f3-286">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="d29f3-286">Az.Databricks</span></span>
* <span data-ttu-id="d29f3-287">Исправлена проблема, из-за которой иногда возвращался результат New-AzDatabricksVNetPeering перед полной подготовкой (https://github.com/Azure/autorest.powershell/issues/610)</span><span class="sxs-lookup"><span data-stu-id="d29f3-287">Fixed an issue that may cause 'New-AzDatabricksVNetPeering' to return before it is fully provisioned (https://github.com/Azure/autorest.powershell/issues/610)</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d29f3-288">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d29f3-288">Az.DataFactory</span></span>
* <span data-ttu-id="d29f3-289">Исправлена команда Invoke-AzDataFactoryV2Pipeline для устранения проблемы с SupportsShouldProcess.</span><span class="sxs-lookup"><span data-stu-id="d29f3-289">Fixed the command 'Invoke-AzDataFactoryV2Pipeline' for SupportsShouldProcess issue</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="d29f3-290">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="d29f3-290">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="d29f3-291">В пул узлов добавлено свойство StartVMOnConnect.</span><span class="sxs-lookup"><span data-stu-id="d29f3-291">Added StartVMOnConnect property to hostpool.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d29f3-292">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d29f3-292">Az.HDInsight</span></span>
* <span data-ttu-id="d29f3-293">В класс AzureHDInsightHostInfo добавлены свойства Fqdn и EffectiveDiskEncryptionKeyUrl.</span><span class="sxs-lookup"><span data-stu-id="d29f3-293">Added properties: Fqdn and EffectiveDiskEncryptionKeyUrl in the class AzureHDInsightHostInfo.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d29f3-294">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d29f3-294">Az.KeyVault</span></span>
* <span data-ttu-id="d29f3-295">В Get-AzKeyVaultSecret добавлен новый параметр -AsPlainText для прямого возврата секрета в виде обычного текста [№ 13630].</span><span class="sxs-lookup"><span data-stu-id="d29f3-295">Added a new parameter '-AsPlainText' to 'Get-AzKeyVaultSecret' to directly return the secret in plain text [#13630]</span></span>
* <span data-ttu-id="d29f3-296">Поддерживается выборочное восстановление ключа из управляемой полной резервной копии HSM [№ 13526].</span><span class="sxs-lookup"><span data-stu-id="d29f3-296">Supported selective restore a key from a managed HSM full backup [#13526]</span></span>
* <span data-ttu-id="d29f3-297">Устранены некоторые незначительные проблемы [№ 13583] [№ 13584].</span><span class="sxs-lookup"><span data-stu-id="d29f3-297">Fixed some minor issues [#13583] [#13584]</span></span>
* <span data-ttu-id="d29f3-298">В модуль SecretManagement добавлены отсутствующие возвращаемые объекты Get-Secret.</span><span class="sxs-lookup"><span data-stu-id="d29f3-298">Added missing return objects of 'Get-Secret' in SecretManagement module</span></span>
* <span data-ttu-id="d29f3-299">Исправлена проблема, из-за которой хранилище иногда создавалось без политики доступа по умолчанию [№ 13687].</span><span class="sxs-lookup"><span data-stu-id="d29f3-299">Fixed an issue that may cause vault to be created without default access policy [#13687]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="d29f3-300">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="d29f3-300">Az.Kusto</span></span>
* <span data-ttu-id="d29f3-301">Версия API обновлена до 2020-09-18.</span><span class="sxs-lookup"><span data-stu-id="d29f3-301">Updated API version to 2020-09-18.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d29f3-302">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d29f3-302">Az.Network</span></span>
* <span data-ttu-id="d29f3-303">Исправлена проблема с удалением пиринга и командлетом подключения для сценария ExpressRouteCircuit:</span><span class="sxs-lookup"><span data-stu-id="d29f3-303">Fixed issue in remove peering and connection cmdlet for ExpressRouteCircuit scenario</span></span>
    - <span data-ttu-id="d29f3-304">Remove-AzExpressRouteCircuitPeeringConfig и Remove-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="d29f3-304">'Remove-AzExpressRouteCircuitPeeringConfig' and 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d29f3-305">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d29f3-305">Az.PolicyInsights</span></span>
* <span data-ttu-id="d29f3-306">Добавлена поддержка возврата страничных результатов для Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="d29f3-306">Added support for returning paginated results for Get-AzPolicyState</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d29f3-307">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-307">Az.RecoveryServices</span></span>
* <span data-ttu-id="d29f3-308">Включена функция обратимого удаления для SQL.</span><span class="sxs-lookup"><span data-stu-id="d29f3-308">Enabled softdelete feature for SQL.</span></span>
* <span data-ttu-id="d29f3-309">Исправлена проблема с восстановлением групп доступности AG и удалена проверка имени контейнера.</span><span class="sxs-lookup"><span data-stu-id="d29f3-309">Fixed SQL AG restore and removed the container name check.</span></span>
* <span data-ttu-id="d29f3-310">Изменен формат имени контейнера для элемента резервного копирования Файлов Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-310">Changed container name format for Azure Files backup item.</span></span>
* <span data-ttu-id="d29f3-311">Добавлена поддержка функции CMK для хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="d29f3-311">Added CMK feature support for Recovery services vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d29f3-312">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-312">Az.Resources</span></span>
* <span data-ttu-id="d29f3-313">Устранена проблема с исключением NullRef в New-AzureManagedApplication и Set-AzureManagedApplication.</span><span class="sxs-lookup"><span data-stu-id="d29f3-313">Fixed a NullRef exception issue in 'New-AzureManagedApplication' and 'Set-AzureManagedApplication'.</span></span>
* <span data-ttu-id="d29f3-314">Обновлен пакет SDK Azure Resource Manager для использования последней общедоступной версии API DeploymentScripts: 2020-10-01.</span><span class="sxs-lookup"><span data-stu-id="d29f3-314">Updated Azure Resource Manager SDK to use latest DeploymentScripts GA api-version: 2020-10-01.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d29f3-315">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d29f3-315">Az.ServiceFabric</span></span>
* <span data-ttu-id="d29f3-316">Внесены исправления в Add-AzServiceFabricNodeType.</span><span class="sxs-lookup"><span data-stu-id="d29f3-316">Fixed 'Add-AzServiceFabricNodeType'.</span></span> <span data-ttu-id="d29f3-317">Добавлен тип узла, который можно использовать для кластера Service Fabric перед созданием масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="d29f3-317">Added node type to service fabric cluster before creating virtual machine scale set.</span></span>

#### <a name="azsql"></a><span data-ttu-id="d29f3-318">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-318">Az.Sql</span></span>
* <span data-ttu-id="d29f3-319">Исправлено описание параметра для команды InstanceFailoverGroup.</span><span class="sxs-lookup"><span data-stu-id="d29f3-319">Fixed parameter description for 'InstanceFailoverGroup' command.</span></span>
* <span data-ttu-id="d29f3-320">Обновлена логика, согласно которой данные типа schemaName, tableName и columnName извлекались из идентификатора команд классификации данных SQL.</span><span class="sxs-lookup"><span data-stu-id="d29f3-320">Updated the logic in which schemaName, tableName and columnName are being extracted from the id of SQL Data Classification commands.</span></span>
* <span data-ttu-id="d29f3-321">Исправлены поля Status и StatusMessage в Get-AzSqlDatabaseImportExportStatus, чтобы обеспечить соответствие документации.</span><span class="sxs-lookup"><span data-stu-id="d29f3-321">Fixed Status and StatusMessage fields in 'Get-AzSqlDatabaseImportExportStatus' to conform to documentation</span></span>
* <span data-ttu-id="d29f3-322">Добавлены командлеты аудита для операций поддержки Майкрософт (DevOps): Get-AzSqlServerMSSupportAudit, Set-AzSqlServerMSSupportAudit, Remove-AzSqlServerMSSupportAudit.</span><span class="sxs-lookup"><span data-stu-id="d29f3-322">Added Microsoft support operations (DevOps) auditing cmdlets: Get-AzSqlServerMSSupportAudit, Set-AzSqlServerMSSupportAudit, Remove-AzSqlServerMSSupportAudit</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d29f3-323">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d29f3-323">Az.Storage</span></span>
* <span data-ttu-id="d29f3-324">Поддерживаемые операции создания, обновления, получения и перечисления EncryptionScope учетной записи хранения:</span><span class="sxs-lookup"><span data-stu-id="d29f3-324">Supported create/update/get/list EncryptionScope of a Storage account</span></span>
    - <span data-ttu-id="d29f3-325">New-AzStorageEncryptionScope;</span><span class="sxs-lookup"><span data-stu-id="d29f3-325">'New-AzStorageEncryptionScope'</span></span>
    - <span data-ttu-id="d29f3-326">Update-AzStorageEncryptionScope;</span><span class="sxs-lookup"><span data-stu-id="d29f3-326">'Update-AzStorageEncryptionScope'</span></span>
    - <span data-ttu-id="d29f3-327">Get-AzStorageEncryptionScope.</span><span class="sxs-lookup"><span data-stu-id="d29f3-327">'Get-AzStorageEncryptionScope'</span></span>
* <span data-ttu-id="d29f3-328">Поддерживаемые операции создания контейнера и отправки большого двоичного объекта с параметром области шифрования:</span><span class="sxs-lookup"><span data-stu-id="d29f3-328">Supported create container and upload blob with Encryption Scope setting</span></span>
    - <span data-ttu-id="d29f3-329">New-AzRmStorageContainer;</span><span class="sxs-lookup"><span data-stu-id="d29f3-329">'New-AzRmStorageContainer'</span></span>
    - <span data-ttu-id="d29f3-330">New-AzStorageContainer;</span><span class="sxs-lookup"><span data-stu-id="d29f3-330">'New-AzStorageContainer'</span></span>
    - <span data-ttu-id="d29f3-331">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d29f3-331">'Set-AzStorageBlobContent'</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="d29f3-332">Благодарим наших участников сообщества</span><span class="sxs-lookup"><span data-stu-id="d29f3-332">Thanks to our community contributors</span></span>
* <span data-ttu-id="d29f3-333">Андреас Уолтер (Andreas Wolter) (@AndreasWolter), удален маркетинговый стиль, улучшен пример фильтра (№ 13671).</span><span class="sxs-lookup"><span data-stu-id="d29f3-333">Andreas Wolter (@AndreasWolter), removed marketing language, better example filter (#13671)</span></span>
* <span data-ttu-id="d29f3-334">Тиджани Белмансаур (Tidjani Belmansour) (@BelRarr), обновлен файл Get-AzBillingInvoice.md (№ 13634).</span><span class="sxs-lookup"><span data-stu-id="d29f3-334">Tidjani Belmansour (@BelRarr), Update Get-AzBillingInvoice.md (#13634)</span></span>
* <span data-ttu-id="d29f3-335">Дэвид Клемпфнер (David Klempfner) (@DavidKlempfner):</span><span class="sxs-lookup"><span data-stu-id="d29f3-335">David Klempfner (@DavidKlempfner)</span></span>
  * <span data-ttu-id="d29f3-336">исправлена орфографическая ошибка (№ 13677);</span><span class="sxs-lookup"><span data-stu-id="d29f3-336">Fixed spelling mistake (#13677)</span></span>
  * <span data-ttu-id="d29f3-337">обновлен файл PSMetricNoDetails.cs (№ 13676).</span><span class="sxs-lookup"><span data-stu-id="d29f3-337">Update PSMetricNoDetails.cs (#13676)</span></span>
* <span data-ttu-id="d29f3-338">@kilobyte97, исправлена ошибка командлета для удаления конфигурации (№ 13655).</span><span class="sxs-lookup"><span data-stu-id="d29f3-338">@kilobyte97, bugfix for remove cmdlet to delete config (#13655)</span></span>
* <span data-ttu-id="d29f3-339">@kongou-ae, обновлен файл Set-AzFirewall.md (№ 13727).</span><span class="sxs-lookup"><span data-stu-id="d29f3-339">@kongou-ae, Update Set-AzFirewall.md (#13727)</span></span>
* <span data-ttu-id="d29f3-340">@MasterKuat, исправлено переключение между заголовком и кодом в документации (№ 13666).</span><span class="sxs-lookup"><span data-stu-id="d29f3-340">@MasterKuat, Fix swap between title and code in documentation (#13666)</span></span>
* <span data-ttu-id="d29f3-341">NickT (@nukeulis), обновлен файл Set-AzContext.md (№ 13702).</span><span class="sxs-lookup"><span data-stu-id="d29f3-341">NickT (@nukeulis), Update Set-AzContext.md (#13702)</span></span>
* <span data-ttu-id="d29f3-342">@PaulHCode, обновлен файл Start-AzJitNetworkAccessPolicy.md: исправлен пример для отображения правильного демонстрируемого командлета (№ 13713).</span><span class="sxs-lookup"><span data-stu-id="d29f3-342">@PaulHCode, Update Start-AzJitNetworkAccessPolicy.md - Fix the Example to display the proper cmdlet being demonstrated (#13713)</span></span>
* <span data-ttu-id="d29f3-343">Райан Борстельманн (Ryan Borstelmann) (@ryanborMSFT), удален идентификатор подписки (№ 13715).</span><span class="sxs-lookup"><span data-stu-id="d29f3-343">Ryan Borstelmann (@ryanborMSFT), Removed Subscription ID (#13715)</span></span>
* <span data-ttu-id="d29f3-344">Шашикант Шакья (Shashikant Shakya) (@shshakya), обновлен файл Set-AzSqlDatabase.md (№ 13674).</span><span class="sxs-lookup"><span data-stu-id="d29f3-344">Shashikant Shakya (@shshakya), Update Set-AzSqlDatabase.md (#13674)</span></span>
* <span data-ttu-id="d29f3-345">Себастиан Олсен (Sebastian Olsen) (@Spacebjorn),обновлен файл Get-AzRecoveryServicesBackupItem.md (№ 13719).</span><span class="sxs-lookup"><span data-stu-id="d29f3-345">Sebastian Olsen (@Spacebjorn), Update Get-AzRecoveryServicesBackupItem.md (#13719)</span></span>

## <a name="520---december-2020"></a><span data-ttu-id="d29f3-346">5.2.0 — декабрь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-346">5.2.0 - December 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d29f3-347">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d29f3-347">Az.Accounts</span></span>
* <span data-ttu-id="d29f3-348">Теперь выполняется анализ времени ExpiresOn из необработанного токена, если не удается получить эти данные из базовой библиотеки.</span><span class="sxs-lookup"><span data-stu-id="d29f3-348">Managed to parse ExpiresOn time from raw token if could not get from underlying library</span></span>
* <span data-ttu-id="d29f3-349">Улучшено сообщение с предупреждением, если недоступна интерактивная аутентификация.</span><span class="sxs-lookup"><span data-stu-id="d29f3-349">Improved warning message if Interactive authentication is unavailable</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d29f3-350">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d29f3-350">Az.ApiManagement</span></span>
* <span data-ttu-id="d29f3-351">[Критическое изменение] New-AzApiManagementProduct по умолчанию не имеет ограничения на подписку.</span><span class="sxs-lookup"><span data-stu-id="d29f3-351">[Breaking change] 'New-AzApiManagementProduct' by default has no subscription limit.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d29f3-352">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-352">Az.Compute</span></span>
* <span data-ttu-id="d29f3-353">Изменен командлет Get-AzVm для фильтрации по параметру -Name до проверки регулирования вследствие большого числа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-353">Edited Get-AzVm to filter by '-Name' prior to checking for throttling due to too many resources.</span></span> 
* <span data-ttu-id="d29f3-354">Добавлен новый командлет Start-AzVmssRollingExtensionUpgrade.</span><span class="sxs-lookup"><span data-stu-id="d29f3-354">New cmdlet 'Start-AzVmssRollingExtensionUpgrade'.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="d29f3-355">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d29f3-355">Az.ContainerRegistry</span></span>
* <span data-ttu-id="d29f3-356">Реализована поддержка параметра Name для Get-AzContainerRegistryUsage и значение из входных данных конвейера для этого командлета. [13605]</span><span class="sxs-lookup"><span data-stu-id="d29f3-356">Supported parameter 'Name' for and value from pipeline input for 'Get-AzContainerRegistryUsage' [#13605]</span></span>
* <span data-ttu-id="d29f3-357">Улучшены исключения для Connect-AzContainerRegistry.</span><span class="sxs-lookup"><span data-stu-id="d29f3-357">Polished exceptions for 'Connect-AzContainerRegistry'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d29f3-358">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d29f3-358">Az.DataFactory</span></span>
* <span data-ttu-id="d29f3-359">Пакет SDK ADF для .NET обновлен до версии 4.13.0.</span><span class="sxs-lookup"><span data-stu-id="d29f3-359">Updated ADF .Net SDK version to 4.13.0</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="d29f3-360">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="d29f3-360">Az.HealthcareApis</span></span>
* <span data-ttu-id="d29f3-361">Добавлена поддержка ключей, управляемых клиентом.</span><span class="sxs-lookup"><span data-stu-id="d29f3-361">Added support for customer managed keys</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d29f3-362">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d29f3-362">Az.IotHub</span></span>
* <span data-ttu-id="d29f3-363">Исправлена ошибка маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="d29f3-363">Fixed an issue of SAS token.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d29f3-364">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d29f3-364">Az.KeyVault</span></span>
* <span data-ttu-id="d29f3-365">Добавлена поддержка all в качестве параметра при настройке политик доступа для хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="d29f3-365">Supported 'all' as an option when setting key vault access policies</span></span>
* <span data-ttu-id="d29f3-366">Реализована поддержка новой версии модуля SecretManagement [13366].</span><span class="sxs-lookup"><span data-stu-id="d29f3-366">Supported new version of SecretManagement module [#13366]</span></span>
* <span data-ttu-id="d29f3-367">Реализована поддержка ByteArray, String, PSCredential и Hashtable для SecretValue в SecretManagementModule [12190].</span><span class="sxs-lookup"><span data-stu-id="d29f3-367">Supported ByteArray, String, PSCredential and Hashtable for 'SecretValue' in SecretManagementModule [#12190]</span></span>
* <span data-ttu-id="d29f3-368">[Критическое изменение] Перепроектирована контактная зона API командлетов, связанных с управляемым устройством HSM.</span><span class="sxs-lookup"><span data-stu-id="d29f3-368">[Breaking change] redesigned the API surface of cmdlets related to managed HSM.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d29f3-369">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d29f3-369">Az.Monitor</span></span>
* <span data-ttu-id="d29f3-370">Изменен параметр Rule командлета New-AzAutoscaleProfile для приема пустого списка.</span><span class="sxs-lookup"><span data-stu-id="d29f3-370">Changed parameter 'Rule' of 'New-AzAutoscaleProfile' to accept empty list.</span></span> <span data-ttu-id="d29f3-371">[12903]</span><span class="sxs-lookup"><span data-stu-id="d29f3-371">[#12903]</span></span>
* <span data-ttu-id="d29f3-372">Добавлены новые командлеты для более гибкой поддержки создания диагностических параметров:</span><span class="sxs-lookup"><span data-stu-id="d29f3-372">Added new cmdlets to support creating diagnostic settings more flexible:</span></span>
    * <span data-ttu-id="d29f3-373">Get-AzDiagnosticSettingCategory;</span><span class="sxs-lookup"><span data-stu-id="d29f3-373">'Get-AzDiagnosticSettingCategory'</span></span>
    * <span data-ttu-id="d29f3-374">New-AzDiagnosticSetting;</span><span class="sxs-lookup"><span data-stu-id="d29f3-374">'New-AzDiagnosticSetting'</span></span>
    * <span data-ttu-id="d29f3-375">New-AzDiagnosticDetailSetting.</span><span class="sxs-lookup"><span data-stu-id="d29f3-375">'New-AzDiagnosticDetailSetting'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d29f3-376">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-376">Az.RecoveryServices</span></span>
* <span data-ttu-id="d29f3-377">Внесены изменения в текст справки и названия набора параметров для командлета Restore-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="d29f3-377">Made help text and parameter set name changes to 'Restore-AzRecoveryServicesBackupItem' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d29f3-378">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-378">Az.Resources</span></span>
* <span data-ttu-id="d29f3-379">Добавлена поддержка параметра -Tag в командлеты Set-AzTemplateSpec и New-AzTemplateSpec.</span><span class="sxs-lookup"><span data-stu-id="d29f3-379">Added '-Tag' parameter support to 'Set-AzTemplateSpec' and 'New-AzTemplateSpec'</span></span>
* <span data-ttu-id="d29f3-380">Добавлена поддержка отображения тегов в форматировщик по умолчанию для функции "Спецификации шаблонов".</span><span class="sxs-lookup"><span data-stu-id="d29f3-380">Added Tag display support to default formatter for Template Specs</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="d29f3-381">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d29f3-381">Az.ServiceFabric</span></span>
* <span data-ttu-id="d29f3-382">Добавлен пример в командлет Set-AzServiceFabricSetting с параметром SettingsSectionDescription.</span><span class="sxs-lookup"><span data-stu-id="d29f3-382">Added example to 'Set-AzServiceFabricSetting' with SettingsSectionDescription param</span></span>
* <span data-ttu-id="d29f3-383">Обновлены связанные с приложениями командлеты для отображения сведений о том, что поддержка доступна только для ресурсов, развернутых через ARM.</span><span class="sxs-lookup"><span data-stu-id="d29f3-383">Updated application related cmdlets to call out that support is only for ARM deployed resources</span></span>
* <span data-ttu-id="d29f3-384">Помечены нерекомендуемыми командлеты сертификации кластера Add-AzureRmServiceFabricClusterCertificate и Remove-AzureRmServiceFabricClusterCertificate.</span><span class="sxs-lookup"><span data-stu-id="d29f3-384">Marked for deprecation cluster cert cmdlets 'Add-AzureRmServiceFabricClusterCertificate' and 'Remove-AzureRmServiceFabricClusterCertificate'</span></span>

#### <a name="azsql"></a><span data-ttu-id="d29f3-385">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-385">Az.Sql</span></span>
* <span data-ttu-id="d29f3-386">Добавлен тип SecondaryType к следующим командлетам:</span><span class="sxs-lookup"><span data-stu-id="d29f3-386">Added SecondaryType to the following:</span></span> 
    - <span data-ttu-id="d29f3-387">New-AzSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="d29f3-387">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="d29f3-388">Set-AzSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="d29f3-388">'Set-AzSqlDatabase'</span></span>
    - <span data-ttu-id="d29f3-389">New-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="d29f3-389">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="d29f3-390">Добавлен параметр HighAvailabilityReplicaCount к следующим командлетам:</span><span class="sxs-lookup"><span data-stu-id="d29f3-390">Added HighAvailabilityReplicaCount to the following:</span></span> 
    - <span data-ttu-id="d29f3-391">New-AzSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="d29f3-391">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="d29f3-392">Set-AzSqlDatabase.</span><span class="sxs-lookup"><span data-stu-id="d29f3-392">'Set-AzSqlDatabase'</span></span>
* <span data-ttu-id="d29f3-393">ReadReplicaCount теперь является псевдонимом HighAvailabilityReplicaCount для таких командлетов:</span><span class="sxs-lookup"><span data-stu-id="d29f3-393">Made ReadReplicaCount an alias of HighAvailabilityReplicaCount in the following:</span></span> 
    - <span data-ttu-id="d29f3-394">New-AzSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="d29f3-394">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="d29f3-395">Set-AzSqlDatabase.</span><span class="sxs-lookup"><span data-stu-id="d29f3-395">'Set-AzSqlDatabase'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d29f3-396">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d29f3-396">Az.Storage</span></span>
* <span data-ttu-id="d29f3-397">Реализована поддержка для отправки файла Azure размером до 4 TиБ.</span><span class="sxs-lookup"><span data-stu-id="d29f3-397">Supported upload Azure File size up to 4 TiB</span></span>
    - <span data-ttu-id="d29f3-398">Set-AzStorageFileContent;</span><span class="sxs-lookup"><span data-stu-id="d29f3-398">'Set-AzStorageFileContent'</span></span>
* <span data-ttu-id="d29f3-399">Версия Azure.Storage.Blobs обновлена до 12.7.0.</span><span class="sxs-lookup"><span data-stu-id="d29f3-399">Upgraded Azure.Storage.Blobs to 12.7.0</span></span>
* <span data-ttu-id="d29f3-400">Версия Azure.Storage.Files.Shares обновлена до 12.5.0.</span><span class="sxs-lookup"><span data-stu-id="d29f3-400">Upgraded Azure.Storage.Files.Shares to 12.5.0</span></span>
* <span data-ttu-id="d29f3-401">Версия Azure.Storage.Files.DataLake обновлена до 12.5.0.</span><span class="sxs-lookup"><span data-stu-id="d29f3-401">Upgraded Azure.Storage.Files.DataLake to 12.5.0</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="d29f3-402">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="d29f3-402">Az.StorageSync</span></span>
* <span data-ttu-id="d29f3-403">Добавлена функция политики распределения по уровням в службе "Синхронизация файлов" с политикой скачивания и режимом локального кэша.</span><span class="sxs-lookup"><span data-stu-id="d29f3-403">Added Sync tiering policy feature with download policy and local cache mode</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d29f3-404">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d29f3-404">Az.Websites</span></span>
* <span data-ttu-id="d29f3-405">Теперь предотвращается создание дубликатов для правил ограничения доступа.</span><span class="sxs-lookup"><span data-stu-id="d29f3-405">Prevent duplicate access restriction rules</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="d29f3-406">Благодарим наших участников сообщества</span><span class="sxs-lookup"><span data-stu-id="d29f3-406">Thanks to our community contributors</span></span>
* <span data-ttu-id="d29f3-407">Эндрю Доусона (Andrew Dawson) (@dawsonar802) за обновление Get-AzKeyVaultCertificate.md (получение сертификата и его сохранение в виде раздела pfx для работы с PowerShell Core) (13557).</span><span class="sxs-lookup"><span data-stu-id="d29f3-407">Andrew Dawson (@dawsonar802), Update Get-AzKeyVaultCertificate.md - Get cert and save it as pfx section to work with PowerShell Core (#13557)</span></span>
* <span data-ttu-id="d29f3-408">@iviark за обновление BYOK Powershell в API для здравоохранения (13518).</span><span class="sxs-lookup"><span data-stu-id="d29f3-408">@iviark, Healthcare APIs Powershell BYOK Updates (#13518)</span></span>
* <span data-ttu-id="d29f3-409">Джона Дакмантона (John Duckmanton) (@johnduckmanton) за исправление написания TagPatchOperation (13508).</span><span class="sxs-lookup"><span data-stu-id="d29f3-409">John Duckmanton (@johnduckmanton), Correct spelling of TagPatchOperation (#13508)</span></span>
* <span data-ttu-id="d29f3-410">Майкла Джеймса (Michael James) (@mikejwhat):</span><span class="sxs-lookup"><span data-stu-id="d29f3-410">Michael James (@mikejwhat)</span></span>
  * <span data-ttu-id="d29f3-411">за корректировку справки по Get-AzLogicAppRunHistory (13513).</span><span class="sxs-lookup"><span data-stu-id="d29f3-411">Get-AzLogicAppRunHistory Help Tidy (#13513)</span></span>
* <span data-ttu-id="d29f3-412">Ричарда де Цварта (Richard de Zwart) (@mountain65):</span><span class="sxs-lookup"><span data-stu-id="d29f3-412">Richard de Zwart (@mountain65)</span></span>
  * <span data-ttu-id="d29f3-413">за обновление Update-AzAppConfigurationStore.md (13485);</span><span class="sxs-lookup"><span data-stu-id="d29f3-413">Update Update-AzAppConfigurationStore.md (#13485)</span></span>
  * <span data-ttu-id="d29f3-414">за обновление Update New-AzCosmosDBAccount.md (13490).</span><span class="sxs-lookup"><span data-stu-id="d29f3-414">Update New-AzCosmosDBAccount.md (#13490)</span></span>
* <span data-ttu-id="d29f3-415">@SteppingRazor, New-AzApiManagementProduct: за изменение значения по умолчанию для параметра SubscriptionsLimit на None (13457).</span><span class="sxs-lookup"><span data-stu-id="d29f3-415">@SteppingRazor, New-AzApiManagementProduct: Change SubscriptionsLimit parameter default value to None (#13457)</span></span>
* <span data-ttu-id="d29f3-416">Стива Баркетта (Steve Burkett) (@SteveBurkettNZ) за исправление ошибки для параметра WorkspaceResourceId в примере (13589).</span><span class="sxs-lookup"><span data-stu-id="d29f3-416">Steve Burkett (@SteveBurkettNZ), Fix Typo for WorkspaceResourceId parameter in example (#13589)</span></span>

## <a name="510---november-2020"></a><span data-ttu-id="d29f3-417">5.1.0 — ноябрь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-417">5.1.0 - November 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d29f3-418">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d29f3-418">Az.Accounts</span></span>
* <span data-ttu-id="d29f3-419">Исправлена проблема, из-за которой TenantId может не учитываться при использовании Connect-AzAccount -DeviceCode [№13477].</span><span class="sxs-lookup"><span data-stu-id="d29f3-419">Fixed an issue that TenantId may be not respected if using 'Connect-AzAccount -DeviceCode'[#13477]</span></span>
* <span data-ttu-id="d29f3-420">Добавлен новый командлет Get-AzAccessToken.</span><span class="sxs-lookup"><span data-stu-id="d29f3-420">Added new cmdlet 'Get-AzAccessToken'</span></span>
* <span data-ttu-id="d29f3-421">Исправлена проблема, которая возникает, если путь к профилю пользователя недоступен.</span><span class="sxs-lookup"><span data-stu-id="d29f3-421">Fixed an issue that error happens if user profile path is inaccessible</span></span>
* <span data-ttu-id="d29f3-422">Исправлена проблема, вызывающая ошибку записи объекта при использовании Connect-AzAccount [№13419].</span><span class="sxs-lookup"><span data-stu-id="d29f3-422">Fixed an issue causing Write-Object error during Connect-AzAccount [#13419]</span></span>
* <span data-ttu-id="d29f3-423">Добавлен параметр ContainerRegistryEndpointSuffix в Add-AzEnvironment и Set-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="d29f3-423">Added parameter 'ContainerRegistryEndpointSuffix' to: 'Add-AzEnvironment', 'Set-AzEnvironment'</span></span> 
* <span data-ttu-id="d29f3-424">Поддерживается прерывание входа при нажатии клавиш <kbd>CTRL</kbd>+<kbd>C</kbd>.</span><span class="sxs-lookup"><span data-stu-id="d29f3-424">Supported interrupting login by hitting <kbd>CTRL</kbd>+<kbd>C</kbd></span></span>
* <span data-ttu-id="d29f3-425">Исправлена проблема, из-за которой командлет Connect-AzAccount -KeyVaultAccessToken не работает [№13127].</span><span class="sxs-lookup"><span data-stu-id="d29f3-425">Fixed an issue causing 'Connect-AzAccount -KeyVaultAccessToken' not working [#13127]</span></span>
* <span data-ttu-id="d29f3-426">Исправлена пустая ссылка и обработка метода без учета регистра в Invoke-AzRestMethod.</span><span class="sxs-lookup"><span data-stu-id="d29f3-426">Fixed null reference and method case insensitive in 'Invoke-AzRestMethod'</span></span>

#### <a name="azaks"></a><span data-ttu-id="d29f3-427">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="d29f3-427">Az.Aks</span></span>
* <span data-ttu-id="d29f3-428">Исправлена проблема, из-за которой пользователь не может использовать субъект-службу для создания нового кластера Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="d29f3-428">Fixed the issue that user cannot use service principal to create a new Kubernetes cluster.</span></span> <span data-ttu-id="d29f3-429">[№13012]</span><span class="sxs-lookup"><span data-stu-id="d29f3-429">[#13012]</span></span>

#### <a name="azappconfiguration"></a><span data-ttu-id="d29f3-430">Az.AppConfiguration</span><span class="sxs-lookup"><span data-stu-id="d29f3-430">Az.AppConfiguration</span></span>
* <span data-ttu-id="d29f3-431">Вышла общедоступная версия модуля Az.AppConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d29f3-431">General availability of 'Az.AppConfiguration' module</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d29f3-432">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d29f3-432">Az.DataFactory</span></span>
* <span data-ttu-id="d29f3-433">Улучшено сообщение об ошибке для команды New-AzDataFactoryV2LinkedServiceEncryptedCredential.</span><span class="sxs-lookup"><span data-stu-id="d29f3-433">Improved error message of 'New-AzDataFactoryV2LinkedServiceEncryptedCredential' command</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d29f3-434">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d29f3-434">Az.DataLakeStore</span></span>
* <span data-ttu-id="d29f3-435">Обновлен отдельный пакет SDK ADLS до версии 1.2.4-alpha.</span><span class="sxs-lookup"><span data-stu-id="d29f3-435">Updated ADLS dataplane SDK to 1.2.4-alpha.</span></span> <span data-ttu-id="d29f3-436">Изменения: https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-124-alpha</span><span class="sxs-lookup"><span data-stu-id="d29f3-436">Changes:https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-124-alpha</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="d29f3-437">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="d29f3-437">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="d29f3-438">Добавлены новые командлеты пакета MSIX и обновлены командлеты приложений.</span><span class="sxs-lookup"><span data-stu-id="d29f3-438">Added new MSIX Package cmdlets and updated Applications cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d29f3-439">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d29f3-439">Az.EventHub</span></span>
* <span data-ttu-id="d29f3-440">Исправлены команды кластера для кластера EventHub без тегов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-440">Fixed Cluster commands for EventHub cluster without tags</span></span>
* <span data-ttu-id="d29f3-441">Обновлен текст справки для PartnerNamespace команд AzEventHubGeoDRConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d29f3-441">Updated help text for PartnerNamespace of AzEventHubGeoDRConfiguration commands</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="d29f3-442">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d29f3-442">Az.HDInsight</span></span>
* <span data-ttu-id="d29f3-443">Добавлены параметры ResourceProviderConnection и PrivateLink в командлет New-AzHDInsightCluster для включения поддержки исходящих подключений ретранслятора и приватного канала.</span><span class="sxs-lookup"><span data-stu-id="d29f3-443">Add parameters 'ResourceProviderConnection' and 'PrivateLink' to cmdlet 'New-AzHDInsightCluster' to support relay outbound and private link feature</span></span>
* <span data-ttu-id="d29f3-444">В командлет New-AzHDInsightCluster добавлен параметр AmbariDatabase для включения поддержки пользовательской базы данных Ambari.</span><span class="sxs-lookup"><span data-stu-id="d29f3-444">Add parameter 'AmbariDatabase' to cmdlet 'New-AzHDInsightCluster' to support custom Ambari database feature</span></span>
* <span data-ttu-id="d29f3-445">В параметр MetastoreType командлета Add-AzHDInsightMetastore добавлено значение AmbariDatabase.</span><span class="sxs-lookup"><span data-stu-id="d29f3-445">Add accept value 'AmbariDatabase' to the parameter 'MetastoreType' of the cmdlet 'Add-AzHDInsightMetastore'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d29f3-446">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d29f3-446">Az.IotHub</span></span>
* <span data-ttu-id="d29f3-447">Разрешены теги в командлете для создания Центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="d29f3-447">Allowed tags in IoT Hub create cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d29f3-448">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d29f3-448">Az.KeyVault</span></span>
* <span data-ttu-id="d29f3-449">Поддерживается обновление тега хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="d29f3-449">Supported updating key vault tag</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d29f3-450">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d29f3-450">Az.LogicApp</span></span>
* <span data-ttu-id="d29f3-451">Исправлена проблема, из-за которой командлет Get-AzLogicAppRunHistory получал только первую страницу результатов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-451">Fixed for Get-AzLogicAppRunHistory only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d29f3-452">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d29f3-452">Az.Network</span></span>
* <span data-ttu-id="d29f3-453">Обновлены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="d29f3-453">Updated below cmdlet</span></span> 
    - <span data-ttu-id="d29f3-454">New-AzLoadBalancerFrontendIpConfigCommand, Set-AzLoadBalancerFrontendIpConfigCommand, Add-AzLoadBalancerFrontendIpConfigCommand:</span><span class="sxs-lookup"><span data-stu-id="d29f3-454">'New-AzLoadBalancerFrontendIpConfigCommand', 'Set-AzLoadBalancerFrontendIpConfigCommand', 'Add-AzLoadBalancerFrontendIpConfigCommand':</span></span>
        - <span data-ttu-id="d29f3-455">добавлено свойство PublicIpAddressPrefix;</span><span class="sxs-lookup"><span data-stu-id="d29f3-455">Added PublicIpAddressPrefix property</span></span>
        - <span data-ttu-id="d29f3-456">добавлено свойство PublicIpAddressPrefixId.</span><span class="sxs-lookup"><span data-stu-id="d29f3-456">Added PublicIpAddressPrefixId property</span></span>
* <span data-ttu-id="d29f3-457">Добавлены новые свойства в следующие командлеты для включения глобальной балансировки нагрузки:</span><span class="sxs-lookup"><span data-stu-id="d29f3-457">Added new properties to the following cmdlets to allow for global load balancing</span></span>
    - <span data-ttu-id="d29f3-458">New-AzLoadBalancer:</span><span class="sxs-lookup"><span data-stu-id="d29f3-458">'New-AzLoadBalancer':</span></span>
        - <span data-ttu-id="d29f3-459">добавлено свойство уровня SKU.</span><span class="sxs-lookup"><span data-stu-id="d29f3-459">Added Sku Tier property</span></span>
    - <span data-ttu-id="d29f3-460">New-AzPuplicIpAddress:</span><span class="sxs-lookup"><span data-stu-id="d29f3-460">'New-AzPuplicIpAddress':</span></span>
        - <span data-ttu-id="d29f3-461">добавлено свойство уровня SKU.</span><span class="sxs-lookup"><span data-stu-id="d29f3-461">Added Sku Tier property</span></span>
    - <span data-ttu-id="d29f3-462">New-AzPublicIpPrefix:</span><span class="sxs-lookup"><span data-stu-id="d29f3-462">'New-AzPublicIpPrefix':</span></span>
        - <span data-ttu-id="d29f3-463">добавлено свойство уровня SKU.</span><span class="sxs-lookup"><span data-stu-id="d29f3-463">Added Sku Tier property</span></span>
    - <span data-ttu-id="d29f3-464">New-AzLoadBalancerBackendAddressConfig:</span><span class="sxs-lookup"><span data-stu-id="d29f3-464">'New-AzLoadBalancerBackendAddressConfig':</span></span>
        - <span data-ttu-id="d29f3-465">добавлено свойство LoadBalancerFrontendIPConfigurationId.</span><span class="sxs-lookup"><span data-stu-id="d29f3-465">Added LoadBalancerFrontendIPConfigurationId property</span></span>
* <span data-ttu-id="d29f3-466">Обновлены планы по включению сообщений о прекращении поддержки для следующих командлетов:   -New-AzVirtualHubRoute   -New-AzVirtualHubRouteTable   -Add-AzVirtualHubRoute   -Add-AzVirtualHubRouteTable   -Get-AzVirtualHubRouteTable   -Remove-AzVirtualHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="d29f3-466">Updated planning to deprecate warnings for the following cmdlets   -'New-AzVirtualHubRoute'   -'New-AzVirtualHubRouteTable'   -'Add-AzVirtualHubRoute'   -'Add-AzVirtualHubRouteTable'   -'Get-AzVirtualHubRouteTable'   -'Remove-AzVirtualHubRouteTable'</span></span>
* <span data-ttu-id="d29f3-467">Обновлены планы по включению сообщений о прекращении поддержки для аргумента RouteTable для следующих командлетов:   -New-AzVirtualHub   -Set-AzVirtualHub   -Update-AzVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="d29f3-467">Added planning to deprecate warnings on the argument 'RouteTable' for the following cmdlets   -'New-AzVirtualHub'   -'Set-AzVirtualHub'   -'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="d29f3-468">Аргументы -MinScaleUnits и -MaxScaleUnits в Set-AzExpressRouteGateway сделаны необязательными.</span><span class="sxs-lookup"><span data-stu-id="d29f3-468">Made arguments '-MinScaleUnits' and '-MaxScaleUnits' optional in 'Set-AzExpressRouteGateway'</span></span>
* <span data-ttu-id="d29f3-469">Добавлены новые командлеты для включения взаимной проверки подлинности и профилей SSL в Шлюзе приложений:</span><span class="sxs-lookup"><span data-stu-id="d29f3-469">Added new cmdlets to support Mutual Authentication and SSL Profiles on Application Gateway</span></span>
    - <span data-ttu-id="d29f3-470">Get-AzApplicationGatewayClientAuthConfiguration;</span><span class="sxs-lookup"><span data-stu-id="d29f3-470">'Get-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="d29f3-471">New-AzApplicationGatewayClientAuthConfiguration;</span><span class="sxs-lookup"><span data-stu-id="d29f3-471">'New-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="d29f3-472">Remove-AzApplicationGatewayClientAuthConfiguration;</span><span class="sxs-lookup"><span data-stu-id="d29f3-472">'Remove-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="d29f3-473">Set-AzApplicationGatewayClientAuthConfiguration;</span><span class="sxs-lookup"><span data-stu-id="d29f3-473">'Set-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="d29f3-474">Add-AzApplicationGatewayTrustedClientCertificate;</span><span class="sxs-lookup"><span data-stu-id="d29f3-474">'Add-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="d29f3-475">Get-AzApplicationGatewayTrustedClientCertificate;</span><span class="sxs-lookup"><span data-stu-id="d29f3-475">'Get-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="d29f3-476">New-AzApplicationGatewayTrustedClientCertificate;</span><span class="sxs-lookup"><span data-stu-id="d29f3-476">'New-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="d29f3-477">Remove-AzApplicationGatewayTrustedClientCertificate;</span><span class="sxs-lookup"><span data-stu-id="d29f3-477">'Remove-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="d29f3-478">Set-AzApplicationGatewayTrustedClientCertificate;</span><span class="sxs-lookup"><span data-stu-id="d29f3-478">'Set-AzApplicationGatewayTrustedClientCertificate'</span></span>
    - <span data-ttu-id="d29f3-479">Add-AzApplicationGatewaySslProfile;</span><span class="sxs-lookup"><span data-stu-id="d29f3-479">'Add-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="d29f3-480">Get-AzApplicationGatewaySslProfile;</span><span class="sxs-lookup"><span data-stu-id="d29f3-480">'Get-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="d29f3-481">New-AzApplicationGatewaySslProfile;</span><span class="sxs-lookup"><span data-stu-id="d29f3-481">'New-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="d29f3-482">Remove-AzApplicationGatewaySslProfile;</span><span class="sxs-lookup"><span data-stu-id="d29f3-482">'Remove-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="d29f3-483">Set-AzApplicationGatewaySslProfile;</span><span class="sxs-lookup"><span data-stu-id="d29f3-483">'Set-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="d29f3-484">Get-AzApplicationGatewaySslProfilePolicy;</span><span class="sxs-lookup"><span data-stu-id="d29f3-484">'Get-AzApplicationGatewaySslProfilePolicy'</span></span>
    - <span data-ttu-id="d29f3-485">Remove-AzApplicationGatewaySslProfilePolicy;</span><span class="sxs-lookup"><span data-stu-id="d29f3-485">'Remove-AzApplicationGatewaySslProfilePolicy'</span></span>
    - <span data-ttu-id="d29f3-486">Set-AzApplicationGatewaySslProfilePolicy.</span><span class="sxs-lookup"><span data-stu-id="d29f3-486">'Set-AzApplicationGatewaySslProfilePolicy'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d29f3-487">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-487">Az.RecoveryServices</span></span>
* <span data-ttu-id="d29f3-488">Указано время в формате UTC для BackupTime политики.</span><span class="sxs-lookup"><span data-stu-id="d29f3-488">Specifying policy BackupTime is in UTC.</span></span>
* <span data-ttu-id="d29f3-489">Изменено предупреждение о критическом изменении в командлете Get-AzRecoveryServicesBackupJobDetails.</span><span class="sxs-lookup"><span data-stu-id="d29f3-489">Modifying breaking change warning in Get-AzRecoveryServicesBackupJobDetails cmdlet.</span></span>
* <span data-ttu-id="d29f3-490">Обновлен примера текста справки для командлета Set-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="d29f3-490">Updating sample script help text for Set-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d29f3-491">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-491">Az.Resources</span></span>
* <span data-ttu-id="d29f3-492">Исправлена проблема, из-за которой при использовании What-If отображаются две области группы ресурсов с разными регистрами.</span><span class="sxs-lookup"><span data-stu-id="d29f3-492">Fixed an issue where What-If shows two resource group scopes with different casing</span></span>
* <span data-ttu-id="d29f3-493">Обновлен командлет Export-AzResourceGroup для использования пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="d29f3-493">Updated 'Export-AzResourceGroup' to use the SDK.</span></span>
* <span data-ttu-id="d29f3-494">Добавлены сведения о языке и региональных параметрах для методов синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="d29f3-494">Added culture info to parse methods</span></span>

#### <a name="azsql"></a><span data-ttu-id="d29f3-495">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-495">Az.Sql</span></span>
* <span data-ttu-id="d29f3-496">Исправлены проблемы, из-за которых командлет Set-AzSqlDatabaseAudit не поддерживал базу данных уровня "Гипермасштабирование" и не удавалось определить выпуск базы данных.</span><span class="sxs-lookup"><span data-stu-id="d29f3-496">Fixed issues where Set-AzSqlDatabaseAudit were not support Hyperscale database and database edition cannot be determined</span></span>
* <span data-ttu-id="d29f3-497">В New-AzSqlInstance и Set-AzSqlInstance добавлен параметр MaintenanceConfigurationId.</span><span class="sxs-lookup"><span data-stu-id="d29f3-497">Added MaintenanceConfigurationId to 'New-AzSqlInstance' and 'Set-AzSqlInstance'</span></span>
* <span data-ttu-id="d29f3-498">Исправлена ошибка в GetAzureSqlDatabaseReplicationLink.cs, где параметр PartnerServerName проверялся по значению, а не по ключу.</span><span class="sxs-lookup"><span data-stu-id="d29f3-498">Fixed a bug in GetAzureSqlDatabaseReplicationLink.cs where PartnerServerName parameter was being checked for by value instead of key</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d29f3-499">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d29f3-499">Az.Websites</span></span>
* <span data-ttu-id="d29f3-500">Включена поддержка новых возможностей ограничения доступа: ServiceTag, multi-ip и http-headers.</span><span class="sxs-lookup"><span data-stu-id="d29f3-500">Added support for new access restriction features: ServiceTag, multi-ip and http-headers</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="d29f3-501">Благодарим наших участников сообщества</span><span class="sxs-lookup"><span data-stu-id="d29f3-501">Thanks to our community contributors</span></span>
* <span data-ttu-id="d29f3-502">Джон К. Мартин (John Q. Martin) (@johnmart82), добавление сведений о предварительных требованиях для брандмауэра (№13385).</span><span class="sxs-lookup"><span data-stu-id="d29f3-502">John Q. Martin (@johnmart82), Adding firewall prerequisite information (#13385)</span></span>
* <span data-ttu-id="d29f3-503">Маникандан Дураисами (Manikandan Duraisamy) (@madurais-msft), исправление аргумента PublicSubnetName (№13417).</span><span class="sxs-lookup"><span data-stu-id="d29f3-503">Manikandan Duraisamy (@madurais-msft), Corrected the PublicSubnetName argument (#13417)</span></span>
* <span data-ttu-id="d29f3-504">@mahortas, обновление значений параметров для параметра -HostName (№13349).</span><span class="sxs-lookup"><span data-stu-id="d29f3-504">@mahortas, Update for -HostNames parameter values (#13349)</span></span>
* <span data-ttu-id="d29f3-505">@MariachiForHire, добавлены поддерживаемые значения TrafficAnalyticsInterval (№13304).</span><span class="sxs-lookup"><span data-stu-id="d29f3-505">@MariachiForHire, added supported TrafficAnalyticsInterval values (#13304)</span></span>
* <span data-ttu-id="d29f3-506">Майкл Джеймс (Michael James) (@mikejwhat), включена поддержка Get-AzLogicAppRunHistory для получения более 30 записей (№13393).</span><span class="sxs-lookup"><span data-stu-id="d29f3-506">Michael James (@mikejwhat), Allow Get-AzLogicAppRunHistory to return more than 30 entries (#13393)</span></span>
* <span data-ttu-id="d29f3-507">Шашикант Шакья (Shashikant Shakya) (@shshakya), обновление файла Restore-AzSqlInstanceDatabase.md (№13404).</span><span class="sxs-lookup"><span data-stu-id="d29f3-507">Shashikant Shakya (@shshakya), Update Restore-AzSqlInstanceDatabase.md (#13404)</span></span>

## <a name="500---october-2020"></a><span data-ttu-id="d29f3-508">5.0.0 — октябрь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-508">5.0.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d29f3-509">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d29f3-509">Az.Accounts</span></span>
* <span data-ttu-id="d29f3-510">[Критическое изменение] Удалены командлеты Get-AzProfile и Select-AzProfile.</span><span class="sxs-lookup"><span data-stu-id="d29f3-510">[Breaking Change] Removed 'Get-AzProfile' and 'Select-AzProfile'</span></span>
* <span data-ttu-id="d29f3-511">Библиотека проверки подлинности Azure Active Directory заменена библиотекой проверки подлинности Microsoft (MSAL).</span><span class="sxs-lookup"><span data-stu-id="d29f3-511">Replaced Azure Directory Authentication Library with Microsoft Authentication Library(MSAL)</span></span>

#### <a name="azaks"></a><span data-ttu-id="d29f3-512">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="d29f3-512">Az.Aks</span></span>
* <span data-ttu-id="d29f3-513">[Критическое изменение] Удален псевдоним параметра ClientIdAndSecret в командлетах New-AzAksCluster и Set-AzAksCluster.</span><span class="sxs-lookup"><span data-stu-id="d29f3-513">[Breaking Change] Removed parameter alias 'ClientIdAndSecret' in 'New-AzAksCluster' and 'Set-AzAksCluster'.</span></span>
* <span data-ttu-id="d29f3-514">[Критическое изменение] Изменено значение по умолчанию NodeVmSetType в New-AzAksCluster с AvailabilitySet на VirtualMachineScaleSets.</span><span class="sxs-lookup"><span data-stu-id="d29f3-514">[Breaking Change] Changed the default value of 'NodeVmSetType' in 'New-AzAksCluster' from 'AvailabilitySet' to 'VirtualMachineScaleSets'.</span></span>
* <span data-ttu-id="d29f3-515">[Критическое изменение] Изменено значение по умолчанию NetworkPlugin в New-AzAksCluster с None на azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-515">[Breaking Change] Changed the default value of 'NetworkPlugin' in 'New-AzAksCluster' from 'None' to 'azure'.</span></span>
* <span data-ttu-id="d29f3-516">[Критическое изменение] Удален параметр NodeOsType в New-AzAksCluster, так как поддерживается только одно значение Linux.</span><span class="sxs-lookup"><span data-stu-id="d29f3-516">[Breaking Change] Removed parameter 'NodeOsType' in 'New-AzAksCluster' as it supports only one value Linux.</span></span>

#### <a name="azbilling"></a><span data-ttu-id="d29f3-517">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="d29f3-517">Az.Billing</span></span>
* <span data-ttu-id="d29f3-518">Добавлен командлет Get-AzBillingAccount.</span><span class="sxs-lookup"><span data-stu-id="d29f3-518">Added 'Get-AzBillingAccount' cmdlet</span></span>
* <span data-ttu-id="d29f3-519">Добавлен командлет Get-AzBillingProfile.</span><span class="sxs-lookup"><span data-stu-id="d29f3-519">Added 'Get-AzBillingProfile' cmdlet</span></span>
* <span data-ttu-id="d29f3-520">Добавлен командлет Get-AzInvoiceSection.</span><span class="sxs-lookup"><span data-stu-id="d29f3-520">Added 'Get-AzInvoiceSection' cmdlet</span></span>
* <span data-ttu-id="d29f3-521">Добавлены новые параметры в командлет Get-AzBillingInvoice.</span><span class="sxs-lookup"><span data-stu-id="d29f3-521">Added new parameters in 'Get-AzBillingInvoice' cmdlet</span></span>
* <span data-ttu-id="d29f3-522">Удалены свойства DownloadUrlExpiry, Type и BillingPeriodNames из ответа командлета Get-AzBillingInvoice.</span><span class="sxs-lookup"><span data-stu-id="d29f3-522">Removed properties DownloadUrlExpiry, Type, BillingPeriodNames from the response of Get-AzBillingInvoice cmdlet</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d29f3-523">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d29f3-523">Az.Cdn</span></span>
* <span data-ttu-id="d29f3-524">Добавлены командлеты для включения функций с поддержкой нескольких источников и приватных каналов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-524">Added cmdlets to support multi-origin and private link functionality</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="d29f3-525">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-525">Az.CognitiveServices</span></span>
* <span data-ttu-id="d29f3-526">Обновлен пакет SDK до версии 7.4.0-preview.</span><span class="sxs-lookup"><span data-stu-id="d29f3-526">Updated SDK to 7.4.0-preview.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d29f3-527">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-527">Az.Compute</span></span>
* <span data-ttu-id="d29f3-528">Добавлен параметр -VmssId в командлет New-AzVm.</span><span class="sxs-lookup"><span data-stu-id="d29f3-528">Added '-VmssId' parameter to 'New-AzVm'</span></span>
* <span data-ttu-id="d29f3-529">Добавлен параметр PlatformFaultDomainCount в командлет New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="d29f3-529">Added 'PlatformFaultDomainCount' parameter to the 'New-AzVmss' cmdlet.</span></span>
* <span data-ttu-id="d29f3-530">Добавлен новый командлет Get-AzDiskEncryptionSetAssociatedResource.</span><span class="sxs-lookup"><span data-stu-id="d29f3-530">New cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span></span>
* <span data-ttu-id="d29f3-531">Добавлены необязательные параметры Tier и LogicalSectorSize в командлет New-AzDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="d29f3-531">Added 'Tier' and 'LogicalSectorSize' optional parameters to the New-AzDiskConfig cmdlet.</span></span> 
* <span data-ttu-id="d29f3-532">Добавлены необязательные параметры Tier, MaxSharesCount, DiskIOPSReadOnly и DiskMBpsReadOnly в командлет New-AzDiskUpdateConfig.</span><span class="sxs-lookup"><span data-stu-id="d29f3-532">Added 'Tier', 'MaxSharesCount', 'DiskIOPSReadOnly', and 'DiskMBpsReadOnly' optional parameters to the 'New-AzDiskUpdateConfig' cmdlet.</span></span> 

#### <a name="azcontainerregistry"></a><span data-ttu-id="d29f3-533">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d29f3-533">Az.ContainerRegistry</span></span>
* <span data-ttu-id="d29f3-534">[Критическое изменение] Обновлена версия API до 2019-05-01.</span><span class="sxs-lookup"><span data-stu-id="d29f3-534">[Breaking Change] Updates API version to 2019-05-01</span></span>
* <span data-ttu-id="d29f3-535">[Критическое изменение] Удалены номер SKU "Классический" и параметр StorageAccountName из командлета New-AzContainerRegistry.</span><span class="sxs-lookup"><span data-stu-id="d29f3-535">[Breaking Change] Removed SKU 'Classic' and parameter 'StorageAccountName' from 'New-AzContainerRegistry'</span></span>
* <span data-ttu-id="d29f3-536">Добавлены новые командлеты: Connect-AzContainerRegistry, Import-AzContainerRegistry, Get-AzContainerRegistryUsage, New-AzContainerRegistryNetworkRule, Set-AzContainerRegistryNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="d29f3-536">Added New cmdlets: 'Connect-AzContainerRegistry', 'Import-AzContainerRegistry', 'Get-AzContainerRegistryUsage', 'New-AzContainerRegistryNetworkRule', 'Set-AzContainerRegistryNetworkRule'</span></span>
* <span data-ttu-id="d29f3-537">Добавлен новый параметр NetworkRuleSet в командлет Update-AzContainerRegistry.</span><span class="sxs-lookup"><span data-stu-id="d29f3-537">Added new parameter 'NetworkRuleSet' to 'Update-AzContainerRegistry'</span></span>

#### <a name="azdatabricks"></a><span data-ttu-id="d29f3-538">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="d29f3-538">Az.Databricks</span></span>
* <span data-ttu-id="d29f3-539">Исправлена ошибка, которая может вызвать сбой при обновлении рабочей области Databricks без `-EncryptionKeyVersion`.</span><span class="sxs-lookup"><span data-stu-id="d29f3-539">Fixed a bug that may cause updating databricks workspace without `-EncryptionKeyVersion` to fail.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d29f3-540">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d29f3-540">Az.DataFactory</span></span>
* <span data-ttu-id="d29f3-541">Пакет SDK ADF для .NET обновлен до версии 4.12.0.</span><span class="sxs-lookup"><span data-stu-id="d29f3-541">Updated ADF .Net SDK version to 4.12.0</span></span>
* <span data-ttu-id="d29f3-542">Пакет SDK клиента шифрования ADF обновлен до версии 4.14.7587.7.</span><span class="sxs-lookup"><span data-stu-id="d29f3-542">Updated ADF encryption client SDK version to 4.14.7587.7</span></span>
* <span data-ttu-id="d29f3-543">Добавлены команды Stop-AzDataFactoryV2TriggerRun и Invoke-AzDataFactoryV2TriggerRun.</span><span class="sxs-lookup"><span data-stu-id="d29f3-543">Added 'Stop-AzDataFactoryV2TriggerRun' and 'Invoke-AzDataFactoryV2TriggerRun' commands</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="d29f3-544">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="d29f3-544">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="d29f3-545">Требуется свойство Location для создания объектов ARM верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="d29f3-545">Require Location property for creating top level arm objects.</span></span>
        <span data-ttu-id="d29f3-546">\*`ApplicationGroupType` требуется для `New-AzWvdApplicationGroup`.</span><span class="sxs-lookup"><span data-stu-id="d29f3-546">\* Made `ApplicationGroupType` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="d29f3-547">\*`HostPoolArmPath` требуется для `New-AzWvdApplicationGroup`.</span><span class="sxs-lookup"><span data-stu-id="d29f3-547">\* Made `HostPoolArmPath` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="d29f3-548">\*Добавлен параметр `PreferredAppGroupType` для `New-AzWvdHostPool`.</span><span class="sxs-lookup"><span data-stu-id="d29f3-548">\* Added `PreferredAppGroupType` for `New-AzWvdHostPool`.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="d29f3-549">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="d29f3-549">Az.Functions</span></span>
* <span data-ttu-id="d29f3-550">[Критическое изменение] Удален параметр-переключатель IncludeSlot из всех наборов параметров Get-AzFunctionApp, кроме одного.</span><span class="sxs-lookup"><span data-stu-id="d29f3-550">[Breaking Change] Removed 'IncludeSlot' switch parameter from all but one parameter set of 'Get-AzFunctionApp'.</span></span> <span data-ttu-id="d29f3-551">Командлет теперь поддерживает получение слотов развертывания в результатах, если указать IncludeSlot.</span><span class="sxs-lookup"><span data-stu-id="d29f3-551">The cmdlet now supports retrieving deployment slots in the results when '-IncludeSlot' is specified.</span></span> 
* <span data-ttu-id="d29f3-552">Обновлен командлет New-AzFunctionApp:</span><span class="sxs-lookup"><span data-stu-id="d29f3-552">Updated 'New-AzFunctionApp':</span></span>
  - <span data-ttu-id="d29f3-553">исправлена проблема с -DisableApplicationInsights, чтобы при указании этого параметра не создавался проект Application Insights.</span><span class="sxs-lookup"><span data-stu-id="d29f3-553">Fixed -DisableApplicationInsights so that no application insights project is created when this option is specified.</span></span> <span data-ttu-id="d29f3-554">[№12728]</span><span class="sxs-lookup"><span data-stu-id="d29f3-554">[#12728]</span></span>
  - <span data-ttu-id="d29f3-555">[Критическое изменение] Отключена поддержка создания приложений-функций PowerShell 6.2.</span><span class="sxs-lookup"><span data-stu-id="d29f3-555">[Breaking Change] Removed support to create PowerShell 6.2 function apps.</span></span>
  - <span data-ttu-id="d29f3-556">[Критическое изменение] Изменена версия среды выполнения по умолчанию (с версии 6.2 на 7.0) в Функциях версии 3 в Windows для приложений-функций PowerShell, если не указать параметр RuntimeVersion.</span><span class="sxs-lookup"><span data-stu-id="d29f3-556">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="d29f3-557">[Критическое изменение] Изменена версия среды выполнения по умолчанию (с версии 10 на 12) в Функциях версии 3 в Windows и Linux для приложений-функций Node, если не указать параметр RuntimeVersion.</span><span class="sxs-lookup"><span data-stu-id="d29f3-557">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="d29f3-558">[Критическое изменение] Изменена версия среды выполнения по умолчанию (с версии 3.7 на 3.8) в Функциях версии 3 в Linux для приложений-функций Python, если не указать параметр RuntimeVersion.</span><span class="sxs-lookup"><span data-stu-id="d29f3-558">[Breaking Change] Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the RuntimeVersion parameter is not specified.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d29f3-559">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d29f3-559">Az.HDInsight</span></span>
 * <span data-ttu-id="d29f3-560">Для командлета New-AzHDInsightCluster:</span><span class="sxs-lookup"><span data-stu-id="d29f3-560">For New-AzHDInsightCluster cmdlet:</span></span>
     - <span data-ttu-id="d29f3-561">заменен параметр DefaultStorageAccountName на StorageAccountResourceId;</span><span class="sxs-lookup"><span data-stu-id="d29f3-561">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="d29f3-562">заменен параметр DefaultStorageAccountKey на StorageAccountKey;</span><span class="sxs-lookup"><span data-stu-id="d29f3-562">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="d29f3-563">заменен параметр DefaultStorageAccountType на StorageAccountType;</span><span class="sxs-lookup"><span data-stu-id="d29f3-563">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="d29f3-564">удален параметр PublicNetworkAccessType;</span><span class="sxs-lookup"><span data-stu-id="d29f3-564">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="d29f3-565">удален параметр OutboundPublicNetworkAccessType.</span><span class="sxs-lookup"><span data-stu-id="d29f3-565">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
     - <span data-ttu-id="d29f3-566">Добавлены новые параметры: StorageFileSystem и StorageAccountManagedIdentity для включения поддержки ADLS 2-го поколения.</span><span class="sxs-lookup"><span data-stu-id="d29f3-566">Added new parameters: 'StorageFileSystem' and 'StorageAccountManagedIdentity' to support ADLSGen2</span></span>
     - <span data-ttu-id="d29f3-567">Добавлен новый параметр EnableIDBroker для включения поддержки брокера удостоверений HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d29f3-567">Added new parameter 'EnableIDBroker' to Support HDInsight ID Broker</span></span>
     - <span data-ttu-id="d29f3-568">Добавлены новые параметры: KafkaClientGroupId, KafkaClientGroupName и KafkaManagementNodeSize для включения поддержки прокси-сервера REST для Kafka.</span><span class="sxs-lookup"><span data-stu-id="d29f3-568">Added new parameters: 'KafkaClientGroupId', 'KafkaClientGroupName' and 'KafkaManagementNodeSize' to support Kafka Rest Proxy</span></span>
 * <span data-ttu-id="d29f3-569">Для командлета New-AzHDInsightClusterConfig:</span><span class="sxs-lookup"><span data-stu-id="d29f3-569">For New-AzHDInsightClusterConfig cmdlet:</span></span>
     - <span data-ttu-id="d29f3-570">заменен параметр DefaultStorageAccountName на StorageAccountResourceId;</span><span class="sxs-lookup"><span data-stu-id="d29f3-570">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="d29f3-571">заменен параметр DefaultStorageAccountKey на StorageAccountKey;</span><span class="sxs-lookup"><span data-stu-id="d29f3-571">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="d29f3-572">заменен параметр DefaultStorageAccountType на StorageAccountType;</span><span class="sxs-lookup"><span data-stu-id="d29f3-572">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="d29f3-573">удален параметр PublicNetworkAccessType;</span><span class="sxs-lookup"><span data-stu-id="d29f3-573">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="d29f3-574">удален параметр OutboundPublicNetworkAccessType.</span><span class="sxs-lookup"><span data-stu-id="d29f3-574">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="d29f3-575">Для командлета Set-AzHDInsightDefaultStorage:</span><span class="sxs-lookup"><span data-stu-id="d29f3-575">For Set-AzHDInsightDefaultStorage cmdlet:</span></span>
    - <span data-ttu-id="d29f3-576">заменен параметр StorageAccountName на StorageAccountResourceId.</span><span class="sxs-lookup"><span data-stu-id="d29f3-576">Replaced parameter 'StorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="d29f3-577">Для командлета Add-AzHDInsightSecurityProfile:</span><span class="sxs-lookup"><span data-stu-id="d29f3-577">For Add-AzHDInsightSecurityProfile cmdlet:</span></span>
    - <span data-ttu-id="d29f3-578">заменен параметр Domain на DomainResourceId;</span><span class="sxs-lookup"><span data-stu-id="d29f3-578">Replaced parameter 'Domain' with 'DomainResourceId'</span></span>
    - <span data-ttu-id="d29f3-579">удалено обязательное требование использовать параметр OrganizationalUnitDN.</span><span class="sxs-lookup"><span data-stu-id="d29f3-579">Removed the mandatory requirement for parameter 'OrganizationalUnitDN'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d29f3-580">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d29f3-580">Az.KeyVault</span></span>
* <span data-ttu-id="d29f3-581">[Критическое изменение] Не рекомендуется использовать параметр DisableSoftDelete в командлете New-AzKeyVault и параметр EnableSoftDelete в командлете Update-AzKeyVault.</span><span class="sxs-lookup"><span data-stu-id="d29f3-581">[Breaking Change] Deprecated parameter DisableSoftDelete in 'New-AzKeyVault' and EnableSoftDelete in 'Update-AzKeyVault'</span></span>
* <span data-ttu-id="d29f3-582">[Критическое изменение] Удален атрибут SecretValueText, чтобы значение SecretValue не отображалось напрямую [№12266].</span><span class="sxs-lookup"><span data-stu-id="d29f3-582">[Breaking Change] Removed attribute SecretValueText to avoid displaying SecretValue directly [#12266]</span></span>
* <span data-ttu-id="d29f3-583">Включена поддержка нового типа ресурса: управляемое устройство HSM.</span><span class="sxs-lookup"><span data-stu-id="d29f3-583">Supported new resource type: managed HSM</span></span>
    - <span data-ttu-id="d29f3-584">CRUD управляемого устройства HSM и командлеты для работы с ключами на управляемом устройстве HSM.</span><span class="sxs-lookup"><span data-stu-id="d29f3-584">CRUD of managed HSM and cmdlets to operate keys on managed HSM</span></span>
    - <span data-ttu-id="d29f3-585">Полное резервное копирование и восстановление HSM, создание ключа AES, резервное копирование и восстановление домена безопасности, RBAC.</span><span class="sxs-lookup"><span data-stu-id="d29f3-585">Full HSM backup/restore, AES key creation, security domain backup/restore, RBAC</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="d29f3-586">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-586">Az.ManagedServices</span></span>
* <span data-ttu-id="d29f3-587">[Критическое изменение] Обновлены соглашения об именовании параметров и связанные примеры.</span><span class="sxs-lookup"><span data-stu-id="d29f3-587">[Breaking Change] Updated parameters naming conventions and associated examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d29f3-588">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d29f3-588">Az.Network</span></span>
* <span data-ttu-id="d29f3-589">[Критическое изменение] Удален параметр HostedSubnet и вместо него добавлен параметр Subnet.</span><span class="sxs-lookup"><span data-stu-id="d29f3-589">[Breaking Change] Removed parameter 'HostedSubnet' and added 'Subnet' instead</span></span>
* <span data-ttu-id="d29f3-590">Добавлены новые командлеты для маршрутов пиринга виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="d29f3-590">Added new cmdlets for Virtual Router Peer Routes</span></span>
    - <span data-ttu-id="d29f3-591">Get-AzVirtualRouterPeerLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="d29f3-591">'Get-AzVirtualRouterPeerLearnedRoute'</span></span>
    - <span data-ttu-id="d29f3-592">Get-AzVirtualRouterPeerAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="d29f3-592">'Get-AzVirtualRouterPeerAdvertisedRoute'</span></span>
* <span data-ttu-id="d29f3-593">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="d29f3-593">Updated New-AzFirewall cmdlet:</span></span>
    - <span data-ttu-id="d29f3-594">добавлен параметр -SkuTier;</span><span class="sxs-lookup"><span data-stu-id="d29f3-594">Added parameter '-SkuTier'</span></span>
    - <span data-ttu-id="d29f3-595">добавлен параметр -SkuName и номер SKU в качестве псевдонима;</span><span class="sxs-lookup"><span data-stu-id="d29f3-595">Added parameter '-SkuName' and made Sku as Alias for this</span></span>
    - <span data-ttu-id="d29f3-596">удален параметр -Sku.</span><span class="sxs-lookup"><span data-stu-id="d29f3-596">Removed parameter '-Sku'</span></span>
* <span data-ttu-id="d29f3-597">[Критическое изменение] Сделан обязательным аргумент Connectionlink в командлетах Start-AzVpnConnectionPacketCapture и Stop-AzVpnConnectionPacketCapture.</span><span class="sxs-lookup"><span data-stu-id="d29f3-597">[Breaking Change] Made 'Connectionlink' argument mandatory in 'Start-AzVpnConnectionPacketCapture' and 'Stop-AzVpnConnectionPacketCapture'</span></span>
* <span data-ttu-id="d29f3-598">[Критическое изменение] В командлете New-AzNetworkWatcherConnectionMonitorEndPointObject удален параметр -Filter.</span><span class="sxs-lookup"><span data-stu-id="d29f3-598">[Breaking Change] Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' to remove parameter '-Filter'</span></span>
* <span data-ttu-id="d29f3-599">[Критическое изменение] Заменен командлет New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject на New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.</span><span class="sxs-lookup"><span data-stu-id="d29f3-599">[Breaking Change] Replaced 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' cmdlet with 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'</span></span>
* <span data-ttu-id="d29f3-600">Обновлен командлет New-AzNetworkWatcherConnectionMonitorEndPointObject:</span><span class="sxs-lookup"><span data-stu-id="d29f3-600">Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' cmdlet:</span></span>
    - <span data-ttu-id="d29f3-601">добавлен параметр -Type;</span><span class="sxs-lookup"><span data-stu-id="d29f3-601">Added parameter '-Type'</span></span>
    - <span data-ttu-id="d29f3-602">добавлен параметр -CoverageLevel;</span><span class="sxs-lookup"><span data-stu-id="d29f3-602">Added parameter '-CoverageLevel'</span></span>
    - <span data-ttu-id="d29f3-603">добавлен параметр -Scope.</span><span class="sxs-lookup"><span data-stu-id="d29f3-603">Added parameter '-Scope'</span></span>
* <span data-ttu-id="d29f3-604">В командлет New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject добавлен новый параметр -DestinationPortBehavior.</span><span class="sxs-lookup"><span data-stu-id="d29f3-604">Updated 'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' cmdlet with new parameter '-DestinationPortBehavior'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d29f3-605">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-605">Az.RecoveryServices</span></span>
* <span data-ttu-id="d29f3-606">Исправлена проблема с восстановлением рабочей нагрузки для разрешений участника.</span><span class="sxs-lookup"><span data-stu-id="d29f3-606">Fixing Workload Restore for contributor permissions.</span></span>
* <span data-ttu-id="d29f3-607">Добавлены новые наборы параметров и проверки для командлета Restore-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="d29f3-607">Added new parameter sets and validations for Restore-AzRecoveryServicesBackupItem cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d29f3-608">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-608">Az.Resources</span></span>
* <span data-ttu-id="d29f3-609">Исправлена ошибка синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="d29f3-609">Fixed parsing bug</span></span>
* <span data-ttu-id="d29f3-610">Обновлены командлеты What-If шаблона ARM для удаления сообщения о предварительной версии из результатов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-610">Updated ARM template What-If cmdlets to remove preview message from results</span></span>
* <span data-ttu-id="d29f3-611">Исправлена ошибка, из-за которой командлеты развертывания шаблонов завершаются сбоем, если для параметра -WhatIf задана более высокая область [№13038].</span><span class="sxs-lookup"><span data-stu-id="d29f3-611">Fixed an issue where template deployment cmdlets crash if '-WhatIf' is set at a higher scope [#13038]</span></span>
* <span data-ttu-id="d29f3-612">Исправлена ошибка, из-за которой командлеты развертывания шаблона не сохраняют регистр для параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="d29f3-612">Fixed an issue where template deployment cmdlets does not preserve case for template parameters</span></span>
* <span data-ttu-id="d29f3-613">Добавлена версия API по умолчанию для использования в командлете Export-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d29f3-613">Added a default API version to be used in 'Export-AzResourceGroup' cmdlet</span></span>
* <span data-ttu-id="d29f3-614">Добавлены командлеты для Спецификаций шаблонов (Get-AzTemplateSpec, Set-AzTemplateSpec, New-AzTemplateSpec, Remove-AzTemplateSpec, Export-AzTemplateSpec).</span><span class="sxs-lookup"><span data-stu-id="d29f3-614">Added cmdlets for Template Specs ('Get-AzTemplateSpec', 'Set-AzTemplateSpec', 'New-AzTemplateSpec', 'Remove-AzTemplateSpec', 'Export-AzTemplateSpec')</span></span>
* <span data-ttu-id="d29f3-615">Включена поддержка развертывания Спецификаций шаблонов с помощью существующих командлетов развертывания (с использованием нового параметра -TemplateSpecId).</span><span class="sxs-lookup"><span data-stu-id="d29f3-615">Added support for deploying Template Specs using existing deployment cmdlets (via the new -TemplateSpecId parameter)</span></span> 
* <span data-ttu-id="d29f3-616">Включена возможность использовать SDK в командлете Get-AzResourceGroupDeploymentOperation.</span><span class="sxs-lookup"><span data-stu-id="d29f3-616">Updated 'Get-AzResourceGroupDeploymentOperation' to use the SDK.</span></span>
* <span data-ttu-id="d29f3-617">Удален параметр -ApiVersion из командлетов \*-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="d29f3-617">Removed '-ApiVersion' parameter from '\*-AzDeployment' cmdlets.</span></span>

#### <a name="azsql"></a><span data-ttu-id="d29f3-618">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-618">Az.Sql</span></span>
* <span data-ttu-id="d29f3-619">Исправлена ошибка, из-за которой выполнение командлета New-AzSqlDatabaseExport завершается сбоем, если не указать networkIsolation [№13097].</span><span class="sxs-lookup"><span data-stu-id="d29f3-619">Fixed issue where New-AzSqlDatabaseExport fails if networkIsolation not specified [#13097]</span></span>
* <span data-ttu-id="d29f3-620">Исправлена ошибка, из-за которой командлеты New-AzSqlDatabaseExport и New-AzSqlDatabaseImport не возвращали OperationStatusLink в результирующем объекте [№13097].</span><span class="sxs-lookup"><span data-stu-id="d29f3-620">Fixed issue where New-AzSqlDatabaseExport and New-AzSqlDatabaseImport were not returning OperationStatusLink in the result object [#13097]</span></span>
* <span data-ttu-id="d29f3-621">Обновлены URL-адреса парных регионов Azure в предупреждениях об избыточности хранилища резервных копий.</span><span class="sxs-lookup"><span data-stu-id="d29f3-621">Update Azure Paired Regions URL in Backup Storage Redundancy Warnings</span></span> 

#### <a name="azstorage"></a><span data-ttu-id="d29f3-622">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d29f3-622">Az.Storage</span></span>
* <span data-ttu-id="d29f3-623">Удалено устаревшее свойство RestorePolicy.LastEnabledTime.</span><span class="sxs-lookup"><span data-stu-id="d29f3-623">Removed obsolete property RestorePolicy.LastEnabledTime</span></span>
    - <span data-ttu-id="d29f3-624">Enable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="d29f3-624">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="d29f3-625">Disable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="d29f3-625">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="d29f3-626">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d29f3-626">'Get-AzStorageBlobServiceProperty'</span></span>
    - <span data-ttu-id="d29f3-627">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d29f3-627">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="d29f3-628">Изменен тип DaysAfterModificationGreaterThan с целочисленного на целочисленный?</span><span class="sxs-lookup"><span data-stu-id="d29f3-628">Change Type of DaysAfterModificationGreaterThan from int to int?</span></span>
    - <span data-ttu-id="d29f3-629">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d29f3-629">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="d29f3-630">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d29f3-630">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="d29f3-631">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="d29f3-631">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="d29f3-632">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="d29f3-632">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="d29f3-633">Поддерживается создание или обновление общей папки с уровнем доступа.</span><span class="sxs-lookup"><span data-stu-id="d29f3-633">Supported create/update file share with access tier</span></span>
    - <span data-ttu-id="d29f3-634">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="d29f3-634">'New-AzRmStorageShare'</span></span>
    - <span data-ttu-id="d29f3-635">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="d29f3-635">'Update-AzRmStorageShare'</span></span>
* <span data-ttu-id="d29f3-636">Поддерживается установка, обновление и удаление ACL рекурсивно для элемента Datalake 2-го поколения.</span><span class="sxs-lookup"><span data-stu-id="d29f3-636">Supported set/update/remove Acl recursively on Datalake Gen2 item</span></span> 
    -  <span data-ttu-id="d29f3-637">Set-AzDataLakeGen2AclRecursive</span><span class="sxs-lookup"><span data-stu-id="d29f3-637">'Set-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="d29f3-638">Update-AzDataLakeGen2AclRecursive</span><span class="sxs-lookup"><span data-stu-id="d29f3-638">'Update-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="d29f3-639">Remove-AzDataLakeGen2AclRecursive</span><span class="sxs-lookup"><span data-stu-id="d29f3-639">'Remove-AzDataLakeGen2AclRecursive'</span></span>
* <span data-ttu-id="d29f3-640">Включена поддержка политики доступа контейнеров с новым разрешением x,t.</span><span class="sxs-lookup"><span data-stu-id="d29f3-640">Supported Container access policy with new permission x,t</span></span>
    -  <span data-ttu-id="d29f3-641">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d29f3-641">'New-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="d29f3-642">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d29f3-642">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="d29f3-643">Изменены выходные данные командлета политики доступа контейнера get/set путем изменения типа разрешения дочернего свойства с enum на string.</span><span class="sxs-lookup"><span data-stu-id="d29f3-643">Changed the output of get/set Container access policy cmdlet, by change the child property Permission type from enum to String</span></span>
    -  <span data-ttu-id="d29f3-644">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d29f3-644">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="d29f3-645">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d29f3-645">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="d29f3-646">Исправлена проблема с примером скрипта для политики управления наборами с помощью JSON.</span><span class="sxs-lookup"><span data-stu-id="d29f3-646">Fixed a sample script issue of set management policy with json</span></span>
    -  <span data-ttu-id="d29f3-647">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d29f3-647">'Set-AzStorageAccountManagementPolicy'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d29f3-648">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d29f3-648">Az.Websites</span></span>
* <span data-ttu-id="d29f3-649">Включена поддержка ценовой категории "Премиум" версии 3.</span><span class="sxs-lookup"><span data-stu-id="d29f3-649">Added support for Premium V3 pricing tier</span></span>
* <span data-ttu-id="d29f3-650">Пакет SDK для веб-сайтов обновлен до версии 3.1.0.</span><span class="sxs-lookup"><span data-stu-id="d29f3-650">Updated the WebSites SDK to 3.1.0</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="d29f3-651">Благодарим наших участников сообщества</span><span class="sxs-lookup"><span data-stu-id="d29f3-651">Thanks to our community contributors</span></span>
* <span data-ttu-id="d29f3-652">@atul-ram, обновление Get-AzDelegation.md (№13176).</span><span class="sxs-lookup"><span data-stu-id="d29f3-652">@atul-ram, Update Get-AzDelegation.md (#13176)</span></span>
* <span data-ttu-id="d29f3-653">@dineshreddy007, правильное назначение ролей приложения в случае регистрации Stack HCI с использованием токена WAC.</span><span class="sxs-lookup"><span data-stu-id="d29f3-653">@dineshreddy007, Get the App Roles assigned correctly in case of Stack HCI registration using WAC token.</span></span> <span data-ttu-id="d29f3-654">(№13249).</span><span class="sxs-lookup"><span data-stu-id="d29f3-654">(#13249)</span></span>
* <span data-ttu-id="d29f3-655">@kongou-ae, обновление New-AzOffice365PolicyProperty.md (№13217).</span><span class="sxs-lookup"><span data-stu-id="d29f3-655">@kongou-ae, Update New-AzOffice365PolicyProperty.md (#13217)</span></span>
* <span data-ttu-id="d29f3-656">Lohith Chowdary Chilukuri (@Lochiluk), обновление Set-AzApplicationGateway.md (№13150).</span><span class="sxs-lookup"><span data-stu-id="d29f3-656">Lohith Chowdary Chilukuri (@Lochiluk), Update Set-AzApplicationGateway.md (#13150)</span></span>
* <span data-ttu-id="d29f3-657">Matthew Burleigh (@mburleigh):</span><span class="sxs-lookup"><span data-stu-id="d29f3-657">Matthew Burleigh (@mburleigh)</span></span>
  * <span data-ttu-id="d29f3-658">добавление ссылок на командлеты PowerShell, указанные в документации (№13203);</span><span class="sxs-lookup"><span data-stu-id="d29f3-658">Add links to PowerShell cmdlets referenced in the document (#13203)</span></span>
  * <span data-ttu-id="d29f3-659">добавление ссылок на командлеты PowerShell, указанные в документации (№13190);</span><span class="sxs-lookup"><span data-stu-id="d29f3-659">Add links to PowerShell cmdlets referenced in the document (#13190)</span></span>
  * <span data-ttu-id="d29f3-660">добавление ссылок на командлеты PowerShell, указанные в документации (№13189);</span><span class="sxs-lookup"><span data-stu-id="d29f3-660">Add links to PowerShell cmdlets referenced in the document (#13189)</span></span>
  * <span data-ttu-id="d29f3-661">добавление ссылок на указанные командлеты (№13137);</span><span class="sxs-lookup"><span data-stu-id="d29f3-661">add links to referenced cmdlets (#13137)</span></span>
  * <span data-ttu-id="d29f3-662">добавление ссылок на командлеты PowerShell, указанные в документации (№13204);</span><span class="sxs-lookup"><span data-stu-id="d29f3-662">Add links to PowerShell cmdlets referenced in the document (#13204)</span></span>
  * <span data-ttu-id="d29f3-663">добавление ссылок на командлеты PowerShell, указанные в документации (№13205).</span><span class="sxs-lookup"><span data-stu-id="d29f3-663">Add links to PowerShell cmdlets referenced in the document (#13205)</span></span>

## <a name="480---october-2020"></a><span data-ttu-id="d29f3-664">4.8.0 — октябрь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-664">4.8.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d29f3-665">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d29f3-665">Az.Accounts</span></span>
* <span data-ttu-id="d29f3-666">Исправлена проблема с анализом фиксированных дат DateTime в общих библиотеках [№ 13045]</span><span class="sxs-lookup"><span data-stu-id="d29f3-666">Fixed DateTime parse issue in common libraries [#13045]</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d29f3-667">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-667">Az.CognitiveServices</span></span>
* <span data-ttu-id="d29f3-668">Добавлен командлет New-AzCognitiveServicesAccountApiProperty.</span><span class="sxs-lookup"><span data-stu-id="d29f3-668">Added 'New-AzCognitiveServicesAccountApiProperty' cmdlet.</span></span>
* <span data-ttu-id="d29f3-669">Добавлена поддержка параметра ApiProperty для New-AzCognitiveServicesAccount и Set-AzCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="d29f3-669">Supported 'ApiProperty' parameter for 'New-AzCognitiveServicesAccount' and 'Set-AzCognitiveServicesAccount'</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d29f3-670">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-670">Az.Compute</span></span>
* <span data-ttu-id="d29f3-671">Исправлена проблема в Update-ASRRecoveryPlan путем заполнения FailoverTypes.</span><span class="sxs-lookup"><span data-stu-id="d29f3-671">Fixed issue in 'Update-ASRRecoveryPlan' by populating FailoverTypes</span></span>
* <span data-ttu-id="d29f3-672">В командлет Get-AzVmImage добавлены необязательные параметры -Top и -OrderBy.</span><span class="sxs-lookup"><span data-stu-id="d29f3-672">Added the '-Top' and '-OrderBy' optional parameters to the 'Get-AzVmImage' cmdlet.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="d29f3-673">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="d29f3-673">Az.Databricks</span></span>
* <span data-ttu-id="d29f3-674">Вышла общедоступная версия модуля Az.Databricks.</span><span class="sxs-lookup"><span data-stu-id="d29f3-674">General availability of 'Az.Databricks' module</span></span>
* <span data-ttu-id="d29f3-675">Добавлена поддержка пиринга между виртуальными сетями</span><span class="sxs-lookup"><span data-stu-id="d29f3-675">Added support for virtual network peering</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d29f3-676">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d29f3-676">Az.DataFactory</span></span>
* <span data-ttu-id="d29f3-677">Исправлена опечатка в выходных сообщениях</span><span class="sxs-lookup"><span data-stu-id="d29f3-677">Fixed typo in output messages</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d29f3-678">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d29f3-678">Az.EventHub</span></span>
* <span data-ttu-id="d29f3-679">Добавлен необязательный параметр-переключатель TrustedServiceAccessEnabled в командлет Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d29f3-679">Added optional switch parameter 'TrustedServiceAccessEnabled' to 'Set-AzEventHubNetworkRuleSet' cmdlet</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d29f3-680">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d29f3-680">Az.HDInsight</span></span>
* <span data-ttu-id="d29f3-681">Добавлено предупреждающее сообщение о том, что планируется прекращение поддержки параметров PublicNetworkAccessType и OutboundPublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="d29f3-681">Added warning message for planning to deprecate the parameters 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="d29f3-682">Добавлено предупреждающее сообщение о том, что планируется замена параметра DefaultStorageAccountName на StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="d29f3-682">Added warning message for planning to replace the parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="d29f3-683">Добавлено предупреждающее сообщение о том, что планируется замена параметра DefaultStorageAccountKey на StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d29f3-683">Added warning message for planning to replace the parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
* <span data-ttu-id="d29f3-684">Добавлено предупреждающее сообщение о том, что планируется замена параметра DefaultStorageAccountType на StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="d29f3-684">Added warning message for planning to replace the parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
* <span data-ttu-id="d29f3-685">Добавлено предупреждающее сообщение о том, что планируется замена параметра DefaultStorageContainer на StorageContainer</span><span class="sxs-lookup"><span data-stu-id="d29f3-685">Added warning message for planning to replace the parameter 'DefaultStorageContainer' with 'StorageContainer'</span></span>
* <span data-ttu-id="d29f3-686">Добавлено предупреждающее сообщение о том, что планируется замена параметра DefaultStorageRootPath на StorageRootPath</span><span class="sxs-lookup"><span data-stu-id="d29f3-686">Added warning message for planning to replace the parameter 'DefaultStorageRootPath' with 'StorageRootPath'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d29f3-687">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d29f3-687">Az.IotHub</span></span>
* <span data-ttu-id="d29f3-688">Обновлен пакет SDK для устройств.</span><span class="sxs-lookup"><span data-stu-id="d29f3-688">Updated devices sdk.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d29f3-689">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d29f3-689">Az.KeyVault</span></span>
* <span data-ttu-id="d29f3-690">Указана точная дата удаления свойства SecretValueText</span><span class="sxs-lookup"><span data-stu-id="d29f3-690">Provided the detailed date of removing property SecretValueText</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="d29f3-691">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-691">Az.ManagedServices</span></span>
* <span data-ttu-id="d29f3-692">Изменены предупреждения о критических изменениях в командлетах назначения и определения управляемых служб.</span><span class="sxs-lookup"><span data-stu-id="d29f3-692">Updated breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d29f3-693">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d29f3-693">Az.Monitor</span></span>
* <span data-ttu-id="d29f3-694">Исправлена ошибка, не позволявшая подавить предупреждающие сообщения.</span><span class="sxs-lookup"><span data-stu-id="d29f3-694">Fixed the bug that warning message cannot be suppressed.</span></span> <span data-ttu-id="d29f3-695">[№ 12889]</span><span class="sxs-lookup"><span data-stu-id="d29f3-695">[#12889]</span></span>
* <span data-ttu-id="d29f3-696">Добавлена поддержка параметра SkipMetricValidation в критериях правила генерации оповещений.</span><span class="sxs-lookup"><span data-stu-id="d29f3-696">Supported 'SkipMetricValidation' parameter in alert rule criteria.</span></span> <span data-ttu-id="d29f3-697">Это позволяет создать правило генерации оповещений для пользовательской метрики, которая еще не создана, настроив пропуск проверки этой метрики.</span><span class="sxs-lookup"><span data-stu-id="d29f3-697">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d29f3-698">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d29f3-698">Az.Network</span></span>
* <span data-ttu-id="d29f3-699">Добавлена политика Office365 в ресурс VPNSite</span><span class="sxs-lookup"><span data-stu-id="d29f3-699">Added Office365 Policy to VPNSite Resource</span></span>
    - <span data-ttu-id="d29f3-700">New-AzO365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="d29f3-700">'New-AzO365PolicyProperty'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d29f3-701">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-701">Az.RecoveryServices</span></span>
* <span data-ttu-id="d29f3-702">Добавлена проверка имени контейнера для резервного копирования рабочей нагрузки.</span><span class="sxs-lookup"><span data-stu-id="d29f3-702">Added container name validation for workload backup.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="d29f3-703">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d29f3-703">Az.RedisCache</span></span>
* <span data-ttu-id="d29f3-704">Устранен сбой командлетов New-AzRedisCache и Set-AzRedisCache из-за проблемы с разрешениями, связанной с регистрацией поставщика ресурсов Microsoft.Cache</span><span class="sxs-lookup"><span data-stu-id="d29f3-704">Made 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets not fail because of permission issue related to registering Microsoft.Cache RP</span></span>

#### <a name="azsql"></a><span data-ttu-id="d29f3-705">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-705">Az.Sql</span></span>
* <span data-ttu-id="d29f3-706">Добавлен параметр BackupStorageRedundancy к следующим командлетам:</span><span class="sxs-lookup"><span data-stu-id="d29f3-706">Added BackupStorageRedundancy to the following:</span></span> 
    - <span data-ttu-id="d29f3-707">Restore-AzureRmSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="d29f3-707">'Restore-AzureRmSqlDatabase'</span></span>
    - <span data-ttu-id="d29f3-708">New-AzSqlDatabaseCopy;</span><span class="sxs-lookup"><span data-stu-id="d29f3-708">'New-AzSqlDatabaseCopy'</span></span>
    - <span data-ttu-id="d29f3-709">New-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="d29f3-709">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="d29f3-710">Удален учет регистра для параметра BackupStorageRedundancy во всех ссылках на базы данных SQL</span><span class="sxs-lookup"><span data-stu-id="d29f3-710">Removed case sensitivity for BackupStorageRedundancy parameter for all SQL DB references</span></span> 
* <span data-ttu-id="d29f3-711">Обновлены имена в предупреждающем сообщении BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="d29f3-711">Updated BackupStorageRedundancy warning message names</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d29f3-712">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d29f3-712">Az.Storage</span></span>
* <span data-ttu-id="d29f3-713">Добавлена поддержка включения, отключения и получения свойств обратимого удаления для общей папки в службе файлов учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="d29f3-713">Supported enable/disable/get share soft delete properties on file Service of a Storage account</span></span>
    - <span data-ttu-id="d29f3-714">Update-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d29f3-714">'Update-AzStorageFileServiceProperty'</span></span>
    - <span data-ttu-id="d29f3-715">Get-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d29f3-715">'Get-AzStorageFileServiceProperty'</span></span>
* <span data-ttu-id="d29f3-716">Поддерживается вывод списка общих папок в учетной записи хранения, включая удаленные общие папки, а также добавлена возможность получить данные об использовании одной общей папки.</span><span class="sxs-lookup"><span data-stu-id="d29f3-716">Supported list file shares include the deleted ones of a Storage account, and Get single file share usage</span></span>
    - <span data-ttu-id="d29f3-717">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="d29f3-717">'Get-AzRmStorageShare'</span></span>
* <span data-ttu-id="d29f3-718">Добавлено восстановление удаленной общей папки</span><span class="sxs-lookup"><span data-stu-id="d29f3-718">Supported restore a deleted file share</span></span>
    - <span data-ttu-id="d29f3-719">Restore-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="d29f3-719">'Restore-AzRmStorageShare'</span></span>
* <span data-ttu-id="d29f3-720">Изменены командлеты для изменения свойств службы BLOB-объектов. Эти командлеты не получают свойства с сервера, а только сохраняют новые параметры на сервер.</span><span class="sxs-lookup"><span data-stu-id="d29f3-720">Changed the cmdlets for modify blob service properties, won't get the original properties from server, but only set the modified properties to server.</span></span>
    - <span data-ttu-id="d29f3-721">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d29f3-721">'Enable-AzStorageBlobDeleteRetentionPolicy'</span></span>
    - <span data-ttu-id="d29f3-722">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d29f3-722">'Disable-AzStorageBlobDeleteRetentionPolicy'</span></span>  
    - <span data-ttu-id="d29f3-723">Enable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="d29f3-723">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="d29f3-724">Disable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="d29f3-724">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="d29f3-725">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d29f3-725">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="d29f3-726">Устранена проблема с получением справки для значения по умолчанию для параметра -Kind командлета New-AzStorageAccount [№ 12189]</span><span class="sxs-lookup"><span data-stu-id="d29f3-726">Fixed help issue for New-AzStorageAccount parameter -Kind default value [#12189]</span></span>
* <span data-ttu-id="d29f3-727">Устранена проблема путем добавления примера правильной настройки ContentType для отправки большого двоичного объекта [№ 12989]</span><span class="sxs-lookup"><span data-stu-id="d29f3-727">Fixed issue by add example to show how to set correct ContentType in blob upload [#12989]</span></span>

## <a name="470---september-2020"></a><span data-ttu-id="d29f3-728">4.7.0 — сентябрь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-728">4.7.0 - September 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d29f3-729">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d29f3-729">Az.Accounts</span></span>
* <span data-ttu-id="d29f3-730">Изменен формат сообщений о предстоящих критических изменениях.</span><span class="sxs-lookup"><span data-stu-id="d29f3-730">Formatted the upcoming breaking change messages</span></span>
* <span data-ttu-id="d29f3-731">Версия Azure.Core обновлена до 1.4.1.</span><span class="sxs-lookup"><span data-stu-id="d29f3-731">Updated Azure.Core to 1.4.1</span></span>

#### <a name="azaks"></a><span data-ttu-id="d29f3-732">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="d29f3-732">Az.Aks</span></span>
* <span data-ttu-id="d29f3-733">Добавлена логика проверки параметров на стороне клиента для командлетов New-AzAksCluster, Set-AzAksCluster и New-AzAksNodePool.</span><span class="sxs-lookup"><span data-stu-id="d29f3-733">Added client side parameter validation logic for 'New-AzAksCluster', 'Set-AzAksCluster' and 'New-AzAksNodePool'.</span></span> <span data-ttu-id="d29f3-734">[12372]</span><span class="sxs-lookup"><span data-stu-id="d29f3-734">[#12372]</span></span>
* <span data-ttu-id="d29f3-735">Добавлена поддержка для надстроек в командлете New-AzAksCluster.</span><span class="sxs-lookup"><span data-stu-id="d29f3-735">Added support for add-ons in 'New-AzAksCluster'.</span></span> <span data-ttu-id="d29f3-736">[11239]</span><span class="sxs-lookup"><span data-stu-id="d29f3-736">[#11239]</span></span>
* <span data-ttu-id="d29f3-737">Добавлены командлеты Enable-AzAksAddOn и Disable-AzAksAddOn для надстроек.</span><span class="sxs-lookup"><span data-stu-id="d29f3-737">Added cmdlets 'Enable-AzAksAddOn' and 'Disable-AzAksAddOn' for add-ons.</span></span> <span data-ttu-id="d29f3-738">[11239]</span><span class="sxs-lookup"><span data-stu-id="d29f3-738">[#11239]</span></span>
* <span data-ttu-id="d29f3-739">Добавлен параметр GenerateSshKey для командлета New-AzAksCluster.</span><span class="sxs-lookup"><span data-stu-id="d29f3-739">Added parameter 'GenerateSshKey' for 'New-AzAksCluster'.</span></span> <span data-ttu-id="d29f3-740">[12371]</span><span class="sxs-lookup"><span data-stu-id="d29f3-740">[#12371]</span></span>
* <span data-ttu-id="d29f3-741">Обновлена версия API до 2020-06-01.</span><span class="sxs-lookup"><span data-stu-id="d29f3-741">Updated api version to 2020-06-01.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d29f3-742">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-742">Az.CognitiveServices</span></span>
* <span data-ttu-id="d29f3-743">Реализовано отображение дополнительных юридических условий для определенных API.</span><span class="sxs-lookup"><span data-stu-id="d29f3-743">Showed additional legal terms for certain APIs.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d29f3-744">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-744">Az.Compute</span></span>
* <span data-ttu-id="d29f3-745">Добавлен необязательный параметр -EncryptionType к командлету New-AzVmDiskEncryptionSetConfig.</span><span class="sxs-lookup"><span data-stu-id="d29f3-745">Added the '-EncryptionType' optional parameter to 'New-AzVmDiskEncryptionSetConfig'</span></span>
* <span data-ttu-id="d29f3-746">Новые командлеты для нового типа ресурсов: DiskAccess (Get-AzDiskAccess, New-AzDiskAccess, Get-AzDiskAccess).</span><span class="sxs-lookup"><span data-stu-id="d29f3-746">New cmdlets for new resource type: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span></span>
* <span data-ttu-id="d29f3-747">Добавлены необязательные параметры -DiskAccessId и -NetworkAccessPolicy к командлету New-AzSnapshotConfig.</span><span class="sxs-lookup"><span data-stu-id="d29f3-747">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzSnapshotConfig'</span></span>
* <span data-ttu-id="d29f3-748">Добавлены необязательные параметры -DiskAccessId и -NetworkAccessPolicy к командлету New-AzDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="d29f3-748">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzDiskConfig'</span></span>
* <span data-ttu-id="d29f3-749">Добавлено свойство PatchStatus к представлению экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d29f3-749">Added 'PatchStatus' property to VirtualMachine Instance View</span></span>
* <span data-ttu-id="d29f3-750">Добавлено свойство VMHealth к представлению экземпляра виртуальной машины, которое является возвращенным объектом при вызове Get-AzVm с параметром -Status.</span><span class="sxs-lookup"><span data-stu-id="d29f3-750">Added 'VMHealth' property to the virtual machine's instance view, which is the returned object when 'Get-AzVm' is invoked with '-Status'</span></span>
* <span data-ttu-id="d29f3-751">Добавлено поле AssignedHost к представлениям экземпляра Get-AzVM и Get-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="d29f3-751">Added 'AssignedHost' field to 'Get-AzVM' and 'Get-AzVmss' instance views.</span></span> <span data-ttu-id="d29f3-752">В поле отображается идентификатор ресурса для экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d29f3-752">The field shows the resource id of the virtual machine instance</span></span>
* <span data-ttu-id="d29f3-753">Добавлен необязательный параметр -SupportAutomaticPlacement к командлету New-AzHostGroup.</span><span class="sxs-lookup"><span data-stu-id="d29f3-753">Added optional parameter '-SupportAutomaticPlacement' to 'New-AzHostGroup'</span></span> 
* <span data-ttu-id="d29f3-754">Добавлен параметр -HostGroupId к командлетам New-AzVm и New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="d29f3-754">Added the '-HostGroupId' parameter to 'New-AzVm' and 'New-AzVmss'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d29f3-755">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d29f3-755">Az.DataFactory</span></span>
* <span data-ttu-id="d29f3-756">Версия пакета SDK ADF для .NET обновлена до 4.11.0.</span><span class="sxs-lookup"><span data-stu-id="d29f3-756">Updated ADF .Net SDK version to 4.11.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d29f3-757">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d29f3-757">Az.EventHub</span></span>
* <span data-ttu-id="d29f3-758">Добавлены новые командлеты кластера: New-AzEventHubCluster, Set-AzEventHubCluster, Get-AzEventHubCluster, Remove-AzEventHubCluster, Get-AzEventHubClustersAvailableRegions.</span><span class="sxs-lookup"><span data-stu-id="d29f3-758">Added new Cluster cmdlets - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span></span>
* <span data-ttu-id="d29f3-759">Исправление для проблемы № 10722: исправление ошибки, из-за которой свойству AuthorizationRule.Rights назначалось только значение Listen (Прослушивание).</span><span class="sxs-lookup"><span data-stu-id="d29f3-759">Fixed for issue #10722 : Fix for assigning only 'Listen' to AuthorizationRule rights.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="d29f3-760">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="d29f3-760">Az.Functions</span></span>
* <span data-ttu-id="d29f3-761">Удалена возможность создавать Функции версии 2 в регионах, которые не поддерживают ее.</span><span class="sxs-lookup"><span data-stu-id="d29f3-761">Removed the ability to create v2 Functions in regions that do not support it.</span></span>
* <span data-ttu-id="d29f3-762">PowerShell 6.2 не рекомендуется к использованию.</span><span class="sxs-lookup"><span data-stu-id="d29f3-762">Deprecated PowerShell 6.2.</span></span> <span data-ttu-id="d29f3-763">Добавлено предупреждение при создании пользователем приложения-функции PowerShell 6.2 о том, что рекомендуется создать приложение-функцию PowerShell 7.0.</span><span class="sxs-lookup"><span data-stu-id="d29f3-763">Added a warning for when a user creates a PowerShell 6.2 function app that advises them to create a PowerShell 7.0 function app instead.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d29f3-764">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d29f3-764">Az.HDInsight</span></span>
* <span data-ttu-id="d29f3-765">Добавлена поддержка создания кластера с использованием конфигурации автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="d29f3-765">Supported creating cluster with Autoscale configuration</span></span>
    - <span data-ttu-id="d29f3-766">Добавлен новый параметр AutoscaleConfiguration к командлету New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="d29f3-766">Add new parameter 'AutoscaleConfiguration' to the cmdlet 'New-AzHDInsightCluster'</span></span>
* <span data-ttu-id="d29f3-767">Добавлена поддержка управления конфигурацией автомасштабирования для кластера.</span><span class="sxs-lookup"><span data-stu-id="d29f3-767">Supported operating cluster's Autoscale configuration</span></span>
    - <span data-ttu-id="d29f3-768">Добавлен новый командлет Get-AzHDInsihgtClusterAutoscaleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d29f3-768">Add new cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="d29f3-769">Добавлен новый командлет New-AzHDInsihgtClusterAutoscaleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d29f3-769">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="d29f3-770">Добавлен новый командлет Set-AzHDInsihgtClusterAutoscaleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d29f3-770">Add new cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="d29f3-771">Добавлен новый командлет Remove-AzHDInsihgtClusterAutoscaleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d29f3-771">Add new cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="d29f3-772">Добавлен новый командлет New-AzHDInsihgtClusterAutoscaleScheduleCondition.</span><span class="sxs-lookup"><span data-stu-id="d29f3-772">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d29f3-773">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d29f3-773">Az.KeyVault</span></span>
* <span data-ttu-id="d29f3-774">Добавлена поддержка авторизации с помощью RBAC [10557].</span><span class="sxs-lookup"><span data-stu-id="d29f3-774">Added support for RBAC authorization [#10557]</span></span>
* <span data-ttu-id="d29f3-775">Расширена обработка ошибок в командлете Set-AzKeyVaultAccessPolicy [4007].</span><span class="sxs-lookup"><span data-stu-id="d29f3-775">Enhanced error handling in 'Set-AzKeyVaultAccessPolicy' [#4007]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="d29f3-776">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="d29f3-776">Az.Kusto</span></span>
* <span data-ttu-id="d29f3-777">Выпущена общедоступная версия модуля Az.Kusto.</span><span class="sxs-lookup"><span data-stu-id="d29f3-777">General availability of 'Az.Kusto' module</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d29f3-778">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d29f3-778">Az.Network</span></span>
* <span data-ttu-id="d29f3-779">[Критическое изменение] Обновлены приведенные ниже командлеты для соответствия виртуальному маршрутизатору ресурсов и виртуальному концентратору.</span><span class="sxs-lookup"><span data-stu-id="d29f3-779">[Breaking Change] Updated below cmdlets to align resource virtual router and virtual hub</span></span>
    - <span data-ttu-id="d29f3-780">New-AzVirtualRouter:</span><span class="sxs-lookup"><span data-stu-id="d29f3-780">'New-AzVirtualRouter':</span></span> 
        - <span data-ttu-id="d29f3-781">Добавлен параметр -HostedSubnet для поддержки дочернего ресурса конфигурации IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-781">Added -HostedSubnet parameter to support IP configuration child resource</span></span>
        - <span data-ttu-id="d29f3-782">Удалены параметры -HostedGateway и -HostedGatewayId.</span><span class="sxs-lookup"><span data-stu-id="d29f3-782">deleted -HostedGateway and -HostedGatewayId</span></span>
    - <span data-ttu-id="d29f3-783">Get-AzVirtualRouter:</span><span class="sxs-lookup"><span data-stu-id="d29f3-783">'Get-AzVirtualRouter':</span></span>
        - <span data-ttu-id="d29f3-784">добавлен набор параметров на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="d29f3-784">Added subscription level parameter set</span></span>
    - <span data-ttu-id="d29f3-785">Remove-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="d29f3-785">'Remove-AzVirtualRouter'</span></span>
    - <span data-ttu-id="d29f3-786">Add-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="d29f3-786">'Add-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="d29f3-787">Get-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="d29f3-787">'Get-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="d29f3-788">Remove-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="d29f3-788">'Remove-AzVirtualRouterPeer'</span></span>
* <span data-ttu-id="d29f3-789">Добавлен новый командлет для порта Azure Express Route.</span><span class="sxs-lookup"><span data-stu-id="d29f3-789">Added new cmdlet for Azure Express Route Port</span></span>
    - <span data-ttu-id="d29f3-790">New-AzExpressRoutePortLOA</span><span class="sxs-lookup"><span data-stu-id="d29f3-790">'New-AzExpressRoutePortLOA'</span></span>
* <span data-ttu-id="d29f3-791">Добавлено свойство RemoteBgpCommunities к ресурсу пиринга виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d29f3-791">Added RemoteBgpCommunities property to the VirtualNetwork Peering Resource</span></span>
* <span data-ttu-id="d29f3-792">Изменено сообщение с предупреждением для New-AzLoadBalancerFrontendIpConfig, New-AzPublicIpAddress и New-AzPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="d29f3-792">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>
* <span data-ttu-id="d29f3-793">Добавлено свойство VpnGatewayIpConfigurations в выходные данные командлета Get-AzVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="d29f3-793">Added VpnGatewayIpConfigurations to 'Get-AzVpnGateway' output</span></span>
* <span data-ttu-id="d29f3-794">Исправлена ошибка командлета Set-AzApplicationGatewaySslCertificate [9488].</span><span class="sxs-lookup"><span data-stu-id="d29f3-794">Fixed bug for 'Set-AzApplicationGatewaySslCertificate' [#9488]</span></span>
* <span data-ttu-id="d29f3-795">Добавлен параметр AllowActiveFTP в AzureFirewall.</span><span class="sxs-lookup"><span data-stu-id="d29f3-795">Added 'AllowActiveFTP' parameter to 'AzureFirewall'</span></span>
* <span data-ttu-id="d29f3-796">Обновлены следующие команды для функции: Включена возможность настройки и удаления параметров безопасности в Интернете на VPN-шлюзе P2S виртуальной глобальной сети.</span><span class="sxs-lookup"><span data-stu-id="d29f3-796">Updated below commands for feature: Enable internet security set/remove on VirtualWan P2SVpnGateway.</span></span>
- <span data-ttu-id="d29f3-797">Обновлен командлет New-AzP2sVpnGateway: Добавлен необязательный параметр EnableInternetSecurityFlag для клиентов, позволяющий задать значение true для включения безопасности в Интернете на VPN-шлюзе P2S, который будет применяться к клиентам с подключениями типа "точка — сеть".</span><span class="sxs-lookup"><span data-stu-id="d29f3-797">Updated 'New-AzP2sVpnGateway': Added optional switch parameter 'EnableInternetSecurityFlag' for customers to set true to enable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
- <span data-ttu-id="d29f3-798">Обновлен командлет Update-AzP2sVpnGateway: Добавлены необязательные параметры EnableInternetSecurityFlag и DisableInternetSecurityFlag для клиентов, позволяющий задать значение true/false для включения/отключения безопасности в Интернете на VPN-шлюзе P2S, который будет применяться к клиентам с подключениями типа "точка — сеть".</span><span class="sxs-lookup"><span data-stu-id="d29f3-798">Updated 'Update-AzP2sVpnGateway': Added optional switch parameters 'EnableInternetSecurityFlag' or 'DisableInternetSecurityFlag' for customers to set true/false to enable/disable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
* <span data-ttu-id="d29f3-799">Добавлен новый командлет Reset-AzP2sVpnGateway для клиентов, позволяющий сбрасывать и перезагружать VPN-шлюз P2S виртуальной глобальной сети для устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="d29f3-799">Added new cmdlet 'Reset-AzP2sVpnGateway' for customers to reset/reboot their VirtualWan P2SVpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="d29f3-800">Добавлен новый командлет Reset-AzVpnGateway для клиентов, позволяющий сбрасывать и перезагружать VPN-шлюз виртуальной глобальной сети для устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="d29f3-800">Added new cmdlet 'Reset-AzVpnGateway' for customers to reset/reboot their VirtualWan VpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="d29f3-801">Обновлен командлет Set-AzVirtualNetworkSubnetConfig.</span><span class="sxs-lookup"><span data-stu-id="d29f3-801">Updated 'Set-AzVirtualNetworkSubnetConfig'</span></span>
    - <span data-ttu-id="d29f3-802">Для свойств группы безопасности сети и таблицы маршрутизации подсети теперь задаются значения NULL, если они явно указаны в параметрах [1548][9718].</span><span class="sxs-lookup"><span data-stu-id="d29f3-802">Set NSG and Route Table properties of subnet to null if explicitly set in parameters [#1548][#9718]</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d29f3-803">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-803">Az.RecoveryServices</span></span>
* <span data-ttu-id="d29f3-804">Исправлено состояние удаления для элементов резервного копирования рабочей нагрузки.</span><span class="sxs-lookup"><span data-stu-id="d29f3-804">Fixed the Delete State for workload Backup Items.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d29f3-805">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-805">Az.Resources</span></span>
* <span data-ttu-id="d29f3-806">Добавлена отсутствующая проверка для командлета Set-AzRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="d29f3-806">Added missing check for Set-AzRoleAssignment</span></span>
* <span data-ttu-id="d29f3-807">Добавлен важный атрибут в параметр SubscriptionId командлета Get-AzResourceGroupDeploymentOperation.</span><span class="sxs-lookup"><span data-stu-id="d29f3-807">Added breaking change attribute to 'SubscriptionId' parameter of 'Get-AzResourceGroupDeploymentOperation'</span></span>
* <span data-ttu-id="d29f3-808">Обновлены командлеты What-If шаблона ARM для отображения изменений ресурса Ignore последними.</span><span class="sxs-lookup"><span data-stu-id="d29f3-808">Updated ARM template What-If cmdlets to show 'Ignore' resource changes last</span></span>
* <span data-ttu-id="d29f3-809">Исправлены проблемы безопасности и сериализации параметров массива для командлетов развертывания [12773].</span><span class="sxs-lookup"><span data-stu-id="d29f3-809">Fixed secure and array parameter serialization issues for deployment cmdlets [#12773]</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d29f3-810">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d29f3-810">Az.ServiceFabric</span></span>
* <span data-ttu-id="d29f3-811">Добавлены новые командлеты для управляемых кластеров и типов узлов:</span><span class="sxs-lookup"><span data-stu-id="d29f3-811">Added new cmdlets for managed clusters and node types:</span></span>
    - <span data-ttu-id="d29f3-812">New-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="d29f3-812">'New-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="d29f3-813">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="d29f3-813">'Get-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="d29f3-814">Set-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="d29f3-814">'Set-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="d29f3-815">Remove-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="d29f3-815">'Remove-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="d29f3-816">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="d29f3-816">'Add-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="d29f3-817">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="d29f3-817">'Remove-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="d29f3-818">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="d29f3-818">'New-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="d29f3-819">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="d29f3-819">'Get-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="d29f3-820">Set-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="d29f3-820">'Set-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="d29f3-821">Remove-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="d29f3-821">'Remove-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="d29f3-822">Add-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="d29f3-822">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="d29f3-823">Add-AzServiceFabricManagedNodeTypeVMSecret</span><span class="sxs-lookup"><span data-stu-id="d29f3-823">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span></span>
    - <span data-ttu-id="d29f3-824">Remove-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="d29f3-824">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="d29f3-825">Restart-AzServiceFabricManagedNodeTyp</span><span class="sxs-lookup"><span data-stu-id="d29f3-825">'Restart-AzServiceFabricManagedNodeTyp'</span></span>
* <span data-ttu-id="d29f3-826">Пакет SDK для Service Fabric обновлен до версии 1.2.0, в которой используется версия API 2020-03-01 поставщика ресурсов Service Fabric для текущей модели и 2020-01-01-preview для управляемых кластеров.</span><span class="sxs-lookup"><span data-stu-id="d29f3-826">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2020-03-01 for the current model and 2020-01-01-preview for managed clusters.</span></span>

#### <a name="azsql"></a><span data-ttu-id="d29f3-827">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-827">Az.Sql</span></span>
* <span data-ttu-id="d29f3-828">Добавлен параметр BackupStorageRedundancy к командлетам New-AzSqlInstance и Get-AzSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="d29f3-828">Added BackupStorageRedundancy to 'New-AzSqlInstance' and 'Get-AzSqlInstance'</span></span>
* <span data-ttu-id="d29f3-829">Добавлен командлет Get-AzSqlServerActiveDirectoryOnlyAuthentication.</span><span class="sxs-lookup"><span data-stu-id="d29f3-829">Added cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="d29f3-830">Добавлен командлет Enable-AzSqlServerActiveDirectoryOnlyAuthentication.</span><span class="sxs-lookup"><span data-stu-id="d29f3-830">Added cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="d29f3-831">Добавлен параметр Force к командлету New-AzSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="d29f3-831">Added Force parameter to 'New-AzSqlInstance'</span></span>
* <span data-ttu-id="d29f3-832">Добавлены командлеты для службы воспроизведения журнала управляемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="d29f3-832">Added cmdlets for Managed Database Log Replay service</span></span>
    - <span data-ttu-id="d29f3-833">Start-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="d29f3-833">'Start-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="d29f3-834">Get-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="d29f3-834">'Get-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="d29f3-835">Complete-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="d29f3-835">'Complete-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="d29f3-836">Stop-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="d29f3-836">'Stop-AzSqlInstanceDatabaseLogReplay'</span></span>
* <span data-ttu-id="d29f3-837">Добавлен командлет Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.</span><span class="sxs-lookup"><span data-stu-id="d29f3-837">Added cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="d29f3-838">Добавлен командлет Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.</span><span class="sxs-lookup"><span data-stu-id="d29f3-838">Added cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="d29f3-839">Добавлен командлет Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.</span><span class="sxs-lookup"><span data-stu-id="d29f3-839">Added cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="d29f3-840">Обновлены командлеты New-AzSqlDatabaseImport и New-AzSqlDatabaseExport для поддержки функциональности сетевой изоляции.</span><span class="sxs-lookup"><span data-stu-id="d29f3-840">Updated cmdlets 'New-AzSqlDatabaseImport' and 'New-AzSqlDatabaseExport' to support network isolation functionality</span></span>
* <span data-ttu-id="d29f3-841">Добавлен командлет New-AzSqlDatabaseImportExisting.</span><span class="sxs-lookup"><span data-stu-id="d29f3-841">Added cmdlet 'New-AzSqlDatabaseImportExisting'</span></span>
* <span data-ttu-id="d29f3-842">Обновлены командлеты баз данных для поддержки указания типа хранилища резервных копий.</span><span class="sxs-lookup"><span data-stu-id="d29f3-842">Updated Databases cmdlets to support backup storage type specification</span></span>
* <span data-ttu-id="d29f3-843">Добавлен параметр Force к командлету New-AzSqlDatabase.</span><span class="sxs-lookup"><span data-stu-id="d29f3-843">Added Force parameter to 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="d29f3-844">Добавлено предупреждение для конфигурации BackupStorageRedundancy в выбранных регионах в командлете New-AzSqlDatabase.</span><span class="sxs-lookup"><span data-stu-id="d29f3-844">Added warning for BackupStorageRedundancy configuration in select regions in 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="d29f3-845">Обновлены командлеты ActiveDirectoryOnlyAuthentication для сервера и экземпляра для включения ResourceId и InputObject.</span><span class="sxs-lookup"><span data-stu-id="d29f3-845">Updated ActiveDirectoryOnlyAuthentication cmdlets for server and instance to include ResourceId and InputObject</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d29f3-846">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d29f3-846">Az.Storage</span></span>
* <span data-ttu-id="d29f3-847">Исправлен сбой отправки BLOB-объекта путем обновления до Microsoft.Azure.Storage.DataMovement 2.0.0 [12220].</span><span class="sxs-lookup"><span data-stu-id="d29f3-847">Fixed upload blob fail by upgrade to Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span></span>
* <span data-ttu-id="d29f3-848">Реализована поддержка восстановления до точки во времени.</span><span class="sxs-lookup"><span data-stu-id="d29f3-848">Supported Point In Time Restore</span></span>
    - <span data-ttu-id="d29f3-849">Enable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="d29f3-849">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="d29f3-850">Disable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="d29f3-850">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="d29f3-851">New-AzStorageBlobRangeToRestore</span><span class="sxs-lookup"><span data-stu-id="d29f3-851">'New-AzStorageBlobRangeToRestore'</span></span>
    - <span data-ttu-id="d29f3-852">Restore-AzStorageBlobRange</span><span class="sxs-lookup"><span data-stu-id="d29f3-852">'Restore-AzStorageBlobRange'</span></span>
* <span data-ttu-id="d29f3-853">Реализована поддержка получения состояния восстановления BLOB-объекта путем выполнения командлета Get-AzureRmStorageAccount с параметром -IncludeBlobRestoreStatus.</span><span class="sxs-lookup"><span data-stu-id="d29f3-853">Supported get blob restore status of Storage account by run get-AzureRMStorageAccount with parameter -IncludeBlobRestoreStatus</span></span> 
    - <span data-ttu-id="d29f3-854">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d29f3-854">'Get-AzureRMStorageAccount'</span></span>
* <span data-ttu-id="d29f3-855">Добавлено важное сообщение с предупреждением о предстоящем изменении выходных данных командлета.</span><span class="sxs-lookup"><span data-stu-id="d29f3-855">Added breaking change warning message for upcoming cmdlet output change</span></span>
    - <span data-ttu-id="d29f3-856">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d29f3-856">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="d29f3-857">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d29f3-857">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="d29f3-858">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d29f3-858">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="d29f3-859">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d29f3-859">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="d29f3-860">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="d29f3-860">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="d29f3-861">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="d29f3-861">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="d29f3-862">Версия пакета SDK Microsoft.Azure.Cosmos.Table обновлена до 1.0.8.</span><span class="sxs-lookup"><span data-stu-id="d29f3-862">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.8</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="d29f3-863">Благодарим наших участников сообщества</span><span class="sxs-lookup"><span data-stu-id="d29f3-863">Thanks to our community contributors</span></span>
* <span data-ttu-id="d29f3-864">Томас Ван Лере (Thomas Van Laere) (@ThomVanL), добавление Dockerfile-alpine-3.10 (12911).</span><span class="sxs-lookup"><span data-stu-id="d29f3-864">Thomas Van Laere (@ThomVanL), Add Dockerfile-alpine-3.10 (#12911)</span></span> 
* <span data-ttu-id="d29f3-865">Лохит Чаудари Чилукури (Lohith Chowdary Chilukuri) (@Lochiluk), обновление Remove-AzNetworkInterfaceIpConfig.md (12807).</span><span class="sxs-lookup"><span data-stu-id="d29f3-865">Lohith Chowdary Chilukuri (@Lochiluk), Update Remove-AzNetworkInterfaceIpConfig.md (#12807)</span></span> 
* <span data-ttu-id="d29f3-866">Роберт Стрэнд (Roberth Strand) (@roberthstrand), Get-AzResourceGroup — новый пример и очистка (12828).</span><span class="sxs-lookup"><span data-stu-id="d29f3-866">Roberth Strand (@roberthstrand), Get-AzResourceGroup - New example, and cleanup (#12828)</span></span> 
* <span data-ttu-id="d29f3-867">Рави Мишра (Ravi Mishra) (@inmishrar), обновление стека среды выполнения веб-приложений Azure до .NET Core (12833).</span><span class="sxs-lookup"><span data-stu-id="d29f3-867">Ravi Mishra (@inmishrar), update Azure Web App runtime stack to DOTNETCORE (#12833)</span></span> 
* <span data-ttu-id="d29f3-868">@jack-education, обновление Set-AzVirtualNetworkSubnetConfig для разрешения удаления группы безопасности сети и таблицы маршрутизации из подсети (12351).</span><span class="sxs-lookup"><span data-stu-id="d29f3-868">@jack-education, Updated Set-AzVirtualNetworkSubnetConfig to allow NSG and Route Table to be removed from subnet (#12351)</span></span> 
* <span data-ttu-id="d29f3-869">@hagop-globanet, обновление Add-AzApplicationGatewayCustomError.md (12784).</span><span class="sxs-lookup"><span data-stu-id="d29f3-869">@hagop-globanet, Update Add-AzApplicationGatewayCustomError.md (#12784)</span></span> 
* <span data-ttu-id="d29f3-870">Джошуа Ван Даален (Joshua Van Daalen) (@greenSacrifice)</span><span class="sxs-lookup"><span data-stu-id="d29f3-870">Joshua Van Daalen (@greenSacrifice)</span></span>
  * <span data-ttu-id="d29f3-871">Изменение правописания Proeprty на Property (12821)</span><span class="sxs-lookup"><span data-stu-id="d29f3-871">Update spelling of Property to Property (#12821)</span></span> 
  * <span data-ttu-id="d29f3-872">Обновление примеров New-AzResourceLock.md (12806)</span><span class="sxs-lookup"><span data-stu-id="d29f3-872">Update New-AzResourceLock.md examples (#12806)</span></span>
* <span data-ttu-id="d29f3-873">Эрагон Риддл (Eragon Riddle) (@eragonriddle), исправлено имя поля параметра в примере (12825)</span><span class="sxs-lookup"><span data-stu-id="d29f3-873">Eragon Riddle (@eragonriddle), Corrected parameter field name in the example (#12825)</span></span> 
* <span data-ttu-id="d29f3-874">@rossifumax, исправление опечатки в New-AzConfigurationAssignment.md (12701)</span><span class="sxs-lookup"><span data-stu-id="d29f3-874">@rossifumax, Fix typo in New-AzConfigurationAssignment.md (#12701)</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="d29f3-875">4.6.1 — август 2020 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-875">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="d29f3-876">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-876">Az.Compute</span></span>
* <span data-ttu-id="d29f3-877">Исправлен параметр -EncryptionAtHost в New-AzVm для удаления значения false по умолчанию [№ 12776].</span><span class="sxs-lookup"><span data-stu-id="d29f3-877">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="d29f3-878">4.6.0 — август 2020 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-878">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d29f3-879">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d29f3-879">Az.Accounts</span></span>
* <span data-ttu-id="d29f3-880">Загружаются все общедоступные облачные среды, когда конечная точка обнаружения не возвращает AzureCloud по умолчанию или другие общедоступные среды [№ 12633]</span><span class="sxs-lookup"><span data-stu-id="d29f3-880">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="d29f3-881">В Get-AzSubscription предоставлен параметр SubscriptionPolicies [№ 12551].</span><span class="sxs-lookup"><span data-stu-id="d29f3-881">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d29f3-882">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d29f3-882">Az.Automation</span></span>
* <span data-ttu-id="d29f3-883">В Set-AzAutomationWebhook добавлен параметр -RunOn для определения группы гибридной рабочей роли.</span><span class="sxs-lookup"><span data-stu-id="d29f3-883">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d29f3-884">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-884">Az.Compute</span></span>
* <span data-ttu-id="d29f3-885">В New-AzVm, New-AzVmss, New-AzVMConfig, New-AzVmssConfig, Update-AzVM и Update-AzVmss добавлен параметр -EncryptionAtHost.</span><span class="sxs-lookup"><span data-stu-id="d29f3-885">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="d29f3-886">В возвращаемый объект Get-AzVM и Get-AzVmss добавлен параметр SecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="d29f3-886">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="d29f3-887">В Get-AzHostGroup добавлен необязательный параметр -InstanceView.</span><span class="sxs-lookup"><span data-stu-id="d29f3-887">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="d29f3-888">Добавлен новый командлет Invoke-AzVmPatchAssessment.</span><span class="sxs-lookup"><span data-stu-id="d29f3-888">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d29f3-889">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d29f3-889">Az.DataFactory</span></span>
* <span data-ttu-id="d29f3-890">В класс PSPipelineRun добавлены отсутствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d29f3-890">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d29f3-891">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d29f3-891">Az.HDInsight</span></span>
* <span data-ttu-id="d29f3-892">Включена поддержка создания кластера с функцией шифрования на узле.</span><span class="sxs-lookup"><span data-stu-id="d29f3-892">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d29f3-893">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d29f3-893">Az.KeyVault</span></span>
* <span data-ttu-id="d29f3-894">Добавлены предупреждающие сообщения для планирования отключения обратимого удаления.</span><span class="sxs-lookup"><span data-stu-id="d29f3-894">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="d29f3-895">Добавлены предупреждающие сообщения для планирования удаления атрибута SecretValueText.</span><span class="sxs-lookup"><span data-stu-id="d29f3-895">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="d29f3-896">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="d29f3-896">Az.Maintenance</span></span>
* <span data-ttu-id="d29f3-897">В New-AzMaintenanceConfiguration добавлены дополнительные поля, связанные с расписанием.</span><span class="sxs-lookup"><span data-stu-id="d29f3-897">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="d29f3-898">Добавлен новый командлет для Get-AzMaintenancePublicConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d29f3-898">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="d29f3-899">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-899">Az.ManagedServices</span></span>
* <span data-ttu-id="d29f3-900">Добавлены предупреждения о критических изменениях в командлетах назначения и определения управляемых служб.</span><span class="sxs-lookup"><span data-stu-id="d29f3-900">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d29f3-901">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d29f3-901">Az.Monitor</span></span>
* <span data-ttu-id="d29f3-902">Расширен набор параметров, заданный в Set-AzDiagnosticSetting, для разделения включения журналов и метрик [№ 12482].</span><span class="sxs-lookup"><span data-stu-id="d29f3-902">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="d29f3-903">Для Add-AzMetricAlertRuleV2 исправлена ошибка, возникающая при получении оповещения метрики из конвейера.</span><span class="sxs-lookup"><span data-stu-id="d29f3-903">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="d29f3-904">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-904">Az.Resources</span></span>
* <span data-ttu-id="d29f3-905">Изменен ответ Get-AzPolicyAlias для включения сведений о том, изменяется ли этот псевдоним Политикой Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-905">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="d29f3-906">Создан новый командлет Set-AzRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="d29f3-906">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="d29f3-907">Добавлен командлет Get-AzDeploymentManagementGroupWhatIfResult для получения результатов выполнения What-If в шаблоне ARM в области группы управления.</span><span class="sxs-lookup"><span data-stu-id="d29f3-907">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="d29f3-908">Добавлен командлет Get-AzTenantWhatIfResult для получения результатов выполнения What-If в шаблоне ARM в области арендатора.</span><span class="sxs-lookup"><span data-stu-id="d29f3-908">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="d29f3-909">Переопределены параметры -WhatIf и -Confirm для New-AzManagementGroupDeployment и New-AzTenantDeployment для использования результатов выполнения What-If в шаблоне ARM.</span><span class="sxs-lookup"><span data-stu-id="d29f3-909">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="d29f3-910">Исправлено поведение параметров -WhatIf и -Confirm для новых командлетов развертывания, чтобы они соответствовали значению False.</span><span class="sxs-lookup"><span data-stu-id="d29f3-910">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="d29f3-911">Исправлена ошибка сериализации для -TemplateObject и TemplateParameterObject [№ 1528] [№ 6292].</span><span class="sxs-lookup"><span data-stu-id="d29f3-911">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="d29f3-912">Добавлен атрибут критического изменения в Get-AzResourceGroupDeploymentOperation для предстоящего изменения типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="d29f3-912">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="d29f3-913">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="d29f3-913">Az.SignalR</span></span>
* <span data-ttu-id="d29f3-914">Исправлены ошибки файлов справки Restart-AzSignalR и Update-AzSignalR.</span><span class="sxs-lookup"><span data-stu-id="d29f3-914">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="d29f3-915">Добавлены командлеты Update-AzSignalRNetworkAcl, Set-AzSignalRUpstream.</span><span class="sxs-lookup"><span data-stu-id="d29f3-915">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d29f3-916">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d29f3-916">Az.Storage</span></span>
* <span data-ttu-id="d29f3-917">Поддерживается ускорение запросов больших двоичных объектов:</span><span class="sxs-lookup"><span data-stu-id="d29f3-917">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="d29f3-918">Get-AzStorageBlobQueryResult;</span><span class="sxs-lookup"><span data-stu-id="d29f3-918">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="d29f3-919">New-AzStorageBlobQueryConfig.</span><span class="sxs-lookup"><span data-stu-id="d29f3-919">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="d29f3-920">Обновлен файл справки; дополнено описание и исправлена опечатка.</span><span class="sxs-lookup"><span data-stu-id="d29f3-920">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="d29f3-921">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="d29f3-921">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="d29f3-922">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="d29f3-922">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="d29f3-923">Исправлена ошибка, из-за которой работа большого двоичного объекта завершается ошибкой, если связанный подкаталог не существует [№ 12592].</span><span class="sxs-lookup"><span data-stu-id="d29f3-923">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="d29f3-924">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d29f3-924">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="d29f3-925">Включена поддержка задания, получения и удаления политики репликации объекта в учетных записях хранения:</span><span class="sxs-lookup"><span data-stu-id="d29f3-925">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="d29f3-926">New-AzStorageObjectReplicationPolicyRule;</span><span class="sxs-lookup"><span data-stu-id="d29f3-926">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="d29f3-927">Set-AzStorageObjectReplicationPolicy;</span><span class="sxs-lookup"><span data-stu-id="d29f3-927">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="d29f3-928">Get-AzStorageObjectReplicationPolicy;</span><span class="sxs-lookup"><span data-stu-id="d29f3-928">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="d29f3-929">Remove-AzStorageObjectReplicationPolicy.</span><span class="sxs-lookup"><span data-stu-id="d29f3-929">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="d29f3-930">Включена поддержка включения и отключения канала изменений в службе BLOB-объектов учетной записи хранения:</span><span class="sxs-lookup"><span data-stu-id="d29f3-930">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="d29f3-931">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d29f3-931">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="d29f3-932">4.5.0 — август 2020 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-932">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d29f3-933">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d29f3-933">Az.Accounts</span></span>
* <span data-ttu-id="d29f3-934">Командлет Connect-AzAccount теперь принимает параметр MaxContextPopulation (№ 9865).</span><span class="sxs-lookup"><span data-stu-id="d29f3-934">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="d29f3-935">Версия SubscriptionClient обновлена до 2019-06-01 и поддерживает отображение доменов арендаторов (№ 9838).</span><span class="sxs-lookup"><span data-stu-id="d29f3-935">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="d29f3-936">Добавлена поддержка домашнего арендатора и сведений managedBy арендатора для подписки.</span><span class="sxs-lookup"><span data-stu-id="d29f3-936">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="d29f3-937">Исправлено имя модуля и сведения о версии в данных телеметрии.</span><span class="sxs-lookup"><span data-stu-id="d29f3-937">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="d29f3-938">Исправлено поведение SqlDatabaseDnsSuffix и ServiceManagementUrl, когда конечная точка метаданных среды возвращает несовместимое значение.</span><span class="sxs-lookup"><span data-stu-id="d29f3-938">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="d29f3-939">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="d29f3-939">Az.Aks</span></span>
* <span data-ttu-id="d29f3-940">Параметр ClientIdAndSecret замен на ServicePrincipalIdAndSecret и задан в виде псевдонима (№ 12381).</span><span class="sxs-lookup"><span data-stu-id="d29f3-940">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="d29f3-941">Командлеты Get-AzAks, New-AzAks, Remove-AzAks, Set-AzAks заменены на Get-AzAksCluster, New-AzAksCluster, Remove-AzAksCluster, Set-AzAksCluster. Исходные командлеты заданы в виде псевдонимов (№ 12373).</span><span class="sxs-lookup"><span data-stu-id="d29f3-941">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d29f3-942">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d29f3-942">Az.ApiManagement</span></span>
* <span data-ttu-id="d29f3-943">Добавлен новый командлет Add-AzApiManagementApiToGateway.</span><span class="sxs-lookup"><span data-stu-id="d29f3-943">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="d29f3-944">Добавлен новый командлет Get-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="d29f3-944">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="d29f3-945">Добавлен новый командлет Get-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d29f3-945">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="d29f3-946">Добавлен новый командлет Get-AzApiManagementGatewayKey.</span><span class="sxs-lookup"><span data-stu-id="d29f3-946">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="d29f3-947">Добавлен новый командлет New-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="d29f3-947">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="d29f3-948">Добавлен новый командлет New-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d29f3-948">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="d29f3-949">Добавлен новый командлет New-AzApiManagementResourceLocationObject.</span><span class="sxs-lookup"><span data-stu-id="d29f3-949">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="d29f3-950">Добавлен новый командлет Remove-AzApiManagementApiFromGateway.</span><span class="sxs-lookup"><span data-stu-id="d29f3-950">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="d29f3-951">Добавлен новый командлет Remove-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="d29f3-951">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="d29f3-952">Добавлен новый командлет Remove-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d29f3-952">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="d29f3-953">Добавлен новый командлет Update-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="d29f3-953">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="d29f3-954">Добавлен новый необязательный параметр [-GatewayId] в командлет Get-AzApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="d29f3-954">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d29f3-955">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-955">Az.CognitiveServices</span></span>
* <span data-ttu-id="d29f3-956">Задано явное использование действия "Отклонить" в качестве действия NetworkRules по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d29f3-956">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d29f3-957">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d29f3-957">Az.FrontDoor</span></span>
* <span data-ttu-id="d29f3-958">Исправлена проблема, связанная с возникновением исключения при попытке Enum.Parse привести значение NULL к значениям перечисления Enabled или Disabled (№ 12344).</span><span class="sxs-lookup"><span data-stu-id="d29f3-958">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d29f3-959">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d29f3-959">Az.HDInsight</span></span>
* <span data-ttu-id="d29f3-960">Добавлена поддержка создания кластера с функцией шифрования передаваемых данных.</span><span class="sxs-lookup"><span data-stu-id="d29f3-960">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="d29f3-961">Добавлен новый параметр EncryptionInTransit в командлет New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="d29f3-961">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="d29f3-962">Добавлен новый параметр EncryptionInTransit в командлет New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="d29f3-962">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="d29f3-963">Добавлена поддержка создания кластера с функцией приватного канала:</span><span class="sxs-lookup"><span data-stu-id="d29f3-963">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="d29f3-964">Добавлен новый параметр PublicNetworkAccessType и OutboundPublicNetworkAccessType в командлет New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="d29f3-964">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="d29f3-965">Добавлен новый параметр PublicNetworkAccessType и OutboundPublicNetworkAccessType в командлет New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="d29f3-965">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="d29f3-966">Реализовано возвращение сведений о виртуальной сети при вызове New-AzHDInsightCluster или Get-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="d29f3-966">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d29f3-967">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d29f3-967">Az.Network</span></span>
* <span data-ttu-id="d29f3-968">Включена поддержка параметра AddressPrefixType в Remove-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="d29f3-968">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="d29f3-969">Реализованы некритические изменения: функциональность PeerAddressType для частного пиринга в Remove-AzExpressRouteCircutPeeringConfig.</span><span class="sxs-lookup"><span data-stu-id="d29f3-969">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="d29f3-970">Код изменен для игнорирования регистра в параметрах AddressPrefixType и PeerAddressType.</span><span class="sxs-lookup"><span data-stu-id="d29f3-970">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="d29f3-971">Изменено сообщение с предупреждением для New-AzLoadBalancerFrontendIpConfig, New-AzPublicIpAddress и New-AzPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="d29f3-971">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d29f3-972">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d29f3-972">Az.OperationalInsights</span></span>
* <span data-ttu-id="d29f3-973">Добавлен параметр -ForceDelete для Remove-AzOperationalInsightsworkspace.</span><span class="sxs-lookup"><span data-stu-id="d29f3-973">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="d29f3-974">Добавлен новый командлет Get-AzOperationalInsightsDeletedWorkspace.</span><span class="sxs-lookup"><span data-stu-id="d29f3-974">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="d29f3-975">Добавлен новый командлет Restore-AzOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="d29f3-975">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d29f3-976">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-976">Az.RecoveryServices</span></span>
* <span data-ttu-id="d29f3-977">Улучшена работа с обнаружением контейнеров и элементов Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="d29f3-977">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d29f3-978">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-978">Az.Resources</span></span>
* <span data-ttu-id="d29f3-979">Добавлены свойства Condition, ConditionVersion и Description в New-AzRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="d29f3-979">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="d29f3-980">Это касается всех соответствующих изменений моделей данных.</span><span class="sxs-lookup"><span data-stu-id="d29f3-980">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="d29f3-981">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-981">Az.Sql</span></span>
* <span data-ttu-id="d29f3-982">Исправлена ошибка, связанная с потенциальным игнорированием регистра имени сервера в New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="d29f3-982">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="d29f3-983">Исправлена ошибка, из-за которой возвращалось неправильное имя существующей базы данных в New-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="d29f3-983">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d29f3-984">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d29f3-984">Az.Storage</span></span>
* <span data-ttu-id="d29f3-985">Добавлена поддержка создания маркера SAS контейнера и BLOB-объекта с новым разрешением x,t.</span><span class="sxs-lookup"><span data-stu-id="d29f3-985">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="d29f3-986">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="d29f3-986">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="d29f3-987">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="d29f3-987">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="d29f3-988">Добавлена поддержка создания маркера SAS учетной записи с новым разрешением x,t,f.</span><span class="sxs-lookup"><span data-stu-id="d29f3-988">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="d29f3-989">New-AzStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="d29f3-989">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="d29f3-990">Добавлена поддержка получения данных об использовании одной общей папки.</span><span class="sxs-lookup"><span data-stu-id="d29f3-990">Supported get single file share usage</span></span>
    - <span data-ttu-id="d29f3-991">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="d29f3-991">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="d29f3-992">4.4.0 — июль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-992">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d29f3-993">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d29f3-993">Az.Accounts</span></span>
* <span data-ttu-id="d29f3-994">Добавлен новый командлет Invoke-AzRestMethod.</span><span class="sxs-lookup"><span data-stu-id="d29f3-994">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="d29f3-995">Устранена неполадка, из-за которой могли возникать ошибки с проверкой подлинности в сценариях с несколькими процессами, такими как выполнение нескольких командлетов Azure PowerShell с помощью Start-Job [№ 9448].</span><span class="sxs-lookup"><span data-stu-id="d29f3-995">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="d29f3-996">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="d29f3-996">Az.Aks</span></span>
* <span data-ttu-id="d29f3-997">Исправлена ошибка, из-за которой Get-AzAks выводит не все кластеры [ №12296].</span><span class="sxs-lookup"><span data-stu-id="d29f3-997">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d29f3-998">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-998">Az.AnalysisServices</span></span>
* <span data-ttu-id="d29f3-999">Удалена ссылка на проект для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="d29f3-999">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d29f3-1000">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d29f3-1000">Az.Automation</span></span>
* <span data-ttu-id="d29f3-1001">Исправлена ошибка, из-за которой строка с escape-символами не преобразовывалась в объект JSON.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1001">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d29f3-1002">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-1002">Az.Compute</span></span>
* <span data-ttu-id="d29f3-1003">Добавлено предупреждение, которое отображается при использовании New-AzVmss, если версия образа не является последней.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1003">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d29f3-1004">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d29f3-1004">Az.DataFactory</span></span>
* <span data-ttu-id="d29f3-1005">Добавлены глобальные параметры в Фабрику данных.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1005">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d29f3-1006">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d29f3-1006">Az.EventGrid</span></span>
* <span data-ttu-id="d29f3-1007">Обновлен модуль для использования API версии 2020-06-01.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1007">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="d29f3-1008">Добавлены новые возможности:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1008">Added new features:</span></span>
    - <span data-ttu-id="d29f3-1009">сопоставление входных данных;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1009">Input mapping</span></span>
    - <span data-ttu-id="d29f3-1010">схема доставки событий;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1010">Event Delivery Schema</span></span>
    - <span data-ttu-id="d29f3-1011">Приватный канал</span><span class="sxs-lookup"><span data-stu-id="d29f3-1011">Private Link</span></span>
    - <span data-ttu-id="d29f3-1012">схема событий облака (версия 1.0);</span><span class="sxs-lookup"><span data-stu-id="d29f3-1012">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="d29f3-1013">раздел служебной шины как назначение;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1013">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="d29f3-1014">функция Azure как назначение;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1014">Azure Function As Destination</span></span>
    - <span data-ttu-id="d29f3-1015">пакетная обработка данных веб-перехватчика;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1015">WebHook Batching</span></span>
    - <span data-ttu-id="d29f3-1016">безопасный веб-перехватчик (поддержка AAD);</span><span class="sxs-lookup"><span data-stu-id="d29f3-1016">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="d29f3-1017">фильтрация IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1017">IpFiltering</span></span>
* <span data-ttu-id="d29f3-1018">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1018">Updated cmdlets:</span></span>
    - <span data-ttu-id="d29f3-1019">New-AzEventGridSubscription или Update-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1019">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="d29f3-1020">Добавлены новые необязательные параметры для поддержки пакетной обработки данных веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1020">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="d29f3-1021">Добавлены новые необязательные параметры для поддержки безопасного веб-перехватчика с использованием AAD.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1021">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="d29f3-1022">Добавлено новое перечисление для параметра EndpointType, чтобы обеспечить поддержку функции Azure и раздела служебной шины в качестве назначения.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1022">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="d29f3-1023">Добавлен новый необязательный параметр для схемы доставки.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1023">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="d29f3-1024">New-AzEventGridTopic или Update-AzEventGridTopic и New-AzEventGridDomain или Update-AzEventGridDomain:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1024">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="d29f3-1025">Добавлены новые необязательные параметры для поддержки фильтрации IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1025">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="d29f3-1026">New-AzEventGridTopic или New-AzEventGridDomain:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1026">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="d29f3-1027">Добавлены новые необязательные параметры для поддержки сопоставления входных данных.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1027">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d29f3-1028">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d29f3-1028">Az.FrontDoor</span></span>
* <span data-ttu-id="d29f3-1029">Обновлен модуль для использования API версии 2020-05-01.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1029">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="d29f3-1030">Включена поддержка Приватного канала для ресурсов службы хранилища, Key Vault и службы веб-приложений.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1030">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d29f3-1031">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d29f3-1031">Az.HDInsight</span></span>
* <span data-ttu-id="d29f3-1032">Включена поддержка создания кластера с хранилищем ADLS 1-го и 2-го поколения в национальных облаках.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1032">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d29f3-1033">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d29f3-1033">Az.Monitor</span></span>
* <span data-ttu-id="d29f3-1034">Исправлена ошибка с Get-AzDiagnosticSetting, связанная с присвоением значения NULL метрикам или журналам [№ 12272].</span><span class="sxs-lookup"><span data-stu-id="d29f3-1034">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d29f3-1035">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d29f3-1035">Az.Network</span></span>
* <span data-ttu-id="d29f3-1036">Исправлены ошибки с переключением параметров для подключения виртуальной сети концентратора к глобальной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1036">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="d29f3-1037">Добавлены новые командлеты для сайтов сетевых виртуальных модулей Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1037">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="d29f3-1038">Get-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="d29f3-1038">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="d29f3-1039">New-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="d29f3-1039">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="d29f3-1040">Remove-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="d29f3-1040">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="d29f3-1041">Update-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="d29f3-1041">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="d29f3-1042">New-AzOffice365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="d29f3-1042">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="d29f3-1043">Добавлены новые командлеты для сетевого виртуального модуля Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1043">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="d29f3-1044">Get-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="d29f3-1044">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="d29f3-1045">New-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="d29f3-1045">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="d29f3-1046">Remove-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="d29f3-1046">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="d29f3-1047">Update-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="d29f3-1047">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="d29f3-1048">Get-AzNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="d29f3-1048">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="d29f3-1049">New-AzVirtualApplianceSkuProperty</span><span class="sxs-lookup"><span data-stu-id="d29f3-1049">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="d29f3-1050">Общие командлеты для Шлюза приложений, подключенного к Приватному каналу.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1050">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="d29f3-1051">Общие командлеты для службы синхронизации хранилища, подключенной к Приватному каналу.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1051">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="d29f3-1052">Общие командлеты для службы SignalR, подключенной к Приватному каналу.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1052">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d29f3-1053">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-1053">Az.RecoveryServices</span></span>
* <span data-ttu-id="d29f3-1054">Удалена ссылка на проект для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1054">Removed project reference to Authentication</span></span>
* <span data-ttu-id="d29f3-1055">В Azure Backup представлена более точная справка по командлетам.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1055">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="d29f3-1056">В Azure Backup включена поддержка выборки заданий агента MAB с помощью командлета Get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1056">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d29f3-1057">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-1057">Az.Resources</span></span>
* <span data-ttu-id="d29f3-1058">Обновлен командлет Save-AzResourceGroupDeploymentTemplate для использования пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1058">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="d29f3-1059">Добавлен командлет Unregister-AzResourceProvider.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1059">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="d29f3-1060">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-1060">Az.Sql</span></span>
* <span data-ttu-id="d29f3-1061">Включена поддержка субъекта-службы и гостевых пользователей для командлета Set-AzSqlInstanceActiveDirectoryAdministrator.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1061">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="d29f3-1062">Исправлена ошибка в командлетах классификации данных.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1062">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="d29f3-1063">Включена поддержка отработки отказа Управляемого экземпляра SQL Azure. Invoke-AzSqlInstanceFailover</span><span class="sxs-lookup"><span data-stu-id="d29f3-1063">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d29f3-1064">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d29f3-1064">Az.Storage</span></span>
* <span data-ttu-id="d29f3-1065">Исправлена ошибка, из-за которой в некоторых командлетах плоскости данных не добавлялся объект UserAgent.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1065">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="d29f3-1066">Включена поддержка создания и обновления учетной записи хранения с использованием MinimumTlsVersion и AllowBlobPublicAccess.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1066">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="d29f3-1067">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d29f3-1067">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="d29f3-1068">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d29f3-1068">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="d29f3-1069">Включена поддержка включения и отключения управления версиями в службе BLOB-объектов учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1069">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="d29f3-1070">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d29f3-1070">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="d29f3-1071">Включена поддержка вывода списка BLOB-объектов с данными о версиях BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1071">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="d29f3-1072">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="d29f3-1072">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="d29f3-1073">Включена поддержка получения или удаления одного моментального снимка BLOB-объекта или версии BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1073">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="d29f3-1074">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="d29f3-1074">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="d29f3-1075">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="d29f3-1075">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="d29f3-1076">Включена поддержка конвейера на основе BLOB-объекта, созданного с помощью Azure.Storage.Blobs версии 12.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1076">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="d29f3-1077">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d29f3-1077">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="d29f3-1078">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="d29f3-1078">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="d29f3-1079">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="d29f3-1079">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="d29f3-1080">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d29f3-1080">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="d29f3-1081">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="d29f3-1081">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="d29f3-1082">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="d29f3-1082">Az.StorageSync</span></span>
* <span data-ttu-id="d29f3-1083">Добавлена новая версия пакета SDK StorageSync, предназначенная для API версии 2020-03-01.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1083">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="d29f3-1084">Добавлен командлет для обновления службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1084">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="d29f3-1085">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="d29f3-1085">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="d29f3-1086">Добавлены классы IncomingTrafficPolicy и IncomingTrafficPolicy в командлеты службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1086">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d29f3-1087">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d29f3-1087">Az.Websites</span></span>
* <span data-ttu-id="d29f3-1088">Включена поддержка выполнения операций для слотов, которые находятся не в той же группе ресурсов, что и план службы приложений.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1088">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="d29f3-1089">4.3.0 — июнь 2020 года</span><span class="sxs-lookup"><span data-stu-id="d29f3-1089">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d29f3-1090">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d29f3-1090">Az.Accounts</span></span>
* <span data-ttu-id="d29f3-1091">Включена поддержка обнаружения параметров среды по умолчанию и добавления окружения с помощью командлета Add-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1091">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="d29f3-1092">Обновлены предварительно загруженные сборки [№ 12024], [№ 11976].</span><span class="sxs-lookup"><span data-stu-id="d29f3-1092">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="d29f3-1093">Обновлена сборка Azure.Core.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1093">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="d29f3-1094">Исправлена ошибка, из-за которой выполнение Connect-AzAccount может завершаться сбоем при многопоточном выполнении [№ 11201].</span><span class="sxs-lookup"><span data-stu-id="d29f3-1094">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="d29f3-1095">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="d29f3-1095">Az.Aks</span></span>
* <span data-ttu-id="d29f3-1096">Заменено использование старого [API AccessProfile](/rest/api/aks/managedclusters/getaccessprofile) вызовами API [ListClusterAdmin](/rest/api/aks/managedclusters/listclusteradmincredentials) и [ListClusterUser](/rest/api/aks/managedclusters/listclusterusercredentials).</span><span class="sxs-lookup"><span data-stu-id="d29f3-1096">Replaced usage of old [AccessProfile API](/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d29f3-1097">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d29f3-1097">Az.Batch</span></span>
* <span data-ttu-id="d29f3-1098">Изменена версия SDK для Microsoft.Azure.Management.Batch для Az.Batch на 11.0.0.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1098">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="d29f3-1099">Включена возможность задать удостоверение BatchAccount в командлете New-AzBatchAccount.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1099">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d29f3-1100">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-1100">Az.CognitiveServices</span></span>
* <span data-ttu-id="d29f3-1101">Включена поддержка отображения возможностей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1101">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="d29f3-1102">Включена поддержка изменения PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1102">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d29f3-1103">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-1103">Az.Compute</span></span>
* <span data-ttu-id="d29f3-1104">Добавлен параметр SimulateEviction в командлеты Set-AzVM и Set-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1104">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="d29f3-1105">Добавлен фрагмент Premium_LRS в средство заполнения аргументов параметра StorageAccountType для командлета New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1105">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="d29f3-1106">Добавлены подсостояния для VMCustomScriptExtension [№ 11297].</span><span class="sxs-lookup"><span data-stu-id="d29f3-1106">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="d29f3-1107">Добавлен фрагмент Delete в средство заполнения аргументов параметра EvictionPolicy для командлетов New-AzVM и New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1107">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="d29f3-1108">Исправлено имя нового расширения виртуальной машины для SAP.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1108">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d29f3-1109">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d29f3-1109">Az.DataFactory</span></span>
* <span data-ttu-id="d29f3-1110">Обновлен пакет SDK ADF для .NET до версии 4.9.0.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1110">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d29f3-1111">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d29f3-1111">Az.EventHub</span></span>
* <span data-ttu-id="d29f3-1112">Добавлены параметры управляемого удостоверения для командлетов New-AzEventHubNamespace и Set-AzEventHubNamespace.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1112">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="d29f3-1113">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="d29f3-1113">Az.Functions</span></span>
* <span data-ttu-id="d29f3-1114">Включена поддержка создания приложений-функций PowerShell 7.0 и Java 11.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1114">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d29f3-1115">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d29f3-1115">Az.HDInsight</span></span>
* <span data-ttu-id="d29f3-1116">Включена поддержка перечисления узлов и перезагрузка отдельных узлов кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1116">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="d29f3-1117">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="d29f3-1117">Az.HealthcareApis</span></span>
* <span data-ttu-id="d29f3-1118">Обновлен пакет SDK до версии 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1118">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="d29f3-1119">Включена поддержка параметров экспорта и управляемого удостоверения.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1119">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d29f3-1120">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d29f3-1120">Az.Monitor</span></span>
* <span data-ttu-id="d29f3-1121">Исправлен входной параметр объекта для Set-AzActivityLogAlert.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1121">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="d29f3-1122">Исправлен параметр InputObject для Set-AzActionGroup [№ 10868].</span><span class="sxs-lookup"><span data-stu-id="d29f3-1122">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d29f3-1123">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d29f3-1123">Az.Network</span></span>
* <span data-ttu-id="d29f3-1124">Включена поддержка параметра AddressPrefixType в Remove-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1124">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="d29f3-1125">Добавлены новые командлеты для политики Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1125">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="d29f3-1126">New-AzFirewallPolicyDnsSetting</span><span class="sxs-lookup"><span data-stu-id="d29f3-1126">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="d29f3-1127">Включена поддержка полного доменного имени назначения в правилах сети для политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1127">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="d29f3-1128">Включена поддержка операций серверного пула адресов:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1128">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="d29f3-1129">New-AzLoadBalancerBackendAddressConfig</span><span class="sxs-lookup"><span data-stu-id="d29f3-1129">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="d29f3-1130">New-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d29f3-1130">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="d29f3-1131">Set-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d29f3-1131">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="d29f3-1132">Remove-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d29f3-1132">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="d29f3-1133">Get-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d29f3-1133">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="d29f3-1134">Добавлена проверка имени для New-AzIpGroup.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1134">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="d29f3-1135">Добавлены новые командлеты для политики Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1135">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="d29f3-1136">New-AzFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="d29f3-1136">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="d29f3-1137">Обновлены следующие команды для функции: Включена возможность настройки и удаления пользовательских DNS-серверов в шлюзе VPN P2S виртуальной глобальной сети.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1137">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="d29f3-1138">Обновлен командлет New-AzP2sVpnGateway: добавлен необязательный параметр -CustomDnsServer, чтобы пользователи могли указывать свои DNS-серверы для настройки в шлюзе VPN P2S для использования клиентами с подключением "точка — сеть".</span><span class="sxs-lookup"><span data-stu-id="d29f3-1138">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="d29f3-1139">Обновлен командлет Update-AzP2sVpnGateway: добавлен необязательный параметр -CustomDnsServer, чтобы пользователи могли указывать свои DNS-серверы для настройки в шлюзе VPN P2S для использования клиентами с подключением "точка — сеть".</span><span class="sxs-lookup"><span data-stu-id="d29f3-1139">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="d29f3-1140">Обновлен командлет Update-AzVpnGateway:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1140">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="d29f3-1141">добавлен необязательный параметр -BgpPeeringAddress, чтобы клиенты могли указывать пользовательские маршруты BGP для настройки в шлюзе VPN.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1141">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="d29f3-1142">Добавлен новый командлет для сброса состояния маршрутизации ресурса VirtualHub:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1142">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="d29f3-1143">Reset-AzHubRouter</span><span class="sxs-lookup"><span data-stu-id="d29f3-1143">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="d29f3-1144">Следующие обновления основаны на последнем изменении Swagger для политики брандмауэра:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1144">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="d29f3-1145">изменены имена для RuleGroup, RuleCollectionGroup и RuleType;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1145">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="d29f3-1146">включена поддержка коллекций правил NAT политики брандмауэра для поддержки нескольких коллекций правил NAT.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1146">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="d29f3-1147">[Критическое изменение] Добавлен обязательный параметр SourceIpGroup для командлетов New-AzFirewallPolicyApplicationRule и New-AzFirewallPolicyNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1147">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="d29f3-1148">[Критическое изменение] Параметр SourceAddress для командлета New-AzFirewallPolicyApplicationRule сделан обязательным.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1148">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="d29f3-1149">[Критическое изменение] Параметр SourceAddress для командлета New-AzFirewallPolicyApplicationRule сделан обязательным.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1149">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="d29f3-1150">[Критическое изменение] Удалены обязательные параметры: TranslatedAddress и TranslatedPort для командлета New-AzFirewallPolicyNatRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1150">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="d29f3-1151">Добавлены новые командлеты для поддержки Приватного канала в Шлюзе приложений:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1151">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="d29f3-1152">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d29f3-1152">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="d29f3-1153">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d29f3-1153">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="d29f3-1154">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d29f3-1154">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="d29f3-1155">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d29f3-1155">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="d29f3-1156">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d29f3-1156">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="d29f3-1157">New-AzApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d29f3-1157">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="d29f3-1158">Добавлены новые командлеты для дочернего ресурса HubRouteTables VirtualHub:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1158">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="d29f3-1159">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="d29f3-1159">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="d29f3-1160">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="d29f3-1160">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="d29f3-1161">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="d29f3-1161">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="d29f3-1162">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="d29f3-1162">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="d29f3-1163">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="d29f3-1163">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="d29f3-1164">Обновлены существующие командлеты для включения поддержки необязательного входного параметра RoutingConfiguration для настраиваемой маршрутизации в виртуальной глобальной сети.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1164">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="d29f3-1165">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="d29f3-1165">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="d29f3-1166">Set-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="d29f3-1166">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="d29f3-1167">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="d29f3-1167">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="d29f3-1168">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="d29f3-1168">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="d29f3-1169">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="d29f3-1169">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="d29f3-1170">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="d29f3-1170">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="d29f3-1171">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="d29f3-1171">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="d29f3-1172">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="d29f3-1172">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d29f3-1173">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d29f3-1173">Az.OperationalInsights</span></span>
* <span data-ttu-id="d29f3-1174">Исправлена ошибка, из-за которой PSWorkspace не реализует IOperationalInsightsWorkspace [№ 12135].</span><span class="sxs-lookup"><span data-stu-id="d29f3-1174">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="d29f3-1175">Добавлено значение pergb2018 в действительный набор значений параметра Sku в командлете Set-AzOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1175">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="d29f3-1176">Добавлен псевдоним FunctionParameters для параметра FunctionParameter:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1176">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="d29f3-1177">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="d29f3-1177">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="d29f3-1178">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="d29f3-1178">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d29f3-1179">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-1179">Az.RecoveryServices</span></span>
* <span data-ttu-id="d29f3-1180">Включена поддержка выборки элементов MAB в Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1180">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="d29f3-1181">Включена поддержка типа диска StandardSSD_LRS в Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1181">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="d29f3-1182">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-1182">Az.Resources</span></span>
* <span data-ttu-id="d29f3-1183">Добавлены параметры UsageLocation, GivenName, Surname, AccountEnabled, MailNickname, Mail для PSADUser [№ 10526], [№ 10497].</span><span class="sxs-lookup"><span data-stu-id="d29f3-1183">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="d29f3-1184">Исправлена ошибка, из-за которой параметр -Mail не работает в командлете Get-AzADUser [№ 11981].</span><span class="sxs-lookup"><span data-stu-id="d29f3-1184">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="d29f3-1185">Добавлен параметр -ExcludeChangeType в командлеты Get-AzDeploymentWhatIfResult и Get-AzResourceGroupDeploymentWhatIfResult.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1185">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="d29f3-1186">Добавлен параметр -WhatIfExcludeChangeType в командлеты New-AzDeployment и New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1186">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="d29f3-1187">Обновлены командлеты Test-Az\*Deployment для отображения улучшенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1187">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="d29f3-1188">Исправлено справочное сообщение для параметра -Name в командлетах создания развертывания и командлетах What-If.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1188">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="d29f3-1189">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-1189">Az.Sql</span></span>
* <span data-ttu-id="d29f3-1190">Включена поддержка субъекта-службы для командлета настройки администратора Azure Active Directory SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1190">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="d29f3-1191">Исправлена ошибка синхронизации в командлетах классификации данных.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1191">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="d29f3-1192">Включена поддержка поиска пользователей по адресу электронной почты в командлете Set-AzSqlServerActiveDirectoryAdministrator [№ 12192].</span><span class="sxs-lookup"><span data-stu-id="d29f3-1192">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d29f3-1193">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d29f3-1193">Az.Storage</span></span>
* <span data-ttu-id="d29f3-1194">Включена поддержка создания учетной записи хранения с помощью RequireInfrastructureEncryption.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1194">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="d29f3-1195">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d29f3-1195">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="d29f3-1196">Перемещена логика загрузки Azure.Core в Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1196">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d29f3-1197">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d29f3-1197">Az.Websites</span></span>
* <span data-ttu-id="d29f3-1198">В командлет Restore-AzDeletedWebApp добавлена защитная мера при удалении созданного веб-приложения, если восстановление завершилось сбоем.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1198">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="d29f3-1199">Добавлены параметры SourceWebApp.Location для командлетов New-AzWebApp и New-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1199">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="d29f3-1200">Исправлена ошибка, препятствующая изменению параметров контейнера в командлетах Set-AzWebApp и Set-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1200">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="d29f3-1201">Исправлена ошибка получения SiteConfig, когда параметр -Name не указан для командлета Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1201">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="d29f3-1202">Включена поддержка создания приложений ASP для Linux.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1202">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="d29f3-1203">Добавлены исключения для клонирования в группах ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1203">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="d29f3-1204">4.2.0 — июнь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1204">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d29f3-1205">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d29f3-1205">Az.Accounts</span></span>
* <span data-ttu-id="d29f3-1206">Исправлена проблема, из-за которой модуль Az мог пропускать журналы в заданиях службы автоматизации или PowerShell [№ 11492].</span><span class="sxs-lookup"><span data-stu-id="d29f3-1206">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d29f3-1207">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-1207">Az.AnalysisServices</span></span>
* <span data-ttu-id="d29f3-1208">Обновлена версия сборки командлетов плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1208">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d29f3-1209">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d29f3-1209">Az.ApiManagement</span></span>
* <span data-ttu-id="d29f3-1210">Обновлена версия сборки командлетов управления службами.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1210">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="d29f3-1211">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="d29f3-1211">Az.Billing</span></span>
* <span data-ttu-id="d29f3-1212">Обновлена версия сборки командлетов потребления.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1212">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d29f3-1213">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-1213">Az.CognitiveServices</span></span>
* <span data-ttu-id="d29f3-1214">Реализована поддержка элементов управления PrivateEndpoint и PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1214">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="d29f3-1215">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d29f3-1215">Az.DataFactory</span></span>
* <span data-ttu-id="d29f3-1216">Обновлена версия сборки командлетов фабрики данных версии 2.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1216">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="d29f3-1217">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="d29f3-1217">Az.DataShare</span></span>
* <span data-ttu-id="d29f3-1218">Вышла общедоступная версия модуля Az.DataShare.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1218">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="d29f3-1219">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="d29f3-1219">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="d29f3-1220">Вышла общедоступная версия модуля Az.DesktopVirtualization.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1220">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d29f3-1221">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d29f3-1221">Az.OperationalInsights</span></span>
* <span data-ttu-id="d29f3-1222">Пакет SDK обновлен до версии 0.21.0.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1222">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="d29f3-1223">Добавлены дополнительные параметры в следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1223">Added optional parameters to</span></span> 
    - <span data-ttu-id="d29f3-1224">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="d29f3-1224">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="d29f3-1225">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="d29f3-1225">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d29f3-1226">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d29f3-1226">Az.PolicyInsights</span></span>
* <span data-ttu-id="d29f3-1227">Исправлен пример 3 для командлета Start-AzPolicyComplianceScan.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1227">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="d29f3-1228">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="d29f3-1228">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="d29f3-1229">Обновлена версия сборки командлетов PowerBI.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1229">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="d29f3-1230">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="d29f3-1230">Az.PrivateDns</span></span>
* <span data-ttu-id="d29f3-1231">Исправлено форматирование строки с подробными выходными данными командлета Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1231">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d29f3-1232">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-1232">Az.RecoveryServices</span></span>
* <span data-ttu-id="d29f3-1233">Реализована поддержка Azure Site Recovery для создания плана восстановления и репликации между зонами из входного XML-файла.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1233">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="d29f3-1234">Обновлена версия сборки командлетов SiteRecovery и Backup.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1234">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="d29f3-1235">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-1235">Az.Resources</span></span>
* <span data-ttu-id="d29f3-1236">Добавлен параметр Tail в командлеты Get-AzDeploymentScriptLog и Save-AzDeploymentScriptLog.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1236">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="d29f3-1237">Отформатировано свойство Output и включено в отображаемые выходные данные командлета Get-AzDeploymentScript.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1237">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="d29f3-1238">Параметр -DeploymentScriptInputObject переименован в -DeploymentScriptObject.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1238">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="d29f3-1239">Исправлена ошибка с отсутствующими именами файлов или целевых объектов в сообщениях командлетов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1239">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="d29f3-1240">Обновлена версия сборки командлетов диспетчера ресурсов и обработчика тегов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1240">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="d29f3-1241">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-1241">Az.Sql</span></span>
* <span data-ttu-id="d29f3-1242">Добавлен параметр UsePrivateLinkConnection в командлеты New-AzSqlSyncGroup, Update-AzSqlSyncGroup, New-AzSqlSyncMember и Update-AzSqlSyncMember.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1242">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="d29f3-1243">Добавлен параметр SyncMemberAzureDatabaseResourceId в командлеты New-AzSqlSyncMember и Update-AzSqlSyncMember.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1243">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="d29f3-1244">Реализована поддержка поиска гостевых пользователей в командлете для настройки администратора Active Directory в SQL Server Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1244">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d29f3-1245">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d29f3-1245">Az.Storage</span></span>
* <span data-ttu-id="d29f3-1246">Обновлена версия сборки командлетов плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1246">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="d29f3-1247">4.1.0 — май 2020 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1247">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="d29f3-1248">Основные сведения о новых возможностях с момента последнего выпуска</span><span class="sxs-lookup"><span data-stu-id="d29f3-1248">Highlights since the last release</span></span>
* <span data-ttu-id="d29f3-1249">Поддерживаемые версии PowerShell: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="d29f3-1249">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="d29f3-1250">Вышла общедоступная версия модуля Az.Functions.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1250">General availability of Az.Functions</span></span> 
* <span data-ttu-id="d29f3-1251">Состоялся основной выпуск Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources и Az.Storage.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1251">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d29f3-1252">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d29f3-1252">Az.Accounts</span></span>
* <span data-ttu-id="d29f3-1253">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметры AzureSynapseAnalyticsEndpointResourceId и AzureSynapseAnalyticsEndpointSuffix.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1253">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="d29f3-1254">В Az.Accounts добавлены сборки, связанные с Azure.Core. Добавлена поддержка Windows PowerShell 5.1, PowerShell Core 6.2.4 и PowerShell 7+.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1254">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="d29f3-1255">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="d29f3-1255">Az.Aks</span></span>
* <span data-ttu-id="d29f3-1256">Версия API обновлена до 2019-10-01.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1256">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="d29f3-1257">Добавлена возможность создания контейнера Windows в службе Azure Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1257">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="d29f3-1258">Добавлены новые командлеты: New-AzAksNodePool, Update-AzAksNodePool, Remove-AzAksNodePool, Get-AzAksNodePool, Install-AzAksKubectl, Get-AzAksVersion.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1258">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d29f3-1259">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d29f3-1259">Az.ApiManagement</span></span>
* <span data-ttu-id="d29f3-1260">В New-AzApiManagement и Set-AzApiManagement параметр -AssignIdentity переименован в -SystemAssignedIdentity.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1260">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="d29f3-1261">В New-AzApiManagement и Set-AzApiManagement добавлен новый параметр -UserAssignedIdentity <строка[]>.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1261">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="d29f3-1262">Командлет Get-AzApiManagementProperty переименован в Get-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1262">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="d29f3-1263">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1263">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="d29f3-1264">Командлет New-AzApiManagementProperty переименован в New-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1264">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="d29f3-1265">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1265">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="d29f3-1266">Командлет Set-AzApiManagementProperty переименован в Set-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1266">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="d29f3-1267">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1267">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="d29f3-1268">Командлет Remove-AzApiManagementProperty переименован в Remove-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1268">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="d29f3-1269">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1269">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="d29f3-1270">Добавлен новый командлет Get-AzApiManagementAuthorizationServerClientSecret, а Get-AzApiManagementAuthorizationServer теперь не возвращает секрет клиента.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1270">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="d29f3-1271">Добавлен новый командлет Get-AzApiManagementNamedValueSecretValue, а Get-AzApiManagementNamedValue теперь не возвращает значение секрета.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1271">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="d29f3-1272">Добавлен новый командлет Get-AzApiManagementOpenIdConnectProviderClientSecret, а Get-AzApiManagementOpenIdConnectProvider теперь не возвращает секрет клиента.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1272">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="d29f3-1273">Добавлен новый командлет Get-AzApiManagementSubscriptionKey, а Get-AzApiManagementSubscription теперь не возвращает ключи подписки.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1273">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="d29f3-1274">Добавлен новый командлет Get-AzApiManagementTenantAccessSecret, а Get-AzApiManagementTenantAccess теперь не возвращает ключи.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1274">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="d29f3-1275">Добавлен новый командлет Get-AzApiManagementTenantGitAccessSecret, а Get-AzApiManagementTenantGitAccess теперь не возвращает ключи.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1275">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="d29f3-1276">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="d29f3-1276">Az.ApplicationInsights</span></span>
* <span data-ttu-id="d29f3-1277">В New-AzApplicationInsights добавлены параметры RetentionInDays, PublicNetworkAccessForIngestion и PublicNetworkAccessForQuery.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1277">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="d29f3-1278">Создан командлет Update-AzApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1278">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="d29f3-1279">Созданы командлеты для связанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1279">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d29f3-1280">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d29f3-1280">Az.Batch</span></span>
* <span data-ttu-id="d29f3-1281">В командлеты Az.Batch добавлена поддержка пакетов SDK Microsoft.Azure.Batch версии 13.0.0 и SDK Microsoft.Azure.Management.Batch версии 9.0.0.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1281">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="d29f3-1282">Теперь в New-AzBatchCertificate можно выбрать тип добавляемого сертификата с помощью нового параметра -CertificateKind.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1282">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="d29f3-1283">В PSApplication удалено свойство ApplicationPackages.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1283">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="d29f3-1284">Отдельные пакеты в приложении теперь можно извлечь с помощью Get-AzBatchApplicationPackage.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1284">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="d29f3-1285">Пример: Get-AzBatchApplication -AccountName моя_учетная_запись -ResourceGroupName моя_группа_ресурсов -ApplicationId мое_приложение.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1285">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="d29f3-1286">При создании пула с помощью New-AzBatchPool свойство VirtualMachineImageId элемента PSImageReference теперь может ссылаться только на образ из Общей коллекции образов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1286">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="d29f3-1287">При создании пула с помощью New-AzBatchPool пул можно подготовить без общедоступного IP-адреса, используя новое свойство PublicIPAddressConfiguration элемента PSNetworkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1287">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="d29f3-1288">Свойство PublicIPs элемента PSNetworkConfiguration было передано элементу PSPublicIPAddressConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1288">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="d29f3-1289">Это свойство можно указать, только если параметру IPAddressProvisioningType присвоено значение UserManaged.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1289">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d29f3-1290">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-1290">Az.Compute</span></span>
* <span data-ttu-id="d29f3-1291">В командлет Update-AzVM добавлен параметр HostId.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1291">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="d29f3-1292">Обновлена справочная документация по командлетам New-AzVMConfig, New-AzVmssConfig, Update-AzVmss, Set-AzVMOperatingSystem и Set-AzVmssOsProfile.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1292">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="d29f3-1293">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="d29f3-1293">Breaking changes</span></span>
    - <span data-ttu-id="d29f3-1294">Параметр FilterExpression удален из командлета Get-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1294">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="d29f3-1295">Параметр AssignIdentity удален из командлетов New-AzVmssConfig, New-AzVMConfig и Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1295">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="d29f3-1296">Параметр AutomaticRepairMaxInstanceRepairsPercent удален из командлетов New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1296">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="d29f3-1297">Свойства AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus и VirtualMachineScaleSetsColocationStatus удалены из ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1297">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="d29f3-1298">Свойство MaxInstanceRepairsPercent удалено из AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1298">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="d29f3-1299">Типы AvailabilitySets, VirtualMachines и VirtualMachineScaleSets изменены с IList<SubResource> на IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1299">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="d29f3-1300">Уточнено описание командлета Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1300">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="d29f3-1301">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d29f3-1301">Az.DataFactory</span></span>
* <span data-ttu-id="d29f3-1302">Добавлена поддержка операций CRUD для свойств среды выполнения потока данных в управляемой среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1302">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d29f3-1303">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d29f3-1303">Az.FrontDoor</span></span>
* <span data-ttu-id="d29f3-1304">Добавлены новые командлеты для создания, обновления, извлечения и удаления объекта обработчика правил Front Door.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1304">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="d29f3-1305">Добавлены вспомогательные командлеты для создания объекта обработчика правил Front Door.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1305">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="d29f3-1306">Добавлена ссылка обработчика правил на объект правила маршрутизации Front Door.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1306">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="d29f3-1307">Добавлены параметры Приватного канала на серверный объект Front Door.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1307">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="d29f3-1308">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="d29f3-1308">Az.Functions</span></span>
* <span data-ttu-id="d29f3-1309">Вышла общедоступная версия модуля Az.Functions.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1309">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d29f3-1310">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d29f3-1310">Az.HDInsight</span></span>
* <span data-ttu-id="d29f3-1311">Добавлена поддержка шифрования управляемых клиентом ключей.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1311">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="d29f3-1312">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="d29f3-1312">Az.HealthcareApis</span></span>
* <span data-ttu-id="d29f3-1313">Политики доступа для текущего субъекта теперь не используются по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1313">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d29f3-1314">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d29f3-1314">Az.IotHub</span></span>
* <span data-ttu-id="d29f3-1315">Добавлен командлет для вызова запроса в центре Интернета вещей для получения данных с помощью SQL-подобного языка.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1315">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="d29f3-1316">Устранена проблема, когда с помощью Add-AzIotHubDevice не удавалось создать устройство с поддержкой IoT Edge без дочерних устройств (№ 11597).</span><span class="sxs-lookup"><span data-stu-id="d29f3-1316">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="d29f3-1317">Добавлен командлет для создания маркера SAS для Центра Интернета вещей, устройства или модуля.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1317">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="d29f3-1318">Добавлен командлет для вызова запроса метрик конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1318">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="d29f3-1319">Появилась возможность управлять автоматическим развертыванием IoT Edge в большом масштабе.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1319">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="d29f3-1320">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1320">New cmdlets are:</span></span>
    - <span data-ttu-id="d29f3-1321">Add-AzIotHubDeployment;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1321">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="d29f3-1322">Get-AzIotHubDeployment;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1322">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="d29f3-1323">Remove-AzIotHubDeployment;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1323">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="d29f3-1324">Set-AzIotHubDeployment.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1324">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="d29f3-1325">Добавлен командлет для вызова запроса метрик развертывания IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1325">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="d29f3-1326">Добавлен командлет для применения содержимого конфигурации к указанному пограничному устройству.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1326">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d29f3-1327">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d29f3-1327">Az.KeyVault</span></span>
* <span data-ttu-id="d29f3-1328">Удалены два псевдонима: New-AzKeyVaultCertificateAdministratorDetails и New-AzKeyVaultCertificateOrganizationDetails.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1328">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="d29f3-1329">При создании хранилища ключей обратимое удаление включено по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1329">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="d29f3-1330">Можно задать правила сети, чтобы при создании хранилища ключей управлять доступом из определенных сетевых расположений.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1330">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="d29f3-1331">Добавлена возможность создания собственных ключей (BYOK).</span><span class="sxs-lookup"><span data-stu-id="d29f3-1331">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="d29f3-1332">С помощью Add-AzKeyVaultKey теперь можно создавать ключ обмена ключами.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1332">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="d29f3-1333">С помощью Get-AzKeyVaultKey можно скачать открытый ключ в формате PEM.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1333">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="d29f3-1334">Обновлен раздел KeyOps справочной документации по Add-AzKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1334">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d29f3-1335">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d29f3-1335">Az.Monitor</span></span>
* <span data-ttu-id="d29f3-1336">Исправлена ошибка Set-AzDiagnosticSettings, когда политика хранения не применялась ко всем категориям (№ 11589).</span><span class="sxs-lookup"><span data-stu-id="d29f3-1336">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="d29f3-1337">Добавлена поддержка критериев доступности веб-теста для оповещения метрики версии 2.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1337">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="d29f3-1338">В New-AzMetricAlertRuleV2Criteria добавлена возможность создавать критерии доступности веб-теста.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1338">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="d29f3-1339">Add-AzMetricAlertRuleV2 теперь поддерживает новые критерии доступности веб-теста.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1339">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="d29f3-1340">В PSLogProfile исправлено избыточное определение RetentionPolicy (№ 7608).</span><span class="sxs-lookup"><span data-stu-id="d29f3-1340">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="d29f3-1341">В PSEventData удалены избыточные определения свойств (№ 11353).</span><span class="sxs-lookup"><span data-stu-id="d29f3-1341">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="d29f3-1342">Командлет Get-AzLog переименован в Get-AzActivityLog.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1342">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d29f3-1343">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d29f3-1343">Az.Network</span></span>
* <span data-ttu-id="d29f3-1344">Добавлен атрибут критического изменения, сообщающий о том, что поведение зоны по умолчанию будет изменено.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1344">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="d29f3-1345">New-AzPublicIpAddress;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1345">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="d29f3-1346">New-AzPublicIpPrefix;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1346">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="d29f3-1347">New-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1347">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="d29f3-1348">Добавлена поддержка нового ресурса верхнего уровня SecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1348">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="d29f3-1349">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1349">New cmdlets added:</span></span>
        - <span data-ttu-id="d29f3-1350">New-AzSecurityPartnerProvider;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1350">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="d29f3-1351">Remove-AzSecurityPartnerProvider;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1351">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="d29f3-1352">Get-AzSecurityPartnerProvider;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1352">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="d29f3-1353">Set-AzSecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1353">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="d29f3-1354">В PSPrivateLinkResource добавлен параметр RequiredZoneNames, а в PSPrivateEndpointConnection — GroupId.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1354">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="d29f3-1355">Исправлен неправильный тип параметра SuccessThresholdRoundTripTimeMs для New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1355">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="d29f3-1356">В командлетах VirtualWan аргументу AllowVnetToVnetTraffic теперь по умолчанию присвоено значение True.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1356">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="d29f3-1357">New-AzVirtualWan;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1357">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="d29f3-1358">Update-AzVirtualWan.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1358">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="d29f3-1359">Добавлены новые командлеты для поддержки группы зон DNS для частной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1359">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="d29f3-1360">New-AzPrivateDnsZoneConfig;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1360">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="d29f3-1361">Get-AzPrivateDnsZoneGroup;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1361">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="d29f3-1362">New-AzPrivateDnsZoneGroup;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1362">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="d29f3-1363">Set-AzPrivateDnsZoneGroup;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1363">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="d29f3-1364">Remove-AzPrivateDnsZoneGroup.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1364">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="d29f3-1365">В AzureFirewall добавлены параметры DNSEnableProxy, DNSRequireProxyForNetworkRules и DNSServers.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1365">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="d29f3-1366">В AzureFirewall добавлены параметры EnableDnsProxy, DnsProxyNotRequiredForNetworkRule и DnsServer.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1366">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="d29f3-1367">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1367">Updated cmdlet:</span></span>
        - <span data-ttu-id="d29f3-1368">New-AzFirewall.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1368">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d29f3-1369">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d29f3-1369">Az.OperationalInsights</span></span>
* <span data-ttu-id="d29f3-1370">Обновлен устаревший код для использования новых пакетов SDK.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1370">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="d29f3-1371">Из-за устаревших API-интерфейсов удалены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1371">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="d29f3-1372">Get-AzOperationalInsightsSavedSearchResult (псевдоним Get-AzOperationalInsightsSavedSearchResults);</span><span class="sxs-lookup"><span data-stu-id="d29f3-1372">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="d29f3-1373">Get-AzOperationalInsightsSearchResult (псевдоним Get-AzOperationalInsightsSearchResults);</span><span class="sxs-lookup"><span data-stu-id="d29f3-1373">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="d29f3-1374">Get-AzOperationalInsightsLinkTarget (псевдоним Get-AzOperationalInsightsLinkTargets).</span><span class="sxs-lookup"><span data-stu-id="d29f3-1374">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="d29f3-1375">В Set-AzOperationalInsightsWorkspace и New-AzOperationalInsightsWorkspace добавлены новые параметры.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1375">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="d29f3-1376">Созданы командлеты для связанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1376">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="d29f3-1377">Созданы командлеты для кластеров и связанной службы.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1377">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d29f3-1378">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-1378">Az.RecoveryServices</span></span>
* <span data-ttu-id="d29f3-1379">В Azure Site Recovery добавлена поддержка защиты поставщика Azure для групп размещения виртуальных машин Azure близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1379">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="d29f3-1380">В Azure Site Recovery добавлена поддержка репликации из зоны в зону.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1380">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="d29f3-1381">В Azure Backup добавлена поддержка долгосрочного хранения для точек восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1381">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="d29f3-1382">В выходные данные командлета Get-AzRecoveryServicesBackupItem добавлены свойства исключения диска, добавленного в Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1382">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="d29f3-1383">Добавлена частная конечная точка для файла учетных данных хранилища для службы Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1383">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d29f3-1384">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-1384">Az.Resources</span></span>
* <span data-ttu-id="d29f3-1385">Добавлено предупреждение о задержке представления при создании определения роли.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1385">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="d29f3-1386">Командлеты политики теперь выводят строго типизированные объекты.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1386">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="d29f3-1387">Из командлета Get-AzResourceLock удален параметр -TenantLevel (№ 11335).</span><span class="sxs-lookup"><span data-stu-id="d29f3-1387">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="d29f3-1388">Исправлена ошибка с Remove-AzResourceGroup -Id ResourceId (№ 9882).</span><span class="sxs-lookup"><span data-stu-id="d29f3-1388">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="d29f3-1389">Добавлен новый командлет для получения результатов анализа гипотетических вариантов из шаблона ARM в области группы ресурсов: Get-AzDeploymentResourceGroupWhatIfResult.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1389">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="d29f3-1390">Добавлен новый командлет для получения результатов анализа гипотетических вариантов из шаблона ARM в области подписки: Get-AzDeploymentWhatIfResult.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1390">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="d29f3-1391">Alias: Get-AzSubscriptionDeploymentWhatIf.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1391">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="d29f3-1392">Переопределены параметры -WhatIf и -Confirm для New-AzDeployment и New-AzResourceGroupDeployment для использования результатов анализа гипотетических вариантов из шаблона ARM.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1392">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="d29f3-1393">В командлеты развертывания добавлено сообщение об устаревании для параметра ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1393">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="d29f3-1394">Добавлена возможность отображения улучшенных сообщений об ошибках при развертывании.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1394">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="d29f3-1395">Добавлена возможность регистрации correlationId для сбоев развертывания.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1395">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="d29f3-1396">В выходные данные скрипта развертывания добавлено свойство error.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1396">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="d29f3-1397">Пакет NuGet Microsoft.Azure.Management.ResourceManager обновлен до версии 3.7.1-preview.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1397">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="d29f3-1398">Удаленные определенные тестовые случаи как свойство error в DeploymentValidateResult были изменены на доступные только для чтения из пакета NuGet версии 3.7.1-preview.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1398">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="d29f3-1399">Добавлен GenericResourceExpanded из пакета SDK ResourceManager версии 3.7.1-preview.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1399">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="d29f3-1400">Добавлена поддержка тегов для всех командлетов Get для развертывания, а также для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1400">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="d29f3-1401">New-AzDeployment;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1401">'New-AzDeployment'</span></span>
    - <span data-ttu-id="d29f3-1402">New-AzManagementGroupDeployment;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1402">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="d29f3-1403">New-AzResourceGroupDeployment;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1403">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="d29f3-1404">New-AzTenantDeployment.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1404">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d29f3-1405">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d29f3-1405">Az.ServiceFabric</span></span>
* <span data-ttu-id="d29f3-1406">Исправлена ошибка при добавлении сертификата с помощью параметра -SecretIdentifier, когда возвращался неправильный отпечаток сертификата.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1406">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="d29f3-1407">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-1407">Az.Sql</span></span>
* <span data-ttu-id="d29f3-1408">Оптимизирована работа следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1408">Enhance performance of:</span></span>
    - <span data-ttu-id="d29f3-1409">Set-AzSqlDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1409">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="d29f3-1410">Set-AzSqlInstanceDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1410">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="d29f3-1411">Remove-AzSqlDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1411">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="d29f3-1412">Remove-AzSqlInstanceDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1412">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="d29f3-1413">Enable-AzSqlDatabaseSensitivityRecommendation;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1413">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="d29f3-1414">Enable-AzSqlInstanceDatabaseSensitivityRecommendation;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1414">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="d29f3-1415">Disable-AzSqlDatabaseSensitivityRecommendation;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1415">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="d29f3-1416">Disable-AzSqlInstanceDatabaseSensitivityRecommendation.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1416">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="d29f3-1417">Удалена проверка на стороне клиента параметра RetentionDays из командлета Set-AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1417">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="d29f3-1418">Добавлен аудит учетной записи хранения в виртуальной сети. Исправлена ошибка при создании роли участника данных BLOB-объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1418">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d29f3-1419">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d29f3-1419">Az.Storage</span></span>
* <span data-ttu-id="d29f3-1420">В командлет Get-AzStorageAccount добавлен параметр -AsJob.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1420">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="d29f3-1421">Параметр KeyVersion теперь является необязательным при изменении учетной записи хранения с помощью KeyvaultEncryption, что обеспечивает поддержку автоматической смены ключа.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1421">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="d29f3-1422">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d29f3-1422">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="d29f3-1423">Исправлена ошибка при удалении каталога файлов Azure с конвейером.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1423">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="d29f3-1424">Remove-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1424">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="d29f3-1425">Исправлена ошибка 9880. Значение DefaultAction для NetWorkRule приведено в соответствие со Swagger.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1425">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="d29f3-1426">Update-AzStorageAccountNetworkRuleSet;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1426">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="d29f3-1427">Get-AzStorageAccountNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1427">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="d29f3-1428">Исправлена ошибка 11624. При добавлении NetworkRules дублирующиеся правила пропускаются, чтобы не происходил сбой сервера.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1428">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="d29f3-1429">Add-AzStorageAccountNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1429">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="d29f3-1430">Версия пакета SDK Microsoft.Azure.Cosmos.Table обновлена до 1.0.7.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1430">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="d29f3-1431">Добавлено предупреждающее сообщение, напоминающее пользователю о необходимости повторного вывода списка с помощью ContinuationToken, когда в списке элементов Data Lake 2-го поколения возвращается только часть элементов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1431">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="d29f3-1432">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="d29f3-1432">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="d29f3-1433">Добавлена возможность создания или изменения учетной записи хранения с использованием проверки подлинности Active Directory для Файлов Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1433">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="d29f3-1434">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d29f3-1434">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="d29f3-1435">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d29f3-1435">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="d29f3-1436">Добавлена возможность создания и просмотра ключей Kerberos учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1436">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="d29f3-1437">New-AzStorageAccountKey;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1437">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="d29f3-1438">Get-AzStorageAccountKey.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1438">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="d29f3-1439">Добавлена возможность отработки отказа для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1439">Supported failover Storage account</span></span>
    - <span data-ttu-id="d29f3-1440">Invoke-AzStorageAccountFailover.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1440">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="d29f3-1441">Обновлена справка по Get-AzStorageBlobCopyState.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1441">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="d29f3-1442">Обновлена справка по Get-AzStorageFileCopyState и Start-AzStorageBlobCopy.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1442">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="d29f3-1443">Появилась интегрированная клиентская библиотека хранилища версии 12 для командлетов очередей и файлов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1443">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="d29f3-1444">Тип выходных данных изменен с CloudFile на AzureStorageFile. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1444">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="d29f3-1445">Get-AzStorageFile;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1445">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="d29f3-1446">Remove-AzStorageFile;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1446">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="d29f3-1447">Get-AzStorageFileContent;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1447">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="d29f3-1448">Set-AzStorageFileContent;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1448">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="d29f3-1449">Start-AzStorageFileCopy.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1449">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="d29f3-1450">Тип выходных данных изменен с CloudFileDirectory на AzureStorageFileDirectory. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1450">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="d29f3-1451">New-AzStorageDirectory;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1451">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="d29f3-1452">Remove-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1452">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="d29f3-1453">Тип выходных данных изменен с CloudFileShare на AzureStorageFileShare. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1453">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="d29f3-1454">Get-AzStorageShare;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1454">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="d29f3-1455">New-AzStorageShare;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1455">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="d29f3-1456">Remove-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1456">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="d29f3-1457">Тип выходных данных изменен с FileShareProperties на AzureStorageFileShare. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1457">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="d29f3-1458">Set-AzStorageShareQuota.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1458">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="d29f3-1459">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="d29f3-1459">Az.TrafficManager</span></span>
* <span data-ttu-id="d29f3-1460">Исправлено неправильное имя профиля в подробных выходных данных DisableAzureTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1460">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d29f3-1461">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d29f3-1461">Az.Websites</span></span>
* <span data-ttu-id="d29f3-1462">Исправлена опечатка в справке по Update-AzWebAppAccessRestrictionConfig.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1462">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="d29f3-1463">3.8.0 — апрель 2020 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1463">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="d29f3-1464">Основные сведения о новых возможностях с момента последнего выпуска</span><span class="sxs-lookup"><span data-stu-id="d29f3-1464">Highlights since the last release</span></span>
* <span data-ttu-id="d29f3-1465">Версии PowerShell, которые поддерживает Az.Storage: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="d29f3-1465">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d29f3-1466">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d29f3-1466">Az.Accounts</span></span>
* <span data-ttu-id="d29f3-1467">Обновлен URL-адрес опроса Azure PowerShell в Resolve-AzError [11507].</span><span class="sxs-lookup"><span data-stu-id="d29f3-1467">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d29f3-1468">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d29f3-1468">Az.ApiManagement</span></span>
* <span data-ttu-id="d29f3-1469">Добавлено уведомление о критическом изменении для изменения выходных данных командлетов, выполняющих действия с файлами в Azure, в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1469">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="d29f3-1470">Обновлена документация для Set-AzApiManagementGroup с указанием параметра GroupId.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1470">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d29f3-1471">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d29f3-1471">Az.Cdn</span></span>
* <span data-ttu-id="d29f3-1472">Исправлено отображение ценовой категории (SKU), связанной с ChinaCDN.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1472">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d29f3-1473">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-1473">Az.CognitiveServices</span></span>
* <span data-ttu-id="d29f3-1474">Включена поддержка Identity, Encryption, UserOwnedStorage.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1474">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d29f3-1475">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-1475">Az.Compute</span></span>
* <span data-ttu-id="d29f3-1476">Добавлен командлет Set-AzVmssOrchestrationServiceState.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1476">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="d29f3-1477">Get-AzVmss с параметром -InstanceView отображает состояния OrchestrationService.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1477">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d29f3-1478">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d29f3-1478">Az.IotHub</span></span>
* <span data-ttu-id="d29f3-1479">Реализовано управление конфигурацией двойника устройства Интернета вещей. Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1479">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="d29f3-1480">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="d29f3-1480">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="d29f3-1481">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="d29f3-1481">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="d29f3-1482">Добавлен командлет для вызова прямого метода на устройстве в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1482">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="d29f3-1483">Реализовано управление конфигурацией двойника модуля устройства Интернета вещей. Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1483">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="d29f3-1484">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="d29f3-1484">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="d29f3-1485">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="d29f3-1485">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="d29f3-1486">Реализовано управление конфигурацией автоматического управления устройствами в центре Интернета вещей в большом масштабе.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1486">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="d29f3-1487">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1487">New cmdlets are:</span></span>
    - <span data-ttu-id="d29f3-1488">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="d29f3-1488">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="d29f3-1489">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="d29f3-1489">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="d29f3-1490">Remove-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="d29f3-1490">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="d29f3-1491">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="d29f3-1491">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="d29f3-1492">Добавлен командлет для вызова метода периферийного модуля в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1492">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d29f3-1493">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d29f3-1493">Az.KeyVault</span></span>
* <span data-ttu-id="d29f3-1494">Добавлен новый командлет Update-AzKeyVault, который может включать защиту от обратимого удаления и очистки в хранилище.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1494">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="d29f3-1495">Включена поддержка Microsoft.PowerShell.SecretManagement [11178].</span><span class="sxs-lookup"><span data-stu-id="d29f3-1495">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="d29f3-1496">Исправлена ошибка в примерах Remove-AzKeyVaultManagedStorageSasDefinition [11479].</span><span class="sxs-lookup"><span data-stu-id="d29f3-1496">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="d29f3-1497">Включена поддержка частной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1497">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="d29f3-1498">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="d29f3-1498">Az.Maintenance</span></span>
* <span data-ttu-id="d29f3-1499">Опубликована версия выпуска командлетов обслуживания для общедоступной версии.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1499">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d29f3-1500">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d29f3-1500">Az.Monitor</span></span>
* <span data-ttu-id="d29f3-1501">Добавлены командлеты для области приватных каналов:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1501">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="d29f3-1502">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="d29f3-1502">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="d29f3-1503">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="d29f3-1503">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="d29f3-1504">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="d29f3-1504">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="d29f3-1505">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="d29f3-1505">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="d29f3-1506">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="d29f3-1506">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="d29f3-1507">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="d29f3-1507">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="d29f3-1508">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="d29f3-1508">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d29f3-1509">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d29f3-1509">Az.Network</span></span>
* <span data-ttu-id="d29f3-1510">Обновлены командлеты для включения подключения на частном IP-адресе для шлюза виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1510">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="d29f3-1511">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d29f3-1511">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="d29f3-1512">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d29f3-1512">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="d29f3-1513">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d29f3-1513">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="d29f3-1514">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d29f3-1514">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="d29f3-1515">Обновлены командлеты для включения шлюзов LocalNetworkGateways и сайтов VpnSites на основе FQDN:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1515">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="d29f3-1516">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d29f3-1516">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="d29f3-1517">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="d29f3-1517">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="d29f3-1518">Включена поддержка семейства адресов IPv6 в ExpressRouteCircuitConnectionConfig (Global Reach).</span><span class="sxs-lookup"><span data-stu-id="d29f3-1518">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="d29f3-1519">Добавлен командлет Set-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1519">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="d29f3-1520">Позволяет выполнять настройку всех существующих свойств, включая IPv6CircuitConnectionProperties.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1520">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="d29f3-1521">Обновлен командлет Add-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1521">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="d29f3-1522">Добавлен еще один необязательный параметр AddressPrefixType для указания семейства адресов префикса адреса.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1522">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="d29f3-1523">Обновлены командлеты для включения параметра времени ожидания для обнаружения неиспользуемых одноранговых узлов (DPD) в подключениях шлюзов виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1523">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="d29f3-1524">New-AzVirtualNetworkGatewayConnection;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1524">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="d29f3-1525">Set-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1525">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d29f3-1526">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d29f3-1526">Az.PolicyInsights</span></span>
* <span data-ttu-id="d29f3-1527">Добавлен командлет Start-AzPolicyComplianceScan для запуска проверок соответствия политикам.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1527">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="d29f3-1528">Добавлены версии определения политики, определения набора и назначения в выходные данные командлета Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1528">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d29f3-1529">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d29f3-1529">Az.ServiceFabric</span></span>
* <span data-ttu-id="d29f3-1530">Улучшено форматирование и наглядность кода в примерах New-AzServiceFabricCluster.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1530">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="d29f3-1531">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-1531">Az.Sql</span></span>
* <span data-ttu-id="d29f3-1532">Добавлены командлеты Get-AzSqlInstanceOperation и Stop-AzSqlInstanceOperation.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1532">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="d29f3-1533">Включен аудит учетной записи хранения в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1533">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d29f3-1534">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d29f3-1534">Az.Storage</span></span>
* <span data-ttu-id="d29f3-1535">Добавлено уведомление о критическом изменении для изменения выходных данных командлетов, выполняющих действия с файлами в Azure, в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1535">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="d29f3-1536">Включена поддержка новых имен SKU StandardGZRS, StandardRAGZRS при создании или обновлении учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1536">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="d29f3-1537">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d29f3-1537">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="d29f3-1538">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d29f3-1538">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="d29f3-1539">Добавлена поддержка DataLake 2-го поколения.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1539">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="d29f3-1540">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="d29f3-1540">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="d29f3-1541">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="d29f3-1541">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="d29f3-1542">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="d29f3-1542">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="d29f3-1543">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="d29f3-1543">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="d29f3-1544">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="d29f3-1544">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="d29f3-1545">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="d29f3-1545">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="d29f3-1546">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="d29f3-1546">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="d29f3-1547">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="d29f3-1547">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="d29f3-1548">0.10.0-preview — апрель 2020 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1548">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="d29f3-1549">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="d29f3-1549">General</span></span>
* <span data-ttu-id="d29f3-1550">Модуль Az стали доступными в предварительной версии в Azure Stack Hub.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1550">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="d29f3-1551">Это обеспечивает кросс-платформенную совместимость с Linux и macOs.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1551">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="d29f3-1552">Azure Stack Hub теперь поддерживает PowerShell Core с модулями Az (см. [дополнительные сведения](/azure-stack/operator/powershell-install-az-module))</span><span class="sxs-lookup"><span data-stu-id="d29f3-1552">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](/azure-stack/operator/powershell-install-az-module)</span></span>
* <span data-ttu-id="d29f3-1553">Модули Az поддерживают профиль 2019-03-01-hybrid:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1553">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="d29f3-1554">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="d29f3-1554">Az.Billing</span></span>
  - <span data-ttu-id="d29f3-1555">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-1555">Az.Compute</span></span>
  - <span data-ttu-id="d29f3-1556">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="d29f3-1556">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="d29f3-1557">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d29f3-1557">Az.EventHub</span></span>
  - <span data-ttu-id="d29f3-1558">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d29f3-1558">Az.IotHub</span></span>
  - <span data-ttu-id="d29f3-1559">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d29f3-1559">Az.KeyVault</span></span>
  - <span data-ttu-id="d29f3-1560">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d29f3-1560">Az.Monitor</span></span>
  - <span data-ttu-id="d29f3-1561">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d29f3-1561">Az.Network</span></span>
  - <span data-ttu-id="d29f3-1562">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-1562">Az.Resources</span></span>
  - <span data-ttu-id="d29f3-1563">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d29f3-1563">Az.Storage</span></span>
  - <span data-ttu-id="d29f3-1564">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d29f3-1564">Az.Websites</span></span>
* <span data-ttu-id="d29f3-1565">В PowerShell появились три новых модуля Az, которые работают с Azure Stack Hub: Az.Databox, Az.IotHub и Az.EventHub.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1565">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="d29f3-1566">Команды остаются прежними же за исключением незначительных изменений, таких как изменение AzureRM на Az.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1566">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="d29f3-1567">См. обновленную ссылку на документацию по [PowerShell для Azure Stack Hub](/azure-stack/operator/powershell-install-az-module)</span><span class="sxs-lookup"><span data-stu-id="d29f3-1567">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](/azure-stack/operator/powershell-install-az-module)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="d29f3-1568">3.7.0 — март 2020 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1568">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d29f3-1569">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d29f3-1569">Az.Accounts</span></span>
* <span data-ttu-id="d29f3-1570">Исправлено исключение NullReferenceException командлетов Get-AzTenant/Get-AzDefault/Set-AzDefault, если вход не выполнен [10292]</span><span class="sxs-lookup"><span data-stu-id="d29f3-1570">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d29f3-1571">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-1571">Az.Compute</span></span>
* <span data-ttu-id="d29f3-1572">Добавлены следующие параметры к командлету New-AzDiskConfig:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1572">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="d29f3-1573">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="d29f3-1573">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="d29f3-1574">Разрешено свойство Encryption для параметра Target командлета New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1574">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="d29f3-1575">Исправлена проблема с tempDisk для командлетов Set-AzVmss -Reimage и Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1575">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="d29f3-1576">[11354]</span><span class="sxs-lookup"><span data-stu-id="d29f3-1576">[#11354]</span></span>
* <span data-ttu-id="d29f3-1577">Добавлена поддержка нового расширения SAP для указанных ниже командлетов</span><span class="sxs-lookup"><span data-stu-id="d29f3-1577">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="d29f3-1578">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d29f3-1578">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="d29f3-1579">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d29f3-1579">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="d29f3-1580">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d29f3-1580">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="d29f3-1581">Update-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d29f3-1581">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="d29f3-1582">Исправлены ошибки в примерах справки</span><span class="sxs-lookup"><span data-stu-id="d29f3-1582">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="d29f3-1583">Показано точное строковое значение в табличном формате для свойства PowerState виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1583">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="d29f3-1584">New-AzVmssConfig: исправлена сериализация свойства AutomaticRepairs, если параметр SinglePlacementGroup отключен.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1584">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="d29f3-1585">[11257]</span><span class="sxs-lookup"><span data-stu-id="d29f3-1585">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d29f3-1586">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d29f3-1586">Az.DataFactory</span></span>
* <span data-ttu-id="d29f3-1587">Пакет SDK ADF для .NET обновлен до версии 4.8.0.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1587">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="d29f3-1588">Добавлены необязательные параметры для команды Invoke-AzDataFactoryV2Pipeline для поддержки повторного запуска.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1588">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d29f3-1589">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d29f3-1589">Az.DataLakeStore</span></span>
* <span data-ttu-id="d29f3-1590">Добавлено описание критического изменения для Export-AzDataLakeStoreItem и Import-AzDataLakeStoreItem.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1590">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="d29f3-1591">Добавлен параметр кодирования байтов для New-AzDataLakeStoreItem, Add-AzDAtaLakeStoreItemContent и Get-AzDAtaLakeStoreItemContent.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1591">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d29f3-1592">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d29f3-1592">Az.HDInsight</span></span>
* <span data-ttu-id="d29f3-1593">Добавлена поддержка указания минимальной поддерживаемой версии TLS при создании кластера.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1593">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d29f3-1594">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d29f3-1594">Az.IotHub</span></span>
* <span data-ttu-id="d29f3-1595">Добавлена поддержка для управления распределенными параметрами на отдельных устройствах.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1595">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="d29f3-1596">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1596">New Cmdlets are:</span></span>
    - <span data-ttu-id="d29f3-1597">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="d29f3-1597">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="d29f3-1598">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="d29f3-1598">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d29f3-1599">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d29f3-1599">Az.KeyVault</span></span>
* <span data-ttu-id="d29f3-1600">Добавлены атрибуты критических изменений для New-AzKeyVault.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1600">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d29f3-1601">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d29f3-1601">Az.Monitor</span></span>
* <span data-ttu-id="d29f3-1602">Обновлена документация для New-AzScheduledQueryRuleLogMetricTrigger.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1602">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d29f3-1603">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d29f3-1603">Az.Network</span></span>
* <span data-ttu-id="d29f3-1604">Обновлены командлеты для поддержки подключений VirtualHubVnetConnections между клиентами</span><span class="sxs-lookup"><span data-stu-id="d29f3-1604">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="d29f3-1605">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="d29f3-1605">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="d29f3-1606">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="d29f3-1606">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="d29f3-1607">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="d29f3-1607">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="d29f3-1608">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="d29f3-1608">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="d29f3-1609">Удалена зависимость пакета SDK для управления SQL.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1609">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d29f3-1610">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d29f3-1610">Az.PolicyInsights</span></span>
* <span data-ttu-id="d29f3-1611">Улучшены сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1611">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d29f3-1612">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-1612">Az.RecoveryServices</span></span>
* <span data-ttu-id="d29f3-1613">В Azure Site Recovery реализована поддержка повторной защиты и обновлены свойства зашифрованных виртуальных машин диска Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1613">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="d29f3-1614">Добавлена возможность мониторинг аварийного восстановления для свойств VmwareToAzure в Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1614">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="d29f3-1615">В Azure Backup реализована поддержка повторного обновления политики для элементов с ошибками.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1615">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="d29f3-1616">В Azure Backup реализована поддержка параметров исключения диска во время резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1616">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="d29f3-1617">В Azure Backup реализована поддержка восстановления нескольких файлов или папок в AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="d29f3-1617">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="d29f3-1618">В Azure Backup реализована поддержка указанной пользователем группы Resourcegroup при обновлении политики IaasVM.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1618">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="d29f3-1619">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-1619">Az.Resources</span></span>
* <span data-ttu-id="d29f3-1620">Исправлена команда Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType для использования фактической версии apiVersion ресурсов (а не версии apiVersion по умолчанию) [11267].</span><span class="sxs-lookup"><span data-stu-id="d29f3-1620">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="d29f3-1621">Добавлена возможность регистрации correlationId для сценариев с ошибками.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1621">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="d29f3-1622">Незначительно изменена документация по Get-AzResourceLock.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1622">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="d29f3-1623">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1623">Added example.</span></span>
* <span data-ttu-id="d29f3-1624">Экранирована одинарная кавычка в значении параметра Get-AzADUser [11317].</span><span class="sxs-lookup"><span data-stu-id="d29f3-1624">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="d29f3-1625">Добавлены новые командлеты для сценариев развертывания (Get-AzDeploymentScript, Get-AzDeploymentScriptLog, Save-AzDeploymentScriptLog, Remove-AzDeploymentScript).</span><span class="sxs-lookup"><span data-stu-id="d29f3-1625">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="d29f3-1626">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-1626">Az.Sql</span></span>
* <span data-ttu-id="d29f3-1627">Добавлен параметр вторичной реплики для чтения для командлета Invoke-AzSqlDatabaseFailover.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1627">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="d29f3-1628">Добавлен командлет Disable-AzSqlServerActiveDirectoryOnlyAuthentication.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1628">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="d29f3-1629">Сохранен приоритет конфиденциальности при классификации столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1629">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="d29f3-1630">Az.Support</span><span class="sxs-lookup"><span data-stu-id="d29f3-1630">Az.Support</span></span>
* <span data-ttu-id="d29f3-1631">Модуль Az.Support стал общедоступным.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1631">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d29f3-1632">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d29f3-1632">Az.Websites</span></span>
* <span data-ttu-id="d29f3-1633">Реализована поддержка работы с правилами маршрутизации трафика веб-приложения через указанные ниже командлеты</span><span class="sxs-lookup"><span data-stu-id="d29f3-1633">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="d29f3-1634">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="d29f3-1634">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="d29f3-1635">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="d29f3-1635">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="d29f3-1636">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="d29f3-1636">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="d29f3-1637">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="d29f3-1637">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="d29f3-1638">3.6.1 — март 2020 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1638">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d29f3-1639">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d29f3-1639">Az.Accounts</span></span>
* <span data-ttu-id="d29f3-1640">Открытие страницы опроса Azure PowerShell в Send-Feedback [11020].</span><span class="sxs-lookup"><span data-stu-id="d29f3-1640">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="d29f3-1641">Отображение URL-адреса опроса Azure PowerShell в Resolve-Error [11021].</span><span class="sxs-lookup"><span data-stu-id="d29f3-1641">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="d29f3-1642">Добавлена версия Az в UserAgent.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1642">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d29f3-1643">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d29f3-1643">Az.ApiManagement</span></span>
* <span data-ttu-id="d29f3-1644">Включена поддержка получения и настройки личного домена в конечной точке DeveloperPortal [11007].</span><span class="sxs-lookup"><span data-stu-id="d29f3-1644">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="d29f3-1645">Export-AzApiManagementApi: включена поддержка скачивания определения API в формате JSON [9987].</span><span class="sxs-lookup"><span data-stu-id="d29f3-1645">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="d29f3-1646">Import-AzApiManagementApi: включена поддержка импорта определения OpenApi 3.0 из документа JSON.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1646">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="d29f3-1647">New-AzApiManagementIdentityProvider и Set-AzApiManagementIdentityProvider: включена поддержка настройки входа арендатора для поставщика AAD B2C [9784].</span><span class="sxs-lookup"><span data-stu-id="d29f3-1647">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d29f3-1648">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d29f3-1648">Az.DataLakeStore</span></span>
* <span data-ttu-id="d29f3-1649">Добавлена ссылка на System.Buffers явным образом в CSPROJ и PSD1.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1649">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d29f3-1650">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d29f3-1650">Az.IotHub</span></span>
* <span data-ttu-id="d29f3-1651">Добавлена возможность управления устройствами в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1651">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="d29f3-1652">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1652">New Cmdlets are:</span></span>
    - <span data-ttu-id="d29f3-1653">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="d29f3-1653">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="d29f3-1654">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="d29f3-1654">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="d29f3-1655">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="d29f3-1655">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="d29f3-1656">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="d29f3-1656">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="d29f3-1657">Включена поддержка управления модулями в целевом устройстве Интернета вещей в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1657">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="d29f3-1658">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1658">New Cmdlets are:</span></span>
    - <span data-ttu-id="d29f3-1659">Add-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="d29f3-1659">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="d29f3-1660">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="d29f3-1660">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="d29f3-1661">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="d29f3-1661">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="d29f3-1662">Set-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="d29f3-1662">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="d29f3-1663">Добавлен командлет для получения строки подключения целевого устройства Интернета вещей в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1663">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="d29f3-1664">Добавлен командлет для получения строки подключения модуля на целевом устройстве Интернета вещей в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1664">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="d29f3-1665">Включена поддержка для получения или настройки родительского устройства для устройства Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1665">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="d29f3-1666">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1666">New Cmdlets are:</span></span>
    - <span data-ttu-id="d29f3-1667">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="d29f3-1667">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="d29f3-1668">Set-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="d29f3-1668">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="d29f3-1669">Включена поддержка управления связью "родители — потомки" устройства.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1669">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d29f3-1670">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d29f3-1670">Az.Monitor</span></span>
* <span data-ttu-id="d29f3-1671">Исправлено выходное значение для Get-AzMetricDefinition [9714].</span><span class="sxs-lookup"><span data-stu-id="d29f3-1671">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d29f3-1672">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d29f3-1672">Az.Network</span></span>
* <span data-ttu-id="d29f3-1673">Обновлен пакет SDK для управления SQL.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1673">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="d29f3-1674">Исправлена проблема с разницей в именовании в классе PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1674">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="d29f3-1675">Сопоставление ActionsRequired с ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1675">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="d29f3-1676">Добавление PublicNetworkAccess в команды New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1676">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="d29f3-1677">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-1677">Az.Resources</span></span>
* <span data-ttu-id="d29f3-1678">Исправлена ошибка пустой ссылки в Get-AzRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1678">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="d29f3-1679">Параметры -Force и -PassThru помечены необязательными в Remove-AzADGroup [10849].</span><span class="sxs-lookup"><span data-stu-id="d29f3-1679">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="d29f3-1680">Исправлена ошибка, из-за которой MailNickname не возвращается в Remove-AzADGroup [11167].</span><span class="sxs-lookup"><span data-stu-id="d29f3-1680">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="d29f3-1681">Исправлена ошибка, из-за которой операция канала Remove-AzADGroup не работает [11171].</span><span class="sxs-lookup"><span data-stu-id="d29f3-1681">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="d29f3-1682">Исправлена ошибка с пустой ссылкой в GetAzureRoleAssignmentCommand.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1682">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="d29f3-1683">Добавлено критическое изменение атрибутов для будущих изменений командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1683">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="d29f3-1684">Обновлена команда Get-AzResourceGroup для выполнения фильтрации тегов группы ресурсов на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1684">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="d29f3-1685">Расширены командлеты Tag для включения поддержки параметра -ResourceId.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1685">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="d29f3-1686">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="d29f3-1686">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="d29f3-1687">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="d29f3-1687">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="d29f3-1688">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="d29f3-1688">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="d29f3-1689">Добавлен новый командлет Tag.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1689">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="d29f3-1690">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="d29f3-1690">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="d29f3-1691">Предоставляется ScopedDeployment из пакета SDK 3.3.0.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1691">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="d29f3-1692">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-1692">Az.Sql</span></span>
* <span data-ttu-id="d29f3-1693">Добавление PublicNetworkAccess в команды New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1693">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="d29f3-1694">Включена поддержка конфигурации резервного копирования долгосрочного хранения для управляемых баз данных.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1694">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="d29f3-1695">Получение или настройка политики LTR в управляемой базе данных.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1695">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="d29f3-1696">Получение резервных копий LTR по управляемой базе данных, управляемому экземпляру или расположению.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1696">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="d29f3-1697">Удаление резервной копии LTR.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1697">Remove an LTR backup</span></span>
    - <span data-ttu-id="d29f3-1698">Восстановление резервной копии LTR для создания новой управляемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1698">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="d29f3-1699">Добавление MinimalTlsVersion в New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1699">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="d29f3-1700">Добавление MinimalTlsVersion в New-AzSqlInstance и Set-AzSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1700">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="d29f3-1701">Обновлена версия пакета SDK для SQL для Az.Network.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1701">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d29f3-1702">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d29f3-1702">Az.Storage</span></span>
* <span data-ttu-id="d29f3-1703">Включена поддержка AllowProtectedAppendWrite в ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1703">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="d29f3-1704">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d29f3-1704">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="d29f3-1705">Добавлено предупреждение о критическом изменении для изменения типа AzureStorageTable в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1705">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="d29f3-1706">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="d29f3-1706">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="d29f3-1707">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="d29f3-1707">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d29f3-1708">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d29f3-1708">Az.Websites</span></span>
* <span data-ttu-id="d29f3-1709">Добавлен параметр Tag для New-AzAppServicePlan и Set-AzAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1709">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="d29f3-1710">Завершение выполнения командлета, если при добавлении личного домена на веб-сайт возникает исключение.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1710">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="d29f3-1711">Включена поддержка выполнения операций для Служб приложений, которые находятся не в той же группе ресурсов, что и план службы приложений.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1711">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="d29f3-1712">Применение ограничения доступа к WebApp/Function в разных группах ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1712">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="d29f3-1713">Исправлена ошибка с указанием пользовательских имен узлов для WebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1713">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="d29f3-1714">3.5.0 — февраль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1714">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d29f3-1715">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="d29f3-1715">Highlights since the last major release</span></span>
* <span data-ttu-id="d29f3-1716">Обновлены данные телеметрии на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1716">Updated client side telemetry.</span></span>
* <span data-ttu-id="d29f3-1717">В Az.IotHub добавлены командлеты для управления устройствами.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1717">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="d29f3-1718">В Az.SqlVirtualMachine добавлены командлеты для прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1718">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d29f3-1719">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d29f3-1719">Az.Accounts</span></span>
* <span data-ttu-id="d29f3-1720">В данные телеметрии на стороне клиента добавлены такие сведения, как идентификатор подписки, идентификатор арендатора и время выполнения.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1720">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d29f3-1721">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d29f3-1721">Az.Automation</span></span>
* <span data-ttu-id="d29f3-1722">Исправлена опечатка в примере 1 в справочной документации по New-AzAutomationSoftwareUpdateConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1722">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d29f3-1723">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-1723">Az.CognitiveServices</span></span>
* <span data-ttu-id="d29f3-1724">Обновлен пакет SDK до версии 7.0.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1724">Updated SDK to 7.0</span></span>
* <span data-ttu-id="d29f3-1725">Улучшено сообщение об ошибке, которое появляется, если ответы сервера не содержат текст.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1725">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d29f3-1726">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-1726">Az.Compute</span></span>
* <span data-ttu-id="d29f3-1727">Разрешено использовать пустое значение для ProximityPlacementGroupId во время обновления.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1727">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d29f3-1728">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d29f3-1728">Az.FrontDoor</span></span>
* <span data-ttu-id="d29f3-1729">Добавлен командлет для получения определений управляемых правил, которые могут использоваться в WAF.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1729">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d29f3-1730">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d29f3-1730">Az.IotHub</span></span>
* <span data-ttu-id="d29f3-1731">Добавлена возможность управления устройствами в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1731">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="d29f3-1732">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1732">New Cmdlets are:</span></span>
    - <span data-ttu-id="d29f3-1733">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="d29f3-1733">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="d29f3-1734">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="d29f3-1734">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="d29f3-1735">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="d29f3-1735">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="d29f3-1736">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="d29f3-1736">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d29f3-1737">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d29f3-1737">Az.KeyVault</span></span>
* <span data-ttu-id="d29f3-1738">Устранен дублирующийся текст для Add-AzKeyVaultKey.md.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1738">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d29f3-1739">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d29f3-1739">Az.Monitor</span></span>
* <span data-ttu-id="d29f3-1740">Исправлено описание командлета Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1740">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="d29f3-1741">В команду New-AzMetricAlertRuleV2 добавлен новый параметр ActionGroupId.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1741">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="d29f3-1742">Пользователь может предоставить ActionGroupId(string) или ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="d29f3-1742">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d29f3-1743">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d29f3-1743">Az.Network</span></span>
* <span data-ttu-id="d29f3-1744">Добавлен еще один параметр -EnableProxyProtocol для командлета New-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1744">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="d29f3-1745">Исправлен пример FilterData в Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1745">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="d29f3-1746">Добавлен пример Packet Capture для всех внутренних и внешних пакетов в Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1746">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="d29f3-1747">Добавлена поддерживаемая политика Брандмауэра Azure в брандмауэрах виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1747">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="d29f3-1748">Новые командлеты не добавлены.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1748">No new cmdlets are added.</span></span> <span data-ttu-id="d29f3-1749">Снято ограничение политики брандмауэра в брандмауэрах виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1749">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d29f3-1750">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-1750">Az.RecoveryServices</span></span>
* <span data-ttu-id="d29f3-1751">Добавлена возможность восстановления в виде файлов для Баз данных SQL.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1751">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d29f3-1752">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-1752">Az.Resources</span></span>
* <span data-ttu-id="d29f3-1753">Выполнен рефакторинг командлетов развертывания шаблона.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1753">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="d29f3-1754">Добавлены новые командлеты для управления развертываниями в группе управления: \*-AzManagementGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1754">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="d29f3-1755">Добавлены новые командлеты для управления развертываниями в области арендатора: \*-AzTenantDeployment.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1755">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="d29f3-1756">Выполнен рефакторинг командлетов \*-AzDeployment для работы в области подписки.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1756">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="d29f3-1757">Созданы псевдонимы \*-AzSubscriptionDeployment для командлетов \*-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1757">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="d29f3-1758">Исправлен командлет Update-AzADApplication, когда параметр AvailableToOtherTenants не задан.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1758">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="d29f3-1759">Удален набор параметров ApplicationObjectWithoutCredentialParameterSet, чтобы предотвратить возникновение AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1759">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="d29f3-1760">Повторно созданы файлы справки.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1760">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="d29f3-1761">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-1761">Az.Sql</span></span>
* <span data-ttu-id="d29f3-1762">Добавлена возможность восстановления точки во времени между подписками в Управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1762">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="d29f3-1763">Добавлена возможность изменения существующего поколения оборудования Управляемого экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1763">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="d29f3-1764">Исправлены примеры справки Update-AzSqlServerVulnerabilityAssessmentSetting: выходные данные параметра и свойства — EmailAdmins.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1764">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="d29f3-1765">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d29f3-1765">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="d29f3-1766">Добавлены командлеты для прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1766">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="d29f3-1767">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="d29f3-1767">Az.StorageSync</span></span>
* <span data-ttu-id="d29f3-1768">В командлете Invoke-AzStorageSyncCompatibilityCheck обновлены поддерживаемые наборы символов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1768">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="d29f3-1769">3.4.0 — февраль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1769">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d29f3-1770">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="d29f3-1770">Highlights since the last major release</span></span>
* <span data-ttu-id="d29f3-1771">Выпущена первоначальная версия 0.1.0 Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="d29f3-1771">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="d29f3-1772">Добавлена поддержка Az.Network ConnectionMonitor V2</span><span class="sxs-lookup"><span data-stu-id="d29f3-1772">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d29f3-1773">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d29f3-1773">Az.Accounts</span></span>
* <span data-ttu-id="d29f3-1774">Отключить автоматическое сохранение контекста, если AzureRmContext.json недоступен</span><span class="sxs-lookup"><span data-stu-id="d29f3-1774">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="d29f3-1775">Обновление ссылки на Azure Powershell Common до предварительной версии 1.3.5</span><span class="sxs-lookup"><span data-stu-id="d29f3-1775">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d29f3-1776">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d29f3-1776">Az.ApiManagement</span></span>
* <span data-ttu-id="d29f3-1777">**Get-AzApiManagementApiSchema** Исправлено получение схемы Open-API, связанной с API https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="d29f3-1777">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="d29f3-1778">**New-AzApiManagementProduct** _ и _ *Set-AzApiManagementProduct*\*</span><span class="sxs-lookup"><span data-stu-id="d29f3-1778">**New-AzApiManagementProduct** _ and _ *Set-AzApiManagementProduct*\*</span></span>
  - <span data-ttu-id="d29f3-1779">Исправить документацию для https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="d29f3-1779">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="d29f3-1780">**Set-AzApiManagementApi** Добавлен пример, показывающий, как обновить ServiceUrl с помощью командлета</span><span class="sxs-lookup"><span data-stu-id="d29f3-1780">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d29f3-1781">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-1781">Az.Compute</span></span>
* <span data-ttu-id="d29f3-1782">Ограничение числа состояний виртуальных машин до 100, чтобы избежать регулирования при выполнении Get-AzVM-Status без имени виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1782">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="d29f3-1783">Добавление обновления командлета -AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="d29f3-1783">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="d29f3-1784">Добавление параметров EncryptionType и DiskEncryptionSetId в следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1784">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="d29f3-1785">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="d29f3-1785">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="d29f3-1786">Добавление параметра ColocationStatus в командлет Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1786">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d29f3-1787">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d29f3-1787">Az.DataFactory</span></span>
* <span data-ttu-id="d29f3-1788">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.7.0.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1788">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="d29f3-1789">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="d29f3-1789">Az.DeploymentManager</span></span>
* <span data-ttu-id="d29f3-1790">Добавляет операции LIST для ресурсов</span><span class="sxs-lookup"><span data-stu-id="d29f3-1790">Adds LIST operations for resources</span></span>
* <span data-ttu-id="d29f3-1791">Добавляет возможность выполнения операций на этапах Проверки работоспособности</span><span class="sxs-lookup"><span data-stu-id="d29f3-1791">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d29f3-1792">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d29f3-1792">Az.HDInsight</span></span>
* <span data-ttu-id="d29f3-1793">Исправление ошибки в документе New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1793">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d29f3-1794">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d29f3-1794">Az.KeyVault</span></span>
* <span data-ttu-id="d29f3-1795">Добавление Псевдонимов имени в атрибут VaultName, чтобы Remove-AzureKeyVault соответствовал New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1795">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d29f3-1796">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d29f3-1796">Az.Network</span></span>
* <span data-ttu-id="d29f3-1797">В Set-AzNetworkWatcherConfigFlowLog.md добавлен новый пример для демонстрации сценария отключения Аналитики трафика.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1797">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="d29f3-1798">Добавление поддержки назначения IP-конфигурации для брандмауэра Azure — выделенная подсеть и общедоступный IP-адрес, которые брандмауэр будет использовать для управления трафиком</span><span class="sxs-lookup"><span data-stu-id="d29f3-1798">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="d29f3-1799">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1799">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="d29f3-1800">добавлен параметр — ManagementPublicIpAddress (необязательный), который принимает объект общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="d29f3-1800">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="d29f3-1801">Добавлен метод SetManagementIpConfiguration для объекта брандмауэра — в качестве входных данных требуется подсеть и общедоступный IP-адрес — имя подсети должно быть "AzureFirewallManagementSubnet"</span><span class="sxs-lookup"><span data-stu-id="d29f3-1801">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="d29f3-1802">Исправлены примеры Get-AzNetworkSecurityGroup для отображения примеров для группы безопасности сети (NSG) вместо сетевых интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1802">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="d29f3-1803">Исправлена опечатка в команде New-AzVpnSite, которая препятствовала завершению параметра идентификатором ресурса.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1803">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="d29f3-1804">Добавлена поддержка конфигурации в наборе действий для правил подстановки URL-адресов в шлюзе приложения.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1804">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="d29f3-1805">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1805">New cmdlets added:</span></span>
        - <span data-ttu-id="d29f3-1806">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="d29f3-1806">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="d29f3-1807">В следующие командлеты добавлен необязательный параметр — UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="d29f3-1807">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="d29f3-1808">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="d29f3-1808">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="d29f3-1809">Добавление поддержки для ресурсов NetworkWatcher ConnectionMonitor версии 2</span><span class="sxs-lookup"><span data-stu-id="d29f3-1809">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d29f3-1810">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d29f3-1810">Az.PolicyInsights</span></span>
* <span data-ttu-id="d29f3-1811">Поддержка оценки соответствия до определения того, какой ресурс нужно исправить</span><span class="sxs-lookup"><span data-stu-id="d29f3-1811">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="d29f3-1812">Добавление параметра "—ResourceDiscoverMode" в Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="d29f3-1812">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="d29f3-1813">Добавление командлета Get-AzPolicyMetadata для получения ресурсов метаданных политики</span><span class="sxs-lookup"><span data-stu-id="d29f3-1813">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="d29f3-1814">Get-AzPolicyState и Get-AzPolicyStateSummary обновлены для API версии 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="d29f3-1814">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d29f3-1815">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-1815">Az.RecoveryServices</span></span>
* <span data-ttu-id="d29f3-1816">Поддержка Azure Site Recovery для удаления реплицированного диска.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1816">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="d29f3-1817">В Azure Backup добавлена ​​поддержка добавления тегов при создании Хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1817">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d29f3-1818">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-1818">Az.Resources</span></span>
* <span data-ttu-id="d29f3-1819">Сделайте команду "Область" необязательной в командлетах \*—AzPolicyAssignment с настройкой по умолчанию для контекстной подписки</span><span class="sxs-lookup"><span data-stu-id="d29f3-1819">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="d29f3-1820">Добавление примеров создания ADServicePrincipal с паролем и ключом учетных данных</span><span class="sxs-lookup"><span data-stu-id="d29f3-1820">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="d29f3-1821">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-1821">Az.Sql</span></span>
<span data-ttu-id="d29f3-1822">Исправление командлета New-AzSqlDatabaseSecondary, чтобы проверить существование PartnerDatabaseName, а не DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1822">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d29f3-1823">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d29f3-1823">Az.Storage</span></span>
* <span data-ttu-id="d29f3-1824">Поддержка набора шифрования типа ключа таблиц и очередей в создании учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="d29f3-1824">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="d29f3-1825">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d29f3-1825">New-AzStorageAccount</span></span>
* <span data-ttu-id="d29f3-1826">Представление RequestId, если StorageException не имеет ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="d29f3-1826">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="d29f3-1827">Исправление примера 6 командлета Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="d29f3-1827">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d29f3-1828">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d29f3-1828">Az.Websites</span></span>
* <span data-ttu-id="d29f3-1829">Set-AzWebapp и Set-AzWebappSlot поддерживают свойства AlwaysOn, MinTls и FtpsState</span><span class="sxs-lookup"><span data-stu-id="d29f3-1829">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="d29f3-1830">Устранение проблемы, при которой параметр HttpsOnly с одновременным изменением AppservicePlan с помощью одной команды Set-AzWebApp сбрасывал значение HttpsOnly до значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d29f3-1830">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="d29f3-1831">3.3.0 — январь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1831">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d29f3-1832">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d29f3-1832">Az.Accounts</span></span>
* <span data-ttu-id="d29f3-1833">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment: теперь они принимают параметры AzureAttestationServiceEndpointResourceId и AzureAttestationServiceEndpointSuffix.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1833">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d29f3-1834">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d29f3-1834">Az.Cdn</span></span>
* <span data-ttu-id="d29f3-1835">Теперь в командлете New-AzCdnEndpoint отображаются сведения из сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1835">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d29f3-1836">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-1836">Az.Compute</span></span>
* <span data-ttu-id="d29f3-1837">Командлет Set-AzVMCustomScriptExtension исправлен для виртуальной машины с управляемым диском ОС без профиля ОС.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1837">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="d29f3-1838">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d29f3-1838">Az.ContainerInstance</span></span>
* <span data-ttu-id="d29f3-1839">Исправлены имена параметров, используемые в примере командлета New-AzContainerGroup.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1839">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="d29f3-1840">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="d29f3-1840">Az.DataBoxEdge</span></span>
* <span data-ttu-id="d29f3-1841">Добавлен командлет Get-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1841">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="d29f3-1842">получение контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1842">Get the Edge Storage Container</span></span>
* <span data-ttu-id="d29f3-1843">Добавлен командлет New-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1843">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="d29f3-1844">создание контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1844">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="d29f3-1845">Добавлен командлет Remove-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1845">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="d29f3-1846">удаление контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1846">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="d29f3-1847">Добавлен командлет Invoke-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1847">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="d29f3-1848">вызов действия для обновления данных в контейнере хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1848">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="d29f3-1849">Добавлен командлет Get-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1849">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="d29f3-1850">получение учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1850">Get the Edge Storage Account</span></span>
* <span data-ttu-id="d29f3-1851">Добавлен командлет New-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1851">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="d29f3-1852">создание учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1852">Create new Edge Storage Account</span></span>
* <span data-ttu-id="d29f3-1853">Добавлен командлет Remove-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1853">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="d29f3-1854">удаление учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1854">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="d29f3-1855">Вызов командлета Invoke-AzDataBoxEdgeShare:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1855">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="d29f3-1856">вызов действия для обновления данных в общей папке.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1856">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="d29f3-1857">Добавлен командлет Set-AzDataBoxEdgeStorageAccountCredential:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1857">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="d29f3-1858">установка учетных данных для учетной записи хранилища Azure Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1858">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d29f3-1859">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d29f3-1859">Az.DataFactory</span></span>
* <span data-ttu-id="d29f3-1860">Добавлены свойства AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId и VersionStatus для командлета Get-AzDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1860">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="d29f3-1861">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.6.0.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1861">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="d29f3-1862">Для командлета Set-AzureRmDataFactoryV2IntegrationRuntime добавлен параметр PublicIPs, позволяющий включить создание среды Azure-SSIS IR со статическими общедоступными IP-адресами.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1862">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="d29f3-1863">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="d29f3-1863">Az.DevTestLabs</span></span>
* <span data-ttu-id="d29f3-1864">Удалена недействительная ссылка в файле Get-AzDtlAllowedVMSizesPolicy.md.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1864">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d29f3-1865">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d29f3-1865">Az.EventHub</span></span>
* <span data-ttu-id="d29f3-1866">Устранена проблема № 10634: исправлена ссылка на пустой объект для удаления пространства имен концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1866">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d29f3-1867">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d29f3-1867">Az.HDInsight</span></span>
* <span data-ttu-id="d29f3-1868">Устранена ошибка в файле Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1868">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="d29f3-1869">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="d29f3-1869">Az.MachineLearning</span></span>
* <span data-ttu-id="d29f3-1870">Вычислительная среда Машинного обучения больше недоступна, поэтому удалены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1870">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="d29f3-1871">Get-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1871">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="d29f3-1872">Get-AzMlOpClusterKey;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1872">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="d29f3-1873">New-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1873">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="d29f3-1874">Remove-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1874">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="d29f3-1875">Set-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1875">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="d29f3-1876">Test-AzMlOpClusterSystemServicesUpdateAvailability;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1876">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="d29f3-1877">Update-AzMlOpClusterSystemService.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1877">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d29f3-1878">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d29f3-1878">Az.Network</span></span>
* <span data-ttu-id="d29f3-1879">Обновлена зависимость Microsoft.Azure.Management.Sql от предварительной версии 1.36 до предварительной версии 1.37.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1879">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d29f3-1880">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-1880">Az.RecoveryServices</span></span>
* <span data-ttu-id="d29f3-1881">Добавлена поддержка Azure Site Recovery для виртуальных машин с управляемым диском, зашифрованных при хранении с помощью управляемых клиентом ключей, при восстановлении из Azure в поставщике Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1881">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="d29f3-1882">Добавлена поддержка Azure Site Recovery для необязательного ввода идентификатора набора шифрования диска при включении защиты в рамках восстановления из VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1882">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="d29f3-1883">Добавлена поддержка Azure Site Recovery для необязательного ввода идентификатора набора шифрования диска на уровне диска при включении защиты в рамках восстановления из VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1883">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="d29f3-1884">Добавлена поддержка Azure Site Recovery для обновления элемента, защищенного репликацией, путем сопоставления набора шифрования диска при восстановлении из HyperV в Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1884">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d29f3-1885">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-1885">Az.Resources</span></span>
* <span data-ttu-id="d29f3-1886">Исправлена ошибка в справочном документе о командлете Remove-AzTag.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1886">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="d29f3-1887">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-1887">Az.Sql</span></span>
* <span data-ttu-id="d29f3-1888">Исправлена функция основных командлетов установки оценки уязвимостей: теперь она позволяет работать с базой данных master для базы данных Azure и ограничить ее в системных базах данных управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1888">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="d29f3-1889">Устранена ошибка, возникающая при создании группы отработки отказа экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1889">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="d29f3-1890">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d29f3-1890">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="d29f3-1891">Добавлен новый допустимый тип лицензии: DR (аварийное восстановление).</span><span class="sxs-lookup"><span data-stu-id="d29f3-1891">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d29f3-1892">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d29f3-1892">Az.Storage</span></span>
* <span data-ttu-id="d29f3-1893">Добавлено предупреждающее сообщение о критическом изменении значения DefaultAction в следующем выпуске:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1893">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="d29f3-1894">Update-AzStorageAccountNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1894">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="d29f3-1895">Включена поддержка получения времени последней синхронизации учетной записи хранения путем выполнения командлета Get-AzureRmStorageAccount с параметром -IncludeGeoReplicationStats:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1895">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="d29f3-1896">Get-AzureRmStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1896">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="d29f3-1897">3.2.0 — декабрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1897">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="d29f3-1898">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="d29f3-1898">General</span></span>
* <span data-ttu-id="d29f3-1899">Обновление ссылок в .psd1 для использования относительного пути для всех модулей.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1899">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d29f3-1900">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d29f3-1900">Az.Accounts</span></span>
* <span data-ttu-id="d29f3-1901">Установка правильного параметра UserAgent для телеметрии на стороне клиента для Az 4.0 (предварительная версия).</span><span class="sxs-lookup"><span data-stu-id="d29f3-1901">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="d29f3-1902">Отображение понятного пользователю сообщения об ошибке, если в Az 4.0 (предварительная версия) не указан контекст.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1902">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d29f3-1903">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d29f3-1903">Az.Batch</span></span>
* <span data-ttu-id="d29f3-1904">Исправлена проблема [№ 10602](https://github.com/Azure/azure-powershell/issues/10602), из-за которой использование командлета **New-AzBatchPool** приводило к неправильной отправке VirtualMachineConfiguration.ContainerConfiguration или VirtualMachineConfiguration.DataDisks на сервер.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1904">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d29f3-1905">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d29f3-1905">Az.DataFactory</span></span>
* <span data-ttu-id="d29f3-1906">Обновление пакета SDK Фабрики данных для .NET до версии 4.5.0.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1906">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d29f3-1907">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d29f3-1907">Az.FrontDoor</span></span>
* <span data-ttu-id="d29f3-1908">Включена поддержка исключений управляемых правил WAF.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1908">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="d29f3-1909">Добавление SocketAddr в список автозавершения.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1909">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="d29f3-1910">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="d29f3-1910">Az.HealthcareApis</span></span>
* <span data-ttu-id="d29f3-1911">Обработка исключений.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1911">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d29f3-1912">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d29f3-1912">Az.KeyVault</span></span>
* <span data-ttu-id="d29f3-1913">Исправлена ошибка при получении доступа к значению, которое может быть не задано.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1913">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="d29f3-1914">Управление сертификатами шифрования на основе эллиптических кривых.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1914">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="d29f3-1915">Включена возможность указания кривой для политик сертификатов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1915">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d29f3-1916">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d29f3-1916">Az.Monitor</span></span>
* <span data-ttu-id="d29f3-1917">Добавление необязательного аргумента в команду добавления параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1917">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="d29f3-1918">Существующий аргумент switch указывает на то, что экспорт в Log Analytics должен выполняться в фиксированную схему</span><span class="sxs-lookup"><span data-stu-id="d29f3-1918">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="d29f3-1919">(выделенный тип данных).</span><span class="sxs-lookup"><span data-stu-id="d29f3-1919">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d29f3-1920">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d29f3-1920">Az.Network</span></span>
* <span data-ttu-id="d29f3-1921">В приложении AzureFirewall, NAT и сетевых правилах включена поддержка IpGroups.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1921">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d29f3-1922">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-1922">Az.Resources</span></span>
* <span data-ttu-id="d29f3-1923">Устранена проблема, из-за которой при развертывании шаблона не удавалось считать его параметр, если имя параметра конфликтовало с именем встроенного параметра.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1923">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="d29f3-1924">Обновлены командлеты политики для использования новой версии API 2019-09-01 с поддержкой группирования в определениях наборов политик.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1924">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="d29f3-1925">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-1925">Az.Sql</span></span>
* <span data-ttu-id="d29f3-1926">Обновлена функция автоматического создания расширенного хранилища для службы оценки уязвимостей в учетной записи StorageV2.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1926">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d29f3-1927">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d29f3-1927">Az.Storage</span></span>
* <span data-ttu-id="d29f3-1928">Включена поддержка создания маркера SAS на основе удостоверения контейнера и большого двоичного объекта с аутентификацией Oauth на основе контекста службы хранилища:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1928">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="d29f3-1929">New-AzStorageContainerSASToken;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1929">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="d29f3-1930">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="d29f3-1930">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="d29f3-1931">Отозвана поддержка ключей делегирования пользователя учетной записи хранения, а также всех маркеров SAS удостоверения:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1931">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="d29f3-1932">Revoke-AzStorageAccountUserDelegationKeys.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1932">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="d29f3-1933">Выполнено обновление до Microsoft.Azure.Management.Storage версии 14.2.0 для включения поддержки нового API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1933">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="d29f3-1934">Включена поддержка QuotaGiB (квота общего ресурса в ГиБ) для значений свыше 5120 в командлетах для работы с общими папками в плоскости управления и добавлен псевдоним Quota для параметра QuotaGiB.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1934">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="d29f3-1935">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1935">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="d29f3-1936">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="d29f3-1936">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="d29f3-1937">Добавлен псевдоним QuotaGiB для параметра Quota:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1937">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="d29f3-1938">Set-AzStorageShareQuota.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1938">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="d29f3-1939">Устранена проблема, из-за которой при использовании AzStorageContainerAcl могла очищаться хранимая политика доступа:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1939">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="d29f3-1940">Set-AzStorageContainerAcl.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1940">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="d29f3-1941">Версия 3.1.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1941">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d29f3-1942">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="d29f3-1942">Highlights since the last major release</span></span>
* <span data-ttu-id="d29f3-1943">Выпуск Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="d29f3-1943">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="d29f3-1944">Выпуск Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="d29f3-1944">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d29f3-1945">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-1945">Az.Compute</span></span>
* <span data-ttu-id="d29f3-1946">Функция повторного применения виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="d29f3-1946">VM Reapply feature</span></span>
    - <span data-ttu-id="d29f3-1947">Добавлен параметр повторного применения в командлет Set-AzVM.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1947">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="d29f3-1948">Функция AutomaticRepairs масштабируемого набора виртуальных машин:</span><span class="sxs-lookup"><span data-stu-id="d29f3-1948">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="d29f3-1949">Добавлены параметры EnableAutomaticRepair, AutomaticRepairGracePeriod и AutomaticRepairMaxInstanceRepairsPercent в следующие командлеты:   New-AzVmssConfig Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d29f3-1949">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="d29f3-1950">Включена поддержка образа из коллекции разных клиентов для New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1950">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="d29f3-1951">Добавлен фрагмент Spot в средство заполнения аргументов параметра Priority в командлетах New-AzVM, New-AzVMConfig и New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1951">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="d29f3-1952">Добавлены параметры DiskIOPSReadWrite и DiskMBpsReadWrite в командлет Add-AzVmssDataDisk.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1952">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="d29f3-1953">Изменен параметр SourceImageId командлета New-AzGalleryImageVersion на необязательный.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1953">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="d29f3-1954">Добавлены параметры OSDiskImage и DataDiskImage в командлет New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1954">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="d29f3-1955">Добавлен параметр HyperVGeneration в командлет New-AzGalleryImageDefinition.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1955">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="d29f3-1956">Добавлены параметры SkipExtensionsOnOverprovisionedVMs в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1956">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="d29f3-1957">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="d29f3-1957">Az.DataBoxEdge</span></span>
* <span data-ttu-id="d29f3-1958">Добавлен командлет `Get-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1958">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="d29f3-1959">Получение заказа.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1959">Get the Order</span></span>
* <span data-ttu-id="d29f3-1960">Добавлен командлет `New-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1960">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="d29f3-1961">Создание заказа.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1961">Create new Order</span></span>
* <span data-ttu-id="d29f3-1962">Добавлен командлет `Remove-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1962">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="d29f3-1963">Удаление заказа.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1963">Remove the Order</span></span>
* <span data-ttu-id="d29f3-1964">Изменен командлет `New-AzDataBoxEdgeShare`.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1964">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="d29f3-1965">Создание локальной общей папки.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1965">Now creates Local Share</span></span>
* <span data-ttu-id="d29f3-1966">Добавлен командлет `Set-AzDataBoxEdgeRole`.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1966">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="d29f3-1967">Сопоставление IotRole с общей папкой.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1967">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="d29f3-1968">Добавлен командлет `Invoke-AzDataBoxEdgeDevice`.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1968">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="d29f3-1969">Вызов проверки обновлений, скачивание обновления, установка обновления на устройстве.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1969">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="d29f3-1970">Добавлен командлет `Get-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1970">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="d29f3-1971">Получение сведений о триггерах.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1971">Gets the information about Triggers</span></span>
* <span data-ttu-id="d29f3-1972">Добавлен командлет `New-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1972">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="d29f3-1973">Создание триггеров.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1973">Create new Triggers</span></span>
* <span data-ttu-id="d29f3-1974">Добавлен командлет `Remove-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1974">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="d29f3-1975">Удаление триггеров.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1975">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d29f3-1976">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d29f3-1976">Az.DataFactory</span></span>
* <span data-ttu-id="d29f3-1977">Обновление пакета SDK Фабрики данных для .NET до версии 4.4.0.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1977">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="d29f3-1978">Добавлен параметр ExpressCustomSetup в командлет Set-AzureRmDataFactoryV2IntegrationRuntime для включения конфигураций установки и сторонних компонентов без использования настраиваемого скрипта установки.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1978">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d29f3-1979">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d29f3-1979">Az.DataLakeStore</span></span>
* <span data-ttu-id="d29f3-1980">Обновлена документация по Get-AzDataLakeStoreDeletedItem и Restore-AzDataLakeStoreDeletedItem.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1980">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d29f3-1981">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d29f3-1981">Az.EventHub</span></span>
* <span data-ttu-id="d29f3-1982">Исправлена проблема № 10301. Исправлен формат даты маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1982">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d29f3-1983">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d29f3-1983">Az.FrontDoor</span></span>
* <span data-ttu-id="d29f3-1984">Добавлен параметр MinimumTlsVersion в Enable-AzFrontDoorCustomDomainHttps и New-AzFrontDoorFrontendEndpointObject.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1984">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="d29f3-1985">Добавлены параметры HealthProbeMethod и EnabledState в New-AzFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1985">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="d29f3-1986">Добавлен новый командлет для создания объекта BackendPoolsSettings для передачи при создании и обновлении Front Door.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1986">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="d29f3-1987">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="d29f3-1987">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d29f3-1988">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d29f3-1988">Az.Network</span></span>
* <span data-ttu-id="d29f3-1989">Изменены примеры параметра FilterData Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1989">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="d29f3-1990">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="d29f3-1990">Az.PrivateDns</span></span>
* <span data-ttu-id="d29f3-1991">Пакет SDK PrivateDns для .NET обновлен до версии 1.0.0</span><span class="sxs-lookup"><span data-stu-id="d29f3-1991">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d29f3-1992">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-1992">Az.RecoveryServices</span></span>
* <span data-ttu-id="d29f3-1993">Включена поддержка Azure Site Recovery для выбора типа диска при включении защиты.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1993">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="d29f3-1994">Внесено исправление Azure Site Recovery для изменения действия плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1994">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="d29f3-1995">Включена поддержка восстановления SQL Azure Backup для принятия баз данных файлового потока.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1995">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="d29f3-1996">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d29f3-1996">Az.RedisCache</span></span>
* <span data-ttu-id="d29f3-1997">Добавлен параметр MinimumTlsVersion в командлеты New-AzRedisCache и Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1997">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="d29f3-1998">Кроме того, добавлен параметр MinimumTlsVersion в выходные данные командлета Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1998">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="d29f3-1999">Добавлена проверка параметра -Size для командлетов Set-AzRedisCache и New-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="d29f3-1999">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="d29f3-2000">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-2000">Az.Resources</span></span>
- <span data-ttu-id="d29f3-2001">Обновлены командлеты политики для использования новой версии API 2019-06-01 с новым свойством EnforcementMode в назначении политики.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2001">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="d29f3-2002">Обновлен пример справки по созданию определения политики</span><span class="sxs-lookup"><span data-stu-id="d29f3-2002">Updated create policy definition help example</span></span>
- <span data-ttu-id="d29f3-2003">Исправлена ошибка с параметром -ServicePrincipalName командлета Remove-AZADServicePrincipal с возвратом пустой ссылки, если имя субъекта службы не найдено.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2003">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="d29f3-2004">Исправлена ошибка с New-AZADServicePrincipal с возвратом пустой ссылки, если у клиента нет подписки.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2004">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="d29f3-2005">Изменен командлет New-AzAdServicePrincipal для добавления учетных данных только для связанного приложения.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2005">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="d29f3-2006">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-2006">Az.Sql</span></span>
* <span data-ttu-id="d29f3-2007">Добавлена поддержка ReadReplicaCount для базы данных.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2007">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="d29f3-2008">Исправлена ошибка с Set-AzSqlDatabase, если избыточность в пределах зоны не настроена.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2008">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="d29f3-2009">Версия 3.0.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2009">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="d29f3-2010">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="d29f3-2010">General</span></span>
* <span data-ttu-id="d29f3-2011">Выпущена версия Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="d29f3-2011">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d29f3-2012">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d29f3-2012">Az.Accounts</span></span>
* <span data-ttu-id="d29f3-2013">Добавлено сообщение об устаревании для псевдонима "Resolve-Error".</span><span class="sxs-lookup"><span data-stu-id="d29f3-2013">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="d29f3-2014">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="d29f3-2014">Az.Advisor</span></span>
* <span data-ttu-id="d29f3-2015">Добавлена новая категория Operational Excellence (Эффективность работы) в командлет Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2015">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d29f3-2016">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d29f3-2016">Az.Batch</span></span>
* <span data-ttu-id="d29f3-2017">`CoreQuota` в `BatchAccountContext` переименован в `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2017">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="d29f3-2018">Также появился новый `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2018">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="d29f3-2019">Это влияет на **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2019">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="d29f3-2020">Параметр **New-AzBatchTask** `-ResourceFile` теперь принимает коллекцию объектов `PSResourceFile`, которые можно создать с помощью нового командлета **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2020">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="d29f3-2021">Новый командлет **New-AzBatchResourceFile**, который помогает создавать объекты `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2021">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="d29f3-2022">Их можно передавать в **New-AzBatchTask** в параметре `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2022">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="d29f3-2023">Это позволяет поддерживать два новых типа файлов ресурсов, которые дополняют существующий метод `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2023">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="d29f3-2024">Файлы ресурсов на основе `AutoStorageContainerName` скачивают весь контейнер автоматического хранения в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2024">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="d29f3-2025">Файлы ресурсов на основе `StorageContainerUrl` скачивают указанный в URL-адресе контейнер в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2025">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="d29f3-2026">Удалено свойство `ApplicationPackages` в `PSApplication`, который возвращается из **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2026">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="d29f3-2027">Отдельные пакеты в приложении теперь можно извлечь с помощью **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2027">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="d29f3-2028">Например: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2028">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="d29f3-2029">`ApplicationId` переименован в `ApplicationName` для **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** и **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2029">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="d29f3-2030">Теперь `ApplicationId` является псевдонимом для `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2030">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="d29f3-2031">Добавлено новое свойство `PSWindowsUserConfiguration` в `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2031">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="d29f3-2032">`Version` переименован в `Name` для `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2032">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="d29f3-2033">`BlobSource` переименован в `HttpUrl` для `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2033">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="d29f3-2034">Удалено свойство `OSDisk` из `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2034">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="d29f3-2035">Удалена операция **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2035">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="d29f3-2036">Больше она не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2036">This operation is no longer supported.</span></span>
* <span data-ttu-id="d29f3-2037">Удалено `TargetOSVersion` из `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2037">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="d29f3-2038">`CurrentOSVersion` переименован в `OSVersion` для `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2038">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="d29f3-2039">Удалено `DataEgressGiB` и `DataIngressGiB` из `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2039">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="d29f3-2040">Операция **Get-AzBatchNodeAgentSku** удалена и заменена на **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2040">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="d29f3-2041">**Get-AzBatchSupportedImage** возвращает те же данные, что и **Get-AzBatchNodeAgentSku**, но в более удобном формате.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2041">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="d29f3-2042">Также возвращаются новые непроверенные образы.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2042">New non-verified images are also now returned.</span></span> <span data-ttu-id="d29f3-2043">Включается и дополнительная информация о `Capabilities` и `BatchSupportEndOfLife` для каждого образа.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2043">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="d29f3-2044">Добавлена возможность монтировать файловые системы на каждом узле пула с помощью нового параметра `MountConfiguration` в **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2044">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="d29f3-2045">Теперь поддерживаются правила безопасности сети, которые блокируют сетевой доступ к пулу по исходящему порту трафика.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2045">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="d29f3-2046">Это выполняется с помощью свойства `SourcePortRanges` для `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2046">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="d29f3-2047">Что касается выполнения контейнеров, пакетная служба теперь поддерживает выполнение задачи в рабочей папке контейнера или рабочей папке задачи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2047">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="d29f3-2048">Выбор зависит от параметра `WorkingDirectory` в `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2048">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="d29f3-2049">Добавлена возможность указать коллекцию общедоступных IP-адресов для `PSNetworkConfiguration` с помощью нового свойства `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2049">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="d29f3-2050">Это гарантирует, что узлы в пуле будут иметь IP-адреса из списка, предоставленного пользователем.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2050">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="d29f3-2051">Если значение не задано, по умолчанию для `WaitForSuccess` в `PSSTartTask` используется значение `$True` (ранее `$False`).</span><span class="sxs-lookup"><span data-stu-id="d29f3-2051">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="d29f3-2052">Если значение не задано, по умолчанию для `Scope` в `PSAutoUserSpecification` используется значение `Pool` (ранее `Task` для Windows или `Pool` для Linux).</span><span class="sxs-lookup"><span data-stu-id="d29f3-2052">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d29f3-2053">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d29f3-2053">Az.Cdn</span></span>
* <span data-ttu-id="d29f3-2054">Добавлены UrlRewriteAction и CacheKeyQueryStringAction в RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2054">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="d29f3-2055">Исправлено несколько ошибок, таких как отсутствующий входной параметр Selector в командлете New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2055">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d29f3-2056">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-2056">Az.Compute</span></span>
* <span data-ttu-id="d29f3-2057">Функция набора шифрования диска</span><span class="sxs-lookup"><span data-stu-id="d29f3-2057">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="d29f3-2058">Новые командлеты:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="d29f3-2058">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="d29f3-2059">Добавлен параметр ProximityPlacementGroupId в следующие командлеты:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="d29f3-2059">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="d29f3-2060">Параметры DiskEncryptionSetId и EncryptionType добавлены в следующие командлеты:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="d29f3-2060">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="d29f3-2061">Добавлен параметр PublicIPAddressVersion в New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="d29f3-2061">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="d29f3-2062">FileUris для расширения пользовательских скриптов теперь будет защищенным, а не общедоступным параметром</span><span class="sxs-lookup"><span data-stu-id="d29f3-2062">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="d29f3-2063">Добавлено ScaleInPolicy в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d29f3-2063">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="d29f3-2064">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="d29f3-2064">Breaking changes</span></span>
    - <span data-ttu-id="d29f3-2065">Параметр UploadSizeInBytes применяется теперь вместо DiskSizeGB для New-AzDiskConfig, если CreateOption имеет значение Upload</span><span class="sxs-lookup"><span data-stu-id="d29f3-2065">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="d29f3-2066">PublishingProfile.Source.ManagedImage.Id заменяется на StorageProfile.Source.Id в объекте GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="d29f3-2066">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d29f3-2067">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d29f3-2067">Az.DataFactory</span></span>
* <span data-ttu-id="d29f3-2068">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.3.0.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2068">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d29f3-2069">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d29f3-2069">Az.DataLakeStore</span></span>
* <span data-ttu-id="d29f3-2070">Обновлен пакет SDK для ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), включает следующие исправления</span><span class="sxs-lookup"><span data-stu-id="d29f3-2070">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="d29f3-2071">Не создается исключение при невозможности десериализовать значение времени создания для записи в корзине или каталоге.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2071">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="d29f3-2072">Предоставляется параметр для времени ожидания запроса в adlsclient</span><span class="sxs-lookup"><span data-stu-id="d29f3-2072">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="d29f3-2073">Исправлена передача исходного значения syncflag для восстановления badoffset</span><span class="sxs-lookup"><span data-stu-id="d29f3-2073">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="d29f3-2074">Исправлена операция EnumerateDirectory, чтобы она извлекала токен продолжения после проверки ответа</span><span class="sxs-lookup"><span data-stu-id="d29f3-2074">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="d29f3-2075">Исправлена ошибка объединения</span><span class="sxs-lookup"><span data-stu-id="d29f3-2075">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d29f3-2076">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d29f3-2076">Az.FrontDoor</span></span>
* <span data-ttu-id="d29f3-2077">Исправлены разные опечатки в разных частях модуля</span><span class="sxs-lookup"><span data-stu-id="d29f3-2077">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d29f3-2078">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d29f3-2078">Az.HDInsight</span></span>
* <span data-ttu-id="d29f3-2079">Исправлена ошибка, из-за которой клиент получал сообщение об ошибке 'Not a valid Base-64 string' (Не является допустимой строкой Base64) при выполнении Get-AzHDInsightCluster для получения кластера с хранилищем ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2079">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="d29f3-2080">Добавлен параметр с именем ApplicationId в три командлета Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig и New-AzHDInsightCluster, чтобы клиент мог предоставить идентификатор приложения субъекта-службы для доступа к Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2080">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="d29f3-2081">Для Microsoft.Azure.Management.HDInsight изменена версия с 2.1.0 на 5.1.0</span><span class="sxs-lookup"><span data-stu-id="d29f3-2081">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="d29f3-2082">Удалены пять командлетов:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2082">Removed five cmdlets:</span></span>
    - <span data-ttu-id="d29f3-2083">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="d29f3-2083">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="d29f3-2084">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="d29f3-2084">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="d29f3-2085">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="d29f3-2085">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="d29f3-2086">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d29f3-2086">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="d29f3-2087">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d29f3-2087">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="d29f3-2088">Добавлены три командлета:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2088">Added three cmdlets:</span></span>
    - <span data-ttu-id="d29f3-2089">Get-AzHDInsightMonitoring заменяет собой Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2089">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="d29f3-2090">Enable-AzHDInsightMonitoring заменяет собой Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2090">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="d29f3-2091">Disable-AzHDInsightMonitoring заменяет собой Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2091">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="d29f3-2092">Исправлен командлет Get-AzHDInsightProperties, чтобы он поддерживал получение сведений о возможностях из определенного расположения.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2092">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="d29f3-2093">Удалены наборы параметров ("Spark1", "Spark2") из Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2093">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="d29f3-2094">Добавлены примеры в справочные документы по командлету Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2094">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="d29f3-2095">Изменен тип выходных данных для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2095">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="d29f3-2096">Для Get-AzHDInsightProperties тип выходных данных изменен с CapabilitiesResponse на AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2096">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="d29f3-2097">Для Remove-AzHDInsightCluster тип выходных данных изменен с ClusterGetResponse на bool.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2097">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="d29f3-2098">Для Set-AzHDInsightGatewaySettings тип выходных данных изменен с HttpConnectivitySettings на GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2098">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="d29f3-2099">Добавлены несколько условий для проверки сценариев.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2099">Added some scenario test cases.</span></span>
* <span data-ttu-id="d29f3-2100">Удалены несколько псевдонимов: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2100">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d29f3-2101">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d29f3-2101">Az.IotHub</span></span>
* <span data-ttu-id="d29f3-2102">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="d29f3-2102">Breaking changes:</span></span>
    - <span data-ttu-id="d29f3-2103">Командлет Add-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2103">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="d29f3-2104">Удален набор параметров __AllParameterSets для командлета Add-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2104">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="d29f3-2105">Командлет Get-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2105">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="d29f3-2106">Удален набор параметров __AllParameterSets для командлета Get-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2106">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="d29f3-2107">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2107">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="d29f3-2108">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2108">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="d29f3-2109">Командлет New-AzIotHubExportDevice больше не поддерживает псевдоним New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2109">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="d29f3-2110">Командлет New-AzIotHubImportDevice больше не поддерживает псевдоним New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2110">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="d29f3-2111">Командлет Remove-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2111">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="d29f3-2112">Удален набор параметров __AllParameterSets для командлета Remove-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2112">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="d29f3-2113">Командлет Set-AzIotHub теперь не поддерживает параметр OperationsMonitoringProperties и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2113">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="d29f3-2114">Удален набор параметров UpdateOperationsMonitoringProperties для командлета Set-AzIotHub.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2114">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d29f3-2115">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-2115">Az.RecoveryServices</span></span>
* <span data-ttu-id="d29f3-2116">Azure Site Recovery поддерживает настройку сетевых ресурсов, например групп безопасности сети, общедоступных IP-адресов и внутренних подсистем балансировки нагрузки из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2116">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="d29f3-2117">Azure Site Recovery поддерживает запись на управляемый диск из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2117">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="d29f3-2118">Azure Site Recovery поддерживает сокращение NIC из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2118">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="d29f3-2119">Azure Site Recovery поддерживает ускорение сети NIC из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2119">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="d29f3-2120">Azure Site Recovery поддерживает автоматическое обновление агента из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2120">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="d29f3-2121">Azure Site Recovery поддерживает стандартный SSD-накопитель из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2121">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="d29f3-2122">Azure Site Recovery поддерживает двухпроходное шифрование диска Azure из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2122">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="d29f3-2123">Azure Site Recovery поддерживает новый добавленный диск из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2123">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="d29f3-2124">Добавлена функция SoftDelete для виртуальных машин и соответствующие тесты</span><span class="sxs-lookup"><span data-stu-id="d29f3-2124">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="d29f3-2125">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-2125">Az.Resources</span></span>
* <span data-ttu-id="d29f3-2126">Обновлена сборка зависимостей Microsoft.Extensions.Caching.Memory с версии 1.1.1 до 2.2</span><span class="sxs-lookup"><span data-stu-id="d29f3-2126">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d29f3-2127">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d29f3-2127">Az.Network</span></span>
* <span data-ttu-id="d29f3-2128">Изменены все командлеты для PrivateEndpointConnection, чтобы они поддерживали универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2128">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="d29f3-2129">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2129">Updated cmdlet:</span></span>
        - <span data-ttu-id="d29f3-2130">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2130">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d29f3-2131">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2131">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d29f3-2132">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2132">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d29f3-2133">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2133">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d29f3-2134">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d29f3-2134">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="d29f3-2135">Добавлен новый командлет для PrivateLinkResource, который поддерживает универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2135">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="d29f3-2136">Новый командлет</span><span class="sxs-lookup"><span data-stu-id="d29f3-2136">New cmdlet:</span></span>
        - <span data-ttu-id="d29f3-2137">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="d29f3-2137">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="d29f3-2138">Добавлены новые поля и параметр для протокола прокси версии 2.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2138">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="d29f3-2139">Добавлено свойство EnableProxyProtocol в PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d29f3-2139">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="d29f3-2140">Добавлено свойство LinkIdentifier в PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d29f3-2140">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="d29f3-2141">Обновлен New-AzPrivateLinkService для поддержки нового необязательного параметра EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2141">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="d29f3-2142">Исправлено описание параметра в справочной документации по командлету New-AzApplicationGatewaySku.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2142">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="d29f3-2143">Новые командлеты для поддержки политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="d29f3-2143">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="d29f3-2144">Добавлена поддержка дочерних ресурсов RouteTables для VirtualHub</span><span class="sxs-lookup"><span data-stu-id="d29f3-2144">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="d29f3-2145">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2145">New cmdlets added:</span></span>
        - <span data-ttu-id="d29f3-2146">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="d29f3-2146">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="d29f3-2147">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="d29f3-2147">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="d29f3-2148">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="d29f3-2148">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="d29f3-2149">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="d29f3-2149">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="d29f3-2150">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="d29f3-2150">Set-AzVirtualHub</span></span>
* <span data-ttu-id="d29f3-2151">Добавлена поддержка новых свойств SKU для VirtualHub и VirtualWANType в VirtualWan</span><span class="sxs-lookup"><span data-stu-id="d29f3-2151">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="d29f3-2152">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2152">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="d29f3-2153">New-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="d29f3-2153">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="d29f3-2154">Update-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="d29f3-2154">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="d29f3-2155">New-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="d29f3-2155">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="d29f3-2156">Update-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="d29f3-2156">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="d29f3-2157">Добавлена поддержка свойства EnableInternetSecurity для HubVnetConnection, VpnConnection и ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="d29f3-2157">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="d29f3-2158">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2158">New cmdlets added:</span></span>
        - <span data-ttu-id="d29f3-2159">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="d29f3-2159">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="d29f3-2160">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2160">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="d29f3-2161">New-AzureRmVirtualHubVnetConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="d29f3-2161">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="d29f3-2162">New-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="d29f3-2162">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="d29f3-2163">Update-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="d29f3-2163">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="d29f3-2164">New-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="d29f3-2164">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="d29f3-2165">Set-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="d29f3-2165">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="d29f3-2166">Добавлена поддержка настройки политики верхнего уровня WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="d29f3-2166">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="d29f3-2167">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2167">New cmdlets added:</span></span>
        - <span data-ttu-id="d29f3-2168">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="d29f3-2168">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="d29f3-2169">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="d29f3-2169">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="d29f3-2170">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="d29f3-2170">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="d29f3-2171">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="d29f3-2171">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="d29f3-2172">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="d29f3-2172">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="d29f3-2173">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="d29f3-2173">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="d29f3-2174">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2174">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="d29f3-2175">New-AzApplicationGatewayFirewallPolicy: добавлены параметры PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="d29f3-2175">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="d29f3-2176">Добавлена поддержка оператора Geo-Match для CustomRule</span><span class="sxs-lookup"><span data-stu-id="d29f3-2176">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="d29f3-2177">Добавлен параметр GeoMatch в оператор для FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="d29f3-2177">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="d29f3-2178">Добавлена поддержка политики брандмауэра perListener и perSite</span><span class="sxs-lookup"><span data-stu-id="d29f3-2178">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="d29f3-2179">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2179">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="d29f3-2180">New-AzApplicationGatewayHttpListener: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="d29f3-2180">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="d29f3-2181">New-AzApplicationGatewayPathRuleConfig: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="d29f3-2181">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="d29f3-2182">Исправлен учет регистра для требуемой подсети с именем AzureBastionSubnet в PSBastion</span><span class="sxs-lookup"><span data-stu-id="d29f3-2182">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="d29f3-2183">Поддержка полного доменного имени назначения в правилах сети и преобразованного полного доменного имени в правилах NAT для брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="d29f3-2183">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="d29f3-2184">Добавлена поддержка ресурсов верхнего уровня RouteTables для IpGroup</span><span class="sxs-lookup"><span data-stu-id="d29f3-2184">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="d29f3-2185">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2185">New cmdlets added:</span></span>
        - <span data-ttu-id="d29f3-2186">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="d29f3-2186">New-AzIpGroup</span></span>
        - <span data-ttu-id="d29f3-2187">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="d29f3-2187">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="d29f3-2188">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="d29f3-2188">Get-AzIpGroup</span></span>
        - <span data-ttu-id="d29f3-2189">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="d29f3-2189">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d29f3-2190">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d29f3-2190">Az.ServiceFabric</span></span>
* <span data-ttu-id="d29f3-2191">Удален командлет Add-AzServiceFabricApplicationCertificate, так как соответствующий сценарий выполняется командлетом Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2191">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="d29f3-2192">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-2192">Az.Sql</span></span>
* <span data-ttu-id="d29f3-2193">Добавлена поддержка восстановления удаленных баз данных в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2193">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="d29f3-2194">Из кода удалены старые командлеты аудита.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2194">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="d29f3-2195">Удалены нерекомендуемые псевдонимы:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2195">Removed deprecated aliases:</span></span>
* <span data-ttu-id="d29f3-2196">Get-AzSqlDatabaseIndexRecommendations (вместо него используйте Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="d29f3-2196">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="d29f3-2197">Get-AzSqlDatabaseRestorePoints (вместо него используйте Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="d29f3-2197">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="d29f3-2198">Удален командлет Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d29f3-2198">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="d29f3-2199">Удалены псевдонимы для нерекомендуемых командлетов параметров оценки уязвимостей</span><span class="sxs-lookup"><span data-stu-id="d29f3-2199">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="d29f3-2200">Командлеты расширенного обнаружения угроз объявлены устаревшими</span><span class="sxs-lookup"><span data-stu-id="d29f3-2200">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="d29f3-2201">Добавлены командлеты для отключения и включения рекомендаций о конфиденциальности для столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2201">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d29f3-2202">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d29f3-2202">Az.Storage</span></span>
* <span data-ttu-id="d29f3-2203">Поддержка включения большой общей папки при создании или обновлении учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="d29f3-2203">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="d29f3-2204">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d29f3-2204">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="d29f3-2205">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d29f3-2205">Set-AzStorageAccount</span></span>
* <span data-ttu-id="d29f3-2206">При закрытии или получении маркера файла пропускается проверка того, является ли входной путь файлом или каталогом, чтобы избежать сбоев при получении объектов в состоянии DeletePending.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2206">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="d29f3-2207">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="d29f3-2207">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="d29f3-2208">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="d29f3-2208">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="d29f3-2209">2.8.0 — октябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2209">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="d29f3-2210">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="d29f3-2210">General</span></span>
* <span data-ttu-id="d29f3-2211">Выпуск Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="d29f3-2211">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d29f3-2212">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d29f3-2212">Az.Accounts</span></span>
* <span data-ttu-id="d29f3-2213">Обновление телеметрии и перезаписи URL-адресов для созданных модулей, исправление для модульных тестов Windows.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2213">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d29f3-2214">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d29f3-2214">Az.ApiManagement</span></span>
* <span data-ttu-id="d29f3-2215">**Set-AzApiManagementApi** — в ApiVersionSet добавлена поддержка обновления API.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2215">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="d29f3-2216">исправлена проблема https://github.com/Azure/azure-powershell/issues/10068.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2216">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d29f3-2217">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d29f3-2217">Az.Automation</span></span>
* <span data-ttu-id="d29f3-2218">Исправлен командлет New-AzureAutomationSoftwareUpdateConfiguration для параметра перезагрузки Linux.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2218">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d29f3-2219">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d29f3-2219">Az.Batch</span></span>
* <span data-ttu-id="d29f3-2220">Командлет **Get-AzBatchNodeAgentSku** объявлен устаревшим и будет заменен на **Get-AzBatchSupportImage** в версии 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2220">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d29f3-2221">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-2221">Az.Compute</span></span>
* <span data-ttu-id="d29f3-2222">В командлеты New-AzVM и New-AzVmss добавлены параметры Priority, EvictionPolicy и MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2222">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="d29f3-2223">Исправлены предупреждающее сообщение для командлетов Add-AzVMAdditionalUnattendContent и Add-AzVMSshPublicKey и справочная документация по ним.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2223">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="d29f3-2224">Для Set-AzVMDiskEncryptionExtension исправлено исключение -skipVmBackup для виртуальных машин Linux с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2224">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="d29f3-2225">Исправлена ошибка при изменении параметров шифрования в Set-AzVMDiskEncryptionExtension, реализован двухэтапный сценарий.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2225">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d29f3-2226">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d29f3-2226">Az.DataFactory</span></span>
* <span data-ttu-id="d29f3-2227">Добавлены команды CRUD для потока данных Фабрики данных Azure версии 2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow и Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2227">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="d29f3-2228">Добавлены команды действий для сеанса отладки потока данных Фабрики данных Azure версии 2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand и Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2228">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="d29f3-2229">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.2.0.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2229">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d29f3-2230">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d29f3-2230">Az.DataLakeStore</span></span>
* <span data-ttu-id="d29f3-2231">Проверка учетной записи исправлена так, чтобы учетные записи, содержащие знак "-", можно было передавать без домена.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2231">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="d29f3-2232">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="d29f3-2232">Az.HealthcareApis</span></span>
* <span data-ttu-id="d29f3-2233">Версия PowerShell обновлена до 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2233">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="d29f3-2234">Версия пакета SDK обновлена до 1.0.2.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2234">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="d29f3-2235">В тестах обновлены ссылки на новую версию пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2235">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="d29f3-2236">Вложенная выходная структура заменена на плоскую.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2236">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d29f3-2237">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d29f3-2237">Az.IotHub</span></span>
* <span data-ttu-id="d29f3-2238">Добавлен новый источник маршрутизации DigitalTwinChangeEvents.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2238">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="d29f3-2239">Исправлены незначительные ошибки: Get-AzIothub не возвращает subscriptionId.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2239">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d29f3-2240">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d29f3-2240">Az.Monitor</span></span>
* <span data-ttu-id="d29f3-2241">Добавлены новые получатели групп действий: -ItsmReceiver, -VoiceReceiver, -ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2241">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="d29f3-2242">Для получателей включите общую схему оповещений.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2242">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="d29f3-2243">Это не касается получателей SMS, push-уведомлений приложения Azure, ITSM и голосовых сообщений.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2243">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="d29f3-2244">Веб-перехватчики теперь поддерживают аутентификацию Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2244">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d29f3-2245">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d29f3-2245">Az.Network</span></span>
* <span data-ttu-id="d29f3-2246">Добавлен новый командлет Get-AzAvailableServiceAlias, позволяющий получить псевдонимы для политик конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2246">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="d29f3-2247">В подключениях шлюза виртуальной сети появилась возможность добавлять селекторы трафика.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2247">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="d29f3-2248">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2248">New cmdlets added:</span></span>
        - <span data-ttu-id="d29f3-2249">New-AzureRmTrafficSelectorPolicy.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2249">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="d29f3-2250">В командлеты добавлены необязательные параметры -TrafficSelectorPolicies, -New-AzureRmVirtualNetworkGatewayConnection, -Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2250">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="d29f3-2251">В конфигурациях правил сетевой безопасности добавлена поддержка протоколов ESP и AH.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2251">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="d29f3-2252">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2252">Updated cmdlets:</span></span>
        - <span data-ttu-id="d29f3-2253">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2253">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="d29f3-2254">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2254">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="d29f3-2255">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2255">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="d29f3-2256">Улучшена обработка исключений в командлетах Cortex.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2256">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="d29f3-2257">Выпущены новые поколения и номера SKU VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2257">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="d29f3-2258">Представлены новые поколения VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2258">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="d29f3-2259">Представлены новые номера SKU VirtualNetworkGateways с высокой пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2259">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="d29f3-2260">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d29f3-2260">Az.RedisCache</span></span>
* <span data-ttu-id="d29f3-2261">В справочную документацию по Set-AzRedisCache добавлены недостающие значения для параметра -Size.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2261">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="d29f3-2262">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-2262">Az.Sql</span></span>
* <span data-ttu-id="d29f3-2263">Добавлена возможность назначать администратора Active Directory в Управляемом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2263">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d29f3-2264">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d29f3-2264">Az.Storage</span></span>
* <span data-ttu-id="d29f3-2265">Клиентская библиотека службы хранилища Azure обновлена до версии 11.1.0.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2265">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="d29f3-2266">NextPageLink теперь позволяет получить список контейнеров с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2266">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="d29f3-2267">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d29f3-2267">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="d29f3-2268">NextPageLink теперь позволяет получить список учетных записей хранения из подписки.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2268">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="d29f3-2269">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d29f3-2269">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="d29f3-2270">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="d29f3-2270">Az.StorageSync</span></span>
* <span data-ttu-id="d29f3-2271">Исправлена проблема 9810 с Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2271">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d29f3-2272">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d29f3-2272">Az.Websites</span></span>
* <span data-ttu-id="d29f3-2273">Обновление плана службы приложений с помощью Set-AzWebApp приводило к сбою приложения.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2273">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="d29f3-2274">2.7.0 — сентябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2274">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="d29f3-2275">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d29f3-2275">Az.ApiManagement</span></span>
* <span data-ttu-id="d29f3-2276">В справочной документации по командлету Set-AzApiManagementPolicy обновлено описание параметра -Format.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2276">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="d29f3-2277">Из справочной документации удалены ссылки на нерекомендуемый командлет Update-AzApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2277">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="d29f3-2278">Вместо него следует использовать командлет Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2278">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d29f3-2279">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d29f3-2279">Az.Automation</span></span>
* <span data-ttu-id="d29f3-2280">В справочной документации по командлету Register-AzAutomationDscNode исправлена опечатка в примере.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2280">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="d29f3-2281">Добавлено уточнение об ограничениях ОС для командлета Register-AzAutomationDSCNode.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2281">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="d29f3-2282">Исправлено исключение пустой ссылки для параметра -Wait в командлете Start-AzAutomationRunbook.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2282">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d29f3-2283">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-2283">Az.Compute</span></span>
* <span data-ttu-id="d29f3-2284">Добавлен параметр UploadSizeInBytes для командлета New-AzDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2284">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="d29f3-2285">Добавлен добавочный параметр для командлета New-AzSnapshotConfig.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2285">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="d29f3-2286">Для виртуальной машины добавлены такие функции с низким приоритетом:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2286">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="d29f3-2287">Для командлета New-AzVMConfig добавлены параметры MaxPrice, EvictionPolicy и Priority.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2287">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="d29f3-2288">Для командлетов New-AzVmssConfig, Update-AzVM и Update-AzVmss добавлен параметр MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2288">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="d29f3-2289">Для командлета Get-AzAvailabilitySet устранена проблема со ссылкой на виртуальную машину, когда в нем перечисляются все группы доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2289">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="d29f3-2290">Исправлено исключение NULL для командлета Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2290">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="d29f3-2291">Исправлен метод поиска VHD для относительной конечной позиции.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2291">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="d29f3-2292">Устранена проблема с UltraSSD для командлетов New-AzVM и Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2292">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d29f3-2293">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d29f3-2293">Az.DataFactory</span></span>
* <span data-ttu-id="d29f3-2294">Добавлены 3 новые команды для ADF версии 2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription и Get-AzDataFactoryV2TriggerSubscriptionStatus.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2294">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="d29f3-2295">Пакет SDK ADF для .NET обновлен до версии 4.1.3.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2295">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d29f3-2296">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d29f3-2296">Az.HDInsight</span></span>
* <span data-ttu-id="d29f3-2297">Укажите критические изменения.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2297">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d29f3-2298">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d29f3-2298">Az.IotHub</span></span>
* <span data-ttu-id="d29f3-2299">Добавлена поддержка для вызова отработки отказа для IotHub в георегион аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2299">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="d29f3-2300">Добавлена поддержка для управления обогащением сообщений для IotHub.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2300">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="d29f3-2301">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2301">New cmdlets are:</span></span>
    - <span data-ttu-id="d29f3-2302">Add-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="d29f3-2302">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="d29f3-2303">Get-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="d29f3-2303">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="d29f3-2304">Remove-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="d29f3-2304">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="d29f3-2305">Set-AzIotHubMessageEnrichment.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2305">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d29f3-2306">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d29f3-2306">Az.Monitor</span></span>
* <span data-ttu-id="d29f3-2307">Указание на самую последнюю версию пакета SDK для монитора, т. е. 0.24.1-preview:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2307">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="d29f3-2308">В командлеты метрик добавлены некритические изменения, т. е. перечисление единиц поддерживает несколько новых значений.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2308">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="d29f3-2309">Эти командлеты доступны только для чтения, поэтому входные данные командлетов не будут изменены.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2309">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="d29f3-2310">Актуальная версия API запросов **ActionGroups** — **2019-06-01**. До этого была версия **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2310">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="d29f3-2311">Тесты сценария обновлены в соответствии с этим изменением.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2311">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="d29f3-2312">В конструкторы классов **EmailReceiver** и **WebhookReceiver** добавлен один новый обязательный аргумент — логическое значение с именем **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2312">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="d29f3-2313">Сейчас для него установлено значение **false**, чтобы скрыть это критическое изменение от командлетов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2313">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="d29f3-2314">**Примечание**. Это временное изменение, которое должно быть подтверждено командой оповещения.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2314">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="d29f3-2315">Порядок аргументов для конструктора класса **Source** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2315">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="d29f3-2316">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2316">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="d29f3-2317">Порядок аргументов для конструктора класса **AlertingAction** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2317">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="d29f3-2318">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2318">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="d29f3-2319">Добавлена поддержка критериев динамического порога для оповещения метрики версии 2:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2319">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="d29f3-2320">New-AzMetricAlertRuleV2Criteria: теперь также позволяет создавать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2320">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="d29f3-2321">Add-AzMetricAlertRuleV2: теперь также позволяет принимать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2321">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="d29f3-2322">Добавлены усовершенствования в командлетах запланированных правил запросов (SQR).</span><span class="sxs-lookup"><span data-stu-id="d29f3-2322">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="d29f3-2323">Командлеты будут принимать параметр Location в обоих форматах: расположение (например, eastus) или отображаемое имя расположения (например, "восточная часть США").</span><span class="sxs-lookup"><span data-stu-id="d29f3-2323">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="d29f3-2324">Параметр Enabled проиллюстрирован в файлах справки надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2324">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="d29f3-2325">Добавлены примеры для необязательного параметра ActionGroup.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2325">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="d29f3-2326">Все файлы справки улучшены.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2326">Overall improved help files</span></span>
* <span data-ttu-id="d29f3-2327">Исправлена ошибка в определении типа области для командлета Set-AzActionRule.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2327">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d29f3-2328">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d29f3-2328">Az.Network</span></span>
* <span data-ttu-id="d29f3-2329">Исправлен неправильный пример в справочной документации по командлету New-AzApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2329">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="d29f3-2330">В справочную документацию по командлету Get-AzNetworkWatcherPacketCapture добавлено примечание, посвященное извлечению всех свойств для записи пакетов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2330">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="d29f3-2331">В справочной документации по командлету Test-AzNetworkWatcherIPFlow исправлен пример: теперь он правильно перечисляет сетевые карты.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2331">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="d29f3-2332">Улучшен анализ облачных исключений для отображения дополнительных сведений (при их наличии).</span><span class="sxs-lookup"><span data-stu-id="d29f3-2332">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="d29f3-2333">Улучшен анализ облачных исключений для обработки дополнительного типа исключения SDK.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2333">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="d29f3-2334">Исправлено неправильное сопоставление моделей правил безопасности.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2334">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="d29f3-2335">Добавлены свойства сетевого интерфейса для компонента частного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2335">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="d29f3-2336">Для интерфейса PSNetworkInterface добавлено свойство PrivateEndpoint с типом PSResourceId.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2336">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="d29f3-2337">В PSNetworkInterfaceIPConfiguration добавлено свойство PrivateLinkConnectionProperties с типом PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2337">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="d29f3-2338">Добавлен новый класс модели: PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2338">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="d29f3-2339">Добавлен новый тип ApplicationRuleProtocolType "mssql" для ресурса Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2339">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="d29f3-2340">Поддержка многоканального подключения в Виртуальной глобальной сети:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2340">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="d29f3-2341">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="d29f3-2341">New cmdlets</span></span>
        - <span data-ttu-id="d29f3-2342">New-AzVpnSiteLink;</span><span class="sxs-lookup"><span data-stu-id="d29f3-2342">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="d29f3-2343">New-AzVpnSiteLinkConnection;</span><span class="sxs-lookup"><span data-stu-id="d29f3-2343">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="d29f3-2344">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2344">Updated cmdlet:</span></span>
        - <span data-ttu-id="d29f3-2345">New-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="d29f3-2345">New-VpnSite</span></span>
        - <span data-ttu-id="d29f3-2346">Update-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="d29f3-2346">Update-VpnSite</span></span>
        - <span data-ttu-id="d29f3-2347">New-VpnConnection;</span><span class="sxs-lookup"><span data-stu-id="d29f3-2347">New-VpnConnection</span></span>
        - <span data-ttu-id="d29f3-2348">Update-VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2348">Update-VpnConnection</span></span>
* <span data-ttu-id="d29f3-2349">Исправлены документы с некоторыми примерами PowerShell для использования командлетов AZ вместо командлетов AzureRM.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2349">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d29f3-2350">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-2350">Az.RecoveryServices</span></span>
* <span data-ttu-id="d29f3-2351">Для объекта AzureVMpolicy добавлен новый атрибут — ProtectedItemsCount.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2351">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="d29f3-2352">Добавлены тесты для политики виртуальной машины и восстановления исходной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2352">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="d29f3-2353">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-2353">Az.Resources</span></span>
* <span data-ttu-id="d29f3-2354">Исправлена ошибка, при которой не удавалось вызвать командлет New-AzRoleAssignment без параметра Scope.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2354">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d29f3-2355">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d29f3-2355">Az.ServiceFabric</span></span>
* <span data-ttu-id="d29f3-2356">Исправлена опечатка в примере в справочной документации по командлету Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2356">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="d29f3-2357">Добавлены новые командлеты для управления приложениями и службами:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2357">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="d29f3-2358">New-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="d29f3-2358">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="d29f3-2359">New-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="d29f3-2359">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="d29f3-2360">New-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="d29f3-2360">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="d29f3-2361">New-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="d29f3-2361">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="d29f3-2362">Update-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="d29f3-2362">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="d29f3-2363">Get-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="d29f3-2363">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="d29f3-2364">Get-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="d29f3-2364">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="d29f3-2365">Get-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="d29f3-2365">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="d29f3-2366">Get-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="d29f3-2366">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="d29f3-2367">Remove-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="d29f3-2367">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="d29f3-2368">Remove-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="d29f3-2368">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="d29f3-2369">Remove-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="d29f3-2369">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="d29f3-2370">Remove-AzServiceFabricServic.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2370">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="d29f3-2371">Пакет SDK для Service Fabric обновлен до версии 1.2.0, в которой используется версия API 2019-03-01 поставщика ресурсов Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2371">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="d29f3-2372">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="d29f3-2372">Az.SignalR</span></span>
* <span data-ttu-id="d29f3-2373">Добавлены командлеты Update, Restart, CheckNameAvailability и GetUsage.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2373">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="d29f3-2374">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-2374">Az.Sql</span></span>
* <span data-ttu-id="d29f3-2375">Обновлен пример в справочной документации по командлету Get-AzSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2375">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="d29f3-2376">Добавлен пример виртуального ядра для командлета создания эластичного пула (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="d29f3-2376">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="d29f3-2377">Удалена проверка свойства EmailAddresses и того, что свойство EmailAdmins правильное в случае, если свойство EmailAddresses пустое в командлетах Set-AzSqlServerAdvancedThreatProtectionPolicy и Set-AzSqlDatabaseAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2377">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="d29f3-2378">Теперь, если существует несколько параметров диагностики, включающих категорию аудита, параметры аудита сервера и базы данных удаляются.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2378">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="d29f3-2379">Исправлена проверка адресов электронной почты в нескольких командлетах оценки уязвимостей SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting и Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="d29f3-2379">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d29f3-2380">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d29f3-2380">Az.Storage</span></span>
* <span data-ttu-id="d29f3-2381">Обновлен пример в справочной документации по командлету Get-AzStorageAccountKey.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2381">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="d29f3-2382">Теперь при отправке и загрузке файла Azure в конечном файле сохраняются свойства SMB исходного файла (атрибуты файла, время создания файла, время последней записи файла).</span><span class="sxs-lookup"><span data-stu-id="d29f3-2382">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="d29f3-2383">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d29f3-2383">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="d29f3-2384">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d29f3-2384">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="d29f3-2385">Исправлена операция отправки блочного BLOB-объекта, в которой происходили сбои свойств и метаданных в контейнере с включенной ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2385">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="d29f3-2386">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d29f3-2386">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="d29f3-2387">Добавлена поддержка управления общими папками Azure в API плоскости управления с помощью таких командлетов:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2387">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="d29f3-2388">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="d29f3-2388">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="d29f3-2389">Get-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="d29f3-2389">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="d29f3-2390">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="d29f3-2390">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="d29f3-2391">Remove-AzRmStorageShare.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2391">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d29f3-2392">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d29f3-2392">Az.Websites</span></span>
* <span data-ttu-id="d29f3-2393">Устранена проблема, из-за которой теги webapp удалялись при переносе приложения в новый ASP.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2393">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="d29f3-2394">Теперь командлет Publish-AzureWebapp работает в Linux и Windows.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2394">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="d29f3-2395">Обновлен пример в справочной документации по командлету Get-AzWebAppPublishingProfile.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2395">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="d29f3-2396">2.6.0 — август 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2396">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="d29f3-2397">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="d29f3-2397">General</span></span>
* <span data-ttu-id="d29f3-2398">Исправлены опечатки в модулях.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2398">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d29f3-2399">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d29f3-2399">Az.Accounts</span></span>
* <span data-ttu-id="d29f3-2400">Добавлена поддержка назначаемого пользователем удостоверения MSI при проверке подлинности в Функциях Azure (№ 9479).</span><span class="sxs-lookup"><span data-stu-id="d29f3-2400">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="d29f3-2401">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="d29f3-2401">Az.Aks</span></span>
* <span data-ttu-id="d29f3-2402">Устранена проблема с выходными данными для Get-AzAks.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2402">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="d29f3-2403">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9847.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2403">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d29f3-2404">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d29f3-2404">Az.ApiManagement</span></span>
* <span data-ttu-id="d29f3-2405">исправлена проблема https://github.com/Azure/azure-powershell/issues/9351.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2405">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="d29f3-2406">Обновлена версия NuGet для .NET, которая не накладывает ограничений на productId, apiId, groupId и userId.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2406">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="d29f3-2407">**Get-AzApiManagementProduct**. Добавлена поддержка запросов к продуктам с помощью API.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2407">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="d29f3-2408">**New-AzApiManagementApiRevision**. Устранена проблема, из-за которой не задавался параметр ApiRevisionDescription при создании новой редакции API https://github.com/Azure/azure-powershell/issues/9752.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2408">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="d29f3-2409">Исправлено написание имени модели c PsApiManagementOAuth2AuthrozationServer на PsApiManagementOAuth2AuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2409">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d29f3-2410">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d29f3-2410">Az.Batch</span></span>
* <span data-ttu-id="d29f3-2411">Исправлена опечатка в написании Windows со строчной буквы в справочных сообщениях и документации.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2411">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d29f3-2412">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d29f3-2412">Az.Cdn</span></span>
* <span data-ttu-id="d29f3-2413">Исправлена опечатка во вспомогательном приложении модуля CDN.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2413">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d29f3-2414">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-2414">Az.Compute</span></span>
* <span data-ttu-id="d29f3-2415">Добавлен параметр VmssId в новый командлет Add New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2415">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="d29f3-2416">Добавлены параметры TerminateScheduledEvents и TerminateScheduledEventNotBeforeTimeoutInMinutes в New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2416">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="d29f3-2417">Добавлено свойство HyperVGeneration в объект образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2417">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="d29f3-2418">Добавлены компоненты Host и HostGroup.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2418">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="d29f3-2419">Новые командлеты:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="d29f3-2419">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="d29f3-2420">Параметр HostId добавлен в New-AzVMConfig и New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2420">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="d29f3-2421">Исправлен пример в документации по Invoke-AzVMRunCommand, в котором теперь используется правильное имя параметра.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2421">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="d29f3-2422">Исправлено описание VolumeType в справочной документации по Set-AzVMDiskEncryptionExtension и Set-AzVmssDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2422">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d29f3-2423">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d29f3-2423">Az.DataFactory</span></span>
* <span data-ttu-id="d29f3-2424">Исправлена опечатка в написании Windows со строчной буквы в документации по New-AzDataFactoryEncryptValue.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2424">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="d29f3-2425">Пакет SDK ADF для .NET обновлен до версии 4.1.2.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2425">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="d29f3-2426">Добавлены параметры DataProxyIntegrationRuntimeName, DataProxyStagingLinkedServiceName и DataProxyStagingPath в командлет Set-AzureRmDataFactoryV2IntegrationRuntime, что позволяет настраивать локальную среду выполнения интеграции в качестве прокси-сервера для Azure-SSIS Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2426">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="d29f3-2427">Обновлены PSTriggerRun для отображения активированных конвейеров, сообщений и свойств и PSActivityRun для отображения типа действия.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2427">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d29f3-2428">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d29f3-2428">Az.DataLakeStore</span></span>
* <span data-ttu-id="d29f3-2429">Устранена проблема, при которой Get-DataLakeStoreDeletedItem переставал отвечать на запросы при возникновении ошибок или удаленных исключений.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2429">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d29f3-2430">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d29f3-2430">Az.EventHub</span></span>
* <span data-ttu-id="d29f3-2431">Исправлена проблема № 9658: опечатка в написании параметра VirtualNteworkRule у Set-AzEventHubNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2431">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="d29f3-2432">Исправлена проблема № 9558: в Set-AzEventHubNamespace используется PATCH вместо PUT.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2432">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="d29f3-2433">В командлет Set-AzEventHubNamespace добавлен параметр EnableKafka.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2433">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="d29f3-2434">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2434">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="d29f3-2435">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="d29f3-2435">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="d29f3-2436">Исправлено написание Azure со строчной буквы.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2436">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d29f3-2437">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d29f3-2437">Az.Monitor</span></span>
* <span data-ttu-id="d29f3-2438">Исправлены неправильные имена параметров в справочной документации.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2438">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d29f3-2439">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d29f3-2439">Az.Network</span></span>
* <span data-ttu-id="d29f3-2440">Обновлен New-AzPrivateLinkServiceIpConfig.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2440">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="d29f3-2441">Параметр PublicIpAddress объявлен нерекомендуемым, так как он не используется на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2441">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="d29f3-2442">Добавлен необязательный параметр Primary, указывающий, является ли текущая IP-конфигурация основной.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2442">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="d29f3-2443">Улучшена обработка исключений из-за ошибок запроса от пакета SDK. Устранена проблема, при которой исключения пакета SDK не обрабатывались правильно, из-за чего не отображались основные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2443">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="d29f3-2444">Настроена логика проверки для префикса IPv6 IP-адреса для проверки правильности длины префикса IPv6.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2444">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="d29f3-2445">Обновлен Get-AzVirtualNetworkSubnetConfig: добавлен набор параметров для получения по идентификатору ресурса подсети.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2445">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="d29f3-2446">Обновлено описание параметра Location для AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2446">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d29f3-2447">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d29f3-2447">Az.OperationalInsights</span></span>
* <span data-ttu-id="d29f3-2448">Обновлена документация по New-AzOperationalInsightsLinuxSyslogDataSource.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2448">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="d29f3-2449">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2449">Added example</span></span>
    - <span data-ttu-id="d29f3-2450">Обновлено описание параметра -Name.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2450">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="d29f3-2451">Добавлен пример для New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="d29f3-2451">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="d29f3-2452">Изменено описание параметра -Name для New-AzOperationalInsightsWindowsEventDataSource.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2452">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d29f3-2453">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-2453">Az.RecoveryServices</span></span>
* <span data-ttu-id="d29f3-2454">Обновлен Get-AzRecoveryServicesBackupJobDetail.md.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2454">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="d29f3-2455">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-2455">Az.Resources</span></span>
* <span data-ttu-id="d29f3-2456">Добавлена поддержка новой версии API 2019-05-10 для Microsoft.Resource.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2456">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="d29f3-2457">Добавлена поддержка copy.count = 0 для переменных, ресурсов и свойств.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2457">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="d29f3-2458">Ресурсы, у которых condition = false или copy.count = 0, будут удаляться в полном режиме.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2458">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="d29f3-2459">В справочную документацию добавлен пример назначения политики на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2459">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d29f3-2460">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d29f3-2460">Az.ServiceBus</span></span>
* <span data-ttu-id="d29f3-2461">Исправлена проблема № 9658: опечатка в написании параметра VirtualNetworkRule В Set-AzServiceBusNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2461">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="d29f3-2462">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2462">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="d29f3-2463">Добавлена новая команда Test-AzServiceBusNameAvailability для проверки доступности имени для очереди и раздела.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2463">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d29f3-2464">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d29f3-2464">Az.ServiceFabric</span></span>
* <span data-ttu-id="d29f3-2465">Устранены ошибки командлета для добавления типа узла:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2465">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="d29f3-2466">ошибка NullReferenceException, возникавшая, если у группы ресурсов были другие VMSS, не связанные с кластером Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2466">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="d29f3-2467">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8681.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2467">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="d29f3-2468">Исправлена ошибка, из-за которой командлет завершился сбоем, если virtualNetwork находилась не в той группе ресурсов, к которой относится кластер.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2468">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="d29f3-2469">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8407.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2469">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="d29f3-2470">Командлет Add-AzServiceFabricApplicationCertificate объявлен нерекомендуемым.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2470">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="d29f3-2471">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-2471">Az.Sql</span></span>
* <span data-ttu-id="d29f3-2472">Обновление документации по старым командлетам аудита.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2472">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d29f3-2473">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d29f3-2473">Az.Storage</span></span>
* <span data-ttu-id="d29f3-2474">Обновлена справка по Get/Close-AzStorageFileHandle: в примеры добавлены сценарии использования командлетов и обновлено описание параметров.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2474">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="d29f3-2475">Добавлена поддержка StandardBlobTier в операции отправки BLOB-объекта и копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2475">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="d29f3-2476">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d29f3-2476">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="d29f3-2477">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="d29f3-2477">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="d29f3-2478">Добавлена поддержка приоритета восстановления в операцию копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2478">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="d29f3-2479">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="d29f3-2479">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d29f3-2480">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d29f3-2480">Az.Websites</span></span>
* <span data-ttu-id="d29f3-2481">Добавлены уточнение для параметра -AppSettings в Set-AzWebApp и Set-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2481">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="d29f3-2482">2.5.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2482">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d29f3-2483">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d29f3-2483">Az.Accounts</span></span>
* <span data-ttu-id="d29f3-2484">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2484">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="d29f3-2485">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="d29f3-2485">Az.ApplicationInsights</span></span>
* <span data-ttu-id="d29f3-2486">Исправлена опечатка в примере в документации по Remove-AzApplicationInsightsApiKey.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2486">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d29f3-2487">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d29f3-2487">Az.Automation</span></span>
* <span data-ttu-id="d29f3-2488">Исправлена опечатка в строке ресурса.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2488">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d29f3-2489">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-2489">Az.CognitiveServices</span></span>
* <span data-ttu-id="d29f3-2490">Добавлена поддержка NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2490">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d29f3-2491">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-2491">Az.Compute</span></span>
* <span data-ttu-id="d29f3-2492">Добавлены недостающие свойства (ComputerName, OsName, OsVersion и HyperVGeneration) для объекта представления экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2492">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="d29f3-2493">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d29f3-2493">Az.ContainerRegistry</span></span>
* <span data-ttu-id="d29f3-2494">Исправлена опечатка в Remove-AzContainerRegistryReplication для параметра репликации.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2494">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="d29f3-2495">См. подробнее: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2495">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d29f3-2496">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d29f3-2496">Az.DataFactory</span></span>
* <span data-ttu-id="d29f3-2497">Пакет SDK для ADF .NET обновлен до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2497">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="d29f3-2498">Исправлена опечатка в документации по Get-AzDataFactoryV2PipelineRun.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2498">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d29f3-2499">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d29f3-2499">Az.EventHub</span></span>
* <span data-ttu-id="d29f3-2500">Добавлен новый командлет для создания маркера SAS: New-AzEventHubAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2500">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="d29f3-2501">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="d29f3-2501">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d29f3-2502">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d29f3-2502">Az.KeyVault</span></span>
* <span data-ttu-id="d29f3-2503">Добавлена поддержка для настройки параметра KeySize в политиках сертификатов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2503">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d29f3-2504">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d29f3-2504">Az.LogicApp</span></span>
* <span data-ttu-id="d29f3-2505">Get-AzIntegrationAccountMap теперь надлежащим образом выводит все типы сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2505">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="d29f3-2506">Добавлен новый параметр MapType для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2506">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="d29f3-2507">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-2507">Az.ManagedServices</span></span>
* <span data-ttu-id="d29f3-2508">Добавлена поддержка API версии 2019-06-01 (общедоступная).</span><span class="sxs-lookup"><span data-stu-id="d29f3-2508">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d29f3-2509">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d29f3-2509">Az.Network</span></span>
* <span data-ttu-id="d29f3-2510">Добавлена поддержка частной конечной точки и службы приватного канала.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2510">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="d29f3-2511">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="d29f3-2511">New cmdlets</span></span>
        - <span data-ttu-id="d29f3-2512">Set-AzPrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2512">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="d29f3-2513">Set-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2513">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="d29f3-2514">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2514">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d29f3-2515">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2515">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d29f3-2516">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2516">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d29f3-2517">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2517">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d29f3-2518">Test-AzPrivateLinkServiceVisibility.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2518">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="d29f3-2519">Get-AzAutoApprovedPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2519">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="d29f3-2520">Обновлены следующие команды для функции: Флаг PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies в подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2520">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="d29f3-2521">Обновлены командлеты New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2521">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="d29f3-2522">Добавлен необязательный параметр -PrivateEndpointNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к частной конечной точке в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2522">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="d29f3-2523">Добавлен необязательный параметр -PrivateLinkServiceNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к службе приватного канала в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2523">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="d29f3-2524">Параметр ServiceName командлета AzPrivateLinkService был переименован на Name с псевдонимом ServiceName для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2524">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="d29f3-2525">Включен протокол ICMP для настройки правил безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2525">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="d29f3-2526">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="d29f3-2526">Updated cmdlets</span></span>
        - <span data-ttu-id="d29f3-2527">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2527">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="d29f3-2528">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2528">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="d29f3-2529">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2529">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="d29f3-2530">Добавлен ConnectionProtocolType (Ikev1/Ikev2) в качестве настраиваемого параметра для командлета New-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2530">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="d29f3-2531">Добавлен PrivateIpAddressVersion в LoadBalancerFrontendIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2531">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="d29f3-2532">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2532">Updated cmdlet:</span></span>
        - <span data-ttu-id="d29f3-2533">New-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2533">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="d29f3-2534">Add-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2534">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="d29f3-2535">Set-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2535">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="d29f3-2536">Команда New-AzApplicationGatewayProbeConfig Шлюза приложений обновлена для поддержки настраиваемого порта в зонде.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2536">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="d29f3-2537">Обновлен командлет New-AzApplicationGatewayProbeConfig: добавлен необязательный параметр Port, который используется при проверке внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2537">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="d29f3-2538">Этот параметр применяется к номерам SKU Standard_V2 и WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2538">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d29f3-2539">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d29f3-2539">Az.OperationalInsights</span></span>
* <span data-ttu-id="d29f3-2540">Обновленная версия по умолчанию для сохраненных операций поиска имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2540">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="d29f3-2541">Исправлены ошибки при обработке регулярных выражений со значениями NULL в журналах.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2541">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d29f3-2542">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-2542">Az.RecoveryServices</span></span>
* <span data-ttu-id="d29f3-2543">Обновлен файл Get-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2543">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="d29f3-2544">Обновлен файл Get-AzRecoveryServicesBackupContainer.md.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2544">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="d29f3-2545">Обновлен файл Get-AzRecoveryServicesVault.md.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2545">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="d29f3-2546">Обновлен файл Wait-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2546">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="d29f3-2547">Обновлен файл Set-AzRecoveryServicesVaultContext.md.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2547">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="d29f3-2548">Обновлен файл Get-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2548">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="d29f3-2549">Обновлен файл Get-AzRecoveryServicesBackupRecoveryPoint.md.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2549">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="d29f3-2550">Обновлен файл Restore-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2550">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="d29f3-2551">Обновлен вызов службы для отмены регистрации контейнера в общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2551">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="d29f3-2552">Обновлен файл Set-AzRecoveryServicesAsrAlertSetting.md.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2552">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="d29f3-2553">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-2553">Az.Resources</span></span>
- <span data-ttu-id="d29f3-2554">Удален отсутствующий командлет, который упоминается в документации по New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2554">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="d29f3-2555">Обновлены командлеты политик для использования новой версии API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2555">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d29f3-2556">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d29f3-2556">Az.ServiceBus</span></span>
* <span data-ttu-id="d29f3-2557">Добавлен новый командлет для создания маркера SAS: New-AzServiceBusAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2557">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="d29f3-2558">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="d29f3-2558">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="d29f3-2559">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-2559">Az.Sql</span></span>
* <span data-ttu-id="d29f3-2560">Исправлены отсутствующие примеры для командлета Set-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2560">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="d29f3-2561">Исправлены заданные повторяющиеся проверки для оценки наличия уязвимостей без указания адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2561">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="d29f3-2562">Исправлена незначительная опечатка в сообщении предупреждения.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2562">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d29f3-2563">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d29f3-2563">Az.Storage</span></span>
* <span data-ttu-id="d29f3-2564">Обновлен пример в справочной документации для использования командлетом Get-AzStorageAccount правильного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2564">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="d29f3-2565">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="d29f3-2565">Az.StorageSync</span></span>
* <span data-ttu-id="d29f3-2566">Добавлен командлет Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2566">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="d29f3-2567">Исправлена проблема № 9551, связанная с TierFilesOlderThanDays.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2567">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d29f3-2568">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d29f3-2568">Az.Websites</span></span>
* <span data-ttu-id="d29f3-2569">Исправлена ошибка, при которой некоторые свойства SiteConfig не возвращались Get-AzWebApp и Set-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2569">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="d29f3-2570">Добавлен новый параметр Location в Get-AzDeletedWebApp и Restore-AzDeletedWebApp.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2570">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="d29f3-2571">Исправлена ошибка, которая возникала при клонировании слотов веб-приложений с помощью командлета New-AzWebApp-IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2571">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="d29f3-2572">2.4.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2572">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d29f3-2573">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d29f3-2573">Az.Accounts</span></span>
* <span data-ttu-id="d29f3-2574">Добавлена поддержка командлетов профиля.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2574">Add support for profile cmdlets</span></span>
* <span data-ttu-id="d29f3-2575">Добавлена поддержка сред и плоскостей данных в созданных командлетах.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2575">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="d29f3-2576">Исправлена ошибка, когда в командлетах плоскости данных в Windows PowerShell в некоторых случаях использовалась неправильная конечная точка.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2576">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="d29f3-2577">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="d29f3-2577">Az.Advisor</span></span>
* <span data-ttu-id="d29f3-2578">Выпущена общедоступная версия Az.Advisor.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2578">GA release of Az.Advisor</span></span>
* <span data-ttu-id="d29f3-2579">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2579">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d29f3-2580">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d29f3-2580">Az.ApiManagement</span></span>
* <span data-ttu-id="d29f3-2581">исправлена проблема https://github.com/Azure/azure-powershell/issues/8671.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2581">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="d29f3-2582">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="d29f3-2582">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="d29f3-2583">Добавлена поддержка запрашивания подписок по пользователю и продукту.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2583">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="d29f3-2584">Добавлена поддержка создания запросов с использованием области "/", "/apis", "/apis/echo-api".</span><span class="sxs-lookup"><span data-stu-id="d29f3-2584">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="d29f3-2585">Исправлены проблемы https://github.com/Azure/azure-powershell/issues/9307 и https://github.com/Azure/azure-powershell/issues/8432.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2585">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="d29f3-2586">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="d29f3-2586">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="d29f3-2587">Добавлена поддержка указания ApiVersion и ApiVersionSetId при импорте API-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2587">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d29f3-2588">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d29f3-2588">Az.Automation</span></span>
* <span data-ttu-id="d29f3-2589">Исправлена ошибка командлета Set-AzAutomationConnectionFieldValue при обработке строкового значения.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2589">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d29f3-2590">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-2590">Az.Compute</span></span>
* <span data-ttu-id="d29f3-2591">В New AzImageConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2591">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d29f3-2592">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d29f3-2592">Az.DataFactory</span></span>
* <span data-ttu-id="d29f3-2593">Обновление выходных данных командлетов ADF, предназначенных для получения числа выполнений действий, конвейеров и триггеров, для поддержки канала Select-Object.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2593">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d29f3-2594">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d29f3-2594">Az.EventGrid</span></span>
* <span data-ttu-id="d29f3-2595">Исправлена опечатка в документации по командлету New-AzEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2595">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d29f3-2596">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d29f3-2596">Az.IotHub</span></span>
* <span data-ttu-id="d29f3-2597">Добавлена поддержка повторного создания ключей политики авторизации.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2597">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d29f3-2598">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d29f3-2598">Az.Network</span></span>
* <span data-ttu-id="d29f3-2599">К тегам общедоступного IP-адреса добавлен тег RoutingPreference.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2599">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="d29f3-2600">Улучшены примеры для справочной документации по командлету Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2600">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d29f3-2601">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d29f3-2601">Az.PolicyInsights</span></span>
* <span data-ttu-id="d29f3-2602">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2602">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="d29f3-2603">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9446.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2603">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d29f3-2604">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d29f3-2604">Az.OperationalInsights</span></span>
* <span data-ttu-id="d29f3-2605">Исправленная модель источника данных CustomLog возвращена в командлет Get-AzOperationalInsightsDataSource.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2605">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d29f3-2606">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-2606">Az.RecoveryServices</span></span>
* <span data-ttu-id="d29f3-2607">Выпущено исправление для команды get-policy для виртуальных машин IaaS.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2607">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="d29f3-2608">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-2608">Az.Resources</span></span>
    - <span data-ttu-id="d29f3-2609">Исправлен текст справки по параметру Get-AzPolicyState -Top.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2609">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="d29f3-2610">Добавлена поддержка разбиения по страницам на стороне клиента для Get-AzPolicyAlias.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2610">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="d29f3-2611">Добавлены новые параметры для Set-AzPolicyAssignment, -PolicyParameters и -PolicyParametersObject.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2611">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="d29f3-2612">Добавлен ряд обновлений документов и примеров для командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2612">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d29f3-2613">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d29f3-2613">Az.ServiceBus</span></span>
* <span data-ttu-id="d29f3-2614">Исправление ошибки № 4938: командлет New-AzureRmServiceBusQueue возвращает ответ BadRequest (Недопустимый запрос) при задании значения MaxSizeInMegabytes.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2614">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="d29f3-2615">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-2615">Az.Sql</span></span>
* <span data-ttu-id="d29f3-2616">Из выпуска предварительной версии в выпуск общедоступной версии добавлены командлеты группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2616">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="d29f3-2617">Поддержка аудита Azure SQL Server и баз данных с помощью новых командлетов:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2617">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="d29f3-2618">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="d29f3-2618">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="d29f3-2619">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="d29f3-2619">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="d29f3-2620">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="d29f3-2620">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="d29f3-2621">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="d29f3-2621">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="d29f3-2622">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="d29f3-2622">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="d29f3-2623">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="d29f3-2623">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="d29f3-2624">Из параметров оценки уязвимостей удалены ограничения, касающиеся электронной почты.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2624">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d29f3-2625">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d29f3-2625">Az.Storage</span></span>
* <span data-ttu-id="d29f3-2626">Два параметра в указанном ниже командлете — -IndexDocument и -ErrorDocument404Path, — которые ранее были обязательными, стали необязательными:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2626">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="d29f3-2627">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="d29f3-2627">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="d29f3-2628">Обновлена справка по командлету Get-AzStorageBlobContent: добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2628">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="d29f3-2629">При сбое выполнения командлета с ошибкой StorageException отображаются дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2629">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="d29f3-2630">Добавлена поддержка создания или обновления учетной записи хранения с использованием проверки подлинности AAD DS для службы "Файлы Azure".</span><span class="sxs-lookup"><span data-stu-id="d29f3-2630">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="d29f3-2631">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d29f3-2631">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="d29f3-2632">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d29f3-2632">Set-AzStorageAccount</span></span>
* <span data-ttu-id="d29f3-2633">Добавлена поддержка перечисления или закрытия дескрипторов файлов для общей папки, каталога файлов или файла:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2633">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="d29f3-2634">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="d29f3-2634">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="d29f3-2635">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="d29f3-2635">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="d29f3-2636">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="d29f3-2636">Az.StorageSync</span></span>
* <span data-ttu-id="d29f3-2637">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2637">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="d29f3-2638">2.3.2 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2638">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d29f3-2639">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d29f3-2639">Az.Accounts</span></span>
* <span data-ttu-id="d29f3-2640">Исправлена ошибка, связанная с использованием неправильного URL-адреса для вызовов функций.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2640">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="d29f3-2641">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8983.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2641">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="d29f3-2642">Устранена проблема с псевдонимами из AzureRM для командлетов Az.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2642">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="d29f3-2643">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2643">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="d29f3-2644">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2644">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d29f3-2645">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-2645">Az.Compute</span></span>
* <span data-ttu-id="d29f3-2646">Простые наборы параметров New-AzVm и New-AzVmss теперь принимают параметр ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2646">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="d29f3-2647">Исправлена опечатка в справочной документации по New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2647">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="d29f3-2648">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="d29f3-2648">Az.Dns</span></span>
* <span data-ttu-id="d29f3-2649">Исправлена опечатка в справочных примерах по использованию Set-AzDnsZone.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2649">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d29f3-2650">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d29f3-2650">Az.EventGrid</span></span>
* <span data-ttu-id="d29f3-2651">Обновлен для использования API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2651">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="d29f3-2652">Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2652">New cmdlets:</span></span>
    - <span data-ttu-id="d29f3-2653">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="d29f3-2653">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="d29f3-2654">Создает домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2654">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="d29f3-2655">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="d29f3-2655">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="d29f3-2656">Возвращает сведения о домене Сетки событий или список всех доменов Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2656">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="d29f3-2657">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="d29f3-2657">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="d29f3-2658">Удаляет домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2658">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="d29f3-2659">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="d29f3-2659">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="d29f3-2660">Повторно создает ключ общего доступа для домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2660">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="d29f3-2661">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="d29f3-2661">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="d29f3-2662">Возвращает ключи общего доступа, используемые для публикации событий в домене Сетки событий.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2662">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="d29f3-2663">New-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="d29f3-2663">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="d29f3-2664">Создает раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2664">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="d29f3-2665">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="d29f3-2665">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="d29f3-2666">Возвращает сведения о разделе домена Сетки событий или список всех разделов определенного домена Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2666">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="d29f3-2667">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="d29f3-2667">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="d29f3-2668">Удаляет раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2668">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="d29f3-2669">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2669">Updated cmdlets:</span></span>
    - <span data-ttu-id="d29f3-2670">New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="d29f3-2670">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="d29f3-2671">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для нового домена Сетки событий и раздела домена Сетки событий и позволяющие создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2671">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="d29f3-2672">Добавляют новые обязательные параметры для указания имени нового домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2672">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="d29f3-2673">Добавляют новые наборы параметров для доменов и разделов домена и позволяют повторно использовать существующие параметры (например, EndPointType, SubjectBeginsWith и т. д.).</span><span class="sxs-lookup"><span data-stu-id="d29f3-2673">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="d29f3-2674">Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2674">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="d29f3-2675">срока действия подписки на событие;</span><span class="sxs-lookup"><span data-stu-id="d29f3-2675">Event subscription expiration date,</span></span>
            - <span data-ttu-id="d29f3-2676">параметров расширенной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2676">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="d29f3-2677">Добавляют новое перечисление для ServiceBusQueue в качестве места назначения.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2677">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="d29f3-2678">Запрещают использование значение All в параметре -IncludedEventType и заменяют его следующим:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2678">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="d29f3-2679">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="d29f3-2679">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="d29f3-2680">Добавляют новые необязательные параметры (Top, ODataQuery и NextLink) для поддержки разбиения на страницы и фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2680">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="d29f3-2681">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="d29f3-2681">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="d29f3-2682">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для домена Сетки событий и раздела домена Сетки событий и позволяющие удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2682">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="d29f3-2683">Добавляют новые обязательные параметры для указания имени домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2683">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d29f3-2684">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d29f3-2684">Az.FrontDoor</span></span>
* <span data-ttu-id="d29f3-2685">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="d29f3-2685">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="d29f3-2686">Добавляет поддержку преобразований и новое значение оператора автозавершения (RegEx).</span><span class="sxs-lookup"><span data-stu-id="d29f3-2686">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="d29f3-2687">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="d29f3-2687">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="d29f3-2688">Добавляет новые значения автозавершения.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2688">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d29f3-2689">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d29f3-2689">Az.Network</span></span>
* <span data-ttu-id="d29f3-2690">Добавляет поддержку ресурса шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2690">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="d29f3-2691">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="d29f3-2691">New cmdlets</span></span>
        - <span data-ttu-id="d29f3-2692">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="d29f3-2692">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="d29f3-2693">Добавляет AvailablePrivateEndpointType.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2693">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="d29f3-2694">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="d29f3-2694">New cmdlets</span></span>
        - <span data-ttu-id="d29f3-2695">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="d29f3-2695">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="d29f3-2696">Добавляет PrivatePrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2696">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="d29f3-2697">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="d29f3-2697">New cmdlets</span></span>
        - <span data-ttu-id="d29f3-2698">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d29f3-2698">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="d29f3-2699">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d29f3-2699">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="d29f3-2700">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d29f3-2700">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="d29f3-2701">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d29f3-2701">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="d29f3-2702">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d29f3-2702">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="d29f3-2703">Добавляет PrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2703">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="d29f3-2704">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="d29f3-2704">New cmdlets</span></span>
        - <span data-ttu-id="d29f3-2705">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d29f3-2705">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="d29f3-2706">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d29f3-2706">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="d29f3-2707">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d29f3-2707">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="d29f3-2708">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="d29f3-2708">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="d29f3-2709">Обновлены следующие команды для функции: флаг UseLocalAzureIpAddress для VPN-подключения.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2709">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="d29f3-2710">Обновлен командлет New-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2710">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="d29f3-2711">Обновлен командлет Set-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2711">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="d29f3-2712">В пиринг ExpressRoute добавлено поле только для чтения PeeredConnections.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2712">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="d29f3-2713">В ExpressRoute добавлено поле только для чтения GlobalReachEnabled.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2713">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="d29f3-2714">Добавлен атрибут в рамках критического изменения, отменяющего статус устаревшего поля AllowGlobalReach в модели ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2714">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="d29f3-2715">Исправлена проблема, связанная с ошибкой 8756, при использовании TargetListenerID с командлетами AzApplicationGatewayRedirectConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2715">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="d29f3-2716">Исправлена ошибка в New-AzApplicationGatewayPathRuleConfig, не позволявшая задавать набор правил повторного создания.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2716">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="d29f3-2717">Исправлено отображение VirtualNetworkTaps в NetworkInterfaceIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2717">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="d29f3-2718">Исправлены командлеты Cortex Get для отображения всех частей.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2718">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="d29f3-2719">Исправлено создание ссылок VirtualHub для ExpressRouteGateways и VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2719">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="d29f3-2720">В AzureFirewall и NatGateway добавлена поддержка Зон доступности.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2720">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="d29f3-2721">Добавлен командлет Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2721">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="d29f3-2722">Добавлена поддержка нескольких общедоступных IP-адресов для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2722">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="d29f3-2723">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2723">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="d29f3-2724">Добавлен параметр -PublicIpAddress, который принимает один или несколько объектов общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2724">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="d29f3-2725">Добавлен параметр -VirtualNetwork, который принимает объект виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2725">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="d29f3-2726">Добавлены методы AddPublicIpAddress и RemovePublicIpAddress для объекта брандмауэра. Они принимают объект общедоступного IP-адреса в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2726">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="d29f3-2727">Не рекомендуется использовать параметры -PublicIpName и -VirtualNetworkName.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2727">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="d29f3-2728">Обновлены следующие команды для функции: В параметрах проверки подлинности AAD VPN-клиента задан ресурс шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2728">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="d29f3-2729">Обновлен командлет New-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2729">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="d29f3-2730">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2730">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="d29f3-2731">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр-переключатель RemoveAadAuthentication для удаления в шлюзе параметров проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2731">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d29f3-2732">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d29f3-2732">Az.OperationalInsights</span></span>
* <span data-ttu-id="d29f3-2733">Добавлена поддержка SKU **pergb2018** в команде New-AzureRmOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2733">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="d29f3-2734">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-2734">Az.Resources</span></span>
* <span data-ttu-id="d29f3-2735">Поддержка дополнительных вариантов экспорта шаблона.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2735">Support for additional Template Export options</span></span>
    - <span data-ttu-id="d29f3-2736">В Export-AzResourceGroup добавлен параметр -SkipResourceNameParameterization.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2736">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="d29f3-2737">В Export-AzResourceGroup добавлен параметр -SkipAllParameterization.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2737">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="d29f3-2738">В Export-AzResourceGroup добавлен параметр -Resource для фильтрации экспортированных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2738">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d29f3-2739">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d29f3-2739">Az.ServiceFabric</span></span>
* <span data-ttu-id="d29f3-2740">Исправлена ошибка, связанная с получением иногда неправильных отпечатков при добавлении сертификата ByExistingKeyVault.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2740">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="d29f3-2741">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-2741">Az.Sql</span></span>
* <span data-ttu-id="d29f3-2742">Исправлен суффикс конечной точки хранилища службы "Расширенная защита от угроз Azure".</span><span class="sxs-lookup"><span data-stu-id="d29f3-2742">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="d29f3-2743">Исправлена ошибка, связанная с возможностью пакета "Расширенная защита данных" переопределять политику службы "Расширенная защита от угроз".</span><span class="sxs-lookup"><span data-stu-id="d29f3-2743">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="d29f3-2744">Новые командлеты для Management.Sql позволяют клиентам добавлять ключи TDE и задавать средство защиты TDE для управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2744">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="d29f3-2745">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d29f3-2745">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="d29f3-2746">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d29f3-2746">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="d29f3-2747">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d29f3-2747">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="d29f3-2748">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="d29f3-2748">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="d29f3-2749">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="d29f3-2749">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d29f3-2750">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d29f3-2750">Az.Storage</span></span>
* <span data-ttu-id="d29f3-2751">Поддержка класса Kind в FileStorage и значения Premium_ZRS в SkuName при создании учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2751">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="d29f3-2752">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d29f3-2752">New-AzStorageAccount</span></span>
* <span data-ttu-id="d29f3-2753">Уточнено описание командлета неизменности BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2753">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="d29f3-2754">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d29f3-2754">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d29f3-2755">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d29f3-2755">Az.Websites</span></span>
* <span data-ttu-id="d29f3-2756">Оптимизирует Get-AzWebAppCertificate для фильтрации по группе ресурсов на сервере, а не в клиенте.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2756">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="d29f3-2757">Добавляет параметр-переключатель - UseDisasterRecovery в Get AzWebAppSnapshot.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2757">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="d29f3-2758">2.2.0 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2758">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="d29f3-2759">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d29f3-2759">Az.Cdn</span></span>
* <span data-ttu-id="d29f3-2760">Обновлены командлеты для поддержки функции rulesEngine на основе API версии 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2760">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d29f3-2761">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-2761">Az.Compute</span></span>
* <span data-ttu-id="d29f3-2762">Добавлен параметр `NoWait`, который запускает операцию и немедленно возвращает значение еще до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2762">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="d29f3-2763">Обновлены командлеты:   Export-AzLogAnalyticRequestRateByInterval; Export-AzLogAnalyticThrottledRequest; Remove-AzVM; Remove-AzVMAccessExtension; Remove-AzVMAEMExtension; Remove-AzVMChefExtension; Remove-AzVMCustomScriptExtension; Remove-AzVMDiagnosticsExtension; Remove-AzVMDiskEncryptionExtension; Remove-AzVMDscExtension; Remove-AzVMSqlServerExtension; Restart-AzVM; Set-AzVM; Set-AzVMAccessExtension; Set-AzVMADDomainExtension; Set-AzVMAEMExtension; Set-AzVMBginfoExtension; Set-AzVMChefExtension; Set-AzVMCustomScriptExtension; Set-AzVMDiagnosticsExtension; Set-AzVMDscExtension; Set-AzVMExtension; Start-AzVM; Stop-AzVM; Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2763">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d29f3-2764">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d29f3-2764">Az.EventHub</span></span>
* <span data-ttu-id="d29f3-2765">Исправлена ошибка № 9231. Командлет Get-AzEventHubNamespace не возвращал теги.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2765">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="d29f3-2766">Исправлена ошибка № 9230. Командлет Get-AzEventHubNamespace возвращал значение ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2766">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d29f3-2767">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d29f3-2767">Az.Network</span></span>
* <span data-ttu-id="d29f3-2768">Обновлены параметры ResourceId и InputObject для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2768">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="d29f3-2769">Добавлены псевдонимы для параметров ResourceId и InputObject.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2769">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d29f3-2770">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d29f3-2770">Az.PolicyInsights</span></span>
* <span data-ttu-id="d29f3-2771">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyEvent.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2771">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d29f3-2772">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-2772">Az.RecoveryServices</span></span>
* <span data-ttu-id="d29f3-2773">Минимальный срок хранения политики IaaSVM изменился с 1 до 7 дней.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2773">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d29f3-2774">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d29f3-2774">Az.ServiceBus</span></span>
* <span data-ttu-id="d29f3-2775">Исправлена ошибка № 9182. Командлет Get-AzServiceBusNamespace возвращал ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2775">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d29f3-2776">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d29f3-2776">Az.ServiceFabric</span></span>
* <span data-ttu-id="d29f3-2777">Исправлена опечатка в сообщении об ошибке для командлета Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2777">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="d29f3-2778">Добавлен отсутствующий символ в командных строках Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2778">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="d29f3-2779">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-2779">Az.Sql</span></span>
* <span data-ttu-id="d29f3-2780">Для командлета New-AzureSqlInstance добавлен параметр DnsZonePartner, обеспечивающий поддержку AutoDr для Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2780">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="d29f3-2781">Командлет Get-AzSqlDatabaseSecureConnectionPolicy объявлен неподдерживаемым.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2781">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="d29f3-2782">Командлеты обнаружения угроз переименованы в командлеты Расширенной защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2782">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="d29f3-2783">Параметры -StorageSizeInGB и -LicenseType командлета New-AzSqlInstance теперь необязательны.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2783">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d29f3-2784">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d29f3-2784">Az.Websites</span></span>
* <span data-ttu-id="d29f3-2785">Исправлены проблемы, когда удалялись теги при использовании Set-AzWebApp и Set-AzWebAppSlot со свойством -WebApp.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2785">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="d29f3-2786">2.1.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2786">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="d29f3-2787">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d29f3-2787">Az.ApiManagement</span></span>
* <span data-ttu-id="d29f3-2788">Созданы командлеты для управления диагностикой в глобальной области и в области API.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2788">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="d29f3-2789">**Get-AzApiManagementDiagnostic** — получение диагностики, заданной глобально или на уровне области API.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2789">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="d29f3-2790">**New-AzApiManagementDiagnostic** — создание диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2790">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="d29f3-2791">**New-AzApiManagementHttpMessageDiagnostic** — создание параметра диагностики, для которого регистрируются заголовки и размер байтов тела.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2791">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="d29f3-2792">**New-AzApiManagementPipelineDiagnosticSetting** — создание параметров диагностики для сообщений HTTP, поступающих в шлюз или исходящих из него.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2792">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="d29f3-2793">**New-AzApiManagementSamplingSetting** — создание параметра выборки для запросов и ответов касательно диагностики.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2793">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="d29f3-2794">**Remove-AzApiManagementDiagnostic** — удаление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2794">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="d29f3-2795">**Set-AzApiManagementDiagnostic** — обновление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2795">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="d29f3-2796">Созданы командлеты для управления кэшем в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2796">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="d29f3-2797">**Get-AzApiManagementCache** — получение сведений о кэше, указанном идентификатором, или обо всех кэшах.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2797">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="d29f3-2798">**New-AzApiManagementCache** — создание кэша по умолчанию или кэша в определенном регионе Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2798">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="d29f3-2799">**Remove-AzApiManagementCache** — удаление кэша.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2799">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="d29f3-2800">**Update-AzApiManagementCache** — обновление кэша.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2800">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="d29f3-2801">Созданы командлеты для управления схемой API.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2801">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="d29f3-2802">**New-AzApiManagementSchema** — создание схемы для API.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2802">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="d29f3-2803">**Get-AzApiManagementSchema** — получение схем, настроенных в API.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2803">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="d29f3-2804">**Remove-AzApiManagementSchema** — удаление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2804">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="d29f3-2805">**Set-AzApiManagementSchema** — обновление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2805">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="d29f3-2806">Создан командлет для создания токена пользователя.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2806">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="d29f3-2807">**New-AzApiManagementUserToken** — создание токена пользователя, по умолчанию действительного в течение 8 часов. С помощью этого командлета можно создавать токен для пользователя GIT.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2807">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="d29f3-2808">Создан командлет для получения состояния сети.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2808">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="d29f3-2809">**Get-AzApiManagementNetworkStatus** — получение состояния подключения сети ресурсов, от которых зависит служба "Управление API".</span><span class="sxs-lookup"><span data-stu-id="d29f3-2809">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="d29f3-2810">Это полезно при развертывании службы ApiManagement в виртуальной сети и проверке того, не нарушена ли какая-либо из зависимостей.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2810">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="d29f3-2811">Обновлен командлет **New-AzApiManagement** для управления службой ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2811">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="d29f3-2812">Добавлена поддержка нового SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2812">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="d29f3-2813">Добавлена поддержка для включения флага EnableClientCertificate в SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2813">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="d29f3-2814">Новый командлет **New-AzApiManagementSslSetting** позволяет настраивать параметр TLS/SSL для сервера (Backend) и внешнего интерфейса (Frontend).</span><span class="sxs-lookup"><span data-stu-id="d29f3-2814">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="d29f3-2815">Его также можно использовать для настройки Ciphers как 3DES, в ServerProtocols как Http2 для внешнего интерфейса (Frontend) службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2815">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="d29f3-2816">Добавлена поддержка настройки имени узла DeveloperPortal в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2816">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="d29f3-2817">Обновлен командлет **Get-AzApiManagementSsoToken** для извлечения объекта PsApiManagement в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2817">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="d29f3-2818">Обновлен командлет для отображения встроенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2818">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="d29f3-2819">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Код ошибки: ValidationError. Сообщение об ошибке: "Некоторые поля содержат неправильные значения". Сведения об ошибке: [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="d29f3-2819">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="d29f3-2820">Обновлен командлет **Export-AzApiManagementApi** для экспортирования программных интерфейсов в формате OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2820">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="d29f3-2821">Обновлен командлет **Import-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2821">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="d29f3-2822">Для импортирования API из спецификации документа OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2822">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="d29f3-2823">Для переопределения свойства PsApiManagementSchema, указанного в любом документе (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="d29f3-2823">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="d29f3-2824">Для переопределения свойства ServiceUrl, указанного в любом документе.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2824">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="d29f3-2825">Обновлен командлет **Get-AzApiManagementPolicy** для возврата политики в формате, экранированном не для XML, с использованием rawxml.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2825">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="d29f3-2826">Обновлен командлет **Set-AzApiManagementPolicy**. Он принимает политику в формате, экранированном не для XML, с использованием rawxml и в формате, экранированном для XML, с использованием XML.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2826">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="d29f3-2827">Обновлен командлет **New-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2827">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="d29f3-2828">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2828">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="d29f3-2829">Для создания API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2829">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="d29f3-2830">Для клонирования API с использованием значений SourceApiId и SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2830">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="d29f3-2831">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2831">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="d29f3-2832">Обновлен командлет **Set-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2832">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="d29f3-2833">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2833">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="d29f3-2834">Для обновления API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2834">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="d29f3-2835">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2835">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="d29f3-2836">Обновлен командлет **New-AzApiManagementRevision**:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2836">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="d29f3-2837">Для клонирования (копирования тегов, продуктов, операций и политик) существующей редакции с использованием SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2837">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="d29f3-2838">Новая редакция предполагает родительский идентификатор ApiId.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2838">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="d29f3-2839">Для предоставления ApiRevisionDescription.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2839">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="d29f3-2840">Для переопределения значения ServiceUrl при клонировании API.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2840">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="d29f3-2841">Обновлен командлет **New-AzApiManagementIdentityProvider**:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2841">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="d29f3-2842">Для настройки AAD или AADB2C с Authority.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2842">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="d29f3-2843">Для установки политик SignupPolicy, SigninPolicy, ProfileEditingPolicy и PasswordResetPolicy.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2843">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="d29f3-2844">Обновлен командлет **New-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2844">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="d29f3-2845">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2845">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="d29f3-2846">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2846">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="d29f3-2847">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2847">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="d29f3-2848">Обновлен командлет **Set-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2848">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="d29f3-2849">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2849">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="d29f3-2850">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2850">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="d29f3-2851">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2851">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="d29f3-2852">Следующие командлеты обновлены, чтобы принимать значение ResourceId в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2852">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="d29f3-2853">New-AzApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2853">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="d29f3-2854">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="d29f3-2854">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="d29f3-2855">Get-AzApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2855">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="d29f3-2856">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="d29f3-2856">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="d29f3-2857">Get-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2857">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="d29f3-2858">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="d29f3-2858">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="d29f3-2859">Get-AzApiManagementAuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2859">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="d29f3-2860">Get-AzApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2860">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="d29f3-2861">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="d29f3-2861">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="d29f3-2862">Get-AzApiManagementCertificate.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2862">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="d29f3-2863">Remove-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2863">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="d29f3-2864">Remove-AzApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2864">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d29f3-2865">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d29f3-2865">Az.Automation</span></span>
* <span data-ttu-id="d29f3-2866">Обновлен командлет Get-AzAutomationJobOutputRecord для обработки значений в формате JSON и в виде текстовой записи.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2866">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="d29f3-2867">исправлена проблема https://github.com/Azure/azure-powershell/issues/7977.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2867">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="d29f3-2868">исправлена проблема https://github.com/Azure/azure-powershell/issues/8600.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2868">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="d29f3-2869">Поведение командлета Start-AzAutomationDscCompilationJob изменено так, чтобы сразу же запустить задание, а не ждать его завершения.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2869">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="d29f3-2870">исправлена проблема https://github.com/Azure/azure-powershell/issues/8347.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2870">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="d29f3-2871">Исправлен командлет Get-AzAutomationDscNode, возвращающий все узлы при использовании -Name.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2871">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="d29f3-2872">Теперь он возвращает только соответствующий узел.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2872">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d29f3-2873">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-2873">Az.Compute</span></span>
* <span data-ttu-id="d29f3-2874">Добавлены параметры ProtectFromScaleIn и ProtectFromScaleSetAction для командлета Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2874">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="d29f3-2875">Командлет New-AzVM с простым набором параметров теперь по умолчанию использует доступное расположение, если регион "восточная часть США" не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2875">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d29f3-2876">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d29f3-2876">Az.DataLakeStore</span></span>
* <span data-ttu-id="d29f3-2877">Обновлен пакет SDK ADLS для использования httpclient. В инфраструктуру Azure интегрирована проверка плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2877">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d29f3-2878">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d29f3-2878">Az.Monitor</span></span>
* <span data-ttu-id="d29f3-2879">Исправлены неправильные имена параметров в справочных примерах.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2879">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d29f3-2880">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d29f3-2880">Az.Network</span></span>
* <span data-ttu-id="d29f3-2881">Добавлен флаг DisableBgpRoutePropagation для выходных данных действующей таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2881">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="d29f3-2882">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2882">Updated cmdlet:</span></span>
        - <span data-ttu-id="d29f3-2883">Get-AzEffectiveRouteTable.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2883">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="d29f3-2884">Исправлен двойной дефис в документации New-AzApplicationGatewayTrustedRootCertificate.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2884">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="d29f3-2885">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-2885">Az.Resources</span></span>
* <span data-ttu-id="d29f3-2886">Добавлен новый командлет Get-AzureRmDenyAssignment для получения запрещающих назначений.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2886">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="d29f3-2887">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-2887">Az.Sql</span></span>
* <span data-ttu-id="d29f3-2888">Командлеты Расширенной защиты от угроз переименованы на командлеты Расширенной защиты данных, и оценка уязвимости включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2888">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="d29f3-2889">2.0.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2889">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d29f3-2890">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d29f3-2890">Az.Accounts</span></span>
* <span data-ttu-id="d29f3-2891">Обновлена библиотека аутентификации для устранения проблем с ADFS при использовании аутентификации на основе имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2891">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d29f3-2892">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-2892">Az.CognitiveServices</span></span>
* <span data-ttu-id="d29f3-2893">Отображается только заявление об отказе Bing для служб Поиска Bing.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2893">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="d29f3-2894">Исправлена проблема с созданием учетной записи.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2894">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d29f3-2895">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-2895">Az.Compute</span></span>
* <span data-ttu-id="d29f3-2896">Функция группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2896">Proximity placement group feature.</span></span>
    - <span data-ttu-id="d29f3-2897">Добавлены следующие новые командлеты:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="d29f3-2897">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="d29f3-2898">Новый параметр ProximityPlacementGroupId будет добавлен в следующие командлеты:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="d29f3-2898">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="d29f3-2899">В командлет New-AzGalleryImageVersion добавлен параметр StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2899">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="d29f3-2900">TargetRegion в командлете New-AzGalleryImageVersion может содержать StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2900">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="d29f3-2901">Параметр-переключатель SkipShutdown добавлен в командлеты Stop-AzVM и Stop-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2901">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="d29f3-2902">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="d29f3-2902">Breaking changes</span></span>
    - <span data-ttu-id="d29f3-2903">Командлет SET-AzVMBootDiagnostics изменен на Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2903">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="d29f3-2904">Командлет Export-AzLogAnalyticThrottledRequests изменен на Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2904">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="d29f3-2905">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="d29f3-2905">Az.DeploymentManager</span></span>
* <span data-ttu-id="d29f3-2906">Первая общедоступная версия командлетов диспетчера развертывания Azure</span><span class="sxs-lookup"><span data-stu-id="d29f3-2906">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="d29f3-2907">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="d29f3-2907">Az.Dns</span></span>
* <span data-ttu-id="d29f3-2908">Автоматическое делегирование DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="d29f3-2908">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="d29f3-2909">Командлет для создания зоны DNS принимает имя родительской зоны в качестве дополнительного необязательного параметра.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2909">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="d29f3-2910">Он добавляет записи NS в родительской зоне для созданной дочерней зоны.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2910">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d29f3-2911">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d29f3-2911">Az.FrontDoor</span></span>
* <span data-ttu-id="d29f3-2912">Первая общедоступная версия командлетов Azure FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2912">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="d29f3-2913">Переименованы командлеты WAF для включения Waf.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2913">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="d29f3-2914">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d29f3-2914">Az.HDInsight</span></span>
* <span data-ttu-id="d29f3-2915">Удалены два командлета:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2915">Removed two cmdlets:</span></span>
    - <span data-ttu-id="d29f3-2916">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d29f3-2916">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="d29f3-2917">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d29f3-2917">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="d29f3-2918">Добавлен новый командлет Set-AzHDInsightGatewayCredential для замены Grant-AzHDInsightHttpServicesAccess.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2918">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="d29f3-2919">Обновлен командлет Get-AzHDInsightJobOutput для различения ролей читателя и оператора HDInsight:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2919">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="d29f3-2920">Пользователям с ролью читателя не нужно указывать параметр DefaultStorageAccountKey явным образом, иначе возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2920">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="d29f3-2921">На пользователей с ролью оператора HDInsight это не повлияет.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2921">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d29f3-2922">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d29f3-2922">Az.Monitor</span></span>
* <span data-ttu-id="d29f3-2923">Новые командлеты для API SQR (запланированное правило запросов)</span><span class="sxs-lookup"><span data-stu-id="d29f3-2923">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="d29f3-2924">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="d29f3-2924">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="d29f3-2925">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="d29f3-2925">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="d29f3-2926">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="d29f3-2926">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="d29f3-2927">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="d29f3-2927">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="d29f3-2928">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="d29f3-2928">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="d29f3-2929">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="d29f3-2929">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="d29f3-2930">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d29f3-2930">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d29f3-2931">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d29f3-2931">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d29f3-2932">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d29f3-2932">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d29f3-2933">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d29f3-2933">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d29f3-2934">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d29f3-2934">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d29f3-2935">См. подробнее об [API SQR](/rest/api/monitor/scheduledqueryrules).</span><span class="sxs-lookup"><span data-stu-id="d29f3-2935">[More](/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="d29f3-2936">Обновлен файл Az.Monitor.md для включения командлетов для правила генерации оповещений на основе метрик GenV2(не классическая версия).</span><span class="sxs-lookup"><span data-stu-id="d29f3-2936">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d29f3-2937">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d29f3-2937">Az.Network</span></span>
* <span data-ttu-id="d29f3-2938">Добавлена поддержка для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2938">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="d29f3-2939">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="d29f3-2939">New cmdlets</span></span>
        - <span data-ttu-id="d29f3-2940">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d29f3-2940">New-AzNatGateway</span></span>
        - <span data-ttu-id="d29f3-2941">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d29f3-2941">Get-AzNatGateway</span></span>
        - <span data-ttu-id="d29f3-2942">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d29f3-2942">Set-AzNatGateway</span></span>
        - <span data-ttu-id="d29f3-2943">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d29f3-2943">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="d29f3-2944">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="d29f3-2944">Updated cmdlets</span></span>
        - <span data-ttu-id="d29f3-2945">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="d29f3-2945">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="d29f3-2946">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="d29f3-2946">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="d29f3-2947">Обновлены следующие команды для функции: Настройка и удаление пользовательских маршрутов через шлюз в Бруклине.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2947">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="d29f3-2948">Обновлен командлет New-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2948">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="d29f3-2949">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2949">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d29f3-2950">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d29f3-2950">Az.PolicyInsights</span></span>
* <span data-ttu-id="d29f3-2951">Добавлена поддержка сведений об оценке политики запросов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2951">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="d29f3-2952">Добавлен параметр -Expand в командлет Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2952">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="d29f3-2953">Добавлена поддержка -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2953">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d29f3-2954">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-2954">Az.RecoveryServices</span></span>
* <span data-ttu-id="d29f3-2955">Добавлена поддержка перекрестной подписки на Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2955">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="d29f3-2956">Добавлена возможность отмечать предстоящие критически важные изменения для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2956">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="d29f3-2957">Исправлены план восстановления и план действий для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2957">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="d29f3-2958">Исправлено сетевое сопоставление обновления Azure Site Recovery (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="d29f3-2958">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="d29f3-2959">Исправлено направление защиты обновления Azure Site Recovery для управляемых дисков (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="d29f3-2959">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="d29f3-2960">Добавлены другие незначительные исправления.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2960">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="d29f3-2961">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="d29f3-2961">Az.Relay</span></span>
* <span data-ttu-id="d29f3-2962">Исправлены опечатки в сообщениях для клиентов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2962">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d29f3-2963">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d29f3-2963">Az.ServiceBus</span></span>
* <span data-ttu-id="d29f3-2964">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2964">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d29f3-2965">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d29f3-2965">Az.Storage</span></span>
* <span data-ttu-id="d29f3-2966">Выполнено обновление клиентской библиотеки хранилища до версии 10.0.1 (пространство имен всех объектов из этого пакета SDK изменено с Microsoft.WindowsAzure.Storage. *на Microsoft.Azure.Storage*).</span><span class="sxs-lookup"><span data-stu-id="d29f3-2966">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="d29f3-2967">Выполнено обновление до Microsoft.Azure.Management.Storage версии 11.0.0 для включения поддержки нового API версии 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2967">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="d29f3-2968">Значение свойства Kind по умолчанию в учетной записи хранения изменено со Storage на StorageV2.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2968">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="d29f3-2969">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d29f3-2969">New-AzStorageAccount</span></span>
* <span data-ttu-id="d29f3-2970">Изменено значение Sku.Name в выходных данных командлета учетной записи хранения в соответствии со значением Sku.Name во входных данных путем добавления _ (например, StandardLRS изменено на Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="d29f3-2970">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="d29f3-2971">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d29f3-2971">New-AzStorageAccount</span></span>
    - <span data-ttu-id="d29f3-2972">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d29f3-2972">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="d29f3-2973">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d29f3-2973">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d29f3-2974">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d29f3-2974">Az.Websites</span></span>
* <span data-ttu-id="d29f3-2975">Свойство Kind теперь будет задаваться объектам PSSite, возвращаемым командлетом Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2975">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="d29f3-2976">Get-AzWebApp\*Metrics и Get-AzAppServicePlanMetrics считаются нерекомендуемыми.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2976">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="d29f3-2977">1.8.0 — апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2977">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d29f3-2978">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="d29f3-2978">Highlights since the last major release</span></span>
* <span data-ttu-id="d29f3-2979">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2979">General availability of `Az` module</span></span>
* <span data-ttu-id="d29f3-2980">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="d29f3-2980">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="d29f3-2981">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="d29f3-2981">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="d29f3-2982">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2982">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="d29f3-2983">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2983">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d29f3-2984">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2984">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="d29f3-2985">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="d29f3-2985">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d29f3-2986">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d29f3-2986">Az.Accounts</span></span>
* <span data-ttu-id="d29f3-2987">Обновлен командлет Uninstall-AzureRm для правильного удаления модулей в Mac.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2987">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d29f3-2988">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d29f3-2988">Az.Batch</span></span>
* <span data-ttu-id="d29f3-2989">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2989">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d29f3-2990">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d29f3-2990">Az.Cdn</span></span>
* <span data-ttu-id="d29f3-2991">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2991">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d29f3-2992">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-2992">Az.CognitiveServices</span></span>
* <span data-ttu-id="d29f3-2993">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2993">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d29f3-2994">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-2994">Az.Compute</span></span>
* <span data-ttu-id="d29f3-2995">Устранена проблема с установкой AEM, если в идентификаторах ресурсов дисков группа ресурсов указана в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2995">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="d29f3-2996">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2996">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d29f3-2997">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2997">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d29f3-2998">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d29f3-2998">Az.DataFactory</span></span>
* <span data-ttu-id="d29f3-2999">Добавлены свойства SsisProperties, если NodeCount не имеет значения NULL для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="d29f3-2999">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d29f3-3000">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d29f3-3000">Az.DataLakeStore</span></span>
* <span data-ttu-id="d29f3-3001">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3001">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d29f3-3002">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d29f3-3002">Az.EventGrid</span></span>
* <span data-ttu-id="d29f3-3003">Обновлен текст справки для конечной точки, указывающий, что необходимо создать ресурсы, прежде чем использовать командлеты для создания или обновления подписки на события.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3003">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d29f3-3004">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d29f3-3004">Az.EventHub</span></span>
* <span data-ttu-id="d29f3-3005">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3005">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d29f3-3006">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d29f3-3006">Az.HDInsight</span></span>
* <span data-ttu-id="d29f3-3007">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3007">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d29f3-3008">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d29f3-3008">Az.IotHub</span></span>
* <span data-ttu-id="d29f3-3009">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3009">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d29f3-3010">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d29f3-3010">Az.KeyVault</span></span>
* <span data-ttu-id="d29f3-3011">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3011">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d29f3-3012">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3012">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="d29f3-3013">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="d29f3-3013">Az.MachineLearning</span></span>
* <span data-ttu-id="d29f3-3014">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3014">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="d29f3-3015">Az.Media</span><span class="sxs-lookup"><span data-stu-id="d29f3-3015">Az.Media</span></span>
* <span data-ttu-id="d29f3-3016">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3016">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d29f3-3017">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d29f3-3017">Az.Monitor</span></span>
  * <span data-ttu-id="d29f3-3018">Добавлены новые командлеты для правила генерации оповещений на основе метрик GenV2 (не классических).</span><span class="sxs-lookup"><span data-stu-id="d29f3-3018">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="d29f3-3019">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="d29f3-3019">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="d29f3-3020">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="d29f3-3020">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="d29f3-3021">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="d29f3-3021">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="d29f3-3022">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="d29f3-3022">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="d29f3-3023">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="d29f3-3023">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="d29f3-3024">Обновлен пакет SDK Monitor до предварительной версии 0.22.0.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3024">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d29f3-3025">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d29f3-3025">Az.Network</span></span>
* <span data-ttu-id="d29f3-3026">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3026">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d29f3-3027">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3027">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="d29f3-3028">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="d29f3-3028">Az.NotificationHubs</span></span>
* <span data-ttu-id="d29f3-3029">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3029">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d29f3-3030">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d29f3-3030">Az.OperationalInsights</span></span>
* <span data-ttu-id="d29f3-3031">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3031">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="d29f3-3032">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="d29f3-3032">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="d29f3-3033">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3033">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d29f3-3034">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-3034">Az.RecoveryServices</span></span>
* <span data-ttu-id="d29f3-3035">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3035">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d29f3-3036">Обновлен табличный формат для SQL на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3036">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="d29f3-3037">Добавлен альтернативный метод для получения расположения в Общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3037">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="d29f3-3038">Обновлено значение ScheduleRunDays в объекте SchedulePolicy в соответствии с часовым поясом.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3038">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="d29f3-3039">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d29f3-3039">Az.RedisCache</span></span>
* <span data-ttu-id="d29f3-3040">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3040">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d29f3-3041">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-3041">Az.Resources</span></span>
* <span data-ttu-id="d29f3-3042">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3042">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="d29f3-3043">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-3043">Az.Sql</span></span>
* <span data-ttu-id="d29f3-3044">Заменена зависимость от пакета SDK монитора на обычный код.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3044">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="d29f3-3045">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3045">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d29f3-3046">Улучшен процесс классификации нескольких столбцов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3046">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="d29f3-3047">Добавлены свойства SKU (имя, семейство, производительность SKU) в отклике Get-AzSqlServerServiceObjective, а также по умолчанию задан табличный формат.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3047">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="d29f3-3048">C помощью Get-AzSqlServerServiceObjective теперь можно получать список доступных целевых служб по расположению без необходимости заранее размещать сервер в регионе.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3048">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="d29f3-3049">Поддерживается параметр часового пояса при создании Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3049">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="d29f3-3050">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3050">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d29f3-3051">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d29f3-3051">Az.Websites</span></span>
* <span data-ttu-id="d29f3-3052">Исправлены командлеты Set-AzWebApp и Set-AzWebAppSlot, которые теперь не удаляют теги при выполнении.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3052">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="d29f3-3053">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3053">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d29f3-3054">Обновлен пакет SDK веб-узлов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3054">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="d29f3-3055">Удалено свойство AdminSiteName из PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3055">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="d29f3-3056">1.7.0 —апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3056">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d29f3-3057">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="d29f3-3057">Highlights since the last major release</span></span>
* <span data-ttu-id="d29f3-3058">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3058">General availability of `Az` module</span></span>
* <span data-ttu-id="d29f3-3059">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="d29f3-3059">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="d29f3-3060">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="d29f3-3060">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="d29f3-3061">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3061">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="d29f3-3062">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3062">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d29f3-3063">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3063">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="d29f3-3064">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="d29f3-3064">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d29f3-3065">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d29f3-3065">Az.Accounts</span></span>
* <span data-ttu-id="d29f3-3066">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметр AzureAnalysisServicesEndpointResourceId.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3066">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d29f3-3067">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-3067">Az.AnalysisServices</span></span>
* <span data-ttu-id="d29f3-3068">Использование ServiceClient в командлетах плоскости данных и удаление исходной логики проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3068">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="d29f3-3069">Add-AzureASAccount используется как оболочка для Connect-AzAccount во избежание критических изменений.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3069">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d29f3-3070">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d29f3-3070">Az.Automation</span></span>
* <span data-ttu-id="d29f3-3071">Исправлена ошибка командлета New-AzAutomationSoftwareUpdateConfiguration, связанная с включением.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3071">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="d29f3-3072">Теперь параметры IncludedKbNumber и IncludedPackageNameMask должны работать нормально.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3072">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="d29f3-3073">Исправлена ошибка динамической группы управления обновлениями службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3073">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d29f3-3074">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-3074">Az.Compute</span></span>
* <span data-ttu-id="d29f3-3075">В командлеты New-AzDiskConfig и New-AzSnapshotConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3075">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="d29f3-3076">Теперь можно создавать виртуальные машину на основе образов из коллекции от других клиентов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3076">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="d29f3-3077">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d29f3-3077">Az.ContainerInstance</span></span>
* <span data-ttu-id="d29f3-3078">Исправлена проблема в параметре -Command командлета New-AzContainerGroup, из-за которой в конце добавлялся пустой аргумент.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3078">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d29f3-3079">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d29f3-3079">Az.DataFactory</span></span>
* <span data-ttu-id="d29f3-3080">Пакет SDK для ADF .NET обновлен до версии 3.0.2.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3080">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="d29f3-3081">Командлет Set-AzDataFactoryV2 обновлен с помощью дополнительных параметров для настроек, связанных с RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3081">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d29f3-3082">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-3082">Az.Resources</span></span>
* <span data-ttu-id="d29f3-3083">Улучшена обработка поставщиков Get-AzResource при предоставлении параметров -ResourceId или -ResourceGroupName, -Name и -ResourceType.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3083">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="d29f3-3084">Улучшена обработка ошибок в командлетах Test-AzDeployment и Test-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3084">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="d29f3-3085">Теперь ошибки, возникающие за пределами проверки развертывания, обрабатываются и включаются в выходные данные команды.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3085">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="d29f3-3086">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3086">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="d29f3-3087">Добавлен параметр-переключатель -IgnoreDynamicParameters, с помощью которого можно настроить командлеты развертывания так, чтобы они пропускали запросы в сценариях скриптов и заданий.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3087">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="d29f3-3088">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3088">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="d29f3-3089">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-3089">Az.Sql</span></span>
* <span data-ttu-id="d29f3-3090">Поддержка классификации данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3090">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d29f3-3091">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d29f3-3091">Az.Storage</span></span>
* <span data-ttu-id="d29f3-3092">Подробные сообщения об ошибке передаются при создании контекста хранилища с помощью параметра -UseConnectedAccount, но без входа в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3092">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="d29f3-3093">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d29f3-3093">New-AzStorageContext</span></span>
* <span data-ttu-id="d29f3-3094">Поддержка свойств службы управления BLOB-объектов в указанной учетной записи хранения с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3094">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="d29f3-3095">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d29f3-3095">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="d29f3-3096">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d29f3-3096">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="d29f3-3097">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d29f3-3097">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="d29f3-3098">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d29f3-3098">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="d29f3-3099">Поддержка параметра -AsJob в командлетах для отправки и скачивания больших двоичных объектов и файлов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3099">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="d29f3-3100">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d29f3-3100">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="d29f3-3101">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d29f3-3101">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="d29f3-3102">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d29f3-3102">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="d29f3-3103">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d29f3-3103">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="d29f3-3104">1.6.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3104">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d29f3-3105">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="d29f3-3105">Highlights since the last major release</span></span>
* <span data-ttu-id="d29f3-3106">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3106">General availability of `Az` module</span></span>
* <span data-ttu-id="d29f3-3107">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="d29f3-3107">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="d29f3-3108">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="d29f3-3108">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="d29f3-3109">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3109">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="d29f3-3110">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3110">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d29f3-3111">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3111">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="d29f3-3112">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="d29f3-3112">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d29f3-3113">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d29f3-3113">Az.Automation</span></span>
* <span data-ttu-id="d29f3-3114">В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:</span><span class="sxs-lookup"><span data-stu-id="d29f3-3114">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="d29f3-3115">динамическое группирование;</span><span class="sxs-lookup"><span data-stu-id="d29f3-3115">Dynamic grouping</span></span>
    * <span data-ttu-id="d29f3-3116">скрипты предварительного или последующего выполнения;</span><span class="sxs-lookup"><span data-stu-id="d29f3-3116">Pre-Post script</span></span>
    * <span data-ttu-id="d29f3-3117">параметр перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3117">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d29f3-3118">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-3118">Az.Compute</span></span>
* <span data-ttu-id="d29f3-3119">Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3119">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="d29f3-3120">Обновление клиентской библиотеки вычислений до версии 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3120">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d29f3-3121">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d29f3-3121">Az.KeyVault</span></span>
* <span data-ttu-id="d29f3-3122">Добавлена поддержка подстановочных знаков в командлетах KeyVault.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3122">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d29f3-3123">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d29f3-3123">Az.Network</span></span>
* <span data-ttu-id="d29f3-3124">Добавлена поддержка анализа угроз для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3124">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="d29f3-3125">Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3125">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d29f3-3126">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-3126">Az.RecoveryServices</span></span>
* <span data-ttu-id="d29f3-3127">В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3127">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="d29f3-3128">Добавлена поддержка канала для отмены регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3128">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="d29f3-3129">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-3129">Az.Resources</span></span>
* <span data-ttu-id="d29f3-3130">Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3130">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="d29f3-3131">Обновлены учетные данные, используемые при общих вызовах к ARM.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3131">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="d29f3-3132">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-3132">Az.Sql</span></span>
* <span data-ttu-id="d29f3-3133">Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3133">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d29f3-3134">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d29f3-3134">Az.Storage</span></span>
* <span data-ttu-id="d29f3-3135">Поддержка получения, настройки и удаления политики управления в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3135">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="d29f3-3136">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d29f3-3136">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="d29f3-3137">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d29f3-3137">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="d29f3-3138">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d29f3-3138">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="d29f3-3139">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="d29f3-3139">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="d29f3-3140">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="d29f3-3140">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="d29f3-3141">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="d29f3-3141">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d29f3-3142">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d29f3-3142">Az.Websites</span></span>
* <span data-ttu-id="d29f3-3143">Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3143">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="d29f3-3144">1.5.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3144">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d29f3-3145">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d29f3-3145">Az.Accounts</span></span>
* <span data-ttu-id="d29f3-3146">Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3146">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="d29f3-3147">Обновлены примеры для Connect AzAccount.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3147">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d29f3-3148">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d29f3-3148">Az.Automation</span></span>
* <span data-ttu-id="d29f3-3149">Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3149">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="d29f3-3150">Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3150">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="d29f3-3151">Теперь он возвращает все узлы.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3151">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d29f3-3152">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d29f3-3152">Az.Cdn</span></span>
* <span data-ttu-id="d29f3-3153">Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3153">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d29f3-3154">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-3154">Az.Compute</span></span>
* <span data-ttu-id="d29f3-3155">Добавлена поддержка подстановочных знаков в командлетах Get.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3155">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d29f3-3156">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d29f3-3156">Az.DataFactory</span></span>
* <span data-ttu-id="d29f3-3157">Обновлен пакет SDK для ADF .NET до версии 3.0.1.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3157">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d29f3-3158">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d29f3-3158">Az.LogicApp</span></span>
* <span data-ttu-id="d29f3-3159">Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3159">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d29f3-3160">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d29f3-3160">Az.Network</span></span>
* <span data-ttu-id="d29f3-3161">Добавлена поддержка подстановочных знаков в командлетах Network.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3161">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d29f3-3162">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-3162">Az.RecoveryServices</span></span>
* <span data-ttu-id="d29f3-3163">Добавлена поддержка SQL Server на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3163">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="d29f3-3164">Обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="d29f3-3164">SDK Update</span></span>
* <span data-ttu-id="d29f3-3165">Удалена проверка VMappContainer в Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3165">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="d29f3-3166">Добавлены параметры Name и ServerName для Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3166">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="d29f3-3167">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-3167">Az.Resources</span></span>
* <span data-ttu-id="d29f3-3168">Добавлен параметр `-TemplateObject` в командлеты для развертывания.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3168">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="d29f3-3169">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3169">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="d29f3-3170">Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3170">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="d29f3-3171">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3171">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="d29f3-3172">Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3172">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="d29f3-3173">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3173">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="d29f3-3174">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-3174">Az.Sql</span></span>
* <span data-ttu-id="d29f3-3175">Обновление AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3175">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="d29f3-3176">Исправлено поведение для пограничного случая при создании параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3176">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d29f3-3177">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d29f3-3177">Az.Storage</span></span>
* <span data-ttu-id="d29f3-3178">Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3178">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="d29f3-3179">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3179">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="d29f3-3180">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-3180">Az.AnalysisServices</span></span>
* <span data-ttu-id="d29f3-3181">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3181">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d29f3-3182">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d29f3-3182">Az.Automation</span></span>
* <span data-ttu-id="d29f3-3183">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3183">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="d29f3-3184">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3184">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="d29f3-3185">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3185">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d29f3-3186">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-3186">Az.CognitiveServices</span></span>
* <span data-ttu-id="d29f3-3187">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3187">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d29f3-3188">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-3188">Az.Compute</span></span>
* <span data-ttu-id="d29f3-3189">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3189">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="d29f3-3190">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3190">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="d29f3-3191">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3191">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="d29f3-3192">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3192">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d29f3-3193">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d29f3-3193">Az.DataLakeStore</span></span>
* <span data-ttu-id="d29f3-3194">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3194">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d29f3-3195">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d29f3-3195">Az.EventHub</span></span>
* <span data-ttu-id="d29f3-3196">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3196">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d29f3-3197">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d29f3-3197">Az.KeyVault</span></span>
* <span data-ttu-id="d29f3-3198">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3198">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d29f3-3199">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d29f3-3199">Az.LogicApp</span></span>
* <span data-ttu-id="d29f3-3200">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3200">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="d29f3-3201">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3201">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="d29f3-3202">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="d29f3-3202">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="d29f3-3203">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="d29f3-3203">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="d29f3-3204">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="d29f3-3204">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="d29f3-3205">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="d29f3-3205">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="d29f3-3206">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3206">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="d29f3-3207">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="d29f3-3207">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="d29f3-3208">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="d29f3-3208">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="d29f3-3209">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="d29f3-3209">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="d29f3-3210">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="d29f3-3210">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="d29f3-3211">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3211">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="d29f3-3212">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3212">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d29f3-3213">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d29f3-3213">Az.Monitor</span></span>
* <span data-ttu-id="d29f3-3214">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3214">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d29f3-3215">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d29f3-3215">Az.Network</span></span>
* <span data-ttu-id="d29f3-3216">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3216">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d29f3-3217">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d29f3-3217">Az.OperationalInsights</span></span>
* <span data-ttu-id="d29f3-3218">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3218">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="d29f3-3219">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3219">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="d29f3-3220">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3220">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d29f3-3221">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-3221">Az.Resources</span></span>
* <span data-ttu-id="d29f3-3222">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3222">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="d29f3-3223">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3223">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="d29f3-3224">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3224">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="d29f3-3225">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3225">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="d29f3-3226">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-3226">Az.Sql</span></span>
* <span data-ttu-id="d29f3-3227">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3227">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="d29f3-3228">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3228">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d29f3-3229">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d29f3-3229">Az.Websites</span></span>
* <span data-ttu-id="d29f3-3230">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3230">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="d29f3-3231">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3231">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d29f3-3232">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d29f3-3232">Az.Accounts</span></span>
* <span data-ttu-id="d29f3-3233">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="d29f3-3233">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d29f3-3234">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-3234">Az.AnalysisServices</span></span>
<span data-ttu-id="d29f3-3235">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3235">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d29f3-3236">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-3236">Az.Compute</span></span>
* <span data-ttu-id="d29f3-3237">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3237">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="d29f3-3238">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3238">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="d29f3-3239">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3239">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d29f3-3240">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-3240">Az.RecoveryServices</span></span>
<span data-ttu-id="d29f3-3241">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3241">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d29f3-3242">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-3242">Az.Resources</span></span>
* <span data-ttu-id="d29f3-3243">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3243">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="d29f3-3244">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3244">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="d29f3-3245">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3245">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="d29f3-3246">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3246">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="d29f3-3247">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-3247">Az.Sql</span></span>
* <span data-ttu-id="d29f3-3248">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3248">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="d29f3-3249">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3249">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="d29f3-3250">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3250">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="d29f3-3251">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3251">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d29f3-3252">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d29f3-3252">Az.Accounts</span></span>
* <span data-ttu-id="d29f3-3253">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3253">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d29f3-3254">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-3254">Az.AnalysisServices</span></span>
* <span data-ttu-id="d29f3-3255">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3255">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d29f3-3256">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-3256">Az.RecoveryServices</span></span>
* <span data-ttu-id="d29f3-3257">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3257">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="d29f3-3258">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3258">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d29f3-3259">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d29f3-3259">Az.Accounts</span></span>
* <span data-ttu-id="d29f3-3260">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3260">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d29f3-3261">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3261">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d29f3-3262">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3262">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="d29f3-3263">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="d29f3-3263">Az.Aks</span></span>
* <span data-ttu-id="d29f3-3264">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3264">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d29f3-3265">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d29f3-3265">Az.Automation</span></span>
* <span data-ttu-id="d29f3-3266">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3266">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="d29f3-3267">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3267">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d29f3-3268">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d29f3-3268">Az.Cdn</span></span>
* <span data-ttu-id="d29f3-3269">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3269">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d29f3-3270">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-3270">Az.Compute</span></span>
* <span data-ttu-id="d29f3-3271">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3271">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="d29f3-3272">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3272">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="d29f3-3273">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3273">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="d29f3-3274">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d29f3-3274">Az.ContainerRegistry</span></span>
* <span data-ttu-id="d29f3-3275">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3275">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d29f3-3276">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d29f3-3276">Az.DataFactory</span></span>
* <span data-ttu-id="d29f3-3277">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3277">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d29f3-3278">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d29f3-3278">Az.DataLakeStore</span></span>
* <span data-ttu-id="d29f3-3279">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3279">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="d29f3-3280">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3280">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="d29f3-3281">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3281">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d29f3-3282">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d29f3-3282">Az.IotHub</span></span>
* <span data-ttu-id="d29f3-3283">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3283">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d29f3-3284">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d29f3-3284">Az.KeyVault</span></span>
* <span data-ttu-id="d29f3-3285">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3285">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d29f3-3286">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d29f3-3286">Az.Network</span></span>
* <span data-ttu-id="d29f3-3287">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3287">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="d29f3-3288">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-3288">Az.Resources</span></span>
* <span data-ttu-id="d29f3-3289">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3289">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="d29f3-3290">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3290">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="d29f3-3291">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3291">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="d29f3-3292">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3292">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="d29f3-3293">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3293">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="d29f3-3294">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3294">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="d29f3-3295">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3295">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d29f3-3296">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d29f3-3296">Az.ServiceFabric</span></span>
* <span data-ttu-id="d29f3-3297">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3297">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="d29f3-3298">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3298">Fix some error messages.</span></span>
* <span data-ttu-id="d29f3-3299">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3299">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="d29f3-3300">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3300">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="d29f3-3301">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="d29f3-3301">Az.SignalR</span></span>
* <span data-ttu-id="d29f3-3302">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3302">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="d29f3-3303">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-3303">Az.Sql</span></span>
* <span data-ttu-id="d29f3-3304">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3304">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d29f3-3305">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3305">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="d29f3-3306">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3306">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="d29f3-3307">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3307">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d29f3-3308">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d29f3-3308">Az.Storage</span></span>
* <span data-ttu-id="d29f3-3309">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3309">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d29f3-3310">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3310">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="d29f3-3311">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="d29f3-3311">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="d29f3-3312">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="d29f3-3312">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="d29f3-3313">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="d29f3-3313">Az.TrafficManager</span></span>
* <span data-ttu-id="d29f3-3314">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3314">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d29f3-3315">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d29f3-3315">Az.Websites</span></span>
* <span data-ttu-id="d29f3-3316">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3316">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d29f3-3317">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3317">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="d29f3-3318">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3318">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="d29f3-3319">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3319">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d29f3-3320">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d29f3-3320">Az.Accounts</span></span>
* <span data-ttu-id="d29f3-3321">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3321">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d29f3-3322">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-3322">Az.Compute</span></span>
* <span data-ttu-id="d29f3-3323">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3323">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="d29f3-3324">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3324">Updated the description of ID in help files</span></span>
* <span data-ttu-id="d29f3-3325">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3325">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d29f3-3326">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d29f3-3326">Az.DataLakeStore</span></span>
* <span data-ttu-id="d29f3-3327">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3327">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="d29f3-3328">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3328">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d29f3-3329">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d29f3-3329">Az.EventGrid</span></span>
* <span data-ttu-id="d29f3-3330">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3330">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="d29f3-3331">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3331">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="d29f3-3332">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="d29f3-3332">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="d29f3-3333">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="d29f3-3333">Event Time-To-Live,</span></span>
        - <span data-ttu-id="d29f3-3334">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="d29f3-3334">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="d29f3-3335">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3335">Dead letter endpoint.</span></span>
    - <span data-ttu-id="d29f3-3336">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="d29f3-3336">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="d29f3-3337">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="d29f3-3337">Event Time-To-Live,</span></span>
        - <span data-ttu-id="d29f3-3338">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="d29f3-3338">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="d29f3-3339">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3339">Dead letter endpoint.</span></span>
* <span data-ttu-id="d29f3-3340">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3340">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="d29f3-3341">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3341">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d29f3-3342">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d29f3-3342">Az.IotHub</span></span>
* <span data-ttu-id="d29f3-3343">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3343">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d29f3-3344">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d29f3-3344">Az.LogicApp</span></span>
* <span data-ttu-id="d29f3-3345">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3345">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="d29f3-3346">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-3346">Az.Resources</span></span>
* <span data-ttu-id="d29f3-3347">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="d29f3-3347">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="d29f3-3348">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3348">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="d29f3-3349">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3349">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="d29f3-3350">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3350">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="d29f3-3351">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="d29f3-3351">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="d29f3-3352">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3352">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="d29f3-3353">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="d29f3-3353">Az.SignalR</span></span>
* <span data-ttu-id="d29f3-3354">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3354">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="d29f3-3355">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-3355">Az.Sql</span></span>
* <span data-ttu-id="d29f3-3356">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3356">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d29f3-3357">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d29f3-3357">Az.Storage</span></span>
* <span data-ttu-id="d29f3-3358">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3358">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="d29f3-3359">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d29f3-3359">New-AzStorageContext</span></span>
* <span data-ttu-id="d29f3-3360">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3360">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="d29f3-3361">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="d29f3-3361">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d29f3-3362">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d29f3-3362">Az.Websites</span></span>
* <span data-ttu-id="d29f3-3363">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="d29f3-3363">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="d29f3-3364">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3364">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="d29f3-3365">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3365">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="d29f3-3366">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="d29f3-3366">General</span></span>

- <span data-ttu-id="d29f3-3367">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3367">General Availability of Az Module</span></span>
- <span data-ttu-id="d29f3-3368">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3368">Online help for each module</span></span>
- <span data-ttu-id="d29f3-3369">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="d29f3-3369">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="d29f3-3370">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="d29f3-3370">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="d29f3-3371">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d29f3-3371">Az.Accounts</span></span>
- <span data-ttu-id="d29f3-3372">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3372">Changed from Az.Profile</span></span>
- <span data-ttu-id="d29f3-3373">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3373">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="d29f3-3374">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d29f3-3374">Az.ApiManagement</span></span>
- <span data-ttu-id="d29f3-3375">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3375">Fixes for #7002</span></span>
- <span data-ttu-id="d29f3-3376">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="d29f3-3376">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="d29f3-3377">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d29f3-3377">Az.Batch</span></span>
- <span data-ttu-id="d29f3-3378">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3378">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="d29f3-3379">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3379">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="d29f3-3380">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="d29f3-3380">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="d29f3-3381">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="d29f3-3381">Az.Billing</span></span>
- <span data-ttu-id="d29f3-3382">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="d29f3-3382">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="d29f3-3383">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-3383">Az.CognitivServices</span></span>
- <span data-ttu-id="d29f3-3384">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3384">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="d29f3-3385">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3385">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="d29f3-3386">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d29f3-3386">Az.ContainerInstance</span></span>
- <span data-ttu-id="d29f3-3387">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3387">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="d29f3-3388">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="d29f3-3388">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="d29f3-3389">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="d29f3-3389">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="d29f3-3390">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d29f3-3390">Az.DataLakeStore</span></span>
- <span data-ttu-id="d29f3-3391">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="d29f3-3391">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="d29f3-3392">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d29f3-3392">Az.Monitor</span></span>
- <span data-ttu-id="d29f3-3393">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="d29f3-3393">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="d29f3-3394">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d29f3-3394">Az.KeyVault</span></span>
- <span data-ttu-id="d29f3-3395">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="d29f3-3395">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="d29f3-3396">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="d29f3-3396">Az.MachineLearning</span></span>
- <span data-ttu-id="d29f3-3397">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="d29f3-3397">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="d29f3-3398">Az.Media</span><span class="sxs-lookup"><span data-stu-id="d29f3-3398">Az.Media</span></span>
- <span data-ttu-id="d29f3-3399">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="d29f3-3399">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="d29f3-3400">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d29f3-3400">Az.Network</span></span>
<span data-ttu-id="d29f3-3401">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="d29f3-3401">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="d29f3-3402">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="d29f3-3402">New cmdlets added:</span></span>
        - <span data-ttu-id="d29f3-3403">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d29f3-3403">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d29f3-3404">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d29f3-3404">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d29f3-3405">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d29f3-3405">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d29f3-3406">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d29f3-3406">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d29f3-3407">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d29f3-3407">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d29f3-3408">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="d29f3-3408">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="d29f3-3409">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="d29f3-3409">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="d29f3-3410">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="d29f3-3410">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="d29f3-3411">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d29f3-3411">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="d29f3-3412">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d29f3-3412">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="d29f3-3413">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d29f3-3413">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="d29f3-3414">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d29f3-3414">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="d29f3-3415">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d29f3-3415">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="d29f3-3416">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d29f3-3416">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="d29f3-3417">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3417">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="d29f3-3418">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="d29f3-3418">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="d29f3-3419">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d29f3-3419">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="d29f3-3420">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d29f3-3420">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="d29f3-3421">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d29f3-3421">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="d29f3-3422">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="d29f3-3422">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="d29f3-3423">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="d29f3-3423">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="d29f3-3424">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d29f3-3424">Az.OperationalInsights</span></span>
- <span data-ttu-id="d29f3-3425">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="d29f3-3425">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="d29f3-3426">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d29f3-3426">Az.Profile</span></span>
- <span data-ttu-id="d29f3-3427">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3427">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="d29f3-3428">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-3428">Az.RecoveryServices</span></span>
- <span data-ttu-id="d29f3-3429">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="d29f3-3429">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="d29f3-3430">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-3430">Az.Resources</span></span>
- <span data-ttu-id="d29f3-3431">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="d29f3-3431">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="d29f3-3432">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d29f3-3432">Az.ServiceFabric</span></span>
- <span data-ttu-id="d29f3-3433">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="d29f3-3433">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="d29f3-3434">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="d29f3-3434">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="d29f3-3435">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="d29f3-3435">Az.SIgnalR</span></span>
- <span data-ttu-id="d29f3-3436">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="d29f3-3436">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="d29f3-3437">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-3437">Az.Sql</span></span>
- <span data-ttu-id="d29f3-3438">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="d29f3-3438">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="d29f3-3439">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-3439">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="d29f3-3440">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="d29f3-3440">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="d29f3-3441">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d29f3-3441">Az.Storage</span></span>
- <span data-ttu-id="d29f3-3442">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="d29f3-3442">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="d29f3-3443">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d29f3-3443">Az.Websites</span></span>
- <span data-ttu-id="d29f3-3444">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="d29f3-3444">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="d29f3-3445">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3445">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="d29f3-3446">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="d29f3-3446">General</span></span>

* <span data-ttu-id="d29f3-3447">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="d29f3-3447">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="d29f3-3448">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-3448">Az.Compute</span></span>

* <span data-ttu-id="d29f3-3449">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3449">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="d29f3-3450">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d29f3-3450">Az.DataLakeStore</span></span>

* <span data-ttu-id="d29f3-3451">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="d29f3-3451">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="d29f3-3452">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d29f3-3452">Az.FrontDoor</span></span>

* <span data-ttu-id="d29f3-3453">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="d29f3-3453">Fixed some broken links</span></span>
    - <span data-ttu-id="d29f3-3454">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3454">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="d29f3-3455">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3455">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="d29f3-3456">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-3456">Az.RecoveryServices</span></span>

* <span data-ttu-id="d29f3-3457">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3457">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="d29f3-3458">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3458">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="d29f3-3459">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-3459">Az.Resources</span></span>

* <span data-ttu-id="d29f3-3460">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3460">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="d29f3-3461">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3461">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="d29f3-3462">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-3462">Az.Sql</span></span>

* <span data-ttu-id="d29f3-3463">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="d29f3-3463">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="d29f3-3464">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3464">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="d29f3-3465">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3465">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="d29f3-3466">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d29f3-3466">Az.Storage</span></span>

* <span data-ttu-id="d29f3-3467">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d29f3-3467">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="d29f3-3468">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="d29f3-3468">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="d29f3-3469">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="d29f3-3469">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="d29f3-3470">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="d29f3-3470">Support Static Website configuration</span></span>
    - <span data-ttu-id="d29f3-3471">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="d29f3-3471">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="d29f3-3472">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="d29f3-3472">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="d29f3-3473">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d29f3-3473">Az.Websites</span></span>

* <span data-ttu-id="d29f3-3474">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d29f3-3474">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="d29f3-3475">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3475">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="d29f3-3476">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3476">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="d29f3-3477">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3477">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="d29f3-3478">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d29f3-3478">Az.ApiManagement</span></span>
* <span data-ttu-id="d29f3-3479">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3479">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="d29f3-3480">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d29f3-3480">Az.Automation</span></span>
* <span data-ttu-id="d29f3-3481">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3481">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="d29f3-3482">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3482">Added Update Management cmdlets</span></span>
* <span data-ttu-id="d29f3-3483">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3483">Added Source Control cmdlets</span></span>
* <span data-ttu-id="d29f3-3484">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3484">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="d29f3-3485">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3485">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="d29f3-3486">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-3486">Az.Compute</span></span>
* <span data-ttu-id="d29f3-3487">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3487">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="d29f3-3488">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3488">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="d29f3-3489">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d29f3-3489">Az.ContainerInstance</span></span>
* <span data-ttu-id="d29f3-3490">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3490">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="d29f3-3491">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="d29f3-3491">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="d29f3-3492">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3492">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="d29f3-3493">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d29f3-3493">Az.Network</span></span>
* <span data-ttu-id="d29f3-3494">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3494">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="d29f3-3495">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3495">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="d29f3-3496">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3496">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="d29f3-3497">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3497">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="d29f3-3498">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="d29f3-3498">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="d29f3-3499">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3499">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="d29f3-3500">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3500">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="d29f3-3501">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="d29f3-3501">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="d29f3-3502">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3502">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="d29f3-3503">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3503">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="d29f3-3504">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="d29f3-3504">Az.Relay</span></span>
* <span data-ttu-id="d29f3-3505">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3505">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="d29f3-3506">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-3506">Az.Resources</span></span>
* <span data-ttu-id="d29f3-3507">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3507">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="d29f3-3508">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3508">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="d29f3-3509">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3509">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="d29f3-3510">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d29f3-3510">Az.ServiceFabric</span></span>
* <span data-ttu-id="d29f3-3511">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3511">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="d29f3-3512">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-3512">Az.Sql</span></span>
* <span data-ttu-id="d29f3-3513">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3513">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="d29f3-3514">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3514">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d29f3-3515">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3515">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d29f3-3516">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3516">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d29f3-3517">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3517">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d29f3-3518">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3518">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="d29f3-3519">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3519">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="d29f3-3520">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3520">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="d29f3-3521">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3521">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="d29f3-3522">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3522">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="d29f3-3523">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3523">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="d29f3-3524">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3524">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="d29f3-3525">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3525">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="d29f3-3526">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3526">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="d29f3-3527">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3527">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="d29f3-3528">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3528">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="d29f3-3529">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3529">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="d29f3-3530">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3530">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="d29f3-3531">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="d29f3-3531">General</span></span>
* <span data-ttu-id="d29f3-3532">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="d29f3-3532">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="d29f3-3533">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d29f3-3533">Az.Profile</span></span>
* <span data-ttu-id="d29f3-3534">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3534">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="d29f3-3535">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="d29f3-3535">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="d29f3-3536">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="d29f3-3536">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="d29f3-3537">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3537">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="d29f3-3538">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3538">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="d29f3-3539">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3539">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="d29f3-3540">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="d29f3-3540">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="d29f3-3541">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-3541">Az.CognitiveServices</span></span>
* <span data-ttu-id="d29f3-3542">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3542">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d29f3-3543">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-3543">Az.Compute</span></span>
* <span data-ttu-id="d29f3-3544">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="d29f3-3544">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="d29f3-3545">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="d29f3-3545">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="d29f3-3546">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3546">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d29f3-3547">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d29f3-3547">Az.DataLakeStore</span></span>
* <span data-ttu-id="d29f3-3548">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3548">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="d29f3-3549">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3549">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="d29f3-3550">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="d29f3-3550">Az.Insights</span></span>
* <span data-ttu-id="d29f3-3551">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="d29f3-3551">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="d29f3-3552">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="d29f3-3552">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="d29f3-3553">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="d29f3-3553">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="d29f3-3554">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3554">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d29f3-3555">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d29f3-3555">Az.Network</span></span>
* <span data-ttu-id="d29f3-3556">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="d29f3-3556">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="d29f3-3557">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="d29f3-3557">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="d29f3-3558">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="d29f3-3558">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="d29f3-3559">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="d29f3-3559">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="d29f3-3560">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="d29f3-3560">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="d29f3-3561">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="d29f3-3561">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="d29f3-3562">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="d29f3-3562">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d29f3-3563">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d29f3-3563">Az.PolicyInsights</span></span>
* <span data-ttu-id="d29f3-3564">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3564">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="d29f3-3565">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-3565">Az.Resources</span></span>
* <span data-ttu-id="d29f3-3566">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3566">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="d29f3-3567">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="d29f3-3567">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d29f3-3568">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d29f3-3568">Az.ServiceBus</span></span>
* <span data-ttu-id="d29f3-3569">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3569">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d29f3-3570">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d29f3-3570">Az.ServiceFabric</span></span>
* <span data-ttu-id="d29f3-3571">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3571">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="d29f3-3572">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="d29f3-3572">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="d29f3-3573">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="d29f3-3573">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="d29f3-3574">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="d29f3-3574">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="d29f3-3575">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3575">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="d29f3-3576">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3576">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="d29f3-3577">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d29f3-3577">Az.Profile</span></span>
* <span data-ttu-id="d29f3-3578">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="d29f3-3578">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="d29f3-3579">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3579">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d29f3-3580">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-3580">Az.Compute</span></span>
* <span data-ttu-id="d29f3-3581">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="d29f3-3581">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="d29f3-3582">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3582">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d29f3-3583">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d29f3-3583">Az.DataLakeStore</span></span>
* <span data-ttu-id="d29f3-3584">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="d29f3-3584">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="d29f3-3585">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3585">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="d29f3-3586">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3586">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="d29f3-3587">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3587">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="d29f3-3588">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3588">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d29f3-3589">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d29f3-3589">Az.Network</span></span>
* <span data-ttu-id="d29f3-3590">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3590">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="d29f3-3591">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3591">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d29f3-3592">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-3592">Az.Resources</span></span>
* <span data-ttu-id="d29f3-3593">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3593">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="d29f3-3594">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3594">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="d29f3-3595">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3595">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="d29f3-3596">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="d29f3-3596">Azure.Storage</span></span>
* <span data-ttu-id="d29f3-3597">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3597">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="d29f3-3598">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="d29f3-3598">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="d29f3-3599">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="d29f3-3599">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="d29f3-3600">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3600">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="d29f3-3601">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="d29f3-3601">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d29f3-3602">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d29f3-3602">Az.CognitiveServices</span></span>
* <span data-ttu-id="d29f3-3603">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3603">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d29f3-3604">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d29f3-3604">Az.Compute</span></span>
* <span data-ttu-id="d29f3-3605">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="d29f3-3605">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="d29f3-3606">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3606">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="d29f3-3607">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3607">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="d29f3-3608">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="d29f3-3608">Az.DataFactoryV2</span></span>
* <span data-ttu-id="d29f3-3609">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3609">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d29f3-3610">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d29f3-3610">Az.Network</span></span>
* <span data-ttu-id="d29f3-3611">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3611">Added NetworkProfile functionality.</span></span> <span data-ttu-id="d29f3-3612">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="d29f3-3612">new cmdlets added</span></span>
    - <span data-ttu-id="d29f3-3613">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d29f3-3613">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="d29f3-3614">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d29f3-3614">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="d29f3-3615">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d29f3-3615">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="d29f3-3616">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d29f3-3616">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="d29f3-3617">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="d29f3-3617">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="d29f3-3618">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="d29f3-3618">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="d29f3-3619">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3619">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="d29f3-3620">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="d29f3-3620">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="d29f3-3621">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="d29f3-3621">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="d29f3-3622">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d29f3-3622">Az.RedisCache</span></span>
* <span data-ttu-id="d29f3-3623">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3623">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="d29f3-3624">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3624">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="d29f3-3625">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d29f3-3625">Az.Resources</span></span>
* <span data-ttu-id="d29f3-3626">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d29f3-3626">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="d29f3-3627">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="d29f3-3627">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="d29f3-3628">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d29f3-3628">Az.Sql</span></span>
* <span data-ttu-id="d29f3-3629">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3629">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d29f3-3630">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d29f3-3630">Az.Websites</span></span>
* <span data-ttu-id="d29f3-3631">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="d29f3-3631">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="d29f3-3632">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="d29f3-3632">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="d29f3-3633">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="d29f3-3633">0.2.0 - September 2018</span></span>
 <span data-ttu-id="d29f3-3634">Начальный выпуск</span><span class="sxs-lookup"><span data-stu-id="d29f3-3634">Initial Release</span></span>
