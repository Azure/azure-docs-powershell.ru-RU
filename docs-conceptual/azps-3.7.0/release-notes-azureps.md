---
title: Заметки о выпуске Azure PowerShell
description: Узнайте обо всех последних обновлениях модулей Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: 9e60e76206127922902804112e0b3f837cf03d76
ms.sourcegitcommit: eeb720e053939a68873ae3973bc81d5826358c9f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2020
ms.locfileid: "80440509"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="1b379-103">Заметки о выпуске Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="1b379-103">Azure PowerShell release notes</span></span>
## <a name="370---march-2020"></a><span data-ttu-id="1b379-104">3.7.0 — март 2020 г.</span><span class="sxs-lookup"><span data-stu-id="1b379-104">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1b379-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1b379-105">Az.Accounts</span></span>
* <span data-ttu-id="1b379-106">Исправлено исключение NullReferenceException командлетов Get-AzTenant/Get-AzDefault/Set-AzDefault, если вход не выполнен [10292]</span><span class="sxs-lookup"><span data-stu-id="1b379-106">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1b379-107">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1b379-107">Az.Compute</span></span>
* <span data-ttu-id="1b379-108">Добавлены следующие параметры к командлету New-AzDiskConfig:</span><span class="sxs-lookup"><span data-stu-id="1b379-108">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span> 
    - <span data-ttu-id="1b379-109">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="1b379-109">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="1b379-110">Разрешено свойство Encryption для параметра Target командлета New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="1b379-110">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="1b379-111">Исправлена проблема с tempDisk для командлетов Set-AzVmss -Reimage и Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="1b379-111">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="1b379-112">[11354]</span><span class="sxs-lookup"><span data-stu-id="1b379-112">[#11354]</span></span>
* <span data-ttu-id="1b379-113">Добавлена поддержка нового расширения SAP для указанных ниже командлетов</span><span class="sxs-lookup"><span data-stu-id="1b379-113">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="1b379-114">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="1b379-114">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="1b379-115">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="1b379-115">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="1b379-116">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="1b379-116">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="1b379-117">Update-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="1b379-117">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="1b379-118">Исправлены ошибки в примерах справки</span><span class="sxs-lookup"><span data-stu-id="1b379-118">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="1b379-119">Показано точное строковое значение в табличном формате для свойства PowerState виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1b379-119">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="1b379-120">New-AzVmssConfig: исправлена сериализация свойства AutomaticRepairs, если параметр SinglePlacementGroup отключен.</span><span class="sxs-lookup"><span data-stu-id="1b379-120">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="1b379-121">[11257]</span><span class="sxs-lookup"><span data-stu-id="1b379-121">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1b379-122">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1b379-122">Az.DataFactory</span></span>
* <span data-ttu-id="1b379-123">Пакет SDK ADF для .NET обновлен до версии 4.8.0.</span><span class="sxs-lookup"><span data-stu-id="1b379-123">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="1b379-124">Добавлены необязательные параметры для команды Invoke-AzDataFactoryV2Pipeline для поддержки повторного запуска.</span><span class="sxs-lookup"><span data-stu-id="1b379-124">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1b379-125">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1b379-125">Az.DataLakeStore</span></span>
* <span data-ttu-id="1b379-126">Добавлено описание критического изменения для Export-AzDataLakeStoreItem и Import-AzDataLakeStoreItem.</span><span class="sxs-lookup"><span data-stu-id="1b379-126">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="1b379-127">Добавлен параметр кодирования байтов для New-AzDataLakeStoreItem, Add-AzDAtaLakeStoreItemContent и Get-AzDAtaLakeStoreItemContent.</span><span class="sxs-lookup"><span data-stu-id="1b379-127">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="1b379-128">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1b379-128">Az.HDInsight</span></span>
* <span data-ttu-id="1b379-129">Добавлена поддержка указания минимальной поддерживаемой версии TLS при создании кластера.</span><span class="sxs-lookup"><span data-stu-id="1b379-129">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1b379-130">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1b379-130">Az.IotHub</span></span>
* <span data-ttu-id="1b379-131">Добавлена поддержка для управления распределенными параметрами на отдельных устройствах.</span><span class="sxs-lookup"><span data-stu-id="1b379-131">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="1b379-132">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="1b379-132">New Cmdlets are:</span></span>
    - <span data-ttu-id="1b379-133">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="1b379-133">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="1b379-134">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="1b379-134">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1b379-135">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1b379-135">Az.KeyVault</span></span>
* <span data-ttu-id="1b379-136">Добавлены атрибуты критических изменений для New-AzKeyVault.</span><span class="sxs-lookup"><span data-stu-id="1b379-136">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1b379-137">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1b379-137">Az.Monitor</span></span>
* <span data-ttu-id="1b379-138">Обновлена документация для New-AzScheduledQueryRuleLogMetricTrigger.</span><span class="sxs-lookup"><span data-stu-id="1b379-138">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1b379-139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1b379-139">Az.Network</span></span>
* <span data-ttu-id="1b379-140">Обновлены командлеты для поддержки подключений VirtualHubVnetConnections между клиентами</span><span class="sxs-lookup"><span data-stu-id="1b379-140">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="1b379-141">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="1b379-141">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="1b379-142">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="1b379-142">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="1b379-143">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="1b379-143">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="1b379-144">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="1b379-144">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="1b379-145">Удалена зависимость пакета SDK для управления SQL.</span><span class="sxs-lookup"><span data-stu-id="1b379-145">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="1b379-146">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="1b379-146">Az.PolicyInsights</span></span>
* <span data-ttu-id="1b379-147">Улучшены сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="1b379-147">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1b379-148">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1b379-148">Az.RecoveryServices</span></span>
* <span data-ttu-id="1b379-149">В Azure Site Recovery реализована поддержка повторной защиты и обновлены свойства зашифрованных виртуальных машин диска Azure.</span><span class="sxs-lookup"><span data-stu-id="1b379-149">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="1b379-150">Добавлена возможность мониторинг аварийного восстановления для свойств VmwareToAzure в Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="1b379-150">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="1b379-151">В Azure Backup реализована поддержка повторного обновления политики для элементов с ошибками.</span><span class="sxs-lookup"><span data-stu-id="1b379-151">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="1b379-152">В Azure Backup реализована поддержка параметров исключения диска во время резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="1b379-152">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="1b379-153">В Azure Backup реализована поддержка восстановления нескольких файлов или папок в AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="1b379-153">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="1b379-154">В Azure Backup реализована поддержка указанной пользователем группы Resourcegroup при обновлении политики IaasVM.</span><span class="sxs-lookup"><span data-stu-id="1b379-154">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="1b379-155">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1b379-155">Az.Resources</span></span>
* <span data-ttu-id="1b379-156">Исправлена команда Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType для использования фактической версии apiVersion ресурсов (а не версии apiVersion по умолчанию) [11267].</span><span class="sxs-lookup"><span data-stu-id="1b379-156">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="1b379-157">Добавлена возможность регистрации correlationId для сценариев с ошибками.</span><span class="sxs-lookup"><span data-stu-id="1b379-157">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="1b379-158">Незначительно изменена документация по Get-AzResourceLock.</span><span class="sxs-lookup"><span data-stu-id="1b379-158">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="1b379-159">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="1b379-159">Added example.</span></span>
* <span data-ttu-id="1b379-160">Экранирована одинарная кавычка в значении параметра Get-AzADUser [11317].</span><span class="sxs-lookup"><span data-stu-id="1b379-160">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="1b379-161">Добавлены новые командлеты для сценариев развертывания (Get-AzDeploymentScript, Get-AzDeploymentScriptLog, Save-AzDeploymentScriptLog, Remove-AzDeploymentScript).</span><span class="sxs-lookup"><span data-stu-id="1b379-161">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="1b379-162">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1b379-162">Az.Sql</span></span>
* <span data-ttu-id="1b379-163">Добавлен параметр вторичной реплики для чтения для командлета Invoke-AzSqlDatabaseFailover.</span><span class="sxs-lookup"><span data-stu-id="1b379-163">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="1b379-164">Добавлен командлет Disable-AzSqlServerActiveDirectoryOnlyAuthentication.</span><span class="sxs-lookup"><span data-stu-id="1b379-164">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="1b379-165">Сохранен приоритет конфиденциальности при классификации столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="1b379-165">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="1b379-166">Az.Support</span><span class="sxs-lookup"><span data-stu-id="1b379-166">Az.Support</span></span>
* <span data-ttu-id="1b379-167">Модуль Az.Support стал общедоступным.</span><span class="sxs-lookup"><span data-stu-id="1b379-167">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1b379-168">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1b379-168">Az.Websites</span></span>
* <span data-ttu-id="1b379-169">Реализована поддержка работы с правилами маршрутизации трафика веб-приложения через указанные ниже командлеты</span><span class="sxs-lookup"><span data-stu-id="1b379-169">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="1b379-170">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="1b379-170">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="1b379-171">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="1b379-171">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="1b379-172">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="1b379-172">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="1b379-173">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="1b379-173">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="1b379-174">3.6.1 — март 2020 г.</span><span class="sxs-lookup"><span data-stu-id="1b379-174">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1b379-175">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1b379-175">Az.Accounts</span></span>
* <span data-ttu-id="1b379-176">Открытие страницы опроса Azure PowerShell в Send-Feedback [11020].</span><span class="sxs-lookup"><span data-stu-id="1b379-176">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="1b379-177">Отображение URL-адреса опроса Azure PowerShell в Resolve-Error [11021].</span><span class="sxs-lookup"><span data-stu-id="1b379-177">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="1b379-178">Добавлена версия Az в UserAgent.</span><span class="sxs-lookup"><span data-stu-id="1b379-178">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="1b379-179">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1b379-179">Az.ApiManagement</span></span>
* <span data-ttu-id="1b379-180">Включена поддержка получения и настройки личного домена в конечной точке DeveloperPortal [11007].</span><span class="sxs-lookup"><span data-stu-id="1b379-180">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="1b379-181">Export-AzApiManagementApi: включена поддержка скачивания определения API в формате JSON [9987].</span><span class="sxs-lookup"><span data-stu-id="1b379-181">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="1b379-182">Import-AzApiManagementApi: включена поддержка импорта определения OpenApi 3.0 из документа JSON.</span><span class="sxs-lookup"><span data-stu-id="1b379-182">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="1b379-183">New-AzApiManagementIdentityProvider и Set-AzApiManagementIdentityProvider: включена поддержка настройки входа арендатора для поставщика AAD B2C [9784].</span><span class="sxs-lookup"><span data-stu-id="1b379-183">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1b379-184">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1b379-184">Az.DataLakeStore</span></span>
* <span data-ttu-id="1b379-185">Добавлена ссылка на System.Buffers явным образом в CSPROJ и PSD1.</span><span class="sxs-lookup"><span data-stu-id="1b379-185">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1b379-186">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1b379-186">Az.IotHub</span></span>
* <span data-ttu-id="1b379-187">Добавлена возможность управления устройствами в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="1b379-187">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="1b379-188">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="1b379-188">New Cmdlets are:</span></span>
    - <span data-ttu-id="1b379-189">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="1b379-189">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="1b379-190">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="1b379-190">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="1b379-191">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="1b379-191">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="1b379-192">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="1b379-192">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="1b379-193">Включена поддержка управления модулями в целевом устройстве Интернета вещей в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="1b379-193">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="1b379-194">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="1b379-194">New Cmdlets are:</span></span>
    - <span data-ttu-id="1b379-195">Add-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="1b379-195">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="1b379-196">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="1b379-196">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="1b379-197">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="1b379-197">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="1b379-198">Set-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="1b379-198">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="1b379-199">Добавлен командлет для получения строки подключения целевого устройства Интернета вещей в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="1b379-199">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="1b379-200">Добавлен командлет для получения строки подключения модуля на целевом устройстве Интернета вещей в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="1b379-200">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="1b379-201">Включена поддержка для получения или настройки родительского устройства для устройства Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="1b379-201">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="1b379-202">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="1b379-202">New Cmdlets are:</span></span>
    - <span data-ttu-id="1b379-203">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="1b379-203">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="1b379-204">Set-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="1b379-204">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="1b379-205">Включена поддержка управления связью "родители — потомки" устройства.</span><span class="sxs-lookup"><span data-stu-id="1b379-205">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1b379-206">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1b379-206">Az.Monitor</span></span>
* <span data-ttu-id="1b379-207">Исправлено выходное значение для Get-AzMetricDefinition [9714].</span><span class="sxs-lookup"><span data-stu-id="1b379-207">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1b379-208">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1b379-208">Az.Network</span></span>
* <span data-ttu-id="1b379-209">Обновлен пакет SDK для управления SQL.</span><span class="sxs-lookup"><span data-stu-id="1b379-209">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="1b379-210">Исправлена проблема с разницей в именовании в классе PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="1b379-210">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="1b379-211">Сопоставление ActionsRequired с ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="1b379-211">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="1b379-212">Добавление PublicNetworkAccess в команды New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="1b379-212">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="1b379-213">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1b379-213">Az.Resources</span></span>
* <span data-ttu-id="1b379-214">Исправлена ошибка пустой ссылки в Get-AzRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="1b379-214">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="1b379-215">Параметры -Force и -PassThru помечены необязательными в Remove-AzADGroup [10849].</span><span class="sxs-lookup"><span data-stu-id="1b379-215">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="1b379-216">Исправлена ошибка, из-за которой MailNickname не возвращается в Remove-AzADGroup [11167].</span><span class="sxs-lookup"><span data-stu-id="1b379-216">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="1b379-217">Исправлена ошибка, из-за которой операция канала Remove-AzADGroup не работает [11171].</span><span class="sxs-lookup"><span data-stu-id="1b379-217">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="1b379-218">Исправлена ошибка с пустой ссылкой в GetAzureRoleAssignmentCommand.</span><span class="sxs-lookup"><span data-stu-id="1b379-218">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="1b379-219">Добавлено критическое изменение атрибутов для будущих изменений командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="1b379-219">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="1b379-220">Обновлена команда Get-AzResourceGroup для выполнения фильтрации тегов группы ресурсов на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="1b379-220">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="1b379-221">Расширены командлеты Tag для включения поддержки параметра -ResourceId.</span><span class="sxs-lookup"><span data-stu-id="1b379-221">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="1b379-222">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b379-222">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="1b379-223">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b379-223">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="1b379-224">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b379-224">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="1b379-225">Добавлен новый командлет Tag.</span><span class="sxs-lookup"><span data-stu-id="1b379-225">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="1b379-226">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b379-226">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="1b379-227">Предоставляется ScopedDeployment из пакета SDK 3.3.0.</span><span class="sxs-lookup"><span data-stu-id="1b379-227">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="1b379-228">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1b379-228">Az.Sql</span></span>
* <span data-ttu-id="1b379-229">Добавление PublicNetworkAccess в команды New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="1b379-229">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="1b379-230">Включена поддержка конфигурации резервного копирования долгосрочного хранения для управляемых баз данных.</span><span class="sxs-lookup"><span data-stu-id="1b379-230">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="1b379-231">Получение или настройка политики LTR в управляемой базе данных.</span><span class="sxs-lookup"><span data-stu-id="1b379-231">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="1b379-232">Получение резервных копий LTR по управляемой базе данных, управляемому экземпляру или расположению.</span><span class="sxs-lookup"><span data-stu-id="1b379-232">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="1b379-233">Удаление резервной копии LTR.</span><span class="sxs-lookup"><span data-stu-id="1b379-233">Remove an LTR backup</span></span>
    - <span data-ttu-id="1b379-234">Восстановление резервной копии LTR для создания новой управляемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="1b379-234">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="1b379-235">Добавление MinimalTlsVersion в New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="1b379-235">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="1b379-236">Добавление MinimalTlsVersion в New-AzSqlInstance и Set-AzSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="1b379-236">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="1b379-237">Обновлена версия пакета SDK для SQL для Az.Network.</span><span class="sxs-lookup"><span data-stu-id="1b379-237">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1b379-238">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1b379-238">Az.Storage</span></span>
* <span data-ttu-id="1b379-239">Включена поддержка AllowProtectedAppendWrite в ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="1b379-239">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="1b379-240">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1b379-240">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="1b379-241">Добавлено предупреждение о критическом изменении для изменения типа AzureStorageTable в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="1b379-241">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="1b379-242">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="1b379-242">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="1b379-243">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="1b379-243">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1b379-244">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1b379-244">Az.Websites</span></span>
* <span data-ttu-id="1b379-245">Добавлен параметр Tag для New-AzAppServicePlan и Set-AzAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="1b379-245">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="1b379-246">Завершение выполнения командлета, если при добавлении личного домена на веб-сайт возникает исключение.</span><span class="sxs-lookup"><span data-stu-id="1b379-246">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="1b379-247">Включена поддержка выполнения операций для Служб приложений, которые находятся не в той же группе ресурсов, что и план службы приложений.</span><span class="sxs-lookup"><span data-stu-id="1b379-247">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="1b379-248">Применение ограничения доступа к WebApp/Function в разных группах ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1b379-248">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="1b379-249">Исправлена ошибка с указанием пользовательских имен узлов для WebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="1b379-249">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="1b379-250">3.5.0 — февраль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="1b379-250">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="1b379-251">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="1b379-251">Highlights since the last major release</span></span>
* <span data-ttu-id="1b379-252">Обновлены данные телеметрии на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="1b379-252">Updated client side telemetry.</span></span>
* <span data-ttu-id="1b379-253">В Az.IotHub добавлены командлеты для управления устройствами.</span><span class="sxs-lookup"><span data-stu-id="1b379-253">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="1b379-254">В Az.SqlVirtualMachine добавлены командлеты для прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="1b379-254">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="1b379-255">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1b379-255">Az.Accounts</span></span>
* <span data-ttu-id="1b379-256">В данные телеметрии на стороне клиента добавлены такие сведения, как идентификатор подписки, идентификатор арендатора и время выполнения.</span><span class="sxs-lookup"><span data-stu-id="1b379-256">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1b379-257">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1b379-257">Az.Automation</span></span>
* <span data-ttu-id="1b379-258">Исправлена опечатка в примере 1 в справочной документации по New-AzAutomationSoftwareUpdateConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1b379-258">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="1b379-259">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1b379-259">Az.CognitiveServices</span></span>
* <span data-ttu-id="1b379-260">Обновлен пакет SDK до версии 7.0.</span><span class="sxs-lookup"><span data-stu-id="1b379-260">Updated SDK to 7.0</span></span>
* <span data-ttu-id="1b379-261">Улучшено сообщение об ошибке, которое появляется, если ответы сервера не содержат текст.</span><span class="sxs-lookup"><span data-stu-id="1b379-261">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1b379-262">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1b379-262">Az.Compute</span></span>
* <span data-ttu-id="1b379-263">Разрешено использовать пустое значение для ProximityPlacementGroupId во время обновления.</span><span class="sxs-lookup"><span data-stu-id="1b379-263">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="1b379-264">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="1b379-264">Az.FrontDoor</span></span>
* <span data-ttu-id="1b379-265">Добавлен командлет для получения определений управляемых правил, которые могут использоваться в WAF.</span><span class="sxs-lookup"><span data-stu-id="1b379-265">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1b379-266">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1b379-266">Az.IotHub</span></span>
* <span data-ttu-id="1b379-267">Добавлена возможность управления устройствами в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="1b379-267">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="1b379-268">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="1b379-268">New Cmdlets are:</span></span>
    - <span data-ttu-id="1b379-269">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="1b379-269">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="1b379-270">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="1b379-270">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="1b379-271">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="1b379-271">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="1b379-272">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="1b379-272">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1b379-273">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1b379-273">Az.KeyVault</span></span>
* <span data-ttu-id="1b379-274">Устранен дублирующийся текст для Add-AzKeyVaultKey.md.</span><span class="sxs-lookup"><span data-stu-id="1b379-274">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1b379-275">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1b379-275">Az.Monitor</span></span>
* <span data-ttu-id="1b379-276">Исправлено описание командлета Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="1b379-276">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="1b379-277">В команду New-AzMetricAlertRuleV2 добавлен новый параметр ActionGroupId.</span><span class="sxs-lookup"><span data-stu-id="1b379-277">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="1b379-278">Пользователь может предоставить ActionGroupId(string) или ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="1b379-278">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1b379-279">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1b379-279">Az.Network</span></span>
* <span data-ttu-id="1b379-280">Добавлен еще один параметр -EnableProxyProtocol для командлета New-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="1b379-280">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="1b379-281">Исправлен пример FilterData в Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="1b379-281">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="1b379-282">Добавлен пример Packet Capture для всех внутренних и внешних пакетов в Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="1b379-282">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="1b379-283">Добавлена поддерживаемая политика Брандмауэра Azure в брандмауэрах виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="1b379-283">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="1b379-284">Новые командлеты не добавлены.</span><span class="sxs-lookup"><span data-stu-id="1b379-284">No new cmdlets are added.</span></span> <span data-ttu-id="1b379-285">Снято ограничение политики брандмауэра в брандмауэрах виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="1b379-285">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1b379-286">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1b379-286">Az.RecoveryServices</span></span>
* <span data-ttu-id="1b379-287">Добавлена возможность восстановления в виде файлов для Баз данных SQL.</span><span class="sxs-lookup"><span data-stu-id="1b379-287">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1b379-288">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1b379-288">Az.Resources</span></span>
* <span data-ttu-id="1b379-289">Выполнен рефакторинг командлетов развертывания шаблона.</span><span class="sxs-lookup"><span data-stu-id="1b379-289">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="1b379-290">Добавлены новые командлеты для управления развертываниями в группе управления: \*-AzManagementGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="1b379-290">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="1b379-291">Добавлены новые командлеты для управления развертываниями в области арендатора: \*-AzTenantDeployment.</span><span class="sxs-lookup"><span data-stu-id="1b379-291">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="1b379-292">Выполнен рефакторинг командлетов \*-AzDeployment для работы в области подписки.</span><span class="sxs-lookup"><span data-stu-id="1b379-292">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="1b379-293">Созданы псевдонимы \*-AzSubscriptionDeployment для командлетов \*-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="1b379-293">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="1b379-294">Исправлен командлет Update-AzADApplication, когда параметр AvailableToOtherTenants не задан.</span><span class="sxs-lookup"><span data-stu-id="1b379-294">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="1b379-295">Удален набор параметров ApplicationObjectWithoutCredentialParameterSet, чтобы предотвратить возникновение AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="1b379-295">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="1b379-296">Повторно созданы файлы справки.</span><span class="sxs-lookup"><span data-stu-id="1b379-296">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="1b379-297">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1b379-297">Az.Sql</span></span>
* <span data-ttu-id="1b379-298">Добавлена возможность восстановления точки во времени между подписками в Управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="1b379-298">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="1b379-299">Добавлена возможность изменения существующего поколения оборудования Управляемого экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="1b379-299">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="1b379-300">Исправлены примеры справки Update-AzSqlServerVulnerabilityAssessmentSetting: выходные данные параметра и свойства — EmailAdmins.</span><span class="sxs-lookup"><span data-stu-id="1b379-300">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="1b379-301">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="1b379-301">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="1b379-302">Добавлены командлеты для прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="1b379-302">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="1b379-303">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="1b379-303">Az.StorageSync</span></span>
* <span data-ttu-id="1b379-304">В командлете Invoke-AzStorageSyncCompatibilityCheck обновлены поддерживаемые наборы символов.</span><span class="sxs-lookup"><span data-stu-id="1b379-304">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="1b379-305">3.4.0 — февраль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="1b379-305">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="1b379-306">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="1b379-306">Highlights since the last major release</span></span>
* <span data-ttu-id="1b379-307">Выпущена первоначальная версия 0.1.0 Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="1b379-307">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="1b379-308">Добавлена поддержка Az.Network ConnectionMonitor V2</span><span class="sxs-lookup"><span data-stu-id="1b379-308">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="1b379-309">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1b379-309">Az.Accounts</span></span>
* <span data-ttu-id="1b379-310">Отключить автоматическое сохранение контекста, если AzureRmContext.json недоступен</span><span class="sxs-lookup"><span data-stu-id="1b379-310">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="1b379-311">Обновление ссылки на Azure Powershell Common до предварительной версии 1.3.5</span><span class="sxs-lookup"><span data-stu-id="1b379-311">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="1b379-312">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1b379-312">Az.ApiManagement</span></span>
* <span data-ttu-id="1b379-313">**Get-AzApiManagementApiSchema** Исправлено получение схемы Open-API, связанной с API https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="1b379-313">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="1b379-314">**New-AzApiManagementProduct**\* и **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="1b379-314">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="1b379-315">Исправить документацию для https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="1b379-315">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="1b379-316">**Set-AzApiManagementApi** Добавлен пример, показывающий, как обновить ServiceUrl с помощью командлета</span><span class="sxs-lookup"><span data-stu-id="1b379-316">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1b379-317">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1b379-317">Az.Compute</span></span>
* <span data-ttu-id="1b379-318">Ограничение числа состояний виртуальных машин до 100, чтобы избежать регулирования при выполнении Get-AzVM-Status без имени виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1b379-318">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="1b379-319">Добавление обновления командлета -AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="1b379-319">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="1b379-320">Добавление параметров EncryptionType и DiskEncryptionSetId в следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="1b379-320">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="1b379-321">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="1b379-321">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="1b379-322">Добавление параметра ColocationStatus в командлет Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="1b379-322">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1b379-323">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1b379-323">Az.DataFactory</span></span>
* <span data-ttu-id="1b379-324">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.7.0.</span><span class="sxs-lookup"><span data-stu-id="1b379-324">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="1b379-325">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="1b379-325">Az.DeploymentManager</span></span>
* <span data-ttu-id="1b379-326">Добавляет операции LIST для ресурсов</span><span class="sxs-lookup"><span data-stu-id="1b379-326">Adds LIST operations for resources</span></span>
* <span data-ttu-id="1b379-327">Добавляет возможность выполнения операций на этапах Проверки работоспособности</span><span class="sxs-lookup"><span data-stu-id="1b379-327">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="1b379-328">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1b379-328">Az.HDInsight</span></span>
* <span data-ttu-id="1b379-329">Исправление ошибки в документе New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="1b379-329">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1b379-330">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1b379-330">Az.KeyVault</span></span>
* <span data-ttu-id="1b379-331">Добавление Псевдонимов имени в атрибут VaultName, чтобы Remove-AzureKeyVault соответствовал New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="1b379-331">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1b379-332">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1b379-332">Az.Network</span></span>
* <span data-ttu-id="1b379-333">В Set-AzNetworkWatcherConfigFlowLog.md добавлен новый пример для демонстрации сценария отключения Аналитики трафика.</span><span class="sxs-lookup"><span data-stu-id="1b379-333">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="1b379-334">Добавление поддержки назначения IP-конфигурации для брандмауэра Azure — выделенная подсеть и общедоступный IP-адрес, которые брандмауэр будет использовать для управления трафиком</span><span class="sxs-lookup"><span data-stu-id="1b379-334">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="1b379-335">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="1b379-335">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="1b379-336">добавлен параметр — ManagementPublicIpAddress (необязательный), который принимает объект общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="1b379-336">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="1b379-337">Добавлен метод SetManagementIpConfiguration для объекта брандмауэра — в качестве входных данных требуется подсеть и общедоступный IP-адрес — имя подсети должно быть "AzureFirewallManagementSubnet"</span><span class="sxs-lookup"><span data-stu-id="1b379-337">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="1b379-338">Исправлены примеры Get-AzNetworkSecurityGroup для отображения примеров для группы безопасности сети (NSG) вместо сетевых интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="1b379-338">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="1b379-339">Исправлена опечатка в команде New-AzVpnSite, которая препятствовала завершению параметра идентификатором ресурса.</span><span class="sxs-lookup"><span data-stu-id="1b379-339">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="1b379-340">Добавлена поддержка конфигурации в наборе действий для правил подстановки URL-адресов в шлюзе приложения.</span><span class="sxs-lookup"><span data-stu-id="1b379-340">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="1b379-341">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="1b379-341">New cmdlets added:</span></span>
        - <span data-ttu-id="1b379-342">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b379-342">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="1b379-343">В следующие командлеты добавлен необязательный параметр — UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b379-343">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="1b379-344">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="1b379-344">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="1b379-345">Добавление поддержки для ресурсов NetworkWatcher ConnectionMonitor версии 2</span><span class="sxs-lookup"><span data-stu-id="1b379-345">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="1b379-346">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="1b379-346">Az.PolicyInsights</span></span>
* <span data-ttu-id="1b379-347">Поддержка оценки соответствия до определения того, какой ресурс нужно исправить</span><span class="sxs-lookup"><span data-stu-id="1b379-347">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="1b379-348">Добавление параметра "—ResourceDiscoverMode" в Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="1b379-348">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="1b379-349">Добавление командлета Get-AzPolicyMetadata для получения ресурсов метаданных политики</span><span class="sxs-lookup"><span data-stu-id="1b379-349">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="1b379-350">Get-AzPolicyState и Get-AzPolicyStateSummary обновлены для API версии 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="1b379-350">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1b379-351">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1b379-351">Az.RecoveryServices</span></span>
* <span data-ttu-id="1b379-352">Поддержка Azure Site Recovery для удаления реплицированного диска.</span><span class="sxs-lookup"><span data-stu-id="1b379-352">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="1b379-353">В Azure Backup добавлена ​​поддержка добавления тегов при создании Хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="1b379-353">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1b379-354">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1b379-354">Az.Resources</span></span>
* <span data-ttu-id="1b379-355">Сделайте команду "Область" необязательной в командлетах \*—AzPolicyAssignment с настройкой по умолчанию для контекстной подписки</span><span class="sxs-lookup"><span data-stu-id="1b379-355">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="1b379-356">Добавление примеров создания ADServicePrincipal с паролем и ключом учетных данных</span><span class="sxs-lookup"><span data-stu-id="1b379-356">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="1b379-357">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1b379-357">Az.Sql</span></span>
<span data-ttu-id="1b379-358">Исправление командлета New-AzSqlDatabaseSecondary, чтобы проверить существование PartnerDatabaseName, а не DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="1b379-358">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1b379-359">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1b379-359">Az.Storage</span></span>
* <span data-ttu-id="1b379-360">Поддержка набора шифрования типа ключа таблиц и очередей в создании учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="1b379-360">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="1b379-361">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1b379-361">New-AzStorageAccount</span></span>
* <span data-ttu-id="1b379-362">Представление RequestId, если StorageException не имеет ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="1b379-362">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="1b379-363">Исправление примера 6 командлета Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="1b379-363">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1b379-364">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1b379-364">Az.Websites</span></span>
* <span data-ttu-id="1b379-365">Set-AzWebapp и Set-AzWebappSlot поддерживают свойства AlwaysOn, MinTls и FtpsState</span><span class="sxs-lookup"><span data-stu-id="1b379-365">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="1b379-366">Устранение проблемы, при которой параметр HttpsOnly с одновременным изменением AppservicePlan с помощью одной команды Set-AzWebApp сбрасывал значение HttpsOnly до значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="1b379-366">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="1b379-367">3.3.0 — январь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="1b379-367">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1b379-368">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1b379-368">Az.Accounts</span></span>
* <span data-ttu-id="1b379-369">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment: теперь они принимают параметры AzureAttestationServiceEndpointResourceId и AzureAttestationServiceEndpointSuffix.</span><span class="sxs-lookup"><span data-stu-id="1b379-369">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="1b379-370">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="1b379-370">Az.Cdn</span></span>
* <span data-ttu-id="1b379-371">Теперь в командлете New-AzCdnEndpoint отображаются сведения из сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="1b379-371">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1b379-372">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1b379-372">Az.Compute</span></span>
* <span data-ttu-id="1b379-373">Командлет Set-AzVMCustomScriptExtension исправлен для виртуальной машины с управляемым диском ОС без профиля ОС.</span><span class="sxs-lookup"><span data-stu-id="1b379-373">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="1b379-374">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="1b379-374">Az.ContainerInstance</span></span>
* <span data-ttu-id="1b379-375">Исправлены имена параметров, используемые в примере командлета New-AzContainerGroup.</span><span class="sxs-lookup"><span data-stu-id="1b379-375">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="1b379-376">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="1b379-376">Az.DataBoxEdge</span></span>
* <span data-ttu-id="1b379-377">Добавлен командлет Get-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="1b379-377">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="1b379-378">получение контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="1b379-378">Get the Edge Storage Container</span></span>
* <span data-ttu-id="1b379-379">Добавлен командлет New-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="1b379-379">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="1b379-380">создание контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="1b379-380">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="1b379-381">Добавлен командлет Remove-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="1b379-381">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="1b379-382">удаление контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="1b379-382">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="1b379-383">Добавлен командлет Invoke-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="1b379-383">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="1b379-384">вызов действия для обновления данных в контейнере хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="1b379-384">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="1b379-385">Добавлен командлет Get-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="1b379-385">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="1b379-386">получение учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="1b379-386">Get the Edge Storage Account</span></span>
* <span data-ttu-id="1b379-387">Добавлен командлет New-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="1b379-387">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="1b379-388">создание учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="1b379-388">Create new Edge Storage Account</span></span>
* <span data-ttu-id="1b379-389">Добавлен командлет Remove-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="1b379-389">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="1b379-390">удаление учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="1b379-390">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="1b379-391">Вызов командлета Invoke-AzDataBoxEdgeShare:</span><span class="sxs-lookup"><span data-stu-id="1b379-391">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="1b379-392">вызов действия для обновления данных в общей папке.</span><span class="sxs-lookup"><span data-stu-id="1b379-392">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="1b379-393">Добавлен командлет Set-AzDataBoxEdgeStorageAccountCredential:</span><span class="sxs-lookup"><span data-stu-id="1b379-393">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="1b379-394">установка учетных данных для учетной записи хранилища Azure Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="1b379-394">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1b379-395">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1b379-395">Az.DataFactory</span></span>
* <span data-ttu-id="1b379-396">Добавлены свойства AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId и VersionStatus для командлета Get-AzDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="1b379-396">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="1b379-397">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.6.0.</span><span class="sxs-lookup"><span data-stu-id="1b379-397">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="1b379-398">Для командлета Set-AzureRmDataFactoryV2IntegrationRuntime добавлен параметр PublicIPs, позволяющий включить создание среды Azure-SSIS IR со статическими общедоступными IP-адресами.</span><span class="sxs-lookup"><span data-stu-id="1b379-398">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="1b379-399">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="1b379-399">Az.DevTestLabs</span></span>
* <span data-ttu-id="1b379-400">Удалена недействительная ссылка в файле Get-AzDtlAllowedVMSizesPolicy.md.</span><span class="sxs-lookup"><span data-stu-id="1b379-400">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="1b379-401">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="1b379-401">Az.EventHub</span></span>
* <span data-ttu-id="1b379-402">Устранена проблема № 10634: исправлена ссылка на пустой объект для удаления пространства имен концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="1b379-402">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="1b379-403">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1b379-403">Az.HDInsight</span></span>
* <span data-ttu-id="1b379-404">Устранена ошибка в файле Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="1b379-404">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="1b379-405">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="1b379-405">Az.MachineLearning</span></span>
* <span data-ttu-id="1b379-406">Вычислительная среда Машинного обучения больше недоступна, поэтому удалены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="1b379-406">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="1b379-407">Get-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="1b379-407">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="1b379-408">Get-AzMlOpClusterKey;</span><span class="sxs-lookup"><span data-stu-id="1b379-408">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="1b379-409">New-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="1b379-409">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="1b379-410">Remove-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="1b379-410">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="1b379-411">Set-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="1b379-411">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="1b379-412">Test-AzMlOpClusterSystemServicesUpdateAvailability;</span><span class="sxs-lookup"><span data-stu-id="1b379-412">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="1b379-413">Update-AzMlOpClusterSystemService.</span><span class="sxs-lookup"><span data-stu-id="1b379-413">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1b379-414">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1b379-414">Az.Network</span></span>
* <span data-ttu-id="1b379-415">Обновлена зависимость Microsoft.Azure.Management.Sql от предварительной версии 1.36 до предварительной версии 1.37.</span><span class="sxs-lookup"><span data-stu-id="1b379-415">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1b379-416">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1b379-416">Az.RecoveryServices</span></span>
* <span data-ttu-id="1b379-417">Добавлена поддержка Azure Site Recovery для виртуальных машин с управляемым диском, зашифрованных при хранении с помощью управляемых клиентом ключей, при восстановлении из Azure в поставщике Azure.</span><span class="sxs-lookup"><span data-stu-id="1b379-417">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="1b379-418">Добавлена поддержка Azure Site Recovery для необязательного ввода идентификатора набора шифрования диска при включении защиты в рамках восстановления из VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="1b379-418">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="1b379-419">Добавлена поддержка Azure Site Recovery для необязательного ввода идентификатора набора шифрования диска на уровне диска при включении защиты в рамках восстановления из VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="1b379-419">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="1b379-420">Добавлена поддержка Azure Site Recovery для обновления элемента, защищенного репликацией, путем сопоставления набора шифрования диска при восстановлении из HyperV в Azure.</span><span class="sxs-lookup"><span data-stu-id="1b379-420">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1b379-421">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1b379-421">Az.Resources</span></span>
* <span data-ttu-id="1b379-422">Исправлена ошибка в справочном документе о командлете Remove-AzTag.</span><span class="sxs-lookup"><span data-stu-id="1b379-422">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="1b379-423">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1b379-423">Az.Sql</span></span>
* <span data-ttu-id="1b379-424">Исправлена функция основных командлетов установки оценки уязвимостей: теперь она позволяет работать с базой данных master для базы данных Azure и ограничить ее в системных базах данных управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="1b379-424">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="1b379-425">Устранена ошибка, возникающая при создании группы отработки отказа экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="1b379-425">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="1b379-426">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="1b379-426">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="1b379-427">Добавлен новый допустимый тип лицензии: DR (аварийное восстановление).</span><span class="sxs-lookup"><span data-stu-id="1b379-427">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1b379-428">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1b379-428">Az.Storage</span></span>
* <span data-ttu-id="1b379-429">Добавлено предупреждающее сообщение о критическом изменении значения DefaultAction в следующем выпуске:</span><span class="sxs-lookup"><span data-stu-id="1b379-429">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="1b379-430">Update-AzStorageAccountNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="1b379-430">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="1b379-431">Включена поддержка получения времени последней синхронизации учетной записи хранения путем выполнения командлета Get-AzureRmStorageAccount с параметром -IncludeGeoReplicationStats:</span><span class="sxs-lookup"><span data-stu-id="1b379-431">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="1b379-432">Get-AzureRmStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="1b379-432">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="1b379-433">3.2.0 — декабрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="1b379-433">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="1b379-434">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="1b379-434">General</span></span>
* <span data-ttu-id="1b379-435">Обновление ссылок в .psd1 для использования относительного пути для всех модулей.</span><span class="sxs-lookup"><span data-stu-id="1b379-435">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="1b379-436">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1b379-436">Az.Accounts</span></span>
* <span data-ttu-id="1b379-437">Установка правильного параметра UserAgent для телеметрии на стороне клиента для Az 4.0 (предварительная версия).</span><span class="sxs-lookup"><span data-stu-id="1b379-437">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="1b379-438">Отображение понятного пользователю сообщения об ошибке, если в Az 4.0 (предварительная версия) не указан контекст.</span><span class="sxs-lookup"><span data-stu-id="1b379-438">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="1b379-439">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="1b379-439">Az.Batch</span></span>
* <span data-ttu-id="1b379-440">Исправлена проблема [№ 10602](https://github.com/Azure/azure-powershell/issues/10602), из-за которой использование командлета **New-AzBatchPool** приводило к неправильной отправке VirtualMachineConfiguration.ContainerConfiguration или VirtualMachineConfiguration.DataDisks на сервер.</span><span class="sxs-lookup"><span data-stu-id="1b379-440">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1b379-441">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1b379-441">Az.DataFactory</span></span>
* <span data-ttu-id="1b379-442">Обновление пакета SDK Фабрики данных для .NET до версии 4.5.0.</span><span class="sxs-lookup"><span data-stu-id="1b379-442">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="1b379-443">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="1b379-443">Az.FrontDoor</span></span>
* <span data-ttu-id="1b379-444">Включена поддержка исключений управляемых правил WAF.</span><span class="sxs-lookup"><span data-stu-id="1b379-444">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="1b379-445">Добавление SocketAddr в список автозавершения.</span><span class="sxs-lookup"><span data-stu-id="1b379-445">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="1b379-446">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="1b379-446">Az.HealthcareApis</span></span>
* <span data-ttu-id="1b379-447">Обработка исключений.</span><span class="sxs-lookup"><span data-stu-id="1b379-447">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1b379-448">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1b379-448">Az.KeyVault</span></span>
* <span data-ttu-id="1b379-449">Исправлена ошибка при получении доступа к значению, которое может быть не задано.</span><span class="sxs-lookup"><span data-stu-id="1b379-449">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="1b379-450">Управление сертификатами шифрования на основе эллиптических кривых.</span><span class="sxs-lookup"><span data-stu-id="1b379-450">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="1b379-451">Включена возможность указания кривой для политик сертификатов.</span><span class="sxs-lookup"><span data-stu-id="1b379-451">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1b379-452">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1b379-452">Az.Monitor</span></span>
* <span data-ttu-id="1b379-453">Добавление необязательного аргумента в команду добавления параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="1b379-453">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="1b379-454">Существующий аргумент switch указывает на то, что экспорт в Log Analytics должен выполняться в фиксированную схему</span><span class="sxs-lookup"><span data-stu-id="1b379-454">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="1b379-455">(выделенный тип данных).</span><span class="sxs-lookup"><span data-stu-id="1b379-455">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1b379-456">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1b379-456">Az.Network</span></span>
* <span data-ttu-id="1b379-457">В приложении AzureFirewall, NAT и сетевых правилах включена поддержка IpGroups.</span><span class="sxs-lookup"><span data-stu-id="1b379-457">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1b379-458">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1b379-458">Az.Resources</span></span>
* <span data-ttu-id="1b379-459">Устранена проблема, из-за которой при развертывании шаблона не удавалось считать его параметр, если имя параметра конфликтовало с именем встроенного параметра.</span><span class="sxs-lookup"><span data-stu-id="1b379-459">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="1b379-460">Обновлены командлеты политики для использования новой версии API 2019-09-01 с поддержкой группирования в определениях наборов политик.</span><span class="sxs-lookup"><span data-stu-id="1b379-460">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="1b379-461">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1b379-461">Az.Sql</span></span>
* <span data-ttu-id="1b379-462">Обновлена функция автоматического создания расширенного хранилища для службы оценки уязвимостей в учетной записи StorageV2.</span><span class="sxs-lookup"><span data-stu-id="1b379-462">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1b379-463">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1b379-463">Az.Storage</span></span>
* <span data-ttu-id="1b379-464">Включена поддержка создания маркера SAS на основе удостоверения контейнера и большого двоичного объекта с аутентификацией Oauth на основе контекста службы хранилища:</span><span class="sxs-lookup"><span data-stu-id="1b379-464">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="1b379-465">New-AzStorageContainerSASToken;</span><span class="sxs-lookup"><span data-stu-id="1b379-465">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="1b379-466">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="1b379-466">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="1b379-467">Отозвана поддержка ключей делегирования пользователя учетной записи хранения, а также всех маркеров SAS удостоверения:</span><span class="sxs-lookup"><span data-stu-id="1b379-467">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="1b379-468">Revoke-AzStorageAccountUserDelegationKeys.</span><span class="sxs-lookup"><span data-stu-id="1b379-468">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="1b379-469">Выполнено обновление до Microsoft.Azure.Management.Storage версии 14.2.0 для включения поддержки нового API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="1b379-469">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="1b379-470">Включена поддержка QuotaGiB (квота общего ресурса в ГиБ) для значений свыше 5120 в командлетах для работы с общими папками в плоскости управления и добавлен псевдоним Quota для параметра QuotaGiB.</span><span class="sxs-lookup"><span data-stu-id="1b379-470">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="1b379-471">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="1b379-471">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="1b379-472">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="1b379-472">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="1b379-473">Добавлен псевдоним QuotaGiB для параметра Quota:</span><span class="sxs-lookup"><span data-stu-id="1b379-473">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="1b379-474">Set-AzStorageShareQuota.</span><span class="sxs-lookup"><span data-stu-id="1b379-474">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="1b379-475">Устранена проблема, из-за которой при использовании AzStorageContainerAcl могла очищаться хранимая политика доступа:</span><span class="sxs-lookup"><span data-stu-id="1b379-475">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="1b379-476">Set-AzStorageContainerAcl.</span><span class="sxs-lookup"><span data-stu-id="1b379-476">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="1b379-477">Версия 3.1.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="1b379-477">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="1b379-478">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="1b379-478">Highlights since the last major release</span></span>
* <span data-ttu-id="1b379-479">Выпуск Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="1b379-479">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="1b379-480">Выпуск Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="1b379-480">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1b379-481">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1b379-481">Az.Compute</span></span>
* <span data-ttu-id="1b379-482">Функция повторного применения виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="1b379-482">VM Reapply feature</span></span>
    - <span data-ttu-id="1b379-483">Добавлен параметр повторного применения в командлет Set-AzVM.</span><span class="sxs-lookup"><span data-stu-id="1b379-483">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="1b379-484">Функция AutomaticRepairs масштабируемого набора виртуальных машин:</span><span class="sxs-lookup"><span data-stu-id="1b379-484">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="1b379-485">Добавлены параметры EnableAutomaticRepair, AutomaticRepairGracePeriod и AutomaticRepairMaxInstanceRepairsPercent в следующие командлеты:   New-AzVmssConfig Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="1b379-485">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="1b379-486">Включена поддержка образа из коллекции разных клиентов для New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="1b379-486">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="1b379-487">Добавлен фрагмент Spot в средство заполнения аргументов параметра Priority в командлетах New-AzVM, New-AzVMConfig и New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="1b379-487">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="1b379-488">Добавлены параметры DiskIOPSReadWrite и DiskMBpsReadWrite в командлет Add-AzVmssDataDisk.</span><span class="sxs-lookup"><span data-stu-id="1b379-488">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="1b379-489">Изменен параметр SourceImageId командлета New-AzGalleryImageVersion на необязательный.</span><span class="sxs-lookup"><span data-stu-id="1b379-489">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="1b379-490">Добавлены параметры OSDiskImage и DataDiskImage в командлет New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="1b379-490">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="1b379-491">Добавлен параметр HyperVGeneration в командлет New-AzGalleryImageDefinition.</span><span class="sxs-lookup"><span data-stu-id="1b379-491">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="1b379-492">Добавлены параметры SkipExtensionsOnOverprovisionedVMs в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="1b379-492">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="1b379-493">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="1b379-493">Az.DataBoxEdge</span></span>
* <span data-ttu-id="1b379-494">Добавлен командлет `Get-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="1b379-494">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="1b379-495">Получение заказа.</span><span class="sxs-lookup"><span data-stu-id="1b379-495">Get the Order</span></span>
* <span data-ttu-id="1b379-496">Добавлен командлет `New-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="1b379-496">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="1b379-497">Создание заказа.</span><span class="sxs-lookup"><span data-stu-id="1b379-497">Create new Order</span></span>
* <span data-ttu-id="1b379-498">Добавлен командлет `Remove-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="1b379-498">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="1b379-499">Удаление заказа.</span><span class="sxs-lookup"><span data-stu-id="1b379-499">Remove the Order</span></span>
* <span data-ttu-id="1b379-500">Изменен командлет `New-AzDataBoxEdgeShare`.</span><span class="sxs-lookup"><span data-stu-id="1b379-500">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="1b379-501">Создание локальной общей папки.</span><span class="sxs-lookup"><span data-stu-id="1b379-501">Now creates Local Share</span></span>
* <span data-ttu-id="1b379-502">Добавлен командлет `Set-AzDataBoxEdgeRole`.</span><span class="sxs-lookup"><span data-stu-id="1b379-502">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="1b379-503">Сопоставление IotRole с общей папкой.</span><span class="sxs-lookup"><span data-stu-id="1b379-503">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="1b379-504">Добавлен командлет `Invoke-AzDataBoxEdgeDevice`.</span><span class="sxs-lookup"><span data-stu-id="1b379-504">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="1b379-505">Вызов проверки обновлений, скачивание обновления, установка обновления на устройстве.</span><span class="sxs-lookup"><span data-stu-id="1b379-505">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="1b379-506">Добавлен командлет `Get-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="1b379-506">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="1b379-507">Получение сведений о триггерах.</span><span class="sxs-lookup"><span data-stu-id="1b379-507">Gets the information about Triggers</span></span>
* <span data-ttu-id="1b379-508">Добавлен командлет `New-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="1b379-508">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="1b379-509">Создание триггеров.</span><span class="sxs-lookup"><span data-stu-id="1b379-509">Create new Triggers</span></span>
* <span data-ttu-id="1b379-510">Добавлен командлет `Remove-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="1b379-510">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="1b379-511">Удаление триггеров.</span><span class="sxs-lookup"><span data-stu-id="1b379-511">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1b379-512">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1b379-512">Az.DataFactory</span></span>
* <span data-ttu-id="1b379-513">Обновление пакета SDK Фабрики данных для .NET до версии 4.4.0.</span><span class="sxs-lookup"><span data-stu-id="1b379-513">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="1b379-514">Добавлен параметр ExpressCustomSetup в командлет Set-AzureRmDataFactoryV2IntegrationRuntime для включения конфигураций установки и сторонних компонентов без использования настраиваемого скрипта установки.</span><span class="sxs-lookup"><span data-stu-id="1b379-514">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1b379-515">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1b379-515">Az.DataLakeStore</span></span>
* <span data-ttu-id="1b379-516">Обновлена документация по Get-AzDataLakeStoreDeletedItem и Restore-AzDataLakeStoreDeletedItem.</span><span class="sxs-lookup"><span data-stu-id="1b379-516">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="1b379-517">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="1b379-517">Az.EventHub</span></span>
* <span data-ttu-id="1b379-518">Исправлена проблема № 10301. Исправлен формат даты маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="1b379-518">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="1b379-519">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="1b379-519">Az.FrontDoor</span></span>
* <span data-ttu-id="1b379-520">Добавлен параметр MinimumTlsVersion в Enable-AzFrontDoorCustomDomainHttps и New-AzFrontDoorFrontendEndpointObject.</span><span class="sxs-lookup"><span data-stu-id="1b379-520">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="1b379-521">Добавлены параметры HealthProbeMethod и EnabledState в New-AzFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="1b379-521">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="1b379-522">Добавлен новый командлет для создания объекта BackendPoolsSettings для передачи при создании и обновлении Front Door.</span><span class="sxs-lookup"><span data-stu-id="1b379-522">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="1b379-523">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="1b379-523">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1b379-524">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1b379-524">Az.Network</span></span>
* <span data-ttu-id="1b379-525">Изменены примеры параметра FilterData Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="1b379-525">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="1b379-526">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="1b379-526">Az.PrivateDns</span></span>
* <span data-ttu-id="1b379-527">Пакет SDK PrivateDns для .NET обновлен до версии 1.0.0</span><span class="sxs-lookup"><span data-stu-id="1b379-527">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1b379-528">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1b379-528">Az.RecoveryServices</span></span>
* <span data-ttu-id="1b379-529">Включена поддержка Azure Site Recovery для выбора типа диска при включении защиты.</span><span class="sxs-lookup"><span data-stu-id="1b379-529">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="1b379-530">Внесено исправление Azure Site Recovery для изменения действия плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="1b379-530">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="1b379-531">Включена поддержка восстановления SQL Azure Backup для принятия баз данных файлового потока.</span><span class="sxs-lookup"><span data-stu-id="1b379-531">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="1b379-532">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="1b379-532">Az.RedisCache</span></span>
* <span data-ttu-id="1b379-533">Добавлен параметр MinimumTlsVersion в командлеты New-AzRedisCache и Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="1b379-533">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="1b379-534">Кроме того, добавлен параметр MinimumTlsVersion в выходные данные командлета Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="1b379-534">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="1b379-535">Добавлена проверка параметра -Size для командлетов Set-AzRedisCache и New-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="1b379-535">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="1b379-536">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1b379-536">Az.Resources</span></span>
- <span data-ttu-id="1b379-537">Обновлены командлеты политики для использования новой версии API 2019-06-01 с новым свойством EnforcementMode в назначении политики.</span><span class="sxs-lookup"><span data-stu-id="1b379-537">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="1b379-538">Обновлен пример справки по созданию определения политики</span><span class="sxs-lookup"><span data-stu-id="1b379-538">Updated create policy definition help example</span></span>
- <span data-ttu-id="1b379-539">Исправлена ошибка с параметром -ServicePrincipalName командлета Remove-AZADServicePrincipal с возвратом пустой ссылки, если имя субъекта службы не найдено.</span><span class="sxs-lookup"><span data-stu-id="1b379-539">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="1b379-540">Исправлена ошибка с New-AZADServicePrincipal с возвратом пустой ссылки, если у клиента нет подписки.</span><span class="sxs-lookup"><span data-stu-id="1b379-540">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="1b379-541">Изменен командлет New-AzAdServicePrincipal для добавления учетных данных только для связанного приложения.</span><span class="sxs-lookup"><span data-stu-id="1b379-541">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="1b379-542">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1b379-542">Az.Sql</span></span>
* <span data-ttu-id="1b379-543">Добавлена поддержка ReadReplicaCount для базы данных.</span><span class="sxs-lookup"><span data-stu-id="1b379-543">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="1b379-544">Исправлена ошибка с Set-AzSqlDatabase, если избыточность в пределах зоны не настроена.</span><span class="sxs-lookup"><span data-stu-id="1b379-544">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="1b379-545">Версия 3.0.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="1b379-545">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="1b379-546">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="1b379-546">General</span></span>
* <span data-ttu-id="1b379-547">Выпущена версия Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="1b379-547">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="1b379-548">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1b379-548">Az.Accounts</span></span>
* <span data-ttu-id="1b379-549">Добавлено сообщение об устаревании для псевдонима "Resolve-Error".</span><span class="sxs-lookup"><span data-stu-id="1b379-549">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="1b379-550">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="1b379-550">Az.Advisor</span></span>
* <span data-ttu-id="1b379-551">Добавлена новая категория Operational Excellence (Эффективность работы) в командлет Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="1b379-551">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="1b379-552">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="1b379-552">Az.Batch</span></span>
* <span data-ttu-id="1b379-553">`CoreQuota` в `BatchAccountContext` переименован в `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="1b379-553">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="1b379-554">Также появился новый `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="1b379-554">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="1b379-555">Это влияет на **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="1b379-555">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="1b379-556">Параметр **New-AzBatchTask** `-ResourceFile` теперь принимает коллекцию объектов `PSResourceFile`, которые можно создать с помощью нового командлета **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="1b379-556">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="1b379-557">Новый командлет **New-AzBatchResourceFile**, который помогает создавать объекты `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="1b379-557">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="1b379-558">Их можно передавать в **New-AzBatchTask** в параметре `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="1b379-558">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="1b379-559">Это позволяет поддерживать два новых типа файлов ресурсов, которые дополняют существующий метод `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="1b379-559">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="1b379-560">Файлы ресурсов на основе `AutoStorageContainerName` скачивают весь контейнер автоматического хранения в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="1b379-560">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="1b379-561">Файлы ресурсов на основе `StorageContainerUrl` скачивают указанный в URL-адресе контейнер в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="1b379-561">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="1b379-562">Удалено свойство `ApplicationPackages` в `PSApplication`, который возвращается из **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="1b379-562">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="1b379-563">Отдельные пакеты в приложении теперь можно извлечь с помощью **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="1b379-563">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="1b379-564">Например: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="1b379-564">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="1b379-565">`ApplicationId` переименован в `ApplicationName` для **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** и **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="1b379-565">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="1b379-566">Теперь `ApplicationId` является псевдонимом для `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="1b379-566">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="1b379-567">Добавлено новое свойство `PSWindowsUserConfiguration` в `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="1b379-567">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="1b379-568">`Version` переименован в `Name` для `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="1b379-568">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="1b379-569">`BlobSource` переименован в `HttpUrl` для `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="1b379-569">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="1b379-570">Удалено свойство `OSDisk` из `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="1b379-570">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="1b379-571">Удалена операция **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="1b379-571">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="1b379-572">Больше она не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1b379-572">This operation is no longer supported.</span></span>
* <span data-ttu-id="1b379-573">Удалено `TargetOSVersion` из `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="1b379-573">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="1b379-574">`CurrentOSVersion` переименован в `OSVersion` для `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="1b379-574">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="1b379-575">Удалено `DataEgressGiB` и `DataIngressGiB` из `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="1b379-575">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="1b379-576">Операция **Get-AzBatchNodeAgentSku** удалена и заменена на **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="1b379-576">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="1b379-577">**Get-AzBatchSupportedImage** возвращает те же данные, что и **Get-AzBatchNodeAgentSku**, но в более удобном формате.</span><span class="sxs-lookup"><span data-stu-id="1b379-577">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="1b379-578">Также возвращаются новые непроверенные образы.</span><span class="sxs-lookup"><span data-stu-id="1b379-578">New non-verified images are also now returned.</span></span> <span data-ttu-id="1b379-579">Включается и дополнительная информация о `Capabilities` и `BatchSupportEndOfLife` для каждого образа.</span><span class="sxs-lookup"><span data-stu-id="1b379-579">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="1b379-580">Добавлена возможность монтировать файловые системы на каждом узле пула с помощью нового параметра `MountConfiguration` в **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="1b379-580">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="1b379-581">Теперь поддерживаются правила безопасности сети, которые блокируют сетевой доступ к пулу по исходящему порту трафика.</span><span class="sxs-lookup"><span data-stu-id="1b379-581">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="1b379-582">Это выполняется с помощью свойства `SourcePortRanges` для `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="1b379-582">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="1b379-583">Что касается выполнения контейнеров, пакетная служба теперь поддерживает выполнение задачи в рабочей папке контейнера или рабочей папке задачи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="1b379-583">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="1b379-584">Выбор зависит от параметра `WorkingDirectory` в `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="1b379-584">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="1b379-585">Добавлена возможность указать коллекцию общедоступных IP-адресов для `PSNetworkConfiguration` с помощью нового свойства `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="1b379-585">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="1b379-586">Это гарантирует, что узлы в пуле будут иметь IP-адреса из списка, предоставленного пользователем.</span><span class="sxs-lookup"><span data-stu-id="1b379-586">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="1b379-587">Если значение не задано, по умолчанию для `WaitForSuccess` в `PSSTartTask` используется значение `$True` (ранее `$False`).</span><span class="sxs-lookup"><span data-stu-id="1b379-587">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="1b379-588">Если значение не задано, по умолчанию для `Scope` в `PSAutoUserSpecification` используется значение `Pool` (ранее `Task` для Windows или `Pool` для Linux).</span><span class="sxs-lookup"><span data-stu-id="1b379-588">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="1b379-589">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="1b379-589">Az.Cdn</span></span>
* <span data-ttu-id="1b379-590">Добавлены UrlRewriteAction и CacheKeyQueryStringAction в RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="1b379-590">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="1b379-591">Исправлено несколько ошибок, таких как отсутствующий входной параметр Selector в командлете New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="1b379-591">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1b379-592">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1b379-592">Az.Compute</span></span>
* <span data-ttu-id="1b379-593">Функция набора шифрования диска</span><span class="sxs-lookup"><span data-stu-id="1b379-593">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="1b379-594">Новые командлеты:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="1b379-594">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="1b379-595">Добавлен параметр ProximityPlacementGroupId в следующие командлеты:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="1b379-595">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="1b379-596">Параметры DiskEncryptionSetId и EncryptionType добавлены в следующие командлеты:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="1b379-596">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="1b379-597">Добавлен параметр PublicIPAddressVersion в New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="1b379-597">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="1b379-598">FileUris для расширения пользовательских скриптов теперь будет защищенным, а не общедоступным параметром</span><span class="sxs-lookup"><span data-stu-id="1b379-598">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="1b379-599">Добавлено ScaleInPolicy в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="1b379-599">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="1b379-600">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="1b379-600">Breaking changes</span></span>
    - <span data-ttu-id="1b379-601">Параметр UploadSizeInBytes применяется теперь вместо DiskSizeGB для New-AzDiskConfig, если CreateOption имеет значение Upload</span><span class="sxs-lookup"><span data-stu-id="1b379-601">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="1b379-602">PublishingProfile.Source.ManagedImage.Id заменяется на StorageProfile.Source.Id в объекте GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="1b379-602">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1b379-603">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1b379-603">Az.DataFactory</span></span>
* <span data-ttu-id="1b379-604">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.3.0.</span><span class="sxs-lookup"><span data-stu-id="1b379-604">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1b379-605">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1b379-605">Az.DataLakeStore</span></span>
* <span data-ttu-id="1b379-606">Обновлен пакет SDK для ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), включает следующие исправления</span><span class="sxs-lookup"><span data-stu-id="1b379-606">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="1b379-607">Не создается исключение при невозможности десериализовать значение времени создания для записи в корзине или каталоге.</span><span class="sxs-lookup"><span data-stu-id="1b379-607">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="1b379-608">Предоставляется параметр для времени ожидания запроса в adlsclient</span><span class="sxs-lookup"><span data-stu-id="1b379-608">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="1b379-609">Исправлена передача исходного значения syncflag для восстановления badoffset</span><span class="sxs-lookup"><span data-stu-id="1b379-609">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="1b379-610">Исправлена операция EnumerateDirectory, чтобы она извлекала токен продолжения после проверки ответа</span><span class="sxs-lookup"><span data-stu-id="1b379-610">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="1b379-611">Исправлена ошибка объединения</span><span class="sxs-lookup"><span data-stu-id="1b379-611">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="1b379-612">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="1b379-612">Az.FrontDoor</span></span>
* <span data-ttu-id="1b379-613">Исправлены разные опечатки в разных частях модуля</span><span class="sxs-lookup"><span data-stu-id="1b379-613">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="1b379-614">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1b379-614">Az.HDInsight</span></span>
* <span data-ttu-id="1b379-615">Исправлена ошибка, из-за которой клиент получал сообщение об ошибке 'Not a valid Base-64 string' (Не является допустимой строкой Base64) при выполнении Get-AzHDInsightCluster для получения кластера с хранилищем ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="1b379-615">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="1b379-616">Добавлен параметр с именем ApplicationId в три командлета Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig и New-AzHDInsightCluster, чтобы клиент мог предоставить идентификатор приложения субъекта-службы для доступа к Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="1b379-616">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="1b379-617">Для Microsoft.Azure.Management.HDInsight изменена версия с 2.1.0 на 5.1.0</span><span class="sxs-lookup"><span data-stu-id="1b379-617">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="1b379-618">Удалены пять командлетов:</span><span class="sxs-lookup"><span data-stu-id="1b379-618">Removed five cmdlets:</span></span>
    - <span data-ttu-id="1b379-619">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="1b379-619">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="1b379-620">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="1b379-620">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="1b379-621">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="1b379-621">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="1b379-622">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="1b379-622">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="1b379-623">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="1b379-623">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="1b379-624">Добавлены три командлета:</span><span class="sxs-lookup"><span data-stu-id="1b379-624">Added three cmdlets:</span></span>
    - <span data-ttu-id="1b379-625">Get-AzHDInsightMonitoring заменяет собой Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="1b379-625">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="1b379-626">Enable-AzHDInsightMonitoring заменяет собой Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="1b379-626">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="1b379-627">Disable-AzHDInsightMonitoring заменяет собой Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="1b379-627">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="1b379-628">Исправлен командлет Get-AzHDInsightProperties, чтобы он поддерживал получение сведений о возможностях из определенного расположения.</span><span class="sxs-lookup"><span data-stu-id="1b379-628">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="1b379-629">Удалены наборы параметров ("Spark1", "Spark2") из Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="1b379-629">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="1b379-630">Добавлены примеры в справочные документы по командлету Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="1b379-630">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="1b379-631">Изменен тип выходных данных для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="1b379-631">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="1b379-632">Для Get-AzHDInsightProperties тип выходных данных изменен с CapabilitiesResponse на AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="1b379-632">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="1b379-633">Для Remove-AzHDInsightCluster тип выходных данных изменен с ClusterGetResponse на bool.</span><span class="sxs-lookup"><span data-stu-id="1b379-633">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="1b379-634">Для Set-AzHDInsightGatewaySettings тип выходных данных изменен с HttpConnectivitySettings на GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="1b379-634">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="1b379-635">Добавлены несколько условий для проверки сценариев.</span><span class="sxs-lookup"><span data-stu-id="1b379-635">Added some scenario test cases.</span></span>
* <span data-ttu-id="1b379-636">Удалены несколько псевдонимов: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="1b379-636">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1b379-637">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1b379-637">Az.IotHub</span></span>
* <span data-ttu-id="1b379-638">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="1b379-638">Breaking changes:</span></span>
    - <span data-ttu-id="1b379-639">Командлет Add-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="1b379-639">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="1b379-640">Удален набор параметров __AllParameterSets для командлета Add-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="1b379-640">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="1b379-641">Командлет Get-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="1b379-641">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="1b379-642">Удален набор параметров __AllParameterSets для командлета Get-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="1b379-642">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="1b379-643">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties.</span><span class="sxs-lookup"><span data-stu-id="1b379-643">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="1b379-644">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties.</span><span class="sxs-lookup"><span data-stu-id="1b379-644">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="1b379-645">Командлет New-AzIotHubExportDevice больше не поддерживает псевдоним New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="1b379-645">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="1b379-646">Командлет New-AzIotHubImportDevice больше не поддерживает псевдоним New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="1b379-646">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="1b379-647">Командлет Remove-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="1b379-647">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="1b379-648">Удален набор параметров __AllParameterSets для командлета Remove-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="1b379-648">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="1b379-649">Командлет Set-AzIotHub теперь не поддерживает параметр OperationsMonitoringProperties и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="1b379-649">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="1b379-650">Удален набор параметров UpdateOperationsMonitoringProperties для командлета Set-AzIotHub.</span><span class="sxs-lookup"><span data-stu-id="1b379-650">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1b379-651">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1b379-651">Az.RecoveryServices</span></span>
* <span data-ttu-id="1b379-652">Azure Site Recovery поддерживает настройку сетевых ресурсов, например групп безопасности сети, общедоступных IP-адресов и внутренних подсистем балансировки нагрузки из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="1b379-652">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="1b379-653">Azure Site Recovery поддерживает запись на управляемый диск из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="1b379-653">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="1b379-654">Azure Site Recovery поддерживает сокращение NIC из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="1b379-654">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="1b379-655">Azure Site Recovery поддерживает ускорение сети NIC из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="1b379-655">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="1b379-656">Azure Site Recovery поддерживает автоматическое обновление агента из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="1b379-656">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="1b379-657">Azure Site Recovery поддерживает стандартный SSD-накопитель из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="1b379-657">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="1b379-658">Azure Site Recovery поддерживает двухпроходное шифрование диска Azure из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="1b379-658">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="1b379-659">Azure Site Recovery поддерживает новый добавленный диск из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="1b379-659">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="1b379-660">Добавлена функция SoftDelete для виртуальных машин и соответствующие тесты</span><span class="sxs-lookup"><span data-stu-id="1b379-660">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="1b379-661">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1b379-661">Az.Resources</span></span>
* <span data-ttu-id="1b379-662">Обновлена сборка зависимостей Microsoft.Extensions.Caching.Memory с версии 1.1.1 до 2.2</span><span class="sxs-lookup"><span data-stu-id="1b379-662">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1b379-663">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1b379-663">Az.Network</span></span>
* <span data-ttu-id="1b379-664">Изменены все командлеты для PrivateEndpointConnection, чтобы они поддерживали универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="1b379-664">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="1b379-665">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="1b379-665">Updated cmdlet:</span></span>
        - <span data-ttu-id="1b379-666">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="1b379-666">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="1b379-667">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="1b379-667">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="1b379-668">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="1b379-668">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="1b379-669">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="1b379-669">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="1b379-670">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1b379-670">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="1b379-671">Добавлен новый командлет для PrivateLinkResource, который поддерживает универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="1b379-671">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="1b379-672">Новый командлет</span><span class="sxs-lookup"><span data-stu-id="1b379-672">New cmdlet:</span></span>
        - <span data-ttu-id="1b379-673">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="1b379-673">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="1b379-674">Добавлены новые поля и параметр для протокола прокси версии 2.</span><span class="sxs-lookup"><span data-stu-id="1b379-674">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="1b379-675">Добавлено свойство EnableProxyProtocol в PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="1b379-675">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="1b379-676">Добавлено свойство LinkIdentifier в PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1b379-676">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="1b379-677">Обновлен New-AzPrivateLinkService для поддержки нового необязательного параметра EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="1b379-677">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="1b379-678">Исправлено описание параметра в справочной документации по командлету New-AzApplicationGatewaySku.</span><span class="sxs-lookup"><span data-stu-id="1b379-678">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="1b379-679">Новые командлеты для поддержки политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="1b379-679">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="1b379-680">Добавлена поддержка дочерних ресурсов RouteTables для VirtualHub</span><span class="sxs-lookup"><span data-stu-id="1b379-680">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="1b379-681">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="1b379-681">New cmdlets added:</span></span>
        - <span data-ttu-id="1b379-682">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="1b379-682">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="1b379-683">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="1b379-683">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="1b379-684">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="1b379-684">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="1b379-685">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="1b379-685">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="1b379-686">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="1b379-686">Set-AzVirtualHub</span></span>
* <span data-ttu-id="1b379-687">Добавлена поддержка новых свойств SKU для VirtualHub и VirtualWANType в VirtualWan</span><span class="sxs-lookup"><span data-stu-id="1b379-687">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="1b379-688">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="1b379-688">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="1b379-689">New-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="1b379-689">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="1b379-690">Update-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="1b379-690">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="1b379-691">New-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="1b379-691">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="1b379-692">Update-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="1b379-692">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="1b379-693">Добавлена поддержка свойства EnableInternetSecurity для HubVnetConnection, VpnConnection и ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="1b379-693">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="1b379-694">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="1b379-694">New cmdlets added:</span></span>
        - <span data-ttu-id="1b379-695">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="1b379-695">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="1b379-696">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="1b379-696">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="1b379-697">New-AzureRmVirtualHubVnetConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="1b379-697">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="1b379-698">New-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="1b379-698">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="1b379-699">Update-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="1b379-699">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="1b379-700">New-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="1b379-700">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="1b379-701">Set-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="1b379-701">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="1b379-702">Добавлена поддержка настройки политики верхнего уровня WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="1b379-702">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="1b379-703">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="1b379-703">New cmdlets added:</span></span>
        - <span data-ttu-id="1b379-704">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="1b379-704">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="1b379-705">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="1b379-705">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="1b379-706">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="1b379-706">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="1b379-707">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="1b379-707">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="1b379-708">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="1b379-708">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="1b379-709">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="1b379-709">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="1b379-710">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="1b379-710">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="1b379-711">New-AzApplicationGatewayFirewallPolicy: добавлены параметры PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="1b379-711">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="1b379-712">Добавлена поддержка оператора Geo-Match для CustomRule</span><span class="sxs-lookup"><span data-stu-id="1b379-712">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="1b379-713">Добавлен параметр GeoMatch в оператор для FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="1b379-713">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="1b379-714">Добавлена поддержка политики брандмауэра perListener и perSite</span><span class="sxs-lookup"><span data-stu-id="1b379-714">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="1b379-715">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="1b379-715">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="1b379-716">New-AzApplicationGatewayHttpListener: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="1b379-716">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="1b379-717">New-AzApplicationGatewayPathRuleConfig: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="1b379-717">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="1b379-718">Исправлен учет регистра для требуемой подсети с именем AzureBastionSubnet в PSBastion</span><span class="sxs-lookup"><span data-stu-id="1b379-718">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="1b379-719">Поддержка полного доменного имени назначения в правилах сети и преобразованного полного доменного имени в правилах NAT для брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="1b379-719">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="1b379-720">Добавлена поддержка ресурсов верхнего уровня RouteTables для IpGroup</span><span class="sxs-lookup"><span data-stu-id="1b379-720">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="1b379-721">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="1b379-721">New cmdlets added:</span></span>
        - <span data-ttu-id="1b379-722">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="1b379-722">New-AzIpGroup</span></span>
        - <span data-ttu-id="1b379-723">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="1b379-723">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="1b379-724">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="1b379-724">Get-AzIpGroup</span></span>
        - <span data-ttu-id="1b379-725">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="1b379-725">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="1b379-726">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1b379-726">Az.ServiceFabric</span></span>
* <span data-ttu-id="1b379-727">Удален командлет Add-AzServiceFabricApplicationCertificate, так как соответствующий сценарий выполняется командлетом Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="1b379-727">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="1b379-728">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1b379-728">Az.Sql</span></span>
* <span data-ttu-id="1b379-729">Добавлена поддержка восстановления удаленных баз данных в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="1b379-729">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="1b379-730">Из кода удалены старые командлеты аудита.</span><span class="sxs-lookup"><span data-stu-id="1b379-730">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="1b379-731">Удалены нерекомендуемые псевдонимы:</span><span class="sxs-lookup"><span data-stu-id="1b379-731">Removed deprecated aliases:</span></span>
* <span data-ttu-id="1b379-732">Get-AzSqlDatabaseIndexRecommendations (вместо него используйте Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="1b379-732">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="1b379-733">Get-AzSqlDatabaseRestorePoints (вместо него используйте Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="1b379-733">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="1b379-734">Удален командлет Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1b379-734">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="1b379-735">Удалены псевдонимы для нерекомендуемых командлетов параметров оценки уязвимостей</span><span class="sxs-lookup"><span data-stu-id="1b379-735">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="1b379-736">Командлеты расширенного обнаружения угроз объявлены устаревшими</span><span class="sxs-lookup"><span data-stu-id="1b379-736">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="1b379-737">Добавлены командлеты для отключения и включения рекомендаций о конфиденциальности для столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="1b379-737">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1b379-738">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1b379-738">Az.Storage</span></span>
* <span data-ttu-id="1b379-739">Поддержка включения большой общей папки при создании или обновлении учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="1b379-739">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="1b379-740">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1b379-740">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="1b379-741">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1b379-741">Set-AzStorageAccount</span></span>
* <span data-ttu-id="1b379-742">При закрытии или получении маркера файла пропускается проверка того, является ли входной путь файлом или каталогом, чтобы избежать сбоев при получении объектов в состоянии DeletePending.</span><span class="sxs-lookup"><span data-stu-id="1b379-742">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="1b379-743">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="1b379-743">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="1b379-744">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="1b379-744">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="1b379-745">2.8.0 — октябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="1b379-745">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="1b379-746">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="1b379-746">General</span></span>
* <span data-ttu-id="1b379-747">Выпуск Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="1b379-747">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="1b379-748">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1b379-748">Az.Accounts</span></span>
* <span data-ttu-id="1b379-749">Обновление телеметрии и перезаписи URL-адресов для созданных модулей, исправление для модульных тестов Windows.</span><span class="sxs-lookup"><span data-stu-id="1b379-749">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="1b379-750">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1b379-750">Az.ApiManagement</span></span>
* <span data-ttu-id="1b379-751">**Set-AzApiManagementApi** — в ApiVersionSet добавлена поддержка обновления API.</span><span class="sxs-lookup"><span data-stu-id="1b379-751">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="1b379-752">исправлена проблема https://github.com/Azure/azure-powershell/issues/10068.</span><span class="sxs-lookup"><span data-stu-id="1b379-752">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1b379-753">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1b379-753">Az.Automation</span></span>
* <span data-ttu-id="1b379-754">Исправлен командлет New-AzureAutomationSoftwareUpdateConfiguration для параметра перезагрузки Linux.</span><span class="sxs-lookup"><span data-stu-id="1b379-754">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="1b379-755">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="1b379-755">Az.Batch</span></span>
* <span data-ttu-id="1b379-756">Командлет **Get-AzBatchNodeAgentSku** объявлен устаревшим и будет заменен на **Get-AzBatchSupportImage** в версии 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="1b379-756">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1b379-757">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1b379-757">Az.Compute</span></span>
* <span data-ttu-id="1b379-758">В командлеты New-AzVM и New-AzVmss добавлены параметры Priority, EvictionPolicy и MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="1b379-758">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="1b379-759">Исправлены предупреждающее сообщение для командлетов Add-AzVMAdditionalUnattendContent и Add-AzVMSshPublicKey и справочная документация по ним.</span><span class="sxs-lookup"><span data-stu-id="1b379-759">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="1b379-760">Для Set-AzVMDiskEncryptionExtension исправлено исключение -skipVmBackup для виртуальных машин Linux с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="1b379-760">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="1b379-761">Исправлена ошибка при изменении параметров шифрования в Set-AzVMDiskEncryptionExtension, реализован двухэтапный сценарий.</span><span class="sxs-lookup"><span data-stu-id="1b379-761">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1b379-762">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1b379-762">Az.DataFactory</span></span>
* <span data-ttu-id="1b379-763">Добавлены команды CRUD для потока данных Фабрики данных Azure версии 2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow и Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="1b379-763">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="1b379-764">Добавлены команды действий для сеанса отладки потока данных Фабрики данных Azure версии 2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand и Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="1b379-764">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="1b379-765">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.2.0.</span><span class="sxs-lookup"><span data-stu-id="1b379-765">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1b379-766">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1b379-766">Az.DataLakeStore</span></span>
* <span data-ttu-id="1b379-767">Проверка учетной записи исправлена так, чтобы учетные записи, содержащие знак "-", можно было передавать без домена.</span><span class="sxs-lookup"><span data-stu-id="1b379-767">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="1b379-768">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="1b379-768">Az.HealthcareApis</span></span>
* <span data-ttu-id="1b379-769">Версия PowerShell обновлена до 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="1b379-769">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="1b379-770">Версия пакета SDK обновлена до 1.0.2.</span><span class="sxs-lookup"><span data-stu-id="1b379-770">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="1b379-771">В тестах обновлены ссылки на новую версию пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="1b379-771">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="1b379-772">Вложенная выходная структура заменена на плоскую.</span><span class="sxs-lookup"><span data-stu-id="1b379-772">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1b379-773">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1b379-773">Az.IotHub</span></span>
* <span data-ttu-id="1b379-774">Добавлен новый источник маршрутизации DigitalTwinChangeEvents.</span><span class="sxs-lookup"><span data-stu-id="1b379-774">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="1b379-775">Исправлены незначительные ошибки: Get-AzIothub не возвращает subscriptionId.</span><span class="sxs-lookup"><span data-stu-id="1b379-775">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1b379-776">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1b379-776">Az.Monitor</span></span>
* <span data-ttu-id="1b379-777">Добавлены новые получатели групп действий: -ItsmReceiver, -VoiceReceiver, -ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver.</span><span class="sxs-lookup"><span data-stu-id="1b379-777">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="1b379-778">Для получателей включите общую схему оповещений.</span><span class="sxs-lookup"><span data-stu-id="1b379-778">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="1b379-779">Это не касается получателей SMS, push-уведомлений приложения Azure, ITSM и голосовых сообщений.</span><span class="sxs-lookup"><span data-stu-id="1b379-779">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="1b379-780">Веб-перехватчики теперь поддерживают аутентификацию Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1b379-780">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1b379-781">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1b379-781">Az.Network</span></span>
* <span data-ttu-id="1b379-782">Добавлен новый командлет Get-AzAvailableServiceAlias, позволяющий получить псевдонимы для политик конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="1b379-782">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="1b379-783">В подключениях шлюза виртуальной сети появилась возможность добавлять селекторы трафика.</span><span class="sxs-lookup"><span data-stu-id="1b379-783">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="1b379-784">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="1b379-784">New cmdlets added:</span></span>
        - <span data-ttu-id="1b379-785">New-AzureRmTrafficSelectorPolicy.</span><span class="sxs-lookup"><span data-stu-id="1b379-785">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="1b379-786">В командлеты добавлены необязательные параметры -TrafficSelectorPolicies, -New-AzureRmVirtualNetworkGatewayConnection, -Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="1b379-786">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="1b379-787">В конфигурациях правил сетевой безопасности добавлена поддержка протоколов ESP и AH.</span><span class="sxs-lookup"><span data-stu-id="1b379-787">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="1b379-788">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="1b379-788">Updated cmdlets:</span></span>
        - <span data-ttu-id="1b379-789">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="1b379-789">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="1b379-790">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="1b379-790">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="1b379-791">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="1b379-791">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="1b379-792">Улучшена обработка исключений в командлетах Cortex.</span><span class="sxs-lookup"><span data-stu-id="1b379-792">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="1b379-793">Выпущены новые поколения и номера SKU VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="1b379-793">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="1b379-794">Представлены новые поколения VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="1b379-794">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="1b379-795">Представлены новые номера SKU VirtualNetworkGateways с высокой пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="1b379-795">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="1b379-796">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="1b379-796">Az.RedisCache</span></span>
* <span data-ttu-id="1b379-797">В справочную документацию по Set-AzRedisCache добавлены недостающие значения для параметра -Size.</span><span class="sxs-lookup"><span data-stu-id="1b379-797">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="1b379-798">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1b379-798">Az.Sql</span></span>
* <span data-ttu-id="1b379-799">Добавлена возможность назначать администратора Active Directory в Управляемом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="1b379-799">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1b379-800">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1b379-800">Az.Storage</span></span>
* <span data-ttu-id="1b379-801">Клиентская библиотека службы хранилища Azure обновлена до версии 11.1.0.</span><span class="sxs-lookup"><span data-stu-id="1b379-801">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="1b379-802">NextPageLink теперь позволяет получить список контейнеров с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="1b379-802">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="1b379-803">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1b379-803">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="1b379-804">NextPageLink теперь позволяет получить список учетных записей хранения из подписки.</span><span class="sxs-lookup"><span data-stu-id="1b379-804">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="1b379-805">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1b379-805">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="1b379-806">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="1b379-806">Az.StorageSync</span></span>
* <span data-ttu-id="1b379-807">Исправлена проблема 9810 с Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="1b379-807">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1b379-808">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1b379-808">Az.Websites</span></span>
* <span data-ttu-id="1b379-809">Обновление плана службы приложений с помощью Set-AzWebApp приводило к сбою приложения.</span><span class="sxs-lookup"><span data-stu-id="1b379-809">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="1b379-810">2.7.0 — сентябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="1b379-810">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="1b379-811">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1b379-811">Az.ApiManagement</span></span>
* <span data-ttu-id="1b379-812">В справочной документации по командлету Set-AzApiManagementPolicy обновлено описание параметра -Format.</span><span class="sxs-lookup"><span data-stu-id="1b379-812">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="1b379-813">Из справочной документации удалены ссылки на нерекомендуемый командлет Update-AzApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="1b379-813">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="1b379-814">Вместо него следует использовать командлет Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="1b379-814">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1b379-815">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1b379-815">Az.Automation</span></span>
* <span data-ttu-id="1b379-816">В справочной документации по командлету Register-AzAutomationDscNode исправлена опечатка в примере.</span><span class="sxs-lookup"><span data-stu-id="1b379-816">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="1b379-817">Добавлено уточнение об ограничениях ОС для командлета Register-AzAutomationDSCNode.</span><span class="sxs-lookup"><span data-stu-id="1b379-817">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="1b379-818">Исправлено исключение пустой ссылки для параметра -Wait в командлете Start-AzAutomationRunbook.</span><span class="sxs-lookup"><span data-stu-id="1b379-818">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1b379-819">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1b379-819">Az.Compute</span></span>
* <span data-ttu-id="1b379-820">Добавлен параметр UploadSizeInBytes для командлета New-AzDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="1b379-820">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="1b379-821">Добавлен добавочный параметр для командлета New-AzSnapshotConfig.</span><span class="sxs-lookup"><span data-stu-id="1b379-821">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="1b379-822">Для виртуальной машины добавлены такие функции с низким приоритетом:</span><span class="sxs-lookup"><span data-stu-id="1b379-822">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="1b379-823">Для командлета New-AzVMConfig добавлены параметры MaxPrice, EvictionPolicy и Priority.</span><span class="sxs-lookup"><span data-stu-id="1b379-823">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="1b379-824">Для командлетов New-AzVmssConfig, Update-AzVM и Update-AzVmss добавлен параметр MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="1b379-824">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="1b379-825">Для командлета Get-AzAvailabilitySet устранена проблема со ссылкой на виртуальную машину, когда в нем перечисляются все группы доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="1b379-825">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="1b379-826">Исправлено исключение NULL для командлета Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="1b379-826">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="1b379-827">Исправлен метод поиска VHD для относительной конечной позиции.</span><span class="sxs-lookup"><span data-stu-id="1b379-827">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="1b379-828">Устранена проблема с UltraSSD для командлетов New-AzVM и Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="1b379-828">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1b379-829">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1b379-829">Az.DataFactory</span></span>
* <span data-ttu-id="1b379-830">Добавлены 3 новые команды для ADF версии 2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription и Get-AzDataFactoryV2TriggerSubscriptionStatus.</span><span class="sxs-lookup"><span data-stu-id="1b379-830">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="1b379-831">Пакет SDK ADF для .NET обновлен до версии 4.1.3.</span><span class="sxs-lookup"><span data-stu-id="1b379-831">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="1b379-832">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1b379-832">Az.HDInsight</span></span>
* <span data-ttu-id="1b379-833">Укажите критические изменения.</span><span class="sxs-lookup"><span data-stu-id="1b379-833">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1b379-834">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1b379-834">Az.IotHub</span></span>
* <span data-ttu-id="1b379-835">Добавлена поддержка для вызова отработки отказа для IotHub в георегион аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="1b379-835">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="1b379-836">Добавлена поддержка для управления обогащением сообщений для IotHub.</span><span class="sxs-lookup"><span data-stu-id="1b379-836">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="1b379-837">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="1b379-837">New cmdlets are:</span></span>
    - <span data-ttu-id="1b379-838">Add-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="1b379-838">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="1b379-839">Get-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="1b379-839">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="1b379-840">Remove-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="1b379-840">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="1b379-841">Set-AzIotHubMessageEnrichment.</span><span class="sxs-lookup"><span data-stu-id="1b379-841">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1b379-842">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1b379-842">Az.Monitor</span></span>
* <span data-ttu-id="1b379-843">Указание на самую последнюю версию пакета SDK для монитора, т. е. 0.24.1-preview:</span><span class="sxs-lookup"><span data-stu-id="1b379-843">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="1b379-844">В командлеты метрик добавлены некритические изменения, т. е. перечисление единиц поддерживает несколько новых значений.</span><span class="sxs-lookup"><span data-stu-id="1b379-844">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="1b379-845">Эти командлеты доступны только для чтения, поэтому входные данные командлетов не будут изменены.</span><span class="sxs-lookup"><span data-stu-id="1b379-845">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="1b379-846">Актуальная версия API запросов **ActionGroups** — **2019-06-01**. До этого была версия **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="1b379-846">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="1b379-847">Тесты сценария обновлены в соответствии с этим изменением.</span><span class="sxs-lookup"><span data-stu-id="1b379-847">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="1b379-848">В конструкторы классов **EmailReceiver** и **WebhookReceiver** добавлен один новый обязательный аргумент — логическое значение с именем **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="1b379-848">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="1b379-849">Сейчас для него установлено значение **false**, чтобы скрыть это критическое изменение от командлетов.</span><span class="sxs-lookup"><span data-stu-id="1b379-849">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="1b379-850">**Примечание**. Это временное изменение, которое должно быть подтверждено командой оповещения.</span><span class="sxs-lookup"><span data-stu-id="1b379-850">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="1b379-851">Порядок аргументов для конструктора класса **Source** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="1b379-851">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="1b379-852">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="1b379-852">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="1b379-853">Порядок аргументов для конструктора класса **AlertingAction** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="1b379-853">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="1b379-854">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="1b379-854">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="1b379-855">Добавлена поддержка критериев динамического порога для оповещения метрики версии 2:</span><span class="sxs-lookup"><span data-stu-id="1b379-855">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="1b379-856">New-AzMetricAlertRuleV2Criteria: теперь также позволяет создавать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="1b379-856">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="1b379-857">Add-AzMetricAlertRuleV2: теперь также позволяет принимать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="1b379-857">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="1b379-858">Добавлены усовершенствования в командлетах запланированных правил запросов (SQR).</span><span class="sxs-lookup"><span data-stu-id="1b379-858">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="1b379-859">Командлеты будут принимать параметр Location в обоих форматах: расположение (например, eastus) или отображаемое имя расположения (например, "восточная часть США").</span><span class="sxs-lookup"><span data-stu-id="1b379-859">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="1b379-860">Параметр Enabled проиллюстрирован в файлах справки надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="1b379-860">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="1b379-861">Добавлены примеры для необязательного параметра ActionGroup.</span><span class="sxs-lookup"><span data-stu-id="1b379-861">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="1b379-862">Все файлы справки улучшены.</span><span class="sxs-lookup"><span data-stu-id="1b379-862">Overall improved help files</span></span>
* <span data-ttu-id="1b379-863">Исправлена ошибка в определении типа области для командлета Set-AzActionRule.</span><span class="sxs-lookup"><span data-stu-id="1b379-863">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1b379-864">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1b379-864">Az.Network</span></span>
* <span data-ttu-id="1b379-865">Исправлен неправильный пример в справочной документации по командлету New-AzApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="1b379-865">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="1b379-866">В справочную документацию по командлету Get-AzNetworkWatcherPacketCapture добавлено примечание, посвященное извлечению всех свойств для записи пакетов.</span><span class="sxs-lookup"><span data-stu-id="1b379-866">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="1b379-867">В справочной документации по командлету Test-AzNetworkWatcherIPFlow исправлен пример: теперь он правильно перечисляет сетевые карты.</span><span class="sxs-lookup"><span data-stu-id="1b379-867">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="1b379-868">Улучшен анализ облачных исключений для отображения дополнительных сведений (при их наличии).</span><span class="sxs-lookup"><span data-stu-id="1b379-868">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="1b379-869">Улучшен анализ облачных исключений для обработки дополнительного типа исключения SDK.</span><span class="sxs-lookup"><span data-stu-id="1b379-869">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="1b379-870">Исправлено неправильное сопоставление моделей правил безопасности.</span><span class="sxs-lookup"><span data-stu-id="1b379-870">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="1b379-871">Добавлены свойства сетевого интерфейса для компонента частного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="1b379-871">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="1b379-872">Для интерфейса PSNetworkInterface добавлено свойство PrivateEndpoint с типом PSResourceId.</span><span class="sxs-lookup"><span data-stu-id="1b379-872">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="1b379-873">В PSNetworkInterfaceIPConfiguration добавлено свойство PrivateLinkConnectionProperties с типом PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="1b379-873">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="1b379-874">Добавлен новый класс модели: PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="1b379-874">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="1b379-875">Добавлен новый тип ApplicationRuleProtocolType "mssql" для ресурса Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="1b379-875">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="1b379-876">Поддержка многоканального подключения в Виртуальной глобальной сети:</span><span class="sxs-lookup"><span data-stu-id="1b379-876">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="1b379-877">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="1b379-877">New cmdlets</span></span>
        - <span data-ttu-id="1b379-878">New-AzVpnSiteLink;</span><span class="sxs-lookup"><span data-stu-id="1b379-878">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="1b379-879">New-AzVpnSiteLinkConnection;</span><span class="sxs-lookup"><span data-stu-id="1b379-879">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="1b379-880">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="1b379-880">Updated cmdlet:</span></span>
        - <span data-ttu-id="1b379-881">New-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="1b379-881">New-VpnSite</span></span>
        - <span data-ttu-id="1b379-882">Update-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="1b379-882">Update-VpnSite</span></span>
        - <span data-ttu-id="1b379-883">New-VpnConnection;</span><span class="sxs-lookup"><span data-stu-id="1b379-883">New-VpnConnection</span></span>
        - <span data-ttu-id="1b379-884">Update-VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="1b379-884">Update-VpnConnection</span></span>
* <span data-ttu-id="1b379-885">Исправлены документы с некоторыми примерами PowerShell для использования командлетов AZ вместо командлетов AzureRM.</span><span class="sxs-lookup"><span data-stu-id="1b379-885">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1b379-886">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1b379-886">Az.RecoveryServices</span></span>
* <span data-ttu-id="1b379-887">Для объекта AzureVMpolicy добавлен новый атрибут — ProtectedItemsCount.</span><span class="sxs-lookup"><span data-stu-id="1b379-887">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="1b379-888">Добавлены тесты для политики виртуальной машины и восстановления исходной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="1b379-888">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="1b379-889">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1b379-889">Az.Resources</span></span>
* <span data-ttu-id="1b379-890">Исправлена ошибка, при которой не удавалось вызвать командлет New-AzRoleAssignment без параметра Scope.</span><span class="sxs-lookup"><span data-stu-id="1b379-890">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="1b379-891">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1b379-891">Az.ServiceFabric</span></span>
* <span data-ttu-id="1b379-892">Исправлена опечатка в примере в справочной документации по командлету Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="1b379-892">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="1b379-893">Добавлены новые командлеты для управления приложениями и службами:</span><span class="sxs-lookup"><span data-stu-id="1b379-893">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="1b379-894">New-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="1b379-894">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="1b379-895">New-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="1b379-895">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="1b379-896">New-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="1b379-896">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="1b379-897">New-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="1b379-897">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="1b379-898">Update-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="1b379-898">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="1b379-899">Get-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="1b379-899">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="1b379-900">Get-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="1b379-900">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="1b379-901">Get-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="1b379-901">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="1b379-902">Get-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="1b379-902">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="1b379-903">Remove-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="1b379-903">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="1b379-904">Remove-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="1b379-904">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="1b379-905">Remove-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="1b379-905">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="1b379-906">Remove-AzServiceFabricServic.</span><span class="sxs-lookup"><span data-stu-id="1b379-906">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="1b379-907">Пакет SDK для Service Fabric обновлен до версии 1.2.0, в которой используется версия API 2019-03-01 поставщика ресурсов Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="1b379-907">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="1b379-908">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="1b379-908">Az.SignalR</span></span>
* <span data-ttu-id="1b379-909">Добавлены командлеты Update, Restart, CheckNameAvailability и GetUsage.</span><span class="sxs-lookup"><span data-stu-id="1b379-909">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="1b379-910">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1b379-910">Az.Sql</span></span>
* <span data-ttu-id="1b379-911">Обновлен пример в справочной документации по командлету Get-AzSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="1b379-911">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="1b379-912">Добавлен пример виртуального ядра для командлета создания эластичного пула (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="1b379-912">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="1b379-913">Удалена проверка свойства EmailAddresses и того, что свойство EmailAdmins правильное в случае, если свойство EmailAddresses пустое в командлетах Set-AzSqlServerAdvancedThreatProtectionPolicy и Set-AzSqlDatabaseAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="1b379-913">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="1b379-914">Теперь, если существует несколько параметров диагностики, включающих категорию аудита, параметры аудита сервера и базы данных удаляются.</span><span class="sxs-lookup"><span data-stu-id="1b379-914">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="1b379-915">Исправлена проверка адресов электронной почты в нескольких командлетах оценки уязвимостей SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting и Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="1b379-915">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1b379-916">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1b379-916">Az.Storage</span></span>
* <span data-ttu-id="1b379-917">Обновлен пример в справочной документации по командлету Get-AzStorageAccountKey.</span><span class="sxs-lookup"><span data-stu-id="1b379-917">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="1b379-918">Теперь при отправке и загрузке файла Azure в конечном файле сохраняются свойства SMB исходного файла (атрибуты файла, время создания файла, время последней записи файла).</span><span class="sxs-lookup"><span data-stu-id="1b379-918">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="1b379-919">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="1b379-919">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="1b379-920">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="1b379-920">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="1b379-921">Исправлена операция отправки блочного BLOB-объекта, в которой происходили сбои свойств и метаданных в контейнере с включенной ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="1b379-921">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="1b379-922">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="1b379-922">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="1b379-923">Добавлена поддержка управления общими папками Azure в API плоскости управления с помощью таких командлетов:</span><span class="sxs-lookup"><span data-stu-id="1b379-923">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="1b379-924">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="1b379-924">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="1b379-925">Get-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="1b379-925">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="1b379-926">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="1b379-926">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="1b379-927">Remove-AzRmStorageShare.</span><span class="sxs-lookup"><span data-stu-id="1b379-927">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1b379-928">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1b379-928">Az.Websites</span></span>
* <span data-ttu-id="1b379-929">Устранена проблема, из-за которой теги webapp удалялись при переносе приложения в новый ASP.</span><span class="sxs-lookup"><span data-stu-id="1b379-929">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="1b379-930">Теперь командлет Publish-AzureWebapp работает в Linux и Windows.</span><span class="sxs-lookup"><span data-stu-id="1b379-930">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="1b379-931">Обновлен пример в справочной документации по командлету Get-AzWebAppPublishingProfile.</span><span class="sxs-lookup"><span data-stu-id="1b379-931">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="1b379-932">2.6.0 — август 2019 г.</span><span class="sxs-lookup"><span data-stu-id="1b379-932">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="1b379-933">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="1b379-933">General</span></span>
* <span data-ttu-id="1b379-934">Исправлены опечатки в модулях.</span><span class="sxs-lookup"><span data-stu-id="1b379-934">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="1b379-935">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1b379-935">Az.Accounts</span></span>
* <span data-ttu-id="1b379-936">Добавлена поддержка назначаемого пользователем удостоверения MSI при проверке подлинности в Функциях Azure (№ 9479).</span><span class="sxs-lookup"><span data-stu-id="1b379-936">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="1b379-937">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="1b379-937">Az.Aks</span></span>
* <span data-ttu-id="1b379-938">Устранена проблема с выходными данными для Get-AzAks.</span><span class="sxs-lookup"><span data-stu-id="1b379-938">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="1b379-939">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9847.</span><span class="sxs-lookup"><span data-stu-id="1b379-939">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="1b379-940">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1b379-940">Az.ApiManagement</span></span>
* <span data-ttu-id="1b379-941">исправлена проблема https://github.com/Azure/azure-powershell/issues/9351.</span><span class="sxs-lookup"><span data-stu-id="1b379-941">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="1b379-942">Обновлена версия NuGet для .NET, которая не накладывает ограничений на productId, apiId, groupId и userId.</span><span class="sxs-lookup"><span data-stu-id="1b379-942">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="1b379-943">**Get-AzApiManagementProduct**. Добавлена поддержка запросов к продуктам с помощью API.</span><span class="sxs-lookup"><span data-stu-id="1b379-943">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="1b379-944">**New-AzApiManagementApiRevision**. Устранена проблема, из-за которой не задавался параметр ApiRevisionDescription при создании новой редакции API https://github.com/Azure/azure-powershell/issues/9752.</span><span class="sxs-lookup"><span data-stu-id="1b379-944">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="1b379-945">Исправлено написание имени модели c PsApiManagementOAuth2AuthrozationServer на PsApiManagementOAuth2AuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="1b379-945">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="1b379-946">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="1b379-946">Az.Batch</span></span>
* <span data-ttu-id="1b379-947">Исправлена опечатка в написании Windows со строчной буквы в справочных сообщениях и документации.</span><span class="sxs-lookup"><span data-stu-id="1b379-947">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="1b379-948">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="1b379-948">Az.Cdn</span></span>
* <span data-ttu-id="1b379-949">Исправлена опечатка во вспомогательном приложении модуля CDN.</span><span class="sxs-lookup"><span data-stu-id="1b379-949">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1b379-950">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1b379-950">Az.Compute</span></span>
* <span data-ttu-id="1b379-951">Добавлен параметр VmssId в новый командлет Add New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="1b379-951">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="1b379-952">Добавлены параметры TerminateScheduledEvents и TerminateScheduledEventNotBeforeTimeoutInMinutes в New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="1b379-952">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="1b379-953">Добавлено свойство HyperVGeneration в объект образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1b379-953">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="1b379-954">Добавлены компоненты Host и HostGroup.</span><span class="sxs-lookup"><span data-stu-id="1b379-954">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="1b379-955">Новые командлеты:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="1b379-955">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="1b379-956">Параметр HostId добавлен в New-AzVMConfig и New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="1b379-956">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="1b379-957">Исправлен пример в документации по Invoke-AzVMRunCommand, в котором теперь используется правильное имя параметра.</span><span class="sxs-lookup"><span data-stu-id="1b379-957">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="1b379-958">Исправлено описание VolumeType в справочной документации по Set-AzVMDiskEncryptionExtension и Set-AzVmssDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="1b379-958">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1b379-959">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1b379-959">Az.DataFactory</span></span>
* <span data-ttu-id="1b379-960">Исправлена опечатка в написании Windows со строчной буквы в документации по New-AzDataFactoryEncryptValue.</span><span class="sxs-lookup"><span data-stu-id="1b379-960">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="1b379-961">Пакет SDK ADF для .NET обновлен до версии 4.1.2.</span><span class="sxs-lookup"><span data-stu-id="1b379-961">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="1b379-962">Добавлены параметры DataProxyIntegrationRuntimeName, DataProxyStagingLinkedServiceName и DataProxyStagingPath в командлет Set-AzureRmDataFactoryV2IntegrationRuntime, что позволяет настраивать локальную среду выполнения интеграции в качестве прокси-сервера для Azure-SSIS Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="1b379-962">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="1b379-963">Обновлены PSTriggerRun для отображения активированных конвейеров, сообщений и свойств и PSActivityRun для отображения типа действия.</span><span class="sxs-lookup"><span data-stu-id="1b379-963">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1b379-964">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1b379-964">Az.DataLakeStore</span></span>
* <span data-ttu-id="1b379-965">Устранена проблема, при которой Get-DataLakeStoreDeletedItem переставал отвечать на запросы при возникновении ошибок или удаленных исключений.</span><span class="sxs-lookup"><span data-stu-id="1b379-965">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="1b379-966">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="1b379-966">Az.EventHub</span></span>
* <span data-ttu-id="1b379-967">Исправлена проблема № 9658: опечатка в написании параметра VirtualNteworkRule у Set-AzEventHubNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="1b379-967">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="1b379-968">Исправлена проблема № 9558: в Set-AzEventHubNamespace используется PATCH вместо PUT.</span><span class="sxs-lookup"><span data-stu-id="1b379-968">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="1b379-969">В командлет Set-AzEventHubNamespace добавлен параметр EnableKafka.</span><span class="sxs-lookup"><span data-stu-id="1b379-969">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="1b379-970">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="1b379-970">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="1b379-971">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="1b379-971">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="1b379-972">Исправлено написание Azure со строчной буквы.</span><span class="sxs-lookup"><span data-stu-id="1b379-972">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1b379-973">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1b379-973">Az.Monitor</span></span>
* <span data-ttu-id="1b379-974">Исправлены неправильные имена параметров в справочной документации.</span><span class="sxs-lookup"><span data-stu-id="1b379-974">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1b379-975">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1b379-975">Az.Network</span></span>
* <span data-ttu-id="1b379-976">Обновлен New-AzPrivateLinkServiceIpConfig.</span><span class="sxs-lookup"><span data-stu-id="1b379-976">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="1b379-977">Параметр PublicIpAddress объявлен нерекомендуемым, так как он не используется на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="1b379-977">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="1b379-978">Добавлен необязательный параметр Primary, указывающий, является ли текущая IP-конфигурация основной.</span><span class="sxs-lookup"><span data-stu-id="1b379-978">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="1b379-979">Улучшена обработка исключений из-за ошибок запроса от пакета SDK. Устранена проблема, при которой исключения пакета SDK не обрабатывались правильно, из-за чего не отображались основные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="1b379-979">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="1b379-980">Настроена логика проверки для префикса IPv6 IP-адреса для проверки правильности длины префикса IPv6.</span><span class="sxs-lookup"><span data-stu-id="1b379-980">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="1b379-981">Обновлен Get-AzVirtualNetworkSubnetConfig: добавлен набор параметров для получения по идентификатору ресурса подсети.</span><span class="sxs-lookup"><span data-stu-id="1b379-981">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="1b379-982">Обновлено описание параметра Location для AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="1b379-982">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="1b379-983">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1b379-983">Az.OperationalInsights</span></span>
* <span data-ttu-id="1b379-984">Обновлена документация по New-AzOperationalInsightsLinuxSyslogDataSource.</span><span class="sxs-lookup"><span data-stu-id="1b379-984">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="1b379-985">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="1b379-985">Added example</span></span>
    - <span data-ttu-id="1b379-986">Обновлено описание параметра -Name.</span><span class="sxs-lookup"><span data-stu-id="1b379-986">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="1b379-987">Добавлен пример для New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="1b379-987">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="1b379-988">Изменено описание параметра -Name для New-AzOperationalInsightsWindowsEventDataSource.</span><span class="sxs-lookup"><span data-stu-id="1b379-988">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1b379-989">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1b379-989">Az.RecoveryServices</span></span>
* <span data-ttu-id="1b379-990">Обновлен Get-AzRecoveryServicesBackupJobDetail.md.</span><span class="sxs-lookup"><span data-stu-id="1b379-990">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="1b379-991">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1b379-991">Az.Resources</span></span>
* <span data-ttu-id="1b379-992">Добавлена поддержка новой версии API 2019-05-10 для Microsoft.Resource.</span><span class="sxs-lookup"><span data-stu-id="1b379-992">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="1b379-993">Добавлена поддержка copy.count = 0 для переменных, ресурсов и свойств.</span><span class="sxs-lookup"><span data-stu-id="1b379-993">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="1b379-994">Ресурсы, у которых condition = false или copy.count = 0, будут удаляться в полном режиме.</span><span class="sxs-lookup"><span data-stu-id="1b379-994">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="1b379-995">В справочную документацию добавлен пример назначения политики на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="1b379-995">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="1b379-996">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1b379-996">Az.ServiceBus</span></span>
* <span data-ttu-id="1b379-997">Исправлена проблема № 9658: опечатка в написании параметра VirtualNetworkRule В Set-AzServiceBusNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="1b379-997">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="1b379-998">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="1b379-998">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="1b379-999">Добавлена новая команда Test-AzServiceBusNameAvailability для проверки доступности имени для очереди и раздела.</span><span class="sxs-lookup"><span data-stu-id="1b379-999">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="1b379-1000">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1b379-1000">Az.ServiceFabric</span></span>
* <span data-ttu-id="1b379-1001">Устранены ошибки командлета для добавления типа узла:</span><span class="sxs-lookup"><span data-stu-id="1b379-1001">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="1b379-1002">ошибка NullReferenceException, возникавшая, если у группы ресурсов были другие VMSS, не связанные с кластером Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="1b379-1002">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="1b379-1003">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8681.</span><span class="sxs-lookup"><span data-stu-id="1b379-1003">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="1b379-1004">Исправлена ошибка, из-за которой командлет завершился сбоем, если virtualNetwork находилась не в той группе ресурсов, к которой относится кластер.</span><span class="sxs-lookup"><span data-stu-id="1b379-1004">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="1b379-1005">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8407.</span><span class="sxs-lookup"><span data-stu-id="1b379-1005">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="1b379-1006">Командлет Add-AzServiceFabricApplicationCertificate объявлен нерекомендуемым.</span><span class="sxs-lookup"><span data-stu-id="1b379-1006">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="1b379-1007">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1b379-1007">Az.Sql</span></span>
* <span data-ttu-id="1b379-1008">Обновление документации по старым командлетам аудита.</span><span class="sxs-lookup"><span data-stu-id="1b379-1008">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1b379-1009">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1b379-1009">Az.Storage</span></span>
* <span data-ttu-id="1b379-1010">Обновлена справка по Get/Close-AzStorageFileHandle: в примеры добавлены сценарии использования командлетов и обновлено описание параметров.</span><span class="sxs-lookup"><span data-stu-id="1b379-1010">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="1b379-1011">Добавлена поддержка StandardBlobTier в операции отправки BLOB-объекта и копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="1b379-1011">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="1b379-1012">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="1b379-1012">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="1b379-1013">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="1b379-1013">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="1b379-1014">Добавлена поддержка приоритета восстановления в операцию копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="1b379-1014">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="1b379-1015">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="1b379-1015">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1b379-1016">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1b379-1016">Az.Websites</span></span>
* <span data-ttu-id="1b379-1017">Добавлены уточнение для параметра -AppSettings в Set-AzWebApp и Set-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="1b379-1017">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="1b379-1018">2.5.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="1b379-1018">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1b379-1019">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1b379-1019">Az.Accounts</span></span>
* <span data-ttu-id="1b379-1020">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1b379-1020">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="1b379-1021">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="1b379-1021">Az.ApplicationInsights</span></span>
* <span data-ttu-id="1b379-1022">Исправлена опечатка в примере в документации по Remove-AzApplicationInsightsApiKey.</span><span class="sxs-lookup"><span data-stu-id="1b379-1022">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1b379-1023">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1b379-1023">Az.Automation</span></span>
* <span data-ttu-id="1b379-1024">Исправлена опечатка в строке ресурса.</span><span class="sxs-lookup"><span data-stu-id="1b379-1024">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="1b379-1025">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1b379-1025">Az.CognitiveServices</span></span>
* <span data-ttu-id="1b379-1026">Добавлена поддержка NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="1b379-1026">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1b379-1027">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1b379-1027">Az.Compute</span></span>
* <span data-ttu-id="1b379-1028">Добавлены недостающие свойства (ComputerName, OsName, OsVersion и HyperVGeneration) для объекта представления экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1b379-1028">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="1b379-1029">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1b379-1029">Az.ContainerRegistry</span></span>
* <span data-ttu-id="1b379-1030">Исправлена опечатка в Remove-AzContainerRegistryReplication для параметра репликации.</span><span class="sxs-lookup"><span data-stu-id="1b379-1030">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="1b379-1031">См. подробнее: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="1b379-1031">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1b379-1032">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1b379-1032">Az.DataFactory</span></span>
* <span data-ttu-id="1b379-1033">Пакет SDK для ADF .NET обновлен до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="1b379-1033">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="1b379-1034">Исправлена опечатка в документации по Get-AzDataFactoryV2PipelineRun.</span><span class="sxs-lookup"><span data-stu-id="1b379-1034">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="1b379-1035">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="1b379-1035">Az.EventHub</span></span>
* <span data-ttu-id="1b379-1036">Добавлен новый командлет для создания маркера SAS: New-AzEventHubAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="1b379-1036">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="1b379-1037">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="1b379-1037">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1b379-1038">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1b379-1038">Az.KeyVault</span></span>
* <span data-ttu-id="1b379-1039">Добавлена поддержка для настройки параметра KeySize в политиках сертификатов.</span><span class="sxs-lookup"><span data-stu-id="1b379-1039">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="1b379-1040">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="1b379-1040">Az.LogicApp</span></span>
* <span data-ttu-id="1b379-1041">Get-AzIntegrationAccountMap теперь надлежащим образом выводит все типы сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="1b379-1041">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="1b379-1042">Добавлен новый параметр MapType для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="1b379-1042">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="1b379-1043">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="1b379-1043">Az.ManagedServices</span></span>
* <span data-ttu-id="1b379-1044">Добавлена поддержка API версии 2019-06-01 (общедоступная).</span><span class="sxs-lookup"><span data-stu-id="1b379-1044">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1b379-1045">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1b379-1045">Az.Network</span></span>
* <span data-ttu-id="1b379-1046">Добавлена поддержка частной конечной точки и службы приватного канала.</span><span class="sxs-lookup"><span data-stu-id="1b379-1046">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="1b379-1047">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="1b379-1047">New cmdlets</span></span>
        - <span data-ttu-id="1b379-1048">Set-AzPrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="1b379-1048">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="1b379-1049">Set-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="1b379-1049">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="1b379-1050">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="1b379-1050">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="1b379-1051">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="1b379-1051">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="1b379-1052">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="1b379-1052">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="1b379-1053">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="1b379-1053">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="1b379-1054">Test-AzPrivateLinkServiceVisibility.</span><span class="sxs-lookup"><span data-stu-id="1b379-1054">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="1b379-1055">Get-AzAutoApprovedPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="1b379-1055">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="1b379-1056">Обновлены следующие команды для функции: Флаг PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies в подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="1b379-1056">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="1b379-1057">Обновлены командлеты New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig.</span><span class="sxs-lookup"><span data-stu-id="1b379-1057">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="1b379-1058">Добавлен необязательный параметр -PrivateEndpointNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к частной конечной точке в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="1b379-1058">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="1b379-1059">Добавлен необязательный параметр -PrivateLinkServiceNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к службе приватного канала в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="1b379-1059">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="1b379-1060">Параметр ServiceName командлета AzPrivateLinkService был переименован на Name с псевдонимом ServiceName для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="1b379-1060">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="1b379-1061">Включен протокол ICMP для настройки правил безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="1b379-1061">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="1b379-1062">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="1b379-1062">Updated cmdlets</span></span>
        - <span data-ttu-id="1b379-1063">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="1b379-1063">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="1b379-1064">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="1b379-1064">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="1b379-1065">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="1b379-1065">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="1b379-1066">Добавлен ConnectionProtocolType (Ikev1/Ikev2) в качестве настраиваемого параметра для командлета New-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="1b379-1066">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="1b379-1067">Добавлен PrivateIpAddressVersion в LoadBalancerFrontendIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1b379-1067">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="1b379-1068">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="1b379-1068">Updated cmdlet:</span></span>
        - <span data-ttu-id="1b379-1069">New-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="1b379-1069">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="1b379-1070">Add-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="1b379-1070">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="1b379-1071">Set-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="1b379-1071">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="1b379-1072">Команда New-AzApplicationGatewayProbeConfig Шлюза приложений обновлена для поддержки настраиваемого порта в зонде.</span><span class="sxs-lookup"><span data-stu-id="1b379-1072">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="1b379-1073">Обновлен командлет New-AzApplicationGatewayProbeConfig: добавлен необязательный параметр Port, который используется при проверке внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="1b379-1073">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="1b379-1074">Этот параметр применяется к номерам SKU Standard_V2 и WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="1b379-1074">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="1b379-1075">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1b379-1075">Az.OperationalInsights</span></span>
* <span data-ttu-id="1b379-1076">Обновленная версия по умолчанию для сохраненных операций поиска имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="1b379-1076">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="1b379-1077">Исправлены ошибки при обработке регулярных выражений со значениями NULL в журналах.</span><span class="sxs-lookup"><span data-stu-id="1b379-1077">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1b379-1078">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1b379-1078">Az.RecoveryServices</span></span>
* <span data-ttu-id="1b379-1079">Обновлен файл Get-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="1b379-1079">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="1b379-1080">Обновлен файл Get-AzRecoveryServicesBackupContainer.md.</span><span class="sxs-lookup"><span data-stu-id="1b379-1080">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="1b379-1081">Обновлен файл Get-AzRecoveryServicesVault.md.</span><span class="sxs-lookup"><span data-stu-id="1b379-1081">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="1b379-1082">Обновлен файл Wait-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="1b379-1082">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="1b379-1083">Обновлен файл Set-AzRecoveryServicesVaultContext.md.</span><span class="sxs-lookup"><span data-stu-id="1b379-1083">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="1b379-1084">Обновлен файл Get-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="1b379-1084">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="1b379-1085">Обновлен файл Get-AzRecoveryServicesBackupRecoveryPoint.md.</span><span class="sxs-lookup"><span data-stu-id="1b379-1085">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="1b379-1086">Обновлен файл Restore-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="1b379-1086">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="1b379-1087">Обновлен вызов службы для отмены регистрации контейнера в общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="1b379-1087">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="1b379-1088">Обновлен файл Set-AzRecoveryServicesAsrAlertSetting.md.</span><span class="sxs-lookup"><span data-stu-id="1b379-1088">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="1b379-1089">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1b379-1089">Az.Resources</span></span>
- <span data-ttu-id="1b379-1090">Удален отсутствующий командлет, который упоминается в документации по New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="1b379-1090">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="1b379-1091">Обновлены командлеты политик для использования новой версии API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="1b379-1091">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="1b379-1092">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1b379-1092">Az.ServiceBus</span></span>
* <span data-ttu-id="1b379-1093">Добавлен новый командлет для создания маркера SAS: New-AzServiceBusAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="1b379-1093">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="1b379-1094">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="1b379-1094">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="1b379-1095">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1b379-1095">Az.Sql</span></span>
* <span data-ttu-id="1b379-1096">Исправлены отсутствующие примеры для командлета Set-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="1b379-1096">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="1b379-1097">Исправлены заданные повторяющиеся проверки для оценки наличия уязвимостей без указания адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="1b379-1097">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="1b379-1098">Исправлена незначительная опечатка в сообщении предупреждения.</span><span class="sxs-lookup"><span data-stu-id="1b379-1098">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1b379-1099">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1b379-1099">Az.Storage</span></span>
* <span data-ttu-id="1b379-1100">Обновлен пример в справочной документации для использования командлетом Get-AzStorageAccount правильного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="1b379-1100">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="1b379-1101">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="1b379-1101">Az.StorageSync</span></span>
* <span data-ttu-id="1b379-1102">Добавлен командлет Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="1b379-1102">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="1b379-1103">Исправлена проблема № 9551, связанная с TierFilesOlderThanDays.</span><span class="sxs-lookup"><span data-stu-id="1b379-1103">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1b379-1104">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1b379-1104">Az.Websites</span></span>
* <span data-ttu-id="1b379-1105">Исправлена ошибка, при которой некоторые свойства SiteConfig не возвращались Get-AzWebApp и Set-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="1b379-1105">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="1b379-1106">Добавлен новый параметр Location в Get-AzDeletedWebApp и Restore-AzDeletedWebApp.</span><span class="sxs-lookup"><span data-stu-id="1b379-1106">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="1b379-1107">Исправлена ошибка, которая возникала при клонировании слотов веб-приложений с помощью командлета New-AzWebApp-IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="1b379-1107">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="1b379-1108">2.4.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="1b379-1108">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1b379-1109">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1b379-1109">Az.Accounts</span></span>
* <span data-ttu-id="1b379-1110">Добавлена поддержка командлетов профиля.</span><span class="sxs-lookup"><span data-stu-id="1b379-1110">Add support for profile cmdlets</span></span>
* <span data-ttu-id="1b379-1111">Добавлена поддержка сред и плоскостей данных в созданных командлетах.</span><span class="sxs-lookup"><span data-stu-id="1b379-1111">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="1b379-1112">Исправлена ошибка, когда в командлетах плоскости данных в Windows PowerShell в некоторых случаях использовалась неправильная конечная точка.</span><span class="sxs-lookup"><span data-stu-id="1b379-1112">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="1b379-1113">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="1b379-1113">Az.Advisor</span></span>
* <span data-ttu-id="1b379-1114">Выпущена общедоступная версия Az.Advisor.</span><span class="sxs-lookup"><span data-stu-id="1b379-1114">GA release of Az.Advisor</span></span>
* <span data-ttu-id="1b379-1115">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="1b379-1115">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="1b379-1116">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1b379-1116">Az.ApiManagement</span></span>
* <span data-ttu-id="1b379-1117">исправлена проблема https://github.com/Azure/azure-powershell/issues/8671.</span><span class="sxs-lookup"><span data-stu-id="1b379-1117">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="1b379-1118">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="1b379-1118">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="1b379-1119">Добавлена поддержка запрашивания подписок по пользователю и продукту.</span><span class="sxs-lookup"><span data-stu-id="1b379-1119">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="1b379-1120">Добавлена поддержка создания запросов с использованием области "/", "/apis", "/apis/echo-api".</span><span class="sxs-lookup"><span data-stu-id="1b379-1120">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="1b379-1121">Исправлены проблемы https://github.com/Azure/azure-powershell/issues/9307 и https://github.com/Azure/azure-powershell/issues/8432.</span><span class="sxs-lookup"><span data-stu-id="1b379-1121">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="1b379-1122">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="1b379-1122">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="1b379-1123">Добавлена поддержка указания ApiVersion и ApiVersionSetId при импорте API-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="1b379-1123">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1b379-1124">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1b379-1124">Az.Automation</span></span>
* <span data-ttu-id="1b379-1125">Исправлена ошибка командлета Set-AzAutomationConnectionFieldValue при обработке строкового значения.</span><span class="sxs-lookup"><span data-stu-id="1b379-1125">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1b379-1126">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1b379-1126">Az.Compute</span></span>
* <span data-ttu-id="1b379-1127">В New AzImageConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="1b379-1127">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1b379-1128">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1b379-1128">Az.DataFactory</span></span>
* <span data-ttu-id="1b379-1129">Обновление выходных данных командлетов ADF, предназначенных для получения числа выполнений действий, конвейеров и триггеров, для поддержки канала Select-Object.</span><span class="sxs-lookup"><span data-stu-id="1b379-1129">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="1b379-1130">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="1b379-1130">Az.EventGrid</span></span>
* <span data-ttu-id="1b379-1131">Исправлена опечатка в документации по командлету New-AzEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="1b379-1131">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1b379-1132">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1b379-1132">Az.IotHub</span></span>
* <span data-ttu-id="1b379-1133">Добавлена поддержка повторного создания ключей политики авторизации.</span><span class="sxs-lookup"><span data-stu-id="1b379-1133">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1b379-1134">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1b379-1134">Az.Network</span></span>
* <span data-ttu-id="1b379-1135">К тегам общедоступного IP-адреса добавлен тег RoutingPreference.</span><span class="sxs-lookup"><span data-stu-id="1b379-1135">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="1b379-1136">Улучшены примеры для справочной документации по командлету Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="1b379-1136">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="1b379-1137">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="1b379-1137">Az.PolicyInsights</span></span>
* <span data-ttu-id="1b379-1138">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="1b379-1138">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="1b379-1139">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9446.</span><span class="sxs-lookup"><span data-stu-id="1b379-1139">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="1b379-1140">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1b379-1140">Az.OperationalInsights</span></span>
* <span data-ttu-id="1b379-1141">Исправленная модель источника данных CustomLog возвращена в командлет Get-AzOperationalInsightsDataSource.</span><span class="sxs-lookup"><span data-stu-id="1b379-1141">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1b379-1142">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1b379-1142">Az.RecoveryServices</span></span>
* <span data-ttu-id="1b379-1143">Выпущено исправление для команды get-policy для виртуальных машин IaaS.</span><span class="sxs-lookup"><span data-stu-id="1b379-1143">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="1b379-1144">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1b379-1144">Az.Resources</span></span>
    - <span data-ttu-id="1b379-1145">Исправлен текст справки по параметру Get-AzPolicyState -Top.</span><span class="sxs-lookup"><span data-stu-id="1b379-1145">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="1b379-1146">Добавлена поддержка разбиения по страницам на стороне клиента для Get-AzPolicyAlias.</span><span class="sxs-lookup"><span data-stu-id="1b379-1146">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="1b379-1147">Добавлены новые параметры для Set-AzPolicyAssignment, -PolicyParameters и -PolicyParametersObject.</span><span class="sxs-lookup"><span data-stu-id="1b379-1147">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="1b379-1148">Добавлен ряд обновлений документов и примеров для командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="1b379-1148">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="1b379-1149">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1b379-1149">Az.ServiceBus</span></span>
* <span data-ttu-id="1b379-1150">Исправление ошибки № 4938: командлет New-AzureRmServiceBusQueue возвращает ответ BadRequest (Недопустимый запрос) при задании значения MaxSizeInMegabytes.</span><span class="sxs-lookup"><span data-stu-id="1b379-1150">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="1b379-1151">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1b379-1151">Az.Sql</span></span>
* <span data-ttu-id="1b379-1152">Из выпуска предварительной версии в выпуск общедоступной версии добавлены командлеты группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="1b379-1152">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="1b379-1153">Поддержка аудита Azure SQL Server и баз данных с помощью новых командлетов:</span><span class="sxs-lookup"><span data-stu-id="1b379-1153">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="1b379-1154">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="1b379-1154">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="1b379-1155">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="1b379-1155">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="1b379-1156">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="1b379-1156">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="1b379-1157">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="1b379-1157">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="1b379-1158">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="1b379-1158">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="1b379-1159">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="1b379-1159">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="1b379-1160">Из параметров оценки уязвимостей удалены ограничения, касающиеся электронной почты.</span><span class="sxs-lookup"><span data-stu-id="1b379-1160">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1b379-1161">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1b379-1161">Az.Storage</span></span>
* <span data-ttu-id="1b379-1162">Два параметра в указанном ниже командлете — -IndexDocument и -ErrorDocument404Path, — которые ранее были обязательными, стали необязательными:</span><span class="sxs-lookup"><span data-stu-id="1b379-1162">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="1b379-1163">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="1b379-1163">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="1b379-1164">Обновлена справка по командлету Get-AzStorageBlobContent: добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="1b379-1164">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="1b379-1165">При сбое выполнения командлета с ошибкой StorageException отображаются дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="1b379-1165">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="1b379-1166">Добавлена поддержка создания или обновления учетной записи хранения с использованием проверки подлинности AAD DS для службы "Файлы Azure".</span><span class="sxs-lookup"><span data-stu-id="1b379-1166">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="1b379-1167">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1b379-1167">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="1b379-1168">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1b379-1168">Set-AzStorageAccount</span></span>
* <span data-ttu-id="1b379-1169">Добавлена поддержка перечисления или закрытия дескрипторов файлов для общей папки, каталога файлов или файла:</span><span class="sxs-lookup"><span data-stu-id="1b379-1169">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="1b379-1170">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="1b379-1170">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="1b379-1171">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="1b379-1171">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="1b379-1172">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="1b379-1172">Az.StorageSync</span></span>
* <span data-ttu-id="1b379-1173">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="1b379-1173">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="1b379-1174">2.3.2 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="1b379-1174">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1b379-1175">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1b379-1175">Az.Accounts</span></span>
* <span data-ttu-id="1b379-1176">Исправлена ошибка, связанная с использованием неправильного URL-адреса для вызовов функций.</span><span class="sxs-lookup"><span data-stu-id="1b379-1176">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="1b379-1177">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8983.</span><span class="sxs-lookup"><span data-stu-id="1b379-1177">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="1b379-1178">Устранена проблема с псевдонимами из AzureRM для командлетов Az.</span><span class="sxs-lookup"><span data-stu-id="1b379-1178">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="1b379-1179">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="1b379-1179">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="1b379-1180">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest.</span><span class="sxs-lookup"><span data-stu-id="1b379-1180">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1b379-1181">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1b379-1181">Az.Compute</span></span>
* <span data-ttu-id="1b379-1182">Простые наборы параметров New-AzVm и New-AzVmss теперь принимают параметр ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="1b379-1182">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="1b379-1183">Исправлена опечатка в справочной документации по New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="1b379-1183">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="1b379-1184">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="1b379-1184">Az.Dns</span></span>
* <span data-ttu-id="1b379-1185">Исправлена опечатка в справочных примерах по использованию Set-AzDnsZone.</span><span class="sxs-lookup"><span data-stu-id="1b379-1185">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="1b379-1186">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="1b379-1186">Az.EventGrid</span></span>
* <span data-ttu-id="1b379-1187">Обновлен для использования API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="1b379-1187">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="1b379-1188">Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="1b379-1188">New cmdlets:</span></span>
    - <span data-ttu-id="1b379-1189">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="1b379-1189">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="1b379-1190">Создает домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="1b379-1190">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="1b379-1191">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="1b379-1191">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="1b379-1192">Возвращает сведения о домене Сетки событий или список всех доменов Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="1b379-1192">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="1b379-1193">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="1b379-1193">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="1b379-1194">Удаляет домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="1b379-1194">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="1b379-1195">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="1b379-1195">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="1b379-1196">Повторно создает ключ общего доступа для домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="1b379-1196">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="1b379-1197">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="1b379-1197">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="1b379-1198">Возвращает ключи общего доступа, используемые для публикации событий в домене Сетки событий.</span><span class="sxs-lookup"><span data-stu-id="1b379-1198">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="1b379-1199">New-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="1b379-1199">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="1b379-1200">Создает раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="1b379-1200">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="1b379-1201">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="1b379-1201">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="1b379-1202">Возвращает сведения о разделе домена Сетки событий или список всех разделов определенного домена Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="1b379-1202">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="1b379-1203">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="1b379-1203">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="1b379-1204">Удаляет раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="1b379-1204">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="1b379-1205">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="1b379-1205">Updated cmdlets:</span></span>
    - <span data-ttu-id="1b379-1206">New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="1b379-1206">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="1b379-1207">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для нового домена Сетки событий и раздела домена Сетки событий и позволяющие создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="1b379-1207">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="1b379-1208">Добавляют новые обязательные параметры для указания имени нового домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="1b379-1208">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="1b379-1209">Добавляют новые наборы параметров для доменов и разделов домена и позволяют повторно использовать существующие параметры (например, EndPointType, SubjectBeginsWith и т. д.).</span><span class="sxs-lookup"><span data-stu-id="1b379-1209">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="1b379-1210">Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="1b379-1210">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="1b379-1211">срока действия подписки на событие;</span><span class="sxs-lookup"><span data-stu-id="1b379-1211">Event subscription expiration date,</span></span>
            - <span data-ttu-id="1b379-1212">параметров расширенной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="1b379-1212">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="1b379-1213">Добавляют новое перечисление для ServiceBusQueue в качестве места назначения.</span><span class="sxs-lookup"><span data-stu-id="1b379-1213">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="1b379-1214">Запрещают использование значение All в параметре -IncludedEventType и заменяют его следующим:</span><span class="sxs-lookup"><span data-stu-id="1b379-1214">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="1b379-1215">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="1b379-1215">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="1b379-1216">Добавляют новые необязательные параметры (Top, ODataQuery и NextLink) для поддержки разбиения на страницы и фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="1b379-1216">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="1b379-1217">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="1b379-1217">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="1b379-1218">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для домена Сетки событий и раздела домена Сетки событий и позволяющие удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="1b379-1218">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="1b379-1219">Добавляют новые обязательные параметры для указания имени домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="1b379-1219">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="1b379-1220">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="1b379-1220">Az.FrontDoor</span></span>
* <span data-ttu-id="1b379-1221">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="1b379-1221">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="1b379-1222">Добавляет поддержку преобразований и новое значение оператора автозавершения (RegEx).</span><span class="sxs-lookup"><span data-stu-id="1b379-1222">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="1b379-1223">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="1b379-1223">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="1b379-1224">Добавляет новые значения автозавершения.</span><span class="sxs-lookup"><span data-stu-id="1b379-1224">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1b379-1225">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1b379-1225">Az.Network</span></span>
* <span data-ttu-id="1b379-1226">Добавляет поддержку ресурса шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="1b379-1226">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="1b379-1227">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="1b379-1227">New cmdlets</span></span>
        - <span data-ttu-id="1b379-1228">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="1b379-1228">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="1b379-1229">Добавляет AvailablePrivateEndpointType.</span><span class="sxs-lookup"><span data-stu-id="1b379-1229">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="1b379-1230">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="1b379-1230">New cmdlets</span></span>
        - <span data-ttu-id="1b379-1231">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="1b379-1231">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="1b379-1232">Добавляет PrivatePrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="1b379-1232">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="1b379-1233">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="1b379-1233">New cmdlets</span></span>
        - <span data-ttu-id="1b379-1234">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="1b379-1234">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="1b379-1235">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="1b379-1235">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="1b379-1236">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="1b379-1236">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="1b379-1237">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="1b379-1237">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="1b379-1238">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1b379-1238">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="1b379-1239">Добавляет PrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="1b379-1239">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="1b379-1240">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="1b379-1240">New cmdlets</span></span>
        - <span data-ttu-id="1b379-1241">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="1b379-1241">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="1b379-1242">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="1b379-1242">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="1b379-1243">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="1b379-1243">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="1b379-1244">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="1b379-1244">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="1b379-1245">Обновлены следующие команды для функции: флаг UseLocalAzureIpAddress для VPN-подключения.</span><span class="sxs-lookup"><span data-stu-id="1b379-1245">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="1b379-1246">Обновлен командлет New-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="1b379-1246">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="1b379-1247">Обновлен командлет Set-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="1b379-1247">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="1b379-1248">В пиринг ExpressRoute добавлено поле только для чтения PeeredConnections.</span><span class="sxs-lookup"><span data-stu-id="1b379-1248">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="1b379-1249">В ExpressRoute добавлено поле только для чтения GlobalReachEnabled.</span><span class="sxs-lookup"><span data-stu-id="1b379-1249">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="1b379-1250">Добавлен атрибут в рамках критического изменения, отменяющего статус устаревшего поля AllowGlobalReach в модели ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="1b379-1250">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="1b379-1251">Исправлена проблема, связанная с ошибкой 8756, при использовании TargetListenerID с командлетами AzApplicationGatewayRedirectConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1b379-1251">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="1b379-1252">Исправлена ошибка в New-AzApplicationGatewayPathRuleConfig, не позволявшая задавать набор правил повторного создания.</span><span class="sxs-lookup"><span data-stu-id="1b379-1252">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="1b379-1253">Исправлено отображение VirtualNetworkTaps в NetworkInterfaceIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1b379-1253">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="1b379-1254">Исправлены командлеты Cortex Get для отображения всех частей.</span><span class="sxs-lookup"><span data-stu-id="1b379-1254">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="1b379-1255">Исправлено создание ссылок VirtualHub для ExpressRouteGateways и VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="1b379-1255">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="1b379-1256">В AzureFirewall и NatGateway добавлена поддержка Зон доступности.</span><span class="sxs-lookup"><span data-stu-id="1b379-1256">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="1b379-1257">Добавлен командлет Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="1b379-1257">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="1b379-1258">Добавлена поддержка нескольких общедоступных IP-адресов для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="1b379-1258">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="1b379-1259">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="1b379-1259">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="1b379-1260">Добавлен параметр -PublicIpAddress, который принимает один или несколько объектов общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="1b379-1260">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="1b379-1261">Добавлен параметр -VirtualNetwork, который принимает объект виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="1b379-1261">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="1b379-1262">Добавлены методы AddPublicIpAddress и RemovePublicIpAddress для объекта брандмауэра. Они принимают объект общедоступного IP-адреса в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="1b379-1262">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="1b379-1263">Не рекомендуется использовать параметры -PublicIpName и -VirtualNetworkName.</span><span class="sxs-lookup"><span data-stu-id="1b379-1263">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="1b379-1264">Обновлены следующие команды для функции: В параметрах проверки подлинности AAD VPN-клиента задан ресурс шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="1b379-1264">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="1b379-1265">Обновлен командлет New-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="1b379-1265">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="1b379-1266">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="1b379-1266">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="1b379-1267">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр-переключатель RemoveAadAuthentication для удаления в шлюзе параметров проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="1b379-1267">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="1b379-1268">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1b379-1268">Az.OperationalInsights</span></span>
* <span data-ttu-id="1b379-1269">Добавлена поддержка SKU **pergb2018** в команде New-AzureRmOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="1b379-1269">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="1b379-1270">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1b379-1270">Az.Resources</span></span>
* <span data-ttu-id="1b379-1271">Поддержка дополнительных вариантов экспорта шаблона.</span><span class="sxs-lookup"><span data-stu-id="1b379-1271">Support for additional Template Export options</span></span>
    - <span data-ttu-id="1b379-1272">В Export-AzResourceGroup добавлен параметр -SkipResourceNameParameterization.</span><span class="sxs-lookup"><span data-stu-id="1b379-1272">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="1b379-1273">В Export-AzResourceGroup добавлен параметр -SkipAllParameterization.</span><span class="sxs-lookup"><span data-stu-id="1b379-1273">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="1b379-1274">В Export-AzResourceGroup добавлен параметр -Resource для фильтрации экспортированных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1b379-1274">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="1b379-1275">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1b379-1275">Az.ServiceFabric</span></span>
* <span data-ttu-id="1b379-1276">Исправлена ошибка, связанная с получением иногда неправильных отпечатков при добавлении сертификата ByExistingKeyVault.</span><span class="sxs-lookup"><span data-stu-id="1b379-1276">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="1b379-1277">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1b379-1277">Az.Sql</span></span>
* <span data-ttu-id="1b379-1278">Исправлен суффикс конечной точки хранилища службы "Расширенная защита от угроз Azure".</span><span class="sxs-lookup"><span data-stu-id="1b379-1278">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="1b379-1279">Исправлена ошибка, связанная с возможностью пакета "Расширенная защита данных" переопределять политику службы "Расширенная защита от угроз".</span><span class="sxs-lookup"><span data-stu-id="1b379-1279">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="1b379-1280">Новые командлеты для Management.Sql позволяют клиентам добавлять ключи TDE и задавать средство защиты TDE для управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="1b379-1280">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="1b379-1281">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1b379-1281">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="1b379-1282">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1b379-1282">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="1b379-1283">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1b379-1283">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="1b379-1284">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="1b379-1284">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="1b379-1285">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="1b379-1285">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1b379-1286">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1b379-1286">Az.Storage</span></span>
* <span data-ttu-id="1b379-1287">Поддержка класса Kind в FileStorage и значения Premium_ZRS в SkuName при создании учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="1b379-1287">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="1b379-1288">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1b379-1288">New-AzStorageAccount</span></span>
* <span data-ttu-id="1b379-1289">Уточнено описание командлета неизменности BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="1b379-1289">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="1b379-1290">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1b379-1290">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1b379-1291">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1b379-1291">Az.Websites</span></span>
* <span data-ttu-id="1b379-1292">Оптимизирует Get-AzWebAppCertificate для фильтрации по группе ресурсов на сервере, а не в клиенте.</span><span class="sxs-lookup"><span data-stu-id="1b379-1292">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="1b379-1293">Добавляет параметр-переключатель - UseDisasterRecovery в Get AzWebAppSnapshot.</span><span class="sxs-lookup"><span data-stu-id="1b379-1293">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="1b379-1294">2.2.0 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="1b379-1294">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="1b379-1295">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="1b379-1295">Az.Cdn</span></span>
* <span data-ttu-id="1b379-1296">Обновлены командлеты для поддержки функции rulesEngine на основе API версии 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="1b379-1296">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1b379-1297">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1b379-1297">Az.Compute</span></span>
* <span data-ttu-id="1b379-1298">Добавлен параметр `NoWait`, который запускает операцию и немедленно возвращает значение еще до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="1b379-1298">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="1b379-1299">Обновлены командлеты:   Export-AzLogAnalyticRequestRateByInterval; Export-AzLogAnalyticThrottledRequest; Remove-AzVM; Remove-AzVMAccessExtension; Remove-AzVMAEMExtension; Remove-AzVMChefExtension; Remove-AzVMCustomScriptExtension; Remove-AzVMDiagnosticsExtension; Remove-AzVMDiskEncryptionExtension; Remove-AzVMDscExtension; Remove-AzVMSqlServerExtension; Restart-AzVM; Set-AzVM; Set-AzVMAccessExtension; Set-AzVMADDomainExtension; Set-AzVMAEMExtension; Set-AzVMBginfoExtension; Set-AzVMChefExtension; Set-AzVMCustomScriptExtension; Set-AzVMDiagnosticsExtension; Set-AzVMDscExtension; Set-AzVMExtension; Start-AzVM; Stop-AzVM; Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="1b379-1299">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="1b379-1300">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="1b379-1300">Az.EventHub</span></span>
* <span data-ttu-id="1b379-1301">Исправлена ошибка № 9231. Командлет Get-AzEventHubNamespace не возвращал теги.</span><span class="sxs-lookup"><span data-stu-id="1b379-1301">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="1b379-1302">Исправлена ошибка № 9230. Командлет Get-AzEventHubNamespace возвращал значение ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="1b379-1302">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1b379-1303">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1b379-1303">Az.Network</span></span>
* <span data-ttu-id="1b379-1304">Обновлены параметры ResourceId и InputObject для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="1b379-1304">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="1b379-1305">Добавлены псевдонимы для параметров ResourceId и InputObject.</span><span class="sxs-lookup"><span data-stu-id="1b379-1305">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="1b379-1306">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="1b379-1306">Az.PolicyInsights</span></span>
* <span data-ttu-id="1b379-1307">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyEvent.</span><span class="sxs-lookup"><span data-stu-id="1b379-1307">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1b379-1308">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1b379-1308">Az.RecoveryServices</span></span>
* <span data-ttu-id="1b379-1309">Минимальный срок хранения политики IaaSVM изменился с 1 до 7 дней.</span><span class="sxs-lookup"><span data-stu-id="1b379-1309">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="1b379-1310">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1b379-1310">Az.ServiceBus</span></span>
* <span data-ttu-id="1b379-1311">Исправлена ошибка № 9182. Командлет Get-AzServiceBusNamespace возвращал ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="1b379-1311">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="1b379-1312">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1b379-1312">Az.ServiceFabric</span></span>
* <span data-ttu-id="1b379-1313">Исправлена опечатка в сообщении об ошибке для командлета Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="1b379-1313">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="1b379-1314">Добавлен отсутствующий символ в командных строках Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="1b379-1314">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="1b379-1315">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1b379-1315">Az.Sql</span></span>
* <span data-ttu-id="1b379-1316">Для командлета New-AzureSqlInstance добавлен параметр DnsZonePartner, обеспечивающий поддержку AutoDr для Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="1b379-1316">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="1b379-1317">Командлет Get-AzSqlDatabaseSecureConnectionPolicy объявлен неподдерживаемым.</span><span class="sxs-lookup"><span data-stu-id="1b379-1317">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="1b379-1318">Командлеты обнаружения угроз переименованы в командлеты Расширенной защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="1b379-1318">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="1b379-1319">Параметры -StorageSizeInGB и -LicenseType командлета New-AzSqlInstance теперь необязательны.</span><span class="sxs-lookup"><span data-stu-id="1b379-1319">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1b379-1320">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1b379-1320">Az.Websites</span></span>
* <span data-ttu-id="1b379-1321">Исправлены проблемы, когда удалялись теги при использовании Set-AzWebApp и Set-AzWebAppSlot со свойством -WebApp.</span><span class="sxs-lookup"><span data-stu-id="1b379-1321">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="1b379-1322">2.1.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="1b379-1322">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="1b379-1323">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1b379-1323">Az.ApiManagement</span></span>
* <span data-ttu-id="1b379-1324">Созданы командлеты для управления диагностикой в глобальной области и в области API.</span><span class="sxs-lookup"><span data-stu-id="1b379-1324">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="1b379-1325">**Get-AzApiManagementDiagnostic** — получение диагностики, заданной глобально или на уровне области API.</span><span class="sxs-lookup"><span data-stu-id="1b379-1325">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="1b379-1326">**New-AzApiManagementDiagnostic** — создание диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="1b379-1326">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="1b379-1327">**New-AzApiManagementHttpMessageDiagnostic** — создание параметра диагностики, для которого регистрируются заголовки и размер байтов тела.</span><span class="sxs-lookup"><span data-stu-id="1b379-1327">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="1b379-1328">**New-AzApiManagementPipelineDiagnosticSetting** — создание параметров диагностики для сообщений HTTP, поступающих в шлюз или исходящих из него.</span><span class="sxs-lookup"><span data-stu-id="1b379-1328">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="1b379-1329">**New-AzApiManagementSamplingSetting** — создание параметра выборки для запросов и ответов касательно диагностики.</span><span class="sxs-lookup"><span data-stu-id="1b379-1329">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="1b379-1330">**Remove-AzApiManagementDiagnostic** — удаление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="1b379-1330">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="1b379-1331">**Set-AzApiManagementDiagnostic** — обновление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="1b379-1331">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="1b379-1332">Созданы командлеты для управления кэшем в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="1b379-1332">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="1b379-1333">**Get-AzApiManagementCache** — получение сведений о кэше, указанном идентификатором, или обо всех кэшах.</span><span class="sxs-lookup"><span data-stu-id="1b379-1333">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="1b379-1334">**New-AzApiManagementCache** — создание кэша по умолчанию или кэша в определенном регионе Azure.</span><span class="sxs-lookup"><span data-stu-id="1b379-1334">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="1b379-1335">**Remove-AzApiManagementCache** — удаление кэша.</span><span class="sxs-lookup"><span data-stu-id="1b379-1335">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="1b379-1336">**Update-AzApiManagementCache** — обновление кэша.</span><span class="sxs-lookup"><span data-stu-id="1b379-1336">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="1b379-1337">Созданы командлеты для управления схемой API.</span><span class="sxs-lookup"><span data-stu-id="1b379-1337">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="1b379-1338">**New-AzApiManagementSchema** — создание схемы для API.</span><span class="sxs-lookup"><span data-stu-id="1b379-1338">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="1b379-1339">**Get-AzApiManagementSchema** — получение схем, настроенных в API.</span><span class="sxs-lookup"><span data-stu-id="1b379-1339">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="1b379-1340">**Remove-AzApiManagementSchema** — удаление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="1b379-1340">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="1b379-1341">**Set-AzApiManagementSchema** — обновление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="1b379-1341">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="1b379-1342">Создан командлет для создания токена пользователя.</span><span class="sxs-lookup"><span data-stu-id="1b379-1342">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="1b379-1343">**New-AzApiManagementUserToken** — создание токена пользователя, по умолчанию действительного в течение 8 часов. С помощью этого командлета можно создавать токен для пользователя GIT.</span><span class="sxs-lookup"><span data-stu-id="1b379-1343">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="1b379-1344">Создан командлет для получения состояния сети.</span><span class="sxs-lookup"><span data-stu-id="1b379-1344">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="1b379-1345">**Get-AzApiManagementNetworkStatus** — получение состояния подключения сети ресурсов, от которых зависит служба "Управление API".</span><span class="sxs-lookup"><span data-stu-id="1b379-1345">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="1b379-1346">Это полезно при развертывании службы ApiManagement в виртуальной сети и проверке того, не нарушена ли какая-либо из зависимостей.</span><span class="sxs-lookup"><span data-stu-id="1b379-1346">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="1b379-1347">Обновлен командлет **New-AzApiManagement** для управления службой ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="1b379-1347">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="1b379-1348">Добавлена поддержка нового SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="1b379-1348">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="1b379-1349">Добавлена поддержка для включения флага EnableClientCertificate в SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="1b379-1349">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="1b379-1350">Новый командлет **New-AzApiManagementSslSetting** позволяет настраивать параметр TLS/SSL для сервера (Backend) и внешнего интерфейса (Frontend).</span><span class="sxs-lookup"><span data-stu-id="1b379-1350">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="1b379-1351">Его также можно использовать для настройки Ciphers как 3DES, в ServerProtocols как Http2 для внешнего интерфейса (Frontend) службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="1b379-1351">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="1b379-1352">Добавлена поддержка настройки имени узла DeveloperPortal в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="1b379-1352">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="1b379-1353">Обновлен командлет **Get-AzApiManagementSsoToken** для извлечения объекта PsApiManagement в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="1b379-1353">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="1b379-1354">Обновлен командлет для отображения встроенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="1b379-1354">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="1b379-1355">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Код ошибки: ValidationError. Сообщение об ошибке: "Некоторые поля содержат неправильные значения". Сведения об ошибке: [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="1b379-1355">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="1b379-1356">Обновлен командлет **Export-AzApiManagementApi** для экспортирования программных интерфейсов в формате OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="1b379-1356">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="1b379-1357">Обновлен командлет **Import-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="1b379-1357">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="1b379-1358">Для импортирования API из спецификации документа OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="1b379-1358">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="1b379-1359">Для переопределения свойства PsApiManagementSchema, указанного в любом документе (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="1b379-1359">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="1b379-1360">Для переопределения свойства ServiceUrl, указанного в любом документе.</span><span class="sxs-lookup"><span data-stu-id="1b379-1360">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="1b379-1361">Обновлен командлет **Get-AzApiManagementPolicy** для возврата политики в формате, экранированном не для XML, с использованием rawxml.</span><span class="sxs-lookup"><span data-stu-id="1b379-1361">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="1b379-1362">Обновлен командлет **Set-AzApiManagementPolicy**. Он принимает политику в формате, экранированном не для XML, с использованием rawxml и в формате, экранированном для XML, с использованием XML.</span><span class="sxs-lookup"><span data-stu-id="1b379-1362">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="1b379-1363">Обновлен командлет **New-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="1b379-1363">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="1b379-1364">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="1b379-1364">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="1b379-1365">Для создания API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="1b379-1365">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="1b379-1366">Для клонирования API с использованием значений SourceApiId и SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="1b379-1366">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="1b379-1367">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="1b379-1367">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="1b379-1368">Обновлен командлет **Set-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="1b379-1368">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="1b379-1369">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="1b379-1369">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="1b379-1370">Для обновления API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="1b379-1370">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="1b379-1371">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="1b379-1371">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="1b379-1372">Обновлен командлет **New-AzApiManagementRevision**:</span><span class="sxs-lookup"><span data-stu-id="1b379-1372">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="1b379-1373">Для клонирования (копирования тегов, продуктов, операций и политик) существующей редакции с использованием SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="1b379-1373">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="1b379-1374">Новая редакция предполагает родительский идентификатор ApiId.</span><span class="sxs-lookup"><span data-stu-id="1b379-1374">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="1b379-1375">Для предоставления ApiRevisionDescription.</span><span class="sxs-lookup"><span data-stu-id="1b379-1375">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="1b379-1376">Для переопределения значения ServiceUrl при клонировании API.</span><span class="sxs-lookup"><span data-stu-id="1b379-1376">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="1b379-1377">Обновлен командлет **New-AzApiManagementIdentityProvider**:</span><span class="sxs-lookup"><span data-stu-id="1b379-1377">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="1b379-1378">Для настройки AAD или AADB2C с Authority.</span><span class="sxs-lookup"><span data-stu-id="1b379-1378">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="1b379-1379">Для установки политик SignupPolicy, SigninPolicy, ProfileEditingPolicy и PasswordResetPolicy.</span><span class="sxs-lookup"><span data-stu-id="1b379-1379">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="1b379-1380">Обновлен командлет **New-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="1b379-1380">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="1b379-1381">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="1b379-1381">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="1b379-1382">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="1b379-1382">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="1b379-1383">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="1b379-1383">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="1b379-1384">Обновлен командлет **Set-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="1b379-1384">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="1b379-1385">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="1b379-1385">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="1b379-1386">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="1b379-1386">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="1b379-1387">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="1b379-1387">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="1b379-1388">Следующие командлеты обновлены, чтобы принимать значение ResourceId в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="1b379-1388">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="1b379-1389">New-AzApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="1b379-1389">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="1b379-1390">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="1b379-1390">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="1b379-1391">Get-AzApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="1b379-1391">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="1b379-1392">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="1b379-1392">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="1b379-1393">Get-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="1b379-1393">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="1b379-1394">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="1b379-1394">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="1b379-1395">Get-AzApiManagementAuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="1b379-1395">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="1b379-1396">Get-AzApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="1b379-1396">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="1b379-1397">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="1b379-1397">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="1b379-1398">Get-AzApiManagementCertificate.</span><span class="sxs-lookup"><span data-stu-id="1b379-1398">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="1b379-1399">Remove-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="1b379-1399">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="1b379-1400">Remove-AzApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="1b379-1400">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1b379-1401">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1b379-1401">Az.Automation</span></span>
* <span data-ttu-id="1b379-1402">Обновлен командлет Get-AzAutomationJobOutputRecord для обработки значений в формате JSON и в виде текстовой записи.</span><span class="sxs-lookup"><span data-stu-id="1b379-1402">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="1b379-1403">исправлена проблема https://github.com/Azure/azure-powershell/issues/7977.</span><span class="sxs-lookup"><span data-stu-id="1b379-1403">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="1b379-1404">исправлена проблема https://github.com/Azure/azure-powershell/issues/8600.</span><span class="sxs-lookup"><span data-stu-id="1b379-1404">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="1b379-1405">Поведение командлета Start-AzAutomationDscCompilationJob изменено так, чтобы сразу же запустить задание, а не ждать его завершения.</span><span class="sxs-lookup"><span data-stu-id="1b379-1405">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="1b379-1406">исправлена проблема https://github.com/Azure/azure-powershell/issues/8347.</span><span class="sxs-lookup"><span data-stu-id="1b379-1406">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="1b379-1407">Исправлен командлет Get-AzAutomationDscNode, возвращающий все узлы при использовании -Name.</span><span class="sxs-lookup"><span data-stu-id="1b379-1407">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="1b379-1408">Теперь он возвращает только соответствующий узел.</span><span class="sxs-lookup"><span data-stu-id="1b379-1408">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1b379-1409">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1b379-1409">Az.Compute</span></span>
* <span data-ttu-id="1b379-1410">Добавлены параметры ProtectFromScaleIn и ProtectFromScaleSetAction для командлета Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="1b379-1410">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="1b379-1411">Командлет New-AzVM с простым набором параметров теперь по умолчанию использует доступное расположение, если регион "восточная часть США" не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1b379-1411">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1b379-1412">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1b379-1412">Az.DataLakeStore</span></span>
* <span data-ttu-id="1b379-1413">Обновлен пакет SDK ADLS для использования httpclient. В инфраструктуру Azure интегрирована проверка плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="1b379-1413">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1b379-1414">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1b379-1414">Az.Monitor</span></span>
* <span data-ttu-id="1b379-1415">Исправлены неправильные имена параметров в справочных примерах.</span><span class="sxs-lookup"><span data-stu-id="1b379-1415">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1b379-1416">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1b379-1416">Az.Network</span></span>
* <span data-ttu-id="1b379-1417">Добавлен флаг DisableBgpRoutePropagation для выходных данных действующей таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="1b379-1417">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="1b379-1418">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="1b379-1418">Updated cmdlet:</span></span>
        - <span data-ttu-id="1b379-1419">Get-AzEffectiveRouteTable.</span><span class="sxs-lookup"><span data-stu-id="1b379-1419">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="1b379-1420">Исправлен двойной дефис в документации New-AzApplicationGatewayTrustedRootCertificate.</span><span class="sxs-lookup"><span data-stu-id="1b379-1420">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="1b379-1421">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1b379-1421">Az.Resources</span></span>
* <span data-ttu-id="1b379-1422">Добавлен новый командлет Get-AzureRmDenyAssignment для получения запрещающих назначений.</span><span class="sxs-lookup"><span data-stu-id="1b379-1422">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="1b379-1423">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1b379-1423">Az.Sql</span></span>
* <span data-ttu-id="1b379-1424">Командлеты Расширенной защиты от угроз переименованы на командлеты Расширенной защиты данных, и оценка уязвимости включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1b379-1424">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="1b379-1425">2.0.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="1b379-1425">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1b379-1426">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1b379-1426">Az.Accounts</span></span>
* <span data-ttu-id="1b379-1427">Обновлена библиотека аутентификации для устранения проблем с ADFS при использовании аутентификации на основе имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="1b379-1427">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="1b379-1428">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1b379-1428">Az.CognitiveServices</span></span>
* <span data-ttu-id="1b379-1429">Отображается только заявление об отказе Bing для служб Поиска Bing.</span><span class="sxs-lookup"><span data-stu-id="1b379-1429">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="1b379-1430">Исправлена проблема с созданием учетной записи.</span><span class="sxs-lookup"><span data-stu-id="1b379-1430">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1b379-1431">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1b379-1431">Az.Compute</span></span>
* <span data-ttu-id="1b379-1432">Функция группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="1b379-1432">Proximity placement group feature.</span></span>
    - <span data-ttu-id="1b379-1433">Добавлены следующие новые командлеты:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="1b379-1433">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="1b379-1434">Новый параметр ProximityPlacementGroupId будет добавлен в следующие командлеты:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="1b379-1434">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="1b379-1435">В командлет New-AzGalleryImageVersion добавлен параметр StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="1b379-1435">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="1b379-1436">TargetRegion в командлете New-AzGalleryImageVersion может содержать StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="1b379-1436">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="1b379-1437">Параметр-переключатель SkipShutdown добавлен в командлеты Stop-AzVM и Stop-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="1b379-1437">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="1b379-1438">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="1b379-1438">Breaking changes</span></span>
    - <span data-ttu-id="1b379-1439">Командлет SET-AzVMBootDiagnostics изменен на Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="1b379-1439">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="1b379-1440">Командлет Export-AzLogAnalyticThrottledRequests изменен на Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="1b379-1440">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="1b379-1441">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="1b379-1441">Az.DeploymentManager</span></span>
* <span data-ttu-id="1b379-1442">Первая общедоступная версия командлетов диспетчера развертывания Azure</span><span class="sxs-lookup"><span data-stu-id="1b379-1442">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="1b379-1443">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="1b379-1443">Az.Dns</span></span>
* <span data-ttu-id="1b379-1444">Автоматическое делегирование DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="1b379-1444">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="1b379-1445">Командлет для создания зоны DNS принимает имя родительской зоны в качестве дополнительного необязательного параметра.</span><span class="sxs-lookup"><span data-stu-id="1b379-1445">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="1b379-1446">Он добавляет записи NS в родительской зоне для созданной дочерней зоны.</span><span class="sxs-lookup"><span data-stu-id="1b379-1446">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="1b379-1447">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="1b379-1447">Az.FrontDoor</span></span>
* <span data-ttu-id="1b379-1448">Первая общедоступная версия командлетов Azure FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="1b379-1448">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="1b379-1449">Переименованы командлеты WAF для включения Waf.</span><span class="sxs-lookup"><span data-stu-id="1b379-1449">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="1b379-1450">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1b379-1450">Az.HDInsight</span></span>
* <span data-ttu-id="1b379-1451">Удалены два командлета:</span><span class="sxs-lookup"><span data-stu-id="1b379-1451">Removed two cmdlets:</span></span>
    - <span data-ttu-id="1b379-1452">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="1b379-1452">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="1b379-1453">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="1b379-1453">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="1b379-1454">Добавлен новый командлет Set-AzHDInsightGatewayCredential для замены Grant-AzHDInsightHttpServicesAccess.</span><span class="sxs-lookup"><span data-stu-id="1b379-1454">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="1b379-1455">Обновлен командлет Get-AzHDInsightJobOutput для различения ролей читателя и оператора HDInsight:</span><span class="sxs-lookup"><span data-stu-id="1b379-1455">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="1b379-1456">Пользователям с ролью читателя не нужно указывать параметр DefaultStorageAccountKey явным образом, иначе возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="1b379-1456">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="1b379-1457">На пользователей с ролью оператора HDInsight это не повлияет.</span><span class="sxs-lookup"><span data-stu-id="1b379-1457">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1b379-1458">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1b379-1458">Az.Monitor</span></span>
* <span data-ttu-id="1b379-1459">Новые командлеты для API SQR (запланированное правило запросов)</span><span class="sxs-lookup"><span data-stu-id="1b379-1459">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="1b379-1460">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="1b379-1460">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="1b379-1461">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="1b379-1461">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="1b379-1462">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="1b379-1462">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="1b379-1463">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="1b379-1463">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="1b379-1464">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="1b379-1464">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="1b379-1465">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="1b379-1465">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="1b379-1466">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="1b379-1466">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="1b379-1467">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="1b379-1467">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="1b379-1468">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="1b379-1468">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="1b379-1469">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="1b379-1469">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="1b379-1470">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="1b379-1470">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="1b379-1471">См. подробнее об [API SQR](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules).</span><span class="sxs-lookup"><span data-stu-id="1b379-1471">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="1b379-1472">Обновлен файл Az.Monitor.md для включения командлетов для правила генерации оповещений на основе метрик GenV2(не классическая версия).</span><span class="sxs-lookup"><span data-stu-id="1b379-1472">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1b379-1473">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1b379-1473">Az.Network</span></span>
* <span data-ttu-id="1b379-1474">Добавлена поддержка для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="1b379-1474">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="1b379-1475">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="1b379-1475">New cmdlets</span></span>
        - <span data-ttu-id="1b379-1476">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="1b379-1476">New-AzNatGateway</span></span>
        - <span data-ttu-id="1b379-1477">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="1b379-1477">Get-AzNatGateway</span></span>
        - <span data-ttu-id="1b379-1478">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="1b379-1478">Set-AzNatGateway</span></span>
        - <span data-ttu-id="1b379-1479">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="1b379-1479">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="1b379-1480">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="1b379-1480">Updated cmdlets</span></span>
        - <span data-ttu-id="1b379-1481">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="1b379-1481">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="1b379-1482">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="1b379-1482">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="1b379-1483">Обновлены следующие команды для функции: Настройка и удаление пользовательских маршрутов через шлюз в Бруклине.</span><span class="sxs-lookup"><span data-stu-id="1b379-1483">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="1b379-1484">Обновлен командлет New-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="1b379-1484">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="1b379-1485">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="1b379-1485">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="1b379-1486">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="1b379-1486">Az.PolicyInsights</span></span>
* <span data-ttu-id="1b379-1487">Добавлена поддержка сведений об оценке политики запросов.</span><span class="sxs-lookup"><span data-stu-id="1b379-1487">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="1b379-1488">Добавлен параметр -Expand в командлет Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="1b379-1488">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="1b379-1489">Добавлена поддержка -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="1b379-1489">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1b379-1490">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1b379-1490">Az.RecoveryServices</span></span>
* <span data-ttu-id="1b379-1491">Добавлена поддержка перекрестной подписки на Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="1b379-1491">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="1b379-1492">Добавлена возможность отмечать предстоящие критически важные изменения для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="1b379-1492">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="1b379-1493">Исправлены план восстановления и план действий для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="1b379-1493">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="1b379-1494">Исправлено сетевое сопоставление обновления Azure Site Recovery (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="1b379-1494">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="1b379-1495">Исправлено направление защиты обновления Azure Site Recovery для управляемых дисков (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="1b379-1495">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="1b379-1496">Добавлены другие незначительные исправления.</span><span class="sxs-lookup"><span data-stu-id="1b379-1496">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="1b379-1497">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="1b379-1497">Az.Relay</span></span>
* <span data-ttu-id="1b379-1498">Исправлены опечатки в сообщениях для клиентов.</span><span class="sxs-lookup"><span data-stu-id="1b379-1498">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="1b379-1499">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1b379-1499">Az.ServiceBus</span></span>
* <span data-ttu-id="1b379-1500">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="1b379-1500">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1b379-1501">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1b379-1501">Az.Storage</span></span>
* <span data-ttu-id="1b379-1502">Выполнено обновление клиентской библиотеки хранилища до версии 10.0.1 (пространство имен всех объектов из этого пакета SDK изменено с Microsoft.WindowsAzure.Storage. *на Microsoft.Azure.Storage*).</span><span class="sxs-lookup"><span data-stu-id="1b379-1502">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="1b379-1503">Выполнено обновление до Microsoft.Azure.Management.Storage версии 11.0.0 для включения поддержки нового API версии 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="1b379-1503">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="1b379-1504">Значение свойства Kind по умолчанию в учетной записи хранения изменено со Storage на StorageV2.</span><span class="sxs-lookup"><span data-stu-id="1b379-1504">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="1b379-1505">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1b379-1505">New-AzStorageAccount</span></span>
* <span data-ttu-id="1b379-1506">Изменено значение Sku.Name в выходных данных командлета учетной записи хранения в соответствии со значением Sku.Name во входных данных путем добавления _ (например, StandardLRS изменено на Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="1b379-1506">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="1b379-1507">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1b379-1507">New-AzStorageAccount</span></span>
    - <span data-ttu-id="1b379-1508">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1b379-1508">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="1b379-1509">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1b379-1509">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1b379-1510">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1b379-1510">Az.Websites</span></span>
* <span data-ttu-id="1b379-1511">Свойство Kind теперь будет задаваться объектам PSSite, возвращаемым командлетом Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="1b379-1511">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="1b379-1512">Get-AzWebApp\*Metrics и Get-AzAppServicePlanMetrics считаются нерекомендуемыми.</span><span class="sxs-lookup"><span data-stu-id="1b379-1512">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="1b379-1513">1.8.0 — апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="1b379-1513">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="1b379-1514">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="1b379-1514">Highlights since the last major release</span></span>
* <span data-ttu-id="1b379-1515">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="1b379-1515">General availability of `Az` module</span></span>
* <span data-ttu-id="1b379-1516">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="1b379-1516">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="1b379-1517">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="1b379-1517">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="1b379-1518">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="1b379-1518">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="1b379-1519">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="1b379-1519">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="1b379-1520">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="1b379-1520">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="1b379-1521">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="1b379-1521">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="1b379-1522">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1b379-1522">Az.Accounts</span></span>
* <span data-ttu-id="1b379-1523">Обновлен командлет Uninstall-AzureRm для правильного удаления модулей в Mac.</span><span class="sxs-lookup"><span data-stu-id="1b379-1523">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="1b379-1524">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="1b379-1524">Az.Batch</span></span>
* <span data-ttu-id="1b379-1525">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="1b379-1525">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="1b379-1526">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="1b379-1526">Az.Cdn</span></span>
* <span data-ttu-id="1b379-1527">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="1b379-1527">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="1b379-1528">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1b379-1528">Az.CognitiveServices</span></span>
* <span data-ttu-id="1b379-1529">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="1b379-1529">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1b379-1530">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1b379-1530">Az.Compute</span></span>
* <span data-ttu-id="1b379-1531">Устранена проблема с установкой AEM, если в идентификаторах ресурсов дисков группа ресурсов указана в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="1b379-1531">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="1b379-1532">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="1b379-1532">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="1b379-1533">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="1b379-1533">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1b379-1534">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1b379-1534">Az.DataFactory</span></span>
* <span data-ttu-id="1b379-1535">Добавлены свойства SsisProperties, если NodeCount не имеет значения NULL для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="1b379-1535">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1b379-1536">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1b379-1536">Az.DataLakeStore</span></span>
* <span data-ttu-id="1b379-1537">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="1b379-1537">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="1b379-1538">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="1b379-1538">Az.EventGrid</span></span>
* <span data-ttu-id="1b379-1539">Обновлен текст справки для конечной точки, указывающий, что необходимо создать ресурсы, прежде чем использовать командлеты для создания или обновления подписки на события.</span><span class="sxs-lookup"><span data-stu-id="1b379-1539">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="1b379-1540">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="1b379-1540">Az.EventHub</span></span>
* <span data-ttu-id="1b379-1541">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="1b379-1541">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="1b379-1542">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1b379-1542">Az.HDInsight</span></span>
* <span data-ttu-id="1b379-1543">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="1b379-1543">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1b379-1544">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1b379-1544">Az.IotHub</span></span>
* <span data-ttu-id="1b379-1545">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="1b379-1545">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1b379-1546">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1b379-1546">Az.KeyVault</span></span>
* <span data-ttu-id="1b379-1547">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="1b379-1547">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="1b379-1548">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="1b379-1548">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="1b379-1549">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="1b379-1549">Az.MachineLearning</span></span>
* <span data-ttu-id="1b379-1550">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="1b379-1550">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="1b379-1551">Az.Media</span><span class="sxs-lookup"><span data-stu-id="1b379-1551">Az.Media</span></span>
* <span data-ttu-id="1b379-1552">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="1b379-1552">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1b379-1553">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1b379-1553">Az.Monitor</span></span>
  * <span data-ttu-id="1b379-1554">Добавлены новые командлеты для правила генерации оповещений на основе метрик GenV2 (не классических).</span><span class="sxs-lookup"><span data-stu-id="1b379-1554">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="1b379-1555">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="1b379-1555">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="1b379-1556">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="1b379-1556">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="1b379-1557">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="1b379-1557">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="1b379-1558">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="1b379-1558">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="1b379-1559">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="1b379-1559">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="1b379-1560">Обновлен пакет SDK Monitor до предварительной версии 0.22.0.</span><span class="sxs-lookup"><span data-stu-id="1b379-1560">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1b379-1561">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1b379-1561">Az.Network</span></span>
* <span data-ttu-id="1b379-1562">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="1b379-1562">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="1b379-1563">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="1b379-1563">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="1b379-1564">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="1b379-1564">Az.NotificationHubs</span></span>
* <span data-ttu-id="1b379-1565">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="1b379-1565">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="1b379-1566">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1b379-1566">Az.OperationalInsights</span></span>
* <span data-ttu-id="1b379-1567">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="1b379-1567">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="1b379-1568">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="1b379-1568">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="1b379-1569">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="1b379-1569">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1b379-1570">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1b379-1570">Az.RecoveryServices</span></span>
* <span data-ttu-id="1b379-1571">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="1b379-1571">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="1b379-1572">Обновлен табличный формат для SQL на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="1b379-1572">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="1b379-1573">Добавлен альтернативный метод для получения расположения в Общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="1b379-1573">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="1b379-1574">Обновлено значение ScheduleRunDays в объекте SchedulePolicy в соответствии с часовым поясом.</span><span class="sxs-lookup"><span data-stu-id="1b379-1574">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="1b379-1575">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="1b379-1575">Az.RedisCache</span></span>
* <span data-ttu-id="1b379-1576">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="1b379-1576">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1b379-1577">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1b379-1577">Az.Resources</span></span>
* <span data-ttu-id="1b379-1578">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="1b379-1578">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="1b379-1579">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1b379-1579">Az.Sql</span></span>
* <span data-ttu-id="1b379-1580">Заменена зависимость от пакета SDK монитора на обычный код.</span><span class="sxs-lookup"><span data-stu-id="1b379-1580">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="1b379-1581">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="1b379-1581">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="1b379-1582">Улучшен процесс классификации нескольких столбцов.</span><span class="sxs-lookup"><span data-stu-id="1b379-1582">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="1b379-1583">Добавлены свойства SKU (имя, семейство, производительность SKU) в отклике Get-AzSqlServerServiceObjective, а также по умолчанию задан табличный формат.</span><span class="sxs-lookup"><span data-stu-id="1b379-1583">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="1b379-1584">C помощью Get-AzSqlServerServiceObjective теперь можно получать список доступных целевых служб по расположению без необходимости заранее размещать сервер в регионе.</span><span class="sxs-lookup"><span data-stu-id="1b379-1584">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="1b379-1585">Поддерживается параметр часового пояса при создании Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="1b379-1585">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="1b379-1586">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="1b379-1586">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1b379-1587">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1b379-1587">Az.Websites</span></span>
* <span data-ttu-id="1b379-1588">Исправлены командлеты Set-AzWebApp и Set-AzWebAppSlot, которые теперь не удаляют теги при выполнении.</span><span class="sxs-lookup"><span data-stu-id="1b379-1588">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="1b379-1589">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="1b379-1589">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="1b379-1590">Обновлен пакет SDK веб-узлов.</span><span class="sxs-lookup"><span data-stu-id="1b379-1590">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="1b379-1591">Удалено свойство AdminSiteName из PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="1b379-1591">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="1b379-1592">1.7.0 —апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="1b379-1592">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="1b379-1593">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="1b379-1593">Highlights since the last major release</span></span>
* <span data-ttu-id="1b379-1594">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="1b379-1594">General availability of `Az` module</span></span>
* <span data-ttu-id="1b379-1595">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="1b379-1595">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="1b379-1596">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="1b379-1596">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="1b379-1597">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="1b379-1597">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="1b379-1598">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="1b379-1598">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="1b379-1599">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="1b379-1599">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="1b379-1600">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="1b379-1600">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="1b379-1601">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1b379-1601">Az.Accounts</span></span>
* <span data-ttu-id="1b379-1602">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметр AzureAnalysisServicesEndpointResourceId.</span><span class="sxs-lookup"><span data-stu-id="1b379-1602">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="1b379-1603">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1b379-1603">Az.AnalysisServices</span></span>
* <span data-ttu-id="1b379-1604">Использование ServiceClient в командлетах плоскости данных и удаление исходной логики проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="1b379-1604">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="1b379-1605">Add-AzureASAccount используется как оболочка для Connect-AzAccount во избежание критических изменений.</span><span class="sxs-lookup"><span data-stu-id="1b379-1605">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1b379-1606">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1b379-1606">Az.Automation</span></span>
* <span data-ttu-id="1b379-1607">Исправлена ошибка командлета New-AzAutomationSoftwareUpdateConfiguration, связанная с включением.</span><span class="sxs-lookup"><span data-stu-id="1b379-1607">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="1b379-1608">Теперь параметры IncludedKbNumber и IncludedPackageNameMask должны работать нормально.</span><span class="sxs-lookup"><span data-stu-id="1b379-1608">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="1b379-1609">Исправлена ошибка динамической группы управления обновлениями службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="1b379-1609">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1b379-1610">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1b379-1610">Az.Compute</span></span>
* <span data-ttu-id="1b379-1611">В командлеты New-AzDiskConfig и New-AzSnapshotConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="1b379-1611">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="1b379-1612">Теперь можно создавать виртуальные машину на основе образов из коллекции от других клиентов.</span><span class="sxs-lookup"><span data-stu-id="1b379-1612">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="1b379-1613">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="1b379-1613">Az.ContainerInstance</span></span>
* <span data-ttu-id="1b379-1614">Исправлена проблема в параметре -Command командлета New-AzContainerGroup, из-за которой в конце добавлялся пустой аргумент.</span><span class="sxs-lookup"><span data-stu-id="1b379-1614">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1b379-1615">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1b379-1615">Az.DataFactory</span></span>
* <span data-ttu-id="1b379-1616">Пакет SDK для ADF .NET обновлен до версии 3.0.2.</span><span class="sxs-lookup"><span data-stu-id="1b379-1616">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="1b379-1617">Командлет Set-AzDataFactoryV2 обновлен с помощью дополнительных параметров для настроек, связанных с RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1b379-1617">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1b379-1618">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1b379-1618">Az.Resources</span></span>
* <span data-ttu-id="1b379-1619">Улучшена обработка поставщиков Get-AzResource при предоставлении параметров -ResourceId или -ResourceGroupName, -Name и -ResourceType.</span><span class="sxs-lookup"><span data-stu-id="1b379-1619">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="1b379-1620">Улучшена обработка ошибок в командлетах Test-AzDeployment и Test-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="1b379-1620">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="1b379-1621">Теперь ошибки, возникающие за пределами проверки развертывания, обрабатываются и включаются в выходные данные команды.</span><span class="sxs-lookup"><span data-stu-id="1b379-1621">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="1b379-1622">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="1b379-1622">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="1b379-1623">Добавлен параметр-переключатель -IgnoreDynamicParameters, с помощью которого можно настроить командлеты развертывания так, чтобы они пропускали запросы в сценариях скриптов и заданий.</span><span class="sxs-lookup"><span data-stu-id="1b379-1623">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="1b379-1624">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="1b379-1624">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="1b379-1625">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1b379-1625">Az.Sql</span></span>
* <span data-ttu-id="1b379-1626">Поддержка классификации данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="1b379-1626">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1b379-1627">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1b379-1627">Az.Storage</span></span>
* <span data-ttu-id="1b379-1628">Подробные сообщения об ошибке передаются при создании контекста хранилища с помощью параметра -UseConnectedAccount, но без входа в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="1b379-1628">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="1b379-1629">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="1b379-1629">New-AzStorageContext</span></span>
* <span data-ttu-id="1b379-1630">Поддержка свойств службы управления BLOB-объектов в указанной учетной записи хранения с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="1b379-1630">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="1b379-1631">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="1b379-1631">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="1b379-1632">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="1b379-1632">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="1b379-1633">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="1b379-1633">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="1b379-1634">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="1b379-1634">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="1b379-1635">Поддержка параметра -AsJob в командлетах для отправки и скачивания больших двоичных объектов и файлов.</span><span class="sxs-lookup"><span data-stu-id="1b379-1635">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="1b379-1636">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="1b379-1636">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="1b379-1637">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="1b379-1637">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="1b379-1638">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="1b379-1638">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="1b379-1639">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="1b379-1639">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="1b379-1640">1.6.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="1b379-1640">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="1b379-1641">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="1b379-1641">Highlights since the last major release</span></span>
* <span data-ttu-id="1b379-1642">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="1b379-1642">General availability of `Az` module</span></span>
* <span data-ttu-id="1b379-1643">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="1b379-1643">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="1b379-1644">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="1b379-1644">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="1b379-1645">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="1b379-1645">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="1b379-1646">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="1b379-1646">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="1b379-1647">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="1b379-1647">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="1b379-1648">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="1b379-1648">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1b379-1649">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1b379-1649">Az.Automation</span></span>
* <span data-ttu-id="1b379-1650">В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:</span><span class="sxs-lookup"><span data-stu-id="1b379-1650">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="1b379-1651">динамическое группирование;</span><span class="sxs-lookup"><span data-stu-id="1b379-1651">Dynamic grouping</span></span>
    * <span data-ttu-id="1b379-1652">скрипты предварительного или последующего выполнения;</span><span class="sxs-lookup"><span data-stu-id="1b379-1652">Pre-Post script</span></span>
    * <span data-ttu-id="1b379-1653">параметр перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="1b379-1653">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1b379-1654">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1b379-1654">Az.Compute</span></span>
* <span data-ttu-id="1b379-1655">Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.</span><span class="sxs-lookup"><span data-stu-id="1b379-1655">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="1b379-1656">Обновление клиентской библиотеки вычислений до версии 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="1b379-1656">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1b379-1657">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1b379-1657">Az.KeyVault</span></span>
* <span data-ttu-id="1b379-1658">Добавлена поддержка подстановочных знаков в командлетах KeyVault.</span><span class="sxs-lookup"><span data-stu-id="1b379-1658">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1b379-1659">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1b379-1659">Az.Network</span></span>
* <span data-ttu-id="1b379-1660">Добавлена поддержка анализа угроз для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="1b379-1660">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="1b379-1661">Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="1b379-1661">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1b379-1662">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1b379-1662">Az.RecoveryServices</span></span>
* <span data-ttu-id="1b379-1663">В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.</span><span class="sxs-lookup"><span data-stu-id="1b379-1663">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="1b379-1664">Добавлена поддержка канала для отмены регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="1b379-1664">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="1b379-1665">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1b379-1665">Az.Resources</span></span>
* <span data-ttu-id="1b379-1666">Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1b379-1666">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="1b379-1667">Обновлены учетные данные, используемые при общих вызовах к ARM.</span><span class="sxs-lookup"><span data-stu-id="1b379-1667">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="1b379-1668">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1b379-1668">Az.Sql</span></span>
* <span data-ttu-id="1b379-1669">Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="1b379-1669">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1b379-1670">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1b379-1670">Az.Storage</span></span>
* <span data-ttu-id="1b379-1671">Поддержка получения, настройки и удаления политики управления в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="1b379-1671">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="1b379-1672">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="1b379-1672">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="1b379-1673">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="1b379-1673">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="1b379-1674">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="1b379-1674">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="1b379-1675">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="1b379-1675">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="1b379-1676">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="1b379-1676">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="1b379-1677">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="1b379-1677">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1b379-1678">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1b379-1678">Az.Websites</span></span>
* <span data-ttu-id="1b379-1679">Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="1b379-1679">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="1b379-1680">1.5.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="1b379-1680">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1b379-1681">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1b379-1681">Az.Accounts</span></span>
* <span data-ttu-id="1b379-1682">Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.</span><span class="sxs-lookup"><span data-stu-id="1b379-1682">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="1b379-1683">Обновлены примеры для Connect AzAccount.</span><span class="sxs-lookup"><span data-stu-id="1b379-1683">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1b379-1684">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1b379-1684">Az.Automation</span></span>
* <span data-ttu-id="1b379-1685">Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="1b379-1685">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="1b379-1686">Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов.</span><span class="sxs-lookup"><span data-stu-id="1b379-1686">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="1b379-1687">Теперь он возвращает все узлы.</span><span class="sxs-lookup"><span data-stu-id="1b379-1687">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="1b379-1688">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="1b379-1688">Az.Cdn</span></span>
* <span data-ttu-id="1b379-1689">Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.</span><span class="sxs-lookup"><span data-stu-id="1b379-1689">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1b379-1690">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1b379-1690">Az.Compute</span></span>
* <span data-ttu-id="1b379-1691">Добавлена поддержка подстановочных знаков в командлетах Get.</span><span class="sxs-lookup"><span data-stu-id="1b379-1691">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1b379-1692">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1b379-1692">Az.DataFactory</span></span>
* <span data-ttu-id="1b379-1693">Обновлен пакет SDK для ADF .NET до версии 3.0.1.</span><span class="sxs-lookup"><span data-stu-id="1b379-1693">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="1b379-1694">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="1b379-1694">Az.LogicApp</span></span>
* <span data-ttu-id="1b379-1695">Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.</span><span class="sxs-lookup"><span data-stu-id="1b379-1695">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1b379-1696">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1b379-1696">Az.Network</span></span>
* <span data-ttu-id="1b379-1697">Добавлена поддержка подстановочных знаков в командлетах Network.</span><span class="sxs-lookup"><span data-stu-id="1b379-1697">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1b379-1698">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1b379-1698">Az.RecoveryServices</span></span>
* <span data-ttu-id="1b379-1699">Добавлена поддержка SQL Server на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="1b379-1699">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="1b379-1700">Обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="1b379-1700">SDK Update</span></span>
* <span data-ttu-id="1b379-1701">Удалена проверка VMappContainer в Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="1b379-1701">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="1b379-1702">Добавлены параметры Name и ServerName для Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="1b379-1702">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="1b379-1703">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1b379-1703">Az.Resources</span></span>
* <span data-ttu-id="1b379-1704">Добавлен параметр `-TemplateObject` в командлеты для развертывания.</span><span class="sxs-lookup"><span data-stu-id="1b379-1704">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="1b379-1705">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.</span><span class="sxs-lookup"><span data-stu-id="1b379-1705">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="1b379-1706">Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="1b379-1706">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="1b379-1707">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.</span><span class="sxs-lookup"><span data-stu-id="1b379-1707">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="1b379-1708">Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="1b379-1708">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="1b379-1709">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.</span><span class="sxs-lookup"><span data-stu-id="1b379-1709">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="1b379-1710">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1b379-1710">Az.Sql</span></span>
* <span data-ttu-id="1b379-1711">Обновление AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="1b379-1711">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="1b379-1712">Исправлено поведение для пограничного случая при создании параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="1b379-1712">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1b379-1713">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1b379-1713">Az.Storage</span></span>
* <span data-ttu-id="1b379-1714">Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="1b379-1714">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="1b379-1715">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="1b379-1715">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="1b379-1716">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1b379-1716">Az.AnalysisServices</span></span>
* <span data-ttu-id="1b379-1717">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="1b379-1717">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1b379-1718">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1b379-1718">Az.Automation</span></span>
* <span data-ttu-id="1b379-1719">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1b379-1719">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="1b379-1720">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1b379-1720">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="1b379-1721">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1b379-1721">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="1b379-1722">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1b379-1722">Az.CognitiveServices</span></span>
* <span data-ttu-id="1b379-1723">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="1b379-1723">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1b379-1724">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1b379-1724">Az.Compute</span></span>
* <span data-ttu-id="1b379-1725">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="1b379-1725">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="1b379-1726">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="1b379-1726">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="1b379-1727">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="1b379-1727">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="1b379-1728">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="1b379-1728">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1b379-1729">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1b379-1729">Az.DataLakeStore</span></span>
* <span data-ttu-id="1b379-1730">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="1b379-1730">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="1b379-1731">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="1b379-1731">Az.EventHub</span></span>
* <span data-ttu-id="1b379-1732">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="1b379-1732">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1b379-1733">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1b379-1733">Az.KeyVault</span></span>
* <span data-ttu-id="1b379-1734">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="1b379-1734">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="1b379-1735">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="1b379-1735">Az.LogicApp</span></span>
* <span data-ttu-id="1b379-1736">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="1b379-1736">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="1b379-1737">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="1b379-1737">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="1b379-1738">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="1b379-1738">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="1b379-1739">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="1b379-1739">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="1b379-1740">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="1b379-1740">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="1b379-1741">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="1b379-1741">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="1b379-1742">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="1b379-1742">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="1b379-1743">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="1b379-1743">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="1b379-1744">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="1b379-1744">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="1b379-1745">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="1b379-1745">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="1b379-1746">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="1b379-1746">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="1b379-1747">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1b379-1747">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="1b379-1748">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="1b379-1748">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1b379-1749">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1b379-1749">Az.Monitor</span></span>
* <span data-ttu-id="1b379-1750">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="1b379-1750">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1b379-1751">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1b379-1751">Az.Network</span></span>
* <span data-ttu-id="1b379-1752">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="1b379-1752">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="1b379-1753">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1b379-1753">Az.OperationalInsights</span></span>
* <span data-ttu-id="1b379-1754">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="1b379-1754">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="1b379-1755">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="1b379-1755">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="1b379-1756">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="1b379-1756">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1b379-1757">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1b379-1757">Az.Resources</span></span>
* <span data-ttu-id="1b379-1758">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="1b379-1758">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="1b379-1759">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="1b379-1759">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="1b379-1760">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="1b379-1760">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="1b379-1761">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="1b379-1761">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="1b379-1762">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1b379-1762">Az.Sql</span></span>
* <span data-ttu-id="1b379-1763">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="1b379-1763">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="1b379-1764">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="1b379-1764">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1b379-1765">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1b379-1765">Az.Websites</span></span>
* <span data-ttu-id="1b379-1766">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="1b379-1766">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="1b379-1767">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="1b379-1767">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1b379-1768">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1b379-1768">Az.Accounts</span></span>
* <span data-ttu-id="1b379-1769">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="1b379-1769">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="1b379-1770">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1b379-1770">Az.AnalysisServices</span></span>
<span data-ttu-id="1b379-1771">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="1b379-1771">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1b379-1772">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1b379-1772">Az.Compute</span></span>
* <span data-ttu-id="1b379-1773">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="1b379-1773">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="1b379-1774">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="1b379-1774">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="1b379-1775">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="1b379-1775">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1b379-1776">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1b379-1776">Az.RecoveryServices</span></span>
<span data-ttu-id="1b379-1777">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="1b379-1777">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1b379-1778">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1b379-1778">Az.Resources</span></span>
* <span data-ttu-id="1b379-1779">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1b379-1779">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="1b379-1780">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="1b379-1780">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="1b379-1781">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="1b379-1781">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="1b379-1782">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="1b379-1782">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="1b379-1783">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1b379-1783">Az.Sql</span></span>
* <span data-ttu-id="1b379-1784">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="1b379-1784">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="1b379-1785">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="1b379-1785">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="1b379-1786">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="1b379-1786">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="1b379-1787">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="1b379-1787">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1b379-1788">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1b379-1788">Az.Accounts</span></span>
* <span data-ttu-id="1b379-1789">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="1b379-1789">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="1b379-1790">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1b379-1790">Az.AnalysisServices</span></span>
* <span data-ttu-id="1b379-1791">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="1b379-1791">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1b379-1792">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1b379-1792">Az.RecoveryServices</span></span>
* <span data-ttu-id="1b379-1793">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="1b379-1793">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="1b379-1794">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="1b379-1794">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1b379-1795">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1b379-1795">Az.Accounts</span></span>
* <span data-ttu-id="1b379-1796">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="1b379-1796">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="1b379-1797">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="1b379-1797">Update incorrect online help URLs</span></span>
* <span data-ttu-id="1b379-1798">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="1b379-1798">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="1b379-1799">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="1b379-1799">Az.Aks</span></span>
* <span data-ttu-id="1b379-1800">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="1b379-1800">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1b379-1801">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1b379-1801">Az.Automation</span></span>
* <span data-ttu-id="1b379-1802">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="1b379-1802">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="1b379-1803">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="1b379-1803">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="1b379-1804">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="1b379-1804">Az.Cdn</span></span>
* <span data-ttu-id="1b379-1805">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="1b379-1805">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1b379-1806">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1b379-1806">Az.Compute</span></span>
* <span data-ttu-id="1b379-1807">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="1b379-1807">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="1b379-1808">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="1b379-1808">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="1b379-1809">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="1b379-1809">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="1b379-1810">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1b379-1810">Az.ContainerRegistry</span></span>
* <span data-ttu-id="1b379-1811">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="1b379-1811">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1b379-1812">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1b379-1812">Az.DataFactory</span></span>
* <span data-ttu-id="1b379-1813">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="1b379-1813">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1b379-1814">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1b379-1814">Az.DataLakeStore</span></span>
* <span data-ttu-id="1b379-1815">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="1b379-1815">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="1b379-1816">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="1b379-1816">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="1b379-1817">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="1b379-1817">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1b379-1818">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1b379-1818">Az.IotHub</span></span>
* <span data-ttu-id="1b379-1819">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="1b379-1819">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1b379-1820">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1b379-1820">Az.KeyVault</span></span>
* <span data-ttu-id="1b379-1821">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="1b379-1821">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1b379-1822">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1b379-1822">Az.Network</span></span>
* <span data-ttu-id="1b379-1823">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="1b379-1823">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="1b379-1824">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1b379-1824">Az.Resources</span></span>
* <span data-ttu-id="1b379-1825">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="1b379-1825">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="1b379-1826">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1b379-1826">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="1b379-1827">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="1b379-1827">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="1b379-1828">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="1b379-1828">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="1b379-1829">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="1b379-1829">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="1b379-1830">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="1b379-1830">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="1b379-1831">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="1b379-1831">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="1b379-1832">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1b379-1832">Az.ServiceFabric</span></span>
* <span data-ttu-id="1b379-1833">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="1b379-1833">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="1b379-1834">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="1b379-1834">Fix some error messages.</span></span>
* <span data-ttu-id="1b379-1835">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="1b379-1835">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="1b379-1836">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="1b379-1836">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="1b379-1837">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="1b379-1837">Az.SignalR</span></span>
* <span data-ttu-id="1b379-1838">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="1b379-1838">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="1b379-1839">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1b379-1839">Az.Sql</span></span>
* <span data-ttu-id="1b379-1840">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="1b379-1840">Update incorrect online help URLs</span></span>
* <span data-ttu-id="1b379-1841">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="1b379-1841">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="1b379-1842">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="1b379-1842">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="1b379-1843">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="1b379-1843">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1b379-1844">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1b379-1844">Az.Storage</span></span>
* <span data-ttu-id="1b379-1845">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="1b379-1845">Update incorrect online help URLs</span></span>
* <span data-ttu-id="1b379-1846">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="1b379-1846">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="1b379-1847">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="1b379-1847">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="1b379-1848">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="1b379-1848">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="1b379-1849">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="1b379-1849">Az.TrafficManager</span></span>
* <span data-ttu-id="1b379-1850">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="1b379-1850">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1b379-1851">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1b379-1851">Az.Websites</span></span>
* <span data-ttu-id="1b379-1852">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="1b379-1852">Update incorrect online help URLs</span></span>
* <span data-ttu-id="1b379-1853">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="1b379-1853">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="1b379-1854">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="1b379-1854">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="1b379-1855">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="1b379-1855">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1b379-1856">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1b379-1856">Az.Accounts</span></span>
* <span data-ttu-id="1b379-1857">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="1b379-1857">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1b379-1858">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1b379-1858">Az.Compute</span></span>
* <span data-ttu-id="1b379-1859">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="1b379-1859">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="1b379-1860">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="1b379-1860">Updated the description of ID in help files</span></span>
* <span data-ttu-id="1b379-1861">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="1b379-1861">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1b379-1862">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1b379-1862">Az.DataLakeStore</span></span>
* <span data-ttu-id="1b379-1863">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="1b379-1863">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="1b379-1864">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="1b379-1864">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="1b379-1865">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="1b379-1865">Az.EventGrid</span></span>
* <span data-ttu-id="1b379-1866">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="1b379-1866">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="1b379-1867">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="1b379-1867">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="1b379-1868">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="1b379-1868">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="1b379-1869">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="1b379-1869">Event Time-To-Live,</span></span>
        - <span data-ttu-id="1b379-1870">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="1b379-1870">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="1b379-1871">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="1b379-1871">Dead letter endpoint.</span></span>
    - <span data-ttu-id="1b379-1872">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="1b379-1872">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="1b379-1873">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="1b379-1873">Event Time-To-Live,</span></span>
        - <span data-ttu-id="1b379-1874">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="1b379-1874">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="1b379-1875">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="1b379-1875">Dead letter endpoint.</span></span>
* <span data-ttu-id="1b379-1876">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="1b379-1876">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="1b379-1877">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="1b379-1877">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1b379-1878">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1b379-1878">Az.IotHub</span></span>
* <span data-ttu-id="1b379-1879">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="1b379-1879">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="1b379-1880">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="1b379-1880">Az.LogicApp</span></span>
* <span data-ttu-id="1b379-1881">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="1b379-1881">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="1b379-1882">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1b379-1882">Az.Resources</span></span>
* <span data-ttu-id="1b379-1883">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="1b379-1883">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="1b379-1884">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="1b379-1884">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="1b379-1885">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="1b379-1885">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="1b379-1886">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="1b379-1886">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="1b379-1887">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="1b379-1887">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="1b379-1888">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="1b379-1888">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="1b379-1889">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="1b379-1889">Az.SignalR</span></span>
* <span data-ttu-id="1b379-1890">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="1b379-1890">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="1b379-1891">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1b379-1891">Az.Sql</span></span>
* <span data-ttu-id="1b379-1892">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="1b379-1892">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1b379-1893">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1b379-1893">Az.Storage</span></span>
* <span data-ttu-id="1b379-1894">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="1b379-1894">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="1b379-1895">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="1b379-1895">New-AzStorageContext</span></span>
* <span data-ttu-id="1b379-1896">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="1b379-1896">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="1b379-1897">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="1b379-1897">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1b379-1898">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1b379-1898">Az.Websites</span></span>
* <span data-ttu-id="1b379-1899">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="1b379-1899">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="1b379-1900">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="1b379-1900">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="1b379-1901">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="1b379-1901">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="1b379-1902">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="1b379-1902">General</span></span>

- <span data-ttu-id="1b379-1903">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="1b379-1903">General Availability of Az Module</span></span>
- <span data-ttu-id="1b379-1904">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="1b379-1904">Online help for each module</span></span>
- <span data-ttu-id="1b379-1905">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="1b379-1905">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="1b379-1906">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="1b379-1906">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="1b379-1907">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1b379-1907">Az.Accounts</span></span>
- <span data-ttu-id="1b379-1908">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="1b379-1908">Changed from Az.Profile</span></span>
- <span data-ttu-id="1b379-1909">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="1b379-1909">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="1b379-1910">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1b379-1910">Az.ApiManagement</span></span>
- <span data-ttu-id="1b379-1911">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="1b379-1911">Fixes for #7002</span></span>
- <span data-ttu-id="1b379-1912">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="1b379-1912">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="1b379-1913">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="1b379-1913">Az.Batch</span></span>
- <span data-ttu-id="1b379-1914">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="1b379-1914">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="1b379-1915">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="1b379-1915">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="1b379-1916">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="1b379-1916">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="1b379-1917">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="1b379-1917">Az.Billing</span></span>
- <span data-ttu-id="1b379-1918">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="1b379-1918">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="1b379-1919">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="1b379-1919">Az.CognitivServices</span></span>
- <span data-ttu-id="1b379-1920">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="1b379-1920">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="1b379-1921">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="1b379-1921">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="1b379-1922">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="1b379-1922">Az.ContainerInstance</span></span>
- <span data-ttu-id="1b379-1923">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="1b379-1923">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="1b379-1924">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="1b379-1924">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="1b379-1925">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="1b379-1925">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="1b379-1926">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1b379-1926">Az.DataLakeStore</span></span>
- <span data-ttu-id="1b379-1927">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="1b379-1927">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="1b379-1928">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1b379-1928">Az.Monitor</span></span>
- <span data-ttu-id="1b379-1929">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="1b379-1929">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="1b379-1930">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1b379-1930">Az.KeyVault</span></span>
- <span data-ttu-id="1b379-1931">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="1b379-1931">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="1b379-1932">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="1b379-1932">Az.MachineLearning</span></span>
- <span data-ttu-id="1b379-1933">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="1b379-1933">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="1b379-1934">Az.Media</span><span class="sxs-lookup"><span data-stu-id="1b379-1934">Az.Media</span></span>
- <span data-ttu-id="1b379-1935">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="1b379-1935">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="1b379-1936">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1b379-1936">Az.Network</span></span>
<span data-ttu-id="1b379-1937">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="1b379-1937">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="1b379-1938">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="1b379-1938">New cmdlets added:</span></span>
        - <span data-ttu-id="1b379-1939">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1b379-1939">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="1b379-1940">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1b379-1940">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="1b379-1941">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1b379-1941">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="1b379-1942">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1b379-1942">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="1b379-1943">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1b379-1943">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="1b379-1944">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="1b379-1944">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="1b379-1945">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="1b379-1945">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="1b379-1946">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b379-1946">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="1b379-1947">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1b379-1947">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="1b379-1948">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1b379-1948">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="1b379-1949">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="1b379-1949">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="1b379-1950">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="1b379-1950">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="1b379-1951">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1b379-1951">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="1b379-1952">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1b379-1952">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="1b379-1953">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="1b379-1953">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="1b379-1954">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1b379-1954">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="1b379-1955">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1b379-1955">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="1b379-1956">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1b379-1956">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="1b379-1957">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1b379-1957">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="1b379-1958">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="1b379-1958">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="1b379-1959">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="1b379-1959">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="1b379-1960">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1b379-1960">Az.OperationalInsights</span></span>
- <span data-ttu-id="1b379-1961">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="1b379-1961">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="1b379-1962">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="1b379-1962">Az.Profile</span></span>
- <span data-ttu-id="1b379-1963">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="1b379-1963">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="1b379-1964">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1b379-1964">Az.RecoveryServices</span></span>
- <span data-ttu-id="1b379-1965">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="1b379-1965">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="1b379-1966">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1b379-1966">Az.Resources</span></span>
- <span data-ttu-id="1b379-1967">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="1b379-1967">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="1b379-1968">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1b379-1968">Az.ServiceFabric</span></span>
- <span data-ttu-id="1b379-1969">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="1b379-1969">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="1b379-1970">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="1b379-1970">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="1b379-1971">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="1b379-1971">Az.SIgnalR</span></span>
- <span data-ttu-id="1b379-1972">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="1b379-1972">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="1b379-1973">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1b379-1973">Az.Sql</span></span>
- <span data-ttu-id="1b379-1974">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="1b379-1974">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="1b379-1975">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="1b379-1975">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="1b379-1976">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="1b379-1976">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="1b379-1977">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1b379-1977">Az.Storage</span></span>
- <span data-ttu-id="1b379-1978">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="1b379-1978">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="1b379-1979">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1b379-1979">Az.Websites</span></span>
- <span data-ttu-id="1b379-1980">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="1b379-1980">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="1b379-1981">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="1b379-1981">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="1b379-1982">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="1b379-1982">General</span></span>

* <span data-ttu-id="1b379-1983">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="1b379-1983">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="1b379-1984">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1b379-1984">Az.Compute</span></span>

* <span data-ttu-id="1b379-1985">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="1b379-1985">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="1b379-1986">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1b379-1986">Az.DataLakeStore</span></span>

* <span data-ttu-id="1b379-1987">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="1b379-1987">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="1b379-1988">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="1b379-1988">Az.FrontDoor</span></span>

* <span data-ttu-id="1b379-1989">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="1b379-1989">Fixed some broken links</span></span>
    - <span data-ttu-id="1b379-1990">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="1b379-1990">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="1b379-1991">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="1b379-1991">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="1b379-1992">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1b379-1992">Az.RecoveryServices</span></span>

* <span data-ttu-id="1b379-1993">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="1b379-1993">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="1b379-1994">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="1b379-1994">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="1b379-1995">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1b379-1995">Az.Resources</span></span>

* <span data-ttu-id="1b379-1996">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="1b379-1996">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="1b379-1997">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="1b379-1997">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="1b379-1998">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1b379-1998">Az.Sql</span></span>

* <span data-ttu-id="1b379-1999">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="1b379-1999">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="1b379-2000">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="1b379-2000">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="1b379-2001">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="1b379-2001">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="1b379-2002">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1b379-2002">Az.Storage</span></span>

* <span data-ttu-id="1b379-2003">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1b379-2003">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="1b379-2004">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="1b379-2004">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="1b379-2005">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="1b379-2005">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="1b379-2006">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="1b379-2006">Support Static Website configuration</span></span>
    - <span data-ttu-id="1b379-2007">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="1b379-2007">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="1b379-2008">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="1b379-2008">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="1b379-2009">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1b379-2009">Az.Websites</span></span>

* <span data-ttu-id="1b379-2010">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1b379-2010">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="1b379-2011">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="1b379-2011">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="1b379-2012">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="1b379-2012">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="1b379-2013">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="1b379-2013">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="1b379-2014">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1b379-2014">Az.ApiManagement</span></span>
* <span data-ttu-id="1b379-2015">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="1b379-2015">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="1b379-2016">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1b379-2016">Az.Automation</span></span>
* <span data-ttu-id="1b379-2017">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="1b379-2017">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="1b379-2018">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="1b379-2018">Added Update Management cmdlets</span></span>
* <span data-ttu-id="1b379-2019">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="1b379-2019">Added Source Control cmdlets</span></span>
* <span data-ttu-id="1b379-2020">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="1b379-2020">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="1b379-2021">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="1b379-2021">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="1b379-2022">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1b379-2022">Az.Compute</span></span>
* <span data-ttu-id="1b379-2023">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="1b379-2023">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="1b379-2024">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="1b379-2024">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="1b379-2025">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="1b379-2025">Az.ContainerInstance</span></span>
* <span data-ttu-id="1b379-2026">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="1b379-2026">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="1b379-2027">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="1b379-2027">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="1b379-2028">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="1b379-2028">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="1b379-2029">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1b379-2029">Az.Network</span></span>
* <span data-ttu-id="1b379-2030">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="1b379-2030">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="1b379-2031">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="1b379-2031">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="1b379-2032">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="1b379-2032">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="1b379-2033">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="1b379-2033">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="1b379-2034">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="1b379-2034">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="1b379-2035">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="1b379-2035">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="1b379-2036">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="1b379-2036">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="1b379-2037">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="1b379-2037">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="1b379-2038">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="1b379-2038">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="1b379-2039">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="1b379-2039">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="1b379-2040">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="1b379-2040">Az.Relay</span></span>
* <span data-ttu-id="1b379-2041">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="1b379-2041">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="1b379-2042">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1b379-2042">Az.Resources</span></span>
* <span data-ttu-id="1b379-2043">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="1b379-2043">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="1b379-2044">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="1b379-2044">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="1b379-2045">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="1b379-2045">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="1b379-2046">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1b379-2046">Az.ServiceFabric</span></span>
* <span data-ttu-id="1b379-2047">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="1b379-2047">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="1b379-2048">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1b379-2048">Az.Sql</span></span>
* <span data-ttu-id="1b379-2049">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="1b379-2049">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="1b379-2050">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="1b379-2050">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="1b379-2051">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="1b379-2051">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="1b379-2052">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="1b379-2052">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="1b379-2053">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="1b379-2053">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="1b379-2054">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="1b379-2054">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="1b379-2055">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="1b379-2055">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="1b379-2056">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="1b379-2056">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="1b379-2057">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="1b379-2057">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="1b379-2058">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="1b379-2058">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="1b379-2059">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="1b379-2059">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="1b379-2060">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="1b379-2060">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="1b379-2061">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="1b379-2061">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="1b379-2062">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="1b379-2062">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="1b379-2063">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="1b379-2063">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="1b379-2064">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="1b379-2064">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="1b379-2065">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="1b379-2065">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="1b379-2066">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="1b379-2066">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="1b379-2067">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="1b379-2067">General</span></span>
* <span data-ttu-id="1b379-2068">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="1b379-2068">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="1b379-2069">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="1b379-2069">Az.Profile</span></span>
* <span data-ttu-id="1b379-2070">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1b379-2070">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="1b379-2071">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="1b379-2071">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="1b379-2072">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="1b379-2072">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="1b379-2073">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="1b379-2073">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="1b379-2074">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="1b379-2074">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="1b379-2075">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="1b379-2075">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="1b379-2076">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="1b379-2076">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="1b379-2077">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1b379-2077">Az.CognitiveServices</span></span>
* <span data-ttu-id="1b379-2078">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="1b379-2078">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1b379-2079">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1b379-2079">Az.Compute</span></span>
* <span data-ttu-id="1b379-2080">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="1b379-2080">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="1b379-2081">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="1b379-2081">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="1b379-2082">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="1b379-2082">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1b379-2083">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1b379-2083">Az.DataLakeStore</span></span>
* <span data-ttu-id="1b379-2084">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="1b379-2084">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="1b379-2085">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="1b379-2085">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="1b379-2086">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="1b379-2086">Az.Insights</span></span>
* <span data-ttu-id="1b379-2087">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="1b379-2087">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="1b379-2088">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="1b379-2088">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="1b379-2089">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="1b379-2089">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="1b379-2090">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="1b379-2090">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1b379-2091">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1b379-2091">Az.Network</span></span>
* <span data-ttu-id="1b379-2092">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="1b379-2092">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="1b379-2093">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="1b379-2093">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="1b379-2094">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="1b379-2094">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="1b379-2095">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="1b379-2095">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="1b379-2096">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="1b379-2096">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="1b379-2097">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="1b379-2097">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="1b379-2098">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="1b379-2098">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="1b379-2099">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="1b379-2099">Az.PolicyInsights</span></span>
* <span data-ttu-id="1b379-2100">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="1b379-2100">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="1b379-2101">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1b379-2101">Az.Resources</span></span>
* <span data-ttu-id="1b379-2102">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="1b379-2102">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="1b379-2103">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="1b379-2103">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="1b379-2104">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1b379-2104">Az.ServiceBus</span></span>
* <span data-ttu-id="1b379-2105">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="1b379-2105">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="1b379-2106">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1b379-2106">Az.ServiceFabric</span></span>
* <span data-ttu-id="1b379-2107">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="1b379-2107">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="1b379-2108">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="1b379-2108">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="1b379-2109">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="1b379-2109">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="1b379-2110">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="1b379-2110">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="1b379-2111">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="1b379-2111">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="1b379-2112">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="1b379-2112">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="1b379-2113">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="1b379-2113">Az.Profile</span></span>
* <span data-ttu-id="1b379-2114">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="1b379-2114">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="1b379-2115">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1b379-2115">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1b379-2116">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1b379-2116">Az.Compute</span></span>
* <span data-ttu-id="1b379-2117">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="1b379-2117">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="1b379-2118">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="1b379-2118">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1b379-2119">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1b379-2119">Az.DataLakeStore</span></span>
* <span data-ttu-id="1b379-2120">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="1b379-2120">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="1b379-2121">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1b379-2121">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="1b379-2122">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1b379-2122">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="1b379-2123">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1b379-2123">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="1b379-2124">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1b379-2124">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1b379-2125">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1b379-2125">Az.Network</span></span>
* <span data-ttu-id="1b379-2126">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="1b379-2126">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="1b379-2127">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="1b379-2127">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1b379-2128">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1b379-2128">Az.Resources</span></span>
* <span data-ttu-id="1b379-2129">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="1b379-2129">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="1b379-2130">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="1b379-2130">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="1b379-2131">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="1b379-2131">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="1b379-2132">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="1b379-2132">Azure.Storage</span></span>
* <span data-ttu-id="1b379-2133">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="1b379-2133">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="1b379-2134">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="1b379-2134">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="1b379-2135">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="1b379-2135">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="1b379-2136">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="1b379-2136">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="1b379-2137">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="1b379-2137">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="1b379-2138">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1b379-2138">Az.CognitiveServices</span></span>
* <span data-ttu-id="1b379-2139">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="1b379-2139">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1b379-2140">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1b379-2140">Az.Compute</span></span>
* <span data-ttu-id="1b379-2141">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="1b379-2141">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="1b379-2142">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="1b379-2142">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="1b379-2143">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="1b379-2143">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="1b379-2144">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="1b379-2144">Az.DataFactoryV2</span></span>
* <span data-ttu-id="1b379-2145">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="1b379-2145">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1b379-2146">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1b379-2146">Az.Network</span></span>
* <span data-ttu-id="1b379-2147">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="1b379-2147">Added NetworkProfile functionality.</span></span> <span data-ttu-id="1b379-2148">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="1b379-2148">new cmdlets added</span></span>
    - <span data-ttu-id="1b379-2149">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1b379-2149">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="1b379-2150">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1b379-2150">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="1b379-2151">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1b379-2151">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="1b379-2152">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1b379-2152">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="1b379-2153">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="1b379-2153">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="1b379-2154">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="1b379-2154">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="1b379-2155">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="1b379-2155">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="1b379-2156">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="1b379-2156">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="1b379-2157">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="1b379-2157">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="1b379-2158">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="1b379-2158">Az.RedisCache</span></span>
* <span data-ttu-id="1b379-2159">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="1b379-2159">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="1b379-2160">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="1b379-2160">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="1b379-2161">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1b379-2161">Az.Resources</span></span>
* <span data-ttu-id="1b379-2162">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1b379-2162">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="1b379-2163">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="1b379-2163">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="1b379-2164">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1b379-2164">Az.Sql</span></span>
* <span data-ttu-id="1b379-2165">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="1b379-2165">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1b379-2166">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1b379-2166">Az.Websites</span></span>
* <span data-ttu-id="1b379-2167">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="1b379-2167">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="1b379-2168">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="1b379-2168">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="1b379-2169">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="1b379-2169">0.2.0 - September 2018</span></span>
 <span data-ttu-id="1b379-2170">Начальный выпуск</span><span class="sxs-lookup"><span data-stu-id="1b379-2170">Initial Release</span></span>
