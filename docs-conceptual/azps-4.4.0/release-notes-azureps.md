---
title: Заметки о выпуске Azure PowerShell
description: Узнайте обо всех последних обновлениях модулей Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: 88e9c622ef3608b17e6cd8d4ce8c193812a97520
ms.sourcegitcommit: 23e5b2b0751777ef0a5ca74e40c7772653e339a3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/14/2020
ms.locfileid: "86382350"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="30387-103">Заметки о выпуске Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="30387-103">Azure PowerShell release notes</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="30387-104">4.4.0 — июль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="30387-104">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="30387-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30387-105">Az.Accounts</span></span>
* <span data-ttu-id="30387-106">Добавлен новый командлет Invoke-AzRestMethod.</span><span class="sxs-lookup"><span data-stu-id="30387-106">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="30387-107">Устранена неполадка, из-за которой могли возникать ошибки с проверкой подлинности в сценариях с несколькими процессами, такими как выполнение нескольких командлетов Azure PowerShell с помощью Start-Job [№ 9448].</span><span class="sxs-lookup"><span data-stu-id="30387-107">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="30387-108">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="30387-108">Az.Aks</span></span>
* <span data-ttu-id="30387-109">Исправлена ошибка, из-за которой Get-AzAks выводит не все кластеры [ №12296].</span><span class="sxs-lookup"><span data-stu-id="30387-109">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="30387-110">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="30387-110">Az.AnalysisServices</span></span>
* <span data-ttu-id="30387-111">Удалена ссылка на проект для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="30387-111">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="30387-112">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="30387-112">Az.Automation</span></span>
* <span data-ttu-id="30387-113">Исправлена ошибка, из-за которой строка с escape-символами не преобразовывалась в объект JSON.</span><span class="sxs-lookup"><span data-stu-id="30387-113">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30387-114">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30387-114">Az.Compute</span></span>
* <span data-ttu-id="30387-115">Добавлено предупреждение, которое отображается при использовании New-AzVmss, если версия образа не является последней.</span><span class="sxs-lookup"><span data-stu-id="30387-115">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="30387-116">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="30387-116">Az.DataFactory</span></span>
* <span data-ttu-id="30387-117">Добавлены глобальные параметры в Фабрику данных.</span><span class="sxs-lookup"><span data-stu-id="30387-117">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="30387-118">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="30387-118">Az.EventGrid</span></span>
* <span data-ttu-id="30387-119">Обновлен модуль для использования API версии 2020-06-01.</span><span class="sxs-lookup"><span data-stu-id="30387-119">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="30387-120">Добавлены новые возможности:</span><span class="sxs-lookup"><span data-stu-id="30387-120">Added new features:</span></span>
    - <span data-ttu-id="30387-121">сопоставление входных данных;</span><span class="sxs-lookup"><span data-stu-id="30387-121">Input mapping</span></span>
    - <span data-ttu-id="30387-122">схема доставки событий;</span><span class="sxs-lookup"><span data-stu-id="30387-122">Event Delivery Schema</span></span>
    - <span data-ttu-id="30387-123">Приватный канал</span><span class="sxs-lookup"><span data-stu-id="30387-123">Private Link</span></span>
    - <span data-ttu-id="30387-124">схема событий облака (версия 1.0);</span><span class="sxs-lookup"><span data-stu-id="30387-124">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="30387-125">раздел служебной шины как назначение;</span><span class="sxs-lookup"><span data-stu-id="30387-125">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="30387-126">функция Azure как назначение;</span><span class="sxs-lookup"><span data-stu-id="30387-126">Azure Function As Destination</span></span>
    - <span data-ttu-id="30387-127">пакетная обработка данных веб-перехватчика;</span><span class="sxs-lookup"><span data-stu-id="30387-127">WebHook Batching</span></span>
    - <span data-ttu-id="30387-128">безопасный веб-перехватчик (поддержка AAD);</span><span class="sxs-lookup"><span data-stu-id="30387-128">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="30387-129">фильтрация IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="30387-129">IpFiltering</span></span>
* <span data-ttu-id="30387-130">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="30387-130">Updated cmdlets:</span></span>
    - <span data-ttu-id="30387-131">New-AzEventGridSubscription или Update-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="30387-131">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="30387-132">Добавлены новые необязательные параметры для поддержки пакетной обработки данных веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="30387-132">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="30387-133">Добавлены новые необязательные параметры для поддержки безопасного веб-перехватчика с использованием AAD.</span><span class="sxs-lookup"><span data-stu-id="30387-133">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="30387-134">Добавлено новое перечисление для параметра EndpointType, чтобы обеспечить поддержку функции Azure и раздела служебной шины в качестве назначения.</span><span class="sxs-lookup"><span data-stu-id="30387-134">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="30387-135">Добавлен новый необязательный параметр для схемы доставки.</span><span class="sxs-lookup"><span data-stu-id="30387-135">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="30387-136">New-AzEventGridTopic или Update-AzEventGridTopic и New-AzEventGridDomain или Update-AzEventGridDomain:</span><span class="sxs-lookup"><span data-stu-id="30387-136">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="30387-137">Добавлены новые необязательные параметры для поддержки фильтрации IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="30387-137">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="30387-138">New-AzEventGridTopic или New-AzEventGridDomain:</span><span class="sxs-lookup"><span data-stu-id="30387-138">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="30387-139">Добавлены новые необязательные параметры для поддержки сопоставления входных данных.</span><span class="sxs-lookup"><span data-stu-id="30387-139">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="30387-140">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="30387-140">Az.FrontDoor</span></span>
* <span data-ttu-id="30387-141">Обновлен модуль для использования API версии 2020-05-01.</span><span class="sxs-lookup"><span data-stu-id="30387-141">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="30387-142">Включена поддержка Приватного канала для ресурсов службы хранилища, Key Vault и службы веб-приложений.</span><span class="sxs-lookup"><span data-stu-id="30387-142">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="30387-143">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="30387-143">Az.HDInsight</span></span>
* <span data-ttu-id="30387-144">Включена поддержка создания кластера с хранилищем ADLS 1-го и 2-го поколения в национальных облаках.</span><span class="sxs-lookup"><span data-stu-id="30387-144">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="30387-145">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="30387-145">Az.Monitor</span></span>
* <span data-ttu-id="30387-146">Исправлена ошибка с Get-AzDiagnosticSetting, связанная с присвоением значения NULL метрикам или журналам [№ 12272].</span><span class="sxs-lookup"><span data-stu-id="30387-146">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30387-147">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30387-147">Az.Network</span></span>
* <span data-ttu-id="30387-148">Исправлены ошибки с переключением параметров для подключения виртуальной сети концентратора к глобальной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="30387-148">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="30387-149">Добавлены новые командлеты для сайтов сетевых виртуальных модулей Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-149">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="30387-150">Get-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="30387-150">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="30387-151">New-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="30387-151">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="30387-152">Remove-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="30387-152">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="30387-153">Update-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="30387-153">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="30387-154">New-AzOffice365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="30387-154">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="30387-155">Добавлены новые командлеты для сетевого виртуального модуля Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-155">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="30387-156">Get-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="30387-156">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="30387-157">New-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="30387-157">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="30387-158">Remove-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="30387-158">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="30387-159">Update-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="30387-159">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="30387-160">Get-AzNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="30387-160">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="30387-161">New-AzVirtualApplianceSkuProperty</span><span class="sxs-lookup"><span data-stu-id="30387-161">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="30387-162">Общие командлеты для Шлюза приложений, подключенного к Приватному каналу.</span><span class="sxs-lookup"><span data-stu-id="30387-162">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="30387-163">Общие командлеты для службы синхронизации хранилища, подключенной к Приватному каналу.</span><span class="sxs-lookup"><span data-stu-id="30387-163">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="30387-164">Общие командлеты для службы SignalR, подключенной к Приватному каналу.</span><span class="sxs-lookup"><span data-stu-id="30387-164">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="30387-165">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="30387-165">Az.RecoveryServices</span></span>
* <span data-ttu-id="30387-166">Удалена ссылка на проект для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="30387-166">Removed project reference to Authentication</span></span>
* <span data-ttu-id="30387-167">В Azure Backup представлена более точная справка по командлетам.</span><span class="sxs-lookup"><span data-stu-id="30387-167">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="30387-168">В Azure Backup включена поддержка выборки заданий агента MAB с помощью командлета Get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="30387-168">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="30387-169">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30387-169">Az.Resources</span></span>
* <span data-ttu-id="30387-170">Обновлен командлет Save-AzResourceGroupDeploymentTemplate для использования пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="30387-170">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="30387-171">Добавлен командлет Unregister-AzResourceProvider.</span><span class="sxs-lookup"><span data-stu-id="30387-171">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="30387-172">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30387-172">Az.Sql</span></span>
* <span data-ttu-id="30387-173">Включена поддержка субъекта-службы и гостевых пользователей для командлета Set-AzSqlInstanceActiveDirectoryAdministrator.</span><span class="sxs-lookup"><span data-stu-id="30387-173">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="30387-174">Исправлена ошибка в командлетах классификации данных.</span><span class="sxs-lookup"><span data-stu-id="30387-174">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="30387-175">Включена поддержка отработки отказа Управляемого экземпляра SQL Azure. Invoke-AzSqlInstanceFailover</span><span class="sxs-lookup"><span data-stu-id="30387-175">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="30387-176">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="30387-176">Az.Storage</span></span>
* <span data-ttu-id="30387-177">Исправлена ошибка, из-за которой в некоторых командлетах плоскости данных не добавлялся объект UserAgent.</span><span class="sxs-lookup"><span data-stu-id="30387-177">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="30387-178">Включена поддержка создания и обновления учетной записи хранения с использованием MinimumTlsVersion и AllowBlobPublicAccess.</span><span class="sxs-lookup"><span data-stu-id="30387-178">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="30387-179">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30387-179">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="30387-180">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30387-180">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="30387-181">Включена поддержка включения и отключения управления версиями в службе BLOB-объектов учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="30387-181">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="30387-182">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="30387-182">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="30387-183">Включена поддержка вывода списка BLOB-объектов с данными о версиях BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="30387-183">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="30387-184">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="30387-184">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="30387-185">Включена поддержка получения или удаления одного моментального снимка BLOB-объекта или версии BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="30387-185">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="30387-186">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="30387-186">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="30387-187">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="30387-187">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="30387-188">Включена поддержка конвейера на основе BLOB-объекта, созданного с помощью Azure.Storage.Blobs версии 12.</span><span class="sxs-lookup"><span data-stu-id="30387-188">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="30387-189">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="30387-189">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="30387-190">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="30387-190">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="30387-191">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="30387-191">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="30387-192">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="30387-192">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="30387-193">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="30387-193">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="30387-194">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="30387-194">Az.StorageSync</span></span>
* <span data-ttu-id="30387-195">Добавлена новая версия пакета SDK StorageSync, предназначенная для API версии 2020-03-01.</span><span class="sxs-lookup"><span data-stu-id="30387-195">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="30387-196">Добавлен командлет для обновления службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="30387-196">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="30387-197">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="30387-197">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="30387-198">Добавлены классы IncomingTrafficPolicy и IncomingTrafficPolicy в командлеты службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="30387-198">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="30387-199">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="30387-199">Az.Websites</span></span>
* <span data-ttu-id="30387-200">Включена поддержка выполнения операций для слотов, которые находятся не в той же группе ресурсов, что и план службы приложений.</span><span class="sxs-lookup"><span data-stu-id="30387-200">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="30387-201">4.3.0 — июнь 2020 года</span><span class="sxs-lookup"><span data-stu-id="30387-201">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="30387-202">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30387-202">Az.Accounts</span></span>
* <span data-ttu-id="30387-203">Включена поддержка обнаружения параметров среды по умолчанию и добавления окружения с помощью командлета Add-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="30387-203">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="30387-204">Обновлены предварительно загруженные сборки [№ 12024], [№ 11976].</span><span class="sxs-lookup"><span data-stu-id="30387-204">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="30387-205">Обновлена сборка Azure.Core.</span><span class="sxs-lookup"><span data-stu-id="30387-205">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="30387-206">Исправлена ошибка, из-за которой выполнение Connect-AzAccount может завершаться сбоем при многопоточном выполнении [№ 11201].</span><span class="sxs-lookup"><span data-stu-id="30387-206">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="30387-207">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="30387-207">Az.Aks</span></span>
* <span data-ttu-id="30387-208">Заменено использование старого [API AccessProfile](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) вызовами API [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) и [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials).</span><span class="sxs-lookup"><span data-stu-id="30387-208">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="30387-209">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="30387-209">Az.Batch</span></span>
* <span data-ttu-id="30387-210">Изменена версия SDK для Microsoft.Azure.Management.Batch для Az.Batch на 11.0.0.</span><span class="sxs-lookup"><span data-stu-id="30387-210">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="30387-211">Включена возможность задать удостоверение BatchAccount в командлете New-AzBatchAccount.</span><span class="sxs-lookup"><span data-stu-id="30387-211">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="30387-212">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="30387-212">Az.CognitiveServices</span></span>
* <span data-ttu-id="30387-213">Включена поддержка отображения возможностей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="30387-213">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="30387-214">Включена поддержка изменения PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="30387-214">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30387-215">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30387-215">Az.Compute</span></span>
* <span data-ttu-id="30387-216">Добавлен параметр SimulateEviction в командлеты Set-AzVM и Set-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="30387-216">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="30387-217">Добавлен фрагмент Premium_LRS в средство заполнения аргументов параметра StorageAccountType для командлета New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="30387-217">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="30387-218">Добавлены подсостояния для VMCustomScriptExtension [№ 11297].</span><span class="sxs-lookup"><span data-stu-id="30387-218">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="30387-219">Добавлен фрагмент Delete в средство заполнения аргументов параметра EvictionPolicy для командлетов New-AzVM и New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="30387-219">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="30387-220">Исправлено имя нового расширения виртуальной машины для SAP.</span><span class="sxs-lookup"><span data-stu-id="30387-220">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="30387-221">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="30387-221">Az.DataFactory</span></span>
* <span data-ttu-id="30387-222">Обновлен пакет SDK ADF для .NET до версии 4.9.0.</span><span class="sxs-lookup"><span data-stu-id="30387-222">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="30387-223">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="30387-223">Az.EventHub</span></span>
* <span data-ttu-id="30387-224">Добавлены параметры управляемого удостоверения для командлетов New-AzEventHubNamespace и Set-AzEventHubNamespace.</span><span class="sxs-lookup"><span data-stu-id="30387-224">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="30387-225">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="30387-225">Az.Functions</span></span>
* <span data-ttu-id="30387-226">Включена поддержка создания приложений-функций PowerShell 7.0 и Java 11.</span><span class="sxs-lookup"><span data-stu-id="30387-226">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="30387-227">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="30387-227">Az.HDInsight</span></span>
* <span data-ttu-id="30387-228">Включена поддержка перечисления узлов и перезагрузка отдельных узлов кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="30387-228">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="30387-229">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="30387-229">Az.HealthcareApis</span></span>
* <span data-ttu-id="30387-230">Обновлен пакет SDK до версии 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="30387-230">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="30387-231">Включена поддержка параметров экспорта и управляемого удостоверения.</span><span class="sxs-lookup"><span data-stu-id="30387-231">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="30387-232">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="30387-232">Az.Monitor</span></span>
* <span data-ttu-id="30387-233">Исправлен входной параметр объекта для Set-AzActivityLogAlert.</span><span class="sxs-lookup"><span data-stu-id="30387-233">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="30387-234">Исправлен параметр InputObject для Set-AzActionGroup [№ 10868].</span><span class="sxs-lookup"><span data-stu-id="30387-234">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30387-235">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30387-235">Az.Network</span></span>
* <span data-ttu-id="30387-236">Включена поддержка параметра AddressPrefixType в Remove-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="30387-236">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="30387-237">Добавлены новые командлеты для политики Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-237">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="30387-238">New-AzFirewallPolicyDnsSetting</span><span class="sxs-lookup"><span data-stu-id="30387-238">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="30387-239">Включена поддержка полного доменного имени назначения в правилах сети для политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="30387-239">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="30387-240">Включена поддержка операций серверного пула адресов:</span><span class="sxs-lookup"><span data-stu-id="30387-240">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="30387-241">New-AzLoadBalancerBackendAddressConfig</span><span class="sxs-lookup"><span data-stu-id="30387-241">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="30387-242">New-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="30387-242">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="30387-243">Set-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="30387-243">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="30387-244">Remove-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="30387-244">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="30387-245">Get-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="30387-245">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="30387-246">Добавлена проверка имени для New-AzIpGroup.</span><span class="sxs-lookup"><span data-stu-id="30387-246">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="30387-247">Добавлены новые командлеты для политики Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-247">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="30387-248">New-AzFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="30387-248">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="30387-249">Обновлены следующие команды для функции: Включена возможность настройки и удаления пользовательских DNS-серверов в шлюзе VPN P2S виртуальной глобальной сети.</span><span class="sxs-lookup"><span data-stu-id="30387-249">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="30387-250">Обновлен командлет New-AzP2sVpnGateway: добавлен необязательный параметр -CustomDnsServer, чтобы пользователи могли указывать свои DNS-серверы для настройки в шлюзе VPN P2S для использования клиентами с подключением "точка — сеть".</span><span class="sxs-lookup"><span data-stu-id="30387-250">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="30387-251">Обновлен командлет Update-AzP2sVpnGateway: добавлен необязательный параметр -CustomDnsServer, чтобы пользователи могли указывать свои DNS-серверы для настройки в шлюзе VPN P2S для использования клиентами с подключением "точка — сеть".</span><span class="sxs-lookup"><span data-stu-id="30387-251">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="30387-252">Обновлен командлет Update-AzVpnGateway:</span><span class="sxs-lookup"><span data-stu-id="30387-252">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="30387-253">добавлен необязательный параметр -BgpPeeringAddress, чтобы клиенты могли указывать пользовательские маршруты BGP для настройки в шлюзе VPN.</span><span class="sxs-lookup"><span data-stu-id="30387-253">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="30387-254">Добавлен новый командлет для сброса состояния маршрутизации ресурса VirtualHub:</span><span class="sxs-lookup"><span data-stu-id="30387-254">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="30387-255">Reset-AzHubRouter</span><span class="sxs-lookup"><span data-stu-id="30387-255">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="30387-256">Следующие обновления основаны на последнем изменении Swagger для политики брандмауэра:</span><span class="sxs-lookup"><span data-stu-id="30387-256">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="30387-257">изменены имена для RuleGroup, RuleCollectionGroup и RuleType;</span><span class="sxs-lookup"><span data-stu-id="30387-257">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="30387-258">включена поддержка коллекций правил NAT политики брандмауэра для поддержки нескольких коллекций правил NAT.</span><span class="sxs-lookup"><span data-stu-id="30387-258">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="30387-259">[Критическое изменение] Добавлен обязательный параметр SourceIpGroup для командлетов New-AzFirewallPolicyApplicationRule и New-AzFirewallPolicyNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="30387-259">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="30387-260">[Критическое изменение] Параметр SourceAddress для командлета New-AzFirewallPolicyApplicationRule сделан обязательным.</span><span class="sxs-lookup"><span data-stu-id="30387-260">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="30387-261">[Критическое изменение] Параметр SourceAddress для командлета New-AzFirewallPolicyApplicationRule сделан обязательным.</span><span class="sxs-lookup"><span data-stu-id="30387-261">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="30387-262">[Критическое изменение] Удалены обязательные параметры: TranslatedAddress и TranslatedPort для командлета New-AzFirewallPolicyNatRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="30387-262">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="30387-263">Добавлены новые командлеты для поддержки Приватного канала в Шлюзе приложений:</span><span class="sxs-lookup"><span data-stu-id="30387-263">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="30387-264">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="30387-264">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="30387-265">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="30387-265">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="30387-266">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="30387-266">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="30387-267">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="30387-267">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="30387-268">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="30387-268">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="30387-269">New-AzApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="30387-269">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="30387-270">Добавлены новые командлеты для дочернего ресурса HubRouteTables VirtualHub:</span><span class="sxs-lookup"><span data-stu-id="30387-270">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="30387-271">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="30387-271">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="30387-272">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="30387-272">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="30387-273">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="30387-273">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="30387-274">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="30387-274">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="30387-275">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="30387-275">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="30387-276">Обновлены существующие командлеты для включения поддержки необязательного входного параметра RoutingConfiguration для настраиваемой маршрутизации в виртуальной глобальной сети.</span><span class="sxs-lookup"><span data-stu-id="30387-276">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="30387-277">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="30387-277">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="30387-278">Set-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="30387-278">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="30387-279">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="30387-279">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="30387-280">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="30387-280">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="30387-281">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="30387-281">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="30387-282">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="30387-282">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="30387-283">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="30387-283">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="30387-284">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="30387-284">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="30387-285">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="30387-285">Az.OperationalInsights</span></span>
* <span data-ttu-id="30387-286">Исправлена ошибка, из-за которой PSWorkspace не реализует IOperationalInsightsWorkspace [№ 12135].</span><span class="sxs-lookup"><span data-stu-id="30387-286">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="30387-287">Добавлено значение pergb2018 в действительный набор значений параметра Sku в командлете Set-AzOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="30387-287">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="30387-288">Добавлен псевдоним FunctionParameters для параметра FunctionParameter:</span><span class="sxs-lookup"><span data-stu-id="30387-288">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="30387-289">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="30387-289">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="30387-290">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="30387-290">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="30387-291">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="30387-291">Az.RecoveryServices</span></span>
* <span data-ttu-id="30387-292">Включена поддержка выборки элементов MAB в Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="30387-292">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="30387-293">Включена поддержка типа диска StandardSSD_LRS в Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="30387-293">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="30387-294">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30387-294">Az.Resources</span></span>
* <span data-ttu-id="30387-295">Добавлены параметры UsageLocation, GivenName, Surname, AccountEnabled, MailNickname, Mail для PSADUser [№ 10526], [№ 10497].</span><span class="sxs-lookup"><span data-stu-id="30387-295">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="30387-296">Исправлена ошибка, из-за которой параметр -Mail не работает в командлете Get-AzADUser [№ 11981].</span><span class="sxs-lookup"><span data-stu-id="30387-296">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="30387-297">Добавлен параметр -ExcludeChangeType в командлеты Get-AzDeploymentWhatIfResult и Get-AzResourceGroupDeploymentWhatIfResult.</span><span class="sxs-lookup"><span data-stu-id="30387-297">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="30387-298">Добавлен параметр -WhatIfExcludeChangeType в командлеты New-AzDeployment и New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="30387-298">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="30387-299">Обновлены командлеты Test-Az\*Deployment для отображения улучшенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="30387-299">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="30387-300">Исправлено справочное сообщение для параметра -Name в командлетах создания развертывания и командлетах What-If.</span><span class="sxs-lookup"><span data-stu-id="30387-300">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="30387-301">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30387-301">Az.Sql</span></span>
* <span data-ttu-id="30387-302">Включена поддержка субъекта-службы для командлета настройки администратора Azure Active Directory SQL Server.</span><span class="sxs-lookup"><span data-stu-id="30387-302">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="30387-303">Исправлена ошибка синхронизации в командлетах классификации данных.</span><span class="sxs-lookup"><span data-stu-id="30387-303">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="30387-304">Включена поддержка поиска пользователей по адресу электронной почты в командлете Set-AzSqlServerActiveDirectoryAdministrator [№ 12192].</span><span class="sxs-lookup"><span data-stu-id="30387-304">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="30387-305">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="30387-305">Az.Storage</span></span>
* <span data-ttu-id="30387-306">Включена поддержка создания учетной записи хранения с помощью RequireInfrastructureEncryption.</span><span class="sxs-lookup"><span data-stu-id="30387-306">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="30387-307">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30387-307">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="30387-308">Перемещена логика загрузки Azure.Core в Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="30387-308">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="30387-309">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="30387-309">Az.Websites</span></span>
* <span data-ttu-id="30387-310">В командлет Restore-AzDeletedWebApp добавлена защитная мера при удалении созданного веб-приложения, если восстановление завершилось сбоем.</span><span class="sxs-lookup"><span data-stu-id="30387-310">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="30387-311">Добавлены параметры SourceWebApp.Location для командлетов New-AzWebApp и New-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="30387-311">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="30387-312">Исправлена ошибка, препятствующая изменению параметров контейнера в командлетах Set-AzWebApp и Set-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="30387-312">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="30387-313">Исправлена ошибка получения SiteConfig, когда параметр -Name не указан для командлета Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="30387-313">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="30387-314">Включена поддержка создания приложений ASP для Linux.</span><span class="sxs-lookup"><span data-stu-id="30387-314">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="30387-315">Добавлены исключения для клонирования в группах ресурсов.</span><span class="sxs-lookup"><span data-stu-id="30387-315">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="30387-316">4.2.0 — июнь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="30387-316">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="30387-317">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30387-317">Az.Accounts</span></span>
* <span data-ttu-id="30387-318">Исправлена проблема, из-за которой модуль Az мог пропускать журналы в заданиях службы автоматизации или PowerShell [№ 11492].</span><span class="sxs-lookup"><span data-stu-id="30387-318">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="30387-319">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="30387-319">Az.AnalysisServices</span></span>
* <span data-ttu-id="30387-320">Обновлена версия сборки командлетов плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="30387-320">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="30387-321">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="30387-321">Az.ApiManagement</span></span>
* <span data-ttu-id="30387-322">Обновлена версия сборки командлетов управления службами.</span><span class="sxs-lookup"><span data-stu-id="30387-322">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="30387-323">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="30387-323">Az.Billing</span></span>
* <span data-ttu-id="30387-324">Обновлена версия сборки командлетов потребления.</span><span class="sxs-lookup"><span data-stu-id="30387-324">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="30387-325">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="30387-325">Az.CognitiveServices</span></span>
* <span data-ttu-id="30387-326">Реализована поддержка элементов управления PrivateEndpoint и PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="30387-326">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="30387-327">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="30387-327">Az.DataFactory</span></span>
* <span data-ttu-id="30387-328">Обновлена версия сборки командлетов фабрики данных версии 2.</span><span class="sxs-lookup"><span data-stu-id="30387-328">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="30387-329">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="30387-329">Az.DataShare</span></span>
* <span data-ttu-id="30387-330">Вышла общедоступная версия модуля Az.DataShare.</span><span class="sxs-lookup"><span data-stu-id="30387-330">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="30387-331">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="30387-331">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="30387-332">Вышла общедоступная версия модуля Az.DesktopVirtualization.</span><span class="sxs-lookup"><span data-stu-id="30387-332">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="30387-333">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="30387-333">Az.OperationalInsights</span></span>
* <span data-ttu-id="30387-334">Пакет SDK обновлен до версии 0.21.0.</span><span class="sxs-lookup"><span data-stu-id="30387-334">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="30387-335">Добавлены дополнительные параметры в следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="30387-335">Added optional parameters to</span></span> 
    - <span data-ttu-id="30387-336">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="30387-336">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="30387-337">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="30387-337">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="30387-338">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="30387-338">Az.PolicyInsights</span></span>
* <span data-ttu-id="30387-339">Исправлен пример 3 для командлета Start-AzPolicyComplianceScan.</span><span class="sxs-lookup"><span data-stu-id="30387-339">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="30387-340">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="30387-340">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="30387-341">Обновлена версия сборки командлетов PowerBI.</span><span class="sxs-lookup"><span data-stu-id="30387-341">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="30387-342">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="30387-342">Az.PrivateDns</span></span>
* <span data-ttu-id="30387-343">Исправлено форматирование строки с подробными выходными данными командлета Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="30387-343">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="30387-344">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="30387-344">Az.RecoveryServices</span></span>
* <span data-ttu-id="30387-345">Реализована поддержка Azure Site Recovery для создания плана восстановления и репликации между зонами из входного XML-файла.</span><span class="sxs-lookup"><span data-stu-id="30387-345">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="30387-346">Обновлена версия сборки командлетов SiteRecovery и Backup.</span><span class="sxs-lookup"><span data-stu-id="30387-346">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="30387-347">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30387-347">Az.Resources</span></span>
* <span data-ttu-id="30387-348">Добавлен параметр Tail в командлеты Get-AzDeploymentScriptLog и Save-AzDeploymentScriptLog.</span><span class="sxs-lookup"><span data-stu-id="30387-348">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="30387-349">Отформатировано свойство Output и включено в отображаемые выходные данные командлета Get-AzDeploymentScript.</span><span class="sxs-lookup"><span data-stu-id="30387-349">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="30387-350">Параметр -DeploymentScriptInputObject переименован в -DeploymentScriptObject.</span><span class="sxs-lookup"><span data-stu-id="30387-350">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="30387-351">Исправлена ошибка с отсутствующими именами файлов или целевых объектов в сообщениях командлетов.</span><span class="sxs-lookup"><span data-stu-id="30387-351">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="30387-352">Обновлена версия сборки командлетов диспетчера ресурсов и обработчика тегов.</span><span class="sxs-lookup"><span data-stu-id="30387-352">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="30387-353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30387-353">Az.Sql</span></span>
* <span data-ttu-id="30387-354">Добавлен параметр UsePrivateLinkConnection в командлеты New-AzSqlSyncGroup, Update-AzSqlSyncGroup, New-AzSqlSyncMember и Update-AzSqlSyncMember.</span><span class="sxs-lookup"><span data-stu-id="30387-354">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="30387-355">Добавлен параметр SyncMemberAzureDatabaseResourceId в командлеты New-AzSqlSyncMember и Update-AzSqlSyncMember.</span><span class="sxs-lookup"><span data-stu-id="30387-355">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="30387-356">Реализована поддержка поиска гостевых пользователей в командлете для настройки администратора Active Directory в SQL Server Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-356">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="30387-357">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="30387-357">Az.Storage</span></span>
* <span data-ttu-id="30387-358">Обновлена версия сборки командлетов плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="30387-358">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="30387-359">4.1.0 — май 2020 г.</span><span class="sxs-lookup"><span data-stu-id="30387-359">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="30387-360">Основные сведения о новых возможностях с момента последнего выпуска</span><span class="sxs-lookup"><span data-stu-id="30387-360">Highlights since the last release</span></span>
* <span data-ttu-id="30387-361">Поддерживаемые версии PowerShell: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="30387-361">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="30387-362">Вышла общедоступная версия модуля Az.Functions.</span><span class="sxs-lookup"><span data-stu-id="30387-362">General availability of Az.Functions</span></span> 
* <span data-ttu-id="30387-363">Состоялся основной выпуск Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources и Az.Storage.</span><span class="sxs-lookup"><span data-stu-id="30387-363">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="30387-364">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30387-364">Az.Accounts</span></span>
* <span data-ttu-id="30387-365">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметры AzureSynapseAnalyticsEndpointResourceId и AzureSynapseAnalyticsEndpointSuffix.</span><span class="sxs-lookup"><span data-stu-id="30387-365">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="30387-366">В Az.Accounts добавлены сборки, связанные с Azure.Core. Добавлена поддержка Windows PowerShell 5.1, PowerShell Core 6.2.4 и PowerShell 7+.</span><span class="sxs-lookup"><span data-stu-id="30387-366">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="30387-367">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="30387-367">Az.Aks</span></span>
* <span data-ttu-id="30387-368">Версия API обновлена до 2019-10-01.</span><span class="sxs-lookup"><span data-stu-id="30387-368">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="30387-369">Добавлена возможность создания контейнера Windows в службе Azure Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="30387-369">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="30387-370">Добавлены новые командлеты: New-AzAksNodePool, Update-AzAksNodePool, Remove-AzAksNodePool, Get-AzAksNodePool, Install-AzAksKubectl, Get-AzAksVersion.</span><span class="sxs-lookup"><span data-stu-id="30387-370">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="30387-371">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="30387-371">Az.ApiManagement</span></span>
* <span data-ttu-id="30387-372">В New-AzApiManagement и Set-AzApiManagement параметр -AssignIdentity переименован в -SystemAssignedIdentity.</span><span class="sxs-lookup"><span data-stu-id="30387-372">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="30387-373">В New-AzApiManagement и Set-AzApiManagement добавлен новый параметр -UserAssignedIdentity <строка[]>.</span><span class="sxs-lookup"><span data-stu-id="30387-373">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="30387-374">Командлет Get-AzApiManagementProperty переименован в Get-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="30387-374">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="30387-375">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="30387-375">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="30387-376">Командлет New-AzApiManagementProperty переименован в New-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="30387-376">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="30387-377">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="30387-377">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="30387-378">Командлет Set-AzApiManagementProperty переименован в Set-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="30387-378">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="30387-379">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="30387-379">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="30387-380">Командлет Remove-AzApiManagementProperty переименован в Remove-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="30387-380">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="30387-381">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="30387-381">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="30387-382">Добавлен новый командлет Get-AzApiManagementAuthorizationServerClientSecret, а Get-AzApiManagementAuthorizationServer теперь не возвращает секрет клиента.</span><span class="sxs-lookup"><span data-stu-id="30387-382">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="30387-383">Добавлен новый командлет Get-AzApiManagementNamedValueSecretValue, а Get-AzApiManagementNamedValue теперь не возвращает значение секрета.</span><span class="sxs-lookup"><span data-stu-id="30387-383">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="30387-384">Добавлен новый командлет Get-AzApiManagementOpenIdConnectProviderClientSecret, а Get-AzApiManagementOpenIdConnectProvider теперь не возвращает секрет клиента.</span><span class="sxs-lookup"><span data-stu-id="30387-384">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="30387-385">Добавлен новый командлет Get-AzApiManagementSubscriptionKey, а Get-AzApiManagementSubscription теперь не возвращает ключи подписки.</span><span class="sxs-lookup"><span data-stu-id="30387-385">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="30387-386">Добавлен новый командлет Get-AzApiManagementTenantAccessSecret, а Get-AzApiManagementTenantAccess теперь не возвращает ключи.</span><span class="sxs-lookup"><span data-stu-id="30387-386">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="30387-387">Добавлен новый командлет Get-AzApiManagementTenantGitAccessSecret, а Get-AzApiManagementTenantGitAccess теперь не возвращает ключи.</span><span class="sxs-lookup"><span data-stu-id="30387-387">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="30387-388">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="30387-388">Az.ApplicationInsights</span></span>
* <span data-ttu-id="30387-389">В New-AzApplicationInsights добавлены параметры RetentionInDays, PublicNetworkAccessForIngestion и PublicNetworkAccessForQuery.</span><span class="sxs-lookup"><span data-stu-id="30387-389">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="30387-390">Создан командлет Update-AzApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="30387-390">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="30387-391">Созданы командлеты для связанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="30387-391">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="30387-392">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="30387-392">Az.Batch</span></span>
* <span data-ttu-id="30387-393">В командлеты Az.Batch добавлена поддержка пакетов SDK Microsoft.Azure.Batch версии 13.0.0 и SDK Microsoft.Azure.Management.Batch версии 9.0.0.</span><span class="sxs-lookup"><span data-stu-id="30387-393">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="30387-394">Теперь в New-AzBatchCertificate можно выбрать тип добавляемого сертификата с помощью нового параметра -CertificateKind.</span><span class="sxs-lookup"><span data-stu-id="30387-394">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="30387-395">В PSApplication удалено свойство ApplicationPackages.</span><span class="sxs-lookup"><span data-stu-id="30387-395">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="30387-396">Отдельные пакеты в приложении теперь можно извлечь с помощью Get-AzBatchApplicationPackage.</span><span class="sxs-lookup"><span data-stu-id="30387-396">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="30387-397">Пример: Get-AzBatchApplication -AccountName моя_учетная_запись -ResourceGroupName моя_группа_ресурсов -ApplicationId мое_приложение.</span><span class="sxs-lookup"><span data-stu-id="30387-397">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="30387-398">При создании пула с помощью New-AzBatchPool свойство VirtualMachineImageId элемента PSImageReference теперь может ссылаться только на образ из Общей коллекции образов.</span><span class="sxs-lookup"><span data-stu-id="30387-398">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="30387-399">При создании пула с помощью New-AzBatchPool пул можно подготовить без общедоступного IP-адреса, используя новое свойство PublicIPAddressConfiguration элемента PSNetworkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="30387-399">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="30387-400">Свойство PublicIPs элемента PSNetworkConfiguration было передано элементу PSPublicIPAddressConfiguration.</span><span class="sxs-lookup"><span data-stu-id="30387-400">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="30387-401">Это свойство можно указать, только если параметру IPAddressProvisioningType присвоено значение UserManaged.</span><span class="sxs-lookup"><span data-stu-id="30387-401">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30387-402">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30387-402">Az.Compute</span></span>
* <span data-ttu-id="30387-403">В командлет Update-AzVM добавлен параметр HostId.</span><span class="sxs-lookup"><span data-stu-id="30387-403">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="30387-404">Обновлена справочная документация по командлетам New-AzVMConfig, New-AzVmssConfig, Update-AzVmss, Set-AzVMOperatingSystem и Set-AzVmssOsProfile.</span><span class="sxs-lookup"><span data-stu-id="30387-404">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="30387-405">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="30387-405">Breaking changes</span></span>
    - <span data-ttu-id="30387-406">Параметр FilterExpression удален из командлета Get-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="30387-406">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="30387-407">Параметр AssignIdentity удален из командлетов New-AzVmssConfig, New-AzVMConfig и Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="30387-407">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="30387-408">Параметр AutomaticRepairMaxInstanceRepairsPercent удален из командлетов New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="30387-408">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="30387-409">Свойства AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus и VirtualMachineScaleSetsColocationStatus удалены из ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="30387-409">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="30387-410">Свойство MaxInstanceRepairsPercent удалено из AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="30387-410">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="30387-411">Типы AvailabilitySets, VirtualMachines и VirtualMachineScaleSets изменены с IList<SubResource> на IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="30387-411">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="30387-412">Уточнено описание командлета Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="30387-412">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="30387-413">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="30387-413">Az.DataFactory</span></span>
