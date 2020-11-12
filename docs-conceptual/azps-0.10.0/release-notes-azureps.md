---
title: Заметки о выпуске Azure PowerShell
description: Узнайте обо всех последних обновлениях модулей Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 2e824dbbf593e0da9a2a8735aaa094b1944e306c
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2020
ms.locfileid: "93408876"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="0a3b9-103">Заметки о выпуске Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="0a3b9-103">Azure PowerShell release notes</span></span>
## <a name="0100-preview---april-2020"></a><span data-ttu-id="0a3b9-104">0.10.0-preview — апрель 2020 г.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-104">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="0a3b9-105">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="0a3b9-105">General</span></span>
* <span data-ttu-id="0a3b9-106">Модуль Az стали доступными в предварительной версии в Azure Stack Hub.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-106">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="0a3b9-107">Это обеспечивает кросс-платформенную совместимость с Linux и macOs.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-107">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="0a3b9-108">Azure Stack Hub теперь поддерживает PowerShell Core с модулями Az (см. [дополнительные сведения](https://aka.ms/az4AzureStack))</span><span class="sxs-lookup"><span data-stu-id="0a3b9-108">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="0a3b9-109">Модули Az поддерживают профиль 2019-03-01-hybrid:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-109">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="0a3b9-110">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="0a3b9-110">Az.Billing</span></span>
  - <span data-ttu-id="0a3b9-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a3b9-111">Az.Compute</span></span>
  - <span data-ttu-id="0a3b9-112">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="0a3b9-112">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="0a3b9-113">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0a3b9-113">Az.EventHub</span></span>
  - <span data-ttu-id="0a3b9-114">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0a3b9-114">Az.IotHub</span></span>
  - <span data-ttu-id="0a3b9-115">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a3b9-115">Az.KeyVault</span></span>
  - <span data-ttu-id="0a3b9-116">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0a3b9-116">Az.Monitor</span></span>
  - <span data-ttu-id="0a3b9-117">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a3b9-117">Az.Network</span></span>
  - <span data-ttu-id="0a3b9-118">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a3b9-118">Az.Resources</span></span>
  - <span data-ttu-id="0a3b9-119">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a3b9-119">Az.Storage</span></span>
  - <span data-ttu-id="0a3b9-120">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a3b9-120">Az.Websites</span></span>
* <span data-ttu-id="0a3b9-121">В PowerShell появились три новых модуля Az, которые работают с Azure Stack Hub: Az.Databox, Az.IotHub и Az.EventHub.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-121">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="0a3b9-122">Команды остаются прежними же за исключением незначительных изменений, таких как изменение AzureRM на Az.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-122">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="0a3b9-123">См. обновленную ссылку на документацию по [PowerShell для Azure Stack Hub](https://aka.ms/InstallASHPowerShell)</span><span class="sxs-lookup"><span data-stu-id="0a3b9-123">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0a3b9-124">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a3b9-124">Az.Accounts</span></span>
* <span data-ttu-id="0a3b9-125">Обновление ADAL до MSAL</span><span class="sxs-lookup"><span data-stu-id="0a3b9-125">Upgrade from ADAL to MSAL</span></span>


## <a name="370---march-2020"></a><span data-ttu-id="0a3b9-126">3.7.0 — март 2020 г.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-126">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0a3b9-127">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a3b9-127">Az.Accounts</span></span>
* <span data-ttu-id="0a3b9-128">Исправлено исключение NullReferenceException командлетов Get-AzTenant/Get-AzDefault/Set-AzDefault, если вход не выполнен [10292]</span><span class="sxs-lookup"><span data-stu-id="0a3b9-128">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a3b9-129">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a3b9-129">Az.Compute</span></span>
* <span data-ttu-id="0a3b9-130">Добавлены следующие параметры к командлету New-AzDiskConfig:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-130">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="0a3b9-131">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="0a3b9-131">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="0a3b9-132">Разрешено свойство Encryption для параметра Target командлета New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-132">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="0a3b9-133">Исправлена проблема с tempDisk для командлетов Set-AzVmss -Reimage и Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-133">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="0a3b9-134">[11354]</span><span class="sxs-lookup"><span data-stu-id="0a3b9-134">[#11354]</span></span>
* <span data-ttu-id="0a3b9-135">Добавлена поддержка нового расширения SAP для указанных ниже командлетов</span><span class="sxs-lookup"><span data-stu-id="0a3b9-135">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="0a3b9-136">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="0a3b9-136">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="0a3b9-137">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="0a3b9-137">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="0a3b9-138">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="0a3b9-138">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="0a3b9-139">Update-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="0a3b9-139">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="0a3b9-140">Исправлены ошибки в примерах справки</span><span class="sxs-lookup"><span data-stu-id="0a3b9-140">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="0a3b9-141">Показано точное строковое значение в табличном формате для свойства PowerState виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-141">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="0a3b9-142">New-AzVmssConfig: исправлена сериализация свойства AutomaticRepairs, если параметр SinglePlacementGroup отключен.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-142">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="0a3b9-143">[11257]</span><span class="sxs-lookup"><span data-stu-id="0a3b9-143">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a3b9-144">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a3b9-144">Az.DataFactory</span></span>
* <span data-ttu-id="0a3b9-145">Пакет SDK ADF для .NET обновлен до версии 4.8.0.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-145">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="0a3b9-146">Добавлены необязательные параметры для команды Invoke-AzDataFactoryV2Pipeline для поддержки повторного запуска.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-146">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0a3b9-147">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a3b9-147">Az.DataLakeStore</span></span>
* <span data-ttu-id="0a3b9-148">Добавлено описание критического изменения для Export-AzDataLakeStoreItem и Import-AzDataLakeStoreItem.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-148">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="0a3b9-149">Добавлен параметр кодирования байтов для New-AzDataLakeStoreItem, Add-AzDAtaLakeStoreItemContent и Get-AzDAtaLakeStoreItemContent.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-149">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="0a3b9-150">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0a3b9-150">Az.HDInsight</span></span>
* <span data-ttu-id="0a3b9-151">Добавлена поддержка указания минимальной поддерживаемой версии TLS при создании кластера.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-151">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0a3b9-152">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0a3b9-152">Az.IotHub</span></span>
* <span data-ttu-id="0a3b9-153">Добавлена поддержка для управления распределенными параметрами на отдельных устройствах.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-153">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="0a3b9-154">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-154">New Cmdlets are:</span></span>
    - <span data-ttu-id="0a3b9-155">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="0a3b9-155">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="0a3b9-156">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="0a3b9-156">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0a3b9-157">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a3b9-157">Az.KeyVault</span></span>
* <span data-ttu-id="0a3b9-158">Добавлены атрибуты критических изменений для New-AzKeyVault.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-158">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0a3b9-159">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0a3b9-159">Az.Monitor</span></span>
* <span data-ttu-id="0a3b9-160">Обновлена документация для New-AzScheduledQueryRuleLogMetricTrigger.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-160">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a3b9-161">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a3b9-161">Az.Network</span></span>
* <span data-ttu-id="0a3b9-162">Обновлены командлеты для поддержки подключений VirtualHubVnetConnections между клиентами</span><span class="sxs-lookup"><span data-stu-id="0a3b9-162">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="0a3b9-163">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="0a3b9-163">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="0a3b9-164">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="0a3b9-164">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="0a3b9-165">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="0a3b9-165">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="0a3b9-166">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="0a3b9-166">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="0a3b9-167">Удалена зависимость пакета SDK для управления SQL.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-167">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0a3b9-168">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0a3b9-168">Az.PolicyInsights</span></span>
* <span data-ttu-id="0a3b9-169">Улучшены сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-169">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a3b9-170">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a3b9-170">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a3b9-171">В Azure Site Recovery реализована поддержка повторной защиты и обновлены свойства зашифрованных виртуальных машин диска Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-171">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="0a3b9-172">Добавлена возможность мониторинг аварийного восстановления для свойств VmwareToAzure в Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-172">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="0a3b9-173">В Azure Backup реализована поддержка повторного обновления политики для элементов с ошибками.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-173">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="0a3b9-174">В Azure Backup реализована поддержка параметров исключения диска во время резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-174">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="0a3b9-175">В Azure Backup реализована поддержка восстановления нескольких файлов или папок в AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="0a3b9-175">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="0a3b9-176">В Azure Backup реализована поддержка указанной пользователем группы Resourcegroup при обновлении политики IaasVM.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-176">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a3b9-177">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a3b9-177">Az.Resources</span></span>
* <span data-ttu-id="0a3b9-178">Исправлена команда Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType для использования фактической версии apiVersion ресурсов (а не версии apiVersion по умолчанию) [11267].</span><span class="sxs-lookup"><span data-stu-id="0a3b9-178">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="0a3b9-179">Добавлена возможность регистрации correlationId для сценариев с ошибками.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-179">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="0a3b9-180">Незначительно изменена документация по Get-AzResourceLock.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-180">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="0a3b9-181">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-181">Added example.</span></span>
* <span data-ttu-id="0a3b9-182">Экранирована одинарная кавычка в значении параметра Get-AzADUser [11317].</span><span class="sxs-lookup"><span data-stu-id="0a3b9-182">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="0a3b9-183">Добавлены новые командлеты для сценариев развертывания (Get-AzDeploymentScript, Get-AzDeploymentScriptLog, Save-AzDeploymentScriptLog, Remove-AzDeploymentScript).</span><span class="sxs-lookup"><span data-stu-id="0a3b9-183">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a3b9-184">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a3b9-184">Az.Sql</span></span>
* <span data-ttu-id="0a3b9-185">Добавлен параметр вторичной реплики для чтения для командлета Invoke-AzSqlDatabaseFailover.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-185">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="0a3b9-186">Добавлен командлет Disable-AzSqlServerActiveDirectoryOnlyAuthentication.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-186">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="0a3b9-187">Сохранен приоритет конфиденциальности при классификации столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-187">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="0a3b9-188">Az.Support</span><span class="sxs-lookup"><span data-stu-id="0a3b9-188">Az.Support</span></span>
* <span data-ttu-id="0a3b9-189">Модуль Az.Support стал общедоступным.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-189">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a3b9-190">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a3b9-190">Az.Websites</span></span>
* <span data-ttu-id="0a3b9-191">Реализована поддержка работы с правилами маршрутизации трафика веб-приложения через указанные ниже командлеты</span><span class="sxs-lookup"><span data-stu-id="0a3b9-191">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="0a3b9-192">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="0a3b9-192">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="0a3b9-193">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="0a3b9-193">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="0a3b9-194">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="0a3b9-194">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="0a3b9-195">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="0a3b9-195">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="0a3b9-196">3.6.1 — март 2020 г.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-196">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0a3b9-197">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a3b9-197">Az.Accounts</span></span>
* <span data-ttu-id="0a3b9-198">Открытие страницы опроса Azure PowerShell в Send-Feedback [11020].</span><span class="sxs-lookup"><span data-stu-id="0a3b9-198">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="0a3b9-199">Отображение URL-адреса опроса Azure PowerShell в Resolve-Error [11021].</span><span class="sxs-lookup"><span data-stu-id="0a3b9-199">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="0a3b9-200">Добавлена версия Az в UserAgent.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-200">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="0a3b9-201">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a3b9-201">Az.ApiManagement</span></span>
* <span data-ttu-id="0a3b9-202">Включена поддержка получения и настройки личного домена в конечной точке DeveloperPortal [11007].</span><span class="sxs-lookup"><span data-stu-id="0a3b9-202">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="0a3b9-203">Export-AzApiManagementApi: включена поддержка скачивания определения API в формате JSON [9987].</span><span class="sxs-lookup"><span data-stu-id="0a3b9-203">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="0a3b9-204">Import-AzApiManagementApi: включена поддержка импорта определения OpenApi 3.0 из документа JSON.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-204">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="0a3b9-205">New-AzApiManagementIdentityProvider и Set-AzApiManagementIdentityProvider: включена поддержка настройки входа арендатора для поставщика AAD B2C [9784].</span><span class="sxs-lookup"><span data-stu-id="0a3b9-205">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0a3b9-206">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a3b9-206">Az.DataLakeStore</span></span>
* <span data-ttu-id="0a3b9-207">Добавлена ссылка на System.Buffers явным образом в CSPROJ и PSD1.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-207">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0a3b9-208">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0a3b9-208">Az.IotHub</span></span>
* <span data-ttu-id="0a3b9-209">Добавлена возможность управления устройствами в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-209">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="0a3b9-210">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-210">New Cmdlets are:</span></span>
    - <span data-ttu-id="0a3b9-211">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="0a3b9-211">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="0a3b9-212">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="0a3b9-212">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="0a3b9-213">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="0a3b9-213">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="0a3b9-214">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="0a3b9-214">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="0a3b9-215">Включена поддержка управления модулями в целевом устройстве Интернета вещей в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-215">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="0a3b9-216">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-216">New Cmdlets are:</span></span>
    - <span data-ttu-id="0a3b9-217">Add-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="0a3b9-217">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="0a3b9-218">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="0a3b9-218">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="0a3b9-219">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="0a3b9-219">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="0a3b9-220">Set-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="0a3b9-220">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="0a3b9-221">Добавлен командлет для получения строки подключения целевого устройства Интернета вещей в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-221">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="0a3b9-222">Добавлен командлет для получения строки подключения модуля на целевом устройстве Интернета вещей в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-222">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="0a3b9-223">Включена поддержка для получения или настройки родительского устройства для устройства Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-223">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="0a3b9-224">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-224">New Cmdlets are:</span></span>
    - <span data-ttu-id="0a3b9-225">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="0a3b9-225">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="0a3b9-226">Set-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="0a3b9-226">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="0a3b9-227">Включена поддержка управления связью "родители — потомки" устройства.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-227">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0a3b9-228">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0a3b9-228">Az.Monitor</span></span>
* <span data-ttu-id="0a3b9-229">Исправлено выходное значение для Get-AzMetricDefinition [9714].</span><span class="sxs-lookup"><span data-stu-id="0a3b9-229">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a3b9-230">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a3b9-230">Az.Network</span></span>
* <span data-ttu-id="0a3b9-231">Обновлен пакет SDK для управления SQL.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-231">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="0a3b9-232">Исправлена проблема с разницей в именовании в классе PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-232">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="0a3b9-233">Сопоставление ActionsRequired с ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-233">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="0a3b9-234">Добавление PublicNetworkAccess в команды New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-234">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a3b9-235">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a3b9-235">Az.Resources</span></span>
* <span data-ttu-id="0a3b9-236">Исправлена ошибка пустой ссылки в Get-AzRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-236">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="0a3b9-237">Параметры -Force и -PassThru помечены необязательными в Remove-AzADGroup [10849].</span><span class="sxs-lookup"><span data-stu-id="0a3b9-237">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="0a3b9-238">Исправлена ошибка, из-за которой MailNickname не возвращается в Remove-AzADGroup [11167].</span><span class="sxs-lookup"><span data-stu-id="0a3b9-238">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="0a3b9-239">Исправлена ошибка, из-за которой операция канала Remove-AzADGroup не работает [11171].</span><span class="sxs-lookup"><span data-stu-id="0a3b9-239">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="0a3b9-240">Исправлена ошибка с пустой ссылкой в GetAzureRoleAssignmentCommand.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-240">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="0a3b9-241">Добавлено критическое изменение атрибутов для будущих изменений командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-241">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="0a3b9-242">Обновлена команда Get-AzResourceGroup для выполнения фильтрации тегов группы ресурсов на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-242">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="0a3b9-243">Расширены командлеты Tag для включения поддержки параметра -ResourceId.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-243">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="0a3b9-244">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a3b9-244">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="0a3b9-245">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a3b9-245">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="0a3b9-246">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a3b9-246">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="0a3b9-247">Добавлен новый командлет Tag.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-247">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="0a3b9-248">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a3b9-248">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="0a3b9-249">Предоставляется ScopedDeployment из пакета SDK 3.3.0.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-249">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a3b9-250">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a3b9-250">Az.Sql</span></span>
* <span data-ttu-id="0a3b9-251">Добавление PublicNetworkAccess в команды New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-251">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="0a3b9-252">Включена поддержка конфигурации резервного копирования долгосрочного хранения для управляемых баз данных.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-252">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="0a3b9-253">Получение или настройка политики LTR в управляемой базе данных.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-253">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="0a3b9-254">Получение резервных копий LTR по управляемой базе данных, управляемому экземпляру или расположению.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-254">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="0a3b9-255">Удаление резервной копии LTR.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-255">Remove an LTR backup</span></span>
    - <span data-ttu-id="0a3b9-256">Восстановление резервной копии LTR для создания новой управляемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-256">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="0a3b9-257">Добавление MinimalTlsVersion в New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-257">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="0a3b9-258">Добавление MinimalTlsVersion в New-AzSqlInstance и Set-AzSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-258">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="0a3b9-259">Обновлена версия пакета SDK для SQL для Az.Network.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-259">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a3b9-260">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a3b9-260">Az.Storage</span></span>
* <span data-ttu-id="0a3b9-261">Включена поддержка AllowProtectedAppendWrite в ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-261">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="0a3b9-262">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="0a3b9-262">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="0a3b9-263">Добавлено предупреждение о критическом изменении для изменения типа AzureStorageTable в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-263">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="0a3b9-264">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="0a3b9-264">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="0a3b9-265">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="0a3b9-265">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a3b9-266">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a3b9-266">Az.Websites</span></span>
* <span data-ttu-id="0a3b9-267">Добавлен параметр Tag для New-AzAppServicePlan и Set-AzAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-267">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="0a3b9-268">Завершение выполнения командлета, если при добавлении личного домена на веб-сайт возникает исключение.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-268">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="0a3b9-269">Включена поддержка выполнения операций для Служб приложений, которые находятся не в той же группе ресурсов, что и план службы приложений.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-269">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="0a3b9-270">Применение ограничения доступа к WebApp/Function в разных группах ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-270">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="0a3b9-271">Исправлена ошибка с указанием пользовательских имен узлов для WebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-271">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="0a3b9-272">3.5.0 — февраль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-272">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0a3b9-273">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="0a3b9-273">Highlights since the last major release</span></span>
* <span data-ttu-id="0a3b9-274">Обновлены данные телеметрии на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-274">Updated client side telemetry.</span></span>
* <span data-ttu-id="0a3b9-275">В Az.IotHub добавлены командлеты для управления устройствами.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-275">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="0a3b9-276">В Az.SqlVirtualMachine добавлены командлеты для прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-276">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0a3b9-277">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a3b9-277">Az.Accounts</span></span>
* <span data-ttu-id="0a3b9-278">В данные телеметрии на стороне клиента добавлены такие сведения, как идентификатор подписки, идентификатор арендатора и время выполнения.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-278">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0a3b9-279">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0a3b9-279">Az.Automation</span></span>
* <span data-ttu-id="0a3b9-280">Исправлена опечатка в примере 1 в справочной документации по New-AzAutomationSoftwareUpdateConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-280">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0a3b9-281">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0a3b9-281">Az.CognitiveServices</span></span>
* <span data-ttu-id="0a3b9-282">Обновлен пакет SDK до версии 7.0.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-282">Updated SDK to 7.0</span></span>
* <span data-ttu-id="0a3b9-283">Улучшено сообщение об ошибке, которое появляется, если ответы сервера не содержат текст.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-283">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a3b9-284">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a3b9-284">Az.Compute</span></span>
* <span data-ttu-id="0a3b9-285">Разрешено использовать пустое значение для ProximityPlacementGroupId во время обновления.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-285">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0a3b9-286">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0a3b9-286">Az.FrontDoor</span></span>
* <span data-ttu-id="0a3b9-287">Добавлен командлет для получения определений управляемых правил, которые могут использоваться в WAF.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-287">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0a3b9-288">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0a3b9-288">Az.IotHub</span></span>
* <span data-ttu-id="0a3b9-289">Добавлена возможность управления устройствами в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-289">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="0a3b9-290">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-290">New Cmdlets are:</span></span>
    - <span data-ttu-id="0a3b9-291">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="0a3b9-291">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="0a3b9-292">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="0a3b9-292">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="0a3b9-293">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="0a3b9-293">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="0a3b9-294">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="0a3b9-294">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0a3b9-295">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a3b9-295">Az.KeyVault</span></span>
* <span data-ttu-id="0a3b9-296">Устранен дублирующийся текст для Add-AzKeyVaultKey.md.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-296">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0a3b9-297">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0a3b9-297">Az.Monitor</span></span>
* <span data-ttu-id="0a3b9-298">Исправлено описание командлета Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-298">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="0a3b9-299">В команду New-AzMetricAlertRuleV2 добавлен новый параметр ActionGroupId.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-299">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="0a3b9-300">Пользователь может предоставить ActionGroupId(string) или ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="0a3b9-300">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a3b9-301">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a3b9-301">Az.Network</span></span>
* <span data-ttu-id="0a3b9-302">Добавлен еще один параметр -EnableProxyProtocol для командлета New-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-302">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="0a3b9-303">Исправлен пример FilterData в Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-303">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="0a3b9-304">Добавлен пример Packet Capture для всех внутренних и внешних пакетов в Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-304">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="0a3b9-305">Добавлена поддерживаемая политика Брандмауэра Azure в брандмауэрах виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-305">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="0a3b9-306">Новые командлеты не добавлены.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-306">No new cmdlets are added.</span></span> <span data-ttu-id="0a3b9-307">Снято ограничение политики брандмауэра в брандмауэрах виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-307">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a3b9-308">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a3b9-308">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a3b9-309">Добавлена возможность восстановления в виде файлов для Баз данных SQL.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-309">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a3b9-310">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a3b9-310">Az.Resources</span></span>
* <span data-ttu-id="0a3b9-311">Выполнен рефакторинг командлетов развертывания шаблона.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-311">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="0a3b9-312">Добавлены новые командлеты для управления развертываниями в группе управления: \*-AzManagementGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-312">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="0a3b9-313">Добавлены новые командлеты для управления развертываниями в области арендатора: \*-AzTenantDeployment.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-313">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="0a3b9-314">Выполнен рефакторинг командлетов \*-AzDeployment для работы в области подписки.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-314">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="0a3b9-315">Созданы псевдонимы \*-AzSubscriptionDeployment для командлетов \*-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-315">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="0a3b9-316">Исправлен командлет Update-AzADApplication, когда параметр AvailableToOtherTenants не задан.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-316">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="0a3b9-317">Удален набор параметров ApplicationObjectWithoutCredentialParameterSet, чтобы предотвратить возникновение AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-317">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="0a3b9-318">Повторно созданы файлы справки.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-318">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a3b9-319">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a3b9-319">Az.Sql</span></span>
* <span data-ttu-id="0a3b9-320">Добавлена возможность восстановления точки во времени между подписками в Управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-320">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="0a3b9-321">Добавлена возможность изменения существующего поколения оборудования Управляемого экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-321">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="0a3b9-322">Исправлены примеры справки Update-AzSqlServerVulnerabilityAssessmentSetting: выходные данные параметра и свойства — EmailAdmins.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-322">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="0a3b9-323">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="0a3b9-323">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="0a3b9-324">Добавлены командлеты для прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-324">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="0a3b9-325">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="0a3b9-325">Az.StorageSync</span></span>
* <span data-ttu-id="0a3b9-326">В командлете Invoke-AzStorageSyncCompatibilityCheck обновлены поддерживаемые наборы символов.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-326">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="0a3b9-327">3.4.0 — февраль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-327">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0a3b9-328">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="0a3b9-328">Highlights since the last major release</span></span>
* <span data-ttu-id="0a3b9-329">Выпущена первоначальная версия 0.1.0 Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="0a3b9-329">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="0a3b9-330">Добавлена поддержка Az.Network ConnectionMonitor V2</span><span class="sxs-lookup"><span data-stu-id="0a3b9-330">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0a3b9-331">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a3b9-331">Az.Accounts</span></span>
* <span data-ttu-id="0a3b9-332">Отключить автоматическое сохранение контекста, если AzureRmContext.json недоступен</span><span class="sxs-lookup"><span data-stu-id="0a3b9-332">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="0a3b9-333">Обновление ссылки на Azure Powershell Common до предварительной версии 1.3.5</span><span class="sxs-lookup"><span data-stu-id="0a3b9-333">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="0a3b9-334">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a3b9-334">Az.ApiManagement</span></span>
* <span data-ttu-id="0a3b9-335">**Get-AzApiManagementApiSchema** Исправлено получение схемы Open-API, связанной с API https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="0a3b9-335">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="0a3b9-336">**New-AzApiManagementProduct** _ и _ *Set-AzApiManagementProduct*\*</span><span class="sxs-lookup"><span data-stu-id="0a3b9-336">**New-AzApiManagementProduct** _ and _ *Set-AzApiManagementProduct*\*</span></span>
  - <span data-ttu-id="0a3b9-337">Исправить документацию для https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="0a3b9-337">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="0a3b9-338">**Set-AzApiManagementApi** Добавлен пример, показывающий, как обновить ServiceUrl с помощью командлета</span><span class="sxs-lookup"><span data-stu-id="0a3b9-338">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a3b9-339">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a3b9-339">Az.Compute</span></span>
* <span data-ttu-id="0a3b9-340">Ограничение числа состояний виртуальных машин до 100, чтобы избежать регулирования при выполнении Get-AzVM-Status без имени виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-340">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="0a3b9-341">Добавление обновления командлета -AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="0a3b9-341">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="0a3b9-342">Добавление параметров EncryptionType и DiskEncryptionSetId в следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-342">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="0a3b9-343">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="0a3b9-343">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="0a3b9-344">Добавление параметра ColocationStatus в командлет Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-344">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a3b9-345">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a3b9-345">Az.DataFactory</span></span>
* <span data-ttu-id="0a3b9-346">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.7.0.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-346">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="0a3b9-347">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="0a3b9-347">Az.DeploymentManager</span></span>
* <span data-ttu-id="0a3b9-348">Добавляет операции LIST для ресурсов</span><span class="sxs-lookup"><span data-stu-id="0a3b9-348">Adds LIST operations for resources</span></span>
* <span data-ttu-id="0a3b9-349">Добавляет возможность выполнения операций на этапах Проверки работоспособности</span><span class="sxs-lookup"><span data-stu-id="0a3b9-349">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="0a3b9-350">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0a3b9-350">Az.HDInsight</span></span>
* <span data-ttu-id="0a3b9-351">Исправление ошибки в документе New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-351">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0a3b9-352">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a3b9-352">Az.KeyVault</span></span>
* <span data-ttu-id="0a3b9-353">Добавление Псевдонимов имени в атрибут VaultName, чтобы Remove-AzureKeyVault соответствовал New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-353">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a3b9-354">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a3b9-354">Az.Network</span></span>
* <span data-ttu-id="0a3b9-355">В Set-AzNetworkWatcherConfigFlowLog.md добавлен новый пример для демонстрации сценария отключения Аналитики трафика.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-355">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="0a3b9-356">Добавление поддержки назначения IP-конфигурации для брандмауэра Azure — выделенная подсеть и общедоступный IP-адрес, которые брандмауэр будет использовать для управления трафиком</span><span class="sxs-lookup"><span data-stu-id="0a3b9-356">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="0a3b9-357">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-357">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="0a3b9-358">добавлен параметр — ManagementPublicIpAddress (необязательный), который принимает объект общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="0a3b9-358">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="0a3b9-359">Добавлен метод SetManagementIpConfiguration для объекта брандмауэра — в качестве входных данных требуется подсеть и общедоступный IP-адрес — имя подсети должно быть "AzureFirewallManagementSubnet"</span><span class="sxs-lookup"><span data-stu-id="0a3b9-359">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="0a3b9-360">Исправлены примеры Get-AzNetworkSecurityGroup для отображения примеров для группы безопасности сети (NSG) вместо сетевых интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-360">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="0a3b9-361">Исправлена опечатка в команде New-AzVpnSite, которая препятствовала завершению параметра идентификатором ресурса.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-361">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="0a3b9-362">Добавлена поддержка конфигурации в наборе действий для правил подстановки URL-адресов в шлюзе приложения.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-362">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="0a3b9-363">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-363">New cmdlets added:</span></span>
        - <span data-ttu-id="0a3b9-364">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a3b9-364">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="0a3b9-365">В следующие командлеты добавлен необязательный параметр — UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a3b9-365">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="0a3b9-366">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="0a3b9-366">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="0a3b9-367">Добавление поддержки для ресурсов NetworkWatcher ConnectionMonitor версии 2</span><span class="sxs-lookup"><span data-stu-id="0a3b9-367">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0a3b9-368">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0a3b9-368">Az.PolicyInsights</span></span>
* <span data-ttu-id="0a3b9-369">Поддержка оценки соответствия до определения того, какой ресурс нужно исправить</span><span class="sxs-lookup"><span data-stu-id="0a3b9-369">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="0a3b9-370">Добавление параметра "—ResourceDiscoverMode" в Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="0a3b9-370">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="0a3b9-371">Добавление командлета Get-AzPolicyMetadata для получения ресурсов метаданных политики</span><span class="sxs-lookup"><span data-stu-id="0a3b9-371">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="0a3b9-372">Get-AzPolicyState и Get-AzPolicyStateSummary обновлены для API версии 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="0a3b9-372">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a3b9-373">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a3b9-373">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a3b9-374">Поддержка Azure Site Recovery для удаления реплицированного диска.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-374">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="0a3b9-375">В Azure Backup добавлена ​​поддержка добавления тегов при создании Хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-375">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a3b9-376">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a3b9-376">Az.Resources</span></span>
* <span data-ttu-id="0a3b9-377">Сделайте команду "Область" необязательной в командлетах \*—AzPolicyAssignment с настройкой по умолчанию для контекстной подписки</span><span class="sxs-lookup"><span data-stu-id="0a3b9-377">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="0a3b9-378">Добавление примеров создания ADServicePrincipal с паролем и ключом учетных данных</span><span class="sxs-lookup"><span data-stu-id="0a3b9-378">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a3b9-379">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a3b9-379">Az.Sql</span></span>
<span data-ttu-id="0a3b9-380">Исправление командлета New-AzSqlDatabaseSecondary, чтобы проверить существование PartnerDatabaseName, а не DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-380">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a3b9-381">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a3b9-381">Az.Storage</span></span>
* <span data-ttu-id="0a3b9-382">Поддержка набора шифрования типа ключа таблиц и очередей в создании учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="0a3b9-382">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="0a3b9-383">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a3b9-383">New-AzStorageAccount</span></span>
* <span data-ttu-id="0a3b9-384">Представление RequestId, если StorageException не имеет ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="0a3b9-384">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="0a3b9-385">Исправление примера 6 командлета Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0a3b9-385">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a3b9-386">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a3b9-386">Az.Websites</span></span>
* <span data-ttu-id="0a3b9-387">Set-AzWebapp и Set-AzWebappSlot поддерживают свойства AlwaysOn, MinTls и FtpsState</span><span class="sxs-lookup"><span data-stu-id="0a3b9-387">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="0a3b9-388">Устранение проблемы, при которой параметр HttpsOnly с одновременным изменением AppservicePlan с помощью одной команды Set-AzWebApp сбрасывал значение HttpsOnly до значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="0a3b9-388">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="0a3b9-389">3.3.0 — январь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-389">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0a3b9-390">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a3b9-390">Az.Accounts</span></span>
* <span data-ttu-id="0a3b9-391">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment: теперь они принимают параметры AzureAttestationServiceEndpointResourceId и AzureAttestationServiceEndpointSuffix.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-391">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0a3b9-392">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0a3b9-392">Az.Cdn</span></span>
* <span data-ttu-id="0a3b9-393">Теперь в командлете New-AzCdnEndpoint отображаются сведения из сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-393">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a3b9-394">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a3b9-394">Az.Compute</span></span>
* <span data-ttu-id="0a3b9-395">Командлет Set-AzVMCustomScriptExtension исправлен для виртуальной машины с управляемым диском ОС без профиля ОС.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-395">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="0a3b9-396">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0a3b9-396">Az.ContainerInstance</span></span>
* <span data-ttu-id="0a3b9-397">Исправлены имена параметров, используемые в примере командлета New-AzContainerGroup.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-397">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="0a3b9-398">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="0a3b9-398">Az.DataBoxEdge</span></span>
* <span data-ttu-id="0a3b9-399">Добавлен командлет Get-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-399">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="0a3b9-400">получение контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-400">Get the Edge Storage Container</span></span>
* <span data-ttu-id="0a3b9-401">Добавлен командлет New-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-401">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="0a3b9-402">создание контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-402">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="0a3b9-403">Добавлен командлет Remove-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-403">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="0a3b9-404">удаление контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-404">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="0a3b9-405">Добавлен командлет Invoke-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-405">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="0a3b9-406">вызов действия для обновления данных в контейнере хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-406">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="0a3b9-407">Добавлен командлет Get-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-407">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="0a3b9-408">получение учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-408">Get the Edge Storage Account</span></span>
* <span data-ttu-id="0a3b9-409">Добавлен командлет New-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-409">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="0a3b9-410">создание учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-410">Create new Edge Storage Account</span></span>
* <span data-ttu-id="0a3b9-411">Добавлен командлет Remove-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-411">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="0a3b9-412">удаление учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-412">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="0a3b9-413">Вызов командлета Invoke-AzDataBoxEdgeShare:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-413">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="0a3b9-414">вызов действия для обновления данных в общей папке.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-414">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="0a3b9-415">Добавлен командлет Set-AzDataBoxEdgeStorageAccountCredential:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-415">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="0a3b9-416">установка учетных данных для учетной записи хранилища Azure Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-416">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a3b9-417">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a3b9-417">Az.DataFactory</span></span>
* <span data-ttu-id="0a3b9-418">Добавлены свойства AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId и VersionStatus для командлета Get-AzDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-418">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="0a3b9-419">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.6.0.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-419">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="0a3b9-420">Для командлета Set-AzureRmDataFactoryV2IntegrationRuntime добавлен параметр PublicIPs, позволяющий включить создание среды Azure-SSIS IR со статическими общедоступными IP-адресами.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-420">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="0a3b9-421">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="0a3b9-421">Az.DevTestLabs</span></span>
* <span data-ttu-id="0a3b9-422">Удалена недействительная ссылка в файле Get-AzDtlAllowedVMSizesPolicy.md.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-422">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0a3b9-423">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0a3b9-423">Az.EventHub</span></span>
* <span data-ttu-id="0a3b9-424">Устранена проблема № 10634: исправлена ссылка на пустой объект для удаления пространства имен концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-424">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="0a3b9-425">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0a3b9-425">Az.HDInsight</span></span>
* <span data-ttu-id="0a3b9-426">Устранена ошибка в файле Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-426">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="0a3b9-427">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="0a3b9-427">Az.MachineLearning</span></span>
* <span data-ttu-id="0a3b9-428">Вычислительная среда Машинного обучения больше недоступна, поэтому удалены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-428">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="0a3b9-429">Get-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-429">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="0a3b9-430">Get-AzMlOpClusterKey;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-430">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="0a3b9-431">New-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-431">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="0a3b9-432">Remove-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-432">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="0a3b9-433">Set-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-433">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="0a3b9-434">Test-AzMlOpClusterSystemServicesUpdateAvailability;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-434">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="0a3b9-435">Update-AzMlOpClusterSystemService.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-435">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a3b9-436">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a3b9-436">Az.Network</span></span>
* <span data-ttu-id="0a3b9-437">Обновлена зависимость Microsoft.Azure.Management.Sql от предварительной версии 1.36 до предварительной версии 1.37.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-437">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a3b9-438">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a3b9-438">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a3b9-439">Добавлена поддержка Azure Site Recovery для виртуальных машин с управляемым диском, зашифрованных при хранении с помощью управляемых клиентом ключей, при восстановлении из Azure в поставщике Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-439">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="0a3b9-440">Добавлена поддержка Azure Site Recovery для необязательного ввода идентификатора набора шифрования диска при включении защиты в рамках восстановления из VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-440">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="0a3b9-441">Добавлена поддержка Azure Site Recovery для необязательного ввода идентификатора набора шифрования диска на уровне диска при включении защиты в рамках восстановления из VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-441">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="0a3b9-442">Добавлена поддержка Azure Site Recovery для обновления элемента, защищенного репликацией, путем сопоставления набора шифрования диска при восстановлении из HyperV в Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-442">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a3b9-443">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a3b9-443">Az.Resources</span></span>
* <span data-ttu-id="0a3b9-444">Исправлена ошибка в справочном документе о командлете Remove-AzTag.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-444">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a3b9-445">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a3b9-445">Az.Sql</span></span>
* <span data-ttu-id="0a3b9-446">Исправлена функция основных командлетов установки оценки уязвимостей: теперь она позволяет работать с базой данных master для базы данных Azure и ограничить ее в системных базах данных управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-446">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="0a3b9-447">Устранена ошибка, возникающая при создании группы отработки отказа экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-447">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="0a3b9-448">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="0a3b9-448">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="0a3b9-449">Добавлен новый допустимый тип лицензии: DR (аварийное восстановление).</span><span class="sxs-lookup"><span data-stu-id="0a3b9-449">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a3b9-450">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a3b9-450">Az.Storage</span></span>
* <span data-ttu-id="0a3b9-451">Добавлено предупреждающее сообщение о критическом изменении значения DefaultAction в следующем выпуске:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-451">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="0a3b9-452">Update-AzStorageAccountNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-452">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="0a3b9-453">Включена поддержка получения времени последней синхронизации учетной записи хранения путем выполнения командлета Get-AzureRmStorageAccount с параметром -IncludeGeoReplicationStats:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-453">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="0a3b9-454">Get-AzureRmStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-454">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="0a3b9-455">3.2.0 — декабрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-455">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="0a3b9-456">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="0a3b9-456">General</span></span>
* <span data-ttu-id="0a3b9-457">Обновление ссылок в .psd1 для использования относительного пути для всех модулей.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-457">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0a3b9-458">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a3b9-458">Az.Accounts</span></span>
* <span data-ttu-id="0a3b9-459">Установка правильного параметра UserAgent для телеметрии на стороне клиента для Az 4.0 (предварительная версия).</span><span class="sxs-lookup"><span data-stu-id="0a3b9-459">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="0a3b9-460">Отображение понятного пользователю сообщения об ошибке, если в Az 4.0 (предварительная версия) не указан контекст.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-460">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="0a3b9-461">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0a3b9-461">Az.Batch</span></span>
* <span data-ttu-id="0a3b9-462">Исправлена проблема [№ 10602](https://github.com/Azure/azure-powershell/issues/10602), из-за которой использование командлета **New-AzBatchPool** приводило к неправильной отправке VirtualMachineConfiguration.ContainerConfiguration или VirtualMachineConfiguration.DataDisks на сервер.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-462">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a3b9-463">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a3b9-463">Az.DataFactory</span></span>
* <span data-ttu-id="0a3b9-464">Обновление пакета SDK Фабрики данных для .NET до версии 4.5.0.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-464">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0a3b9-465">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0a3b9-465">Az.FrontDoor</span></span>
* <span data-ttu-id="0a3b9-466">Включена поддержка исключений управляемых правил WAF.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-466">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="0a3b9-467">Добавление SocketAddr в список автозавершения.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-467">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="0a3b9-468">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="0a3b9-468">Az.HealthcareApis</span></span>
* <span data-ttu-id="0a3b9-469">Обработка исключений.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-469">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0a3b9-470">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a3b9-470">Az.KeyVault</span></span>
* <span data-ttu-id="0a3b9-471">Исправлена ошибка при получении доступа к значению, которое может быть не задано.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-471">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="0a3b9-472">Управление сертификатами шифрования на основе эллиптических кривых.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-472">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="0a3b9-473">Включена возможность указания кривой для политик сертификатов.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-473">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0a3b9-474">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0a3b9-474">Az.Monitor</span></span>
* <span data-ttu-id="0a3b9-475">Добавление необязательного аргумента в команду добавления параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-475">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="0a3b9-476">Существующий аргумент switch указывает на то, что экспорт в Log Analytics должен выполняться в фиксированную схему</span><span class="sxs-lookup"><span data-stu-id="0a3b9-476">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="0a3b9-477">(выделенный тип данных).</span><span class="sxs-lookup"><span data-stu-id="0a3b9-477">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a3b9-478">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a3b9-478">Az.Network</span></span>
* <span data-ttu-id="0a3b9-479">В приложении AzureFirewall, NAT и сетевых правилах включена поддержка IpGroups.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-479">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a3b9-480">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a3b9-480">Az.Resources</span></span>
* <span data-ttu-id="0a3b9-481">Устранена проблема, из-за которой при развертывании шаблона не удавалось считать его параметр, если имя параметра конфликтовало с именем встроенного параметра.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-481">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="0a3b9-482">Обновлены командлеты политики для использования новой версии API 2019-09-01 с поддержкой группирования в определениях наборов политик.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-482">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a3b9-483">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a3b9-483">Az.Sql</span></span>
* <span data-ttu-id="0a3b9-484">Обновлена функция автоматического создания расширенного хранилища для службы оценки уязвимостей в учетной записи StorageV2.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-484">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a3b9-485">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a3b9-485">Az.Storage</span></span>
* <span data-ttu-id="0a3b9-486">Включена поддержка создания маркера SAS на основе удостоверения контейнера и большого двоичного объекта с аутентификацией Oauth на основе контекста службы хранилища:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-486">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="0a3b9-487">New-AzStorageContainerSASToken;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-487">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="0a3b9-488">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="0a3b9-488">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="0a3b9-489">Отозвана поддержка ключей делегирования пользователя учетной записи хранения, а также всех маркеров SAS удостоверения:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-489">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="0a3b9-490">Revoke-AzStorageAccountUserDelegationKeys.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-490">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="0a3b9-491">Выполнено обновление до Microsoft.Azure.Management.Storage версии 14.2.0 для включения поддержки нового API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-491">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="0a3b9-492">Включена поддержка QuotaGiB (квота общего ресурса в ГиБ) для значений свыше 5120 в командлетах для работы с общими папками в плоскости управления и добавлен псевдоним Quota для параметра QuotaGiB.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-492">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="0a3b9-493">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-493">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="0a3b9-494">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-494">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="0a3b9-495">Добавлен псевдоним QuotaGiB для параметра Quota:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-495">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="0a3b9-496">Set-AzStorageShareQuota.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-496">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="0a3b9-497">Устранена проблема, из-за которой при использовании AzStorageContainerAcl могла очищаться хранимая политика доступа:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-497">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="0a3b9-498">Set-AzStorageContainerAcl.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-498">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="0a3b9-499">Версия 3.1.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-499">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0a3b9-500">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="0a3b9-500">Highlights since the last major release</span></span>
* <span data-ttu-id="0a3b9-501">Выпуск Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="0a3b9-501">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="0a3b9-502">Выпуск Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="0a3b9-502">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a3b9-503">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a3b9-503">Az.Compute</span></span>
* <span data-ttu-id="0a3b9-504">Функция повторного применения виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="0a3b9-504">VM Reapply feature</span></span>
    - <span data-ttu-id="0a3b9-505">Добавлен параметр повторного применения в командлет Set-AzVM.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-505">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="0a3b9-506">Функция AutomaticRepairs масштабируемого набора виртуальных машин:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-506">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="0a3b9-507">Добавлены параметры EnableAutomaticRepair, AutomaticRepairGracePeriod и AutomaticRepairMaxInstanceRepairsPercent в следующие командлеты:   New-AzVmssConfig Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0a3b9-507">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="0a3b9-508">Включена поддержка образа из коллекции разных клиентов для New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-508">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="0a3b9-509">Добавлен фрагмент Spot в средство заполнения аргументов параметра Priority в командлетах New-AzVM, New-AzVMConfig и New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-509">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="0a3b9-510">Добавлены параметры DiskIOPSReadWrite и DiskMBpsReadWrite в командлет Add-AzVmssDataDisk.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-510">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="0a3b9-511">Изменен параметр SourceImageId командлета New-AzGalleryImageVersion на необязательный.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-511">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="0a3b9-512">Добавлены параметры OSDiskImage и DataDiskImage в командлет New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-512">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="0a3b9-513">Добавлен параметр HyperVGeneration в командлет New-AzGalleryImageDefinition.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-513">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="0a3b9-514">Добавлены параметры SkipExtensionsOnOverprovisionedVMs в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-514">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="0a3b9-515">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="0a3b9-515">Az.DataBoxEdge</span></span>
* <span data-ttu-id="0a3b9-516">Добавлен командлет `Get-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-516">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="0a3b9-517">Получение заказа.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-517">Get the Order</span></span>
* <span data-ttu-id="0a3b9-518">Добавлен командлет `New-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-518">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="0a3b9-519">Создание заказа.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-519">Create new Order</span></span>
* <span data-ttu-id="0a3b9-520">Добавлен командлет `Remove-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-520">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="0a3b9-521">Удаление заказа.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-521">Remove the Order</span></span>
* <span data-ttu-id="0a3b9-522">Изменен командлет `New-AzDataBoxEdgeShare`.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-522">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="0a3b9-523">Создание локальной общей папки.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-523">Now creates Local Share</span></span>
* <span data-ttu-id="0a3b9-524">Добавлен командлет `Set-AzDataBoxEdgeRole`.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-524">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="0a3b9-525">Сопоставление IotRole с общей папкой.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-525">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="0a3b9-526">Добавлен командлет `Invoke-AzDataBoxEdgeDevice`.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-526">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="0a3b9-527">Вызов проверки обновлений, скачивание обновления, установка обновления на устройстве.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-527">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="0a3b9-528">Добавлен командлет `Get-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-528">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="0a3b9-529">Получение сведений о триггерах.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-529">Gets the information about Triggers</span></span>
* <span data-ttu-id="0a3b9-530">Добавлен командлет `New-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-530">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="0a3b9-531">Создание триггеров.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-531">Create new Triggers</span></span>
* <span data-ttu-id="0a3b9-532">Добавлен командлет `Remove-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-532">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="0a3b9-533">Удаление триггеров.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-533">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a3b9-534">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a3b9-534">Az.DataFactory</span></span>
* <span data-ttu-id="0a3b9-535">Обновление пакета SDK Фабрики данных для .NET до версии 4.4.0.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-535">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="0a3b9-536">Добавлен параметр ExpressCustomSetup в командлет Set-AzureRmDataFactoryV2IntegrationRuntime для включения конфигураций установки и сторонних компонентов без использования настраиваемого скрипта установки.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-536">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0a3b9-537">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a3b9-537">Az.DataLakeStore</span></span>
* <span data-ttu-id="0a3b9-538">Обновлена документация по Get-AzDataLakeStoreDeletedItem и Restore-AzDataLakeStoreDeletedItem.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-538">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0a3b9-539">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0a3b9-539">Az.EventHub</span></span>
* <span data-ttu-id="0a3b9-540">Исправлена проблема № 10301. Исправлен формат даты маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-540">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0a3b9-541">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0a3b9-541">Az.FrontDoor</span></span>
* <span data-ttu-id="0a3b9-542">Добавлен параметр MinimumTlsVersion в Enable-AzFrontDoorCustomDomainHttps и New-AzFrontDoorFrontendEndpointObject.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-542">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="0a3b9-543">Добавлены параметры HealthProbeMethod и EnabledState в New-AzFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-543">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="0a3b9-544">Добавлен новый командлет для создания объекта BackendPoolsSettings для передачи при создании и обновлении Front Door.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-544">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="0a3b9-545">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="0a3b9-545">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a3b9-546">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a3b9-546">Az.Network</span></span>
* <span data-ttu-id="0a3b9-547">Изменены примеры параметра FilterData Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-547">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="0a3b9-548">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="0a3b9-548">Az.PrivateDns</span></span>
* <span data-ttu-id="0a3b9-549">Пакет SDK PrivateDns для .NET обновлен до версии 1.0.0</span><span class="sxs-lookup"><span data-stu-id="0a3b9-549">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a3b9-550">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a3b9-550">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a3b9-551">Включена поддержка Azure Site Recovery для выбора типа диска при включении защиты.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-551">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="0a3b9-552">Внесено исправление Azure Site Recovery для изменения действия плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-552">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="0a3b9-553">Включена поддержка восстановления SQL Azure Backup для принятия баз данных файлового потока.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-553">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="0a3b9-554">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0a3b9-554">Az.RedisCache</span></span>
* <span data-ttu-id="0a3b9-555">Добавлен параметр MinimumTlsVersion в командлеты New-AzRedisCache и Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-555">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="0a3b9-556">Кроме того, добавлен параметр MinimumTlsVersion в выходные данные командлета Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-556">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="0a3b9-557">Добавлена проверка параметра -Size для командлетов Set-AzRedisCache и New-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-557">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a3b9-558">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a3b9-558">Az.Resources</span></span>
- <span data-ttu-id="0a3b9-559">Обновлены командлеты политики для использования новой версии API 2019-06-01 с новым свойством EnforcementMode в назначении политики.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-559">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="0a3b9-560">Обновлен пример справки по созданию определения политики</span><span class="sxs-lookup"><span data-stu-id="0a3b9-560">Updated create policy definition help example</span></span>
- <span data-ttu-id="0a3b9-561">Исправлена ошибка с параметром -ServicePrincipalName командлета Remove-AZADServicePrincipal с возвратом пустой ссылки, если имя субъекта службы не найдено.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-561">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="0a3b9-562">Исправлена ошибка с New-AZADServicePrincipal с возвратом пустой ссылки, если у клиента нет подписки.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-562">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="0a3b9-563">Изменен командлет New-AzAdServicePrincipal для добавления учетных данных только для связанного приложения.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-563">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a3b9-564">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a3b9-564">Az.Sql</span></span>
* <span data-ttu-id="0a3b9-565">Добавлена поддержка ReadReplicaCount для базы данных.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-565">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="0a3b9-566">Исправлена ошибка с Set-AzSqlDatabase, если избыточность в пределах зоны не настроена.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-566">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="0a3b9-567">Версия 3.0.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-567">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="0a3b9-568">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="0a3b9-568">General</span></span>
* <span data-ttu-id="0a3b9-569">Выпущена версия Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="0a3b9-569">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0a3b9-570">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a3b9-570">Az.Accounts</span></span>
* <span data-ttu-id="0a3b9-571">Добавлено сообщение об устаревании для псевдонима "Resolve-Error".</span><span class="sxs-lookup"><span data-stu-id="0a3b9-571">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="0a3b9-572">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="0a3b9-572">Az.Advisor</span></span>
* <span data-ttu-id="0a3b9-573">Добавлена новая категория Operational Excellence (Эффективность работы) в командлет Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-573">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="0a3b9-574">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0a3b9-574">Az.Batch</span></span>
* <span data-ttu-id="0a3b9-575">`CoreQuota` в `BatchAccountContext` переименован в `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-575">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="0a3b9-576">Также появился новый `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-576">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="0a3b9-577">Это влияет на **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-577">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="0a3b9-578">Параметр **New-AzBatchTask** `-ResourceFile` теперь принимает коллекцию объектов `PSResourceFile`, которые можно создать с помощью нового командлета **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-578">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="0a3b9-579">Новый командлет **New-AzBatchResourceFile** , который помогает создавать объекты `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-579">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="0a3b9-580">Их можно передавать в **New-AzBatchTask** в параметре `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-580">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="0a3b9-581">Это позволяет поддерживать два новых типа файлов ресурсов, которые дополняют существующий метод `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-581">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="0a3b9-582">Файлы ресурсов на основе `AutoStorageContainerName` скачивают весь контейнер автоматического хранения в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-582">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="0a3b9-583">Файлы ресурсов на основе `StorageContainerUrl` скачивают указанный в URL-адресе контейнер в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-583">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="0a3b9-584">Удалено свойство `ApplicationPackages` в `PSApplication`, который возвращается из **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-584">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="0a3b9-585">Отдельные пакеты в приложении теперь можно извлечь с помощью **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-585">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="0a3b9-586">Например: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-586">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="0a3b9-587">`ApplicationId` переименован в `ApplicationName` для **Get-AzBatchApplicationPackage** , **New-AzBatchApplicationPackage** , **Remove-AzBatchApplicationPackage** , **Get-AzBatchApplication** , **New-AzBatchApplication** , **Remove-AzBatchApplication** и **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-587">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage** , **New-AzBatchApplicationPackage** , **Remove-AzBatchApplicationPackage** , **Get-AzBatchApplication** , **New-AzBatchApplication** , **Remove-AzBatchApplication** , and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="0a3b9-588">Теперь `ApplicationId` является псевдонимом для `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-588">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="0a3b9-589">Добавлено новое свойство `PSWindowsUserConfiguration` в `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-589">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="0a3b9-590">`Version` переименован в `Name` для `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-590">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="0a3b9-591">`BlobSource` переименован в `HttpUrl` для `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-591">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="0a3b9-592">Удалено свойство `OSDisk` из `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-592">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="0a3b9-593">Удалена операция **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-593">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="0a3b9-594">Больше она не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-594">This operation is no longer supported.</span></span>
* <span data-ttu-id="0a3b9-595">Удалено `TargetOSVersion` из `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-595">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="0a3b9-596">`CurrentOSVersion` переименован в `OSVersion` для `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-596">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="0a3b9-597">Удалено `DataEgressGiB` и `DataIngressGiB` из `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-597">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="0a3b9-598">Операция **Get-AzBatchNodeAgentSku** удалена и заменена на **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-598">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="0a3b9-599">**Get-AzBatchSupportedImage** возвращает те же данные, что и **Get-AzBatchNodeAgentSku** , но в более удобном формате.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-599">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="0a3b9-600">Также возвращаются новые непроверенные образы.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-600">New non-verified images are also now returned.</span></span> <span data-ttu-id="0a3b9-601">Включается и дополнительная информация о `Capabilities` и `BatchSupportEndOfLife` для каждого образа.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-601">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="0a3b9-602">Добавлена возможность монтировать файловые системы на каждом узле пула с помощью нового параметра `MountConfiguration` в **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-602">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="0a3b9-603">Теперь поддерживаются правила безопасности сети, которые блокируют сетевой доступ к пулу по исходящему порту трафика.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-603">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="0a3b9-604">Это выполняется с помощью свойства `SourcePortRanges` для `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-604">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="0a3b9-605">Что касается выполнения контейнеров, пакетная служба теперь поддерживает выполнение задачи в рабочей папке контейнера или рабочей папке задачи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-605">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="0a3b9-606">Выбор зависит от параметра `WorkingDirectory` в `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-606">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="0a3b9-607">Добавлена возможность указать коллекцию общедоступных IP-адресов для `PSNetworkConfiguration` с помощью нового свойства `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-607">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="0a3b9-608">Это гарантирует, что узлы в пуле будут иметь IP-адреса из списка, предоставленного пользователем.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-608">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="0a3b9-609">Если значение не задано, по умолчанию для `WaitForSuccess` в `PSSTartTask` используется значение `$True` (ранее `$False`).</span><span class="sxs-lookup"><span data-stu-id="0a3b9-609">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="0a3b9-610">Если значение не задано, по умолчанию для `Scope` в `PSAutoUserSpecification` используется значение `Pool` (ранее `Task` для Windows или `Pool` для Linux).</span><span class="sxs-lookup"><span data-stu-id="0a3b9-610">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0a3b9-611">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0a3b9-611">Az.Cdn</span></span>
* <span data-ttu-id="0a3b9-612">Добавлены UrlRewriteAction и CacheKeyQueryStringAction в RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-612">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="0a3b9-613">Исправлено несколько ошибок, таких как отсутствующий входной параметр Selector в командлете New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-613">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a3b9-614">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a3b9-614">Az.Compute</span></span>
* <span data-ttu-id="0a3b9-615">Функция набора шифрования диска</span><span class="sxs-lookup"><span data-stu-id="0a3b9-615">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="0a3b9-616">Новые командлеты:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="0a3b9-616">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="0a3b9-617">Добавлен параметр ProximityPlacementGroupId в следующие командлеты:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="0a3b9-617">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="0a3b9-618">Параметры DiskEncryptionSetId и EncryptionType добавлены в следующие командлеты:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="0a3b9-618">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="0a3b9-619">Добавлен параметр PublicIPAddressVersion в New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="0a3b9-619">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="0a3b9-620">FileUris для расширения пользовательских скриптов теперь будет защищенным, а не общедоступным параметром</span><span class="sxs-lookup"><span data-stu-id="0a3b9-620">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="0a3b9-621">Добавлено ScaleInPolicy в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0a3b9-621">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="0a3b9-622">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="0a3b9-622">Breaking changes</span></span>
    - <span data-ttu-id="0a3b9-623">Параметр UploadSizeInBytes применяется теперь вместо DiskSizeGB для New-AzDiskConfig, если CreateOption имеет значение Upload</span><span class="sxs-lookup"><span data-stu-id="0a3b9-623">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="0a3b9-624">PublishingProfile.Source.ManagedImage.Id заменяется на StorageProfile.Source.Id в объекте GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="0a3b9-624">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a3b9-625">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a3b9-625">Az.DataFactory</span></span>
* <span data-ttu-id="0a3b9-626">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.3.0.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-626">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0a3b9-627">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a3b9-627">Az.DataLakeStore</span></span>
* <span data-ttu-id="0a3b9-628">Обновлен пакет SDK для ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), включает следующие исправления</span><span class="sxs-lookup"><span data-stu-id="0a3b9-628">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="0a3b9-629">Не создается исключение при невозможности десериализовать значение времени создания для записи в корзине или каталоге.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-629">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="0a3b9-630">Предоставляется параметр для времени ожидания запроса в adlsclient</span><span class="sxs-lookup"><span data-stu-id="0a3b9-630">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="0a3b9-631">Исправлена передача исходного значения syncflag для восстановления badoffset</span><span class="sxs-lookup"><span data-stu-id="0a3b9-631">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="0a3b9-632">Исправлена операция EnumerateDirectory, чтобы она извлекала токен продолжения после проверки ответа</span><span class="sxs-lookup"><span data-stu-id="0a3b9-632">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="0a3b9-633">Исправлена ошибка объединения</span><span class="sxs-lookup"><span data-stu-id="0a3b9-633">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0a3b9-634">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0a3b9-634">Az.FrontDoor</span></span>
* <span data-ttu-id="0a3b9-635">Исправлены разные опечатки в разных частях модуля</span><span class="sxs-lookup"><span data-stu-id="0a3b9-635">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="0a3b9-636">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0a3b9-636">Az.HDInsight</span></span>
* <span data-ttu-id="0a3b9-637">Исправлена ошибка, из-за которой клиент получал сообщение об ошибке 'Not a valid Base-64 string' (Не является допустимой строкой Base64) при выполнении Get-AzHDInsightCluster для получения кластера с хранилищем ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-637">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="0a3b9-638">Добавлен параметр с именем ApplicationId в три командлета Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig и New-AzHDInsightCluster, чтобы клиент мог предоставить идентификатор приложения субъекта-службы для доступа к Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-638">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="0a3b9-639">Для Microsoft.Azure.Management.HDInsight изменена версия с 2.1.0 на 5.1.0</span><span class="sxs-lookup"><span data-stu-id="0a3b9-639">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="0a3b9-640">Удалены пять командлетов:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-640">Removed five cmdlets:</span></span>
    - <span data-ttu-id="0a3b9-641">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="0a3b9-641">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="0a3b9-642">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="0a3b9-642">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="0a3b9-643">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="0a3b9-643">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="0a3b9-644">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0a3b9-644">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="0a3b9-645">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0a3b9-645">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="0a3b9-646">Добавлены три командлета:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-646">Added three cmdlets:</span></span>
    - <span data-ttu-id="0a3b9-647">Get-AzHDInsightMonitoring заменяет собой Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-647">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="0a3b9-648">Enable-AzHDInsightMonitoring заменяет собой Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-648">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="0a3b9-649">Disable-AzHDInsightMonitoring заменяет собой Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-649">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="0a3b9-650">Исправлен командлет Get-AzHDInsightProperties, чтобы он поддерживал получение сведений о возможностях из определенного расположения.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-650">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="0a3b9-651">Удалены наборы параметров ("Spark1", "Spark2") из Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-651">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="0a3b9-652">Добавлены примеры в справочные документы по командлету Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-652">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="0a3b9-653">Изменен тип выходных данных для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-653">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="0a3b9-654">Для Get-AzHDInsightProperties тип выходных данных изменен с CapabilitiesResponse на AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-654">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="0a3b9-655">Для Remove-AzHDInsightCluster тип выходных данных изменен с ClusterGetResponse на bool.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-655">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="0a3b9-656">Для Set-AzHDInsightGatewaySettings тип выходных данных изменен с HttpConnectivitySettings на GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-656">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="0a3b9-657">Добавлены несколько условий для проверки сценариев.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-657">Added some scenario test cases.</span></span>
* <span data-ttu-id="0a3b9-658">Удалены несколько псевдонимов: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-658">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0a3b9-659">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0a3b9-659">Az.IotHub</span></span>
* <span data-ttu-id="0a3b9-660">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="0a3b9-660">Breaking changes:</span></span>
    - <span data-ttu-id="0a3b9-661">Командлет Add-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-661">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="0a3b9-662">Удален набор параметров __AllParameterSets для командлета Add-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-662">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="0a3b9-663">Командлет Get-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-663">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="0a3b9-664">Удален набор параметров __AllParameterSets для командлета Get-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-664">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="0a3b9-665">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-665">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="0a3b9-666">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-666">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="0a3b9-667">Командлет New-AzIotHubExportDevice больше не поддерживает псевдоним New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-667">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="0a3b9-668">Командлет New-AzIotHubImportDevice больше не поддерживает псевдоним New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-668">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="0a3b9-669">Командлет Remove-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-669">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="0a3b9-670">Удален набор параметров __AllParameterSets для командлета Remove-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-670">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="0a3b9-671">Командлет Set-AzIotHub теперь не поддерживает параметр OperationsMonitoringProperties и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-671">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="0a3b9-672">Удален набор параметров UpdateOperationsMonitoringProperties для командлета Set-AzIotHub.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-672">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a3b9-673">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a3b9-673">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a3b9-674">Azure Site Recovery поддерживает настройку сетевых ресурсов, например групп безопасности сети, общедоступных IP-адресов и внутренних подсистем балансировки нагрузки из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-674">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="0a3b9-675">Azure Site Recovery поддерживает запись на управляемый диск из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-675">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="0a3b9-676">Azure Site Recovery поддерживает сокращение NIC из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-676">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="0a3b9-677">Azure Site Recovery поддерживает ускорение сети NIC из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-677">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="0a3b9-678">Azure Site Recovery поддерживает автоматическое обновление агента из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-678">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="0a3b9-679">Azure Site Recovery поддерживает стандартный SSD-накопитель из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-679">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="0a3b9-680">Azure Site Recovery поддерживает двухпроходное шифрование диска Azure из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-680">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="0a3b9-681">Azure Site Recovery поддерживает новый добавленный диск из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-681">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="0a3b9-682">Добавлена функция SoftDelete для виртуальных машин и соответствующие тесты</span><span class="sxs-lookup"><span data-stu-id="0a3b9-682">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a3b9-683">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a3b9-683">Az.Resources</span></span>
* <span data-ttu-id="0a3b9-684">Обновлена сборка зависимостей Microsoft.Extensions.Caching.Memory с версии 1.1.1 до 2.2</span><span class="sxs-lookup"><span data-stu-id="0a3b9-684">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a3b9-685">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a3b9-685">Az.Network</span></span>
* <span data-ttu-id="0a3b9-686">Изменены все командлеты для PrivateEndpointConnection, чтобы они поддерживали универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-686">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="0a3b9-687">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-687">Updated cmdlet:</span></span>
        - <span data-ttu-id="0a3b9-688">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-688">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0a3b9-689">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-689">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0a3b9-690">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-690">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0a3b9-691">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-691">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0a3b9-692">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0a3b9-692">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="0a3b9-693">Добавлен новый командлет для PrivateLinkResource, который поддерживает универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-693">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="0a3b9-694">Новый командлет</span><span class="sxs-lookup"><span data-stu-id="0a3b9-694">New cmdlet:</span></span>
        - <span data-ttu-id="0a3b9-695">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="0a3b9-695">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="0a3b9-696">Добавлены новые поля и параметр для протокола прокси версии 2.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-696">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="0a3b9-697">Добавлено свойство EnableProxyProtocol в PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0a3b9-697">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="0a3b9-698">Добавлено свойство LinkIdentifier в PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0a3b9-698">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="0a3b9-699">Обновлен New-AzPrivateLinkService для поддержки нового необязательного параметра EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-699">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="0a3b9-700">Исправлено описание параметра в справочной документации по командлету New-AzApplicationGatewaySku.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-700">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="0a3b9-701">Новые командлеты для поддержки политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="0a3b9-701">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="0a3b9-702">Добавлена поддержка дочерних ресурсов RouteTables для VirtualHub</span><span class="sxs-lookup"><span data-stu-id="0a3b9-702">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="0a3b9-703">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-703">New cmdlets added:</span></span>
        - <span data-ttu-id="0a3b9-704">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="0a3b9-704">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="0a3b9-705">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="0a3b9-705">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="0a3b9-706">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="0a3b9-706">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="0a3b9-707">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="0a3b9-707">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="0a3b9-708">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="0a3b9-708">Set-AzVirtualHub</span></span>
* <span data-ttu-id="0a3b9-709">Добавлена поддержка новых свойств SKU для VirtualHub и VirtualWANType в VirtualWan</span><span class="sxs-lookup"><span data-stu-id="0a3b9-709">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="0a3b9-710">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-710">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="0a3b9-711">New-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="0a3b9-711">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="0a3b9-712">Update-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="0a3b9-712">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="0a3b9-713">New-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="0a3b9-713">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="0a3b9-714">Update-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="0a3b9-714">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="0a3b9-715">Добавлена поддержка свойства EnableInternetSecurity для HubVnetConnection, VpnConnection и ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="0a3b9-715">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="0a3b9-716">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-716">New cmdlets added:</span></span>
        - <span data-ttu-id="0a3b9-717">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="0a3b9-717">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="0a3b9-718">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-718">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="0a3b9-719">New-AzureRmVirtualHubVnetConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="0a3b9-719">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="0a3b9-720">New-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="0a3b9-720">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="0a3b9-721">Update-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="0a3b9-721">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="0a3b9-722">New-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="0a3b9-722">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="0a3b9-723">Set-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="0a3b9-723">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="0a3b9-724">Добавлена поддержка настройки политики верхнего уровня WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="0a3b9-724">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="0a3b9-725">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-725">New cmdlets added:</span></span>
        - <span data-ttu-id="0a3b9-726">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="0a3b9-726">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="0a3b9-727">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="0a3b9-727">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="0a3b9-728">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="0a3b9-728">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="0a3b9-729">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="0a3b9-729">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="0a3b9-730">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="0a3b9-730">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="0a3b9-731">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="0a3b9-731">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="0a3b9-732">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-732">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="0a3b9-733">New-AzApplicationGatewayFirewallPolicy: добавлены параметры PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="0a3b9-733">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="0a3b9-734">Добавлена поддержка оператора Geo-Match для CustomRule</span><span class="sxs-lookup"><span data-stu-id="0a3b9-734">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="0a3b9-735">Добавлен параметр GeoMatch в оператор для FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="0a3b9-735">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="0a3b9-736">Добавлена поддержка политики брандмауэра perListener и perSite</span><span class="sxs-lookup"><span data-stu-id="0a3b9-736">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="0a3b9-737">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-737">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="0a3b9-738">New-AzApplicationGatewayHttpListener: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="0a3b9-738">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="0a3b9-739">New-AzApplicationGatewayPathRuleConfig: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="0a3b9-739">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="0a3b9-740">Исправлен учет регистра для требуемой подсети с именем AzureBastionSubnet в PSBastion</span><span class="sxs-lookup"><span data-stu-id="0a3b9-740">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="0a3b9-741">Поддержка полного доменного имени назначения в правилах сети и преобразованного полного доменного имени в правилах NAT для брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="0a3b9-741">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="0a3b9-742">Добавлена поддержка ресурсов верхнего уровня RouteTables для IpGroup</span><span class="sxs-lookup"><span data-stu-id="0a3b9-742">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="0a3b9-743">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-743">New cmdlets added:</span></span>
        - <span data-ttu-id="0a3b9-744">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="0a3b9-744">New-AzIpGroup</span></span>
        - <span data-ttu-id="0a3b9-745">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="0a3b9-745">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="0a3b9-746">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="0a3b9-746">Get-AzIpGroup</span></span>
        - <span data-ttu-id="0a3b9-747">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="0a3b9-747">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0a3b9-748">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0a3b9-748">Az.ServiceFabric</span></span>
* <span data-ttu-id="0a3b9-749">Удален командлет Add-AzServiceFabricApplicationCertificate, так как соответствующий сценарий выполняется командлетом Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-749">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a3b9-750">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a3b9-750">Az.Sql</span></span>
* <span data-ttu-id="0a3b9-751">Добавлена поддержка восстановления удаленных баз данных в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-751">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="0a3b9-752">Из кода удалены старые командлеты аудита.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-752">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="0a3b9-753">Удалены нерекомендуемые псевдонимы:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-753">Removed deprecated aliases:</span></span>
* <span data-ttu-id="0a3b9-754">Get-AzSqlDatabaseIndexRecommendations (вместо него используйте Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="0a3b9-754">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="0a3b9-755">Get-AzSqlDatabaseRestorePoints (вместо него используйте Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="0a3b9-755">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="0a3b9-756">Удален командлет Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0a3b9-756">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="0a3b9-757">Удалены псевдонимы для нерекомендуемых командлетов параметров оценки уязвимостей</span><span class="sxs-lookup"><span data-stu-id="0a3b9-757">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="0a3b9-758">Командлеты расширенного обнаружения угроз объявлены устаревшими</span><span class="sxs-lookup"><span data-stu-id="0a3b9-758">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="0a3b9-759">Добавлены командлеты для отключения и включения рекомендаций о конфиденциальности для столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-759">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a3b9-760">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a3b9-760">Az.Storage</span></span>
* <span data-ttu-id="0a3b9-761">Поддержка включения большой общей папки при создании или обновлении учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="0a3b9-761">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="0a3b9-762">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a3b9-762">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="0a3b9-763">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a3b9-763">Set-AzStorageAccount</span></span>
* <span data-ttu-id="0a3b9-764">При закрытии или получении маркера файла пропускается проверка того, является ли входной путь файлом или каталогом, чтобы избежать сбоев при получении объектов в состоянии DeletePending.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-764">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="0a3b9-765">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="0a3b9-765">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="0a3b9-766">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="0a3b9-766">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="0a3b9-767">2.8.0 — октябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-767">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="0a3b9-768">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="0a3b9-768">General</span></span>
* <span data-ttu-id="0a3b9-769">Выпуск Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="0a3b9-769">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0a3b9-770">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a3b9-770">Az.Accounts</span></span>
* <span data-ttu-id="0a3b9-771">Обновление телеметрии и перезаписи URL-адресов для созданных модулей, исправление для модульных тестов Windows.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-771">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="0a3b9-772">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a3b9-772">Az.ApiManagement</span></span>
* <span data-ttu-id="0a3b9-773">**Set-AzApiManagementApi**  — в ApiVersionSet добавлена поддержка обновления API.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-773">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="0a3b9-774">исправлена проблема https://github.com/Azure/azure-powershell/issues/10068.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-774">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0a3b9-775">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0a3b9-775">Az.Automation</span></span>
* <span data-ttu-id="0a3b9-776">Исправлен командлет New-AzureAutomationSoftwareUpdateConfiguration для параметра перезагрузки Linux.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-776">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="0a3b9-777">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0a3b9-777">Az.Batch</span></span>
* <span data-ttu-id="0a3b9-778">Командлет **Get-AzBatchNodeAgentSku** объявлен устаревшим и будет заменен на **Get-AzBatchSupportImage** в версии 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-778">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a3b9-779">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a3b9-779">Az.Compute</span></span>
* <span data-ttu-id="0a3b9-780">В командлеты New-AzVM и New-AzVmss добавлены параметры Priority, EvictionPolicy и MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-780">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="0a3b9-781">Исправлены предупреждающее сообщение для командлетов Add-AzVMAdditionalUnattendContent и Add-AzVMSshPublicKey и справочная документация по ним.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-781">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="0a3b9-782">Для Set-AzVMDiskEncryptionExtension исправлено исключение -skipVmBackup для виртуальных машин Linux с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-782">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="0a3b9-783">Исправлена ошибка при изменении параметров шифрования в Set-AzVMDiskEncryptionExtension, реализован двухэтапный сценарий.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-783">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a3b9-784">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a3b9-784">Az.DataFactory</span></span>
* <span data-ttu-id="0a3b9-785">Добавлены команды CRUD для потока данных Фабрики данных Azure версии 2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow и Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-785">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="0a3b9-786">Добавлены команды действий для сеанса отладки потока данных Фабрики данных Azure версии 2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand и Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-786">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="0a3b9-787">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.2.0.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-787">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0a3b9-788">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a3b9-788">Az.DataLakeStore</span></span>
* <span data-ttu-id="0a3b9-789">Проверка учетной записи исправлена так, чтобы учетные записи, содержащие знак "-", можно было передавать без домена.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-789">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="0a3b9-790">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="0a3b9-790">Az.HealthcareApis</span></span>
* <span data-ttu-id="0a3b9-791">Версия PowerShell обновлена до 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-791">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="0a3b9-792">Версия пакета SDK обновлена до 1.0.2.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-792">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="0a3b9-793">В тестах обновлены ссылки на новую версию пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-793">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="0a3b9-794">Вложенная выходная структура заменена на плоскую.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-794">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0a3b9-795">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0a3b9-795">Az.IotHub</span></span>
* <span data-ttu-id="0a3b9-796">Добавлен новый источник маршрутизации DigitalTwinChangeEvents.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-796">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="0a3b9-797">Исправлены незначительные ошибки: Get-AzIothub не возвращает subscriptionId.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-797">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0a3b9-798">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0a3b9-798">Az.Monitor</span></span>
* <span data-ttu-id="0a3b9-799">Добавлены новые получатели групп действий: -ItsmReceiver, -VoiceReceiver, -ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-799">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="0a3b9-800">Для получателей включите общую схему оповещений.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-800">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="0a3b9-801">Это не касается получателей SMS, push-уведомлений приложения Azure, ITSM и голосовых сообщений.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-801">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="0a3b9-802">Веб-перехватчики теперь поддерживают аутентификацию Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-802">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a3b9-803">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a3b9-803">Az.Network</span></span>
* <span data-ttu-id="0a3b9-804">Добавлен новый командлет Get-AzAvailableServiceAlias, позволяющий получить псевдонимы для политик конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-804">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="0a3b9-805">В подключениях шлюза виртуальной сети появилась возможность добавлять селекторы трафика.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-805">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="0a3b9-806">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-806">New cmdlets added:</span></span>
        - <span data-ttu-id="0a3b9-807">New-AzureRmTrafficSelectorPolicy.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-807">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="0a3b9-808">В командлеты добавлены необязательные параметры -TrafficSelectorPolicies, -New-AzureRmVirtualNetworkGatewayConnection, -Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-808">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="0a3b9-809">В конфигурациях правил сетевой безопасности добавлена поддержка протоколов ESP и AH.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-809">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="0a3b9-810">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-810">Updated cmdlets:</span></span>
        - <span data-ttu-id="0a3b9-811">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-811">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="0a3b9-812">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-812">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="0a3b9-813">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-813">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="0a3b9-814">Улучшена обработка исключений в командлетах Cortex.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-814">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="0a3b9-815">Выпущены новые поколения и номера SKU VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-815">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="0a3b9-816">Представлены новые поколения VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-816">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="0a3b9-817">Представлены новые номера SKU VirtualNetworkGateways с высокой пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-817">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="0a3b9-818">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0a3b9-818">Az.RedisCache</span></span>
* <span data-ttu-id="0a3b9-819">В справочную документацию по Set-AzRedisCache добавлены недостающие значения для параметра -Size.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-819">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a3b9-820">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a3b9-820">Az.Sql</span></span>
* <span data-ttu-id="0a3b9-821">Добавлена возможность назначать администратора Active Directory в Управляемом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-821">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a3b9-822">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a3b9-822">Az.Storage</span></span>
* <span data-ttu-id="0a3b9-823">Клиентская библиотека службы хранилища Azure обновлена до версии 11.1.0.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-823">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="0a3b9-824">NextPageLink теперь позволяет получить список контейнеров с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-824">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="0a3b9-825">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0a3b9-825">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="0a3b9-826">NextPageLink теперь позволяет получить список учетных записей хранения из подписки.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-826">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="0a3b9-827">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a3b9-827">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="0a3b9-828">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="0a3b9-828">Az.StorageSync</span></span>
* <span data-ttu-id="0a3b9-829">Исправлена проблема 9810 с Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-829">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a3b9-830">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a3b9-830">Az.Websites</span></span>
* <span data-ttu-id="0a3b9-831">Обновление плана службы приложений с помощью Set-AzWebApp приводило к сбою приложения.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-831">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="0a3b9-832">2.7.0 — сентябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-832">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="0a3b9-833">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a3b9-833">Az.ApiManagement</span></span>
* <span data-ttu-id="0a3b9-834">В справочной документации по командлету Set-AzApiManagementPolicy обновлено описание параметра -Format.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-834">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="0a3b9-835">Из справочной документации удалены ссылки на нерекомендуемый командлет Update-AzApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-835">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="0a3b9-836">Вместо него следует использовать командлет Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-836">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0a3b9-837">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0a3b9-837">Az.Automation</span></span>
* <span data-ttu-id="0a3b9-838">В справочной документации по командлету Register-AzAutomationDscNode исправлена опечатка в примере.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-838">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="0a3b9-839">Добавлено уточнение об ограничениях ОС для командлета Register-AzAutomationDSCNode.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-839">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="0a3b9-840">Исправлено исключение пустой ссылки для параметра -Wait в командлете Start-AzAutomationRunbook.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-840">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a3b9-841">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a3b9-841">Az.Compute</span></span>
* <span data-ttu-id="0a3b9-842">Добавлен параметр UploadSizeInBytes для командлета New-AzDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-842">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="0a3b9-843">Добавлен добавочный параметр для командлета New-AzSnapshotConfig.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-843">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="0a3b9-844">Для виртуальной машины добавлены такие функции с низким приоритетом:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-844">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="0a3b9-845">Для командлета New-AzVMConfig добавлены параметры MaxPrice, EvictionPolicy и Priority.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-845">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="0a3b9-846">Для командлетов New-AzVmssConfig, Update-AzVM и Update-AzVmss добавлен параметр MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-846">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="0a3b9-847">Для командлета Get-AzAvailabilitySet устранена проблема со ссылкой на виртуальную машину, когда в нем перечисляются все группы доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-847">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="0a3b9-848">Исправлено исключение NULL для командлета Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-848">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="0a3b9-849">Исправлен метод поиска VHD для относительной конечной позиции.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-849">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="0a3b9-850">Устранена проблема с UltraSSD для командлетов New-AzVM и Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-850">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a3b9-851">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a3b9-851">Az.DataFactory</span></span>
* <span data-ttu-id="0a3b9-852">Добавлены 3 новые команды для ADF версии 2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription и Get-AzDataFactoryV2TriggerSubscriptionStatus.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-852">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="0a3b9-853">Пакет SDK ADF для .NET обновлен до версии 4.1.3.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-853">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="0a3b9-854">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0a3b9-854">Az.HDInsight</span></span>
* <span data-ttu-id="0a3b9-855">Укажите критические изменения.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-855">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0a3b9-856">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0a3b9-856">Az.IotHub</span></span>
* <span data-ttu-id="0a3b9-857">Добавлена поддержка для вызова отработки отказа для IotHub в георегион аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-857">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="0a3b9-858">Добавлена поддержка для управления обогащением сообщений для IotHub.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-858">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="0a3b9-859">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-859">New cmdlets are:</span></span>
    - <span data-ttu-id="0a3b9-860">Add-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-860">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="0a3b9-861">Get-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-861">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="0a3b9-862">Remove-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-862">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="0a3b9-863">Set-AzIotHubMessageEnrichment.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-863">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0a3b9-864">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0a3b9-864">Az.Monitor</span></span>
* <span data-ttu-id="0a3b9-865">Указание на самую последнюю версию пакета SDK для монитора, т. е. 0.24.1-preview:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-865">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="0a3b9-866">В командлеты метрик добавлены некритические изменения, т. е. перечисление единиц поддерживает несколько новых значений.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-866">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="0a3b9-867">Эти командлеты доступны только для чтения, поэтому входные данные командлетов не будут изменены.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-867">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="0a3b9-868">Актуальная версия API запросов **ActionGroups**  — **2019-06-01**. До этого была версия **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-868">The api-version of the **ActionGroups** requests is now **2019-06-01** , before it was **2018-03-01**.</span></span> <span data-ttu-id="0a3b9-869">Тесты сценария обновлены в соответствии с этим изменением.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-869">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="0a3b9-870">В конструкторы классов **EmailReceiver** и **WebhookReceiver** добавлен один новый обязательный аргумент — логическое значение с именем **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-870">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="0a3b9-871">Сейчас для него установлено значение **false** , чтобы скрыть это критическое изменение от командлетов.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-871">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="0a3b9-872">**Примечание**. Это временное изменение, которое должно быть подтверждено командой оповещения.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-872">**NOTE** : this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="0a3b9-873">Порядок аргументов для конструктора класса **Source** (связанного с классом **ScheduledQueryRuleSource** ) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-873">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="0a3b9-874">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-874">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="0a3b9-875">Порядок аргументов для конструктора класса **AlertingAction** (связанного с классом **ScheduledQueryRuleSource** ) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-875">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="0a3b9-876">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-876">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="0a3b9-877">Добавлена поддержка критериев динамического порога для оповещения метрики версии 2:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-877">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="0a3b9-878">New-AzMetricAlertRuleV2Criteria: теперь также позволяет создавать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-878">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="0a3b9-879">Add-AzMetricAlertRuleV2: теперь также позволяет принимать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-879">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="0a3b9-880">Добавлены усовершенствования в командлетах запланированных правил запросов (SQR).</span><span class="sxs-lookup"><span data-stu-id="0a3b9-880">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="0a3b9-881">Командлеты будут принимать параметр Location в обоих форматах: расположение (например, eastus) или отображаемое имя расположения (например, "восточная часть США").</span><span class="sxs-lookup"><span data-stu-id="0a3b9-881">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="0a3b9-882">Параметр Enabled проиллюстрирован в файлах справки надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-882">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="0a3b9-883">Добавлены примеры для необязательного параметра ActionGroup.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-883">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="0a3b9-884">Все файлы справки улучшены.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-884">Overall improved help files</span></span>
* <span data-ttu-id="0a3b9-885">Исправлена ошибка в определении типа области для командлета Set-AzActionRule.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-885">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a3b9-886">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a3b9-886">Az.Network</span></span>
* <span data-ttu-id="0a3b9-887">Исправлен неправильный пример в справочной документации по командлету New-AzApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-887">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="0a3b9-888">В справочную документацию по командлету Get-AzNetworkWatcherPacketCapture добавлено примечание, посвященное извлечению всех свойств для записи пакетов.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-888">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="0a3b9-889">В справочной документации по командлету Test-AzNetworkWatcherIPFlow исправлен пример: теперь он правильно перечисляет сетевые карты.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-889">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="0a3b9-890">Улучшен анализ облачных исключений для отображения дополнительных сведений (при их наличии).</span><span class="sxs-lookup"><span data-stu-id="0a3b9-890">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="0a3b9-891">Улучшен анализ облачных исключений для обработки дополнительного типа исключения SDK.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-891">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="0a3b9-892">Исправлено неправильное сопоставление моделей правил безопасности.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-892">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="0a3b9-893">Добавлены свойства сетевого интерфейса для компонента частного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-893">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="0a3b9-894">Для интерфейса PSNetworkInterface добавлено свойство PrivateEndpoint с типом PSResourceId.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-894">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="0a3b9-895">В PSNetworkInterfaceIPConfiguration добавлено свойство PrivateLinkConnectionProperties с типом PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-895">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="0a3b9-896">Добавлен новый класс модели: PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-896">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="0a3b9-897">Добавлен новый тип ApplicationRuleProtocolType "mssql" для ресурса Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-897">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="0a3b9-898">Поддержка многоканального подключения в Виртуальной глобальной сети:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-898">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="0a3b9-899">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="0a3b9-899">New cmdlets</span></span>
        - <span data-ttu-id="0a3b9-900">New-AzVpnSiteLink;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-900">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="0a3b9-901">New-AzVpnSiteLinkConnection;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-901">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="0a3b9-902">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-902">Updated cmdlet:</span></span>
        - <span data-ttu-id="0a3b9-903">New-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-903">New-VpnSite</span></span>
        - <span data-ttu-id="0a3b9-904">Update-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-904">Update-VpnSite</span></span>
        - <span data-ttu-id="0a3b9-905">New-VpnConnection;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-905">New-VpnConnection</span></span>
        - <span data-ttu-id="0a3b9-906">Update-VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-906">Update-VpnConnection</span></span>
* <span data-ttu-id="0a3b9-907">Исправлены документы с некоторыми примерами PowerShell для использования командлетов AZ вместо командлетов AzureRM.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-907">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a3b9-908">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a3b9-908">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a3b9-909">Для объекта AzureVMpolicy добавлен новый атрибут — ProtectedItemsCount.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-909">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="0a3b9-910">Добавлены тесты для политики виртуальной машины и восстановления исходной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-910">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a3b9-911">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a3b9-911">Az.Resources</span></span>
* <span data-ttu-id="0a3b9-912">Исправлена ошибка, при которой не удавалось вызвать командлет New-AzRoleAssignment без параметра Scope.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-912">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0a3b9-913">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0a3b9-913">Az.ServiceFabric</span></span>
* <span data-ttu-id="0a3b9-914">Исправлена опечатка в примере в справочной документации по командлету Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-914">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="0a3b9-915">Добавлены новые командлеты для управления приложениями и службами:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-915">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="0a3b9-916">New-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-916">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="0a3b9-917">New-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-917">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="0a3b9-918">New-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-918">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="0a3b9-919">New-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-919">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="0a3b9-920">Update-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-920">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="0a3b9-921">Get-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-921">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="0a3b9-922">Get-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-922">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="0a3b9-923">Get-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-923">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="0a3b9-924">Get-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-924">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="0a3b9-925">Remove-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-925">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="0a3b9-926">Remove-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-926">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="0a3b9-927">Remove-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-927">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="0a3b9-928">Remove-AzServiceFabricServic.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-928">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="0a3b9-929">Пакет SDK для Service Fabric обновлен до версии 1.2.0, в которой используется версия API 2019-03-01 поставщика ресурсов Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-929">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="0a3b9-930">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="0a3b9-930">Az.SignalR</span></span>
* <span data-ttu-id="0a3b9-931">Добавлены командлеты Update, Restart, CheckNameAvailability и GetUsage.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-931">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a3b9-932">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a3b9-932">Az.Sql</span></span>
* <span data-ttu-id="0a3b9-933">Обновлен пример в справочной документации по командлету Get-AzSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-933">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="0a3b9-934">Добавлен пример виртуального ядра для командлета создания эластичного пула (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="0a3b9-934">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="0a3b9-935">Удалена проверка свойства EmailAddresses и того, что свойство EmailAdmins правильное в случае, если свойство EmailAddresses пустое в командлетах Set-AzSqlServerAdvancedThreatProtectionPolicy и Set-AzSqlDatabaseAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-935">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="0a3b9-936">Теперь, если существует несколько параметров диагностики, включающих категорию аудита, параметры аудита сервера и базы данных удаляются.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-936">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="0a3b9-937">Исправлена проверка адресов электронной почты в нескольких командлетах оценки уязвимостей SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting и Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="0a3b9-937">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a3b9-938">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a3b9-938">Az.Storage</span></span>
* <span data-ttu-id="0a3b9-939">Обновлен пример в справочной документации по командлету Get-AzStorageAccountKey.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-939">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="0a3b9-940">Теперь при отправке и загрузке файла Azure в конечном файле сохраняются свойства SMB исходного файла (атрибуты файла, время создания файла, время последней записи файла).</span><span class="sxs-lookup"><span data-stu-id="0a3b9-940">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="0a3b9-941">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0a3b9-941">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="0a3b9-942">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0a3b9-942">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="0a3b9-943">Исправлена операция отправки блочного BLOB-объекта, в которой происходили сбои свойств и метаданных в контейнере с включенной ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-943">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="0a3b9-944">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0a3b9-944">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="0a3b9-945">Добавлена поддержка управления общими папками Azure в API плоскости управления с помощью таких командлетов:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-945">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="0a3b9-946">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-946">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="0a3b9-947">Get-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-947">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="0a3b9-948">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-948">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="0a3b9-949">Remove-AzRmStorageShare.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-949">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a3b9-950">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a3b9-950">Az.Websites</span></span>
* <span data-ttu-id="0a3b9-951">Устранена проблема, из-за которой теги webapp удалялись при переносе приложения в новый ASP.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-951">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="0a3b9-952">Теперь командлет Publish-AzureWebapp работает в Linux и Windows.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-952">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="0a3b9-953">Обновлен пример в справочной документации по командлету Get-AzWebAppPublishingProfile.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-953">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="0a3b9-954">2.6.0 — август 2019 г.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-954">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="0a3b9-955">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="0a3b9-955">General</span></span>
* <span data-ttu-id="0a3b9-956">Исправлены опечатки в модулях.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-956">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0a3b9-957">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a3b9-957">Az.Accounts</span></span>
* <span data-ttu-id="0a3b9-958">Добавлена поддержка назначаемого пользователем удостоверения MSI при проверке подлинности в Функциях Azure (№ 9479).</span><span class="sxs-lookup"><span data-stu-id="0a3b9-958">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="0a3b9-959">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="0a3b9-959">Az.Aks</span></span>
* <span data-ttu-id="0a3b9-960">Устранена проблема с выходными данными для Get-AzAks.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-960">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="0a3b9-961">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9847.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-961">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="0a3b9-962">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a3b9-962">Az.ApiManagement</span></span>
* <span data-ttu-id="0a3b9-963">исправлена проблема https://github.com/Azure/azure-powershell/issues/9351.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-963">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="0a3b9-964">Обновлена версия NuGet для .NET, которая не накладывает ограничений на productId, apiId, groupId и userId.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-964">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="0a3b9-965">**Get-AzApiManagementProduct**. Добавлена поддержка запросов к продуктам с помощью API.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-965">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="0a3b9-966">**New-AzApiManagementApiRevision**. Устранена проблема, из-за которой не задавался параметр ApiRevisionDescription при создании новой редакции API https://github.com/Azure/azure-powershell/issues/9752.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-966">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="0a3b9-967">Исправлено написание имени модели c PsApiManagementOAuth2AuthrozationServer на PsApiManagementOAuth2AuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-967">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="0a3b9-968">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0a3b9-968">Az.Batch</span></span>
* <span data-ttu-id="0a3b9-969">Исправлена опечатка в написании Windows со строчной буквы в справочных сообщениях и документации.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-969">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0a3b9-970">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0a3b9-970">Az.Cdn</span></span>
* <span data-ttu-id="0a3b9-971">Исправлена опечатка во вспомогательном приложении модуля CDN.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-971">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a3b9-972">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a3b9-972">Az.Compute</span></span>
* <span data-ttu-id="0a3b9-973">Добавлен параметр VmssId в новый командлет Add New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-973">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="0a3b9-974">Добавлены параметры TerminateScheduledEvents и TerminateScheduledEventNotBeforeTimeoutInMinutes в New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-974">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="0a3b9-975">Добавлено свойство HyperVGeneration в объект образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-975">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="0a3b9-976">Добавлены компоненты Host и HostGroup.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-976">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="0a3b9-977">Новые командлеты:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="0a3b9-977">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="0a3b9-978">Параметр HostId добавлен в New-AzVMConfig и New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-978">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="0a3b9-979">Исправлен пример в документации по Invoke-AzVMRunCommand, в котором теперь используется правильное имя параметра.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-979">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="0a3b9-980">Исправлено описание VolumeType в справочной документации по Set-AzVMDiskEncryptionExtension и Set-AzVmssDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-980">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a3b9-981">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a3b9-981">Az.DataFactory</span></span>
* <span data-ttu-id="0a3b9-982">Исправлена опечатка в написании Windows со строчной буквы в документации по New-AzDataFactoryEncryptValue.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-982">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="0a3b9-983">Пакет SDK ADF для .NET обновлен до версии 4.1.2.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-983">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="0a3b9-984">Добавлены параметры DataProxyIntegrationRuntimeName, DataProxyStagingLinkedServiceName и DataProxyStagingPath в командлет Set-AzureRmDataFactoryV2IntegrationRuntime, что позволяет настраивать локальную среду выполнения интеграции в качестве прокси-сервера для Azure-SSIS Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-984">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="0a3b9-985">Обновлены PSTriggerRun для отображения активированных конвейеров, сообщений и свойств и PSActivityRun для отображения типа действия.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-985">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0a3b9-986">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a3b9-986">Az.DataLakeStore</span></span>
* <span data-ttu-id="0a3b9-987">Устранена проблема, при которой Get-DataLakeStoreDeletedItem переставал отвечать на запросы при возникновении ошибок или удаленных исключений.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-987">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0a3b9-988">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0a3b9-988">Az.EventHub</span></span>
* <span data-ttu-id="0a3b9-989">Исправлена проблема № 9658: опечатка в написании параметра VirtualNteworkRule у Set-AzEventHubNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-989">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="0a3b9-990">Исправлена проблема № 9558: в Set-AzEventHubNamespace используется PATCH вместо PUT.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-990">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="0a3b9-991">В командлет Set-AzEventHubNamespace добавлен параметр EnableKafka.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-991">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="0a3b9-992">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-992">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="0a3b9-993">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="0a3b9-993">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="0a3b9-994">Исправлено написание Azure со строчной буквы.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-994">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0a3b9-995">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0a3b9-995">Az.Monitor</span></span>
* <span data-ttu-id="0a3b9-996">Исправлены неправильные имена параметров в справочной документации.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-996">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a3b9-997">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a3b9-997">Az.Network</span></span>
* <span data-ttu-id="0a3b9-998">Обновлен New-AzPrivateLinkServiceIpConfig.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-998">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="0a3b9-999">Параметр PublicIpAddress объявлен нерекомендуемым, так как он не используется на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-999">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="0a3b9-1000">Добавлен необязательный параметр Primary, указывающий, является ли текущая IP-конфигурация основной.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1000">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="0a3b9-1001">Улучшена обработка исключений из-за ошибок запроса от пакета SDK. Устранена проблема, при которой исключения пакета SDK не обрабатывались правильно, из-за чего не отображались основные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1001">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="0a3b9-1002">Настроена логика проверки для префикса IPv6 IP-адреса для проверки правильности длины префикса IPv6.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1002">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="0a3b9-1003">Обновлен Get-AzVirtualNetworkSubnetConfig: добавлен набор параметров для получения по идентификатору ресурса подсети.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1003">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="0a3b9-1004">Обновлено описание параметра Location для AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1004">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0a3b9-1005">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1005">Az.OperationalInsights</span></span>
* <span data-ttu-id="0a3b9-1006">Обновлена документация по New-AzOperationalInsightsLinuxSyslogDataSource.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1006">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="0a3b9-1007">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1007">Added example</span></span>
    - <span data-ttu-id="0a3b9-1008">Обновлено описание параметра -Name.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1008">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="0a3b9-1009">Добавлен пример для New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1009">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="0a3b9-1010">Изменено описание параметра -Name для New-AzOperationalInsightsWindowsEventDataSource.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1010">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a3b9-1011">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1011">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a3b9-1012">Обновлен Get-AzRecoveryServicesBackupJobDetail.md.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1012">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a3b9-1013">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1013">Az.Resources</span></span>
* <span data-ttu-id="0a3b9-1014">Добавлена поддержка новой версии API 2019-05-10 для Microsoft.Resource.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1014">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="0a3b9-1015">Добавлена поддержка copy.count = 0 для переменных, ресурсов и свойств.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1015">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="0a3b9-1016">Ресурсы, у которых condition = false или copy.count = 0, будут удаляться в полном режиме.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1016">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="0a3b9-1017">В справочную документацию добавлен пример назначения политики на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1017">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0a3b9-1018">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1018">Az.ServiceBus</span></span>
* <span data-ttu-id="0a3b9-1019">Исправлена проблема № 9658: опечатка в написании параметра VirtualNetworkRule В Set-AzServiceBusNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1019">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="0a3b9-1020">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1020">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="0a3b9-1021">Добавлена новая команда Test-AzServiceBusNameAvailability для проверки доступности имени для очереди и раздела.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1021">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0a3b9-1022">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1022">Az.ServiceFabric</span></span>
* <span data-ttu-id="0a3b9-1023">Устранены ошибки командлета для добавления типа узла:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1023">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="0a3b9-1024">ошибка NullReferenceException, возникавшая, если у группы ресурсов были другие VMSS, не связанные с кластером Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1024">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="0a3b9-1025">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8681.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1025">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="0a3b9-1026">Исправлена ошибка, из-за которой командлет завершился сбоем, если virtualNetwork находилась не в той группе ресурсов, к которой относится кластер.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1026">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="0a3b9-1027">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8407.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1027">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="0a3b9-1028">Командлет Add-AzServiceFabricApplicationCertificate объявлен нерекомендуемым.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1028">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a3b9-1029">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1029">Az.Sql</span></span>
* <span data-ttu-id="0a3b9-1030">Обновление документации по старым командлетам аудита.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1030">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a3b9-1031">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1031">Az.Storage</span></span>
* <span data-ttu-id="0a3b9-1032">Обновлена справка по Get/Close-AzStorageFileHandle: в примеры добавлены сценарии использования командлетов и обновлено описание параметров.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1032">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="0a3b9-1033">Добавлена поддержка StandardBlobTier в операции отправки BLOB-объекта и копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1033">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="0a3b9-1034">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1034">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="0a3b9-1035">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1035">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="0a3b9-1036">Добавлена поддержка приоритета восстановления в операцию копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1036">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="0a3b9-1037">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1037">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a3b9-1038">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1038">Az.Websites</span></span>
* <span data-ttu-id="0a3b9-1039">Добавлены уточнение для параметра -AppSettings в Set-AzWebApp и Set-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1039">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="0a3b9-1040">2.5.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1040">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0a3b9-1041">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1041">Az.Accounts</span></span>
* <span data-ttu-id="0a3b9-1042">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1042">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="0a3b9-1043">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1043">Az.ApplicationInsights</span></span>
* <span data-ttu-id="0a3b9-1044">Исправлена опечатка в примере в документации по Remove-AzApplicationInsightsApiKey.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1044">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0a3b9-1045">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1045">Az.Automation</span></span>
* <span data-ttu-id="0a3b9-1046">Исправлена опечатка в строке ресурса.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1046">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0a3b9-1047">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1047">Az.CognitiveServices</span></span>
* <span data-ttu-id="0a3b9-1048">Добавлена поддержка NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1048">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a3b9-1049">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1049">Az.Compute</span></span>
* <span data-ttu-id="0a3b9-1050">Добавлены недостающие свойства (ComputerName, OsName, OsVersion и HyperVGeneration) для объекта представления экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1050">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="0a3b9-1051">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1051">Az.ContainerRegistry</span></span>
* <span data-ttu-id="0a3b9-1052">Исправлена опечатка в Remove-AzContainerRegistryReplication для параметра репликации.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1052">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="0a3b9-1053">См. подробнее: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1053">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a3b9-1054">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1054">Az.DataFactory</span></span>
* <span data-ttu-id="0a3b9-1055">Пакет SDK для ADF .NET обновлен до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1055">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="0a3b9-1056">Исправлена опечатка в документации по Get-AzDataFactoryV2PipelineRun.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1056">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0a3b9-1057">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1057">Az.EventHub</span></span>
* <span data-ttu-id="0a3b9-1058">Добавлен новый командлет для создания маркера SAS: New-AzEventHubAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1058">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="0a3b9-1059">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1059">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0a3b9-1060">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1060">Az.KeyVault</span></span>
* <span data-ttu-id="0a3b9-1061">Добавлена поддержка для настройки параметра KeySize в политиках сертификатов.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1061">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0a3b9-1062">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1062">Az.LogicApp</span></span>
* <span data-ttu-id="0a3b9-1063">Get-AzIntegrationAccountMap теперь надлежащим образом выводит все типы сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1063">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="0a3b9-1064">Добавлен новый параметр MapType для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1064">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="0a3b9-1065">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1065">Az.ManagedServices</span></span>
* <span data-ttu-id="0a3b9-1066">Добавлена поддержка API версии 2019-06-01 (общедоступная).</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1066">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a3b9-1067">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1067">Az.Network</span></span>
* <span data-ttu-id="0a3b9-1068">Добавлена поддержка частной конечной точки и службы приватного канала.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1068">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="0a3b9-1069">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1069">New cmdlets</span></span>
        - <span data-ttu-id="0a3b9-1070">Set-AzPrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1070">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="0a3b9-1071">Set-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1071">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="0a3b9-1072">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1072">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0a3b9-1073">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1073">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0a3b9-1074">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1074">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0a3b9-1075">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1075">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0a3b9-1076">Test-AzPrivateLinkServiceVisibility.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1076">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="0a3b9-1077">Get-AzAutoApprovedPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1077">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="0a3b9-1078">Обновлены следующие команды для функции: Флаг PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies в подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1078">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="0a3b9-1079">Обновлены командлеты New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1079">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="0a3b9-1080">Добавлен необязательный параметр -PrivateEndpointNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к частной конечной точке в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1080">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="0a3b9-1081">Добавлен необязательный параметр -PrivateLinkServiceNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к службе приватного канала в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1081">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="0a3b9-1082">Параметр ServiceName командлета AzPrivateLinkService был переименован на Name с псевдонимом ServiceName для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1082">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="0a3b9-1083">Включен протокол ICMP для настройки правил безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1083">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="0a3b9-1084">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1084">Updated cmdlets</span></span>
        - <span data-ttu-id="0a3b9-1085">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1085">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="0a3b9-1086">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1086">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="0a3b9-1087">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1087">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="0a3b9-1088">Добавлен ConnectionProtocolType (Ikev1/Ikev2) в качестве настраиваемого параметра для командлета New-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1088">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="0a3b9-1089">Добавлен PrivateIpAddressVersion в LoadBalancerFrontendIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1089">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="0a3b9-1090">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1090">Updated cmdlet:</span></span>
        - <span data-ttu-id="0a3b9-1091">New-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1091">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="0a3b9-1092">Add-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1092">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="0a3b9-1093">Set-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1093">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="0a3b9-1094">Команда New-AzApplicationGatewayProbeConfig Шлюза приложений обновлена для поддержки настраиваемого порта в зонде.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1094">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="0a3b9-1095">Обновлен командлет New-AzApplicationGatewayProbeConfig: добавлен необязательный параметр Port, который используется при проверке внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1095">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="0a3b9-1096">Этот параметр применяется к номерам SKU Standard_V2 и WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1096">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0a3b9-1097">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1097">Az.OperationalInsights</span></span>
* <span data-ttu-id="0a3b9-1098">Обновленная версия по умолчанию для сохраненных операций поиска имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1098">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="0a3b9-1099">Исправлены ошибки при обработке регулярных выражений со значениями NULL в журналах.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1099">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a3b9-1100">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1100">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a3b9-1101">Обновлен файл Get-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1101">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="0a3b9-1102">Обновлен файл Get-AzRecoveryServicesBackupContainer.md.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1102">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="0a3b9-1103">Обновлен файл Get-AzRecoveryServicesVault.md.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1103">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="0a3b9-1104">Обновлен файл Wait-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1104">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="0a3b9-1105">Обновлен файл Set-AzRecoveryServicesVaultContext.md.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1105">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="0a3b9-1106">Обновлен файл Get-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1106">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="0a3b9-1107">Обновлен файл Get-AzRecoveryServicesBackupRecoveryPoint.md.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1107">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="0a3b9-1108">Обновлен файл Restore-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1108">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="0a3b9-1109">Обновлен вызов службы для отмены регистрации контейнера в общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1109">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="0a3b9-1110">Обновлен файл Set-AzRecoveryServicesAsrAlertSetting.md.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1110">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a3b9-1111">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1111">Az.Resources</span></span>
- <span data-ttu-id="0a3b9-1112">Удален отсутствующий командлет, который упоминается в документации по New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1112">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="0a3b9-1113">Обновлены командлеты политик для использования новой версии API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1113">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0a3b9-1114">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1114">Az.ServiceBus</span></span>
* <span data-ttu-id="0a3b9-1115">Добавлен новый командлет для создания маркера SAS: New-AzServiceBusAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1115">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="0a3b9-1116">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1116">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a3b9-1117">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1117">Az.Sql</span></span>
* <span data-ttu-id="0a3b9-1118">Исправлены отсутствующие примеры для командлета Set-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1118">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="0a3b9-1119">Исправлены заданные повторяющиеся проверки для оценки наличия уязвимостей без указания адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1119">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="0a3b9-1120">Исправлена незначительная опечатка в сообщении предупреждения.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1120">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a3b9-1121">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1121">Az.Storage</span></span>
* <span data-ttu-id="0a3b9-1122">Обновлен пример в справочной документации для использования командлетом Get-AzStorageAccount правильного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1122">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="0a3b9-1123">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1123">Az.StorageSync</span></span>
* <span data-ttu-id="0a3b9-1124">Добавлен командлет Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1124">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="0a3b9-1125">Исправлена проблема № 9551, связанная с TierFilesOlderThanDays.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1125">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a3b9-1126">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1126">Az.Websites</span></span>
* <span data-ttu-id="0a3b9-1127">Исправлена ошибка, при которой некоторые свойства SiteConfig не возвращались Get-AzWebApp и Set-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1127">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="0a3b9-1128">Добавлен новый параметр Location в Get-AzDeletedWebApp и Restore-AzDeletedWebApp.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1128">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="0a3b9-1129">Исправлена ошибка, которая возникала при клонировании слотов веб-приложений с помощью командлета New-AzWebApp-IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1129">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="0a3b9-1130">2.4.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1130">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0a3b9-1131">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1131">Az.Accounts</span></span>
* <span data-ttu-id="0a3b9-1132">Добавлена поддержка командлетов профиля.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1132">Add support for profile cmdlets</span></span>
* <span data-ttu-id="0a3b9-1133">Добавлена поддержка сред и плоскостей данных в созданных командлетах.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1133">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="0a3b9-1134">Исправлена ошибка, когда в командлетах плоскости данных в Windows PowerShell в некоторых случаях использовалась неправильная конечная точка.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1134">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="0a3b9-1135">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1135">Az.Advisor</span></span>
* <span data-ttu-id="0a3b9-1136">Выпущена общедоступная версия Az.Advisor.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1136">GA release of Az.Advisor</span></span>
* <span data-ttu-id="0a3b9-1137">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1137">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="0a3b9-1138">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1138">Az.ApiManagement</span></span>
* <span data-ttu-id="0a3b9-1139">исправлена проблема https://github.com/Azure/azure-powershell/issues/8671.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1139">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="0a3b9-1140">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1140">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="0a3b9-1141">Добавлена поддержка запрашивания подписок по пользователю и продукту.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1141">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="0a3b9-1142">Добавлена поддержка создания запросов с использованием области "/", "/apis", "/apis/echo-api".</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1142">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="0a3b9-1143">Исправлены проблемы https://github.com/Azure/azure-powershell/issues/9307 и https://github.com/Azure/azure-powershell/issues/8432.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1143">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="0a3b9-1144">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1144">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="0a3b9-1145">Добавлена поддержка указания ApiVersion и ApiVersionSetId при импорте API-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1145">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0a3b9-1146">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1146">Az.Automation</span></span>
* <span data-ttu-id="0a3b9-1147">Исправлена ошибка командлета Set-AzAutomationConnectionFieldValue при обработке строкового значения.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1147">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a3b9-1148">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1148">Az.Compute</span></span>
* <span data-ttu-id="0a3b9-1149">В New AzImageConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1149">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a3b9-1150">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1150">Az.DataFactory</span></span>
* <span data-ttu-id="0a3b9-1151">Обновление выходных данных командлетов ADF, предназначенных для получения числа выполнений действий, конвейеров и триггеров, для поддержки канала Select-Object.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1151">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="0a3b9-1152">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1152">Az.EventGrid</span></span>
* <span data-ttu-id="0a3b9-1153">Исправлена опечатка в документации по командлету New-AzEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1153">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0a3b9-1154">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1154">Az.IotHub</span></span>
* <span data-ttu-id="0a3b9-1155">Добавлена поддержка повторного создания ключей политики авторизации.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1155">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a3b9-1156">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1156">Az.Network</span></span>
* <span data-ttu-id="0a3b9-1157">К тегам общедоступного IP-адреса добавлен тег RoutingPreference.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1157">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="0a3b9-1158">Улучшены примеры для справочной документации по командлету Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1158">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0a3b9-1159">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1159">Az.PolicyInsights</span></span>
* <span data-ttu-id="0a3b9-1160">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1160">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="0a3b9-1161">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9446.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1161">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0a3b9-1162">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1162">Az.OperationalInsights</span></span>
* <span data-ttu-id="0a3b9-1163">Исправленная модель источника данных CustomLog возвращена в командлет Get-AzOperationalInsightsDataSource.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1163">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a3b9-1164">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1164">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a3b9-1165">Выпущено исправление для команды get-policy для виртуальных машин IaaS.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1165">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a3b9-1166">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1166">Az.Resources</span></span>
    - <span data-ttu-id="0a3b9-1167">Исправлен текст справки по параметру Get-AzPolicyState -Top.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1167">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="0a3b9-1168">Добавлена поддержка разбиения по страницам на стороне клиента для Get-AzPolicyAlias.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1168">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="0a3b9-1169">Добавлены новые параметры для Set-AzPolicyAssignment, -PolicyParameters и -PolicyParametersObject.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1169">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="0a3b9-1170">Добавлен ряд обновлений документов и примеров для командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1170">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0a3b9-1171">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1171">Az.ServiceBus</span></span>
* <span data-ttu-id="0a3b9-1172">Исправление ошибки № 4938: командлет New-AzureRmServiceBusQueue возвращает ответ BadRequest (Недопустимый запрос) при задании значения MaxSizeInMegabytes.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1172">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a3b9-1173">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1173">Az.Sql</span></span>
* <span data-ttu-id="0a3b9-1174">Из выпуска предварительной версии в выпуск общедоступной версии добавлены командлеты группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1174">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="0a3b9-1175">Поддержка аудита Azure SQL Server и баз данных с помощью новых командлетов:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1175">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="0a3b9-1176">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1176">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="0a3b9-1177">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1177">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="0a3b9-1178">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1178">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="0a3b9-1179">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1179">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="0a3b9-1180">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1180">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="0a3b9-1181">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1181">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="0a3b9-1182">Из параметров оценки уязвимостей удалены ограничения, касающиеся электронной почты.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1182">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a3b9-1183">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1183">Az.Storage</span></span>
* <span data-ttu-id="0a3b9-1184">Два параметра в указанном ниже командлете — -IndexDocument и -ErrorDocument404Path, — которые ранее были обязательными, стали необязательными:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1184">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="0a3b9-1185">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1185">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="0a3b9-1186">Обновлена справка по командлету Get-AzStorageBlobContent: добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1186">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="0a3b9-1187">При сбое выполнения командлета с ошибкой StorageException отображаются дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1187">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="0a3b9-1188">Добавлена поддержка создания или обновления учетной записи хранения с использованием проверки подлинности AAD DS для службы "Файлы Azure".</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1188">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="0a3b9-1189">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1189">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="0a3b9-1190">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1190">Set-AzStorageAccount</span></span>
* <span data-ttu-id="0a3b9-1191">Добавлена поддержка перечисления или закрытия дескрипторов файлов для общей папки, каталога файлов или файла:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1191">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="0a3b9-1192">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1192">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="0a3b9-1193">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1193">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="0a3b9-1194">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1194">Az.StorageSync</span></span>
* <span data-ttu-id="0a3b9-1195">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1195">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="0a3b9-1196">2.3.2 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1196">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0a3b9-1197">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1197">Az.Accounts</span></span>
* <span data-ttu-id="0a3b9-1198">Исправлена ошибка, связанная с использованием неправильного URL-адреса для вызовов функций.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1198">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="0a3b9-1199">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8983.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1199">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="0a3b9-1200">Устранена проблема с псевдонимами из AzureRM для командлетов Az.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1200">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="0a3b9-1201">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1201">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="0a3b9-1202">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1202">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a3b9-1203">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1203">Az.Compute</span></span>
* <span data-ttu-id="0a3b9-1204">Простые наборы параметров New-AzVm и New-AzVmss теперь принимают параметр ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1204">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="0a3b9-1205">Исправлена опечатка в справочной документации по New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1205">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="0a3b9-1206">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1206">Az.Dns</span></span>
* <span data-ttu-id="0a3b9-1207">Исправлена опечатка в справочных примерах по использованию Set-AzDnsZone.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1207">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="0a3b9-1208">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1208">Az.EventGrid</span></span>
* <span data-ttu-id="0a3b9-1209">Обновлен для использования API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1209">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="0a3b9-1210">Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1210">New cmdlets:</span></span>
    - <span data-ttu-id="0a3b9-1211">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1211">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="0a3b9-1212">Создает домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1212">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="0a3b9-1213">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1213">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="0a3b9-1214">Возвращает сведения о домене Сетки событий или список всех доменов Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1214">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="0a3b9-1215">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1215">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="0a3b9-1216">Удаляет домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1216">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="0a3b9-1217">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1217">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="0a3b9-1218">Повторно создает ключ общего доступа для домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1218">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="0a3b9-1219">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1219">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="0a3b9-1220">Возвращает ключи общего доступа, используемые для публикации событий в домене Сетки событий.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1220">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="0a3b9-1221">New-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1221">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="0a3b9-1222">Создает раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1222">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="0a3b9-1223">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1223">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="0a3b9-1224">Возвращает сведения о разделе домена Сетки событий или список всех разделов определенного домена Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1224">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="0a3b9-1225">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1225">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="0a3b9-1226">Удаляет раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1226">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="0a3b9-1227">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1227">Updated cmdlets:</span></span>
    - <span data-ttu-id="0a3b9-1228">New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1228">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="0a3b9-1229">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для нового домена Сетки событий и раздела домена Сетки событий и позволяющие создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1229">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="0a3b9-1230">Добавляют новые обязательные параметры для указания имени нового домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1230">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="0a3b9-1231">Добавляют новые наборы параметров для доменов и разделов домена и позволяют повторно использовать существующие параметры (например, EndPointType, SubjectBeginsWith и т. д.).</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1231">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="0a3b9-1232">Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1232">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="0a3b9-1233">срока действия подписки на событие;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1233">Event subscription expiration date,</span></span>
            - <span data-ttu-id="0a3b9-1234">параметров расширенной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1234">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="0a3b9-1235">Добавляют новое перечисление для ServiceBusQueue в качестве места назначения.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1235">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="0a3b9-1236">Запрещают использование значение All в параметре -IncludedEventType и заменяют его следующим:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1236">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="0a3b9-1237">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1237">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="0a3b9-1238">Добавляют новые необязательные параметры (Top, ODataQuery и NextLink) для поддержки разбиения на страницы и фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1238">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="0a3b9-1239">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1239">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="0a3b9-1240">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для домена Сетки событий и раздела домена Сетки событий и позволяющие удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1240">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="0a3b9-1241">Добавляют новые обязательные параметры для указания имени домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1241">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0a3b9-1242">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1242">Az.FrontDoor</span></span>
* <span data-ttu-id="0a3b9-1243">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1243">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="0a3b9-1244">Добавляет поддержку преобразований и новое значение оператора автозавершения (RegEx).</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1244">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="0a3b9-1245">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1245">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="0a3b9-1246">Добавляет новые значения автозавершения.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1246">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a3b9-1247">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1247">Az.Network</span></span>
* <span data-ttu-id="0a3b9-1248">Добавляет поддержку ресурса шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1248">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="0a3b9-1249">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1249">New cmdlets</span></span>
        - <span data-ttu-id="0a3b9-1250">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1250">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="0a3b9-1251">Добавляет AvailablePrivateEndpointType.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1251">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="0a3b9-1252">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1252">New cmdlets</span></span>
        - <span data-ttu-id="0a3b9-1253">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1253">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="0a3b9-1254">Добавляет PrivatePrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1254">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="0a3b9-1255">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1255">New cmdlets</span></span>
        - <span data-ttu-id="0a3b9-1256">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1256">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="0a3b9-1257">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1257">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="0a3b9-1258">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1258">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="0a3b9-1259">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1259">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="0a3b9-1260">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1260">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="0a3b9-1261">Добавляет PrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1261">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="0a3b9-1262">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1262">New cmdlets</span></span>
        - <span data-ttu-id="0a3b9-1263">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1263">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="0a3b9-1264">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1264">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="0a3b9-1265">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1265">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="0a3b9-1266">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1266">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="0a3b9-1267">Обновлены следующие команды для функции: флаг UseLocalAzureIpAddress для VPN-подключения.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1267">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="0a3b9-1268">Обновлен командлет New-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1268">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="0a3b9-1269">Обновлен командлет Set-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1269">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="0a3b9-1270">В пиринг ExpressRoute добавлено поле только для чтения PeeredConnections.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1270">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="0a3b9-1271">В ExpressRoute добавлено поле только для чтения GlobalReachEnabled.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1271">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="0a3b9-1272">Добавлен атрибут в рамках критического изменения, отменяющего статус устаревшего поля AllowGlobalReach в модели ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1272">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="0a3b9-1273">Исправлена проблема, связанная с ошибкой 8756, при использовании TargetListenerID с командлетами AzApplicationGatewayRedirectConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1273">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="0a3b9-1274">Исправлена ошибка в New-AzApplicationGatewayPathRuleConfig, не позволявшая задавать набор правил повторного создания.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1274">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="0a3b9-1275">Исправлено отображение VirtualNetworkTaps в NetworkInterfaceIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1275">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="0a3b9-1276">Исправлены командлеты Cortex Get для отображения всех частей.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1276">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="0a3b9-1277">Исправлено создание ссылок VirtualHub для ExpressRouteGateways и VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1277">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="0a3b9-1278">В AzureFirewall и NatGateway добавлена поддержка Зон доступности.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1278">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="0a3b9-1279">Добавлен командлет Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1279">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="0a3b9-1280">Добавлена поддержка нескольких общедоступных IP-адресов для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1280">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="0a3b9-1281">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1281">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="0a3b9-1282">Добавлен параметр -PublicIpAddress, который принимает один или несколько объектов общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1282">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="0a3b9-1283">Добавлен параметр -VirtualNetwork, который принимает объект виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1283">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="0a3b9-1284">Добавлены методы AddPublicIpAddress и RemovePublicIpAddress для объекта брандмауэра. Они принимают объект общедоступного IP-адреса в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1284">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="0a3b9-1285">Не рекомендуется использовать параметры -PublicIpName и -VirtualNetworkName.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1285">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="0a3b9-1286">Обновлены следующие команды для функции: В параметрах проверки подлинности AAD VPN-клиента задан ресурс шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1286">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="0a3b9-1287">Обновлен командлет New-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1287">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="0a3b9-1288">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1288">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="0a3b9-1289">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр-переключатель RemoveAadAuthentication для удаления в шлюзе параметров проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1289">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0a3b9-1290">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1290">Az.OperationalInsights</span></span>
* <span data-ttu-id="0a3b9-1291">Добавлена поддержка SKU **pergb2018** в команде New-AzureRmOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1291">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a3b9-1292">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1292">Az.Resources</span></span>
* <span data-ttu-id="0a3b9-1293">Поддержка дополнительных вариантов экспорта шаблона.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1293">Support for additional Template Export options</span></span>
    - <span data-ttu-id="0a3b9-1294">В Export-AzResourceGroup добавлен параметр -SkipResourceNameParameterization.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1294">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="0a3b9-1295">В Export-AzResourceGroup добавлен параметр -SkipAllParameterization.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1295">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="0a3b9-1296">В Export-AzResourceGroup добавлен параметр -Resource для фильтрации экспортированных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1296">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0a3b9-1297">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1297">Az.ServiceFabric</span></span>
* <span data-ttu-id="0a3b9-1298">Исправлена ошибка, связанная с получением иногда неправильных отпечатков при добавлении сертификата ByExistingKeyVault.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1298">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a3b9-1299">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1299">Az.Sql</span></span>
* <span data-ttu-id="0a3b9-1300">Исправлен суффикс конечной точки хранилища службы "Расширенная защита от угроз Azure".</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1300">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="0a3b9-1301">Исправлена ошибка, связанная с возможностью пакета "Расширенная защита данных" переопределять политику службы "Расширенная защита от угроз".</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1301">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="0a3b9-1302">Новые командлеты для Management.Sql позволяют клиентам добавлять ключи TDE и задавать средство защиты TDE для управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1302">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="0a3b9-1303">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1303">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="0a3b9-1304">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1304">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="0a3b9-1305">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1305">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="0a3b9-1306">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1306">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="0a3b9-1307">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1307">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a3b9-1308">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1308">Az.Storage</span></span>
* <span data-ttu-id="0a3b9-1309">Поддержка класса Kind в FileStorage и значения Premium_ZRS в SkuName при создании учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1309">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="0a3b9-1310">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1310">New-AzStorageAccount</span></span>
* <span data-ttu-id="0a3b9-1311">Уточнено описание командлета неизменности BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1311">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="0a3b9-1312">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1312">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a3b9-1313">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1313">Az.Websites</span></span>
* <span data-ttu-id="0a3b9-1314">Оптимизирует Get-AzWebAppCertificate для фильтрации по группе ресурсов на сервере, а не в клиенте.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1314">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="0a3b9-1315">Добавляет параметр-переключатель - UseDisasterRecovery в Get AzWebAppSnapshot.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1315">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="0a3b9-1316">2.2.0 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1316">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="0a3b9-1317">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1317">Az.Cdn</span></span>
* <span data-ttu-id="0a3b9-1318">Обновлены командлеты для поддержки функции rulesEngine на основе API версии 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1318">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a3b9-1319">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1319">Az.Compute</span></span>
* <span data-ttu-id="0a3b9-1320">Добавлен параметр `NoWait`, который запускает операцию и немедленно возвращает значение еще до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1320">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="0a3b9-1321">Обновлены командлеты:   Export-AzLogAnalyticRequestRateByInterval; Export-AzLogAnalyticThrottledRequest; Remove-AzVM; Remove-AzVMAccessExtension; Remove-AzVMAEMExtension; Remove-AzVMChefExtension; Remove-AzVMCustomScriptExtension; Remove-AzVMDiagnosticsExtension; Remove-AzVMDiskEncryptionExtension; Remove-AzVMDscExtension; Remove-AzVMSqlServerExtension; Restart-AzVM; Set-AzVM; Set-AzVMAccessExtension; Set-AzVMADDomainExtension; Set-AzVMAEMExtension; Set-AzVMBginfoExtension; Set-AzVMChefExtension; Set-AzVMCustomScriptExtension; Set-AzVMDiagnosticsExtension; Set-AzVMDscExtension; Set-AzVMExtension; Start-AzVM; Stop-AzVM; Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1321">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0a3b9-1322">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1322">Az.EventHub</span></span>
* <span data-ttu-id="0a3b9-1323">Исправлена ошибка № 9231. Командлет Get-AzEventHubNamespace не возвращал теги.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1323">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="0a3b9-1324">Исправлена ошибка № 9230. Командлет Get-AzEventHubNamespace возвращал значение ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1324">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a3b9-1325">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1325">Az.Network</span></span>
* <span data-ttu-id="0a3b9-1326">Обновлены параметры ResourceId и InputObject для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1326">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="0a3b9-1327">Добавлены псевдонимы для параметров ResourceId и InputObject.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1327">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0a3b9-1328">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1328">Az.PolicyInsights</span></span>
* <span data-ttu-id="0a3b9-1329">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyEvent.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1329">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a3b9-1330">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1330">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a3b9-1331">Минимальный срок хранения политики IaaSVM изменился с 1 до 7 дней.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1331">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0a3b9-1332">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1332">Az.ServiceBus</span></span>
* <span data-ttu-id="0a3b9-1333">Исправлена ошибка № 9182. Командлет Get-AzServiceBusNamespace возвращал ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1333">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0a3b9-1334">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1334">Az.ServiceFabric</span></span>
* <span data-ttu-id="0a3b9-1335">Исправлена опечатка в сообщении об ошибке для командлета Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1335">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="0a3b9-1336">Добавлен отсутствующий символ в командных строках Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1336">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a3b9-1337">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1337">Az.Sql</span></span>
* <span data-ttu-id="0a3b9-1338">Для командлета New-AzureSqlInstance добавлен параметр DnsZonePartner, обеспечивающий поддержку AutoDr для Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1338">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="0a3b9-1339">Командлет Get-AzSqlDatabaseSecureConnectionPolicy объявлен неподдерживаемым.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1339">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="0a3b9-1340">Командлеты обнаружения угроз переименованы в командлеты Расширенной защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1340">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="0a3b9-1341">Параметры -StorageSizeInGB и -LicenseType командлета New-AzSqlInstance теперь необязательны.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1341">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a3b9-1342">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1342">Az.Websites</span></span>
* <span data-ttu-id="0a3b9-1343">Исправлены проблемы, когда удалялись теги при использовании Set-AzWebApp и Set-AzWebAppSlot со свойством -WebApp.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1343">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="0a3b9-1344">2.1.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1344">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="0a3b9-1345">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1345">Az.ApiManagement</span></span>
* <span data-ttu-id="0a3b9-1346">Созданы командлеты для управления диагностикой в глобальной области и в области API.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1346">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="0a3b9-1347">**Get-AzApiManagementDiagnostic**  — получение диагностики, заданной глобально или на уровне области API.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1347">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="0a3b9-1348">**New-AzApiManagementDiagnostic**  — создание диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1348">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="0a3b9-1349">**New-AzApiManagementHttpMessageDiagnostic**  — создание параметра диагностики, для которого регистрируются заголовки и размер байтов тела.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1349">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="0a3b9-1350">**New-AzApiManagementPipelineDiagnosticSetting**  — создание параметров диагностики для сообщений HTTP, поступающих в шлюз или исходящих из него.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1350">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="0a3b9-1351">**New-AzApiManagementSamplingSetting**  — создание параметра выборки для запросов и ответов касательно диагностики.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1351">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="0a3b9-1352">**Remove-AzApiManagementDiagnostic**  — удаление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1352">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="0a3b9-1353">**Set-AzApiManagementDiagnostic**  — обновление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1353">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="0a3b9-1354">Созданы командлеты для управления кэшем в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1354">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="0a3b9-1355">**Get-AzApiManagementCache**  — получение сведений о кэше, указанном идентификатором, или обо всех кэшах.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1355">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="0a3b9-1356">**New-AzApiManagementCache**  — создание кэша по умолчанию или кэша в определенном регионе Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1356">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="0a3b9-1357">**Remove-AzApiManagementCache**  — удаление кэша.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1357">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="0a3b9-1358">**Update-AzApiManagementCache**  — обновление кэша.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1358">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="0a3b9-1359">Созданы командлеты для управления схемой API.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1359">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="0a3b9-1360">**New-AzApiManagementSchema**  — создание схемы для API.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1360">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="0a3b9-1361">**Get-AzApiManagementSchema**  — получение схем, настроенных в API.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1361">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="0a3b9-1362">**Remove-AzApiManagementSchema**  — удаление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1362">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="0a3b9-1363">**Set-AzApiManagementSchema**  — обновление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1363">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="0a3b9-1364">Создан командлет для создания токена пользователя.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1364">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="0a3b9-1365">**New-AzApiManagementUserToken**  — создание токена пользователя, по умолчанию действительного в течение 8 часов. С помощью этого командлета можно создавать токен для пользователя GIT.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1365">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="0a3b9-1366">Создан командлет для получения состояния сети.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1366">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="0a3b9-1367">**Get-AzApiManagementNetworkStatus**  — получение состояния подключения сети ресурсов, от которых зависит служба "Управление API".</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1367">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="0a3b9-1368">Это полезно при развертывании службы ApiManagement в виртуальной сети и проверке того, не нарушена ли какая-либо из зависимостей.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1368">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="0a3b9-1369">Обновлен командлет **New-AzApiManagement** для управления службой ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1369">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="0a3b9-1370">Добавлена поддержка нового SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1370">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="0a3b9-1371">Добавлена поддержка для включения флага EnableClientCertificate в SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1371">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="0a3b9-1372">Новый командлет **New-AzApiManagementSslSetting** позволяет настраивать параметр TLS/SSL для сервера (Backend) и внешнего интерфейса (Frontend).</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1372">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="0a3b9-1373">Его также можно использовать для настройки Ciphers как 3DES, в ServerProtocols как Http2 для внешнего интерфейса (Frontend) службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1373">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="0a3b9-1374">Добавлена поддержка настройки имени узла DeveloperPortal в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1374">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="0a3b9-1375">Обновлен командлет **Get-AzApiManagementSsoToken** для извлечения объекта PsApiManagement в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1375">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="0a3b9-1376">Обновлен командлет для отображения встроенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1376">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="0a3b9-1377">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Код ошибки: ValidationError. Сообщение об ошибке: "Некоторые поля содержат неправильные значения". Сведения об ошибке: [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1377">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="0a3b9-1378">Обновлен командлет **Export-AzApiManagementApi** для экспортирования программных интерфейсов в формате OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1378">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="0a3b9-1379">Обновлен командлет **Import-AzApiManagementApi** :</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1379">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="0a3b9-1380">Для импортирования API из спецификации документа OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1380">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="0a3b9-1381">Для переопределения свойства PsApiManagementSchema, указанного в любом документе (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1381">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="0a3b9-1382">Для переопределения свойства ServiceUrl, указанного в любом документе.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1382">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="0a3b9-1383">Обновлен командлет **Get-AzApiManagementPolicy** для возврата политики в формате, экранированном не для XML, с использованием rawxml.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1383">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="0a3b9-1384">Обновлен командлет **Set-AzApiManagementPolicy**. Он принимает политику в формате, экранированном не для XML, с использованием rawxml и в формате, экранированном для XML, с использованием XML.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1384">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="0a3b9-1385">Обновлен командлет **New-AzApiManagementApi** :</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1385">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="0a3b9-1386">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1386">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="0a3b9-1387">Для создания API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1387">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="0a3b9-1388">Для клонирования API с использованием значений SourceApiId и SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1388">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="0a3b9-1389">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1389">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="0a3b9-1390">Обновлен командлет **Set-AzApiManagementApi** :</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1390">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="0a3b9-1391">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1391">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="0a3b9-1392">Для обновления API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1392">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="0a3b9-1393">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1393">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="0a3b9-1394">Обновлен командлет **New-AzApiManagementRevision** :</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1394">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="0a3b9-1395">Для клонирования (копирования тегов, продуктов, операций и политик) существующей редакции с использованием SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1395">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="0a3b9-1396">Новая редакция предполагает родительский идентификатор ApiId.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1396">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="0a3b9-1397">Для предоставления ApiRevisionDescription.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1397">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="0a3b9-1398">Для переопределения значения ServiceUrl при клонировании API.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1398">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="0a3b9-1399">Обновлен командлет **New-AzApiManagementIdentityProvider** :</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1399">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="0a3b9-1400">Для настройки AAD или AADB2C с Authority.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1400">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="0a3b9-1401">Для установки политик SignupPolicy, SigninPolicy, ProfileEditingPolicy и PasswordResetPolicy.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1401">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="0a3b9-1402">Обновлен командлет **New-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1402">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="0a3b9-1403">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1403">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="0a3b9-1404">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1404">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="0a3b9-1405">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1405">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="0a3b9-1406">Обновлен командлет **Set-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1406">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="0a3b9-1407">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1407">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="0a3b9-1408">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1408">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="0a3b9-1409">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1409">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="0a3b9-1410">Следующие командлеты обновлены, чтобы принимать значение ResourceId в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1410">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="0a3b9-1411">New-AzApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1411">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="0a3b9-1412">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1412">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="0a3b9-1413">Get-AzApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1413">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="0a3b9-1414">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1414">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="0a3b9-1415">Get-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1415">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="0a3b9-1416">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1416">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="0a3b9-1417">Get-AzApiManagementAuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1417">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="0a3b9-1418">Get-AzApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1418">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="0a3b9-1419">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1419">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="0a3b9-1420">Get-AzApiManagementCertificate.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1420">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="0a3b9-1421">Remove-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1421">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="0a3b9-1422">Remove-AzApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1422">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0a3b9-1423">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1423">Az.Automation</span></span>
* <span data-ttu-id="0a3b9-1424">Обновлен командлет Get-AzAutomationJobOutputRecord для обработки значений в формате JSON и в виде текстовой записи.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1424">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="0a3b9-1425">исправлена проблема https://github.com/Azure/azure-powershell/issues/7977.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1425">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="0a3b9-1426">исправлена проблема https://github.com/Azure/azure-powershell/issues/8600.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1426">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="0a3b9-1427">Поведение командлета Start-AzAutomationDscCompilationJob изменено так, чтобы сразу же запустить задание, а не ждать его завершения.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1427">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="0a3b9-1428">исправлена проблема https://github.com/Azure/azure-powershell/issues/8347.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1428">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="0a3b9-1429">Исправлен командлет Get-AzAutomationDscNode, возвращающий все узлы при использовании -Name.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1429">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="0a3b9-1430">Теперь он возвращает только соответствующий узел.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1430">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a3b9-1431">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1431">Az.Compute</span></span>
* <span data-ttu-id="0a3b9-1432">Добавлены параметры ProtectFromScaleIn и ProtectFromScaleSetAction для командлета Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1432">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="0a3b9-1433">Командлет New-AzVM с простым набором параметров теперь по умолчанию использует доступное расположение, если регион "восточная часть США" не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1433">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0a3b9-1434">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1434">Az.DataLakeStore</span></span>
* <span data-ttu-id="0a3b9-1435">Обновлен пакет SDK ADLS для использования httpclient. В инфраструктуру Azure интегрирована проверка плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1435">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0a3b9-1436">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1436">Az.Monitor</span></span>
* <span data-ttu-id="0a3b9-1437">Исправлены неправильные имена параметров в справочных примерах.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1437">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a3b9-1438">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1438">Az.Network</span></span>
* <span data-ttu-id="0a3b9-1439">Добавлен флаг DisableBgpRoutePropagation для выходных данных действующей таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1439">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="0a3b9-1440">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1440">Updated cmdlet:</span></span>
        - <span data-ttu-id="0a3b9-1441">Get-AzEffectiveRouteTable.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1441">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="0a3b9-1442">Исправлен двойной дефис в документации New-AzApplicationGatewayTrustedRootCertificate.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1442">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a3b9-1443">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1443">Az.Resources</span></span>
* <span data-ttu-id="0a3b9-1444">Добавлен новый командлет Get-AzureRmDenyAssignment для получения запрещающих назначений.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1444">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a3b9-1445">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1445">Az.Sql</span></span>
* <span data-ttu-id="0a3b9-1446">Командлеты Расширенной защиты от угроз переименованы на командлеты Расширенной защиты данных, и оценка уязвимости включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1446">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="0a3b9-1447">2.0.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1447">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0a3b9-1448">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1448">Az.Accounts</span></span>
* <span data-ttu-id="0a3b9-1449">Обновлена библиотека аутентификации для устранения проблем с ADFS при использовании аутентификации на основе имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1449">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0a3b9-1450">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1450">Az.CognitiveServices</span></span>
* <span data-ttu-id="0a3b9-1451">Отображается только заявление об отказе Bing для служб Поиска Bing.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1451">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="0a3b9-1452">Исправлена проблема с созданием учетной записи.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1452">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a3b9-1453">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1453">Az.Compute</span></span>
* <span data-ttu-id="0a3b9-1454">Функция группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1454">Proximity placement group feature.</span></span>
    - <span data-ttu-id="0a3b9-1455">Добавлены следующие новые командлеты:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1455">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="0a3b9-1456">Новый параметр ProximityPlacementGroupId будет добавлен в следующие командлеты:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1456">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="0a3b9-1457">В командлет New-AzGalleryImageVersion добавлен параметр StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1457">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="0a3b9-1458">TargetRegion в командлете New-AzGalleryImageVersion может содержать StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1458">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="0a3b9-1459">Параметр-переключатель SkipShutdown добавлен в командлеты Stop-AzVM и Stop-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1459">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="0a3b9-1460">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1460">Breaking changes</span></span>
    - <span data-ttu-id="0a3b9-1461">Командлет SET-AzVMBootDiagnostics изменен на Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1461">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="0a3b9-1462">Командлет Export-AzLogAnalyticThrottledRequests изменен на Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1462">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="0a3b9-1463">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1463">Az.DeploymentManager</span></span>
* <span data-ttu-id="0a3b9-1464">Первая общедоступная версия командлетов диспетчера развертывания Azure</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1464">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="0a3b9-1465">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1465">Az.Dns</span></span>
* <span data-ttu-id="0a3b9-1466">Автоматическое делегирование DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1466">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="0a3b9-1467">Командлет для создания зоны DNS принимает имя родительской зоны в качестве дополнительного необязательного параметра.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1467">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="0a3b9-1468">Он добавляет записи NS в родительской зоне для созданной дочерней зоны.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1468">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0a3b9-1469">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1469">Az.FrontDoor</span></span>
* <span data-ttu-id="0a3b9-1470">Первая общедоступная версия командлетов Azure FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1470">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="0a3b9-1471">Переименованы командлеты WAF для включения Waf.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1471">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="0a3b9-1472">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1472">Az.HDInsight</span></span>
* <span data-ttu-id="0a3b9-1473">Удалены два командлета:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1473">Removed two cmdlets:</span></span>
    - <span data-ttu-id="0a3b9-1474">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1474">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="0a3b9-1475">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1475">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="0a3b9-1476">Добавлен новый командлет Set-AzHDInsightGatewayCredential для замены Grant-AzHDInsightHttpServicesAccess.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1476">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="0a3b9-1477">Обновлен командлет Get-AzHDInsightJobOutput для различения ролей читателя и оператора HDInsight:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1477">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="0a3b9-1478">Пользователям с ролью читателя не нужно указывать параметр DefaultStorageAccountKey явным образом, иначе возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1478">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="0a3b9-1479">На пользователей с ролью оператора HDInsight это не повлияет.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1479">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0a3b9-1480">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1480">Az.Monitor</span></span>
* <span data-ttu-id="0a3b9-1481">Новые командлеты для API SQR (запланированное правило запросов)</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1481">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="0a3b9-1482">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1482">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="0a3b9-1483">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1483">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="0a3b9-1484">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1484">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="0a3b9-1485">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1485">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="0a3b9-1486">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1486">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="0a3b9-1487">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1487">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="0a3b9-1488">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1488">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0a3b9-1489">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1489">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0a3b9-1490">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1490">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0a3b9-1491">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1491">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0a3b9-1492">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1492">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0a3b9-1493">См. подробнее об [API SQR](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules).</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1493">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="0a3b9-1494">Обновлен файл Az.Monitor.md для включения командлетов для правила генерации оповещений на основе метрик GenV2(не классическая версия).</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1494">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a3b9-1495">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1495">Az.Network</span></span>
* <span data-ttu-id="0a3b9-1496">Добавлена поддержка для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1496">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="0a3b9-1497">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1497">New cmdlets</span></span>
        - <span data-ttu-id="0a3b9-1498">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1498">New-AzNatGateway</span></span>
        - <span data-ttu-id="0a3b9-1499">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1499">Get-AzNatGateway</span></span>
        - <span data-ttu-id="0a3b9-1500">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1500">Set-AzNatGateway</span></span>
        - <span data-ttu-id="0a3b9-1501">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1501">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="0a3b9-1502">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1502">Updated cmdlets</span></span>
        - <span data-ttu-id="0a3b9-1503">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1503">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="0a3b9-1504">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1504">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="0a3b9-1505">Обновлены следующие команды для функции: Настройка и удаление пользовательских маршрутов через шлюз в Бруклине.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1505">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="0a3b9-1506">Обновлен командлет New-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1506">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="0a3b9-1507">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1507">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0a3b9-1508">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1508">Az.PolicyInsights</span></span>
* <span data-ttu-id="0a3b9-1509">Добавлена поддержка сведений об оценке политики запросов.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1509">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="0a3b9-1510">Добавлен параметр -Expand в командлет Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1510">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="0a3b9-1511">Добавлена поддержка -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1511">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a3b9-1512">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1512">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a3b9-1513">Добавлена поддержка перекрестной подписки на Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1513">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="0a3b9-1514">Добавлена возможность отмечать предстоящие критически важные изменения для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1514">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="0a3b9-1515">Исправлены план восстановления и план действий для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1515">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="0a3b9-1516">Исправлено сетевое сопоставление обновления Azure Site Recovery (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1516">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="0a3b9-1517">Исправлено направление защиты обновления Azure Site Recovery для управляемых дисков (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1517">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="0a3b9-1518">Добавлены другие незначительные исправления.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1518">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="0a3b9-1519">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1519">Az.Relay</span></span>
* <span data-ttu-id="0a3b9-1520">Исправлены опечатки в сообщениях для клиентов.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1520">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0a3b9-1521">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1521">Az.ServiceBus</span></span>
* <span data-ttu-id="0a3b9-1522">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1522">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a3b9-1523">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1523">Az.Storage</span></span>
* <span data-ttu-id="0a3b9-1524">Выполнено обновление клиентской библиотеки хранилища до версии 10.0.1 (пространство имен всех объектов из этого пакета SDK изменено с Microsoft.WindowsAzure.Storage. *на Microsoft.Azure.Storage* ).</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1524">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage. *' to 'Microsoft.Azure.Storage.* ')</span></span>
* <span data-ttu-id="0a3b9-1525">Выполнено обновление до Microsoft.Azure.Management.Storage версии 11.0.0 для включения поддержки нового API версии 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1525">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="0a3b9-1526">Значение свойства Kind по умолчанию в учетной записи хранения изменено со Storage на StorageV2.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1526">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="0a3b9-1527">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1527">New-AzStorageAccount</span></span>
* <span data-ttu-id="0a3b9-1528">Изменено значение Sku.Name в выходных данных командлета учетной записи хранения в соответствии со значением Sku.Name во входных данных путем добавления _ (например, StandardLRS изменено на Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1528">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="0a3b9-1529">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1529">New-AzStorageAccount</span></span>
    - <span data-ttu-id="0a3b9-1530">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1530">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="0a3b9-1531">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1531">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a3b9-1532">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1532">Az.Websites</span></span>
* <span data-ttu-id="0a3b9-1533">Свойство Kind теперь будет задаваться объектам PSSite, возвращаемым командлетом Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1533">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="0a3b9-1534">Get-AzWebApp\*Metrics и Get-AzAppServicePlanMetrics считаются нерекомендуемыми.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1534">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="0a3b9-1535">1.8.0 — апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1535">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0a3b9-1536">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1536">Highlights since the last major release</span></span>
* <span data-ttu-id="0a3b9-1537">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1537">General availability of `Az` module</span></span>
* <span data-ttu-id="0a3b9-1538">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1538">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="0a3b9-1539">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1539">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="0a3b9-1540">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1540">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="0a3b9-1541">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1541">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0a3b9-1542">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1542">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="0a3b9-1543">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1543">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0a3b9-1544">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1544">Az.Accounts</span></span>
* <span data-ttu-id="0a3b9-1545">Обновлен командлет Uninstall-AzureRm для правильного удаления модулей в Mac.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1545">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="0a3b9-1546">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1546">Az.Batch</span></span>
* <span data-ttu-id="0a3b9-1547">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1547">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0a3b9-1548">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1548">Az.Cdn</span></span>
* <span data-ttu-id="0a3b9-1549">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1549">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0a3b9-1550">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1550">Az.CognitiveServices</span></span>
* <span data-ttu-id="0a3b9-1551">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1551">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a3b9-1552">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1552">Az.Compute</span></span>
* <span data-ttu-id="0a3b9-1553">Устранена проблема с установкой AEM, если в идентификаторах ресурсов дисков группа ресурсов указана в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1553">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="0a3b9-1554">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1554">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0a3b9-1555">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1555">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a3b9-1556">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1556">Az.DataFactory</span></span>
* <span data-ttu-id="0a3b9-1557">Добавлены свойства SsisProperties, если NodeCount не имеет значения NULL для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1557">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0a3b9-1558">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1558">Az.DataLakeStore</span></span>
* <span data-ttu-id="0a3b9-1559">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1559">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="0a3b9-1560">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1560">Az.EventGrid</span></span>
* <span data-ttu-id="0a3b9-1561">Обновлен текст справки для конечной точки, указывающий, что необходимо создать ресурсы, прежде чем использовать командлеты для создания или обновления подписки на события.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1561">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0a3b9-1562">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1562">Az.EventHub</span></span>
* <span data-ttu-id="0a3b9-1563">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1563">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="0a3b9-1564">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1564">Az.HDInsight</span></span>
* <span data-ttu-id="0a3b9-1565">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1565">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0a3b9-1566">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1566">Az.IotHub</span></span>
* <span data-ttu-id="0a3b9-1567">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1567">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0a3b9-1568">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1568">Az.KeyVault</span></span>
* <span data-ttu-id="0a3b9-1569">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1569">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0a3b9-1570">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1570">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="0a3b9-1571">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1571">Az.MachineLearning</span></span>
* <span data-ttu-id="0a3b9-1572">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1572">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="0a3b9-1573">Az.Media</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1573">Az.Media</span></span>
* <span data-ttu-id="0a3b9-1574">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1574">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0a3b9-1575">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1575">Az.Monitor</span></span>
  * <span data-ttu-id="0a3b9-1576">Добавлены новые командлеты для правила генерации оповещений на основе метрик GenV2 (не классических).</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1576">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="0a3b9-1577">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1577">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="0a3b9-1578">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1578">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="0a3b9-1579">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1579">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="0a3b9-1580">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1580">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="0a3b9-1581">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1581">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="0a3b9-1582">Обновлен пакет SDK Monitor до предварительной версии 0.22.0.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1582">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a3b9-1583">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1583">Az.Network</span></span>
* <span data-ttu-id="0a3b9-1584">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1584">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0a3b9-1585">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1585">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="0a3b9-1586">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1586">Az.NotificationHubs</span></span>
* <span data-ttu-id="0a3b9-1587">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1587">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0a3b9-1588">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1588">Az.OperationalInsights</span></span>
* <span data-ttu-id="0a3b9-1589">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1589">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="0a3b9-1590">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1590">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="0a3b9-1591">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1591">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a3b9-1592">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1592">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a3b9-1593">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1593">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0a3b9-1594">Обновлен табличный формат для SQL на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1594">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="0a3b9-1595">Добавлен альтернативный метод для получения расположения в Общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1595">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="0a3b9-1596">Обновлено значение ScheduleRunDays в объекте SchedulePolicy в соответствии с часовым поясом.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1596">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="0a3b9-1597">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1597">Az.RedisCache</span></span>
* <span data-ttu-id="0a3b9-1598">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1598">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a3b9-1599">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1599">Az.Resources</span></span>
* <span data-ttu-id="0a3b9-1600">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1600">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a3b9-1601">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1601">Az.Sql</span></span>
* <span data-ttu-id="0a3b9-1602">Заменена зависимость от пакета SDK монитора на обычный код.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1602">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="0a3b9-1603">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1603">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0a3b9-1604">Улучшен процесс классификации нескольких столбцов.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1604">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="0a3b9-1605">Добавлены свойства SKU (имя, семейство, производительность SKU) в отклике Get-AzSqlServerServiceObjective, а также по умолчанию задан табличный формат.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1605">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="0a3b9-1606">C помощью Get-AzSqlServerServiceObjective теперь можно получать список доступных целевых служб по расположению без необходимости заранее размещать сервер в регионе.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1606">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="0a3b9-1607">Поддерживается параметр часового пояса при создании Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1607">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="0a3b9-1608">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1608">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a3b9-1609">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1609">Az.Websites</span></span>
* <span data-ttu-id="0a3b9-1610">Исправлены командлеты Set-AzWebApp и Set-AzWebAppSlot, которые теперь не удаляют теги при выполнении.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1610">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="0a3b9-1611">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1611">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0a3b9-1612">Обновлен пакет SDK веб-узлов.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1612">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="0a3b9-1613">Удалено свойство AdminSiteName из PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1613">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="0a3b9-1614">1.7.0 —апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1614">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0a3b9-1615">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1615">Highlights since the last major release</span></span>
* <span data-ttu-id="0a3b9-1616">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1616">General availability of `Az` module</span></span>
* <span data-ttu-id="0a3b9-1617">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1617">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="0a3b9-1618">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1618">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="0a3b9-1619">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1619">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="0a3b9-1620">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1620">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0a3b9-1621">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1621">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="0a3b9-1622">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1622">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0a3b9-1623">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1623">Az.Accounts</span></span>
* <span data-ttu-id="0a3b9-1624">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметр AzureAnalysisServicesEndpointResourceId.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1624">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="0a3b9-1625">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1625">Az.AnalysisServices</span></span>
* <span data-ttu-id="0a3b9-1626">Использование ServiceClient в командлетах плоскости данных и удаление исходной логики проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1626">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="0a3b9-1627">Add-AzureASAccount используется как оболочка для Connect-AzAccount во избежание критических изменений.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1627">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0a3b9-1628">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1628">Az.Automation</span></span>
* <span data-ttu-id="0a3b9-1629">Исправлена ошибка командлета New-AzAutomationSoftwareUpdateConfiguration, связанная с включением.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1629">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="0a3b9-1630">Теперь параметры IncludedKbNumber и IncludedPackageNameMask должны работать нормально.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1630">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="0a3b9-1631">Исправлена ошибка динамической группы управления обновлениями службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1631">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a3b9-1632">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1632">Az.Compute</span></span>
* <span data-ttu-id="0a3b9-1633">В командлеты New-AzDiskConfig и New-AzSnapshotConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1633">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="0a3b9-1634">Теперь можно создавать виртуальные машину на основе образов из коллекции от других клиентов.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1634">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="0a3b9-1635">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1635">Az.ContainerInstance</span></span>
* <span data-ttu-id="0a3b9-1636">Исправлена проблема в параметре -Command командлета New-AzContainerGroup, из-за которой в конце добавлялся пустой аргумент.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1636">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a3b9-1637">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1637">Az.DataFactory</span></span>
* <span data-ttu-id="0a3b9-1638">Пакет SDK для ADF .NET обновлен до версии 3.0.2.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1638">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="0a3b9-1639">Командлет Set-AzDataFactoryV2 обновлен с помощью дополнительных параметров для настроек, связанных с RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1639">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a3b9-1640">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1640">Az.Resources</span></span>
* <span data-ttu-id="0a3b9-1641">Улучшена обработка поставщиков Get-AzResource при предоставлении параметров -ResourceId или -ResourceGroupName, -Name и -ResourceType.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1641">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="0a3b9-1642">Улучшена обработка ошибок в командлетах Test-AzDeployment и Test-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1642">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="0a3b9-1643">Теперь ошибки, возникающие за пределами проверки развертывания, обрабатываются и включаются в выходные данные команды.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1643">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="0a3b9-1644">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1644">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="0a3b9-1645">Добавлен параметр-переключатель -IgnoreDynamicParameters, с помощью которого можно настроить командлеты развертывания так, чтобы они пропускали запросы в сценариях скриптов и заданий.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1645">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="0a3b9-1646">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1646">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a3b9-1647">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1647">Az.Sql</span></span>
* <span data-ttu-id="0a3b9-1648">Поддержка классификации данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1648">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a3b9-1649">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1649">Az.Storage</span></span>
* <span data-ttu-id="0a3b9-1650">Подробные сообщения об ошибке передаются при создании контекста хранилища с помощью параметра -UseConnectedAccount, но без входа в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1650">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="0a3b9-1651">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1651">New-AzStorageContext</span></span>
* <span data-ttu-id="0a3b9-1652">Поддержка свойств службы управления BLOB-объектов в указанной учетной записи хранения с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1652">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="0a3b9-1653">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1653">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="0a3b9-1654">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1654">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="0a3b9-1655">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1655">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="0a3b9-1656">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1656">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="0a3b9-1657">Поддержка параметра -AsJob в командлетах для отправки и скачивания больших двоичных объектов и файлов.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1657">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="0a3b9-1658">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1658">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="0a3b9-1659">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1659">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="0a3b9-1660">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1660">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="0a3b9-1661">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1661">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="0a3b9-1662">1.6.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1662">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0a3b9-1663">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1663">Highlights since the last major release</span></span>
* <span data-ttu-id="0a3b9-1664">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1664">General availability of `Az` module</span></span>
* <span data-ttu-id="0a3b9-1665">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1665">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="0a3b9-1666">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1666">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="0a3b9-1667">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1667">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="0a3b9-1668">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1668">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0a3b9-1669">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1669">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="0a3b9-1670">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1670">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0a3b9-1671">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1671">Az.Automation</span></span>
* <span data-ttu-id="0a3b9-1672">В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1672">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="0a3b9-1673">динамическое группирование;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1673">Dynamic grouping</span></span>
    * <span data-ttu-id="0a3b9-1674">скрипты предварительного или последующего выполнения;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1674">Pre-Post script</span></span>
    * <span data-ttu-id="0a3b9-1675">параметр перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1675">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a3b9-1676">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1676">Az.Compute</span></span>
* <span data-ttu-id="0a3b9-1677">Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1677">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="0a3b9-1678">Обновление клиентской библиотеки вычислений до версии 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1678">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0a3b9-1679">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1679">Az.KeyVault</span></span>
* <span data-ttu-id="0a3b9-1680">Добавлена поддержка подстановочных знаков в командлетах KeyVault.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1680">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a3b9-1681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1681">Az.Network</span></span>
* <span data-ttu-id="0a3b9-1682">Добавлена поддержка анализа угроз для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1682">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="0a3b9-1683">Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1683">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a3b9-1684">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1684">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a3b9-1685">В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1685">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="0a3b9-1686">Добавлена поддержка канала для отмены регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1686">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a3b9-1687">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1687">Az.Resources</span></span>
* <span data-ttu-id="0a3b9-1688">Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1688">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="0a3b9-1689">Обновлены учетные данные, используемые при общих вызовах к ARM.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1689">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a3b9-1690">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1690">Az.Sql</span></span>
* <span data-ttu-id="0a3b9-1691">Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1691">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a3b9-1692">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1692">Az.Storage</span></span>
* <span data-ttu-id="0a3b9-1693">Поддержка получения, настройки и удаления политики управления в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1693">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="0a3b9-1694">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1694">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="0a3b9-1695">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1695">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="0a3b9-1696">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1696">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="0a3b9-1697">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1697">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="0a3b9-1698">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1698">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="0a3b9-1699">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1699">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a3b9-1700">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1700">Az.Websites</span></span>
* <span data-ttu-id="0a3b9-1701">Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1701">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="0a3b9-1702">1.5.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1702">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0a3b9-1703">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1703">Az.Accounts</span></span>
* <span data-ttu-id="0a3b9-1704">Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1704">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="0a3b9-1705">Обновлены примеры для Connect AzAccount.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1705">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0a3b9-1706">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1706">Az.Automation</span></span>
* <span data-ttu-id="0a3b9-1707">Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1707">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="0a3b9-1708">Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1708">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="0a3b9-1709">Теперь он возвращает все узлы.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1709">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0a3b9-1710">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1710">Az.Cdn</span></span>
* <span data-ttu-id="0a3b9-1711">Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1711">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a3b9-1712">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1712">Az.Compute</span></span>
* <span data-ttu-id="0a3b9-1713">Добавлена поддержка подстановочных знаков в командлетах Get.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1713">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a3b9-1714">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1714">Az.DataFactory</span></span>
* <span data-ttu-id="0a3b9-1715">Обновлен пакет SDK для ADF .NET до версии 3.0.1.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1715">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0a3b9-1716">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1716">Az.LogicApp</span></span>
* <span data-ttu-id="0a3b9-1717">Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1717">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a3b9-1718">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1718">Az.Network</span></span>
* <span data-ttu-id="0a3b9-1719">Добавлена поддержка подстановочных знаков в командлетах Network.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1719">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a3b9-1720">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1720">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a3b9-1721">Добавлена поддержка SQL Server на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1721">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="0a3b9-1722">Обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1722">SDK Update</span></span>
* <span data-ttu-id="0a3b9-1723">Удалена проверка VMappContainer в Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1723">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="0a3b9-1724">Добавлены параметры Name и ServerName для Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1724">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a3b9-1725">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1725">Az.Resources</span></span>
* <span data-ttu-id="0a3b9-1726">Добавлен параметр `-TemplateObject` в командлеты для развертывания.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1726">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="0a3b9-1727">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1727">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="0a3b9-1728">Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1728">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="0a3b9-1729">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1729">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="0a3b9-1730">Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1730">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="0a3b9-1731">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1731">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a3b9-1732">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1732">Az.Sql</span></span>
* <span data-ttu-id="0a3b9-1733">Обновление AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1733">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="0a3b9-1734">Исправлено поведение для пограничного случая при создании параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1734">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a3b9-1735">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1735">Az.Storage</span></span>
* <span data-ttu-id="0a3b9-1736">Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1736">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="0a3b9-1737">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1737">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="0a3b9-1738">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1738">Az.AnalysisServices</span></span>
* <span data-ttu-id="0a3b9-1739">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1739">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0a3b9-1740">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1740">Az.Automation</span></span>
* <span data-ttu-id="0a3b9-1741">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1741">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="0a3b9-1742">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1742">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="0a3b9-1743">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1743">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0a3b9-1744">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1744">Az.CognitiveServices</span></span>
* <span data-ttu-id="0a3b9-1745">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1745">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a3b9-1746">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1746">Az.Compute</span></span>
* <span data-ttu-id="0a3b9-1747">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1747">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="0a3b9-1748">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1748">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="0a3b9-1749">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1749">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="0a3b9-1750">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1750">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0a3b9-1751">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1751">Az.DataLakeStore</span></span>
* <span data-ttu-id="0a3b9-1752">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1752">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0a3b9-1753">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1753">Az.EventHub</span></span>
* <span data-ttu-id="0a3b9-1754">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1754">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0a3b9-1755">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1755">Az.KeyVault</span></span>
* <span data-ttu-id="0a3b9-1756">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1756">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0a3b9-1757">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1757">Az.LogicApp</span></span>
* <span data-ttu-id="0a3b9-1758">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1758">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="0a3b9-1759">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1759">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="0a3b9-1760">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1760">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="0a3b9-1761">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1761">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="0a3b9-1762">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1762">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="0a3b9-1763">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1763">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="0a3b9-1764">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1764">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="0a3b9-1765">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1765">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="0a3b9-1766">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1766">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="0a3b9-1767">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1767">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="0a3b9-1768">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1768">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="0a3b9-1769">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1769">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="0a3b9-1770">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1770">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0a3b9-1771">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1771">Az.Monitor</span></span>
* <span data-ttu-id="0a3b9-1772">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1772">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a3b9-1773">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1773">Az.Network</span></span>
* <span data-ttu-id="0a3b9-1774">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1774">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0a3b9-1775">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1775">Az.OperationalInsights</span></span>
* <span data-ttu-id="0a3b9-1776">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1776">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="0a3b9-1777">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1777">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="0a3b9-1778">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1778">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a3b9-1779">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1779">Az.Resources</span></span>
* <span data-ttu-id="0a3b9-1780">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1780">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="0a3b9-1781">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1781">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="0a3b9-1782">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1782">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="0a3b9-1783">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1783">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a3b9-1784">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1784">Az.Sql</span></span>
* <span data-ttu-id="0a3b9-1785">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1785">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="0a3b9-1786">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1786">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a3b9-1787">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1787">Az.Websites</span></span>
* <span data-ttu-id="0a3b9-1788">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1788">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="0a3b9-1789">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1789">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0a3b9-1790">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1790">Az.Accounts</span></span>
* <span data-ttu-id="0a3b9-1791">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1791">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="0a3b9-1792">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1792">Az.AnalysisServices</span></span>
<span data-ttu-id="0a3b9-1793">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1793">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a3b9-1794">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1794">Az.Compute</span></span>
* <span data-ttu-id="0a3b9-1795">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1795">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="0a3b9-1796">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1796">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="0a3b9-1797">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1797">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a3b9-1798">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1798">Az.RecoveryServices</span></span>
<span data-ttu-id="0a3b9-1799">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1799">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a3b9-1800">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1800">Az.Resources</span></span>
* <span data-ttu-id="0a3b9-1801">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1801">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="0a3b9-1802">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1802">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="0a3b9-1803">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1803">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="0a3b9-1804">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1804">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a3b9-1805">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1805">Az.Sql</span></span>
* <span data-ttu-id="0a3b9-1806">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1806">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="0a3b9-1807">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1807">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="0a3b9-1808">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1808">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="0a3b9-1809">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1809">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0a3b9-1810">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1810">Az.Accounts</span></span>
* <span data-ttu-id="0a3b9-1811">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1811">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="0a3b9-1812">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1812">Az.AnalysisServices</span></span>
* <span data-ttu-id="0a3b9-1813">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1813">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a3b9-1814">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1814">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a3b9-1815">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1815">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="0a3b9-1816">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1816">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0a3b9-1817">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1817">Az.Accounts</span></span>
* <span data-ttu-id="0a3b9-1818">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1818">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0a3b9-1819">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1819">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0a3b9-1820">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1820">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="0a3b9-1821">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1821">Az.Aks</span></span>
* <span data-ttu-id="0a3b9-1822">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1822">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0a3b9-1823">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1823">Az.Automation</span></span>
* <span data-ttu-id="0a3b9-1824">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1824">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="0a3b9-1825">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1825">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0a3b9-1826">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1826">Az.Cdn</span></span>
* <span data-ttu-id="0a3b9-1827">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1827">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a3b9-1828">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1828">Az.Compute</span></span>
* <span data-ttu-id="0a3b9-1829">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1829">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="0a3b9-1830">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1830">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="0a3b9-1831">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1831">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="0a3b9-1832">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1832">Az.ContainerRegistry</span></span>
* <span data-ttu-id="0a3b9-1833">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1833">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a3b9-1834">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1834">Az.DataFactory</span></span>
* <span data-ttu-id="0a3b9-1835">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1835">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0a3b9-1836">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1836">Az.DataLakeStore</span></span>
* <span data-ttu-id="0a3b9-1837">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1837">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="0a3b9-1838">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1838">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="0a3b9-1839">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1839">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0a3b9-1840">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1840">Az.IotHub</span></span>
* <span data-ttu-id="0a3b9-1841">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1841">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0a3b9-1842">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1842">Az.KeyVault</span></span>
* <span data-ttu-id="0a3b9-1843">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1843">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a3b9-1844">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1844">Az.Network</span></span>
* <span data-ttu-id="0a3b9-1845">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1845">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a3b9-1846">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1846">Az.Resources</span></span>
* <span data-ttu-id="0a3b9-1847">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1847">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="0a3b9-1848">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1848">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="0a3b9-1849">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1849">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="0a3b9-1850">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1850">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="0a3b9-1851">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1851">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="0a3b9-1852">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1852">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="0a3b9-1853">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1853">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0a3b9-1854">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1854">Az.ServiceFabric</span></span>
* <span data-ttu-id="0a3b9-1855">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1855">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="0a3b9-1856">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1856">Fix some error messages.</span></span>
* <span data-ttu-id="0a3b9-1857">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1857">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="0a3b9-1858">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1858">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="0a3b9-1859">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1859">Az.SignalR</span></span>
* <span data-ttu-id="0a3b9-1860">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1860">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a3b9-1861">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1861">Az.Sql</span></span>
* <span data-ttu-id="0a3b9-1862">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1862">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0a3b9-1863">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1863">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="0a3b9-1864">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1864">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="0a3b9-1865">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1865">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a3b9-1866">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1866">Az.Storage</span></span>
* <span data-ttu-id="0a3b9-1867">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1867">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0a3b9-1868">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1868">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="0a3b9-1869">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1869">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="0a3b9-1870">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1870">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="0a3b9-1871">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1871">Az.TrafficManager</span></span>
* <span data-ttu-id="0a3b9-1872">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1872">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a3b9-1873">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1873">Az.Websites</span></span>
* <span data-ttu-id="0a3b9-1874">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1874">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0a3b9-1875">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1875">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="0a3b9-1876">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1876">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="0a3b9-1877">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1877">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0a3b9-1878">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1878">Az.Accounts</span></span>
* <span data-ttu-id="0a3b9-1879">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1879">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a3b9-1880">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1880">Az.Compute</span></span>
* <span data-ttu-id="0a3b9-1881">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1881">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="0a3b9-1882">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1882">Updated the description of ID in help files</span></span>
* <span data-ttu-id="0a3b9-1883">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1883">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0a3b9-1884">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1884">Az.DataLakeStore</span></span>
* <span data-ttu-id="0a3b9-1885">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1885">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="0a3b9-1886">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1886">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="0a3b9-1887">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1887">Az.EventGrid</span></span>
* <span data-ttu-id="0a3b9-1888">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1888">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="0a3b9-1889">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1889">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="0a3b9-1890">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1890">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="0a3b9-1891">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1891">Event Time-To-Live,</span></span>
        - <span data-ttu-id="0a3b9-1892">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1892">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="0a3b9-1893">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1893">Dead letter endpoint.</span></span>
    - <span data-ttu-id="0a3b9-1894">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1894">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="0a3b9-1895">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1895">Event Time-To-Live,</span></span>
        - <span data-ttu-id="0a3b9-1896">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1896">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="0a3b9-1897">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1897">Dead letter endpoint.</span></span>
* <span data-ttu-id="0a3b9-1898">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1898">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="0a3b9-1899">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1899">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0a3b9-1900">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1900">Az.IotHub</span></span>
* <span data-ttu-id="0a3b9-1901">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1901">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0a3b9-1902">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1902">Az.LogicApp</span></span>
* <span data-ttu-id="0a3b9-1903">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1903">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a3b9-1904">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1904">Az.Resources</span></span>
* <span data-ttu-id="0a3b9-1905">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1905">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="0a3b9-1906">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1906">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="0a3b9-1907">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1907">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="0a3b9-1908">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1908">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="0a3b9-1909">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1909">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="0a3b9-1910">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1910">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="0a3b9-1911">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1911">Az.SignalR</span></span>
* <span data-ttu-id="0a3b9-1912">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1912">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a3b9-1913">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1913">Az.Sql</span></span>
* <span data-ttu-id="0a3b9-1914">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1914">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a3b9-1915">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1915">Az.Storage</span></span>
* <span data-ttu-id="0a3b9-1916">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1916">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="0a3b9-1917">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1917">New-AzStorageContext</span></span>
* <span data-ttu-id="0a3b9-1918">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1918">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="0a3b9-1919">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1919">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a3b9-1920">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1920">Az.Websites</span></span>
* <span data-ttu-id="0a3b9-1921">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1921">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="0a3b9-1922">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1922">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="0a3b9-1923">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1923">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="0a3b9-1924">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1924">General</span></span>

- <span data-ttu-id="0a3b9-1925">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1925">General Availability of Az Module</span></span>
- <span data-ttu-id="0a3b9-1926">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1926">Online help for each module</span></span>
- <span data-ttu-id="0a3b9-1927">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1927">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="0a3b9-1928">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1928">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="0a3b9-1929">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1929">Az.Accounts</span></span>
- <span data-ttu-id="0a3b9-1930">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1930">Changed from Az.Profile</span></span>
- <span data-ttu-id="0a3b9-1931">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1931">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="0a3b9-1932">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1932">Az.ApiManagement</span></span>
- <span data-ttu-id="0a3b9-1933">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1933">Fixes for #7002</span></span>
- <span data-ttu-id="0a3b9-1934">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1934">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="0a3b9-1935">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1935">Az.Batch</span></span>
- <span data-ttu-id="0a3b9-1936">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1936">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="0a3b9-1937">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1937">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="0a3b9-1938">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1938">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="0a3b9-1939">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1939">Az.Billing</span></span>
- <span data-ttu-id="0a3b9-1940">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1940">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="0a3b9-1941">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1941">Az.CognitivServices</span></span>
- <span data-ttu-id="0a3b9-1942">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1942">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="0a3b9-1943">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1943">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="0a3b9-1944">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1944">Az.ContainerInstance</span></span>
- <span data-ttu-id="0a3b9-1945">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1945">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="0a3b9-1946">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1946">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="0a3b9-1947">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1947">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="0a3b9-1948">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1948">Az.DataLakeStore</span></span>
- <span data-ttu-id="0a3b9-1949">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1949">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="0a3b9-1950">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1950">Az.Monitor</span></span>
- <span data-ttu-id="0a3b9-1951">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1951">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="0a3b9-1952">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1952">Az.KeyVault</span></span>
- <span data-ttu-id="0a3b9-1953">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1953">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="0a3b9-1954">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1954">Az.MachineLearning</span></span>
- <span data-ttu-id="0a3b9-1955">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1955">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="0a3b9-1956">Az.Media</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1956">Az.Media</span></span>
- <span data-ttu-id="0a3b9-1957">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1957">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="0a3b9-1958">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1958">Az.Network</span></span>
<span data-ttu-id="0a3b9-1959">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1959">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="0a3b9-1960">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1960">New cmdlets added:</span></span>
        - <span data-ttu-id="0a3b9-1961">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1961">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0a3b9-1962">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1962">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0a3b9-1963">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1963">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0a3b9-1964">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1964">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0a3b9-1965">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1965">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0a3b9-1966">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1966">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="0a3b9-1967">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1967">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="0a3b9-1968">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1968">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="0a3b9-1969">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1969">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="0a3b9-1970">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1970">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="0a3b9-1971">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1971">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="0a3b9-1972">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1972">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="0a3b9-1973">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1973">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="0a3b9-1974">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1974">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="0a3b9-1975">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1975">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="0a3b9-1976">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1976">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="0a3b9-1977">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1977">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="0a3b9-1978">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1978">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="0a3b9-1979">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1979">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="0a3b9-1980">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1980">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="0a3b9-1981">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1981">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="0a3b9-1982">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1982">Az.OperationalInsights</span></span>
- <span data-ttu-id="0a3b9-1983">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1983">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="0a3b9-1984">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1984">Az.Profile</span></span>
- <span data-ttu-id="0a3b9-1985">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1985">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="0a3b9-1986">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1986">Az.RecoveryServices</span></span>
- <span data-ttu-id="0a3b9-1987">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1987">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="0a3b9-1988">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1988">Az.Resources</span></span>
- <span data-ttu-id="0a3b9-1989">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1989">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="0a3b9-1990">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1990">Az.ServiceFabric</span></span>
- <span data-ttu-id="0a3b9-1991">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1991">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="0a3b9-1992">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1992">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="0a3b9-1993">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1993">Az.SIgnalR</span></span>
- <span data-ttu-id="0a3b9-1994">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1994">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="0a3b9-1995">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1995">Az.Sql</span></span>
- <span data-ttu-id="0a3b9-1996">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1996">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="0a3b9-1997">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1997">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="0a3b9-1998">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1998">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="0a3b9-1999">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a3b9-1999">Az.Storage</span></span>
- <span data-ttu-id="0a3b9-2000">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2000">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="0a3b9-2001">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2001">Az.Websites</span></span>
- <span data-ttu-id="0a3b9-2002">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2002">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="0a3b9-2003">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2003">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="0a3b9-2004">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2004">General</span></span>

* <span data-ttu-id="0a3b9-2005">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2005">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="0a3b9-2006">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2006">Az.Compute</span></span>

* <span data-ttu-id="0a3b9-2007">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2007">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="0a3b9-2008">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2008">Az.DataLakeStore</span></span>

* <span data-ttu-id="0a3b9-2009">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2009">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="0a3b9-2010">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2010">Az.FrontDoor</span></span>

* <span data-ttu-id="0a3b9-2011">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2011">Fixed some broken links</span></span>
    - <span data-ttu-id="0a3b9-2012">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2012">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="0a3b9-2013">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2013">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="0a3b9-2014">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2014">Az.RecoveryServices</span></span>

* <span data-ttu-id="0a3b9-2015">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2015">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="0a3b9-2016">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2016">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="0a3b9-2017">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2017">Az.Resources</span></span>

* <span data-ttu-id="0a3b9-2018">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2018">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="0a3b9-2019">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2019">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="0a3b9-2020">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2020">Az.Sql</span></span>

* <span data-ttu-id="0a3b9-2021">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2021">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="0a3b9-2022">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2022">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="0a3b9-2023">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2023">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="0a3b9-2024">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2024">Az.Storage</span></span>

* <span data-ttu-id="0a3b9-2025">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2025">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="0a3b9-2026">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2026">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="0a3b9-2027">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2027">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="0a3b9-2028">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2028">Support Static Website configuration</span></span>
    - <span data-ttu-id="0a3b9-2029">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2029">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="0a3b9-2030">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2030">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="0a3b9-2031">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2031">Az.Websites</span></span>

* <span data-ttu-id="0a3b9-2032">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2032">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="0a3b9-2033">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2033">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="0a3b9-2034">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2034">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="0a3b9-2035">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2035">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="0a3b9-2036">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2036">Az.ApiManagement</span></span>
* <span data-ttu-id="0a3b9-2037">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2037">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="0a3b9-2038">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2038">Az.Automation</span></span>
* <span data-ttu-id="0a3b9-2039">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2039">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="0a3b9-2040">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2040">Added Update Management cmdlets</span></span>
* <span data-ttu-id="0a3b9-2041">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2041">Added Source Control cmdlets</span></span>
* <span data-ttu-id="0a3b9-2042">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2042">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="0a3b9-2043">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2043">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="0a3b9-2044">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2044">Az.Compute</span></span>
* <span data-ttu-id="0a3b9-2045">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2045">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="0a3b9-2046">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2046">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="0a3b9-2047">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2047">Az.ContainerInstance</span></span>
* <span data-ttu-id="0a3b9-2048">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2048">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="0a3b9-2049">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2049">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="0a3b9-2050">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2050">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="0a3b9-2051">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2051">Az.Network</span></span>
* <span data-ttu-id="0a3b9-2052">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2052">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="0a3b9-2053">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2053">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="0a3b9-2054">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2054">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="0a3b9-2055">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2055">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="0a3b9-2056">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2056">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="0a3b9-2057">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2057">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="0a3b9-2058">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2058">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="0a3b9-2059">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2059">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="0a3b9-2060">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2060">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="0a3b9-2061">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2061">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="0a3b9-2062">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2062">Az.Relay</span></span>
* <span data-ttu-id="0a3b9-2063">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2063">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="0a3b9-2064">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2064">Az.Resources</span></span>
* <span data-ttu-id="0a3b9-2065">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2065">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="0a3b9-2066">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2066">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="0a3b9-2067">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2067">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="0a3b9-2068">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2068">Az.ServiceFabric</span></span>
* <span data-ttu-id="0a3b9-2069">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2069">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="0a3b9-2070">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2070">Az.Sql</span></span>
* <span data-ttu-id="0a3b9-2071">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2071">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="0a3b9-2072">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2072">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0a3b9-2073">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2073">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0a3b9-2074">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2074">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0a3b9-2075">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2075">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0a3b9-2076">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2076">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="0a3b9-2077">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2077">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="0a3b9-2078">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2078">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="0a3b9-2079">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2079">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="0a3b9-2080">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2080">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="0a3b9-2081">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2081">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="0a3b9-2082">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2082">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="0a3b9-2083">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2083">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="0a3b9-2084">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2084">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="0a3b9-2085">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2085">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="0a3b9-2086">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2086">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="0a3b9-2087">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2087">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="0a3b9-2088">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2088">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="0a3b9-2089">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2089">General</span></span>
* <span data-ttu-id="0a3b9-2090">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2090">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="0a3b9-2091">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2091">Az.Profile</span></span>
* <span data-ttu-id="0a3b9-2092">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2092">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="0a3b9-2093">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2093">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="0a3b9-2094">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2094">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="0a3b9-2095">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2095">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="0a3b9-2096">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2096">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="0a3b9-2097">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2097">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="0a3b9-2098">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2098">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="0a3b9-2099">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2099">Az.CognitiveServices</span></span>
* <span data-ttu-id="0a3b9-2100">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2100">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a3b9-2101">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2101">Az.Compute</span></span>
* <span data-ttu-id="0a3b9-2102">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2102">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="0a3b9-2103">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2103">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="0a3b9-2104">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2104">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0a3b9-2105">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2105">Az.DataLakeStore</span></span>
* <span data-ttu-id="0a3b9-2106">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2106">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="0a3b9-2107">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2107">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="0a3b9-2108">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2108">Az.Insights</span></span>
* <span data-ttu-id="0a3b9-2109">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2109">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="0a3b9-2110">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2110">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="0a3b9-2111">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2111">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="0a3b9-2112">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2112">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a3b9-2113">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2113">Az.Network</span></span>
* <span data-ttu-id="0a3b9-2114">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2114">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="0a3b9-2115">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2115">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="0a3b9-2116">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2116">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="0a3b9-2117">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2117">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="0a3b9-2118">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2118">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="0a3b9-2119">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2119">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="0a3b9-2120">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2120">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0a3b9-2121">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2121">Az.PolicyInsights</span></span>
* <span data-ttu-id="0a3b9-2122">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2122">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a3b9-2123">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2123">Az.Resources</span></span>
* <span data-ttu-id="0a3b9-2124">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2124">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="0a3b9-2125">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2125">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0a3b9-2126">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2126">Az.ServiceBus</span></span>
* <span data-ttu-id="0a3b9-2127">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2127">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0a3b9-2128">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2128">Az.ServiceFabric</span></span>
* <span data-ttu-id="0a3b9-2129">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2129">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="0a3b9-2130">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2130">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="0a3b9-2131">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2131">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="0a3b9-2132">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2132">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="0a3b9-2133">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2133">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="0a3b9-2134">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2134">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="0a3b9-2135">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2135">Az.Profile</span></span>
* <span data-ttu-id="0a3b9-2136">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2136">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="0a3b9-2137">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2137">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a3b9-2138">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2138">Az.Compute</span></span>
* <span data-ttu-id="0a3b9-2139">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2139">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="0a3b9-2140">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2140">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0a3b9-2141">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2141">Az.DataLakeStore</span></span>
* <span data-ttu-id="0a3b9-2142">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2142">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="0a3b9-2143">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2143">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="0a3b9-2144">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2144">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="0a3b9-2145">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2145">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="0a3b9-2146">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2146">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a3b9-2147">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2147">Az.Network</span></span>
* <span data-ttu-id="0a3b9-2148">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2148">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="0a3b9-2149">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2149">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a3b9-2150">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2150">Az.Resources</span></span>
* <span data-ttu-id="0a3b9-2151">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2151">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="0a3b9-2152">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2152">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="0a3b9-2153">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2153">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="0a3b9-2154">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2154">Azure.Storage</span></span>
* <span data-ttu-id="0a3b9-2155">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2155">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="0a3b9-2156">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2156">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="0a3b9-2157">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2157">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="0a3b9-2158">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2158">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="0a3b9-2159">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2159">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0a3b9-2160">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2160">Az.CognitiveServices</span></span>
* <span data-ttu-id="0a3b9-2161">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2161">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a3b9-2162">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2162">Az.Compute</span></span>
* <span data-ttu-id="0a3b9-2163">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2163">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="0a3b9-2164">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2164">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="0a3b9-2165">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2165">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="0a3b9-2166">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2166">Az.DataFactoryV2</span></span>
* <span data-ttu-id="0a3b9-2167">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2167">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a3b9-2168">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2168">Az.Network</span></span>
* <span data-ttu-id="0a3b9-2169">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2169">Added NetworkProfile functionality.</span></span> <span data-ttu-id="0a3b9-2170">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2170">new cmdlets added</span></span>
    - <span data-ttu-id="0a3b9-2171">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2171">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="0a3b9-2172">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2172">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="0a3b9-2173">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2173">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="0a3b9-2174">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2174">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="0a3b9-2175">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2175">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="0a3b9-2176">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2176">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="0a3b9-2177">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2177">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="0a3b9-2178">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2178">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="0a3b9-2179">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2179">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="0a3b9-2180">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2180">Az.RedisCache</span></span>
* <span data-ttu-id="0a3b9-2181">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2181">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="0a3b9-2182">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2182">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a3b9-2183">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2183">Az.Resources</span></span>
* <span data-ttu-id="0a3b9-2184">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2184">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="0a3b9-2185">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2185">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a3b9-2186">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2186">Az.Sql</span></span>
* <span data-ttu-id="0a3b9-2187">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2187">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a3b9-2188">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2188">Az.Websites</span></span>
* <span data-ttu-id="0a3b9-2189">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2189">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="0a3b9-2190">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2190">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="0a3b9-2191">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2191">0.2.0 - September 2018</span></span>
 <span data-ttu-id="0a3b9-2192">Начальный выпуск</span><span class="sxs-lookup"><span data-stu-id="0a3b9-2192">Initial Release</span></span>