* <span data-ttu-id="30387-414">Добавлена поддержка операций CRUD для свойств среды выполнения потока данных в управляемой среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="30387-414">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="30387-415">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="30387-415">Az.FrontDoor</span></span>
* <span data-ttu-id="30387-416">Добавлены новые командлеты для создания, обновления, извлечения и удаления объекта обработчика правил Front Door.</span><span class="sxs-lookup"><span data-stu-id="30387-416">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="30387-417">Добавлены вспомогательные командлеты для создания объекта обработчика правил Front Door.</span><span class="sxs-lookup"><span data-stu-id="30387-417">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="30387-418">Добавлена ссылка обработчика правил на объект правила маршрутизации Front Door.</span><span class="sxs-lookup"><span data-stu-id="30387-418">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="30387-419">Добавлены параметры Приватного канала на серверный объект Front Door.</span><span class="sxs-lookup"><span data-stu-id="30387-419">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="30387-420">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="30387-420">Az.Functions</span></span>
* <span data-ttu-id="30387-421">Вышла общедоступная версия модуля Az.Functions.</span><span class="sxs-lookup"><span data-stu-id="30387-421">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="30387-422">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="30387-422">Az.HDInsight</span></span>
* <span data-ttu-id="30387-423">Добавлена поддержка шифрования управляемых клиентом ключей.</span><span class="sxs-lookup"><span data-stu-id="30387-423">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="30387-424">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="30387-424">Az.HealthcareApis</span></span>
* <span data-ttu-id="30387-425">Политики доступа для текущего субъекта теперь не используются по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="30387-425">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="30387-426">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="30387-426">Az.IotHub</span></span>
* <span data-ttu-id="30387-427">Добавлен командлет для вызова запроса в центре Интернета вещей для получения данных с помощью SQL-подобного языка.</span><span class="sxs-lookup"><span data-stu-id="30387-427">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="30387-428">Устранена проблема, когда с помощью Add-AzIotHubDevice не удавалось создать устройство с поддержкой IoT Edge без дочерних устройств (№ 11597).</span><span class="sxs-lookup"><span data-stu-id="30387-428">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="30387-429">Добавлен командлет для создания маркера SAS для Центра Интернета вещей, устройства или модуля.</span><span class="sxs-lookup"><span data-stu-id="30387-429">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="30387-430">Добавлен командлет для вызова запроса метрик конфигурации.</span><span class="sxs-lookup"><span data-stu-id="30387-430">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="30387-431">Появилась возможность управлять автоматическим развертыванием IoT Edge в большом масштабе.</span><span class="sxs-lookup"><span data-stu-id="30387-431">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="30387-432">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="30387-432">New cmdlets are:</span></span>
    - <span data-ttu-id="30387-433">Add-AzIotHubDeployment;</span><span class="sxs-lookup"><span data-stu-id="30387-433">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="30387-434">Get-AzIotHubDeployment;</span><span class="sxs-lookup"><span data-stu-id="30387-434">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="30387-435">Remove-AzIotHubDeployment;</span><span class="sxs-lookup"><span data-stu-id="30387-435">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="30387-436">Set-AzIotHubDeployment.</span><span class="sxs-lookup"><span data-stu-id="30387-436">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="30387-437">Добавлен командлет для вызова запроса метрик развертывания IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="30387-437">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="30387-438">Добавлен командлет для применения содержимого конфигурации к указанному пограничному устройству.</span><span class="sxs-lookup"><span data-stu-id="30387-438">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="30387-439">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="30387-439">Az.KeyVault</span></span>
* <span data-ttu-id="30387-440">Удалены два псевдонима: New-AzKeyVaultCertificateAdministratorDetails и New-AzKeyVaultCertificateOrganizationDetails.</span><span class="sxs-lookup"><span data-stu-id="30387-440">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="30387-441">При создании хранилища ключей обратимое удаление включено по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="30387-441">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="30387-442">Можно задать правила сети, чтобы при создании хранилища ключей управлять доступом из определенных сетевых расположений.</span><span class="sxs-lookup"><span data-stu-id="30387-442">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="30387-443">Добавлена возможность создания собственных ключей (BYOK).</span><span class="sxs-lookup"><span data-stu-id="30387-443">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="30387-444">С помощью Add-AzKeyVaultKey теперь можно создавать ключ обмена ключами.</span><span class="sxs-lookup"><span data-stu-id="30387-444">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="30387-445">С помощью Get-AzKeyVaultKey можно скачать открытый ключ в формате PEM.</span><span class="sxs-lookup"><span data-stu-id="30387-445">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="30387-446">Обновлен раздел KeyOps справочной документации по Add-AzKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="30387-446">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="30387-447">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="30387-447">Az.Monitor</span></span>
* <span data-ttu-id="30387-448">Исправлена ошибка Set-AzDiagnosticSettings, когда политика хранения не применялась ко всем категориям (№ 11589).</span><span class="sxs-lookup"><span data-stu-id="30387-448">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="30387-449">Добавлена поддержка критериев доступности веб-теста для оповещения метрики версии 2.</span><span class="sxs-lookup"><span data-stu-id="30387-449">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="30387-450">В New-AzMetricAlertRuleV2Criteria добавлена возможность создавать критерии доступности веб-теста.</span><span class="sxs-lookup"><span data-stu-id="30387-450">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="30387-451">Add-AzMetricAlertRuleV2 теперь поддерживает новые критерии доступности веб-теста.</span><span class="sxs-lookup"><span data-stu-id="30387-451">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="30387-452">В PSLogProfile исправлено избыточное определение RetentionPolicy (№ 7608).</span><span class="sxs-lookup"><span data-stu-id="30387-452">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="30387-453">В PSEventData удалены избыточные определения свойств (№ 11353).</span><span class="sxs-lookup"><span data-stu-id="30387-453">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="30387-454">Командлет Get-AzLog переименован в Get-AzActivityLog.</span><span class="sxs-lookup"><span data-stu-id="30387-454">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30387-455">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30387-455">Az.Network</span></span>
* <span data-ttu-id="30387-456">Добавлен атрибут критического изменения, сообщающий о том, что поведение зоны по умолчанию будет изменено.</span><span class="sxs-lookup"><span data-stu-id="30387-456">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="30387-457">New-AzPublicIpAddress;</span><span class="sxs-lookup"><span data-stu-id="30387-457">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="30387-458">New-AzPublicIpPrefix;</span><span class="sxs-lookup"><span data-stu-id="30387-458">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="30387-459">New-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="30387-459">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="30387-460">Добавлена поддержка нового ресурса верхнего уровня SecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="30387-460">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="30387-461">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="30387-461">New cmdlets added:</span></span>
        - <span data-ttu-id="30387-462">New-AzSecurityPartnerProvider;</span><span class="sxs-lookup"><span data-stu-id="30387-462">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="30387-463">Remove-AzSecurityPartnerProvider;</span><span class="sxs-lookup"><span data-stu-id="30387-463">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="30387-464">Get-AzSecurityPartnerProvider;</span><span class="sxs-lookup"><span data-stu-id="30387-464">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="30387-465">Set-AzSecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="30387-465">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="30387-466">В PSPrivateLinkResource добавлен параметр RequiredZoneNames, а в PSPrivateEndpointConnection — GroupId.</span><span class="sxs-lookup"><span data-stu-id="30387-466">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="30387-467">Исправлен неправильный тип параметра SuccessThresholdRoundTripTimeMs для New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.</span><span class="sxs-lookup"><span data-stu-id="30387-467">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="30387-468">В командлетах VirtualWan аргументу AllowVnetToVnetTraffic теперь по умолчанию присвоено значение True.</span><span class="sxs-lookup"><span data-stu-id="30387-468">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="30387-469">New-AzVirtualWan;</span><span class="sxs-lookup"><span data-stu-id="30387-469">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="30387-470">Update-AzVirtualWan.</span><span class="sxs-lookup"><span data-stu-id="30387-470">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="30387-471">Добавлены новые командлеты для поддержки группы зон DNS для частной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="30387-471">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="30387-472">New-AzPrivateDnsZoneConfig;</span><span class="sxs-lookup"><span data-stu-id="30387-472">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="30387-473">Get-AzPrivateDnsZoneGroup;</span><span class="sxs-lookup"><span data-stu-id="30387-473">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="30387-474">New-AzPrivateDnsZoneGroup;</span><span class="sxs-lookup"><span data-stu-id="30387-474">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="30387-475">Set-AzPrivateDnsZoneGroup;</span><span class="sxs-lookup"><span data-stu-id="30387-475">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="30387-476">Remove-AzPrivateDnsZoneGroup.</span><span class="sxs-lookup"><span data-stu-id="30387-476">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="30387-477">В AzureFirewall добавлены параметры DNSEnableProxy, DNSRequireProxyForNetworkRules и DNSServers.</span><span class="sxs-lookup"><span data-stu-id="30387-477">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="30387-478">В AzureFirewall добавлены параметры EnableDnsProxy, DnsProxyNotRequiredForNetworkRule и DnsServer.</span><span class="sxs-lookup"><span data-stu-id="30387-478">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="30387-479">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="30387-479">Updated cmdlet:</span></span>
        - <span data-ttu-id="30387-480">New-AzFirewall.</span><span class="sxs-lookup"><span data-stu-id="30387-480">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="30387-481">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="30387-481">Az.OperationalInsights</span></span>
* <span data-ttu-id="30387-482">Обновлен устаревший код для использования новых пакетов SDK.</span><span class="sxs-lookup"><span data-stu-id="30387-482">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="30387-483">Из-за устаревших API-интерфейсов удалены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="30387-483">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="30387-484">Get-AzOperationalInsightsSavedSearchResult (псевдоним Get-AzOperationalInsightsSavedSearchResults);</span><span class="sxs-lookup"><span data-stu-id="30387-484">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="30387-485">Get-AzOperationalInsightsSearchResult (псевдоним Get-AzOperationalInsightsSearchResults);</span><span class="sxs-lookup"><span data-stu-id="30387-485">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="30387-486">Get-AzOperationalInsightsLinkTarget (псевдоним Get-AzOperationalInsightsLinkTargets).</span><span class="sxs-lookup"><span data-stu-id="30387-486">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="30387-487">В Set-AzOperationalInsightsWorkspace и New-AzOperationalInsightsWorkspace добавлены новые параметры.</span><span class="sxs-lookup"><span data-stu-id="30387-487">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="30387-488">Созданы командлеты для связанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="30387-488">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="30387-489">Созданы командлеты для кластеров и связанной службы.</span><span class="sxs-lookup"><span data-stu-id="30387-489">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="30387-490">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="30387-490">Az.RecoveryServices</span></span>
* <span data-ttu-id="30387-491">В Azure Site Recovery добавлена поддержка защиты поставщика Azure для групп размещения виртуальных машин Azure близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="30387-491">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="30387-492">В Azure Site Recovery добавлена поддержка репликации из зоны в зону.</span><span class="sxs-lookup"><span data-stu-id="30387-492">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="30387-493">В Azure Backup добавлена поддержка долгосрочного хранения для точек восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-493">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="30387-494">В выходные данные командлета Get-AzRecoveryServicesBackupItem добавлены свойства исключения диска, добавленного в Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="30387-494">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="30387-495">Добавлена частная конечная точка для файла учетных данных хранилища для службы Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="30387-495">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="30387-496">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30387-496">Az.Resources</span></span>
* <span data-ttu-id="30387-497">Добавлено предупреждение о задержке представления при создании определения роли.</span><span class="sxs-lookup"><span data-stu-id="30387-497">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="30387-498">Командлеты политики теперь выводят строго типизированные объекты.</span><span class="sxs-lookup"><span data-stu-id="30387-498">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="30387-499">Из командлета Get-AzResourceLock удален параметр -TenantLevel (№ 11335).</span><span class="sxs-lookup"><span data-stu-id="30387-499">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="30387-500">Исправлена ошибка с Remove-AzResourceGroup -Id ResourceId (№ 9882).</span><span class="sxs-lookup"><span data-stu-id="30387-500">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="30387-501">Добавлен новый командлет для получения результатов анализа гипотетических вариантов из шаблона ARM в области группы ресурсов: Get-AzDeploymentResourceGroupWhatIfResult.</span><span class="sxs-lookup"><span data-stu-id="30387-501">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="30387-502">Добавлен новый командлет для получения результатов анализа гипотетических вариантов из шаблона ARM в области подписки: Get-AzDeploymentWhatIfResult.</span><span class="sxs-lookup"><span data-stu-id="30387-502">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="30387-503">Alias: Get-AzSubscriptionDeploymentWhatIf.</span><span class="sxs-lookup"><span data-stu-id="30387-503">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="30387-504">Переопределены параметры -WhatIf и -Confirm для New-AzDeployment и New-AzResourceGroupDeployment для использования результатов анализа гипотетических вариантов из шаблона ARM.</span><span class="sxs-lookup"><span data-stu-id="30387-504">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="30387-505">В командлеты развертывания добавлено сообщение об устаревании для параметра ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="30387-505">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="30387-506">Добавлена возможность отображения улучшенных сообщений об ошибках при развертывании.</span><span class="sxs-lookup"><span data-stu-id="30387-506">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="30387-507">Добавлена возможность регистрации correlationId для сбоев развертывания.</span><span class="sxs-lookup"><span data-stu-id="30387-507">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="30387-508">В выходные данные скрипта развертывания добавлено свойство error.</span><span class="sxs-lookup"><span data-stu-id="30387-508">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="30387-509">Пакет NuGet Microsoft.Azure.Management.ResourceManager обновлен до версии 3.7.1-preview.</span><span class="sxs-lookup"><span data-stu-id="30387-509">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="30387-510">Удаленные определенные тестовые случаи как свойство error в DeploymentValidateResult были изменены на доступные только для чтения из пакета NuGet версии 3.7.1-preview.</span><span class="sxs-lookup"><span data-stu-id="30387-510">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="30387-511">Добавлен GenericResourceExpanded из пакета SDK ResourceManager версии 3.7.1-preview.</span><span class="sxs-lookup"><span data-stu-id="30387-511">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="30387-512">Добавлена поддержка тегов для всех командлетов Get для развертывания, а также для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="30387-512">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="30387-513">New-AzDeployment;</span><span class="sxs-lookup"><span data-stu-id="30387-513">'New-AzDeployment'</span></span>
    - <span data-ttu-id="30387-514">New-AzManagementGroupDeployment;</span><span class="sxs-lookup"><span data-stu-id="30387-514">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="30387-515">New-AzResourceGroupDeployment;</span><span class="sxs-lookup"><span data-stu-id="30387-515">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="30387-516">New-AzTenantDeployment.</span><span class="sxs-lookup"><span data-stu-id="30387-516">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="30387-517">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="30387-517">Az.ServiceFabric</span></span>
* <span data-ttu-id="30387-518">Исправлена ошибка при добавлении сертификата с помощью параметра -SecretIdentifier, когда возвращался неправильный отпечаток сертификата.</span><span class="sxs-lookup"><span data-stu-id="30387-518">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="30387-519">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30387-519">Az.Sql</span></span>
* <span data-ttu-id="30387-520">Оптимизирована работа следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="30387-520">Enhance performance of:</span></span>
    - <span data-ttu-id="30387-521">Set-AzSqlDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="30387-521">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="30387-522">Set-AzSqlInstanceDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="30387-522">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="30387-523">Remove-AzSqlDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="30387-523">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="30387-524">Remove-AzSqlInstanceDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="30387-524">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="30387-525">Enable-AzSqlDatabaseSensitivityRecommendation;</span><span class="sxs-lookup"><span data-stu-id="30387-525">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="30387-526">Enable-AzSqlInstanceDatabaseSensitivityRecommendation;</span><span class="sxs-lookup"><span data-stu-id="30387-526">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="30387-527">Disable-AzSqlDatabaseSensitivityRecommendation;</span><span class="sxs-lookup"><span data-stu-id="30387-527">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="30387-528">Disable-AzSqlInstanceDatabaseSensitivityRecommendation.</span><span class="sxs-lookup"><span data-stu-id="30387-528">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="30387-529">Удалена проверка на стороне клиента параметра RetentionDays из командлета Set-AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="30387-529">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="30387-530">Добавлен аудит учетной записи хранения в виртуальной сети. Исправлена ошибка при создании роли участника данных BLOB-объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="30387-530">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="30387-531">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="30387-531">Az.Storage</span></span>
* <span data-ttu-id="30387-532">В командлет Get-AzStorageAccount добавлен параметр -AsJob.</span><span class="sxs-lookup"><span data-stu-id="30387-532">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="30387-533">Параметр KeyVersion теперь является необязательным при изменении учетной записи хранения с помощью KeyvaultEncryption, что обеспечивает поддержку автоматической смены ключа.</span><span class="sxs-lookup"><span data-stu-id="30387-533">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="30387-534">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30387-534">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="30387-535">Исправлена ошибка при удалении каталога файлов Azure с конвейером.</span><span class="sxs-lookup"><span data-stu-id="30387-535">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="30387-536">Remove-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="30387-536">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="30387-537">Исправлена ошибка 9880. Значение DefaultAction для NetWorkRule приведено в соответствие со Swagger.</span><span class="sxs-lookup"><span data-stu-id="30387-537">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="30387-538">Update-AzStorageAccountNetworkRuleSet;</span><span class="sxs-lookup"><span data-stu-id="30387-538">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="30387-539">Get-AzStorageAccountNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="30387-539">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="30387-540">Исправлена ошибка 11624. При добавлении NetworkRules дублирующиеся правила пропускаются, чтобы не происходил сбой сервера.</span><span class="sxs-lookup"><span data-stu-id="30387-540">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="30387-541">Add-AzStorageAccountNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="30387-541">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="30387-542">Версия пакета SDK Microsoft.Azure.Cosmos.Table обновлена до 1.0.7.</span><span class="sxs-lookup"><span data-stu-id="30387-542">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="30387-543">Добавлено предупреждающее сообщение, напоминающее пользователю о необходимости повторного вывода списка с помощью ContinuationToken, когда в списке элементов Data Lake 2-го поколения возвращается только часть элементов.</span><span class="sxs-lookup"><span data-stu-id="30387-543">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="30387-544">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="30387-544">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="30387-545">Добавлена возможность создания или изменения учетной записи хранения с использованием проверки подлинности Active Directory для Файлов Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-545">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="30387-546">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30387-546">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="30387-547">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30387-547">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="30387-548">Добавлена возможность создания и просмотра ключей Kerberos учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="30387-548">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="30387-549">New-AzStorageAccountKey;</span><span class="sxs-lookup"><span data-stu-id="30387-549">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="30387-550">Get-AzStorageAccountKey.</span><span class="sxs-lookup"><span data-stu-id="30387-550">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="30387-551">Добавлена возможность отработки отказа для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="30387-551">Supported failover Storage account</span></span>
    - <span data-ttu-id="30387-552">Invoke-AzStorageAccountFailover.</span><span class="sxs-lookup"><span data-stu-id="30387-552">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="30387-553">Обновлена справка по Get-AzStorageBlobCopyState.</span><span class="sxs-lookup"><span data-stu-id="30387-553">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="30387-554">Обновлена справка по Get-AzStorageFileCopyState и Start-AzStorageBlobCopy.</span><span class="sxs-lookup"><span data-stu-id="30387-554">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="30387-555">Появилась интегрированная клиентская библиотека хранилища версии 12 для командлетов очередей и файлов.</span><span class="sxs-lookup"><span data-stu-id="30387-555">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="30387-556">Тип выходных данных изменен с CloudFile на AzureStorageFile. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="30387-556">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="30387-557">Get-AzStorageFile;</span><span class="sxs-lookup"><span data-stu-id="30387-557">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="30387-558">Remove-AzStorageFile;</span><span class="sxs-lookup"><span data-stu-id="30387-558">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="30387-559">Get-AzStorageFileContent;</span><span class="sxs-lookup"><span data-stu-id="30387-559">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="30387-560">Set-AzStorageFileContent;</span><span class="sxs-lookup"><span data-stu-id="30387-560">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="30387-561">Start-AzStorageFileCopy.</span><span class="sxs-lookup"><span data-stu-id="30387-561">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="30387-562">Тип выходных данных изменен с CloudFileDirectory на AzureStorageFileDirectory. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="30387-562">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="30387-563">New-AzStorageDirectory;</span><span class="sxs-lookup"><span data-stu-id="30387-563">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="30387-564">Remove-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="30387-564">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="30387-565">Тип выходных данных изменен с CloudFileShare на AzureStorageFileShare. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="30387-565">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="30387-566">Get-AzStorageShare;</span><span class="sxs-lookup"><span data-stu-id="30387-566">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="30387-567">New-AzStorageShare;</span><span class="sxs-lookup"><span data-stu-id="30387-567">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="30387-568">Remove-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="30387-568">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="30387-569">Тип выходных данных изменен с FileShareProperties на AzureStorageFileShare. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="30387-569">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="30387-570">Set-AzStorageShareQuota.</span><span class="sxs-lookup"><span data-stu-id="30387-570">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="30387-571">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="30387-571">Az.TrafficManager</span></span>
* <span data-ttu-id="30387-572">Исправлено неправильное имя профиля в подробных выходных данных DisableAzureTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="30387-572">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="30387-573">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="30387-573">Az.Websites</span></span>
* <span data-ttu-id="30387-574">Исправлена опечатка в справке по Update-AzWebAppAccessRestrictionConfig.</span><span class="sxs-lookup"><span data-stu-id="30387-574">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="30387-575">3.8.0 — апрель 2020 г.</span><span class="sxs-lookup"><span data-stu-id="30387-575">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="30387-576">Основные сведения о новых возможностях с момента последнего выпуска</span><span class="sxs-lookup"><span data-stu-id="30387-576">Highlights since the last release</span></span>
* <span data-ttu-id="30387-577">Версии PowerShell, которые поддерживает Az.Storage: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="30387-577">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="30387-578">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30387-578">Az.Accounts</span></span>
* <span data-ttu-id="30387-579">Обновлен URL-адрес опроса Azure PowerShell в Resolve-AzError [11507].</span><span class="sxs-lookup"><span data-stu-id="30387-579">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="30387-580">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="30387-580">Az.ApiManagement</span></span>
* <span data-ttu-id="30387-581">Добавлено уведомление о критическом изменении для изменения выходных данных командлетов, выполняющих действия с файлами в Azure, в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="30387-581">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="30387-582">Обновлена документация для Set-AzApiManagementGroup с указанием параметра GroupId.</span><span class="sxs-lookup"><span data-stu-id="30387-582">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="30387-583">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="30387-583">Az.Cdn</span></span>
* <span data-ttu-id="30387-584">Исправлено отображение ценовой категории (SKU), связанной с ChinaCDN.</span><span class="sxs-lookup"><span data-stu-id="30387-584">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="30387-585">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="30387-585">Az.CognitiveServices</span></span>
* <span data-ttu-id="30387-586">Включена поддержка Identity, Encryption, UserOwnedStorage.</span><span class="sxs-lookup"><span data-stu-id="30387-586">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30387-587">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30387-587">Az.Compute</span></span>
* <span data-ttu-id="30387-588">Добавлен командлет Set-AzVmssOrchestrationServiceState.</span><span class="sxs-lookup"><span data-stu-id="30387-588">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="30387-589">Get-AzVmss с параметром -InstanceView отображает состояния OrchestrationService.</span><span class="sxs-lookup"><span data-stu-id="30387-589">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="30387-590">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="30387-590">Az.IotHub</span></span>
* <span data-ttu-id="30387-591">Реализовано управление конфигурацией двойника устройства Интернета вещей. Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="30387-591">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="30387-592">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="30387-592">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="30387-593">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="30387-593">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="30387-594">Добавлен командлет для вызова прямого метода на устройстве в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="30387-594">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="30387-595">Реализовано управление конфигурацией двойника модуля устройства Интернета вещей. Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="30387-595">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="30387-596">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="30387-596">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="30387-597">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="30387-597">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="30387-598">Реализовано управление конфигурацией автоматического управления устройствами в центре Интернета вещей в большом масштабе.</span><span class="sxs-lookup"><span data-stu-id="30387-598">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="30387-599">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="30387-599">New cmdlets are:</span></span>
    - <span data-ttu-id="30387-600">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="30387-600">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="30387-601">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="30387-601">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="30387-602">Remove-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="30387-602">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="30387-603">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="30387-603">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="30387-604">Добавлен командлет для вызова метода периферийного модуля в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="30387-604">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="30387-605">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="30387-605">Az.KeyVault</span></span>
* <span data-ttu-id="30387-606">Добавлен новый командлет Update-AzKeyVault, который может включать защиту от обратимого удаления и очистки в хранилище.</span><span class="sxs-lookup"><span data-stu-id="30387-606">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="30387-607">Включена поддержка Microsoft.PowerShell.SecretManagement [11178].</span><span class="sxs-lookup"><span data-stu-id="30387-607">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="30387-608">Исправлена ошибка в примерах Remove-AzKeyVaultManagedStorageSasDefinition [11479].</span><span class="sxs-lookup"><span data-stu-id="30387-608">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="30387-609">Включена поддержка частной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="30387-609">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="30387-610">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="30387-610">Az.Maintenance</span></span>
* <span data-ttu-id="30387-611">Опубликована версия выпуска командлетов обслуживания для общедоступной версии.</span><span class="sxs-lookup"><span data-stu-id="30387-611">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="30387-612">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="30387-612">Az.Monitor</span></span>
* <span data-ttu-id="30387-613">Добавлены командлеты для области приватных каналов:</span><span class="sxs-lookup"><span data-stu-id="30387-613">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="30387-614">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="30387-614">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="30387-615">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="30387-615">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="30387-616">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="30387-616">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="30387-617">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="30387-617">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="30387-618">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="30387-618">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="30387-619">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="30387-619">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="30387-620">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="30387-620">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30387-621">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30387-621">Az.Network</span></span>
* <span data-ttu-id="30387-622">Обновлены командлеты для включения подключения на частном IP-адресе для шлюза виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="30387-622">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="30387-623">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="30387-623">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="30387-624">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="30387-624">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="30387-625">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="30387-625">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="30387-626">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="30387-626">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="30387-627">Обновлены командлеты для включения шлюзов LocalNetworkGateways и сайтов VpnSites на основе FQDN:</span><span class="sxs-lookup"><span data-stu-id="30387-627">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="30387-628">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="30387-628">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="30387-629">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="30387-629">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="30387-630">Включена поддержка семейства адресов IPv6 в ExpressRouteCircuitConnectionConfig (Global Reach).</span><span class="sxs-lookup"><span data-stu-id="30387-630">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="30387-631">Добавлен командлет Set-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="30387-631">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="30387-632">Позволяет выполнять настройку всех существующих свойств, включая IPv6CircuitConnectionProperties.</span><span class="sxs-lookup"><span data-stu-id="30387-632">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="30387-633">Обновлен командлет Add-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="30387-633">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="30387-634">Добавлен еще один необязательный параметр AddressPrefixType для указания семейства адресов префикса адреса.</span><span class="sxs-lookup"><span data-stu-id="30387-634">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="30387-635">Обновлены командлеты для включения параметра времени ожидания для обнаружения неиспользуемых одноранговых узлов (DPD) в подключениях шлюзов виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="30387-635">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="30387-636">New-AzVirtualNetworkGatewayConnection;</span><span class="sxs-lookup"><span data-stu-id="30387-636">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="30387-637">Set-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="30387-637">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="30387-638">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="30387-638">Az.PolicyInsights</span></span>
* <span data-ttu-id="30387-639">Добавлен командлет Start-AzPolicyComplianceScan для запуска проверок соответствия политикам.</span><span class="sxs-lookup"><span data-stu-id="30387-639">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="30387-640">Добавлены версии определения политики, определения набора и назначения в выходные данные командлета Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="30387-640">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="30387-641">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="30387-641">Az.ServiceFabric</span></span>
* <span data-ttu-id="30387-642">Улучшено форматирование и наглядность кода в примерах New-AzServiceFabricCluster.</span><span class="sxs-lookup"><span data-stu-id="30387-642">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="30387-643">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30387-643">Az.Sql</span></span>
* <span data-ttu-id="30387-644">Добавлены командлеты Get-AzSqlInstanceOperation и Stop-AzSqlInstanceOperation.</span><span class="sxs-lookup"><span data-stu-id="30387-644">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="30387-645">Включен аудит учетной записи хранения в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="30387-645">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="30387-646">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="30387-646">Az.Storage</span></span>
* <span data-ttu-id="30387-647">Добавлено уведомление о критическом изменении для изменения выходных данных командлетов, выполняющих действия с файлами в Azure, в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="30387-647">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="30387-648">Включена поддержка новых имен SKU StandardGZRS, StandardRAGZRS при создании или обновлении учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="30387-648">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="30387-649">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30387-649">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="30387-650">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30387-650">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="30387-651">Добавлена поддержка DataLake 2-го поколения.</span><span class="sxs-lookup"><span data-stu-id="30387-651">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="30387-652">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="30387-652">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="30387-653">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="30387-653">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="30387-654">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="30387-654">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="30387-655">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="30387-655">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="30387-656">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="30387-656">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="30387-657">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="30387-657">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="30387-658">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="30387-658">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="30387-659">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="30387-659">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="30387-660">0.10.0-preview — апрель 2020 г.</span><span class="sxs-lookup"><span data-stu-id="30387-660">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="30387-661">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="30387-661">General</span></span>
* <span data-ttu-id="30387-662">Модуль Az стали доступными в предварительной версии в Azure Stack Hub.</span><span class="sxs-lookup"><span data-stu-id="30387-662">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="30387-663">Это обеспечивает кросс-платформенную совместимость с Linux и macOs.</span><span class="sxs-lookup"><span data-stu-id="30387-663">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="30387-664">Azure Stack Hub теперь поддерживает PowerShell Core с модулями Az (см. [дополнительные сведения](https://aka.ms/az4AzureStack))</span><span class="sxs-lookup"><span data-stu-id="30387-664">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="30387-665">Модули Az поддерживают профиль 2019-03-01-hybrid:</span><span class="sxs-lookup"><span data-stu-id="30387-665">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="30387-666">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="30387-666">Az.Billing</span></span>
  - <span data-ttu-id="30387-667">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30387-667">Az.Compute</span></span>
  - <span data-ttu-id="30387-668">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="30387-668">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="30387-669">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="30387-669">Az.EventHub</span></span>
  - <span data-ttu-id="30387-670">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="30387-670">Az.IotHub</span></span>
  - <span data-ttu-id="30387-671">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="30387-671">Az.KeyVault</span></span>
  - <span data-ttu-id="30387-672">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="30387-672">Az.Monitor</span></span>
  - <span data-ttu-id="30387-673">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30387-673">Az.Network</span></span>
  - <span data-ttu-id="30387-674">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30387-674">Az.Resources</span></span>
  - <span data-ttu-id="30387-675">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="30387-675">Az.Storage</span></span>
  - <span data-ttu-id="30387-676">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="30387-676">Az.Websites</span></span>
* <span data-ttu-id="30387-677">В PowerShell появились три новых модуля Az, которые работают с Azure Stack Hub: Az.Databox, Az.IotHub и Az.EventHub.</span><span class="sxs-lookup"><span data-stu-id="30387-677">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="30387-678">Команды остаются прежними же за исключением незначительных изменений, таких как изменение AzureRM на Az.</span><span class="sxs-lookup"><span data-stu-id="30387-678">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="30387-679">См. обновленную ссылку на документацию по [PowerShell для Azure Stack Hub](https://aka.ms/InstallASHPowerShell)</span><span class="sxs-lookup"><span data-stu-id="30387-679">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="30387-680">3.7.0 — март 2020 г.</span><span class="sxs-lookup"><span data-stu-id="30387-680">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="30387-681">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30387-681">Az.Accounts</span></span>
* <span data-ttu-id="30387-682">Исправлено исключение NullReferenceException командлетов Get-AzTenant/Get-AzDefault/Set-AzDefault, если вход не выполнен [10292]</span><span class="sxs-lookup"><span data-stu-id="30387-682">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30387-683">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30387-683">Az.Compute</span></span>
* <span data-ttu-id="30387-684">Добавлены следующие параметры к командлету New-AzDiskConfig:</span><span class="sxs-lookup"><span data-stu-id="30387-684">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="30387-685">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="30387-685">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="30387-686">Разрешено свойство Encryption для параметра Target командлета New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="30387-686">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="30387-687">Исправлена проблема с tempDisk для командлетов Set-AzVmss -Reimage и Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="30387-687">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="30387-688">[11354]</span><span class="sxs-lookup"><span data-stu-id="30387-688">[#11354]</span></span>
* <span data-ttu-id="30387-689">Добавлена поддержка нового расширения SAP для указанных ниже командлетов</span><span class="sxs-lookup"><span data-stu-id="30387-689">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="30387-690">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="30387-690">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="30387-691">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="30387-691">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="30387-692">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="30387-692">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="30387-693">Update-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="30387-693">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="30387-694">Исправлены ошибки в примерах справки</span><span class="sxs-lookup"><span data-stu-id="30387-694">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="30387-695">Показано точное строковое значение в табличном формате для свойства PowerState виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="30387-695">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="30387-696">New-AzVmssConfig: исправлена сериализация свойства AutomaticRepairs, если параметр SinglePlacementGroup отключен.</span><span class="sxs-lookup"><span data-stu-id="30387-696">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="30387-697">[11257]</span><span class="sxs-lookup"><span data-stu-id="30387-697">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="30387-698">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="30387-698">Az.DataFactory</span></span>
* <span data-ttu-id="30387-699">Пакет SDK ADF для .NET обновлен до версии 4.8.0.</span><span class="sxs-lookup"><span data-stu-id="30387-699">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="30387-700">Добавлены необязательные параметры для команды Invoke-AzDataFactoryV2Pipeline для поддержки повторного запуска.</span><span class="sxs-lookup"><span data-stu-id="30387-700">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="30387-701">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="30387-701">Az.DataLakeStore</span></span>
* <span data-ttu-id="30387-702">Добавлено описание критического изменения для Export-AzDataLakeStoreItem и Import-AzDataLakeStoreItem.</span><span class="sxs-lookup"><span data-stu-id="30387-702">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="30387-703">Добавлен параметр кодирования байтов для New-AzDataLakeStoreItem, Add-AzDAtaLakeStoreItemContent и Get-AzDAtaLakeStoreItemContent.</span><span class="sxs-lookup"><span data-stu-id="30387-703">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="30387-704">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="30387-704">Az.HDInsight</span></span>
* <span data-ttu-id="30387-705">Добавлена поддержка указания минимальной поддерживаемой версии TLS при создании кластера.</span><span class="sxs-lookup"><span data-stu-id="30387-705">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="30387-706">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="30387-706">Az.IotHub</span></span>
* <span data-ttu-id="30387-707">Добавлена поддержка для управления распределенными параметрами на отдельных устройствах.</span><span class="sxs-lookup"><span data-stu-id="30387-707">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="30387-708">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="30387-708">New Cmdlets are:</span></span>
    - <span data-ttu-id="30387-709">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="30387-709">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="30387-710">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="30387-710">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="30387-711">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="30387-711">Az.KeyVault</span></span>
* <span data-ttu-id="30387-712">Добавлены атрибуты критических изменений для New-AzKeyVault.</span><span class="sxs-lookup"><span data-stu-id="30387-712">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="30387-713">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="30387-713">Az.Monitor</span></span>
* <span data-ttu-id="30387-714">Обновлена документация для New-AzScheduledQueryRuleLogMetricTrigger.</span><span class="sxs-lookup"><span data-stu-id="30387-714">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30387-715">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30387-715">Az.Network</span></span>
* <span data-ttu-id="30387-716">Обновлены командлеты для поддержки подключений VirtualHubVnetConnections между клиентами</span><span class="sxs-lookup"><span data-stu-id="30387-716">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="30387-717">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="30387-717">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="30387-718">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="30387-718">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="30387-719">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="30387-719">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="30387-720">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="30387-720">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="30387-721">Удалена зависимость пакета SDK для управления SQL.</span><span class="sxs-lookup"><span data-stu-id="30387-721">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="30387-722">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="30387-722">Az.PolicyInsights</span></span>
* <span data-ttu-id="30387-723">Улучшены сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="30387-723">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="30387-724">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="30387-724">Az.RecoveryServices</span></span>
* <span data-ttu-id="30387-725">В Azure Site Recovery реализована поддержка повторной защиты и обновлены свойства зашифрованных виртуальных машин диска Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-725">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="30387-726">Добавлена возможность мониторинг аварийного восстановления для свойств VmwareToAzure в Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="30387-726">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="30387-727">В Azure Backup реализована поддержка повторного обновления политики для элементов с ошибками.</span><span class="sxs-lookup"><span data-stu-id="30387-727">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="30387-728">В Azure Backup реализована поддержка параметров исключения диска во время резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="30387-728">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="30387-729">В Azure Backup реализована поддержка восстановления нескольких файлов или папок в AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="30387-729">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="30387-730">В Azure Backup реализована поддержка указанной пользователем группы Resourcegroup при обновлении политики IaasVM.</span><span class="sxs-lookup"><span data-stu-id="30387-730">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="30387-731">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30387-731">Az.Resources</span></span>
* <span data-ttu-id="30387-732">Исправлена команда Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType для использования фактической версии apiVersion ресурсов (а не версии apiVersion по умолчанию) [11267].</span><span class="sxs-lookup"><span data-stu-id="30387-732">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="30387-733">Добавлена возможность регистрации correlationId для сценариев с ошибками.</span><span class="sxs-lookup"><span data-stu-id="30387-733">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="30387-734">Незначительно изменена документация по Get-AzResourceLock.</span><span class="sxs-lookup"><span data-stu-id="30387-734">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="30387-735">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="30387-735">Added example.</span></span>
* <span data-ttu-id="30387-736">Экранирована одинарная кавычка в значении параметра Get-AzADUser [11317].</span><span class="sxs-lookup"><span data-stu-id="30387-736">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="30387-737">Добавлены новые командлеты для сценариев развертывания (Get-AzDeploymentScript, Get-AzDeploymentScriptLog, Save-AzDeploymentScriptLog, Remove-AzDeploymentScript).</span><span class="sxs-lookup"><span data-stu-id="30387-737">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="30387-738">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30387-738">Az.Sql</span></span>
* <span data-ttu-id="30387-739">Добавлен параметр вторичной реплики для чтения для командлета Invoke-AzSqlDatabaseFailover.</span><span class="sxs-lookup"><span data-stu-id="30387-739">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="30387-740">Добавлен командлет Disable-AzSqlServerActiveDirectoryOnlyAuthentication.</span><span class="sxs-lookup"><span data-stu-id="30387-740">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="30387-741">Сохранен приоритет конфиденциальности при классификации столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="30387-741">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="30387-742">Az.Support</span><span class="sxs-lookup"><span data-stu-id="30387-742">Az.Support</span></span>
* <span data-ttu-id="30387-743">Модуль Az.Support стал общедоступным.</span><span class="sxs-lookup"><span data-stu-id="30387-743">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="30387-744">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="30387-744">Az.Websites</span></span>
* <span data-ttu-id="30387-745">Реализована поддержка работы с правилами маршрутизации трафика веб-приложения через указанные ниже командлеты</span><span class="sxs-lookup"><span data-stu-id="30387-745">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="30387-746">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="30387-746">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="30387-747">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="30387-747">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="30387-748">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="30387-748">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="30387-749">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="30387-749">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="30387-750">3.6.1 — март 2020 г.</span><span class="sxs-lookup"><span data-stu-id="30387-750">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="30387-751">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30387-751">Az.Accounts</span></span>
* <span data-ttu-id="30387-752">Открытие страницы опроса Azure PowerShell в Send-Feedback [11020].</span><span class="sxs-lookup"><span data-stu-id="30387-752">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="30387-753">Отображение URL-адреса опроса Azure PowerShell в Resolve-Error [11021].</span><span class="sxs-lookup"><span data-stu-id="30387-753">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="30387-754">Добавлена версия Az в UserAgent.</span><span class="sxs-lookup"><span data-stu-id="30387-754">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="30387-755">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="30387-755">Az.ApiManagement</span></span>
* <span data-ttu-id="30387-756">Включена поддержка получения и настройки личного домена в конечной точке DeveloperPortal [11007].</span><span class="sxs-lookup"><span data-stu-id="30387-756">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="30387-757">Export-AzApiManagementApi: включена поддержка скачивания определения API в формате JSON [9987].</span><span class="sxs-lookup"><span data-stu-id="30387-757">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="30387-758">Import-AzApiManagementApi: включена поддержка импорта определения OpenApi 3.0 из документа JSON.</span><span class="sxs-lookup"><span data-stu-id="30387-758">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="30387-759">New-AzApiManagementIdentityProvider и Set-AzApiManagementIdentityProvider: включена поддержка настройки входа арендатора для поставщика AAD B2C [9784].</span><span class="sxs-lookup"><span data-stu-id="30387-759">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="30387-760">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="30387-760">Az.DataLakeStore</span></span>
* <span data-ttu-id="30387-761">Добавлена ссылка на System.Buffers явным образом в CSPROJ и PSD1.</span><span class="sxs-lookup"><span data-stu-id="30387-761">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="30387-762">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="30387-762">Az.IotHub</span></span>
* <span data-ttu-id="30387-763">Добавлена возможность управления устройствами в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="30387-763">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="30387-764">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="30387-764">New Cmdlets are:</span></span>
    - <span data-ttu-id="30387-765">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="30387-765">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="30387-766">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="30387-766">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="30387-767">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="30387-767">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="30387-768">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="30387-768">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="30387-769">Включена поддержка управления модулями в целевом устройстве Интернета вещей в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="30387-769">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="30387-770">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="30387-770">New Cmdlets are:</span></span>
    - <span data-ttu-id="30387-771">Add-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="30387-771">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="30387-772">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="30387-772">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="30387-773">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="30387-773">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="30387-774">Set-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="30387-774">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="30387-775">Добавлен командлет для получения строки подключения целевого устройства Интернета вещей в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="30387-775">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="30387-776">Добавлен командлет для получения строки подключения модуля на целевом устройстве Интернета вещей в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="30387-776">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="30387-777">Включена поддержка для получения или настройки родительского устройства для устройства Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="30387-777">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="30387-778">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="30387-778">New Cmdlets are:</span></span>
    - <span data-ttu-id="30387-779">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="30387-779">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="30387-780">Set-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="30387-780">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="30387-781">Включена поддержка управления связью "родители — потомки" устройства.</span><span class="sxs-lookup"><span data-stu-id="30387-781">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="30387-782">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="30387-782">Az.Monitor</span></span>
* <span data-ttu-id="30387-783">Исправлено выходное значение для Get-AzMetricDefinition [9714].</span><span class="sxs-lookup"><span data-stu-id="30387-783">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30387-784">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30387-784">Az.Network</span></span>
* <span data-ttu-id="30387-785">Обновлен пакет SDK для управления SQL.</span><span class="sxs-lookup"><span data-stu-id="30387-785">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="30387-786">Исправлена проблема с разницей в именовании в классе PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="30387-786">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="30387-787">Сопоставление ActionsRequired с ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="30387-787">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="30387-788">Добавление PublicNetworkAccess в команды New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="30387-788">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="30387-789">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30387-789">Az.Resources</span></span>
* <span data-ttu-id="30387-790">Исправлена ошибка пустой ссылки в Get-AzRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="30387-790">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="30387-791">Параметры -Force и -PassThru помечены необязательными в Remove-AzADGroup [10849].</span><span class="sxs-lookup"><span data-stu-id="30387-791">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="30387-792">Исправлена ошибка, из-за которой MailNickname не возвращается в Remove-AzADGroup [11167].</span><span class="sxs-lookup"><span data-stu-id="30387-792">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="30387-793">Исправлена ошибка, из-за которой операция канала Remove-AzADGroup не работает [11171].</span><span class="sxs-lookup"><span data-stu-id="30387-793">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="30387-794">Исправлена ошибка с пустой ссылкой в GetAzureRoleAssignmentCommand.</span><span class="sxs-lookup"><span data-stu-id="30387-794">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="30387-795">Добавлено критическое изменение атрибутов для будущих изменений командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="30387-795">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="30387-796">Обновлена команда Get-AzResourceGroup для выполнения фильтрации тегов группы ресурсов на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="30387-796">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="30387-797">Расширены командлеты Tag для включения поддержки параметра -ResourceId.</span><span class="sxs-lookup"><span data-stu-id="30387-797">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="30387-798">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="30387-798">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="30387-799">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="30387-799">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="30387-800">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="30387-800">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="30387-801">Добавлен новый командлет Tag.</span><span class="sxs-lookup"><span data-stu-id="30387-801">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="30387-802">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="30387-802">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="30387-803">Предоставляется ScopedDeployment из пакета SDK 3.3.0.</span><span class="sxs-lookup"><span data-stu-id="30387-803">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="30387-804">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30387-804">Az.Sql</span></span>
* <span data-ttu-id="30387-805">Добавление PublicNetworkAccess в команды New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="30387-805">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="30387-806">Включена поддержка конфигурации резервного копирования долгосрочного хранения для управляемых баз данных.</span><span class="sxs-lookup"><span data-stu-id="30387-806">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="30387-807">Получение или настройка политики LTR в управляемой базе данных.</span><span class="sxs-lookup"><span data-stu-id="30387-807">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="30387-808">Получение резервных копий LTR по управляемой базе данных, управляемому экземпляру или расположению.</span><span class="sxs-lookup"><span data-stu-id="30387-808">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="30387-809">Удаление резервной копии LTR.</span><span class="sxs-lookup"><span data-stu-id="30387-809">Remove an LTR backup</span></span>
    - <span data-ttu-id="30387-810">Восстановление резервной копии LTR для создания новой управляемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="30387-810">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="30387-811">Добавление MinimalTlsVersion в New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="30387-811">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="30387-812">Добавление MinimalTlsVersion в New-AzSqlInstance и Set-AzSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="30387-812">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="30387-813">Обновлена версия пакета SDK для SQL для Az.Network.</span><span class="sxs-lookup"><span data-stu-id="30387-813">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="30387-814">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="30387-814">Az.Storage</span></span>
* <span data-ttu-id="30387-815">Включена поддержка AllowProtectedAppendWrite в ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="30387-815">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="30387-816">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="30387-816">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="30387-817">Добавлено предупреждение о критическом изменении для изменения типа AzureStorageTable в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="30387-817">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="30387-818">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="30387-818">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="30387-819">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="30387-819">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="30387-820">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="30387-820">Az.Websites</span></span>
* <span data-ttu-id="30387-821">Добавлен параметр Tag для New-AzAppServicePlan и Set-AzAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="30387-821">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="30387-822">Завершение выполнения командлета, если при добавлении личного домена на веб-сайт возникает исключение.</span><span class="sxs-lookup"><span data-stu-id="30387-822">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="30387-823">Включена поддержка выполнения операций для Служб приложений, которые находятся не в той же группе ресурсов, что и план службы приложений.</span><span class="sxs-lookup"><span data-stu-id="30387-823">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="30387-824">Применение ограничения доступа к WebApp/Function в разных группах ресурсов.</span><span class="sxs-lookup"><span data-stu-id="30387-824">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="30387-825">Исправлена ошибка с указанием пользовательских имен узлов для WebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="30387-825">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="30387-826">3.5.0 — февраль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="30387-826">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="30387-827">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="30387-827">Highlights since the last major release</span></span>
* <span data-ttu-id="30387-828">Обновлены данные телеметрии на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="30387-828">Updated client side telemetry.</span></span>
* <span data-ttu-id="30387-829">В Az.IotHub добавлены командлеты для управления устройствами.</span><span class="sxs-lookup"><span data-stu-id="30387-829">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="30387-830">В Az.SqlVirtualMachine добавлены командлеты для прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="30387-830">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="30387-831">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30387-831">Az.Accounts</span></span>
* <span data-ttu-id="30387-832">В данные телеметрии на стороне клиента добавлены такие сведения, как идентификатор подписки, идентификатор арендатора и время выполнения.</span><span class="sxs-lookup"><span data-stu-id="30387-832">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="30387-833">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="30387-833">Az.Automation</span></span>
* <span data-ttu-id="30387-834">Исправлена опечатка в примере 1 в справочной документации по New-AzAutomationSoftwareUpdateConfiguration.</span><span class="sxs-lookup"><span data-stu-id="30387-834">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="30387-835">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="30387-835">Az.CognitiveServices</span></span>
* <span data-ttu-id="30387-836">Обновлен пакет SDK до версии 7.0.</span><span class="sxs-lookup"><span data-stu-id="30387-836">Updated SDK to 7.0</span></span>
* <span data-ttu-id="30387-837">Улучшено сообщение об ошибке, которое появляется, если ответы сервера не содержат текст.</span><span class="sxs-lookup"><span data-stu-id="30387-837">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30387-838">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30387-838">Az.Compute</span></span>
* <span data-ttu-id="30387-839">Разрешено использовать пустое значение для ProximityPlacementGroupId во время обновления.</span><span class="sxs-lookup"><span data-stu-id="30387-839">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="30387-840">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="30387-840">Az.FrontDoor</span></span>
* <span data-ttu-id="30387-841">Добавлен командлет для получения определений управляемых правил, которые могут использоваться в WAF.</span><span class="sxs-lookup"><span data-stu-id="30387-841">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="30387-842">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="30387-842">Az.IotHub</span></span>
* <span data-ttu-id="30387-843">Добавлена возможность управления устройствами в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="30387-843">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="30387-844">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="30387-844">New Cmdlets are:</span></span>
    - <span data-ttu-id="30387-845">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="30387-845">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="30387-846">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="30387-846">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="30387-847">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="30387-847">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="30387-848">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="30387-848">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="30387-849">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="30387-849">Az.KeyVault</span></span>
* <span data-ttu-id="30387-850">Устранен дублирующийся текст для Add-AzKeyVaultKey.md.</span><span class="sxs-lookup"><span data-stu-id="30387-850">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="30387-851">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="30387-851">Az.Monitor</span></span>
* <span data-ttu-id="30387-852">Исправлено описание командлета Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="30387-852">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="30387-853">В команду New-AzMetricAlertRuleV2 добавлен новый параметр ActionGroupId.</span><span class="sxs-lookup"><span data-stu-id="30387-853">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="30387-854">Пользователь может предоставить ActionGroupId(string) или ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="30387-854">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30387-855">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30387-855">Az.Network</span></span>
* <span data-ttu-id="30387-856">Добавлен еще один параметр -EnableProxyProtocol для командлета New-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="30387-856">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="30387-857">Исправлен пример FilterData в Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="30387-857">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="30387-858">Добавлен пример Packet Capture для всех внутренних и внешних пакетов в Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="30387-858">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="30387-859">Добавлена поддерживаемая политика Брандмауэра Azure в брандмауэрах виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="30387-859">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="30387-860">Новые командлеты не добавлены.</span><span class="sxs-lookup"><span data-stu-id="30387-860">No new cmdlets are added.</span></span> <span data-ttu-id="30387-861">Снято ограничение политики брандмауэра в брандмауэрах виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="30387-861">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="30387-862">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="30387-862">Az.RecoveryServices</span></span>
* <span data-ttu-id="30387-863">Добавлена возможность восстановления в виде файлов для Баз данных SQL.</span><span class="sxs-lookup"><span data-stu-id="30387-863">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="30387-864">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30387-864">Az.Resources</span></span>
* <span data-ttu-id="30387-865">Выполнен рефакторинг командлетов развертывания шаблона.</span><span class="sxs-lookup"><span data-stu-id="30387-865">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="30387-866">Добавлены новые командлеты для управления развертываниями в группе управления: \*-AzManagementGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="30387-866">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="30387-867">Добавлены новые командлеты для управления развертываниями в области арендатора: \*-AzTenantDeployment.</span><span class="sxs-lookup"><span data-stu-id="30387-867">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="30387-868">Выполнен рефакторинг командлетов \*-AzDeployment для работы в области подписки.</span><span class="sxs-lookup"><span data-stu-id="30387-868">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="30387-869">Созданы псевдонимы \*-AzSubscriptionDeployment для командлетов \*-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="30387-869">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="30387-870">Исправлен командлет Update-AzADApplication, когда параметр AvailableToOtherTenants не задан.</span><span class="sxs-lookup"><span data-stu-id="30387-870">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="30387-871">Удален набор параметров ApplicationObjectWithoutCredentialParameterSet, чтобы предотвратить возникновение AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="30387-871">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="30387-872">Повторно созданы файлы справки.</span><span class="sxs-lookup"><span data-stu-id="30387-872">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="30387-873">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30387-873">Az.Sql</span></span>
* <span data-ttu-id="30387-874">Добавлена возможность восстановления точки во времени между подписками в Управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="30387-874">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="30387-875">Добавлена возможность изменения существующего поколения оборудования Управляемого экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="30387-875">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="30387-876">Исправлены примеры справки Update-AzSqlServerVulnerabilityAssessmentSetting: выходные данные параметра и свойства — EmailAdmins.</span><span class="sxs-lookup"><span data-stu-id="30387-876">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="30387-877">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="30387-877">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="30387-878">Добавлены командлеты для прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="30387-878">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="30387-879">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="30387-879">Az.StorageSync</span></span>
* <span data-ttu-id="30387-880">В командлете Invoke-AzStorageSyncCompatibilityCheck обновлены поддерживаемые наборы символов.</span><span class="sxs-lookup"><span data-stu-id="30387-880">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="30387-881">3.4.0 — февраль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="30387-881">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="30387-882">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="30387-882">Highlights since the last major release</span></span>
* <span data-ttu-id="30387-883">Выпущена первоначальная версия 0.1.0 Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="30387-883">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="30387-884">Добавлена поддержка Az.Network ConnectionMonitor V2</span><span class="sxs-lookup"><span data-stu-id="30387-884">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="30387-885">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30387-885">Az.Accounts</span></span>
* <span data-ttu-id="30387-886">Отключить автоматическое сохранение контекста, если AzureRmContext.json недоступен</span><span class="sxs-lookup"><span data-stu-id="30387-886">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="30387-887">Обновление ссылки на Azure Powershell Common до предварительной версии 1.3.5</span><span class="sxs-lookup"><span data-stu-id="30387-887">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="30387-888">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="30387-888">Az.ApiManagement</span></span>
* <span data-ttu-id="30387-889">**Get-AzApiManagementApiSchema** Исправлено получение схемы Open-API, связанной с API https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="30387-889">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="30387-890">**New-AzApiManagementProduct**\* и **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="30387-890">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="30387-891">Исправить документацию для https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="30387-891">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="30387-892">**Set-AzApiManagementApi** Добавлен пример, показывающий, как обновить ServiceUrl с помощью командлета</span><span class="sxs-lookup"><span data-stu-id="30387-892">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30387-893">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30387-893">Az.Compute</span></span>
* <span data-ttu-id="30387-894">Ограничение числа состояний виртуальных машин до 100, чтобы избежать регулирования при выполнении Get-AzVM-Status без имени виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="30387-894">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="30387-895">Добавление обновления командлета -AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="30387-895">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="30387-896">Добавление параметров EncryptionType и DiskEncryptionSetId в следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="30387-896">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="30387-897">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="30387-897">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="30387-898">Добавление параметра ColocationStatus в командлет Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="30387-898">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="30387-899">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="30387-899">Az.DataFactory</span></span>
* <span data-ttu-id="30387-900">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.7.0.</span><span class="sxs-lookup"><span data-stu-id="30387-900">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="30387-901">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="30387-901">Az.DeploymentManager</span></span>
* <span data-ttu-id="30387-902">Добавляет операции LIST для ресурсов</span><span class="sxs-lookup"><span data-stu-id="30387-902">Adds LIST operations for resources</span></span>
* <span data-ttu-id="30387-903">Добавляет возможность выполнения операций на этапах Проверки работоспособности</span><span class="sxs-lookup"><span data-stu-id="30387-903">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="30387-904">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="30387-904">Az.HDInsight</span></span>
* <span data-ttu-id="30387-905">Исправление ошибки в документе New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="30387-905">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="30387-906">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="30387-906">Az.KeyVault</span></span>
* <span data-ttu-id="30387-907">Добавление Псевдонимов имени в атрибут VaultName, чтобы Remove-AzureKeyVault соответствовал New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="30387-907">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30387-908">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30387-908">Az.Network</span></span>
* <span data-ttu-id="30387-909">В Set-AzNetworkWatcherConfigFlowLog.md добавлен новый пример для демонстрации сценария отключения Аналитики трафика.</span><span class="sxs-lookup"><span data-stu-id="30387-909">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="30387-910">Добавление поддержки назначения IP-конфигурации для брандмауэра Azure — выделенная подсеть и общедоступный IP-адрес, которые брандмауэр будет использовать для управления трафиком</span><span class="sxs-lookup"><span data-stu-id="30387-910">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="30387-911">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="30387-911">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="30387-912">добавлен параметр — ManagementPublicIpAddress (необязательный), который принимает объект общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="30387-912">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="30387-913">Добавлен метод SetManagementIpConfiguration для объекта брандмауэра — в качестве входных данных требуется подсеть и общедоступный IP-адрес — имя подсети должно быть "AzureFirewallManagementSubnet"</span><span class="sxs-lookup"><span data-stu-id="30387-913">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="30387-914">Исправлены примеры Get-AzNetworkSecurityGroup для отображения примеров для группы безопасности сети (NSG) вместо сетевых интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="30387-914">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="30387-915">Исправлена опечатка в команде New-AzVpnSite, которая препятствовала завершению параметра идентификатором ресурса.</span><span class="sxs-lookup"><span data-stu-id="30387-915">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="30387-916">Добавлена поддержка конфигурации в наборе действий для правил подстановки URL-адресов в шлюзе приложения.</span><span class="sxs-lookup"><span data-stu-id="30387-916">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="30387-917">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="30387-917">New cmdlets added:</span></span>
        - <span data-ttu-id="30387-918">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="30387-918">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="30387-919">В следующие командлеты добавлен необязательный параметр — UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="30387-919">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="30387-920">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="30387-920">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="30387-921">Добавление поддержки для ресурсов NetworkWatcher ConnectionMonitor версии 2</span><span class="sxs-lookup"><span data-stu-id="30387-921">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="30387-922">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="30387-922">Az.PolicyInsights</span></span>
* <span data-ttu-id="30387-923">Поддержка оценки соответствия до определения того, какой ресурс нужно исправить</span><span class="sxs-lookup"><span data-stu-id="30387-923">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="30387-924">Добавление параметра "—ResourceDiscoverMode" в Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="30387-924">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="30387-925">Добавление командлета Get-AzPolicyMetadata для получения ресурсов метаданных политики</span><span class="sxs-lookup"><span data-stu-id="30387-925">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="30387-926">Get-AzPolicyState и Get-AzPolicyStateSummary обновлены для API версии 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="30387-926">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="30387-927">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="30387-927">Az.RecoveryServices</span></span>
* <span data-ttu-id="30387-928">Поддержка Azure Site Recovery для удаления реплицированного диска.</span><span class="sxs-lookup"><span data-stu-id="30387-928">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="30387-929">В Azure Backup добавлена ​​поддержка добавления тегов при создании Хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="30387-929">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="30387-930">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30387-930">Az.Resources</span></span>
* <span data-ttu-id="30387-931">Сделайте команду "Область" необязательной в командлетах \*—AzPolicyAssignment с настройкой по умолчанию для контекстной подписки</span><span class="sxs-lookup"><span data-stu-id="30387-931">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="30387-932">Добавление примеров создания ADServicePrincipal с паролем и ключом учетных данных</span><span class="sxs-lookup"><span data-stu-id="30387-932">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="30387-933">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30387-933">Az.Sql</span></span>
<span data-ttu-id="30387-934">Исправление командлета New-AzSqlDatabaseSecondary, чтобы проверить существование PartnerDatabaseName, а не DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="30387-934">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="30387-935">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="30387-935">Az.Storage</span></span>
* <span data-ttu-id="30387-936">Поддержка набора шифрования типа ключа таблиц и очередей в создании учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="30387-936">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="30387-937">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30387-937">New-AzStorageAccount</span></span>
* <span data-ttu-id="30387-938">Представление RequestId, если StorageException не имеет ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="30387-938">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="30387-939">Исправление примера 6 командлета Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="30387-939">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="30387-940">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="30387-940">Az.Websites</span></span>
* <span data-ttu-id="30387-941">Set-AzWebapp и Set-AzWebappSlot поддерживают свойства AlwaysOn, MinTls и FtpsState</span><span class="sxs-lookup"><span data-stu-id="30387-941">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="30387-942">Устранение проблемы, при которой параметр HttpsOnly с одновременным изменением AppservicePlan с помощью одной команды Set-AzWebApp сбрасывал значение HttpsOnly до значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="30387-942">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="30387-943">3.3.0 — январь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="30387-943">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="30387-944">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30387-944">Az.Accounts</span></span>
* <span data-ttu-id="30387-945">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment: теперь они принимают параметры AzureAttestationServiceEndpointResourceId и AzureAttestationServiceEndpointSuffix.</span><span class="sxs-lookup"><span data-stu-id="30387-945">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="30387-946">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="30387-946">Az.Cdn</span></span>
* <span data-ttu-id="30387-947">Теперь в командлете New-AzCdnEndpoint отображаются сведения из сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="30387-947">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30387-948">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30387-948">Az.Compute</span></span>
* <span data-ttu-id="30387-949">Командлет Set-AzVMCustomScriptExtension исправлен для виртуальной машины с управляемым диском ОС без профиля ОС.</span><span class="sxs-lookup"><span data-stu-id="30387-949">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="30387-950">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="30387-950">Az.ContainerInstance</span></span>
* <span data-ttu-id="30387-951">Исправлены имена параметров, используемые в примере командлета New-AzContainerGroup.</span><span class="sxs-lookup"><span data-stu-id="30387-951">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="30387-952">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="30387-952">Az.DataBoxEdge</span></span>
* <span data-ttu-id="30387-953">Добавлен командлет Get-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="30387-953">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="30387-954">получение контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="30387-954">Get the Edge Storage Container</span></span>
* <span data-ttu-id="30387-955">Добавлен командлет New-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="30387-955">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="30387-956">создание контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="30387-956">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="30387-957">Добавлен командлет Remove-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="30387-957">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="30387-958">удаление контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="30387-958">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="30387-959">Добавлен командлет Invoke-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="30387-959">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="30387-960">вызов действия для обновления данных в контейнере хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="30387-960">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="30387-961">Добавлен командлет Get-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="30387-961">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="30387-962">получение учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="30387-962">Get the Edge Storage Account</span></span>
* <span data-ttu-id="30387-963">Добавлен командлет New-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="30387-963">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="30387-964">создание учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="30387-964">Create new Edge Storage Account</span></span>
* <span data-ttu-id="30387-965">Добавлен командлет Remove-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="30387-965">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="30387-966">удаление учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="30387-966">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="30387-967">Вызов командлета Invoke-AzDataBoxEdgeShare:</span><span class="sxs-lookup"><span data-stu-id="30387-967">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="30387-968">вызов действия для обновления данных в общей папке.</span><span class="sxs-lookup"><span data-stu-id="30387-968">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="30387-969">Добавлен командлет Set-AzDataBoxEdgeStorageAccountCredential:</span><span class="sxs-lookup"><span data-stu-id="30387-969">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="30387-970">установка учетных данных для учетной записи хранилища Azure Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="30387-970">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="30387-971">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="30387-971">Az.DataFactory</span></span>
* <span data-ttu-id="30387-972">Добавлены свойства AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId и VersionStatus для командлета Get-AzDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="30387-972">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="30387-973">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.6.0.</span><span class="sxs-lookup"><span data-stu-id="30387-973">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="30387-974">Для командлета Set-AzureRmDataFactoryV2IntegrationRuntime добавлен параметр PublicIPs, позволяющий включить создание среды Azure-SSIS IR со статическими общедоступными IP-адресами.</span><span class="sxs-lookup"><span data-stu-id="30387-974">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="30387-975">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="30387-975">Az.DevTestLabs</span></span>
* <span data-ttu-id="30387-976">Удалена недействительная ссылка в файле Get-AzDtlAllowedVMSizesPolicy.md.</span><span class="sxs-lookup"><span data-stu-id="30387-976">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="30387-977">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="30387-977">Az.EventHub</span></span>
* <span data-ttu-id="30387-978">Устранена проблема № 10634: исправлена ссылка на пустой объект для удаления пространства имен концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="30387-978">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="30387-979">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="30387-979">Az.HDInsight</span></span>
* <span data-ttu-id="30387-980">Устранена ошибка в файле Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="30387-980">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="30387-981">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="30387-981">Az.MachineLearning</span></span>
* <span data-ttu-id="30387-982">Вычислительная среда Машинного обучения больше недоступна, поэтому удалены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="30387-982">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="30387-983">Get-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="30387-983">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="30387-984">Get-AzMlOpClusterKey;</span><span class="sxs-lookup"><span data-stu-id="30387-984">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="30387-985">New-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="30387-985">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="30387-986">Remove-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="30387-986">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="30387-987">Set-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="30387-987">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="30387-988">Test-AzMlOpClusterSystemServicesUpdateAvailability;</span><span class="sxs-lookup"><span data-stu-id="30387-988">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="30387-989">Update-AzMlOpClusterSystemService.</span><span class="sxs-lookup"><span data-stu-id="30387-989">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30387-990">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30387-990">Az.Network</span></span>
* <span data-ttu-id="30387-991">Обновлена зависимость Microsoft.Azure.Management.Sql от предварительной версии 1.36 до предварительной версии 1.37.</span><span class="sxs-lookup"><span data-stu-id="30387-991">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="30387-992">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="30387-992">Az.RecoveryServices</span></span>
* <span data-ttu-id="30387-993">Добавлена поддержка Azure Site Recovery для виртуальных машин с управляемым диском, зашифрованных при хранении с помощью управляемых клиентом ключей, при восстановлении из Azure в поставщике Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-993">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="30387-994">Добавлена поддержка Azure Site Recovery для необязательного ввода идентификатора набора шифрования диска при включении защиты в рамках восстановления из VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-994">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="30387-995">Добавлена поддержка Azure Site Recovery для необязательного ввода идентификатора набора шифрования диска на уровне диска при включении защиты в рамках восстановления из VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-995">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="30387-996">Добавлена поддержка Azure Site Recovery для обновления элемента, защищенного репликацией, путем сопоставления набора шифрования диска при восстановлении из HyperV в Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-996">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="30387-997">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30387-997">Az.Resources</span></span>
* <span data-ttu-id="30387-998">Исправлена ошибка в справочном документе о командлете Remove-AzTag.</span><span class="sxs-lookup"><span data-stu-id="30387-998">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="30387-999">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30387-999">Az.Sql</span></span>
* <span data-ttu-id="30387-1000">Исправлена функция основных командлетов установки оценки уязвимостей: теперь она позволяет работать с базой данных master для базы данных Azure и ограничить ее в системных базах данных управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="30387-1000">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="30387-1001">Устранена ошибка, возникающая при создании группы отработки отказа экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="30387-1001">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="30387-1002">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="30387-1002">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="30387-1003">Добавлен новый допустимый тип лицензии: DR (аварийное восстановление).</span><span class="sxs-lookup"><span data-stu-id="30387-1003">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="30387-1004">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="30387-1004">Az.Storage</span></span>
* <span data-ttu-id="30387-1005">Добавлено предупреждающее сообщение о критическом изменении значения DefaultAction в следующем выпуске:</span><span class="sxs-lookup"><span data-stu-id="30387-1005">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="30387-1006">Update-AzStorageAccountNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="30387-1006">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="30387-1007">Включена поддержка получения времени последней синхронизации учетной записи хранения путем выполнения командлета Get-AzureRmStorageAccount с параметром -IncludeGeoReplicationStats:</span><span class="sxs-lookup"><span data-stu-id="30387-1007">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="30387-1008">Get-AzureRmStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="30387-1008">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="30387-1009">3.2.0 — декабрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="30387-1009">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="30387-1010">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="30387-1010">General</span></span>
* <span data-ttu-id="30387-1011">Обновление ссылок в .psd1 для использования относительного пути для всех модулей.</span><span class="sxs-lookup"><span data-stu-id="30387-1011">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="30387-1012">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30387-1012">Az.Accounts</span></span>
* <span data-ttu-id="30387-1013">Установка правильного параметра UserAgent для телеметрии на стороне клиента для Az 4.0 (предварительная версия).</span><span class="sxs-lookup"><span data-stu-id="30387-1013">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="30387-1014">Отображение понятного пользователю сообщения об ошибке, если в Az 4.0 (предварительная версия) не указан контекст.</span><span class="sxs-lookup"><span data-stu-id="30387-1014">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="30387-1015">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="30387-1015">Az.Batch</span></span>
* <span data-ttu-id="30387-1016">Исправлена проблема [№ 10602](https://github.com/Azure/azure-powershell/issues/10602), из-за которой использование командлета **New-AzBatchPool** приводило к неправильной отправке VirtualMachineConfiguration.ContainerConfiguration или VirtualMachineConfiguration.DataDisks на сервер.</span><span class="sxs-lookup"><span data-stu-id="30387-1016">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="30387-1017">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="30387-1017">Az.DataFactory</span></span>
* <span data-ttu-id="30387-1018">Обновление пакета SDK Фабрики данных для .NET до версии 4.5.0.</span><span class="sxs-lookup"><span data-stu-id="30387-1018">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="30387-1019">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="30387-1019">Az.FrontDoor</span></span>
* <span data-ttu-id="30387-1020">Включена поддержка исключений управляемых правил WAF.</span><span class="sxs-lookup"><span data-stu-id="30387-1020">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="30387-1021">Добавление SocketAddr в список автозавершения.</span><span class="sxs-lookup"><span data-stu-id="30387-1021">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="30387-1022">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="30387-1022">Az.HealthcareApis</span></span>
* <span data-ttu-id="30387-1023">Обработка исключений.</span><span class="sxs-lookup"><span data-stu-id="30387-1023">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="30387-1024">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="30387-1024">Az.KeyVault</span></span>
* <span data-ttu-id="30387-1025">Исправлена ошибка при получении доступа к значению, которое может быть не задано.</span><span class="sxs-lookup"><span data-stu-id="30387-1025">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="30387-1026">Управление сертификатами шифрования на основе эллиптических кривых.</span><span class="sxs-lookup"><span data-stu-id="30387-1026">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="30387-1027">Включена возможность указания кривой для политик сертификатов.</span><span class="sxs-lookup"><span data-stu-id="30387-1027">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="30387-1028">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="30387-1028">Az.Monitor</span></span>
* <span data-ttu-id="30387-1029">Добавление необязательного аргумента в команду добавления параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="30387-1029">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="30387-1030">Существующий аргумент switch указывает на то, что экспорт в Log Analytics должен выполняться в фиксированную схему</span><span class="sxs-lookup"><span data-stu-id="30387-1030">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="30387-1031">(выделенный тип данных).</span><span class="sxs-lookup"><span data-stu-id="30387-1031">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30387-1032">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30387-1032">Az.Network</span></span>
* <span data-ttu-id="30387-1033">В приложении AzureFirewall, NAT и сетевых правилах включена поддержка IpGroups.</span><span class="sxs-lookup"><span data-stu-id="30387-1033">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="30387-1034">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30387-1034">Az.Resources</span></span>
* <span data-ttu-id="30387-1035">Устранена проблема, из-за которой при развертывании шаблона не удавалось считать его параметр, если имя параметра конфликтовало с именем встроенного параметра.</span><span class="sxs-lookup"><span data-stu-id="30387-1035">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="30387-1036">Обновлены командлеты политики для использования новой версии API 2019-09-01 с поддержкой группирования в определениях наборов политик.</span><span class="sxs-lookup"><span data-stu-id="30387-1036">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="30387-1037">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30387-1037">Az.Sql</span></span>
* <span data-ttu-id="30387-1038">Обновлена функция автоматического создания расширенного хранилища для службы оценки уязвимостей в учетной записи StorageV2.</span><span class="sxs-lookup"><span data-stu-id="30387-1038">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="30387-1039">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="30387-1039">Az.Storage</span></span>
* <span data-ttu-id="30387-1040">Включена поддержка создания маркера SAS на основе удостоверения контейнера и большого двоичного объекта с аутентификацией Oauth на основе контекста службы хранилища:</span><span class="sxs-lookup"><span data-stu-id="30387-1040">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="30387-1041">New-AzStorageContainerSASToken;</span><span class="sxs-lookup"><span data-stu-id="30387-1041">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="30387-1042">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="30387-1042">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="30387-1043">Отозвана поддержка ключей делегирования пользователя учетной записи хранения, а также всех маркеров SAS удостоверения:</span><span class="sxs-lookup"><span data-stu-id="30387-1043">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="30387-1044">Revoke-AzStorageAccountUserDelegationKeys.</span><span class="sxs-lookup"><span data-stu-id="30387-1044">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="30387-1045">Выполнено обновление до Microsoft.Azure.Management.Storage версии 14.2.0 для включения поддержки нового API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="30387-1045">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="30387-1046">Включена поддержка QuotaGiB (квота общего ресурса в ГиБ) для значений свыше 5120 в командлетах для работы с общими папками в плоскости управления и добавлен псевдоним Quota для параметра QuotaGiB.</span><span class="sxs-lookup"><span data-stu-id="30387-1046">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="30387-1047">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="30387-1047">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="30387-1048">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="30387-1048">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="30387-1049">Добавлен псевдоним QuotaGiB для параметра Quota:</span><span class="sxs-lookup"><span data-stu-id="30387-1049">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="30387-1050">Set-AzStorageShareQuota.</span><span class="sxs-lookup"><span data-stu-id="30387-1050">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="30387-1051">Устранена проблема, из-за которой при использовании AzStorageContainerAcl могла очищаться хранимая политика доступа:</span><span class="sxs-lookup"><span data-stu-id="30387-1051">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="30387-1052">Set-AzStorageContainerAcl.</span><span class="sxs-lookup"><span data-stu-id="30387-1052">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="30387-1053">Версия 3.1.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="30387-1053">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="30387-1054">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="30387-1054">Highlights since the last major release</span></span>
* <span data-ttu-id="30387-1055">Выпуск Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="30387-1055">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="30387-1056">Выпуск Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="30387-1056">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30387-1057">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30387-1057">Az.Compute</span></span>
* <span data-ttu-id="30387-1058">Функция повторного применения виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="30387-1058">VM Reapply feature</span></span>
    - <span data-ttu-id="30387-1059">Добавлен параметр повторного применения в командлет Set-AzVM.</span><span class="sxs-lookup"><span data-stu-id="30387-1059">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="30387-1060">Функция AutomaticRepairs масштабируемого набора виртуальных машин:</span><span class="sxs-lookup"><span data-stu-id="30387-1060">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="30387-1061">Добавлены параметры EnableAutomaticRepair, AutomaticRepairGracePeriod и AutomaticRepairMaxInstanceRepairsPercent в следующие командлеты:   New-AzVmssConfig Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="30387-1061">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="30387-1062">Включена поддержка образа из коллекции разных клиентов для New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="30387-1062">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="30387-1063">Добавлен фрагмент Spot в средство заполнения аргументов параметра Priority в командлетах New-AzVM, New-AzVMConfig и New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="30387-1063">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="30387-1064">Добавлены параметры DiskIOPSReadWrite и DiskMBpsReadWrite в командлет Add-AzVmssDataDisk.</span><span class="sxs-lookup"><span data-stu-id="30387-1064">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="30387-1065">Изменен параметр SourceImageId командлета New-AzGalleryImageVersion на необязательный.</span><span class="sxs-lookup"><span data-stu-id="30387-1065">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="30387-1066">Добавлены параметры OSDiskImage и DataDiskImage в командлет New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="30387-1066">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="30387-1067">Добавлен параметр HyperVGeneration в командлет New-AzGalleryImageDefinition.</span><span class="sxs-lookup"><span data-stu-id="30387-1067">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="30387-1068">Добавлены параметры SkipExtensionsOnOverprovisionedVMs в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="30387-1068">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="30387-1069">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="30387-1069">Az.DataBoxEdge</span></span>
* <span data-ttu-id="30387-1070">Добавлен командлет `Get-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="30387-1070">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="30387-1071">Получение заказа.</span><span class="sxs-lookup"><span data-stu-id="30387-1071">Get the Order</span></span>
* <span data-ttu-id="30387-1072">Добавлен командлет `New-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="30387-1072">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="30387-1073">Создание заказа.</span><span class="sxs-lookup"><span data-stu-id="30387-1073">Create new Order</span></span>
* <span data-ttu-id="30387-1074">Добавлен командлет `Remove-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="30387-1074">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="30387-1075">Удаление заказа.</span><span class="sxs-lookup"><span data-stu-id="30387-1075">Remove the Order</span></span>
* <span data-ttu-id="30387-1076">Изменен командлет `New-AzDataBoxEdgeShare`.</span><span class="sxs-lookup"><span data-stu-id="30387-1076">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="30387-1077">Создание локальной общей папки.</span><span class="sxs-lookup"><span data-stu-id="30387-1077">Now creates Local Share</span></span>
* <span data-ttu-id="30387-1078">Добавлен командлет `Set-AzDataBoxEdgeRole`.</span><span class="sxs-lookup"><span data-stu-id="30387-1078">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="30387-1079">Сопоставление IotRole с общей папкой.</span><span class="sxs-lookup"><span data-stu-id="30387-1079">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="30387-1080">Добавлен командлет `Invoke-AzDataBoxEdgeDevice`.</span><span class="sxs-lookup"><span data-stu-id="30387-1080">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="30387-1081">Вызов проверки обновлений, скачивание обновления, установка обновления на устройстве.</span><span class="sxs-lookup"><span data-stu-id="30387-1081">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="30387-1082">Добавлен командлет `Get-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="30387-1082">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="30387-1083">Получение сведений о триггерах.</span><span class="sxs-lookup"><span data-stu-id="30387-1083">Gets the information about Triggers</span></span>
* <span data-ttu-id="30387-1084">Добавлен командлет `New-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="30387-1084">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="30387-1085">Создание триггеров.</span><span class="sxs-lookup"><span data-stu-id="30387-1085">Create new Triggers</span></span>
* <span data-ttu-id="30387-1086">Добавлен командлет `Remove-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="30387-1086">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="30387-1087">Удаление триггеров.</span><span class="sxs-lookup"><span data-stu-id="30387-1087">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="30387-1088">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="30387-1088">Az.DataFactory</span></span>
* <span data-ttu-id="30387-1089">Обновление пакета SDK Фабрики данных для .NET до версии 4.4.0.</span><span class="sxs-lookup"><span data-stu-id="30387-1089">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="30387-1090">Добавлен параметр ExpressCustomSetup в командлет Set-AzureRmDataFactoryV2IntegrationRuntime для включения конфигураций установки и сторонних компонентов без использования настраиваемого скрипта установки.</span><span class="sxs-lookup"><span data-stu-id="30387-1090">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="30387-1091">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="30387-1091">Az.DataLakeStore</span></span>
* <span data-ttu-id="30387-1092">Обновлена документация по Get-AzDataLakeStoreDeletedItem и Restore-AzDataLakeStoreDeletedItem.</span><span class="sxs-lookup"><span data-stu-id="30387-1092">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="30387-1093">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="30387-1093">Az.EventHub</span></span>
* <span data-ttu-id="30387-1094">Исправлена проблема № 10301. Исправлен формат даты маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="30387-1094">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="30387-1095">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="30387-1095">Az.FrontDoor</span></span>
* <span data-ttu-id="30387-1096">Добавлен параметр MinimumTlsVersion в Enable-AzFrontDoorCustomDomainHttps и New-AzFrontDoorFrontendEndpointObject.</span><span class="sxs-lookup"><span data-stu-id="30387-1096">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="30387-1097">Добавлены параметры HealthProbeMethod и EnabledState в New-AzFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="30387-1097">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="30387-1098">Добавлен новый командлет для создания объекта BackendPoolsSettings для передачи при создании и обновлении Front Door.</span><span class="sxs-lookup"><span data-stu-id="30387-1098">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="30387-1099">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="30387-1099">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30387-1100">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30387-1100">Az.Network</span></span>
* <span data-ttu-id="30387-1101">Изменены примеры параметра FilterData Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="30387-1101">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="30387-1102">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="30387-1102">Az.PrivateDns</span></span>
* <span data-ttu-id="30387-1103">Пакет SDK PrivateDns для .NET обновлен до версии 1.0.0</span><span class="sxs-lookup"><span data-stu-id="30387-1103">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="30387-1104">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="30387-1104">Az.RecoveryServices</span></span>
* <span data-ttu-id="30387-1105">Включена поддержка Azure Site Recovery для выбора типа диска при включении защиты.</span><span class="sxs-lookup"><span data-stu-id="30387-1105">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="30387-1106">Внесено исправление Azure Site Recovery для изменения действия плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="30387-1106">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="30387-1107">Включена поддержка восстановления SQL Azure Backup для принятия баз данных файлового потока.</span><span class="sxs-lookup"><span data-stu-id="30387-1107">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="30387-1108">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="30387-1108">Az.RedisCache</span></span>
* <span data-ttu-id="30387-1109">Добавлен параметр MinimumTlsVersion в командлеты New-AzRedisCache и Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="30387-1109">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="30387-1110">Кроме того, добавлен параметр MinimumTlsVersion в выходные данные командлета Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="30387-1110">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="30387-1111">Добавлена проверка параметра -Size для командлетов Set-AzRedisCache и New-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="30387-1111">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="30387-1112">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30387-1112">Az.Resources</span></span>
- <span data-ttu-id="30387-1113">Обновлены командлеты политики для использования новой версии API 2019-06-01 с новым свойством EnforcementMode в назначении политики.</span><span class="sxs-lookup"><span data-stu-id="30387-1113">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="30387-1114">Обновлен пример справки по созданию определения политики</span><span class="sxs-lookup"><span data-stu-id="30387-1114">Updated create policy definition help example</span></span>
- <span data-ttu-id="30387-1115">Исправлена ошибка с параметром -ServicePrincipalName командлета Remove-AZADServicePrincipal с возвратом пустой ссылки, если имя субъекта службы не найдено.</span><span class="sxs-lookup"><span data-stu-id="30387-1115">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="30387-1116">Исправлена ошибка с New-AZADServicePrincipal с возвратом пустой ссылки, если у клиента нет подписки.</span><span class="sxs-lookup"><span data-stu-id="30387-1116">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="30387-1117">Изменен командлет New-AzAdServicePrincipal для добавления учетных данных только для связанного приложения.</span><span class="sxs-lookup"><span data-stu-id="30387-1117">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="30387-1118">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30387-1118">Az.Sql</span></span>
* <span data-ttu-id="30387-1119">Добавлена поддержка ReadReplicaCount для базы данных.</span><span class="sxs-lookup"><span data-stu-id="30387-1119">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="30387-1120">Исправлена ошибка с Set-AzSqlDatabase, если избыточность в пределах зоны не настроена.</span><span class="sxs-lookup"><span data-stu-id="30387-1120">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="30387-1121">Версия 3.0.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="30387-1121">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="30387-1122">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="30387-1122">General</span></span>
* <span data-ttu-id="30387-1123">Выпущена версия Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="30387-1123">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="30387-1124">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30387-1124">Az.Accounts</span></span>
* <span data-ttu-id="30387-1125">Добавлено сообщение об устаревании для псевдонима "Resolve-Error".</span><span class="sxs-lookup"><span data-stu-id="30387-1125">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="30387-1126">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="30387-1126">Az.Advisor</span></span>
* <span data-ttu-id="30387-1127">Добавлена новая категория Operational Excellence (Эффективность работы) в командлет Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="30387-1127">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="30387-1128">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="30387-1128">Az.Batch</span></span>
* <span data-ttu-id="30387-1129">`CoreQuota` в `BatchAccountContext` переименован в `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="30387-1129">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="30387-1130">Также появился новый `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="30387-1130">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="30387-1131">Это влияет на **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="30387-1131">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="30387-1132">Параметр **New-AzBatchTask** `-ResourceFile` теперь принимает коллекцию объектов `PSResourceFile`, которые можно создать с помощью нового командлета **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="30387-1132">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="30387-1133">Новый командлет **New-AzBatchResourceFile**, который помогает создавать объекты `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="30387-1133">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="30387-1134">Их можно передавать в **New-AzBatchTask** в параметре `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="30387-1134">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="30387-1135">Это позволяет поддерживать два новых типа файлов ресурсов, которые дополняют существующий метод `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="30387-1135">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="30387-1136">Файлы ресурсов на основе `AutoStorageContainerName` скачивают весь контейнер автоматического хранения в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="30387-1136">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="30387-1137">Файлы ресурсов на основе `StorageContainerUrl` скачивают указанный в URL-адресе контейнер в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="30387-1137">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="30387-1138">Удалено свойство `ApplicationPackages` в `PSApplication`, который возвращается из **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="30387-1138">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="30387-1139">Отдельные пакеты в приложении теперь можно извлечь с помощью **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="30387-1139">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="30387-1140">Например: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="30387-1140">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="30387-1141">`ApplicationId` переименован в `ApplicationName` для **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** и **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="30387-1141">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="30387-1142">Теперь `ApplicationId` является псевдонимом для `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="30387-1142">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="30387-1143">Добавлено новое свойство `PSWindowsUserConfiguration` в `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="30387-1143">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="30387-1144">`Version` переименован в `Name` для `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="30387-1144">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="30387-1145">`BlobSource` переименован в `HttpUrl` для `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="30387-1145">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="30387-1146">Удалено свойство `OSDisk` из `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="30387-1146">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="30387-1147">Удалена операция **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="30387-1147">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="30387-1148">Больше она не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="30387-1148">This operation is no longer supported.</span></span>
* <span data-ttu-id="30387-1149">Удалено `TargetOSVersion` из `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="30387-1149">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="30387-1150">`CurrentOSVersion` переименован в `OSVersion` для `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="30387-1150">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="30387-1151">Удалено `DataEgressGiB` и `DataIngressGiB` из `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="30387-1151">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="30387-1152">Операция **Get-AzBatchNodeAgentSku** удалена и заменена на **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="30387-1152">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="30387-1153">**Get-AzBatchSupportedImage** возвращает те же данные, что и **Get-AzBatchNodeAgentSku**, но в более удобном формате.</span><span class="sxs-lookup"><span data-stu-id="30387-1153">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="30387-1154">Также возвращаются новые непроверенные образы.</span><span class="sxs-lookup"><span data-stu-id="30387-1154">New non-verified images are also now returned.</span></span> <span data-ttu-id="30387-1155">Включается и дополнительная информация о `Capabilities` и `BatchSupportEndOfLife` для каждого образа.</span><span class="sxs-lookup"><span data-stu-id="30387-1155">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="30387-1156">Добавлена возможность монтировать файловые системы на каждом узле пула с помощью нового параметра `MountConfiguration` в **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="30387-1156">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="30387-1157">Теперь поддерживаются правила безопасности сети, которые блокируют сетевой доступ к пулу по исходящему порту трафика.</span><span class="sxs-lookup"><span data-stu-id="30387-1157">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="30387-1158">Это выполняется с помощью свойства `SourcePortRanges` для `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="30387-1158">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="30387-1159">Что касается выполнения контейнеров, пакетная служба теперь поддерживает выполнение задачи в рабочей папке контейнера или рабочей папке задачи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="30387-1159">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="30387-1160">Выбор зависит от параметра `WorkingDirectory` в `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="30387-1160">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="30387-1161">Добавлена возможность указать коллекцию общедоступных IP-адресов для `PSNetworkConfiguration` с помощью нового свойства `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="30387-1161">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="30387-1162">Это гарантирует, что узлы в пуле будут иметь IP-адреса из списка, предоставленного пользователем.</span><span class="sxs-lookup"><span data-stu-id="30387-1162">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="30387-1163">Если значение не задано, по умолчанию для `WaitForSuccess` в `PSSTartTask` используется значение `$True` (ранее `$False`).</span><span class="sxs-lookup"><span data-stu-id="30387-1163">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="30387-1164">Если значение не задано, по умолчанию для `Scope` в `PSAutoUserSpecification` используется значение `Pool` (ранее `Task` для Windows или `Pool` для Linux).</span><span class="sxs-lookup"><span data-stu-id="30387-1164">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="30387-1165">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="30387-1165">Az.Cdn</span></span>
* <span data-ttu-id="30387-1166">Добавлены UrlRewriteAction и CacheKeyQueryStringAction в RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="30387-1166">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="30387-1167">Исправлено несколько ошибок, таких как отсутствующий входной параметр Selector в командлете New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="30387-1167">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30387-1168">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30387-1168">Az.Compute</span></span>
* <span data-ttu-id="30387-1169">Функция набора шифрования диска</span><span class="sxs-lookup"><span data-stu-id="30387-1169">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="30387-1170">Новые командлеты:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="30387-1170">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="30387-1171">Добавлен параметр ProximityPlacementGroupId в следующие командлеты:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="30387-1171">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="30387-1172">Параметры DiskEncryptionSetId и EncryptionType добавлены в следующие командлеты:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="30387-1172">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="30387-1173">Добавлен параметр PublicIPAddressVersion в New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="30387-1173">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="30387-1174">FileUris для расширения пользовательских скриптов теперь будет защищенным, а не общедоступным параметром</span><span class="sxs-lookup"><span data-stu-id="30387-1174">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="30387-1175">Добавлено ScaleInPolicy в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="30387-1175">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="30387-1176">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="30387-1176">Breaking changes</span></span>
    - <span data-ttu-id="30387-1177">Параметр UploadSizeInBytes применяется теперь вместо DiskSizeGB для New-AzDiskConfig, если CreateOption имеет значение Upload</span><span class="sxs-lookup"><span data-stu-id="30387-1177">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="30387-1178">PublishingProfile.Source.ManagedImage.Id заменяется на StorageProfile.Source.Id в объекте GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="30387-1178">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="30387-1179">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="30387-1179">Az.DataFactory</span></span>
* <span data-ttu-id="30387-1180">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.3.0.</span><span class="sxs-lookup"><span data-stu-id="30387-1180">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="30387-1181">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="30387-1181">Az.DataLakeStore</span></span>
* <span data-ttu-id="30387-1182">Обновлен пакет SDK для ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), включает следующие исправления</span><span class="sxs-lookup"><span data-stu-id="30387-1182">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="30387-1183">Не создается исключение при невозможности десериализовать значение времени создания для записи в корзине или каталоге.</span><span class="sxs-lookup"><span data-stu-id="30387-1183">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="30387-1184">Предоставляется параметр для времени ожидания запроса в adlsclient</span><span class="sxs-lookup"><span data-stu-id="30387-1184">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="30387-1185">Исправлена передача исходного значения syncflag для восстановления badoffset</span><span class="sxs-lookup"><span data-stu-id="30387-1185">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="30387-1186">Исправлена операция EnumerateDirectory, чтобы она извлекала токен продолжения после проверки ответа</span><span class="sxs-lookup"><span data-stu-id="30387-1186">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="30387-1187">Исправлена ошибка объединения</span><span class="sxs-lookup"><span data-stu-id="30387-1187">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="30387-1188">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="30387-1188">Az.FrontDoor</span></span>
* <span data-ttu-id="30387-1189">Исправлены разные опечатки в разных частях модуля</span><span class="sxs-lookup"><span data-stu-id="30387-1189">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="30387-1190">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="30387-1190">Az.HDInsight</span></span>
* <span data-ttu-id="30387-1191">Исправлена ошибка, из-за которой клиент получал сообщение об ошибке 'Not a valid Base-64 string' (Не является допустимой строкой Base64) при выполнении Get-AzHDInsightCluster для получения кластера с хранилищем ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="30387-1191">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="30387-1192">Добавлен параметр с именем ApplicationId в три командлета Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig и New-AzHDInsightCluster, чтобы клиент мог предоставить идентификатор приложения субъекта-службы для доступа к Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="30387-1192">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="30387-1193">Для Microsoft.Azure.Management.HDInsight изменена версия с 2.1.0 на 5.1.0</span><span class="sxs-lookup"><span data-stu-id="30387-1193">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="30387-1194">Удалены пять командлетов:</span><span class="sxs-lookup"><span data-stu-id="30387-1194">Removed five cmdlets:</span></span>
    - <span data-ttu-id="30387-1195">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="30387-1195">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="30387-1196">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="30387-1196">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="30387-1197">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="30387-1197">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="30387-1198">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="30387-1198">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="30387-1199">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="30387-1199">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="30387-1200">Добавлены три командлета:</span><span class="sxs-lookup"><span data-stu-id="30387-1200">Added three cmdlets:</span></span>
    - <span data-ttu-id="30387-1201">Get-AzHDInsightMonitoring заменяет собой Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="30387-1201">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="30387-1202">Enable-AzHDInsightMonitoring заменяет собой Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="30387-1202">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="30387-1203">Disable-AzHDInsightMonitoring заменяет собой Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="30387-1203">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="30387-1204">Исправлен командлет Get-AzHDInsightProperties, чтобы он поддерживал получение сведений о возможностях из определенного расположения.</span><span class="sxs-lookup"><span data-stu-id="30387-1204">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="30387-1205">Удалены наборы параметров ("Spark1", "Spark2") из Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="30387-1205">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="30387-1206">Добавлены примеры в справочные документы по командлету Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="30387-1206">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="30387-1207">Изменен тип выходных данных для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="30387-1207">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="30387-1208">Для Get-AzHDInsightProperties тип выходных данных изменен с CapabilitiesResponse на AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="30387-1208">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="30387-1209">Для Remove-AzHDInsightCluster тип выходных данных изменен с ClusterGetResponse на bool.</span><span class="sxs-lookup"><span data-stu-id="30387-1209">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="30387-1210">Для Set-AzHDInsightGatewaySettings тип выходных данных изменен с HttpConnectivitySettings на GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="30387-1210">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="30387-1211">Добавлены несколько условий для проверки сценариев.</span><span class="sxs-lookup"><span data-stu-id="30387-1211">Added some scenario test cases.</span></span>
* <span data-ttu-id="30387-1212">Удалены несколько псевдонимов: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="30387-1212">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="30387-1213">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="30387-1213">Az.IotHub</span></span>
* <span data-ttu-id="30387-1214">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="30387-1214">Breaking changes:</span></span>
    - <span data-ttu-id="30387-1215">Командлет Add-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="30387-1215">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="30387-1216">Удален набор параметров __AllParameterSets для командлета Add-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="30387-1216">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="30387-1217">Командлет Get-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="30387-1217">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="30387-1218">Удален набор параметров __AllParameterSets для командлета Get-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="30387-1218">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="30387-1219">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties.</span><span class="sxs-lookup"><span data-stu-id="30387-1219">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="30387-1220">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties.</span><span class="sxs-lookup"><span data-stu-id="30387-1220">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="30387-1221">Командлет New-AzIotHubExportDevice больше не поддерживает псевдоним New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="30387-1221">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="30387-1222">Командлет New-AzIotHubImportDevice больше не поддерживает псевдоним New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="30387-1222">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="30387-1223">Командлет Remove-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="30387-1223">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="30387-1224">Удален набор параметров __AllParameterSets для командлета Remove-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="30387-1224">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="30387-1225">Командлет Set-AzIotHub теперь не поддерживает параметр OperationsMonitoringProperties и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="30387-1225">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="30387-1226">Удален набор параметров UpdateOperationsMonitoringProperties для командлета Set-AzIotHub.</span><span class="sxs-lookup"><span data-stu-id="30387-1226">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="30387-1227">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="30387-1227">Az.RecoveryServices</span></span>
* <span data-ttu-id="30387-1228">Azure Site Recovery поддерживает настройку сетевых ресурсов, например групп безопасности сети, общедоступных IP-адресов и внутренних подсистем балансировки нагрузки из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-1228">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="30387-1229">Azure Site Recovery поддерживает запись на управляемый диск из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-1229">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="30387-1230">Azure Site Recovery поддерживает сокращение NIC из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-1230">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="30387-1231">Azure Site Recovery поддерживает ускорение сети NIC из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-1231">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="30387-1232">Azure Site Recovery поддерживает автоматическое обновление агента из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-1232">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="30387-1233">Azure Site Recovery поддерживает стандартный SSD-накопитель из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-1233">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="30387-1234">Azure Site Recovery поддерживает двухпроходное шифрование диска Azure из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-1234">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="30387-1235">Azure Site Recovery поддерживает новый добавленный диск из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-1235">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="30387-1236">Добавлена функция SoftDelete для виртуальных машин и соответствующие тесты</span><span class="sxs-lookup"><span data-stu-id="30387-1236">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="30387-1237">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30387-1237">Az.Resources</span></span>
* <span data-ttu-id="30387-1238">Обновлена сборка зависимостей Microsoft.Extensions.Caching.Memory с версии 1.1.1 до 2.2</span><span class="sxs-lookup"><span data-stu-id="30387-1238">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30387-1239">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30387-1239">Az.Network</span></span>
* <span data-ttu-id="30387-1240">Изменены все командлеты для PrivateEndpointConnection, чтобы они поддерживали универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="30387-1240">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="30387-1241">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="30387-1241">Updated cmdlet:</span></span>
        - <span data-ttu-id="30387-1242">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="30387-1242">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="30387-1243">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="30387-1243">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="30387-1244">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="30387-1244">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="30387-1245">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="30387-1245">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="30387-1246">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="30387-1246">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="30387-1247">Добавлен новый командлет для PrivateLinkResource, который поддерживает универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="30387-1247">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="30387-1248">Новый командлет</span><span class="sxs-lookup"><span data-stu-id="30387-1248">New cmdlet:</span></span>
        - <span data-ttu-id="30387-1249">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="30387-1249">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="30387-1250">Добавлены новые поля и параметр для протокола прокси версии 2.</span><span class="sxs-lookup"><span data-stu-id="30387-1250">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="30387-1251">Добавлено свойство EnableProxyProtocol в PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="30387-1251">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="30387-1252">Добавлено свойство LinkIdentifier в PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="30387-1252">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="30387-1253">Обновлен New-AzPrivateLinkService для поддержки нового необязательного параметра EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="30387-1253">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="30387-1254">Исправлено описание параметра в справочной документации по командлету New-AzApplicationGatewaySku.</span><span class="sxs-lookup"><span data-stu-id="30387-1254">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="30387-1255">Новые командлеты для поддержки политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="30387-1255">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="30387-1256">Добавлена поддержка дочерних ресурсов RouteTables для VirtualHub</span><span class="sxs-lookup"><span data-stu-id="30387-1256">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="30387-1257">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="30387-1257">New cmdlets added:</span></span>
        - <span data-ttu-id="30387-1258">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="30387-1258">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="30387-1259">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="30387-1259">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="30387-1260">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="30387-1260">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="30387-1261">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="30387-1261">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="30387-1262">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="30387-1262">Set-AzVirtualHub</span></span>
* <span data-ttu-id="30387-1263">Добавлена поддержка новых свойств SKU для VirtualHub и VirtualWANType в VirtualWan</span><span class="sxs-lookup"><span data-stu-id="30387-1263">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="30387-1264">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="30387-1264">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="30387-1265">New-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="30387-1265">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="30387-1266">Update-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="30387-1266">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="30387-1267">New-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="30387-1267">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="30387-1268">Update-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="30387-1268">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="30387-1269">Добавлена поддержка свойства EnableInternetSecurity для HubVnetConnection, VpnConnection и ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="30387-1269">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="30387-1270">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="30387-1270">New cmdlets added:</span></span>
        - <span data-ttu-id="30387-1271">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="30387-1271">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="30387-1272">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="30387-1272">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="30387-1273">New-AzureRmVirtualHubVnetConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="30387-1273">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="30387-1274">New-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="30387-1274">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="30387-1275">Update-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="30387-1275">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="30387-1276">New-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="30387-1276">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="30387-1277">Set-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="30387-1277">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="30387-1278">Добавлена поддержка настройки политики верхнего уровня WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="30387-1278">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="30387-1279">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="30387-1279">New cmdlets added:</span></span>
        - <span data-ttu-id="30387-1280">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="30387-1280">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="30387-1281">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="30387-1281">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="30387-1282">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="30387-1282">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="30387-1283">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="30387-1283">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="30387-1284">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="30387-1284">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="30387-1285">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="30387-1285">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="30387-1286">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="30387-1286">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="30387-1287">New-AzApplicationGatewayFirewallPolicy: добавлены параметры PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="30387-1287">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="30387-1288">Добавлена поддержка оператора Geo-Match для CustomRule</span><span class="sxs-lookup"><span data-stu-id="30387-1288">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="30387-1289">Добавлен параметр GeoMatch в оператор для FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="30387-1289">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="30387-1290">Добавлена поддержка политики брандмауэра perListener и perSite</span><span class="sxs-lookup"><span data-stu-id="30387-1290">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="30387-1291">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="30387-1291">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="30387-1292">New-AzApplicationGatewayHttpListener: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="30387-1292">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="30387-1293">New-AzApplicationGatewayPathRuleConfig: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="30387-1293">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="30387-1294">Исправлен учет регистра для требуемой подсети с именем AzureBastionSubnet в PSBastion</span><span class="sxs-lookup"><span data-stu-id="30387-1294">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="30387-1295">Поддержка полного доменного имени назначения в правилах сети и преобразованного полного доменного имени в правилах NAT для брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="30387-1295">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="30387-1296">Добавлена поддержка ресурсов верхнего уровня RouteTables для IpGroup</span><span class="sxs-lookup"><span data-stu-id="30387-1296">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="30387-1297">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="30387-1297">New cmdlets added:</span></span>
        - <span data-ttu-id="30387-1298">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="30387-1298">New-AzIpGroup</span></span>
        - <span data-ttu-id="30387-1299">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="30387-1299">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="30387-1300">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="30387-1300">Get-AzIpGroup</span></span>
        - <span data-ttu-id="30387-1301">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="30387-1301">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="30387-1302">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="30387-1302">Az.ServiceFabric</span></span>
* <span data-ttu-id="30387-1303">Удален командлет Add-AzServiceFabricApplicationCertificate, так как соответствующий сценарий выполняется командлетом Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="30387-1303">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="30387-1304">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30387-1304">Az.Sql</span></span>
* <span data-ttu-id="30387-1305">Добавлена поддержка восстановления удаленных баз данных в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="30387-1305">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="30387-1306">Из кода удалены старые командлеты аудита.</span><span class="sxs-lookup"><span data-stu-id="30387-1306">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="30387-1307">Удалены нерекомендуемые псевдонимы:</span><span class="sxs-lookup"><span data-stu-id="30387-1307">Removed deprecated aliases:</span></span>
* <span data-ttu-id="30387-1308">Get-AzSqlDatabaseIndexRecommendations (вместо него используйте Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="30387-1308">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="30387-1309">Get-AzSqlDatabaseRestorePoints (вместо него используйте Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="30387-1309">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="30387-1310">Удален командлет Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="30387-1310">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="30387-1311">Удалены псевдонимы для нерекомендуемых командлетов параметров оценки уязвимостей</span><span class="sxs-lookup"><span data-stu-id="30387-1311">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="30387-1312">Командлеты расширенного обнаружения угроз объявлены устаревшими</span><span class="sxs-lookup"><span data-stu-id="30387-1312">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="30387-1313">Добавлены командлеты для отключения и включения рекомендаций о конфиденциальности для столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="30387-1313">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="30387-1314">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="30387-1314">Az.Storage</span></span>
* <span data-ttu-id="30387-1315">Поддержка включения большой общей папки при создании или обновлении учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="30387-1315">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="30387-1316">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30387-1316">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="30387-1317">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30387-1317">Set-AzStorageAccount</span></span>
* <span data-ttu-id="30387-1318">При закрытии или получении маркера файла пропускается проверка того, является ли входной путь файлом или каталогом, чтобы избежать сбоев при получении объектов в состоянии DeletePending.</span><span class="sxs-lookup"><span data-stu-id="30387-1318">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="30387-1319">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="30387-1319">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="30387-1320">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="30387-1320">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="30387-1321">2.8.0 — октябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="30387-1321">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="30387-1322">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="30387-1322">General</span></span>
* <span data-ttu-id="30387-1323">Выпуск Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="30387-1323">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="30387-1324">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30387-1324">Az.Accounts</span></span>
* <span data-ttu-id="30387-1325">Обновление телеметрии и перезаписи URL-адресов для созданных модулей, исправление для модульных тестов Windows.</span><span class="sxs-lookup"><span data-stu-id="30387-1325">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="30387-1326">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="30387-1326">Az.ApiManagement</span></span>
* <span data-ttu-id="30387-1327">**Set-AzApiManagementApi** — в ApiVersionSet добавлена поддержка обновления API.</span><span class="sxs-lookup"><span data-stu-id="30387-1327">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="30387-1328">исправлена проблема https://github.com/Azure/azure-powershell/issues/10068.</span><span class="sxs-lookup"><span data-stu-id="30387-1328">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="30387-1329">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="30387-1329">Az.Automation</span></span>
* <span data-ttu-id="30387-1330">Исправлен командлет New-AzureAutomationSoftwareUpdateConfiguration для параметра перезагрузки Linux.</span><span class="sxs-lookup"><span data-stu-id="30387-1330">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="30387-1331">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="30387-1331">Az.Batch</span></span>
* <span data-ttu-id="30387-1332">Командлет **Get-AzBatchNodeAgentSku** объявлен устаревшим и будет заменен на **Get-AzBatchSupportImage** в версии 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="30387-1332">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30387-1333">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30387-1333">Az.Compute</span></span>
* <span data-ttu-id="30387-1334">В командлеты New-AzVM и New-AzVmss добавлены параметры Priority, EvictionPolicy и MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="30387-1334">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="30387-1335">Исправлены предупреждающее сообщение для командлетов Add-AzVMAdditionalUnattendContent и Add-AzVMSshPublicKey и справочная документация по ним.</span><span class="sxs-lookup"><span data-stu-id="30387-1335">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="30387-1336">Для Set-AzVMDiskEncryptionExtension исправлено исключение -skipVmBackup для виртуальных машин Linux с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="30387-1336">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="30387-1337">Исправлена ошибка при изменении параметров шифрования в Set-AzVMDiskEncryptionExtension, реализован двухэтапный сценарий.</span><span class="sxs-lookup"><span data-stu-id="30387-1337">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="30387-1338">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="30387-1338">Az.DataFactory</span></span>
* <span data-ttu-id="30387-1339">Добавлены команды CRUD для потока данных Фабрики данных Azure версии 2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow и Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="30387-1339">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="30387-1340">Добавлены команды действий для сеанса отладки потока данных Фабрики данных Azure версии 2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand и Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="30387-1340">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="30387-1341">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.2.0.</span><span class="sxs-lookup"><span data-stu-id="30387-1341">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="30387-1342">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="30387-1342">Az.DataLakeStore</span></span>
* <span data-ttu-id="30387-1343">Проверка учетной записи исправлена так, чтобы учетные записи, содержащие знак "-", можно было передавать без домена.</span><span class="sxs-lookup"><span data-stu-id="30387-1343">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="30387-1344">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="30387-1344">Az.HealthcareApis</span></span>
* <span data-ttu-id="30387-1345">Версия PowerShell обновлена до 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="30387-1345">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="30387-1346">Версия пакета SDK обновлена до 1.0.2.</span><span class="sxs-lookup"><span data-stu-id="30387-1346">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="30387-1347">В тестах обновлены ссылки на новую версию пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="30387-1347">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="30387-1348">Вложенная выходная структура заменена на плоскую.</span><span class="sxs-lookup"><span data-stu-id="30387-1348">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="30387-1349">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="30387-1349">Az.IotHub</span></span>
* <span data-ttu-id="30387-1350">Добавлен новый источник маршрутизации DigitalTwinChangeEvents.</span><span class="sxs-lookup"><span data-stu-id="30387-1350">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="30387-1351">Исправлены незначительные ошибки: Get-AzIothub не возвращает subscriptionId.</span><span class="sxs-lookup"><span data-stu-id="30387-1351">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="30387-1352">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="30387-1352">Az.Monitor</span></span>
* <span data-ttu-id="30387-1353">Добавлены новые получатели групп действий: -ItsmReceiver, -VoiceReceiver, -ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver.</span><span class="sxs-lookup"><span data-stu-id="30387-1353">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="30387-1354">Для получателей включите общую схему оповещений.</span><span class="sxs-lookup"><span data-stu-id="30387-1354">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="30387-1355">Это не касается получателей SMS, push-уведомлений приложения Azure, ITSM и голосовых сообщений.</span><span class="sxs-lookup"><span data-stu-id="30387-1355">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="30387-1356">Веб-перехватчики теперь поддерживают аутентификацию Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="30387-1356">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30387-1357">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30387-1357">Az.Network</span></span>
* <span data-ttu-id="30387-1358">Добавлен новый командлет Get-AzAvailableServiceAlias, позволяющий получить псевдонимы для политик конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="30387-1358">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="30387-1359">В подключениях шлюза виртуальной сети появилась возможность добавлять селекторы трафика.</span><span class="sxs-lookup"><span data-stu-id="30387-1359">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="30387-1360">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="30387-1360">New cmdlets added:</span></span>
        - <span data-ttu-id="30387-1361">New-AzureRmTrafficSelectorPolicy.</span><span class="sxs-lookup"><span data-stu-id="30387-1361">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="30387-1362">В командлеты добавлены необязательные параметры -TrafficSelectorPolicies, -New-AzureRmVirtualNetworkGatewayConnection, -Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="30387-1362">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="30387-1363">В конфигурациях правил сетевой безопасности добавлена поддержка протоколов ESP и AH.</span><span class="sxs-lookup"><span data-stu-id="30387-1363">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="30387-1364">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="30387-1364">Updated cmdlets:</span></span>
        - <span data-ttu-id="30387-1365">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="30387-1365">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="30387-1366">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="30387-1366">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="30387-1367">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="30387-1367">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="30387-1368">Улучшена обработка исключений в командлетах Cortex.</span><span class="sxs-lookup"><span data-stu-id="30387-1368">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="30387-1369">Выпущены новые поколения и номера SKU VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="30387-1369">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="30387-1370">Представлены новые поколения VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="30387-1370">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="30387-1371">Представлены новые номера SKU VirtualNetworkGateways с высокой пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="30387-1371">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="30387-1372">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="30387-1372">Az.RedisCache</span></span>
* <span data-ttu-id="30387-1373">В справочную документацию по Set-AzRedisCache добавлены недостающие значения для параметра -Size.</span><span class="sxs-lookup"><span data-stu-id="30387-1373">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="30387-1374">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30387-1374">Az.Sql</span></span>
* <span data-ttu-id="30387-1375">Добавлена возможность назначать администратора Active Directory в Управляемом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="30387-1375">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="30387-1376">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="30387-1376">Az.Storage</span></span>
* <span data-ttu-id="30387-1377">Клиентская библиотека службы хранилища Azure обновлена до версии 11.1.0.</span><span class="sxs-lookup"><span data-stu-id="30387-1377">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="30387-1378">NextPageLink теперь позволяет получить список контейнеров с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="30387-1378">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="30387-1379">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="30387-1379">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="30387-1380">NextPageLink теперь позволяет получить список учетных записей хранения из подписки.</span><span class="sxs-lookup"><span data-stu-id="30387-1380">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="30387-1381">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30387-1381">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="30387-1382">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="30387-1382">Az.StorageSync</span></span>
* <span data-ttu-id="30387-1383">Исправлена проблема 9810 с Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="30387-1383">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="30387-1384">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="30387-1384">Az.Websites</span></span>
* <span data-ttu-id="30387-1385">Обновление плана службы приложений с помощью Set-AzWebApp приводило к сбою приложения.</span><span class="sxs-lookup"><span data-stu-id="30387-1385">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="30387-1386">2.7.0 — сентябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="30387-1386">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="30387-1387">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="30387-1387">Az.ApiManagement</span></span>
* <span data-ttu-id="30387-1388">В справочной документации по командлету Set-AzApiManagementPolicy обновлено описание параметра -Format.</span><span class="sxs-lookup"><span data-stu-id="30387-1388">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="30387-1389">Из справочной документации удалены ссылки на нерекомендуемый командлет Update-AzApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="30387-1389">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="30387-1390">Вместо него следует использовать командлет Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="30387-1390">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="30387-1391">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="30387-1391">Az.Automation</span></span>
* <span data-ttu-id="30387-1392">В справочной документации по командлету Register-AzAutomationDscNode исправлена опечатка в примере.</span><span class="sxs-lookup"><span data-stu-id="30387-1392">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="30387-1393">Добавлено уточнение об ограничениях ОС для командлета Register-AzAutomationDSCNode.</span><span class="sxs-lookup"><span data-stu-id="30387-1393">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="30387-1394">Исправлено исключение пустой ссылки для параметра -Wait в командлете Start-AzAutomationRunbook.</span><span class="sxs-lookup"><span data-stu-id="30387-1394">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30387-1395">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30387-1395">Az.Compute</span></span>
* <span data-ttu-id="30387-1396">Добавлен параметр UploadSizeInBytes для командлета New-AzDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="30387-1396">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="30387-1397">Добавлен добавочный параметр для командлета New-AzSnapshotConfig.</span><span class="sxs-lookup"><span data-stu-id="30387-1397">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="30387-1398">Для виртуальной машины добавлены такие функции с низким приоритетом:</span><span class="sxs-lookup"><span data-stu-id="30387-1398">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="30387-1399">Для командлета New-AzVMConfig добавлены параметры MaxPrice, EvictionPolicy и Priority.</span><span class="sxs-lookup"><span data-stu-id="30387-1399">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="30387-1400">Для командлетов New-AzVmssConfig, Update-AzVM и Update-AzVmss добавлен параметр MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="30387-1400">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="30387-1401">Для командлета Get-AzAvailabilitySet устранена проблема со ссылкой на виртуальную машину, когда в нем перечисляются все группы доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="30387-1401">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="30387-1402">Исправлено исключение NULL для командлета Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="30387-1402">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="30387-1403">Исправлен метод поиска VHD для относительной конечной позиции.</span><span class="sxs-lookup"><span data-stu-id="30387-1403">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="30387-1404">Устранена проблема с UltraSSD для командлетов New-AzVM и Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="30387-1404">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="30387-1405">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="30387-1405">Az.DataFactory</span></span>
* <span data-ttu-id="30387-1406">Добавлены 3 новые команды для ADF версии 2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription и Get-AzDataFactoryV2TriggerSubscriptionStatus.</span><span class="sxs-lookup"><span data-stu-id="30387-1406">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="30387-1407">Пакет SDK ADF для .NET обновлен до версии 4.1.3.</span><span class="sxs-lookup"><span data-stu-id="30387-1407">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="30387-1408">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="30387-1408">Az.HDInsight</span></span>
* <span data-ttu-id="30387-1409">Укажите критические изменения.</span><span class="sxs-lookup"><span data-stu-id="30387-1409">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="30387-1410">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="30387-1410">Az.IotHub</span></span>
* <span data-ttu-id="30387-1411">Добавлена поддержка для вызова отработки отказа для IotHub в георегион аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="30387-1411">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="30387-1412">Добавлена поддержка для управления обогащением сообщений для IotHub.</span><span class="sxs-lookup"><span data-stu-id="30387-1412">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="30387-1413">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="30387-1413">New cmdlets are:</span></span>
    - <span data-ttu-id="30387-1414">Add-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="30387-1414">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="30387-1415">Get-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="30387-1415">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="30387-1416">Remove-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="30387-1416">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="30387-1417">Set-AzIotHubMessageEnrichment.</span><span class="sxs-lookup"><span data-stu-id="30387-1417">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="30387-1418">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="30387-1418">Az.Monitor</span></span>
* <span data-ttu-id="30387-1419">Указание на самую последнюю версию пакета SDK для монитора, т. е. 0.24.1-preview:</span><span class="sxs-lookup"><span data-stu-id="30387-1419">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="30387-1420">В командлеты метрик добавлены некритические изменения, т. е. перечисление единиц поддерживает несколько новых значений.</span><span class="sxs-lookup"><span data-stu-id="30387-1420">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="30387-1421">Эти командлеты доступны только для чтения, поэтому входные данные командлетов не будут изменены.</span><span class="sxs-lookup"><span data-stu-id="30387-1421">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="30387-1422">Актуальная версия API запросов **ActionGroups** — **2019-06-01**. До этого была версия **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="30387-1422">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="30387-1423">Тесты сценария обновлены в соответствии с этим изменением.</span><span class="sxs-lookup"><span data-stu-id="30387-1423">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="30387-1424">В конструкторы классов **EmailReceiver** и **WebhookReceiver** добавлен один новый обязательный аргумент — логическое значение с именем **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="30387-1424">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="30387-1425">Сейчас для него установлено значение **false**, чтобы скрыть это критическое изменение от командлетов.</span><span class="sxs-lookup"><span data-stu-id="30387-1425">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="30387-1426">**Примечание**. Это временное изменение, которое должно быть подтверждено командой оповещения.</span><span class="sxs-lookup"><span data-stu-id="30387-1426">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="30387-1427">Порядок аргументов для конструктора класса **Source** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="30387-1427">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="30387-1428">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="30387-1428">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="30387-1429">Порядок аргументов для конструктора класса **AlertingAction** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="30387-1429">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="30387-1430">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="30387-1430">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="30387-1431">Добавлена поддержка критериев динамического порога для оповещения метрики версии 2:</span><span class="sxs-lookup"><span data-stu-id="30387-1431">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="30387-1432">New-AzMetricAlertRuleV2Criteria: теперь также позволяет создавать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="30387-1432">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="30387-1433">Add-AzMetricAlertRuleV2: теперь также позволяет принимать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="30387-1433">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="30387-1434">Добавлены усовершенствования в командлетах запланированных правил запросов (SQR).</span><span class="sxs-lookup"><span data-stu-id="30387-1434">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="30387-1435">Командлеты будут принимать параметр Location в обоих форматах: расположение (например, eastus) или отображаемое имя расположения (например, "восточная часть США").</span><span class="sxs-lookup"><span data-stu-id="30387-1435">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="30387-1436">Параметр Enabled проиллюстрирован в файлах справки надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="30387-1436">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="30387-1437">Добавлены примеры для необязательного параметра ActionGroup.</span><span class="sxs-lookup"><span data-stu-id="30387-1437">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="30387-1438">Все файлы справки улучшены.</span><span class="sxs-lookup"><span data-stu-id="30387-1438">Overall improved help files</span></span>
* <span data-ttu-id="30387-1439">Исправлена ошибка в определении типа области для командлета Set-AzActionRule.</span><span class="sxs-lookup"><span data-stu-id="30387-1439">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30387-1440">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30387-1440">Az.Network</span></span>
* <span data-ttu-id="30387-1441">Исправлен неправильный пример в справочной документации по командлету New-AzApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="30387-1441">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="30387-1442">В справочную документацию по командлету Get-AzNetworkWatcherPacketCapture добавлено примечание, посвященное извлечению всех свойств для записи пакетов.</span><span class="sxs-lookup"><span data-stu-id="30387-1442">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="30387-1443">В справочной документации по командлету Test-AzNetworkWatcherIPFlow исправлен пример: теперь он правильно перечисляет сетевые карты.</span><span class="sxs-lookup"><span data-stu-id="30387-1443">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="30387-1444">Улучшен анализ облачных исключений для отображения дополнительных сведений (при их наличии).</span><span class="sxs-lookup"><span data-stu-id="30387-1444">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="30387-1445">Улучшен анализ облачных исключений для обработки дополнительного типа исключения SDK.</span><span class="sxs-lookup"><span data-stu-id="30387-1445">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="30387-1446">Исправлено неправильное сопоставление моделей правил безопасности.</span><span class="sxs-lookup"><span data-stu-id="30387-1446">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="30387-1447">Добавлены свойства сетевого интерфейса для компонента частного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="30387-1447">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="30387-1448">Для интерфейса PSNetworkInterface добавлено свойство PrivateEndpoint с типом PSResourceId.</span><span class="sxs-lookup"><span data-stu-id="30387-1448">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="30387-1449">В PSNetworkInterfaceIPConfiguration добавлено свойство PrivateLinkConnectionProperties с типом PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="30387-1449">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="30387-1450">Добавлен новый класс модели: PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="30387-1450">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="30387-1451">Добавлен новый тип ApplicationRuleProtocolType "mssql" для ресурса Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-1451">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="30387-1452">Поддержка многоканального подключения в Виртуальной глобальной сети:</span><span class="sxs-lookup"><span data-stu-id="30387-1452">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="30387-1453">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="30387-1453">New cmdlets</span></span>
        - <span data-ttu-id="30387-1454">New-AzVpnSiteLink;</span><span class="sxs-lookup"><span data-stu-id="30387-1454">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="30387-1455">New-AzVpnSiteLinkConnection;</span><span class="sxs-lookup"><span data-stu-id="30387-1455">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="30387-1456">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="30387-1456">Updated cmdlet:</span></span>
        - <span data-ttu-id="30387-1457">New-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="30387-1457">New-VpnSite</span></span>
        - <span data-ttu-id="30387-1458">Update-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="30387-1458">Update-VpnSite</span></span>
        - <span data-ttu-id="30387-1459">New-VpnConnection;</span><span class="sxs-lookup"><span data-stu-id="30387-1459">New-VpnConnection</span></span>
        - <span data-ttu-id="30387-1460">Update-VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="30387-1460">Update-VpnConnection</span></span>
* <span data-ttu-id="30387-1461">Исправлены документы с некоторыми примерами PowerShell для использования командлетов AZ вместо командлетов AzureRM.</span><span class="sxs-lookup"><span data-stu-id="30387-1461">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="30387-1462">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="30387-1462">Az.RecoveryServices</span></span>
* <span data-ttu-id="30387-1463">Для объекта AzureVMpolicy добавлен новый атрибут — ProtectedItemsCount.</span><span class="sxs-lookup"><span data-stu-id="30387-1463">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="30387-1464">Добавлены тесты для политики виртуальной машины и восстановления исходной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="30387-1464">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="30387-1465">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30387-1465">Az.Resources</span></span>
* <span data-ttu-id="30387-1466">Исправлена ошибка, при которой не удавалось вызвать командлет New-AzRoleAssignment без параметра Scope.</span><span class="sxs-lookup"><span data-stu-id="30387-1466">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="30387-1467">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="30387-1467">Az.ServiceFabric</span></span>
* <span data-ttu-id="30387-1468">Исправлена опечатка в примере в справочной документации по командлету Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="30387-1468">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="30387-1469">Добавлены новые командлеты для управления приложениями и службами:</span><span class="sxs-lookup"><span data-stu-id="30387-1469">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="30387-1470">New-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="30387-1470">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="30387-1471">New-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="30387-1471">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="30387-1472">New-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="30387-1472">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="30387-1473">New-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="30387-1473">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="30387-1474">Update-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="30387-1474">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="30387-1475">Get-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="30387-1475">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="30387-1476">Get-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="30387-1476">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="30387-1477">Get-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="30387-1477">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="30387-1478">Get-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="30387-1478">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="30387-1479">Remove-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="30387-1479">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="30387-1480">Remove-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="30387-1480">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="30387-1481">Remove-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="30387-1481">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="30387-1482">Remove-AzServiceFabricServic.</span><span class="sxs-lookup"><span data-stu-id="30387-1482">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="30387-1483">Пакет SDK для Service Fabric обновлен до версии 1.2.0, в которой используется версия API 2019-03-01 поставщика ресурсов Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="30387-1483">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="30387-1484">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="30387-1484">Az.SignalR</span></span>
* <span data-ttu-id="30387-1485">Добавлены командлеты Update, Restart, CheckNameAvailability и GetUsage.</span><span class="sxs-lookup"><span data-stu-id="30387-1485">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="30387-1486">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30387-1486">Az.Sql</span></span>
* <span data-ttu-id="30387-1487">Обновлен пример в справочной документации по командлету Get-AzSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="30387-1487">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="30387-1488">Добавлен пример виртуального ядра для командлета создания эластичного пула (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="30387-1488">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="30387-1489">Удалена проверка свойства EmailAddresses и того, что свойство EmailAdmins правильное в случае, если свойство EmailAddresses пустое в командлетах Set-AzSqlServerAdvancedThreatProtectionPolicy и Set-AzSqlDatabaseAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="30387-1489">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="30387-1490">Теперь, если существует несколько параметров диагностики, включающих категорию аудита, параметры аудита сервера и базы данных удаляются.</span><span class="sxs-lookup"><span data-stu-id="30387-1490">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="30387-1491">Исправлена проверка адресов электронной почты в нескольких командлетах оценки уязвимостей SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting и Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="30387-1491">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="30387-1492">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="30387-1492">Az.Storage</span></span>
* <span data-ttu-id="30387-1493">Обновлен пример в справочной документации по командлету Get-AzStorageAccountKey.</span><span class="sxs-lookup"><span data-stu-id="30387-1493">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="30387-1494">Теперь при отправке и загрузке файла Azure в конечном файле сохраняются свойства SMB исходного файла (атрибуты файла, время создания файла, время последней записи файла).</span><span class="sxs-lookup"><span data-stu-id="30387-1494">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="30387-1495">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="30387-1495">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="30387-1496">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="30387-1496">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="30387-1497">Исправлена операция отправки блочного BLOB-объекта, в которой происходили сбои свойств и метаданных в контейнере с включенной ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="30387-1497">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="30387-1498">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="30387-1498">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="30387-1499">Добавлена поддержка управления общими папками Azure в API плоскости управления с помощью таких командлетов:</span><span class="sxs-lookup"><span data-stu-id="30387-1499">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="30387-1500">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="30387-1500">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="30387-1501">Get-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="30387-1501">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="30387-1502">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="30387-1502">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="30387-1503">Remove-AzRmStorageShare.</span><span class="sxs-lookup"><span data-stu-id="30387-1503">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="30387-1504">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="30387-1504">Az.Websites</span></span>
* <span data-ttu-id="30387-1505">Устранена проблема, из-за которой теги webapp удалялись при переносе приложения в новый ASP.</span><span class="sxs-lookup"><span data-stu-id="30387-1505">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="30387-1506">Теперь командлет Publish-AzureWebapp работает в Linux и Windows.</span><span class="sxs-lookup"><span data-stu-id="30387-1506">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="30387-1507">Обновлен пример в справочной документации по командлету Get-AzWebAppPublishingProfile.</span><span class="sxs-lookup"><span data-stu-id="30387-1507">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="30387-1508">2.6.0 — август 2019 г.</span><span class="sxs-lookup"><span data-stu-id="30387-1508">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="30387-1509">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="30387-1509">General</span></span>
* <span data-ttu-id="30387-1510">Исправлены опечатки в модулях.</span><span class="sxs-lookup"><span data-stu-id="30387-1510">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="30387-1511">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30387-1511">Az.Accounts</span></span>
* <span data-ttu-id="30387-1512">Добавлена поддержка назначаемого пользователем удостоверения MSI при проверке подлинности в Функциях Azure (№ 9479).</span><span class="sxs-lookup"><span data-stu-id="30387-1512">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="30387-1513">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="30387-1513">Az.Aks</span></span>
* <span data-ttu-id="30387-1514">Устранена проблема с выходными данными для Get-AzAks.</span><span class="sxs-lookup"><span data-stu-id="30387-1514">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="30387-1515">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9847.</span><span class="sxs-lookup"><span data-stu-id="30387-1515">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="30387-1516">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="30387-1516">Az.ApiManagement</span></span>
* <span data-ttu-id="30387-1517">исправлена проблема https://github.com/Azure/azure-powershell/issues/9351.</span><span class="sxs-lookup"><span data-stu-id="30387-1517">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="30387-1518">Обновлена версия NuGet для .NET, которая не накладывает ограничений на productId, apiId, groupId и userId.</span><span class="sxs-lookup"><span data-stu-id="30387-1518">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="30387-1519">**Get-AzApiManagementProduct**. Добавлена поддержка запросов к продуктам с помощью API.</span><span class="sxs-lookup"><span data-stu-id="30387-1519">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="30387-1520">**New-AzApiManagementApiRevision**. Устранена проблема, из-за которой не задавался параметр ApiRevisionDescription при создании новой редакции API https://github.com/Azure/azure-powershell/issues/9752.</span><span class="sxs-lookup"><span data-stu-id="30387-1520">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="30387-1521">Исправлено написание имени модели c PsApiManagementOAuth2AuthrozationServer на PsApiManagementOAuth2AuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="30387-1521">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="30387-1522">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="30387-1522">Az.Batch</span></span>
* <span data-ttu-id="30387-1523">Исправлена опечатка в написании Windows со строчной буквы в справочных сообщениях и документации.</span><span class="sxs-lookup"><span data-stu-id="30387-1523">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="30387-1524">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="30387-1524">Az.Cdn</span></span>
* <span data-ttu-id="30387-1525">Исправлена опечатка во вспомогательном приложении модуля CDN.</span><span class="sxs-lookup"><span data-stu-id="30387-1525">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30387-1526">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30387-1526">Az.Compute</span></span>
* <span data-ttu-id="30387-1527">Добавлен параметр VmssId в новый командлет Add New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="30387-1527">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="30387-1528">Добавлены параметры TerminateScheduledEvents и TerminateScheduledEventNotBeforeTimeoutInMinutes в New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="30387-1528">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="30387-1529">Добавлено свойство HyperVGeneration в объект образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="30387-1529">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="30387-1530">Добавлены компоненты Host и HostGroup.</span><span class="sxs-lookup"><span data-stu-id="30387-1530">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="30387-1531">Новые командлеты:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="30387-1531">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="30387-1532">Параметр HostId добавлен в New-AzVMConfig и New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="30387-1532">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="30387-1533">Исправлен пример в документации по Invoke-AzVMRunCommand, в котором теперь используется правильное имя параметра.</span><span class="sxs-lookup"><span data-stu-id="30387-1533">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="30387-1534">Исправлено описание VolumeType в справочной документации по Set-AzVMDiskEncryptionExtension и Set-AzVmssDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="30387-1534">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="30387-1535">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="30387-1535">Az.DataFactory</span></span>
* <span data-ttu-id="30387-1536">Исправлена опечатка в написании Windows со строчной буквы в документации по New-AzDataFactoryEncryptValue.</span><span class="sxs-lookup"><span data-stu-id="30387-1536">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="30387-1537">Пакет SDK ADF для .NET обновлен до версии 4.1.2.</span><span class="sxs-lookup"><span data-stu-id="30387-1537">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="30387-1538">Добавлены параметры DataProxyIntegrationRuntimeName, DataProxyStagingLinkedServiceName и DataProxyStagingPath в командлет Set-AzureRmDataFactoryV2IntegrationRuntime, что позволяет настраивать локальную среду выполнения интеграции в качестве прокси-сервера для Azure-SSIS Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="30387-1538">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="30387-1539">Обновлены PSTriggerRun для отображения активированных конвейеров, сообщений и свойств и PSActivityRun для отображения типа действия.</span><span class="sxs-lookup"><span data-stu-id="30387-1539">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="30387-1540">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="30387-1540">Az.DataLakeStore</span></span>
* <span data-ttu-id="30387-1541">Устранена проблема, при которой Get-DataLakeStoreDeletedItem переставал отвечать на запросы при возникновении ошибок или удаленных исключений.</span><span class="sxs-lookup"><span data-stu-id="30387-1541">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="30387-1542">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="30387-1542">Az.EventHub</span></span>
* <span data-ttu-id="30387-1543">Исправлена проблема № 9658: опечатка в написании параметра VirtualNteworkRule у Set-AzEventHubNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="30387-1543">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="30387-1544">Исправлена проблема № 9558: в Set-AzEventHubNamespace используется PATCH вместо PUT.</span><span class="sxs-lookup"><span data-stu-id="30387-1544">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="30387-1545">В командлет Set-AzEventHubNamespace добавлен параметр EnableKafka.</span><span class="sxs-lookup"><span data-stu-id="30387-1545">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="30387-1546">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="30387-1546">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="30387-1547">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="30387-1547">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="30387-1548">Исправлено написание Azure со строчной буквы.</span><span class="sxs-lookup"><span data-stu-id="30387-1548">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="30387-1549">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="30387-1549">Az.Monitor</span></span>
* <span data-ttu-id="30387-1550">Исправлены неправильные имена параметров в справочной документации.</span><span class="sxs-lookup"><span data-stu-id="30387-1550">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30387-1551">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30387-1551">Az.Network</span></span>
* <span data-ttu-id="30387-1552">Обновлен New-AzPrivateLinkServiceIpConfig.</span><span class="sxs-lookup"><span data-stu-id="30387-1552">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="30387-1553">Параметр PublicIpAddress объявлен нерекомендуемым, так как он не используется на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="30387-1553">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="30387-1554">Добавлен необязательный параметр Primary, указывающий, является ли текущая IP-конфигурация основной.</span><span class="sxs-lookup"><span data-stu-id="30387-1554">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="30387-1555">Улучшена обработка исключений из-за ошибок запроса от пакета SDK. Устранена проблема, при которой исключения пакета SDK не обрабатывались правильно, из-за чего не отображались основные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="30387-1555">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="30387-1556">Настроена логика проверки для префикса IPv6 IP-адреса для проверки правильности длины префикса IPv6.</span><span class="sxs-lookup"><span data-stu-id="30387-1556">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="30387-1557">Обновлен Get-AzVirtualNetworkSubnetConfig: добавлен набор параметров для получения по идентификатору ресурса подсети.</span><span class="sxs-lookup"><span data-stu-id="30387-1557">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="30387-1558">Обновлено описание параметра Location для AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="30387-1558">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="30387-1559">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="30387-1559">Az.OperationalInsights</span></span>
* <span data-ttu-id="30387-1560">Обновлена документация по New-AzOperationalInsightsLinuxSyslogDataSource.</span><span class="sxs-lookup"><span data-stu-id="30387-1560">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="30387-1561">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="30387-1561">Added example</span></span>
    - <span data-ttu-id="30387-1562">Обновлено описание параметра -Name.</span><span class="sxs-lookup"><span data-stu-id="30387-1562">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="30387-1563">Добавлен пример для New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="30387-1563">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="30387-1564">Изменено описание параметра -Name для New-AzOperationalInsightsWindowsEventDataSource.</span><span class="sxs-lookup"><span data-stu-id="30387-1564">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="30387-1565">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="30387-1565">Az.RecoveryServices</span></span>
* <span data-ttu-id="30387-1566">Обновлен Get-AzRecoveryServicesBackupJobDetail.md.</span><span class="sxs-lookup"><span data-stu-id="30387-1566">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="30387-1567">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30387-1567">Az.Resources</span></span>
* <span data-ttu-id="30387-1568">Добавлена поддержка новой версии API 2019-05-10 для Microsoft.Resource.</span><span class="sxs-lookup"><span data-stu-id="30387-1568">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="30387-1569">Добавлена поддержка copy.count = 0 для переменных, ресурсов и свойств.</span><span class="sxs-lookup"><span data-stu-id="30387-1569">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="30387-1570">Ресурсы, у которых condition = false или copy.count = 0, будут удаляться в полном режиме.</span><span class="sxs-lookup"><span data-stu-id="30387-1570">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="30387-1571">В справочную документацию добавлен пример назначения политики на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="30387-1571">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="30387-1572">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="30387-1572">Az.ServiceBus</span></span>
* <span data-ttu-id="30387-1573">Исправлена проблема № 9658: опечатка в написании параметра VirtualNetworkRule В Set-AzServiceBusNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="30387-1573">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="30387-1574">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="30387-1574">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="30387-1575">Добавлена новая команда Test-AzServiceBusNameAvailability для проверки доступности имени для очереди и раздела.</span><span class="sxs-lookup"><span data-stu-id="30387-1575">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="30387-1576">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="30387-1576">Az.ServiceFabric</span></span>
* <span data-ttu-id="30387-1577">Устранены ошибки командлета для добавления типа узла:</span><span class="sxs-lookup"><span data-stu-id="30387-1577">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="30387-1578">ошибка NullReferenceException, возникавшая, если у группы ресурсов были другие VMSS, не связанные с кластером Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="30387-1578">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="30387-1579">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8681.</span><span class="sxs-lookup"><span data-stu-id="30387-1579">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="30387-1580">Исправлена ошибка, из-за которой командлет завершился сбоем, если virtualNetwork находилась не в той группе ресурсов, к которой относится кластер.</span><span class="sxs-lookup"><span data-stu-id="30387-1580">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="30387-1581">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8407.</span><span class="sxs-lookup"><span data-stu-id="30387-1581">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="30387-1582">Командлет Add-AzServiceFabricApplicationCertificate объявлен нерекомендуемым.</span><span class="sxs-lookup"><span data-stu-id="30387-1582">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="30387-1583">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30387-1583">Az.Sql</span></span>
* <span data-ttu-id="30387-1584">Обновление документации по старым командлетам аудита.</span><span class="sxs-lookup"><span data-stu-id="30387-1584">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="30387-1585">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="30387-1585">Az.Storage</span></span>
* <span data-ttu-id="30387-1586">Обновлена справка по Get/Close-AzStorageFileHandle: в примеры добавлены сценарии использования командлетов и обновлено описание параметров.</span><span class="sxs-lookup"><span data-stu-id="30387-1586">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="30387-1587">Добавлена поддержка StandardBlobTier в операции отправки BLOB-объекта и копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="30387-1587">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="30387-1588">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="30387-1588">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="30387-1589">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="30387-1589">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="30387-1590">Добавлена поддержка приоритета восстановления в операцию копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="30387-1590">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="30387-1591">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="30387-1591">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="30387-1592">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="30387-1592">Az.Websites</span></span>
* <span data-ttu-id="30387-1593">Добавлены уточнение для параметра -AppSettings в Set-AzWebApp и Set-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="30387-1593">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="30387-1594">2.5.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="30387-1594">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="30387-1595">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30387-1595">Az.Accounts</span></span>
* <span data-ttu-id="30387-1596">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="30387-1596">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="30387-1597">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="30387-1597">Az.ApplicationInsights</span></span>
* <span data-ttu-id="30387-1598">Исправлена опечатка в примере в документации по Remove-AzApplicationInsightsApiKey.</span><span class="sxs-lookup"><span data-stu-id="30387-1598">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="30387-1599">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="30387-1599">Az.Automation</span></span>
* <span data-ttu-id="30387-1600">Исправлена опечатка в строке ресурса.</span><span class="sxs-lookup"><span data-stu-id="30387-1600">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="30387-1601">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="30387-1601">Az.CognitiveServices</span></span>
* <span data-ttu-id="30387-1602">Добавлена поддержка NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="30387-1602">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30387-1603">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30387-1603">Az.Compute</span></span>
* <span data-ttu-id="30387-1604">Добавлены недостающие свойства (ComputerName, OsName, OsVersion и HyperVGeneration) для объекта представления экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="30387-1604">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="30387-1605">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="30387-1605">Az.ContainerRegistry</span></span>
* <span data-ttu-id="30387-1606">Исправлена опечатка в Remove-AzContainerRegistryReplication для параметра репликации.</span><span class="sxs-lookup"><span data-stu-id="30387-1606">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="30387-1607">См. подробнее: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="30387-1607">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="30387-1608">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="30387-1608">Az.DataFactory</span></span>
* <span data-ttu-id="30387-1609">Пакет SDK для ADF .NET обновлен до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="30387-1609">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="30387-1610">Исправлена опечатка в документации по Get-AzDataFactoryV2PipelineRun.</span><span class="sxs-lookup"><span data-stu-id="30387-1610">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="30387-1611">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="30387-1611">Az.EventHub</span></span>
* <span data-ttu-id="30387-1612">Добавлен новый командлет для создания маркера SAS: New-AzEventHubAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="30387-1612">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="30387-1613">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="30387-1613">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="30387-1614">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="30387-1614">Az.KeyVault</span></span>
* <span data-ttu-id="30387-1615">Добавлена поддержка для настройки параметра KeySize в политиках сертификатов.</span><span class="sxs-lookup"><span data-stu-id="30387-1615">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="30387-1616">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="30387-1616">Az.LogicApp</span></span>
* <span data-ttu-id="30387-1617">Get-AzIntegrationAccountMap теперь надлежащим образом выводит все типы сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="30387-1617">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="30387-1618">Добавлен новый параметр MapType для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="30387-1618">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="30387-1619">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="30387-1619">Az.ManagedServices</span></span>
* <span data-ttu-id="30387-1620">Добавлена поддержка API версии 2019-06-01 (общедоступная).</span><span class="sxs-lookup"><span data-stu-id="30387-1620">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30387-1621">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30387-1621">Az.Network</span></span>
* <span data-ttu-id="30387-1622">Добавлена поддержка частной конечной точки и службы приватного канала.</span><span class="sxs-lookup"><span data-stu-id="30387-1622">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="30387-1623">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="30387-1623">New cmdlets</span></span>
        - <span data-ttu-id="30387-1624">Set-AzPrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="30387-1624">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="30387-1625">Set-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="30387-1625">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="30387-1626">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="30387-1626">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="30387-1627">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="30387-1627">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="30387-1628">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="30387-1628">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="30387-1629">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="30387-1629">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="30387-1630">Test-AzPrivateLinkServiceVisibility.</span><span class="sxs-lookup"><span data-stu-id="30387-1630">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="30387-1631">Get-AzAutoApprovedPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="30387-1631">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="30387-1632">Обновлены следующие команды для функции: Флаг PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies в подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="30387-1632">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="30387-1633">Обновлены командлеты New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig.</span><span class="sxs-lookup"><span data-stu-id="30387-1633">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="30387-1634">Добавлен необязательный параметр -PrivateEndpointNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к частной конечной точке в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="30387-1634">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="30387-1635">Добавлен необязательный параметр -PrivateLinkServiceNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к службе приватного канала в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="30387-1635">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="30387-1636">Параметр ServiceName командлета AzPrivateLinkService был переименован на Name с псевдонимом ServiceName для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="30387-1636">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="30387-1637">Включен протокол ICMP для настройки правил безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="30387-1637">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="30387-1638">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="30387-1638">Updated cmdlets</span></span>
        - <span data-ttu-id="30387-1639">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="30387-1639">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="30387-1640">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="30387-1640">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="30387-1641">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="30387-1641">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="30387-1642">Добавлен ConnectionProtocolType (Ikev1/Ikev2) в качестве настраиваемого параметра для командлета New-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="30387-1642">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="30387-1643">Добавлен PrivateIpAddressVersion в LoadBalancerFrontendIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="30387-1643">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="30387-1644">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="30387-1644">Updated cmdlet:</span></span>
        - <span data-ttu-id="30387-1645">New-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="30387-1645">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="30387-1646">Add-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="30387-1646">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="30387-1647">Set-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="30387-1647">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="30387-1648">Команда New-AzApplicationGatewayProbeConfig Шлюза приложений обновлена для поддержки настраиваемого порта в зонде.</span><span class="sxs-lookup"><span data-stu-id="30387-1648">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="30387-1649">Обновлен командлет New-AzApplicationGatewayProbeConfig: добавлен необязательный параметр Port, который используется при проверке внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="30387-1649">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="30387-1650">Этот параметр применяется к номерам SKU Standard_V2 и WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="30387-1650">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="30387-1651">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="30387-1651">Az.OperationalInsights</span></span>
* <span data-ttu-id="30387-1652">Обновленная версия по умолчанию для сохраненных операций поиска имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="30387-1652">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="30387-1653">Исправлены ошибки при обработке регулярных выражений со значениями NULL в журналах.</span><span class="sxs-lookup"><span data-stu-id="30387-1653">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="30387-1654">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="30387-1654">Az.RecoveryServices</span></span>
* <span data-ttu-id="30387-1655">Обновлен файл Get-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="30387-1655">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="30387-1656">Обновлен файл Get-AzRecoveryServicesBackupContainer.md.</span><span class="sxs-lookup"><span data-stu-id="30387-1656">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="30387-1657">Обновлен файл Get-AzRecoveryServicesVault.md.</span><span class="sxs-lookup"><span data-stu-id="30387-1657">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="30387-1658">Обновлен файл Wait-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="30387-1658">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="30387-1659">Обновлен файл Set-AzRecoveryServicesVaultContext.md.</span><span class="sxs-lookup"><span data-stu-id="30387-1659">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="30387-1660">Обновлен файл Get-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="30387-1660">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="30387-1661">Обновлен файл Get-AzRecoveryServicesBackupRecoveryPoint.md.</span><span class="sxs-lookup"><span data-stu-id="30387-1661">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="30387-1662">Обновлен файл Restore-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="30387-1662">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="30387-1663">Обновлен вызов службы для отмены регистрации контейнера в общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-1663">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="30387-1664">Обновлен файл Set-AzRecoveryServicesAsrAlertSetting.md.</span><span class="sxs-lookup"><span data-stu-id="30387-1664">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="30387-1665">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30387-1665">Az.Resources</span></span>
- <span data-ttu-id="30387-1666">Удален отсутствующий командлет, который упоминается в документации по New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="30387-1666">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="30387-1667">Обновлены командлеты политик для использования новой версии API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="30387-1667">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="30387-1668">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="30387-1668">Az.ServiceBus</span></span>
* <span data-ttu-id="30387-1669">Добавлен новый командлет для создания маркера SAS: New-AzServiceBusAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="30387-1669">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="30387-1670">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="30387-1670">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="30387-1671">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30387-1671">Az.Sql</span></span>
* <span data-ttu-id="30387-1672">Исправлены отсутствующие примеры для командлета Set-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="30387-1672">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="30387-1673">Исправлены заданные повторяющиеся проверки для оценки наличия уязвимостей без указания адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="30387-1673">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="30387-1674">Исправлена незначительная опечатка в сообщении предупреждения.</span><span class="sxs-lookup"><span data-stu-id="30387-1674">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="30387-1675">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="30387-1675">Az.Storage</span></span>
* <span data-ttu-id="30387-1676">Обновлен пример в справочной документации для использования командлетом Get-AzStorageAccount правильного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="30387-1676">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="30387-1677">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="30387-1677">Az.StorageSync</span></span>
* <span data-ttu-id="30387-1678">Добавлен командлет Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="30387-1678">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="30387-1679">Исправлена проблема № 9551, связанная с TierFilesOlderThanDays.</span><span class="sxs-lookup"><span data-stu-id="30387-1679">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="30387-1680">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="30387-1680">Az.Websites</span></span>
* <span data-ttu-id="30387-1681">Исправлена ошибка, при которой некоторые свойства SiteConfig не возвращались Get-AzWebApp и Set-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="30387-1681">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="30387-1682">Добавлен новый параметр Location в Get-AzDeletedWebApp и Restore-AzDeletedWebApp.</span><span class="sxs-lookup"><span data-stu-id="30387-1682">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="30387-1683">Исправлена ошибка, которая возникала при клонировании слотов веб-приложений с помощью командлета New-AzWebApp-IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="30387-1683">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="30387-1684">2.4.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="30387-1684">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="30387-1685">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30387-1685">Az.Accounts</span></span>
* <span data-ttu-id="30387-1686">Добавлена поддержка командлетов профиля.</span><span class="sxs-lookup"><span data-stu-id="30387-1686">Add support for profile cmdlets</span></span>
* <span data-ttu-id="30387-1687">Добавлена поддержка сред и плоскостей данных в созданных командлетах.</span><span class="sxs-lookup"><span data-stu-id="30387-1687">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="30387-1688">Исправлена ошибка, когда в командлетах плоскости данных в Windows PowerShell в некоторых случаях использовалась неправильная конечная точка.</span><span class="sxs-lookup"><span data-stu-id="30387-1688">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="30387-1689">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="30387-1689">Az.Advisor</span></span>
* <span data-ttu-id="30387-1690">Выпущена общедоступная версия Az.Advisor.</span><span class="sxs-lookup"><span data-stu-id="30387-1690">GA release of Az.Advisor</span></span>
* <span data-ttu-id="30387-1691">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="30387-1691">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="30387-1692">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="30387-1692">Az.ApiManagement</span></span>
* <span data-ttu-id="30387-1693">исправлена проблема https://github.com/Azure/azure-powershell/issues/8671.</span><span class="sxs-lookup"><span data-stu-id="30387-1693">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="30387-1694">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="30387-1694">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="30387-1695">Добавлена поддержка запрашивания подписок по пользователю и продукту.</span><span class="sxs-lookup"><span data-stu-id="30387-1695">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="30387-1696">Добавлена поддержка создания запросов с использованием области "/", "/apis", "/apis/echo-api".</span><span class="sxs-lookup"><span data-stu-id="30387-1696">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="30387-1697">Исправлены проблемы https://github.com/Azure/azure-powershell/issues/9307 и https://github.com/Azure/azure-powershell/issues/8432.</span><span class="sxs-lookup"><span data-stu-id="30387-1697">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="30387-1698">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="30387-1698">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="30387-1699">Добавлена поддержка указания ApiVersion и ApiVersionSetId при импорте API-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="30387-1699">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="30387-1700">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="30387-1700">Az.Automation</span></span>
* <span data-ttu-id="30387-1701">Исправлена ошибка командлета Set-AzAutomationConnectionFieldValue при обработке строкового значения.</span><span class="sxs-lookup"><span data-stu-id="30387-1701">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30387-1702">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30387-1702">Az.Compute</span></span>
* <span data-ttu-id="30387-1703">В New AzImageConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="30387-1703">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="30387-1704">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="30387-1704">Az.DataFactory</span></span>
* <span data-ttu-id="30387-1705">Обновление выходных данных командлетов ADF, предназначенных для получения числа выполнений действий, конвейеров и триггеров, для поддержки канала Select-Object.</span><span class="sxs-lookup"><span data-stu-id="30387-1705">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="30387-1706">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="30387-1706">Az.EventGrid</span></span>
* <span data-ttu-id="30387-1707">Исправлена опечатка в документации по командлету New-AzEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="30387-1707">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="30387-1708">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="30387-1708">Az.IotHub</span></span>
* <span data-ttu-id="30387-1709">Добавлена поддержка повторного создания ключей политики авторизации.</span><span class="sxs-lookup"><span data-stu-id="30387-1709">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30387-1710">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30387-1710">Az.Network</span></span>
* <span data-ttu-id="30387-1711">К тегам общедоступного IP-адреса добавлен тег RoutingPreference.</span><span class="sxs-lookup"><span data-stu-id="30387-1711">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="30387-1712">Улучшены примеры для справочной документации по командлету Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="30387-1712">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="30387-1713">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="30387-1713">Az.PolicyInsights</span></span>
* <span data-ttu-id="30387-1714">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="30387-1714">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="30387-1715">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9446.</span><span class="sxs-lookup"><span data-stu-id="30387-1715">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="30387-1716">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="30387-1716">Az.OperationalInsights</span></span>
* <span data-ttu-id="30387-1717">Исправленная модель источника данных CustomLog возвращена в командлет Get-AzOperationalInsightsDataSource.</span><span class="sxs-lookup"><span data-stu-id="30387-1717">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="30387-1718">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="30387-1718">Az.RecoveryServices</span></span>
* <span data-ttu-id="30387-1719">Выпущено исправление для команды get-policy для виртуальных машин IaaS.</span><span class="sxs-lookup"><span data-stu-id="30387-1719">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="30387-1720">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30387-1720">Az.Resources</span></span>
    - <span data-ttu-id="30387-1721">Исправлен текст справки по параметру Get-AzPolicyState -Top.</span><span class="sxs-lookup"><span data-stu-id="30387-1721">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="30387-1722">Добавлена поддержка разбиения по страницам на стороне клиента для Get-AzPolicyAlias.</span><span class="sxs-lookup"><span data-stu-id="30387-1722">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="30387-1723">Добавлены новые параметры для Set-AzPolicyAssignment, -PolicyParameters и -PolicyParametersObject.</span><span class="sxs-lookup"><span data-stu-id="30387-1723">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="30387-1724">Добавлен ряд обновлений документов и примеров для командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="30387-1724">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="30387-1725">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="30387-1725">Az.ServiceBus</span></span>
* <span data-ttu-id="30387-1726">Исправление ошибки № 4938: командлет New-AzureRmServiceBusQueue возвращает ответ BadRequest (Недопустимый запрос) при задании значения MaxSizeInMegabytes.</span><span class="sxs-lookup"><span data-stu-id="30387-1726">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="30387-1727">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30387-1727">Az.Sql</span></span>
* <span data-ttu-id="30387-1728">Из выпуска предварительной версии в выпуск общедоступной версии добавлены командлеты группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="30387-1728">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="30387-1729">Поддержка аудита Azure SQL Server и баз данных с помощью новых командлетов:</span><span class="sxs-lookup"><span data-stu-id="30387-1729">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="30387-1730">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="30387-1730">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="30387-1731">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="30387-1731">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="30387-1732">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="30387-1732">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="30387-1733">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="30387-1733">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="30387-1734">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="30387-1734">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="30387-1735">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="30387-1735">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="30387-1736">Из параметров оценки уязвимостей удалены ограничения, касающиеся электронной почты.</span><span class="sxs-lookup"><span data-stu-id="30387-1736">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="30387-1737">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="30387-1737">Az.Storage</span></span>
* <span data-ttu-id="30387-1738">Два параметра в указанном ниже командлете — -IndexDocument и -ErrorDocument404Path, — которые ранее были обязательными, стали необязательными:</span><span class="sxs-lookup"><span data-stu-id="30387-1738">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="30387-1739">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="30387-1739">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="30387-1740">Обновлена справка по командлету Get-AzStorageBlobContent: добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="30387-1740">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="30387-1741">При сбое выполнения командлета с ошибкой StorageException отображаются дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="30387-1741">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="30387-1742">Добавлена поддержка создания или обновления учетной записи хранения с использованием проверки подлинности AAD DS для службы "Файлы Azure".</span><span class="sxs-lookup"><span data-stu-id="30387-1742">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="30387-1743">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30387-1743">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="30387-1744">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30387-1744">Set-AzStorageAccount</span></span>
* <span data-ttu-id="30387-1745">Добавлена поддержка перечисления или закрытия дескрипторов файлов для общей папки, каталога файлов или файла:</span><span class="sxs-lookup"><span data-stu-id="30387-1745">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="30387-1746">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="30387-1746">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="30387-1747">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="30387-1747">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="30387-1748">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="30387-1748">Az.StorageSync</span></span>
* <span data-ttu-id="30387-1749">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="30387-1749">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="30387-1750">2.3.2 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="30387-1750">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="30387-1751">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30387-1751">Az.Accounts</span></span>
* <span data-ttu-id="30387-1752">Исправлена ошибка, связанная с использованием неправильного URL-адреса для вызовов функций.</span><span class="sxs-lookup"><span data-stu-id="30387-1752">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="30387-1753">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8983.</span><span class="sxs-lookup"><span data-stu-id="30387-1753">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="30387-1754">Устранена проблема с псевдонимами из AzureRM для командлетов Az.</span><span class="sxs-lookup"><span data-stu-id="30387-1754">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="30387-1755">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="30387-1755">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="30387-1756">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest.</span><span class="sxs-lookup"><span data-stu-id="30387-1756">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30387-1757">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30387-1757">Az.Compute</span></span>
* <span data-ttu-id="30387-1758">Простые наборы параметров New-AzVm и New-AzVmss теперь принимают параметр ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="30387-1758">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="30387-1759">Исправлена опечатка в справочной документации по New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="30387-1759">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="30387-1760">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="30387-1760">Az.Dns</span></span>
* <span data-ttu-id="30387-1761">Исправлена опечатка в справочных примерах по использованию Set-AzDnsZone.</span><span class="sxs-lookup"><span data-stu-id="30387-1761">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="30387-1762">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="30387-1762">Az.EventGrid</span></span>
* <span data-ttu-id="30387-1763">Обновлен для использования API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="30387-1763">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="30387-1764">Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="30387-1764">New cmdlets:</span></span>
    - <span data-ttu-id="30387-1765">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="30387-1765">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="30387-1766">Создает домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-1766">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="30387-1767">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="30387-1767">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="30387-1768">Возвращает сведения о домене Сетки событий или список всех доменов Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-1768">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="30387-1769">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="30387-1769">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="30387-1770">Удаляет домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-1770">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="30387-1771">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="30387-1771">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="30387-1772">Повторно создает ключ общего доступа для домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-1772">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="30387-1773">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="30387-1773">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="30387-1774">Возвращает ключи общего доступа, используемые для публикации событий в домене Сетки событий.</span><span class="sxs-lookup"><span data-stu-id="30387-1774">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="30387-1775">New-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="30387-1775">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="30387-1776">Создает раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-1776">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="30387-1777">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="30387-1777">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="30387-1778">Возвращает сведения о разделе домена Сетки событий или список всех разделов определенного домена Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-1778">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="30387-1779">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="30387-1779">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="30387-1780">Удаляет раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-1780">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="30387-1781">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="30387-1781">Updated cmdlets:</span></span>
    - <span data-ttu-id="30387-1782">New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="30387-1782">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="30387-1783">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для нового домена Сетки событий и раздела домена Сетки событий и позволяющие создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="30387-1783">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="30387-1784">Добавляют новые обязательные параметры для указания имени нового домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="30387-1784">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="30387-1785">Добавляют новые наборы параметров для доменов и разделов домена и позволяют повторно использовать существующие параметры (например, EndPointType, SubjectBeginsWith и т. д.).</span><span class="sxs-lookup"><span data-stu-id="30387-1785">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="30387-1786">Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="30387-1786">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="30387-1787">срока действия подписки на событие;</span><span class="sxs-lookup"><span data-stu-id="30387-1787">Event subscription expiration date,</span></span>
            - <span data-ttu-id="30387-1788">параметров расширенной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="30387-1788">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="30387-1789">Добавляют новое перечисление для ServiceBusQueue в качестве места назначения.</span><span class="sxs-lookup"><span data-stu-id="30387-1789">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="30387-1790">Запрещают использование значение All в параметре -IncludedEventType и заменяют его следующим:</span><span class="sxs-lookup"><span data-stu-id="30387-1790">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="30387-1791">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="30387-1791">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="30387-1792">Добавляют новые необязательные параметры (Top, ODataQuery и NextLink) для поддержки разбиения на страницы и фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="30387-1792">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="30387-1793">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="30387-1793">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="30387-1794">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для домена Сетки событий и раздела домена Сетки событий и позволяющие удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="30387-1794">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="30387-1795">Добавляют новые обязательные параметры для указания имени домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="30387-1795">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="30387-1796">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="30387-1796">Az.FrontDoor</span></span>
* <span data-ttu-id="30387-1797">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="30387-1797">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="30387-1798">Добавляет поддержку преобразований и новое значение оператора автозавершения (RegEx).</span><span class="sxs-lookup"><span data-stu-id="30387-1798">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="30387-1799">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="30387-1799">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="30387-1800">Добавляет новые значения автозавершения.</span><span class="sxs-lookup"><span data-stu-id="30387-1800">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30387-1801">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30387-1801">Az.Network</span></span>
* <span data-ttu-id="30387-1802">Добавляет поддержку ресурса шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="30387-1802">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="30387-1803">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="30387-1803">New cmdlets</span></span>
        - <span data-ttu-id="30387-1804">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="30387-1804">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="30387-1805">Добавляет AvailablePrivateEndpointType.</span><span class="sxs-lookup"><span data-stu-id="30387-1805">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="30387-1806">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="30387-1806">New cmdlets</span></span>
        - <span data-ttu-id="30387-1807">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="30387-1807">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="30387-1808">Добавляет PrivatePrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="30387-1808">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="30387-1809">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="30387-1809">New cmdlets</span></span>
        - <span data-ttu-id="30387-1810">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="30387-1810">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="30387-1811">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="30387-1811">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="30387-1812">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="30387-1812">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="30387-1813">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="30387-1813">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="30387-1814">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="30387-1814">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="30387-1815">Добавляет PrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="30387-1815">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="30387-1816">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="30387-1816">New cmdlets</span></span>
        - <span data-ttu-id="30387-1817">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="30387-1817">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="30387-1818">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="30387-1818">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="30387-1819">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="30387-1819">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="30387-1820">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="30387-1820">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="30387-1821">Обновлены следующие команды для функции: флаг UseLocalAzureIpAddress для VPN-подключения.</span><span class="sxs-lookup"><span data-stu-id="30387-1821">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="30387-1822">Обновлен командлет New-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="30387-1822">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="30387-1823">Обновлен командлет Set-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="30387-1823">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="30387-1824">В пиринг ExpressRoute добавлено поле только для чтения PeeredConnections.</span><span class="sxs-lookup"><span data-stu-id="30387-1824">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="30387-1825">В ExpressRoute добавлено поле только для чтения GlobalReachEnabled.</span><span class="sxs-lookup"><span data-stu-id="30387-1825">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="30387-1826">Добавлен атрибут в рамках критического изменения, отменяющего статус устаревшего поля AllowGlobalReach в модели ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="30387-1826">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="30387-1827">Исправлена проблема, связанная с ошибкой 8756, при использовании TargetListenerID с командлетами AzApplicationGatewayRedirectConfiguration.</span><span class="sxs-lookup"><span data-stu-id="30387-1827">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="30387-1828">Исправлена ошибка в New-AzApplicationGatewayPathRuleConfig, не позволявшая задавать набор правил повторного создания.</span><span class="sxs-lookup"><span data-stu-id="30387-1828">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="30387-1829">Исправлено отображение VirtualNetworkTaps в NetworkInterfaceIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="30387-1829">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="30387-1830">Исправлены командлеты Cortex Get для отображения всех частей.</span><span class="sxs-lookup"><span data-stu-id="30387-1830">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="30387-1831">Исправлено создание ссылок VirtualHub для ExpressRouteGateways и VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="30387-1831">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="30387-1832">В AzureFirewall и NatGateway добавлена поддержка Зон доступности.</span><span class="sxs-lookup"><span data-stu-id="30387-1832">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="30387-1833">Добавлен командлет Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="30387-1833">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="30387-1834">Добавлена поддержка нескольких общедоступных IP-адресов для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-1834">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="30387-1835">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="30387-1835">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="30387-1836">Добавлен параметр -PublicIpAddress, который принимает один или несколько объектов общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="30387-1836">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="30387-1837">Добавлен параметр -VirtualNetwork, который принимает объект виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="30387-1837">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="30387-1838">Добавлены методы AddPublicIpAddress и RemovePublicIpAddress для объекта брандмауэра. Они принимают объект общедоступного IP-адреса в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="30387-1838">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="30387-1839">Не рекомендуется использовать параметры -PublicIpName и -VirtualNetworkName.</span><span class="sxs-lookup"><span data-stu-id="30387-1839">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="30387-1840">Обновлены следующие команды для функции: В параметрах проверки подлинности AAD VPN-клиента задан ресурс шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="30387-1840">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="30387-1841">Обновлен командлет New-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="30387-1841">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="30387-1842">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="30387-1842">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="30387-1843">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр-переключатель RemoveAadAuthentication для удаления в шлюзе параметров проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="30387-1843">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="30387-1844">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="30387-1844">Az.OperationalInsights</span></span>
* <span data-ttu-id="30387-1845">Добавлена поддержка SKU **pergb2018** в команде New-AzureRmOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="30387-1845">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="30387-1846">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30387-1846">Az.Resources</span></span>
* <span data-ttu-id="30387-1847">Поддержка дополнительных вариантов экспорта шаблона.</span><span class="sxs-lookup"><span data-stu-id="30387-1847">Support for additional Template Export options</span></span>
    - <span data-ttu-id="30387-1848">В Export-AzResourceGroup добавлен параметр -SkipResourceNameParameterization.</span><span class="sxs-lookup"><span data-stu-id="30387-1848">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="30387-1849">В Export-AzResourceGroup добавлен параметр -SkipAllParameterization.</span><span class="sxs-lookup"><span data-stu-id="30387-1849">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="30387-1850">В Export-AzResourceGroup добавлен параметр -Resource для фильтрации экспортированных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="30387-1850">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="30387-1851">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="30387-1851">Az.ServiceFabric</span></span>
* <span data-ttu-id="30387-1852">Исправлена ошибка, связанная с получением иногда неправильных отпечатков при добавлении сертификата ByExistingKeyVault.</span><span class="sxs-lookup"><span data-stu-id="30387-1852">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="30387-1853">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30387-1853">Az.Sql</span></span>
* <span data-ttu-id="30387-1854">Исправлен суффикс конечной точки хранилища службы "Расширенная защита от угроз Azure".</span><span class="sxs-lookup"><span data-stu-id="30387-1854">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="30387-1855">Исправлена ошибка, связанная с возможностью пакета "Расширенная защита данных" переопределять политику службы "Расширенная защита от угроз".</span><span class="sxs-lookup"><span data-stu-id="30387-1855">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="30387-1856">Новые командлеты для Management.Sql позволяют клиентам добавлять ключи TDE и задавать средство защиты TDE для управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="30387-1856">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="30387-1857">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="30387-1857">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="30387-1858">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="30387-1858">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="30387-1859">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="30387-1859">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="30387-1860">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="30387-1860">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="30387-1861">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="30387-1861">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="30387-1862">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="30387-1862">Az.Storage</span></span>
* <span data-ttu-id="30387-1863">Поддержка класса Kind в FileStorage и значения Premium_ZRS в SkuName при создании учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="30387-1863">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="30387-1864">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30387-1864">New-AzStorageAccount</span></span>
* <span data-ttu-id="30387-1865">Уточнено описание командлета неизменности BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="30387-1865">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="30387-1866">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="30387-1866">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="30387-1867">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="30387-1867">Az.Websites</span></span>
* <span data-ttu-id="30387-1868">Оптимизирует Get-AzWebAppCertificate для фильтрации по группе ресурсов на сервере, а не в клиенте.</span><span class="sxs-lookup"><span data-stu-id="30387-1868">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="30387-1869">Добавляет параметр-переключатель - UseDisasterRecovery в Get AzWebAppSnapshot.</span><span class="sxs-lookup"><span data-stu-id="30387-1869">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="30387-1870">2.2.0 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="30387-1870">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="30387-1871">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="30387-1871">Az.Cdn</span></span>
* <span data-ttu-id="30387-1872">Обновлены командлеты для поддержки функции rulesEngine на основе API версии 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="30387-1872">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30387-1873">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30387-1873">Az.Compute</span></span>
* <span data-ttu-id="30387-1874">Добавлен параметр `NoWait`, который запускает операцию и немедленно возвращает значение еще до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="30387-1874">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="30387-1875">Обновлены командлеты:   Export-AzLogAnalyticRequestRateByInterval; Export-AzLogAnalyticThrottledRequest; Remove-AzVM; Remove-AzVMAccessExtension; Remove-AzVMAEMExtension; Remove-AzVMChefExtension; Remove-AzVMCustomScriptExtension; Remove-AzVMDiagnosticsExtension; Remove-AzVMDiskEncryptionExtension; Remove-AzVMDscExtension; Remove-AzVMSqlServerExtension; Restart-AzVM; Set-AzVM; Set-AzVMAccessExtension; Set-AzVMADDomainExtension; Set-AzVMAEMExtension; Set-AzVMBginfoExtension; Set-AzVMChefExtension; Set-AzVMCustomScriptExtension; Set-AzVMDiagnosticsExtension; Set-AzVMDscExtension; Set-AzVMExtension; Start-AzVM; Stop-AzVM; Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="30387-1875">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="30387-1876">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="30387-1876">Az.EventHub</span></span>
* <span data-ttu-id="30387-1877">Исправлена ошибка № 9231. Командлет Get-AzEventHubNamespace не возвращал теги.</span><span class="sxs-lookup"><span data-stu-id="30387-1877">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="30387-1878">Исправлена ошибка № 9230. Командлет Get-AzEventHubNamespace возвращал значение ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="30387-1878">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30387-1879">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30387-1879">Az.Network</span></span>
* <span data-ttu-id="30387-1880">Обновлены параметры ResourceId и InputObject для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="30387-1880">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="30387-1881">Добавлены псевдонимы для параметров ResourceId и InputObject.</span><span class="sxs-lookup"><span data-stu-id="30387-1881">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="30387-1882">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="30387-1882">Az.PolicyInsights</span></span>
* <span data-ttu-id="30387-1883">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyEvent.</span><span class="sxs-lookup"><span data-stu-id="30387-1883">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="30387-1884">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="30387-1884">Az.RecoveryServices</span></span>
* <span data-ttu-id="30387-1885">Минимальный срок хранения политики IaaSVM изменился с 1 до 7 дней.</span><span class="sxs-lookup"><span data-stu-id="30387-1885">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="30387-1886">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="30387-1886">Az.ServiceBus</span></span>
* <span data-ttu-id="30387-1887">Исправлена ошибка № 9182. Командлет Get-AzServiceBusNamespace возвращал ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="30387-1887">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="30387-1888">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="30387-1888">Az.ServiceFabric</span></span>
* <span data-ttu-id="30387-1889">Исправлена опечатка в сообщении об ошибке для командлета Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="30387-1889">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="30387-1890">Добавлен отсутствующий символ в командных строках Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="30387-1890">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="30387-1891">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30387-1891">Az.Sql</span></span>
* <span data-ttu-id="30387-1892">Для командлета New-AzureSqlInstance добавлен параметр DnsZonePartner, обеспечивающий поддержку AutoDr для Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="30387-1892">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="30387-1893">Командлет Get-AzSqlDatabaseSecureConnectionPolicy объявлен неподдерживаемым.</span><span class="sxs-lookup"><span data-stu-id="30387-1893">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="30387-1894">Командлеты обнаружения угроз переименованы в командлеты Расширенной защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="30387-1894">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="30387-1895">Параметры -StorageSizeInGB и -LicenseType командлета New-AzSqlInstance теперь необязательны.</span><span class="sxs-lookup"><span data-stu-id="30387-1895">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="30387-1896">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="30387-1896">Az.Websites</span></span>
* <span data-ttu-id="30387-1897">Исправлены проблемы, когда удалялись теги при использовании Set-AzWebApp и Set-AzWebAppSlot со свойством -WebApp.</span><span class="sxs-lookup"><span data-stu-id="30387-1897">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="30387-1898">2.1.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="30387-1898">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="30387-1899">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="30387-1899">Az.ApiManagement</span></span>
* <span data-ttu-id="30387-1900">Созданы командлеты для управления диагностикой в глобальной области и в области API.</span><span class="sxs-lookup"><span data-stu-id="30387-1900">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="30387-1901">**Get-AzApiManagementDiagnostic** — получение диагностики, заданной глобально или на уровне области API.</span><span class="sxs-lookup"><span data-stu-id="30387-1901">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="30387-1902">**New-AzApiManagementDiagnostic** — создание диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="30387-1902">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="30387-1903">**New-AzApiManagementHttpMessageDiagnostic** — создание параметра диагностики, для которого регистрируются заголовки и размер байтов тела.</span><span class="sxs-lookup"><span data-stu-id="30387-1903">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="30387-1904">**New-AzApiManagementPipelineDiagnosticSetting** — создание параметров диагностики для сообщений HTTP, поступающих в шлюз или исходящих из него.</span><span class="sxs-lookup"><span data-stu-id="30387-1904">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="30387-1905">**New-AzApiManagementSamplingSetting** — создание параметра выборки для запросов и ответов касательно диагностики.</span><span class="sxs-lookup"><span data-stu-id="30387-1905">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="30387-1906">**Remove-AzApiManagementDiagnostic** — удаление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="30387-1906">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="30387-1907">**Set-AzApiManagementDiagnostic** — обновление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="30387-1907">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="30387-1908">Созданы командлеты для управления кэшем в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="30387-1908">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="30387-1909">**Get-AzApiManagementCache** — получение сведений о кэше, указанном идентификатором, или обо всех кэшах.</span><span class="sxs-lookup"><span data-stu-id="30387-1909">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="30387-1910">**New-AzApiManagementCache** — создание кэша по умолчанию или кэша в определенном регионе Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-1910">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="30387-1911">**Remove-AzApiManagementCache** — удаление кэша.</span><span class="sxs-lookup"><span data-stu-id="30387-1911">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="30387-1912">**Update-AzApiManagementCache** — обновление кэша.</span><span class="sxs-lookup"><span data-stu-id="30387-1912">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="30387-1913">Созданы командлеты для управления схемой API.</span><span class="sxs-lookup"><span data-stu-id="30387-1913">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="30387-1914">**New-AzApiManagementSchema** — создание схемы для API.</span><span class="sxs-lookup"><span data-stu-id="30387-1914">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="30387-1915">**Get-AzApiManagementSchema** — получение схем, настроенных в API.</span><span class="sxs-lookup"><span data-stu-id="30387-1915">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="30387-1916">**Remove-AzApiManagementSchema** — удаление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="30387-1916">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="30387-1917">**Set-AzApiManagementSchema** — обновление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="30387-1917">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="30387-1918">Создан командлет для создания токена пользователя.</span><span class="sxs-lookup"><span data-stu-id="30387-1918">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="30387-1919">**New-AzApiManagementUserToken** — создание токена пользователя, по умолчанию действительного в течение 8 часов. С помощью этого командлета можно создавать токен для пользователя GIT.</span><span class="sxs-lookup"><span data-stu-id="30387-1919">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="30387-1920">Создан командлет для получения состояния сети.</span><span class="sxs-lookup"><span data-stu-id="30387-1920">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="30387-1921">**Get-AzApiManagementNetworkStatus** — получение состояния подключения сети ресурсов, от которых зависит служба "Управление API".</span><span class="sxs-lookup"><span data-stu-id="30387-1921">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="30387-1922">Это полезно при развертывании службы ApiManagement в виртуальной сети и проверке того, не нарушена ли какая-либо из зависимостей.</span><span class="sxs-lookup"><span data-stu-id="30387-1922">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="30387-1923">Обновлен командлет **New-AzApiManagement** для управления службой ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="30387-1923">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="30387-1924">Добавлена поддержка нового SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="30387-1924">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="30387-1925">Добавлена поддержка для включения флага EnableClientCertificate в SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="30387-1925">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="30387-1926">Новый командлет **New-AzApiManagementSslSetting** позволяет настраивать параметр TLS/SSL для сервера (Backend) и внешнего интерфейса (Frontend).</span><span class="sxs-lookup"><span data-stu-id="30387-1926">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="30387-1927">Его также можно использовать для настройки Ciphers как 3DES, в ServerProtocols как Http2 для внешнего интерфейса (Frontend) службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="30387-1927">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="30387-1928">Добавлена поддержка настройки имени узла DeveloperPortal в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="30387-1928">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="30387-1929">Обновлен командлет **Get-AzApiManagementSsoToken** для извлечения объекта PsApiManagement в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="30387-1929">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="30387-1930">Обновлен командлет для отображения встроенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="30387-1930">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="30387-1931">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Код ошибки: ValidationError. Сообщение об ошибке: "Некоторые поля содержат неправильные значения". Сведения об ошибке: [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="30387-1931">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="30387-1932">Обновлен командлет **Export-AzApiManagementApi** для экспортирования программных интерфейсов в формате OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="30387-1932">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="30387-1933">Обновлен командлет **Import-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="30387-1933">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="30387-1934">Для импортирования API из спецификации документа OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="30387-1934">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="30387-1935">Для переопределения свойства PsApiManagementSchema, указанного в любом документе (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="30387-1935">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="30387-1936">Для переопределения свойства ServiceUrl, указанного в любом документе.</span><span class="sxs-lookup"><span data-stu-id="30387-1936">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="30387-1937">Обновлен командлет **Get-AzApiManagementPolicy** для возврата политики в формате, экранированном не для XML, с использованием rawxml.</span><span class="sxs-lookup"><span data-stu-id="30387-1937">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="30387-1938">Обновлен командлет **Set-AzApiManagementPolicy**. Он принимает политику в формате, экранированном не для XML, с использованием rawxml и в формате, экранированном для XML, с использованием XML.</span><span class="sxs-lookup"><span data-stu-id="30387-1938">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="30387-1939">Обновлен командлет **New-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="30387-1939">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="30387-1940">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="30387-1940">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="30387-1941">Для создания API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="30387-1941">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="30387-1942">Для клонирования API с использованием значений SourceApiId и SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="30387-1942">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="30387-1943">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="30387-1943">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="30387-1944">Обновлен командлет **Set-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="30387-1944">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="30387-1945">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="30387-1945">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="30387-1946">Для обновления API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="30387-1946">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="30387-1947">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="30387-1947">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="30387-1948">Обновлен командлет **New-AzApiManagementRevision**:</span><span class="sxs-lookup"><span data-stu-id="30387-1948">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="30387-1949">Для клонирования (копирования тегов, продуктов, операций и политик) существующей редакции с использованием SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="30387-1949">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="30387-1950">Новая редакция предполагает родительский идентификатор ApiId.</span><span class="sxs-lookup"><span data-stu-id="30387-1950">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="30387-1951">Для предоставления ApiRevisionDescription.</span><span class="sxs-lookup"><span data-stu-id="30387-1951">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="30387-1952">Для переопределения значения ServiceUrl при клонировании API.</span><span class="sxs-lookup"><span data-stu-id="30387-1952">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="30387-1953">Обновлен командлет **New-AzApiManagementIdentityProvider**:</span><span class="sxs-lookup"><span data-stu-id="30387-1953">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="30387-1954">Для настройки AAD или AADB2C с Authority.</span><span class="sxs-lookup"><span data-stu-id="30387-1954">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="30387-1955">Для установки политик SignupPolicy, SigninPolicy, ProfileEditingPolicy и PasswordResetPolicy.</span><span class="sxs-lookup"><span data-stu-id="30387-1955">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="30387-1956">Обновлен командлет **New-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="30387-1956">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="30387-1957">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="30387-1957">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="30387-1958">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="30387-1958">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="30387-1959">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="30387-1959">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="30387-1960">Обновлен командлет **Set-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="30387-1960">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="30387-1961">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="30387-1961">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="30387-1962">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="30387-1962">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="30387-1963">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="30387-1963">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="30387-1964">Следующие командлеты обновлены, чтобы принимать значение ResourceId в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="30387-1964">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="30387-1965">New-AzApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="30387-1965">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="30387-1966">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="30387-1966">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="30387-1967">Get-AzApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="30387-1967">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="30387-1968">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="30387-1968">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="30387-1969">Get-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="30387-1969">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="30387-1970">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="30387-1970">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="30387-1971">Get-AzApiManagementAuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="30387-1971">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="30387-1972">Get-AzApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="30387-1972">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="30387-1973">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="30387-1973">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="30387-1974">Get-AzApiManagementCertificate.</span><span class="sxs-lookup"><span data-stu-id="30387-1974">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="30387-1975">Remove-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="30387-1975">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="30387-1976">Remove-AzApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="30387-1976">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="30387-1977">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="30387-1977">Az.Automation</span></span>
* <span data-ttu-id="30387-1978">Обновлен командлет Get-AzAutomationJobOutputRecord для обработки значений в формате JSON и в виде текстовой записи.</span><span class="sxs-lookup"><span data-stu-id="30387-1978">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="30387-1979">исправлена проблема https://github.com/Azure/azure-powershell/issues/7977.</span><span class="sxs-lookup"><span data-stu-id="30387-1979">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="30387-1980">исправлена проблема https://github.com/Azure/azure-powershell/issues/8600.</span><span class="sxs-lookup"><span data-stu-id="30387-1980">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="30387-1981">Поведение командлета Start-AzAutomationDscCompilationJob изменено так, чтобы сразу же запустить задание, а не ждать его завершения.</span><span class="sxs-lookup"><span data-stu-id="30387-1981">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="30387-1982">исправлена проблема https://github.com/Azure/azure-powershell/issues/8347.</span><span class="sxs-lookup"><span data-stu-id="30387-1982">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="30387-1983">Исправлен командлет Get-AzAutomationDscNode, возвращающий все узлы при использовании -Name.</span><span class="sxs-lookup"><span data-stu-id="30387-1983">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="30387-1984">Теперь он возвращает только соответствующий узел.</span><span class="sxs-lookup"><span data-stu-id="30387-1984">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30387-1985">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30387-1985">Az.Compute</span></span>
* <span data-ttu-id="30387-1986">Добавлены параметры ProtectFromScaleIn и ProtectFromScaleSetAction для командлета Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="30387-1986">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="30387-1987">Командлет New-AzVM с простым набором параметров теперь по умолчанию использует доступное расположение, если регион "восточная часть США" не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="30387-1987">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="30387-1988">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="30387-1988">Az.DataLakeStore</span></span>
* <span data-ttu-id="30387-1989">Обновлен пакет SDK ADLS для использования httpclient. В инфраструктуру Azure интегрирована проверка плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="30387-1989">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="30387-1990">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="30387-1990">Az.Monitor</span></span>
* <span data-ttu-id="30387-1991">Исправлены неправильные имена параметров в справочных примерах.</span><span class="sxs-lookup"><span data-stu-id="30387-1991">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30387-1992">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30387-1992">Az.Network</span></span>
* <span data-ttu-id="30387-1993">Добавлен флаг DisableBgpRoutePropagation для выходных данных действующей таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="30387-1993">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="30387-1994">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="30387-1994">Updated cmdlet:</span></span>
        - <span data-ttu-id="30387-1995">Get-AzEffectiveRouteTable.</span><span class="sxs-lookup"><span data-stu-id="30387-1995">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="30387-1996">Исправлен двойной дефис в документации New-AzApplicationGatewayTrustedRootCertificate.</span><span class="sxs-lookup"><span data-stu-id="30387-1996">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="30387-1997">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30387-1997">Az.Resources</span></span>
* <span data-ttu-id="30387-1998">Добавлен новый командлет Get-AzureRmDenyAssignment для получения запрещающих назначений.</span><span class="sxs-lookup"><span data-stu-id="30387-1998">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="30387-1999">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30387-1999">Az.Sql</span></span>
* <span data-ttu-id="30387-2000">Командлеты Расширенной защиты от угроз переименованы на командлеты Расширенной защиты данных, и оценка уязвимости включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="30387-2000">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="30387-2001">2.0.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="30387-2001">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="30387-2002">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30387-2002">Az.Accounts</span></span>
* <span data-ttu-id="30387-2003">Обновлена библиотека аутентификации для устранения проблем с ADFS при использовании аутентификации на основе имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="30387-2003">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="30387-2004">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="30387-2004">Az.CognitiveServices</span></span>
* <span data-ttu-id="30387-2005">Отображается только заявление об отказе Bing для служб Поиска Bing.</span><span class="sxs-lookup"><span data-stu-id="30387-2005">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="30387-2006">Исправлена проблема с созданием учетной записи.</span><span class="sxs-lookup"><span data-stu-id="30387-2006">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30387-2007">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30387-2007">Az.Compute</span></span>
* <span data-ttu-id="30387-2008">Функция группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="30387-2008">Proximity placement group feature.</span></span>
    - <span data-ttu-id="30387-2009">Добавлены следующие новые командлеты:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="30387-2009">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="30387-2010">Новый параметр ProximityPlacementGroupId будет добавлен в следующие командлеты:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="30387-2010">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="30387-2011">В командлет New-AzGalleryImageVersion добавлен параметр StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="30387-2011">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="30387-2012">TargetRegion в командлете New-AzGalleryImageVersion может содержать StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="30387-2012">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="30387-2013">Параметр-переключатель SkipShutdown добавлен в командлеты Stop-AzVM и Stop-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="30387-2013">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="30387-2014">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="30387-2014">Breaking changes</span></span>
    - <span data-ttu-id="30387-2015">Командлет SET-AzVMBootDiagnostics изменен на Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="30387-2015">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="30387-2016">Командлет Export-AzLogAnalyticThrottledRequests изменен на Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="30387-2016">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="30387-2017">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="30387-2017">Az.DeploymentManager</span></span>
* <span data-ttu-id="30387-2018">Первая общедоступная версия командлетов диспетчера развертывания Azure</span><span class="sxs-lookup"><span data-stu-id="30387-2018">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="30387-2019">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="30387-2019">Az.Dns</span></span>
* <span data-ttu-id="30387-2020">Автоматическое делегирование DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="30387-2020">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="30387-2021">Командлет для создания зоны DNS принимает имя родительской зоны в качестве дополнительного необязательного параметра.</span><span class="sxs-lookup"><span data-stu-id="30387-2021">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="30387-2022">Он добавляет записи NS в родительской зоне для созданной дочерней зоны.</span><span class="sxs-lookup"><span data-stu-id="30387-2022">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="30387-2023">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="30387-2023">Az.FrontDoor</span></span>
* <span data-ttu-id="30387-2024">Первая общедоступная версия командлетов Azure FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="30387-2024">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="30387-2025">Переименованы командлеты WAF для включения Waf.</span><span class="sxs-lookup"><span data-stu-id="30387-2025">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="30387-2026">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="30387-2026">Az.HDInsight</span></span>
* <span data-ttu-id="30387-2027">Удалены два командлета:</span><span class="sxs-lookup"><span data-stu-id="30387-2027">Removed two cmdlets:</span></span>
    - <span data-ttu-id="30387-2028">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="30387-2028">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="30387-2029">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="30387-2029">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="30387-2030">Добавлен новый командлет Set-AzHDInsightGatewayCredential для замены Grant-AzHDInsightHttpServicesAccess.</span><span class="sxs-lookup"><span data-stu-id="30387-2030">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="30387-2031">Обновлен командлет Get-AzHDInsightJobOutput для различения ролей читателя и оператора HDInsight:</span><span class="sxs-lookup"><span data-stu-id="30387-2031">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="30387-2032">Пользователям с ролью читателя не нужно указывать параметр DefaultStorageAccountKey явным образом, иначе возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="30387-2032">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="30387-2033">На пользователей с ролью оператора HDInsight это не повлияет.</span><span class="sxs-lookup"><span data-stu-id="30387-2033">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="30387-2034">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="30387-2034">Az.Monitor</span></span>
* <span data-ttu-id="30387-2035">Новые командлеты для API SQR (запланированное правило запросов)</span><span class="sxs-lookup"><span data-stu-id="30387-2035">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="30387-2036">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="30387-2036">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="30387-2037">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="30387-2037">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="30387-2038">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="30387-2038">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="30387-2039">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="30387-2039">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="30387-2040">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="30387-2040">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="30387-2041">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="30387-2041">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="30387-2042">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="30387-2042">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="30387-2043">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="30387-2043">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="30387-2044">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="30387-2044">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="30387-2045">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="30387-2045">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="30387-2046">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="30387-2046">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="30387-2047">См. подробнее об [API SQR](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules).</span><span class="sxs-lookup"><span data-stu-id="30387-2047">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="30387-2048">Обновлен файл Az.Monitor.md для включения командлетов для правила генерации оповещений на основе метрик GenV2(не классическая версия).</span><span class="sxs-lookup"><span data-stu-id="30387-2048">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30387-2049">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30387-2049">Az.Network</span></span>
* <span data-ttu-id="30387-2050">Добавлена поддержка для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="30387-2050">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="30387-2051">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="30387-2051">New cmdlets</span></span>
        - <span data-ttu-id="30387-2052">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="30387-2052">New-AzNatGateway</span></span>
        - <span data-ttu-id="30387-2053">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="30387-2053">Get-AzNatGateway</span></span>
        - <span data-ttu-id="30387-2054">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="30387-2054">Set-AzNatGateway</span></span>
        - <span data-ttu-id="30387-2055">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="30387-2055">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="30387-2056">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="30387-2056">Updated cmdlets</span></span>
        - <span data-ttu-id="30387-2057">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="30387-2057">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="30387-2058">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="30387-2058">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="30387-2059">Обновлены следующие команды для функции: Настройка и удаление пользовательских маршрутов через шлюз в Бруклине.</span><span class="sxs-lookup"><span data-stu-id="30387-2059">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="30387-2060">Обновлен командлет New-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="30387-2060">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="30387-2061">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="30387-2061">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="30387-2062">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="30387-2062">Az.PolicyInsights</span></span>
* <span data-ttu-id="30387-2063">Добавлена поддержка сведений об оценке политики запросов.</span><span class="sxs-lookup"><span data-stu-id="30387-2063">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="30387-2064">Добавлен параметр -Expand в командлет Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="30387-2064">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="30387-2065">Добавлена поддержка -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="30387-2065">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="30387-2066">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="30387-2066">Az.RecoveryServices</span></span>
* <span data-ttu-id="30387-2067">Добавлена поддержка перекрестной подписки на Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="30387-2067">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="30387-2068">Добавлена возможность отмечать предстоящие критически важные изменения для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="30387-2068">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="30387-2069">Исправлены план восстановления и план действий для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="30387-2069">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="30387-2070">Исправлено сетевое сопоставление обновления Azure Site Recovery (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="30387-2070">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="30387-2071">Исправлено направление защиты обновления Azure Site Recovery для управляемых дисков (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="30387-2071">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="30387-2072">Добавлены другие незначительные исправления.</span><span class="sxs-lookup"><span data-stu-id="30387-2072">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="30387-2073">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="30387-2073">Az.Relay</span></span>
* <span data-ttu-id="30387-2074">Исправлены опечатки в сообщениях для клиентов.</span><span class="sxs-lookup"><span data-stu-id="30387-2074">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="30387-2075">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="30387-2075">Az.ServiceBus</span></span>
* <span data-ttu-id="30387-2076">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="30387-2076">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="30387-2077">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="30387-2077">Az.Storage</span></span>
* <span data-ttu-id="30387-2078">Выполнено обновление клиентской библиотеки хранилища до версии 10.0.1 (пространство имен всех объектов из этого пакета SDK изменено с Microsoft.WindowsAzure.Storage. *на Microsoft.Azure.Storage*).</span><span class="sxs-lookup"><span data-stu-id="30387-2078">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="30387-2079">Выполнено обновление до Microsoft.Azure.Management.Storage версии 11.0.0 для включения поддержки нового API версии 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="30387-2079">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="30387-2080">Значение свойства Kind по умолчанию в учетной записи хранения изменено со Storage на StorageV2.</span><span class="sxs-lookup"><span data-stu-id="30387-2080">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="30387-2081">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30387-2081">New-AzStorageAccount</span></span>
* <span data-ttu-id="30387-2082">Изменено значение Sku.Name в выходных данных командлета учетной записи хранения в соответствии со значением Sku.Name во входных данных путем добавления _ (например, StandardLRS изменено на Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="30387-2082">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="30387-2083">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30387-2083">New-AzStorageAccount</span></span>
    - <span data-ttu-id="30387-2084">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30387-2084">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="30387-2085">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30387-2085">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="30387-2086">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="30387-2086">Az.Websites</span></span>
* <span data-ttu-id="30387-2087">Свойство Kind теперь будет задаваться объектам PSSite, возвращаемым командлетом Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="30387-2087">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="30387-2088">Get-AzWebApp\*Metrics и Get-AzAppServicePlanMetrics считаются нерекомендуемыми.</span><span class="sxs-lookup"><span data-stu-id="30387-2088">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="30387-2089">1.8.0 — апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="30387-2089">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="30387-2090">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="30387-2090">Highlights since the last major release</span></span>
* <span data-ttu-id="30387-2091">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="30387-2091">General availability of `Az` module</span></span>
* <span data-ttu-id="30387-2092">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="30387-2092">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="30387-2093">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="30387-2093">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="30387-2094">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="30387-2094">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="30387-2095">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="30387-2095">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="30387-2096">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="30387-2096">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="30387-2097">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="30387-2097">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="30387-2098">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30387-2098">Az.Accounts</span></span>
* <span data-ttu-id="30387-2099">Обновлен командлет Uninstall-AzureRm для правильного удаления модулей в Mac.</span><span class="sxs-lookup"><span data-stu-id="30387-2099">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="30387-2100">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="30387-2100">Az.Batch</span></span>
* <span data-ttu-id="30387-2101">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="30387-2101">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="30387-2102">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="30387-2102">Az.Cdn</span></span>
* <span data-ttu-id="30387-2103">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="30387-2103">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="30387-2104">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="30387-2104">Az.CognitiveServices</span></span>
* <span data-ttu-id="30387-2105">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="30387-2105">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30387-2106">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30387-2106">Az.Compute</span></span>
* <span data-ttu-id="30387-2107">Устранена проблема с установкой AEM, если в идентификаторах ресурсов дисков группа ресурсов указана в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="30387-2107">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="30387-2108">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="30387-2108">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="30387-2109">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="30387-2109">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="30387-2110">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="30387-2110">Az.DataFactory</span></span>
* <span data-ttu-id="30387-2111">Добавлены свойства SsisProperties, если NodeCount не имеет значения NULL для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="30387-2111">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="30387-2112">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="30387-2112">Az.DataLakeStore</span></span>
* <span data-ttu-id="30387-2113">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="30387-2113">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="30387-2114">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="30387-2114">Az.EventGrid</span></span>
* <span data-ttu-id="30387-2115">Обновлен текст справки для конечной точки, указывающий, что необходимо создать ресурсы, прежде чем использовать командлеты для создания или обновления подписки на события.</span><span class="sxs-lookup"><span data-stu-id="30387-2115">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="30387-2116">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="30387-2116">Az.EventHub</span></span>
* <span data-ttu-id="30387-2117">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="30387-2117">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="30387-2118">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="30387-2118">Az.HDInsight</span></span>
* <span data-ttu-id="30387-2119">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="30387-2119">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="30387-2120">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="30387-2120">Az.IotHub</span></span>
* <span data-ttu-id="30387-2121">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="30387-2121">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="30387-2122">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="30387-2122">Az.KeyVault</span></span>
* <span data-ttu-id="30387-2123">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="30387-2123">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="30387-2124">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="30387-2124">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="30387-2125">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="30387-2125">Az.MachineLearning</span></span>
* <span data-ttu-id="30387-2126">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="30387-2126">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="30387-2127">Az.Media</span><span class="sxs-lookup"><span data-stu-id="30387-2127">Az.Media</span></span>
* <span data-ttu-id="30387-2128">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="30387-2128">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="30387-2129">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="30387-2129">Az.Monitor</span></span>
  * <span data-ttu-id="30387-2130">Добавлены новые командлеты для правила генерации оповещений на основе метрик GenV2 (не классических).</span><span class="sxs-lookup"><span data-stu-id="30387-2130">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="30387-2131">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="30387-2131">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="30387-2132">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="30387-2132">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="30387-2133">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="30387-2133">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="30387-2134">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="30387-2134">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="30387-2135">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="30387-2135">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="30387-2136">Обновлен пакет SDK Monitor до предварительной версии 0.22.0.</span><span class="sxs-lookup"><span data-stu-id="30387-2136">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30387-2137">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30387-2137">Az.Network</span></span>
* <span data-ttu-id="30387-2138">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="30387-2138">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="30387-2139">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="30387-2139">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="30387-2140">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="30387-2140">Az.NotificationHubs</span></span>
* <span data-ttu-id="30387-2141">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="30387-2141">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="30387-2142">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="30387-2142">Az.OperationalInsights</span></span>
* <span data-ttu-id="30387-2143">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="30387-2143">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="30387-2144">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="30387-2144">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="30387-2145">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="30387-2145">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="30387-2146">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="30387-2146">Az.RecoveryServices</span></span>
* <span data-ttu-id="30387-2147">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="30387-2147">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="30387-2148">Обновлен табличный формат для SQL на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-2148">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="30387-2149">Добавлен альтернативный метод для получения расположения в Общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-2149">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="30387-2150">Обновлено значение ScheduleRunDays в объекте SchedulePolicy в соответствии с часовым поясом.</span><span class="sxs-lookup"><span data-stu-id="30387-2150">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="30387-2151">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="30387-2151">Az.RedisCache</span></span>
* <span data-ttu-id="30387-2152">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="30387-2152">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="30387-2153">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30387-2153">Az.Resources</span></span>
* <span data-ttu-id="30387-2154">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="30387-2154">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="30387-2155">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30387-2155">Az.Sql</span></span>
* <span data-ttu-id="30387-2156">Заменена зависимость от пакета SDK монитора на обычный код.</span><span class="sxs-lookup"><span data-stu-id="30387-2156">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="30387-2157">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="30387-2157">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="30387-2158">Улучшен процесс классификации нескольких столбцов.</span><span class="sxs-lookup"><span data-stu-id="30387-2158">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="30387-2159">Добавлены свойства SKU (имя, семейство, производительность SKU) в отклике Get-AzSqlServerServiceObjective, а также по умолчанию задан табличный формат.</span><span class="sxs-lookup"><span data-stu-id="30387-2159">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="30387-2160">C помощью Get-AzSqlServerServiceObjective теперь можно получать список доступных целевых служб по расположению без необходимости заранее размещать сервер в регионе.</span><span class="sxs-lookup"><span data-stu-id="30387-2160">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="30387-2161">Поддерживается параметр часового пояса при создании Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="30387-2161">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="30387-2162">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="30387-2162">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="30387-2163">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="30387-2163">Az.Websites</span></span>
* <span data-ttu-id="30387-2164">Исправлены командлеты Set-AzWebApp и Set-AzWebAppSlot, которые теперь не удаляют теги при выполнении.</span><span class="sxs-lookup"><span data-stu-id="30387-2164">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="30387-2165">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="30387-2165">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="30387-2166">Обновлен пакет SDK веб-узлов.</span><span class="sxs-lookup"><span data-stu-id="30387-2166">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="30387-2167">Удалено свойство AdminSiteName из PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="30387-2167">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="30387-2168">1.7.0 —апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="30387-2168">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="30387-2169">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="30387-2169">Highlights since the last major release</span></span>
* <span data-ttu-id="30387-2170">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="30387-2170">General availability of `Az` module</span></span>
* <span data-ttu-id="30387-2171">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="30387-2171">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="30387-2172">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="30387-2172">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="30387-2173">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="30387-2173">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="30387-2174">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="30387-2174">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="30387-2175">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="30387-2175">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="30387-2176">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="30387-2176">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="30387-2177">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30387-2177">Az.Accounts</span></span>
* <span data-ttu-id="30387-2178">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметр AzureAnalysisServicesEndpointResourceId.</span><span class="sxs-lookup"><span data-stu-id="30387-2178">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="30387-2179">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="30387-2179">Az.AnalysisServices</span></span>
* <span data-ttu-id="30387-2180">Использование ServiceClient в командлетах плоскости данных и удаление исходной логики проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="30387-2180">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="30387-2181">Add-AzureASAccount используется как оболочка для Connect-AzAccount во избежание критических изменений.</span><span class="sxs-lookup"><span data-stu-id="30387-2181">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="30387-2182">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="30387-2182">Az.Automation</span></span>
* <span data-ttu-id="30387-2183">Исправлена ошибка командлета New-AzAutomationSoftwareUpdateConfiguration, связанная с включением.</span><span class="sxs-lookup"><span data-stu-id="30387-2183">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="30387-2184">Теперь параметры IncludedKbNumber и IncludedPackageNameMask должны работать нормально.</span><span class="sxs-lookup"><span data-stu-id="30387-2184">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="30387-2185">Исправлена ошибка динамической группы управления обновлениями службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-2185">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30387-2186">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30387-2186">Az.Compute</span></span>
* <span data-ttu-id="30387-2187">В командлеты New-AzDiskConfig и New-AzSnapshotConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="30387-2187">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="30387-2188">Теперь можно создавать виртуальные машину на основе образов из коллекции от других клиентов.</span><span class="sxs-lookup"><span data-stu-id="30387-2188">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="30387-2189">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="30387-2189">Az.ContainerInstance</span></span>
* <span data-ttu-id="30387-2190">Исправлена проблема в параметре -Command командлета New-AzContainerGroup, из-за которой в конце добавлялся пустой аргумент.</span><span class="sxs-lookup"><span data-stu-id="30387-2190">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="30387-2191">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="30387-2191">Az.DataFactory</span></span>
* <span data-ttu-id="30387-2192">Пакет SDK для ADF .NET обновлен до версии 3.0.2.</span><span class="sxs-lookup"><span data-stu-id="30387-2192">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="30387-2193">Командлет Set-AzDataFactoryV2 обновлен с помощью дополнительных параметров для настроек, связанных с RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="30387-2193">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="30387-2194">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30387-2194">Az.Resources</span></span>
* <span data-ttu-id="30387-2195">Улучшена обработка поставщиков Get-AzResource при предоставлении параметров -ResourceId или -ResourceGroupName, -Name и -ResourceType.</span><span class="sxs-lookup"><span data-stu-id="30387-2195">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="30387-2196">Улучшена обработка ошибок в командлетах Test-AzDeployment и Test-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="30387-2196">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="30387-2197">Теперь ошибки, возникающие за пределами проверки развертывания, обрабатываются и включаются в выходные данные команды.</span><span class="sxs-lookup"><span data-stu-id="30387-2197">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="30387-2198">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="30387-2198">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="30387-2199">Добавлен параметр-переключатель -IgnoreDynamicParameters, с помощью которого можно настроить командлеты развертывания так, чтобы они пропускали запросы в сценариях скриптов и заданий.</span><span class="sxs-lookup"><span data-stu-id="30387-2199">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="30387-2200">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="30387-2200">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="30387-2201">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30387-2201">Az.Sql</span></span>
* <span data-ttu-id="30387-2202">Поддержка классификации данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="30387-2202">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="30387-2203">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="30387-2203">Az.Storage</span></span>
* <span data-ttu-id="30387-2204">Подробные сообщения об ошибке передаются при создании контекста хранилища с помощью параметра -UseConnectedAccount, но без входа в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-2204">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="30387-2205">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="30387-2205">New-AzStorageContext</span></span>
* <span data-ttu-id="30387-2206">Поддержка свойств службы управления BLOB-объектов в указанной учетной записи хранения с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="30387-2206">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="30387-2207">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="30387-2207">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="30387-2208">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="30387-2208">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="30387-2209">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="30387-2209">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="30387-2210">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="30387-2210">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="30387-2211">Поддержка параметра -AsJob в командлетах для отправки и скачивания больших двоичных объектов и файлов.</span><span class="sxs-lookup"><span data-stu-id="30387-2211">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="30387-2212">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="30387-2212">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="30387-2213">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="30387-2213">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="30387-2214">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="30387-2214">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="30387-2215">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="30387-2215">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="30387-2216">1.6.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="30387-2216">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="30387-2217">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="30387-2217">Highlights since the last major release</span></span>
* <span data-ttu-id="30387-2218">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="30387-2218">General availability of `Az` module</span></span>
* <span data-ttu-id="30387-2219">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="30387-2219">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="30387-2220">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="30387-2220">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="30387-2221">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="30387-2221">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="30387-2222">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="30387-2222">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="30387-2223">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="30387-2223">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="30387-2224">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="30387-2224">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="30387-2225">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="30387-2225">Az.Automation</span></span>
* <span data-ttu-id="30387-2226">В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:</span><span class="sxs-lookup"><span data-stu-id="30387-2226">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="30387-2227">динамическое группирование;</span><span class="sxs-lookup"><span data-stu-id="30387-2227">Dynamic grouping</span></span>
    * <span data-ttu-id="30387-2228">скрипты предварительного или последующего выполнения;</span><span class="sxs-lookup"><span data-stu-id="30387-2228">Pre-Post script</span></span>
    * <span data-ttu-id="30387-2229">параметр перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="30387-2229">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30387-2230">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30387-2230">Az.Compute</span></span>
* <span data-ttu-id="30387-2231">Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.</span><span class="sxs-lookup"><span data-stu-id="30387-2231">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="30387-2232">Обновление клиентской библиотеки вычислений до версии 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="30387-2232">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="30387-2233">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="30387-2233">Az.KeyVault</span></span>
* <span data-ttu-id="30387-2234">Добавлена поддержка подстановочных знаков в командлетах KeyVault.</span><span class="sxs-lookup"><span data-stu-id="30387-2234">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30387-2235">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30387-2235">Az.Network</span></span>
* <span data-ttu-id="30387-2236">Добавлена поддержка анализа угроз для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-2236">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="30387-2237">Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="30387-2237">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="30387-2238">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="30387-2238">Az.RecoveryServices</span></span>
* <span data-ttu-id="30387-2239">В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.</span><span class="sxs-lookup"><span data-stu-id="30387-2239">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="30387-2240">Добавлена поддержка канала для отмены регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="30387-2240">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="30387-2241">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30387-2241">Az.Resources</span></span>
* <span data-ttu-id="30387-2242">Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="30387-2242">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="30387-2243">Обновлены учетные данные, используемые при общих вызовах к ARM.</span><span class="sxs-lookup"><span data-stu-id="30387-2243">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="30387-2244">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30387-2244">Az.Sql</span></span>
* <span data-ttu-id="30387-2245">Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="30387-2245">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="30387-2246">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="30387-2246">Az.Storage</span></span>
* <span data-ttu-id="30387-2247">Поддержка получения, настройки и удаления политики управления в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="30387-2247">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="30387-2248">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="30387-2248">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="30387-2249">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="30387-2249">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="30387-2250">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="30387-2250">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="30387-2251">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="30387-2251">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="30387-2252">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="30387-2252">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="30387-2253">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="30387-2253">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="30387-2254">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="30387-2254">Az.Websites</span></span>
* <span data-ttu-id="30387-2255">Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="30387-2255">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="30387-2256">1.5.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="30387-2256">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="30387-2257">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30387-2257">Az.Accounts</span></span>
* <span data-ttu-id="30387-2258">Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.</span><span class="sxs-lookup"><span data-stu-id="30387-2258">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="30387-2259">Обновлены примеры для Connect AzAccount.</span><span class="sxs-lookup"><span data-stu-id="30387-2259">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="30387-2260">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="30387-2260">Az.Automation</span></span>
* <span data-ttu-id="30387-2261">Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-2261">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="30387-2262">Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов.</span><span class="sxs-lookup"><span data-stu-id="30387-2262">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="30387-2263">Теперь он возвращает все узлы.</span><span class="sxs-lookup"><span data-stu-id="30387-2263">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="30387-2264">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="30387-2264">Az.Cdn</span></span>
* <span data-ttu-id="30387-2265">Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.</span><span class="sxs-lookup"><span data-stu-id="30387-2265">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30387-2266">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30387-2266">Az.Compute</span></span>
* <span data-ttu-id="30387-2267">Добавлена поддержка подстановочных знаков в командлетах Get.</span><span class="sxs-lookup"><span data-stu-id="30387-2267">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="30387-2268">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="30387-2268">Az.DataFactory</span></span>
* <span data-ttu-id="30387-2269">Обновлен пакет SDK для ADF .NET до версии 3.0.1.</span><span class="sxs-lookup"><span data-stu-id="30387-2269">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="30387-2270">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="30387-2270">Az.LogicApp</span></span>
* <span data-ttu-id="30387-2271">Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.</span><span class="sxs-lookup"><span data-stu-id="30387-2271">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30387-2272">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30387-2272">Az.Network</span></span>
* <span data-ttu-id="30387-2273">Добавлена поддержка подстановочных знаков в командлетах Network.</span><span class="sxs-lookup"><span data-stu-id="30387-2273">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="30387-2274">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="30387-2274">Az.RecoveryServices</span></span>
* <span data-ttu-id="30387-2275">Добавлена поддержка SQL Server на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-2275">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="30387-2276">Обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="30387-2276">SDK Update</span></span>
* <span data-ttu-id="30387-2277">Удалена проверка VMappContainer в Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="30387-2277">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="30387-2278">Добавлены параметры Name и ServerName для Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="30387-2278">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="30387-2279">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30387-2279">Az.Resources</span></span>
* <span data-ttu-id="30387-2280">Добавлен параметр `-TemplateObject` в командлеты для развертывания.</span><span class="sxs-lookup"><span data-stu-id="30387-2280">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="30387-2281">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.</span><span class="sxs-lookup"><span data-stu-id="30387-2281">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="30387-2282">Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="30387-2282">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="30387-2283">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.</span><span class="sxs-lookup"><span data-stu-id="30387-2283">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="30387-2284">Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="30387-2284">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="30387-2285">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.</span><span class="sxs-lookup"><span data-stu-id="30387-2285">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="30387-2286">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30387-2286">Az.Sql</span></span>
* <span data-ttu-id="30387-2287">Обновление AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="30387-2287">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="30387-2288">Исправлено поведение для пограничного случая при создании параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="30387-2288">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="30387-2289">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="30387-2289">Az.Storage</span></span>
* <span data-ttu-id="30387-2290">Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="30387-2290">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="30387-2291">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="30387-2291">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="30387-2292">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="30387-2292">Az.AnalysisServices</span></span>
* <span data-ttu-id="30387-2293">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="30387-2293">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="30387-2294">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="30387-2294">Az.Automation</span></span>
* <span data-ttu-id="30387-2295">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="30387-2295">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="30387-2296">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="30387-2296">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="30387-2297">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="30387-2297">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="30387-2298">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="30387-2298">Az.CognitiveServices</span></span>
* <span data-ttu-id="30387-2299">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="30387-2299">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30387-2300">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30387-2300">Az.Compute</span></span>
* <span data-ttu-id="30387-2301">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="30387-2301">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="30387-2302">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="30387-2302">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="30387-2303">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="30387-2303">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="30387-2304">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="30387-2304">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="30387-2305">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="30387-2305">Az.DataLakeStore</span></span>
* <span data-ttu-id="30387-2306">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="30387-2306">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="30387-2307">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="30387-2307">Az.EventHub</span></span>
* <span data-ttu-id="30387-2308">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="30387-2308">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="30387-2309">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="30387-2309">Az.KeyVault</span></span>
* <span data-ttu-id="30387-2310">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="30387-2310">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="30387-2311">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="30387-2311">Az.LogicApp</span></span>
* <span data-ttu-id="30387-2312">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="30387-2312">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="30387-2313">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="30387-2313">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="30387-2314">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="30387-2314">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="30387-2315">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="30387-2315">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="30387-2316">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="30387-2316">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="30387-2317">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="30387-2317">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="30387-2318">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="30387-2318">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="30387-2319">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="30387-2319">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="30387-2320">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="30387-2320">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="30387-2321">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="30387-2321">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="30387-2322">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="30387-2322">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="30387-2323">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="30387-2323">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="30387-2324">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="30387-2324">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="30387-2325">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="30387-2325">Az.Monitor</span></span>
* <span data-ttu-id="30387-2326">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="30387-2326">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30387-2327">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30387-2327">Az.Network</span></span>
* <span data-ttu-id="30387-2328">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="30387-2328">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="30387-2329">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="30387-2329">Az.OperationalInsights</span></span>
* <span data-ttu-id="30387-2330">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="30387-2330">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="30387-2331">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="30387-2331">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="30387-2332">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="30387-2332">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="30387-2333">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30387-2333">Az.Resources</span></span>
* <span data-ttu-id="30387-2334">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="30387-2334">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="30387-2335">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="30387-2335">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="30387-2336">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="30387-2336">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="30387-2337">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="30387-2337">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="30387-2338">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30387-2338">Az.Sql</span></span>
* <span data-ttu-id="30387-2339">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="30387-2339">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="30387-2340">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="30387-2340">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="30387-2341">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="30387-2341">Az.Websites</span></span>
* <span data-ttu-id="30387-2342">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="30387-2342">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="30387-2343">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="30387-2343">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="30387-2344">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30387-2344">Az.Accounts</span></span>
* <span data-ttu-id="30387-2345">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="30387-2345">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="30387-2346">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="30387-2346">Az.AnalysisServices</span></span>
<span data-ttu-id="30387-2347">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="30387-2347">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30387-2348">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30387-2348">Az.Compute</span></span>
* <span data-ttu-id="30387-2349">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="30387-2349">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="30387-2350">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="30387-2350">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="30387-2351">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="30387-2351">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="30387-2352">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="30387-2352">Az.RecoveryServices</span></span>
<span data-ttu-id="30387-2353">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="30387-2353">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="30387-2354">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30387-2354">Az.Resources</span></span>
* <span data-ttu-id="30387-2355">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="30387-2355">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="30387-2356">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="30387-2356">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="30387-2357">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="30387-2357">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="30387-2358">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="30387-2358">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="30387-2359">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30387-2359">Az.Sql</span></span>
* <span data-ttu-id="30387-2360">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="30387-2360">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="30387-2361">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-2361">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="30387-2362">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="30387-2362">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="30387-2363">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="30387-2363">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="30387-2364">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30387-2364">Az.Accounts</span></span>
* <span data-ttu-id="30387-2365">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="30387-2365">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="30387-2366">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="30387-2366">Az.AnalysisServices</span></span>
* <span data-ttu-id="30387-2367">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="30387-2367">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="30387-2368">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="30387-2368">Az.RecoveryServices</span></span>
* <span data-ttu-id="30387-2369">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="30387-2369">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="30387-2370">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="30387-2370">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="30387-2371">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30387-2371">Az.Accounts</span></span>
* <span data-ttu-id="30387-2372">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="30387-2372">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="30387-2373">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="30387-2373">Update incorrect online help URLs</span></span>
* <span data-ttu-id="30387-2374">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="30387-2374">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="30387-2375">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="30387-2375">Az.Aks</span></span>
* <span data-ttu-id="30387-2376">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="30387-2376">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="30387-2377">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="30387-2377">Az.Automation</span></span>
* <span data-ttu-id="30387-2378">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="30387-2378">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="30387-2379">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="30387-2379">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="30387-2380">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="30387-2380">Az.Cdn</span></span>
* <span data-ttu-id="30387-2381">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="30387-2381">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30387-2382">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30387-2382">Az.Compute</span></span>
* <span data-ttu-id="30387-2383">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="30387-2383">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="30387-2384">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="30387-2384">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="30387-2385">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="30387-2385">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="30387-2386">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="30387-2386">Az.ContainerRegistry</span></span>
* <span data-ttu-id="30387-2387">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="30387-2387">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="30387-2388">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="30387-2388">Az.DataFactory</span></span>
* <span data-ttu-id="30387-2389">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="30387-2389">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="30387-2390">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="30387-2390">Az.DataLakeStore</span></span>
* <span data-ttu-id="30387-2391">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="30387-2391">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="30387-2392">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="30387-2392">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="30387-2393">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="30387-2393">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="30387-2394">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="30387-2394">Az.IotHub</span></span>
* <span data-ttu-id="30387-2395">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="30387-2395">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="30387-2396">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="30387-2396">Az.KeyVault</span></span>
* <span data-ttu-id="30387-2397">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="30387-2397">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30387-2398">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30387-2398">Az.Network</span></span>
* <span data-ttu-id="30387-2399">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="30387-2399">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="30387-2400">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30387-2400">Az.Resources</span></span>
* <span data-ttu-id="30387-2401">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="30387-2401">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="30387-2402">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="30387-2402">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="30387-2403">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="30387-2403">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="30387-2404">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="30387-2404">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="30387-2405">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="30387-2405">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="30387-2406">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="30387-2406">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="30387-2407">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="30387-2407">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="30387-2408">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="30387-2408">Az.ServiceFabric</span></span>
* <span data-ttu-id="30387-2409">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="30387-2409">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="30387-2410">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="30387-2410">Fix some error messages.</span></span>
* <span data-ttu-id="30387-2411">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="30387-2411">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="30387-2412">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="30387-2412">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="30387-2413">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="30387-2413">Az.SignalR</span></span>
* <span data-ttu-id="30387-2414">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="30387-2414">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="30387-2415">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30387-2415">Az.Sql</span></span>
* <span data-ttu-id="30387-2416">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="30387-2416">Update incorrect online help URLs</span></span>
* <span data-ttu-id="30387-2417">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="30387-2417">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="30387-2418">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="30387-2418">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="30387-2419">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="30387-2419">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="30387-2420">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="30387-2420">Az.Storage</span></span>
* <span data-ttu-id="30387-2421">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="30387-2421">Update incorrect online help URLs</span></span>
* <span data-ttu-id="30387-2422">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="30387-2422">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="30387-2423">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="30387-2423">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="30387-2424">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="30387-2424">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="30387-2425">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="30387-2425">Az.TrafficManager</span></span>
* <span data-ttu-id="30387-2426">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="30387-2426">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="30387-2427">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="30387-2427">Az.Websites</span></span>
* <span data-ttu-id="30387-2428">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="30387-2428">Update incorrect online help URLs</span></span>
* <span data-ttu-id="30387-2429">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="30387-2429">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="30387-2430">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="30387-2430">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="30387-2431">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="30387-2431">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="30387-2432">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30387-2432">Az.Accounts</span></span>
* <span data-ttu-id="30387-2433">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="30387-2433">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30387-2434">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30387-2434">Az.Compute</span></span>
* <span data-ttu-id="30387-2435">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="30387-2435">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="30387-2436">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="30387-2436">Updated the description of ID in help files</span></span>
* <span data-ttu-id="30387-2437">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="30387-2437">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="30387-2438">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="30387-2438">Az.DataLakeStore</span></span>
* <span data-ttu-id="30387-2439">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="30387-2439">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="30387-2440">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="30387-2440">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="30387-2441">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="30387-2441">Az.EventGrid</span></span>
* <span data-ttu-id="30387-2442">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="30387-2442">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="30387-2443">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="30387-2443">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="30387-2444">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="30387-2444">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="30387-2445">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="30387-2445">Event Time-To-Live,</span></span>
        - <span data-ttu-id="30387-2446">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="30387-2446">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="30387-2447">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="30387-2447">Dead letter endpoint.</span></span>
    - <span data-ttu-id="30387-2448">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="30387-2448">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="30387-2449">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="30387-2449">Event Time-To-Live,</span></span>
        - <span data-ttu-id="30387-2450">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="30387-2450">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="30387-2451">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="30387-2451">Dead letter endpoint.</span></span>
* <span data-ttu-id="30387-2452">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="30387-2452">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="30387-2453">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="30387-2453">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="30387-2454">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="30387-2454">Az.IotHub</span></span>
* <span data-ttu-id="30387-2455">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="30387-2455">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="30387-2456">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="30387-2456">Az.LogicApp</span></span>
* <span data-ttu-id="30387-2457">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="30387-2457">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="30387-2458">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30387-2458">Az.Resources</span></span>
* <span data-ttu-id="30387-2459">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="30387-2459">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="30387-2460">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="30387-2460">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="30387-2461">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="30387-2461">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="30387-2462">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="30387-2462">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="30387-2463">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="30387-2463">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="30387-2464">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="30387-2464">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="30387-2465">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="30387-2465">Az.SignalR</span></span>
* <span data-ttu-id="30387-2466">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="30387-2466">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="30387-2467">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30387-2467">Az.Sql</span></span>
* <span data-ttu-id="30387-2468">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="30387-2468">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="30387-2469">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="30387-2469">Az.Storage</span></span>
* <span data-ttu-id="30387-2470">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="30387-2470">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="30387-2471">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="30387-2471">New-AzStorageContext</span></span>
* <span data-ttu-id="30387-2472">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="30387-2472">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="30387-2473">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="30387-2473">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="30387-2474">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="30387-2474">Az.Websites</span></span>
* <span data-ttu-id="30387-2475">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="30387-2475">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="30387-2476">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="30387-2476">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="30387-2477">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="30387-2477">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="30387-2478">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="30387-2478">General</span></span>

- <span data-ttu-id="30387-2479">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="30387-2479">General Availability of Az Module</span></span>
- <span data-ttu-id="30387-2480">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="30387-2480">Online help for each module</span></span>
- <span data-ttu-id="30387-2481">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="30387-2481">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="30387-2482">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="30387-2482">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="30387-2483">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30387-2483">Az.Accounts</span></span>
- <span data-ttu-id="30387-2484">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="30387-2484">Changed from Az.Profile</span></span>
- <span data-ttu-id="30387-2485">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="30387-2485">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="30387-2486">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="30387-2486">Az.ApiManagement</span></span>
- <span data-ttu-id="30387-2487">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="30387-2487">Fixes for #7002</span></span>
- <span data-ttu-id="30387-2488">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="30387-2488">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="30387-2489">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="30387-2489">Az.Batch</span></span>
- <span data-ttu-id="30387-2490">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="30387-2490">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="30387-2491">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="30387-2491">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="30387-2492">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="30387-2492">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="30387-2493">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="30387-2493">Az.Billing</span></span>
- <span data-ttu-id="30387-2494">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="30387-2494">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="30387-2495">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="30387-2495">Az.CognitivServices</span></span>
- <span data-ttu-id="30387-2496">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="30387-2496">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="30387-2497">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="30387-2497">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="30387-2498">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="30387-2498">Az.ContainerInstance</span></span>
- <span data-ttu-id="30387-2499">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="30387-2499">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="30387-2500">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="30387-2500">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="30387-2501">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="30387-2501">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="30387-2502">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="30387-2502">Az.DataLakeStore</span></span>
- <span data-ttu-id="30387-2503">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="30387-2503">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="30387-2504">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="30387-2504">Az.Monitor</span></span>
- <span data-ttu-id="30387-2505">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="30387-2505">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="30387-2506">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="30387-2506">Az.KeyVault</span></span>
- <span data-ttu-id="30387-2507">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="30387-2507">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="30387-2508">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="30387-2508">Az.MachineLearning</span></span>
- <span data-ttu-id="30387-2509">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="30387-2509">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="30387-2510">Az.Media</span><span class="sxs-lookup"><span data-stu-id="30387-2510">Az.Media</span></span>
- <span data-ttu-id="30387-2511">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="30387-2511">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="30387-2512">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30387-2512">Az.Network</span></span>
<span data-ttu-id="30387-2513">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="30387-2513">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="30387-2514">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="30387-2514">New cmdlets added:</span></span>
        - <span data-ttu-id="30387-2515">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="30387-2515">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="30387-2516">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="30387-2516">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="30387-2517">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="30387-2517">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="30387-2518">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="30387-2518">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="30387-2519">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="30387-2519">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="30387-2520">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="30387-2520">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="30387-2521">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="30387-2521">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="30387-2522">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="30387-2522">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="30387-2523">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="30387-2523">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="30387-2524">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="30387-2524">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="30387-2525">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="30387-2525">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="30387-2526">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="30387-2526">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="30387-2527">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="30387-2527">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="30387-2528">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="30387-2528">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="30387-2529">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="30387-2529">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="30387-2530">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="30387-2530">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="30387-2531">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="30387-2531">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="30387-2532">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="30387-2532">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="30387-2533">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="30387-2533">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="30387-2534">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="30387-2534">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="30387-2535">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="30387-2535">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="30387-2536">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="30387-2536">Az.OperationalInsights</span></span>
- <span data-ttu-id="30387-2537">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="30387-2537">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="30387-2538">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="30387-2538">Az.Profile</span></span>
- <span data-ttu-id="30387-2539">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="30387-2539">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="30387-2540">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="30387-2540">Az.RecoveryServices</span></span>
- <span data-ttu-id="30387-2541">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="30387-2541">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="30387-2542">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30387-2542">Az.Resources</span></span>
- <span data-ttu-id="30387-2543">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="30387-2543">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="30387-2544">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="30387-2544">Az.ServiceFabric</span></span>
- <span data-ttu-id="30387-2545">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="30387-2545">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="30387-2546">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="30387-2546">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="30387-2547">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="30387-2547">Az.SIgnalR</span></span>
- <span data-ttu-id="30387-2548">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="30387-2548">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="30387-2549">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30387-2549">Az.Sql</span></span>
- <span data-ttu-id="30387-2550">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="30387-2550">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="30387-2551">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="30387-2551">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="30387-2552">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="30387-2552">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="30387-2553">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="30387-2553">Az.Storage</span></span>
- <span data-ttu-id="30387-2554">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="30387-2554">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="30387-2555">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="30387-2555">Az.Websites</span></span>
- <span data-ttu-id="30387-2556">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="30387-2556">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="30387-2557">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="30387-2557">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="30387-2558">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="30387-2558">General</span></span>

* <span data-ttu-id="30387-2559">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="30387-2559">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="30387-2560">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30387-2560">Az.Compute</span></span>

* <span data-ttu-id="30387-2561">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="30387-2561">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="30387-2562">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="30387-2562">Az.DataLakeStore</span></span>

* <span data-ttu-id="30387-2563">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="30387-2563">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="30387-2564">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="30387-2564">Az.FrontDoor</span></span>

* <span data-ttu-id="30387-2565">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="30387-2565">Fixed some broken links</span></span>
    - <span data-ttu-id="30387-2566">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="30387-2566">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="30387-2567">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="30387-2567">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="30387-2568">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="30387-2568">Az.RecoveryServices</span></span>

* <span data-ttu-id="30387-2569">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-2569">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="30387-2570">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="30387-2570">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="30387-2571">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30387-2571">Az.Resources</span></span>

* <span data-ttu-id="30387-2572">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="30387-2572">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="30387-2573">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="30387-2573">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="30387-2574">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30387-2574">Az.Sql</span></span>

* <span data-ttu-id="30387-2575">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="30387-2575">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="30387-2576">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="30387-2576">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="30387-2577">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="30387-2577">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="30387-2578">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="30387-2578">Az.Storage</span></span>

* <span data-ttu-id="30387-2579">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30387-2579">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="30387-2580">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="30387-2580">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="30387-2581">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="30387-2581">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="30387-2582">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="30387-2582">Support Static Website configuration</span></span>
    - <span data-ttu-id="30387-2583">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="30387-2583">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="30387-2584">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="30387-2584">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="30387-2585">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="30387-2585">Az.Websites</span></span>

* <span data-ttu-id="30387-2586">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="30387-2586">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="30387-2587">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="30387-2587">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="30387-2588">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-2588">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="30387-2589">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="30387-2589">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="30387-2590">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="30387-2590">Az.ApiManagement</span></span>
* <span data-ttu-id="30387-2591">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="30387-2591">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="30387-2592">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="30387-2592">Az.Automation</span></span>
* <span data-ttu-id="30387-2593">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="30387-2593">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="30387-2594">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="30387-2594">Added Update Management cmdlets</span></span>
* <span data-ttu-id="30387-2595">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="30387-2595">Added Source Control cmdlets</span></span>
* <span data-ttu-id="30387-2596">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="30387-2596">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="30387-2597">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="30387-2597">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="30387-2598">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30387-2598">Az.Compute</span></span>
* <span data-ttu-id="30387-2599">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="30387-2599">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="30387-2600">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="30387-2600">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="30387-2601">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="30387-2601">Az.ContainerInstance</span></span>
* <span data-ttu-id="30387-2602">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="30387-2602">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="30387-2603">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="30387-2603">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="30387-2604">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="30387-2604">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="30387-2605">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30387-2605">Az.Network</span></span>
* <span data-ttu-id="30387-2606">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="30387-2606">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="30387-2607">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-2607">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="30387-2608">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="30387-2608">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="30387-2609">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="30387-2609">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="30387-2610">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="30387-2610">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="30387-2611">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="30387-2611">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="30387-2612">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="30387-2612">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="30387-2613">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="30387-2613">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="30387-2614">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="30387-2614">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="30387-2615">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="30387-2615">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="30387-2616">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="30387-2616">Az.Relay</span></span>
* <span data-ttu-id="30387-2617">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="30387-2617">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="30387-2618">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30387-2618">Az.Resources</span></span>
* <span data-ttu-id="30387-2619">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="30387-2619">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="30387-2620">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="30387-2620">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="30387-2621">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="30387-2621">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="30387-2622">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="30387-2622">Az.ServiceFabric</span></span>
* <span data-ttu-id="30387-2623">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="30387-2623">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="30387-2624">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30387-2624">Az.Sql</span></span>
* <span data-ttu-id="30387-2625">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-2625">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="30387-2626">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="30387-2626">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="30387-2627">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="30387-2627">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="30387-2628">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="30387-2628">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="30387-2629">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="30387-2629">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="30387-2630">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="30387-2630">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="30387-2631">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="30387-2631">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="30387-2632">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="30387-2632">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="30387-2633">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="30387-2633">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="30387-2634">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="30387-2634">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="30387-2635">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="30387-2635">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="30387-2636">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="30387-2636">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="30387-2637">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="30387-2637">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="30387-2638">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="30387-2638">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="30387-2639">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="30387-2639">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="30387-2640">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="30387-2640">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="30387-2641">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="30387-2641">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="30387-2642">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="30387-2642">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="30387-2643">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="30387-2643">General</span></span>
* <span data-ttu-id="30387-2644">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="30387-2644">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="30387-2645">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="30387-2645">Az.Profile</span></span>
* <span data-ttu-id="30387-2646">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="30387-2646">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="30387-2647">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="30387-2647">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="30387-2648">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="30387-2648">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="30387-2649">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="30387-2649">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="30387-2650">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="30387-2650">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="30387-2651">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="30387-2651">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="30387-2652">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="30387-2652">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="30387-2653">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="30387-2653">Az.CognitiveServices</span></span>
* <span data-ttu-id="30387-2654">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="30387-2654">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30387-2655">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30387-2655">Az.Compute</span></span>
* <span data-ttu-id="30387-2656">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="30387-2656">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="30387-2657">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="30387-2657">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="30387-2658">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="30387-2658">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="30387-2659">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="30387-2659">Az.DataLakeStore</span></span>
* <span data-ttu-id="30387-2660">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="30387-2660">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="30387-2661">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="30387-2661">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="30387-2662">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="30387-2662">Az.Insights</span></span>
* <span data-ttu-id="30387-2663">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="30387-2663">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="30387-2664">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="30387-2664">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="30387-2665">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="30387-2665">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="30387-2666">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="30387-2666">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30387-2667">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30387-2667">Az.Network</span></span>
* <span data-ttu-id="30387-2668">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="30387-2668">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="30387-2669">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="30387-2669">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="30387-2670">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="30387-2670">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="30387-2671">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="30387-2671">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="30387-2672">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="30387-2672">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="30387-2673">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="30387-2673">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="30387-2674">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="30387-2674">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="30387-2675">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="30387-2675">Az.PolicyInsights</span></span>
* <span data-ttu-id="30387-2676">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="30387-2676">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="30387-2677">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30387-2677">Az.Resources</span></span>
* <span data-ttu-id="30387-2678">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="30387-2678">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="30387-2679">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="30387-2679">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="30387-2680">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="30387-2680">Az.ServiceBus</span></span>
* <span data-ttu-id="30387-2681">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="30387-2681">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="30387-2682">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="30387-2682">Az.ServiceFabric</span></span>
* <span data-ttu-id="30387-2683">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="30387-2683">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="30387-2684">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="30387-2684">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="30387-2685">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="30387-2685">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="30387-2686">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="30387-2686">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="30387-2687">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="30387-2687">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="30387-2688">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="30387-2688">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="30387-2689">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="30387-2689">Az.Profile</span></span>
* <span data-ttu-id="30387-2690">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="30387-2690">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="30387-2691">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="30387-2691">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30387-2692">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30387-2692">Az.Compute</span></span>
* <span data-ttu-id="30387-2693">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="30387-2693">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="30387-2694">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="30387-2694">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="30387-2695">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="30387-2695">Az.DataLakeStore</span></span>
* <span data-ttu-id="30387-2696">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="30387-2696">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="30387-2697">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="30387-2697">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="30387-2698">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="30387-2698">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="30387-2699">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="30387-2699">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="30387-2700">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="30387-2700">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30387-2701">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30387-2701">Az.Network</span></span>
* <span data-ttu-id="30387-2702">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="30387-2702">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="30387-2703">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="30387-2703">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="30387-2704">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30387-2704">Az.Resources</span></span>
* <span data-ttu-id="30387-2705">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="30387-2705">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="30387-2706">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="30387-2706">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="30387-2707">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="30387-2707">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="30387-2708">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="30387-2708">Azure.Storage</span></span>
* <span data-ttu-id="30387-2709">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="30387-2709">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="30387-2710">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="30387-2710">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="30387-2711">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="30387-2711">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="30387-2712">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="30387-2712">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="30387-2713">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="30387-2713">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="30387-2714">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="30387-2714">Az.CognitiveServices</span></span>
* <span data-ttu-id="30387-2715">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="30387-2715">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30387-2716">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30387-2716">Az.Compute</span></span>
* <span data-ttu-id="30387-2717">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="30387-2717">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="30387-2718">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="30387-2718">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="30387-2719">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-2719">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="30387-2720">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="30387-2720">Az.DataFactoryV2</span></span>
* <span data-ttu-id="30387-2721">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="30387-2721">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30387-2722">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30387-2722">Az.Network</span></span>
* <span data-ttu-id="30387-2723">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="30387-2723">Added NetworkProfile functionality.</span></span> <span data-ttu-id="30387-2724">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="30387-2724">new cmdlets added</span></span>
    - <span data-ttu-id="30387-2725">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="30387-2725">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="30387-2726">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="30387-2726">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="30387-2727">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="30387-2727">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="30387-2728">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="30387-2728">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="30387-2729">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="30387-2729">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="30387-2730">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="30387-2730">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="30387-2731">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="30387-2731">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="30387-2732">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="30387-2732">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="30387-2733">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="30387-2733">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="30387-2734">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="30387-2734">Az.RedisCache</span></span>
* <span data-ttu-id="30387-2735">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="30387-2735">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="30387-2736">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="30387-2736">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="30387-2737">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30387-2737">Az.Resources</span></span>
* <span data-ttu-id="30387-2738">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="30387-2738">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="30387-2739">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="30387-2739">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="30387-2740">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30387-2740">Az.Sql</span></span>
* <span data-ttu-id="30387-2741">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="30387-2741">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="30387-2742">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="30387-2742">Az.Websites</span></span>
* <span data-ttu-id="30387-2743">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="30387-2743">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="30387-2744">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="30387-2744">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="30387-2745">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="30387-2745">0.2.0 - September 2018</span></span>
 <span data-ttu-id="30387-2746">Начальный выпуск</span><span class="sxs-lookup"><span data-stu-id="30387-2746">Initial Release</span></span>