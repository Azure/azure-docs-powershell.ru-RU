---
title: Заметки о выпуске Azure PowerShell
description: Узнайте обо всех последних обновлениях модулей Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/09/2020
ms.openlocfilehash: 81afcd63e5ca7a776965849de9090b833f49acc7
ms.sourcegitcommit: a321ef9d134c684fa24ababcbd898f86b00d9364
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "77477239"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="6c394-103">Заметки о выпуске Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="6c394-103">Azure PowerShell release notes</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="6c394-104">3.5.0 — февраль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="6c394-104">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6c394-105">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="6c394-105">Highlights since the last major release</span></span>
* <span data-ttu-id="6c394-106">Обновлены данные телеметрии на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="6c394-106">Updated client side telemetry.</span></span>
* <span data-ttu-id="6c394-107">В Az.IotHub добавлены командлеты для управления устройствами.</span><span class="sxs-lookup"><span data-stu-id="6c394-107">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="6c394-108">В Az.SqlVirtualMachine добавлены командлеты для прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="6c394-108">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6c394-109">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6c394-109">Az.Accounts</span></span>
* <span data-ttu-id="6c394-110">В данные телеметрии на стороне клиента добавлены такие сведения, как идентификатор подписки, идентификатор арендатора и время выполнения.</span><span class="sxs-lookup"><span data-stu-id="6c394-110">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6c394-111">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6c394-111">Az.Automation</span></span>
* <span data-ttu-id="6c394-112">Исправлена опечатка в примере 1 в справочной документации по New-AzAutomationSoftwareUpdateConfiguration.</span><span class="sxs-lookup"><span data-stu-id="6c394-112">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6c394-113">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6c394-113">Az.CognitiveServices</span></span>
* <span data-ttu-id="6c394-114">Обновлен пакет SDK до версии 7.0.</span><span class="sxs-lookup"><span data-stu-id="6c394-114">Updated SDK to 7.0</span></span>
* <span data-ttu-id="6c394-115">Улучшено сообщение об ошибке, которое появляется, если ответы сервера не содержат текст.</span><span class="sxs-lookup"><span data-stu-id="6c394-115">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6c394-116">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6c394-116">Az.Compute</span></span>
* <span data-ttu-id="6c394-117">Разрешено использовать пустое значение для ProximityPlacementGroupId во время обновления.</span><span class="sxs-lookup"><span data-stu-id="6c394-117">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6c394-118">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6c394-118">Az.FrontDoor</span></span>
* <span data-ttu-id="6c394-119">Добавлен командлет для получения определений управляемых правил, которые могут использоваться в WAF.</span><span class="sxs-lookup"><span data-stu-id="6c394-119">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6c394-120">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6c394-120">Az.IotHub</span></span>
* <span data-ttu-id="6c394-121">Добавлена возможность управления устройствами в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="6c394-121">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="6c394-122">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="6c394-122">New Cmdlets are:</span></span>
    - <span data-ttu-id="6c394-123">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="6c394-123">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="6c394-124">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="6c394-124">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="6c394-125">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="6c394-125">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="6c394-126">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="6c394-126">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6c394-127">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6c394-127">Az.KeyVault</span></span>
* <span data-ttu-id="6c394-128">Устранен дублирующийся текст для Add-AzKeyVaultKey.md.</span><span class="sxs-lookup"><span data-stu-id="6c394-128">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6c394-129">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6c394-129">Az.Monitor</span></span>
* <span data-ttu-id="6c394-130">Исправлено описание командлета Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="6c394-130">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="6c394-131">В команду New-AzMetricAlertRuleV2 добавлен новый параметр ActionGroupId.</span><span class="sxs-lookup"><span data-stu-id="6c394-131">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="6c394-132">Пользователь может предоставить ActionGroupId(string) или ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="6c394-132">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6c394-133">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6c394-133">Az.Network</span></span>
* <span data-ttu-id="6c394-134">Добавлен еще один параметр -EnableProxyProtocol для командлета New-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="6c394-134">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="6c394-135">Исправлен пример FilterData в Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="6c394-135">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="6c394-136">Добавлен пример Packet Capture для всех внутренних и внешних пакетов в Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="6c394-136">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="6c394-137">Добавлена поддерживаемая политика Брандмауэра Azure в брандмауэрах виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="6c394-137">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="6c394-138">Новые командлеты не добавлены.</span><span class="sxs-lookup"><span data-stu-id="6c394-138">No new cmdlets are added.</span></span> <span data-ttu-id="6c394-139">Снято ограничение политики брандмауэра в брандмауэрах виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="6c394-139">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6c394-140">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6c394-140">Az.RecoveryServices</span></span>
* <span data-ttu-id="6c394-141">Добавлена возможность восстановления в виде файлов для Баз данных SQL.</span><span class="sxs-lookup"><span data-stu-id="6c394-141">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6c394-142">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6c394-142">Az.Resources</span></span>
* <span data-ttu-id="6c394-143">Выполнен рефакторинг командлетов развертывания шаблона.</span><span class="sxs-lookup"><span data-stu-id="6c394-143">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="6c394-144">Добавлены новые командлеты для управления развертываниями в группе управления: \*-AzManagementGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="6c394-144">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="6c394-145">Добавлены новые командлеты для управления развертываниями в области арендатора: \*-AzTenantDeployment.</span><span class="sxs-lookup"><span data-stu-id="6c394-145">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="6c394-146">Выполнен рефакторинг командлетов \*-AzDeployment для работы в области подписки.</span><span class="sxs-lookup"><span data-stu-id="6c394-146">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="6c394-147">Созданы псевдонимы \*-AzSubscriptionDeployment для командлетов \*-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="6c394-147">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="6c394-148">Исправлен командлет Update-AzADApplication, когда параметр AvailableToOtherTenants не задан.</span><span class="sxs-lookup"><span data-stu-id="6c394-148">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="6c394-149">Удален набор параметров ApplicationObjectWithoutCredentialParameterSet, чтобы предотвратить возникновение AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="6c394-149">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="6c394-150">Повторно созданы файлы справки.</span><span class="sxs-lookup"><span data-stu-id="6c394-150">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="6c394-151">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6c394-151">Az.Sql</span></span>
* <span data-ttu-id="6c394-152">Добавлена возможность восстановления точки во времени между подписками в Управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="6c394-152">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="6c394-153">Добавлена возможность изменения существующего поколения оборудования Управляемого экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="6c394-153">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="6c394-154">Исправлены примеры справки Update-AzSqlServerVulnerabilityAssessmentSetting: выходные данные параметра и свойства — EmailAdmins.</span><span class="sxs-lookup"><span data-stu-id="6c394-154">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="6c394-155">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6c394-155">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="6c394-156">Добавлены командлеты для прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="6c394-156">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="6c394-157">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="6c394-157">Az.StorageSync</span></span>
* <span data-ttu-id="6c394-158">В командлете Invoke-AzStorageSyncCompatibilityCheck обновлены поддерживаемые наборы символов.</span><span class="sxs-lookup"><span data-stu-id="6c394-158">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="6c394-159">3.4.0 — февраль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="6c394-159">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6c394-160">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="6c394-160">Highlights since the last major release</span></span>
* <span data-ttu-id="6c394-161">Выпущена первоначальная версия 0.1.0 Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="6c394-161">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="6c394-162">Добавлена поддержка Az.Network ConnectionMonitor V2</span><span class="sxs-lookup"><span data-stu-id="6c394-162">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6c394-163">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6c394-163">Az.Accounts</span></span>
* <span data-ttu-id="6c394-164">Отключить автоматическое сохранение контекста, если AzureRmContext.json недоступен</span><span class="sxs-lookup"><span data-stu-id="6c394-164">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="6c394-165">Обновление ссылки на Azure Powershell Common до предварительной версии 1.3.5</span><span class="sxs-lookup"><span data-stu-id="6c394-165">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6c394-166">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6c394-166">Az.ApiManagement</span></span>
* <span data-ttu-id="6c394-167">**Get-AzApiManagementApiSchema** Исправлено получение схемы Open-API, связанной с API https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="6c394-167">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="6c394-168">**New-AzApiManagementProduct**\* и **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="6c394-168">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="6c394-169">Исправить документацию для https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="6c394-169">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="6c394-170">**Set-AzApiManagementApi** Добавлен пример, показывающий, как обновить ServiceUrl с помощью командлета</span><span class="sxs-lookup"><span data-stu-id="6c394-170">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6c394-171">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6c394-171">Az.Compute</span></span>
* <span data-ttu-id="6c394-172">Ограничение числа состояний виртуальных машин до 100, чтобы избежать регулирования при выполнении Get-AzVM-Status без имени виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6c394-172">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="6c394-173">Добавление обновления командлета -AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="6c394-173">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="6c394-174">Добавление параметров EncryptionType и DiskEncryptionSetId в следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="6c394-174">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="6c394-175">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="6c394-175">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="6c394-176">Добавление параметра ColocationStatus в командлет Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="6c394-176">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6c394-177">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6c394-177">Az.DataFactory</span></span>
* <span data-ttu-id="6c394-178">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.7.0.</span><span class="sxs-lookup"><span data-stu-id="6c394-178">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="6c394-179">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="6c394-179">Az.DeploymentManager</span></span>
* <span data-ttu-id="6c394-180">Добавляет операции LIST для ресурсов</span><span class="sxs-lookup"><span data-stu-id="6c394-180">Adds LIST operations for resources</span></span>
* <span data-ttu-id="6c394-181">Добавляет возможность выполнения операций на этапах Проверки работоспособности</span><span class="sxs-lookup"><span data-stu-id="6c394-181">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6c394-182">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6c394-182">Az.HDInsight</span></span>
* <span data-ttu-id="6c394-183">Исправление ошибки в документе New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="6c394-183">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6c394-184">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6c394-184">Az.KeyVault</span></span>
* <span data-ttu-id="6c394-185">Добавление Псевдонимов имени в атрибут VaultName, чтобы Remove-AzureKeyVault соответствовал New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="6c394-185">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6c394-186">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6c394-186">Az.Network</span></span>
* <span data-ttu-id="6c394-187">В Set-AzNetworkWatcherConfigFlowLog.md добавлен новый пример для демонстрации сценария отключения Аналитики трафика.</span><span class="sxs-lookup"><span data-stu-id="6c394-187">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="6c394-188">Добавление поддержки назначения IP-конфигурации для брандмауэра Azure — выделенная подсеть и общедоступный IP-адрес, которые брандмауэр будет использовать для управления трафиком</span><span class="sxs-lookup"><span data-stu-id="6c394-188">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="6c394-189">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="6c394-189">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="6c394-190">добавлен параметр — ManagementPublicIpAddress (необязательный), который принимает объект общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="6c394-190">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="6c394-191">Добавлен метод SetManagementIpConfiguration для объекта брандмауэра — в качестве входных данных требуется подсеть и общедоступный IP-адрес — имя подсети должно быть "AzureFirewallManagementSubnet"</span><span class="sxs-lookup"><span data-stu-id="6c394-191">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="6c394-192">Исправлены примеры Get-AzNetworkSecurityGroup для отображения примеров для группы безопасности сети (NSG) вместо сетевых интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="6c394-192">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="6c394-193">Исправлена опечатка в команде New-AzVpnSite, которая препятствовала завершению параметра идентификатором ресурса.</span><span class="sxs-lookup"><span data-stu-id="6c394-193">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="6c394-194">Добавлена поддержка конфигурации в наборе действий для правил подстановки URL-адресов в шлюзе приложения.</span><span class="sxs-lookup"><span data-stu-id="6c394-194">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="6c394-195">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="6c394-195">New cmdlets added:</span></span>
        - <span data-ttu-id="6c394-196">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c394-196">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="6c394-197">В следующие командлеты добавлен необязательный параметр — UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c394-197">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="6c394-198">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="6c394-198">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="6c394-199">Добавление поддержки для ресурсов NetworkWatcher ConnectionMonitor версии 2</span><span class="sxs-lookup"><span data-stu-id="6c394-199">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6c394-200">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6c394-200">Az.PolicyInsights</span></span>
* <span data-ttu-id="6c394-201">Поддержка оценки соответствия до определения того, какой ресурс нужно исправить</span><span class="sxs-lookup"><span data-stu-id="6c394-201">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="6c394-202">Добавление параметра "—ResourceDiscoverMode" в Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="6c394-202">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="6c394-203">Добавление командлета Get-AzPolicyMetadata для получения ресурсов метаданных политики</span><span class="sxs-lookup"><span data-stu-id="6c394-203">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="6c394-204">Get-AzPolicyState и Get-AzPolicyStateSummary обновлены для API версии 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="6c394-204">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6c394-205">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6c394-205">Az.RecoveryServices</span></span>
* <span data-ttu-id="6c394-206">Поддержка Azure Site Recovery для удаления реплицированного диска.</span><span class="sxs-lookup"><span data-stu-id="6c394-206">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="6c394-207">В Azure Backup добавлена ​​поддержка добавления тегов при создании Хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="6c394-207">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6c394-208">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6c394-208">Az.Resources</span></span>
* <span data-ttu-id="6c394-209">Сделайте команду "Область" необязательной в командлетах \*—AzPolicyAssignment с настройкой по умолчанию для контекстной подписки</span><span class="sxs-lookup"><span data-stu-id="6c394-209">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="6c394-210">Добавление примеров создания ADServicePrincipal с паролем и ключом учетных данных</span><span class="sxs-lookup"><span data-stu-id="6c394-210">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="6c394-211">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6c394-211">Az.Sql</span></span>
<span data-ttu-id="6c394-212">Исправление командлета New-AzSqlDatabaseSecondary, чтобы проверить существование PartnerDatabaseName, а не DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="6c394-212">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6c394-213">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6c394-213">Az.Storage</span></span>
* <span data-ttu-id="6c394-214">Поддержка набора шифрования типа ключа таблиц и очередей в создании учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="6c394-214">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="6c394-215">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6c394-215">New-AzStorageAccount</span></span>
* <span data-ttu-id="6c394-216">Представление RequestId, если StorageException не имеет ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="6c394-216">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="6c394-217">Исправление примера 6 командлета Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6c394-217">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6c394-218">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6c394-218">Az.Websites</span></span>
* <span data-ttu-id="6c394-219">Set-AzWebapp и Set-AzWebappSlot поддерживают свойства AlwaysOn, MinTls и FtpsState</span><span class="sxs-lookup"><span data-stu-id="6c394-219">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="6c394-220">Устранение проблемы, при которой параметр HttpsOnly с одновременным изменением AppservicePlan с помощью одной команды Set-AzWebApp сбрасывал значение HttpsOnly до значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="6c394-220">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="6c394-221">3.3.0 — январь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="6c394-221">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6c394-222">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6c394-222">Az.Accounts</span></span>
* <span data-ttu-id="6c394-223">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment: теперь они принимают параметры AzureAttestationServiceEndpointResourceId и AzureAttestationServiceEndpointSuffix.</span><span class="sxs-lookup"><span data-stu-id="6c394-223">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6c394-224">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6c394-224">Az.Cdn</span></span>
* <span data-ttu-id="6c394-225">Теперь в командлете New-AzCdnEndpoint отображаются сведения из сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="6c394-225">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6c394-226">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6c394-226">Az.Compute</span></span>
* <span data-ttu-id="6c394-227">Командлет Set-AzVMCustomScriptExtension исправлен для виртуальной машины с управляемым диском ОС без профиля ОС.</span><span class="sxs-lookup"><span data-stu-id="6c394-227">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="6c394-228">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6c394-228">Az.ContainerInstance</span></span>
* <span data-ttu-id="6c394-229">Исправлены имена параметров, используемые в примере командлета New-AzContainerGroup.</span><span class="sxs-lookup"><span data-stu-id="6c394-229">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="6c394-230">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="6c394-230">Az.DataBoxEdge</span></span>
* <span data-ttu-id="6c394-231">Добавлен командлет Get-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="6c394-231">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="6c394-232">получение контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="6c394-232">Get the Edge Storage Container</span></span>
* <span data-ttu-id="6c394-233">Добавлен командлет New-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="6c394-233">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="6c394-234">создание контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="6c394-234">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="6c394-235">Добавлен командлет Remove-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="6c394-235">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="6c394-236">удаление контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="6c394-236">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="6c394-237">Добавлен командлет Invoke-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="6c394-237">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="6c394-238">вызов действия для обновления данных в контейнере хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="6c394-238">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="6c394-239">Добавлен командлет Get-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="6c394-239">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="6c394-240">получение учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="6c394-240">Get the Edge Storage Account</span></span>
* <span data-ttu-id="6c394-241">Добавлен командлет New-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="6c394-241">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="6c394-242">создание учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="6c394-242">Create new Edge Storage Account</span></span>
* <span data-ttu-id="6c394-243">Добавлен командлет Remove-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="6c394-243">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="6c394-244">удаление учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="6c394-244">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="6c394-245">Вызов командлета Invoke-AzDataBoxEdgeShare:</span><span class="sxs-lookup"><span data-stu-id="6c394-245">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="6c394-246">вызов действия для обновления данных в общей папке.</span><span class="sxs-lookup"><span data-stu-id="6c394-246">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="6c394-247">Добавлен командлет Set-AzDataBoxEdgeStorageAccountCredential:</span><span class="sxs-lookup"><span data-stu-id="6c394-247">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="6c394-248">установка учетных данных для учетной записи хранилища Azure Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="6c394-248">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6c394-249">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6c394-249">Az.DataFactory</span></span>
* <span data-ttu-id="6c394-250">Добавлены свойства AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId и VersionStatus для командлета Get-AzDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c394-250">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="6c394-251">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.6.0.</span><span class="sxs-lookup"><span data-stu-id="6c394-251">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="6c394-252">Для командлета Set-AzureRmDataFactoryV2IntegrationRuntime добавлен параметр PublicIPs, позволяющий включить создание среды Azure-SSIS IR со статическими общедоступными IP-адресами.</span><span class="sxs-lookup"><span data-stu-id="6c394-252">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="6c394-253">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="6c394-253">Az.DevTestLabs</span></span>
* <span data-ttu-id="6c394-254">Удалена недействительная ссылка в файле Get-AzDtlAllowedVMSizesPolicy.md.</span><span class="sxs-lookup"><span data-stu-id="6c394-254">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6c394-255">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6c394-255">Az.EventHub</span></span>
* <span data-ttu-id="6c394-256">Устранена проблема № 10634: исправлена ссылка на пустой объект для удаления пространства имен концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="6c394-256">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6c394-257">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6c394-257">Az.HDInsight</span></span>
* <span data-ttu-id="6c394-258">Устранена ошибка в файле Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="6c394-258">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="6c394-259">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="6c394-259">Az.MachineLearning</span></span>
* <span data-ttu-id="6c394-260">Вычислительная среда Машинного обучения больше недоступна, поэтому удалены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="6c394-260">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="6c394-261">Get-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="6c394-261">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="6c394-262">Get-AzMlOpClusterKey;</span><span class="sxs-lookup"><span data-stu-id="6c394-262">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="6c394-263">New-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="6c394-263">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="6c394-264">Remove-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="6c394-264">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="6c394-265">Set-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="6c394-265">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="6c394-266">Test-AzMlOpClusterSystemServicesUpdateAvailability;</span><span class="sxs-lookup"><span data-stu-id="6c394-266">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="6c394-267">Update-AzMlOpClusterSystemService.</span><span class="sxs-lookup"><span data-stu-id="6c394-267">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6c394-268">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6c394-268">Az.Network</span></span>
* <span data-ttu-id="6c394-269">Обновлена зависимость Microsoft.Azure.Management.Sql от предварительной версии 1.36 до предварительной версии 1.37.</span><span class="sxs-lookup"><span data-stu-id="6c394-269">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6c394-270">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6c394-270">Az.RecoveryServices</span></span>
* <span data-ttu-id="6c394-271">Добавлена поддержка Azure Site Recovery для виртуальных машин с управляемым диском, зашифрованных при хранении с помощью управляемых клиентом ключей, при восстановлении из Azure в поставщике Azure.</span><span class="sxs-lookup"><span data-stu-id="6c394-271">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="6c394-272">Добавлена поддержка Azure Site Recovery для необязательного ввода идентификатора набора шифрования диска при включении защиты в рамках восстановления из VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="6c394-272">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="6c394-273">Добавлена поддержка Azure Site Recovery для необязательного ввода идентификатора набора шифрования диска на уровне диска при включении защиты в рамках восстановления из VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="6c394-273">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="6c394-274">Добавлена поддержка Azure Site Recovery для обновления элемента, защищенного репликацией, путем сопоставления набора шифрования диска при восстановлении из HyperV в Azure.</span><span class="sxs-lookup"><span data-stu-id="6c394-274">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6c394-275">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6c394-275">Az.Resources</span></span>
* <span data-ttu-id="6c394-276">Исправлена ошибка в справочном документе о командлете Remove-AzTag.</span><span class="sxs-lookup"><span data-stu-id="6c394-276">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="6c394-277">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6c394-277">Az.Sql</span></span>
* <span data-ttu-id="6c394-278">Исправлена функция основных командлетов установки оценки уязвимостей: теперь она позволяет работать с базой данных master для базы данных Azure и ограничить ее в системных базах данных управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="6c394-278">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="6c394-279">Устранена ошибка, возникающая при создании группы отработки отказа экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="6c394-279">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="6c394-280">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6c394-280">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="6c394-281">Добавлен новый допустимый тип лицензии: DR (аварийное восстановление).</span><span class="sxs-lookup"><span data-stu-id="6c394-281">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6c394-282">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6c394-282">Az.Storage</span></span>
* <span data-ttu-id="6c394-283">Добавлено предупреждающее сообщение о критическом изменении значения DefaultAction в следующем выпуске:</span><span class="sxs-lookup"><span data-stu-id="6c394-283">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="6c394-284">Update-AzStorageAccountNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="6c394-284">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="6c394-285">Включена поддержка получения времени последней синхронизации учетной записи хранения путем выполнения командлета Get-AzureRmStorageAccount с параметром -IncludeGeoReplicationStats:</span><span class="sxs-lookup"><span data-stu-id="6c394-285">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span> 
    - <span data-ttu-id="6c394-286">Get-AzureRmStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="6c394-286">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="6c394-287">3.2.0 — декабрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6c394-287">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="6c394-288">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="6c394-288">General</span></span>
* <span data-ttu-id="6c394-289">Обновление ссылок в .psd1 для использования относительного пути для всех модулей.</span><span class="sxs-lookup"><span data-stu-id="6c394-289">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6c394-290">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6c394-290">Az.Accounts</span></span>
* <span data-ttu-id="6c394-291">Установка правильного параметра UserAgent для телеметрии на стороне клиента для Az 4.0 (предварительная версия).</span><span class="sxs-lookup"><span data-stu-id="6c394-291">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="6c394-292">Отображение понятного пользователю сообщения об ошибке, если в Az 4.0 (предварительная версия) не указан контекст.</span><span class="sxs-lookup"><span data-stu-id="6c394-292">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6c394-293">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6c394-293">Az.Batch</span></span>
* <span data-ttu-id="6c394-294">Исправлена проблема [№ 10602](https://github.com/Azure/azure-powershell/issues/10602), из-за которой использование командлета **New-AzBatchPool** приводило к неправильной отправке VirtualMachineConfiguration.ContainerConfiguration или VirtualMachineConfiguration.DataDisks на сервер.</span><span class="sxs-lookup"><span data-stu-id="6c394-294">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6c394-295">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6c394-295">Az.DataFactory</span></span>
* <span data-ttu-id="6c394-296">Обновление пакета SDK Фабрики данных для .NET до версии 4.5.0.</span><span class="sxs-lookup"><span data-stu-id="6c394-296">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6c394-297">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6c394-297">Az.FrontDoor</span></span>
* <span data-ttu-id="6c394-298">Включена поддержка исключений управляемых правил WAF.</span><span class="sxs-lookup"><span data-stu-id="6c394-298">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="6c394-299">Добавление SocketAddr в список автозавершения.</span><span class="sxs-lookup"><span data-stu-id="6c394-299">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="6c394-300">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="6c394-300">Az.HealthcareApis</span></span>
* <span data-ttu-id="6c394-301">Обработка исключений.</span><span class="sxs-lookup"><span data-stu-id="6c394-301">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6c394-302">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6c394-302">Az.KeyVault</span></span>
* <span data-ttu-id="6c394-303">Исправлена ошибка при получении доступа к значению, которое может быть не задано.</span><span class="sxs-lookup"><span data-stu-id="6c394-303">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="6c394-304">Управление сертификатами шифрования на основе эллиптических кривых.</span><span class="sxs-lookup"><span data-stu-id="6c394-304">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="6c394-305">Включена возможность указания кривой для политик сертификатов.</span><span class="sxs-lookup"><span data-stu-id="6c394-305">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6c394-306">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6c394-306">Az.Monitor</span></span>
* <span data-ttu-id="6c394-307">Добавление необязательного аргумента в команду добавления параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="6c394-307">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="6c394-308">Существующий аргумент switch указывает на то, что экспорт в Log Analytics должен выполняться в фиксированную схему</span><span class="sxs-lookup"><span data-stu-id="6c394-308">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="6c394-309">(выделенный тип данных).</span><span class="sxs-lookup"><span data-stu-id="6c394-309">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6c394-310">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6c394-310">Az.Network</span></span>
* <span data-ttu-id="6c394-311">В приложении AzureFirewall, NAT и сетевых правилах включена поддержка IpGroups.</span><span class="sxs-lookup"><span data-stu-id="6c394-311">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6c394-312">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6c394-312">Az.Resources</span></span>
* <span data-ttu-id="6c394-313">Устранена проблема, из-за которой при развертывании шаблона не удавалось считать его параметр, если имя параметра конфликтовало с именем встроенного параметра.</span><span class="sxs-lookup"><span data-stu-id="6c394-313">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="6c394-314">Обновлены командлеты политики для использования новой версии API 2019-09-01 с поддержкой группирования в определениях наборов политик.</span><span class="sxs-lookup"><span data-stu-id="6c394-314">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="6c394-315">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6c394-315">Az.Sql</span></span>
* <span data-ttu-id="6c394-316">Обновлена функция автоматического создания расширенного хранилища для службы оценки уязвимостей в учетной записи StorageV2.</span><span class="sxs-lookup"><span data-stu-id="6c394-316">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6c394-317">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6c394-317">Az.Storage</span></span>
* <span data-ttu-id="6c394-318">Включена поддержка создания маркера SAS на основе удостоверения контейнера и большого двоичного объекта с аутентификацией Oauth на основе контекста службы хранилища:</span><span class="sxs-lookup"><span data-stu-id="6c394-318">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="6c394-319">New-AzStorageContainerSASToken;</span><span class="sxs-lookup"><span data-stu-id="6c394-319">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="6c394-320">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="6c394-320">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="6c394-321">Отозвана поддержка ключей делегирования пользователя учетной записи хранения, а также всех маркеров SAS удостоверения:</span><span class="sxs-lookup"><span data-stu-id="6c394-321">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="6c394-322">Revoke-AzStorageAccountUserDelegationKeys.</span><span class="sxs-lookup"><span data-stu-id="6c394-322">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="6c394-323">Выполнено обновление до Microsoft.Azure.Management.Storage версии 14.2.0 для включения поддержки нового API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="6c394-323">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="6c394-324">Включена поддержка QuotaGiB (квота общего ресурса в ГиБ) для значений свыше 5120 в командлетах для работы с общими папками в плоскости управления и добавлен псевдоним Quota для параметра QuotaGiB.</span><span class="sxs-lookup"><span data-stu-id="6c394-324">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span> 
    - <span data-ttu-id="6c394-325">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="6c394-325">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="6c394-326">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="6c394-326">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="6c394-327">Добавлен псевдоним QuotaGiB для параметра Quota:</span><span class="sxs-lookup"><span data-stu-id="6c394-327">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="6c394-328">Set-AzStorageShareQuota.</span><span class="sxs-lookup"><span data-stu-id="6c394-328">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="6c394-329">Устранена проблема, из-за которой при использовании AzStorageContainerAcl могла очищаться хранимая политика доступа:</span><span class="sxs-lookup"><span data-stu-id="6c394-329">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="6c394-330">Set-AzStorageContainerAcl.</span><span class="sxs-lookup"><span data-stu-id="6c394-330">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="6c394-331">Версия 3.1.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6c394-331">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6c394-332">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="6c394-332">Highlights since the last major release</span></span>
* <span data-ttu-id="6c394-333">Выпуск Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="6c394-333">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="6c394-334">Выпуск Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="6c394-334">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6c394-335">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6c394-335">Az.Compute</span></span>
* <span data-ttu-id="6c394-336">Функция повторного применения виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="6c394-336">VM Reapply feature</span></span>
    - <span data-ttu-id="6c394-337">Добавлен параметр повторного применения в командлет Set-AzVM.</span><span class="sxs-lookup"><span data-stu-id="6c394-337">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="6c394-338">Функция AutomaticRepairs масштабируемого набора виртуальных машин:</span><span class="sxs-lookup"><span data-stu-id="6c394-338">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="6c394-339">Добавлены параметры EnableAutomaticRepair, AutomaticRepairGracePeriod и AutomaticRepairMaxInstanceRepairsPercent в следующие командлеты:   New-AzVmssConfig Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6c394-339">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="6c394-340">Включена поддержка образа из коллекции разных клиентов для New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="6c394-340">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="6c394-341">Добавлен фрагмент Spot в средство заполнения аргументов параметра Priority в командлетах New-AzVM, New-AzVMConfig и New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="6c394-341">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="6c394-342">Добавлены параметры DiskIOPSReadWrite и DiskMBpsReadWrite в командлет Add-AzVmssDataDisk.</span><span class="sxs-lookup"><span data-stu-id="6c394-342">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="6c394-343">Изменен параметр SourceImageId командлета New-AzGalleryImageVersion на необязательный.</span><span class="sxs-lookup"><span data-stu-id="6c394-343">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="6c394-344">Добавлены параметры OSDiskImage и DataDiskImage в командлет New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="6c394-344">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="6c394-345">Добавлен параметр HyperVGeneration в командлет New-AzGalleryImageDefinition.</span><span class="sxs-lookup"><span data-stu-id="6c394-345">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="6c394-346">Добавлены параметры SkipExtensionsOnOverprovisionedVMs в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="6c394-346">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="6c394-347">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="6c394-347">Az.DataBoxEdge</span></span>
* <span data-ttu-id="6c394-348">Добавлен командлет `Get-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="6c394-348">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="6c394-349">Получение заказа.</span><span class="sxs-lookup"><span data-stu-id="6c394-349">Get the Order</span></span>
* <span data-ttu-id="6c394-350">Добавлен командлет `New-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="6c394-350">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="6c394-351">Создание заказа.</span><span class="sxs-lookup"><span data-stu-id="6c394-351">Create new Order</span></span>
* <span data-ttu-id="6c394-352">Добавлен командлет `Remove-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="6c394-352">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="6c394-353">Удаление заказа.</span><span class="sxs-lookup"><span data-stu-id="6c394-353">Remove the Order</span></span>
* <span data-ttu-id="6c394-354">Изменен командлет `New-AzDataBoxEdgeShare`.</span><span class="sxs-lookup"><span data-stu-id="6c394-354">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="6c394-355">Создание локальной общей папки.</span><span class="sxs-lookup"><span data-stu-id="6c394-355">Now creates Local Share</span></span>
* <span data-ttu-id="6c394-356">Добавлен командлет `Set-AzDataBoxEdgeRole`.</span><span class="sxs-lookup"><span data-stu-id="6c394-356">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="6c394-357">Сопоставление IotRole с общей папкой.</span><span class="sxs-lookup"><span data-stu-id="6c394-357">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="6c394-358">Добавлен командлет `Invoke-AzDataBoxEdgeDevice`.</span><span class="sxs-lookup"><span data-stu-id="6c394-358">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="6c394-359">Вызов проверки обновлений, скачивание обновления, установка обновления на устройстве.</span><span class="sxs-lookup"><span data-stu-id="6c394-359">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="6c394-360">Добавлен командлет `Get-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="6c394-360">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="6c394-361">Получение сведений о триггерах.</span><span class="sxs-lookup"><span data-stu-id="6c394-361">Gets the information about Triggers</span></span>
* <span data-ttu-id="6c394-362">Добавлен командлет `New-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="6c394-362">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="6c394-363">Создание триггеров.</span><span class="sxs-lookup"><span data-stu-id="6c394-363">Create new Triggers</span></span>
* <span data-ttu-id="6c394-364">Добавлен командлет `Remove-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="6c394-364">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="6c394-365">Удаление триггеров.</span><span class="sxs-lookup"><span data-stu-id="6c394-365">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6c394-366">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6c394-366">Az.DataFactory</span></span>
* <span data-ttu-id="6c394-367">Обновление пакета SDK Фабрики данных для .NET до версии 4.4.0.</span><span class="sxs-lookup"><span data-stu-id="6c394-367">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="6c394-368">Добавлен параметр ExpressCustomSetup в командлет Set-AzureRmDataFactoryV2IntegrationRuntime для включения конфигураций установки и сторонних компонентов без использования настраиваемого скрипта установки.</span><span class="sxs-lookup"><span data-stu-id="6c394-368">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6c394-369">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6c394-369">Az.DataLakeStore</span></span>
* <span data-ttu-id="6c394-370">Обновлена документация по Get-AzDataLakeStoreDeletedItem и Restore-AzDataLakeStoreDeletedItem.</span><span class="sxs-lookup"><span data-stu-id="6c394-370">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6c394-371">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6c394-371">Az.EventHub</span></span>
* <span data-ttu-id="6c394-372">Исправлена проблема № 10301. Исправлен формат даты маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="6c394-372">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6c394-373">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6c394-373">Az.FrontDoor</span></span>
* <span data-ttu-id="6c394-374">Добавлен параметр MinimumTlsVersion в Enable-AzFrontDoorCustomDomainHttps и New-AzFrontDoorFrontendEndpointObject.</span><span class="sxs-lookup"><span data-stu-id="6c394-374">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="6c394-375">Добавлены параметры HealthProbeMethod и EnabledState в New-AzFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="6c394-375">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="6c394-376">Добавлен новый командлет для создания объекта BackendPoolsSettings для передачи при создании и обновлении Front Door.</span><span class="sxs-lookup"><span data-stu-id="6c394-376">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="6c394-377">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="6c394-377">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6c394-378">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6c394-378">Az.Network</span></span>
* <span data-ttu-id="6c394-379">Изменены примеры параметра FilterData Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="6c394-379">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="6c394-380">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="6c394-380">Az.PrivateDns</span></span>
* <span data-ttu-id="6c394-381">Пакет SDK PrivateDns для .NET обновлен до версии 1.0.0</span><span class="sxs-lookup"><span data-stu-id="6c394-381">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6c394-382">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6c394-382">Az.RecoveryServices</span></span>
* <span data-ttu-id="6c394-383">Включена поддержка Azure Site Recovery для выбора типа диска при включении защиты.</span><span class="sxs-lookup"><span data-stu-id="6c394-383">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="6c394-384">Внесено исправление Azure Site Recovery для изменения действия плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="6c394-384">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="6c394-385">Включена поддержка восстановления SQL Azure Backup для принятия баз данных файлового потока.</span><span class="sxs-lookup"><span data-stu-id="6c394-385">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6c394-386">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6c394-386">Az.RedisCache</span></span>
* <span data-ttu-id="6c394-387">Добавлен параметр MinimumTlsVersion в командлеты New-AzRedisCache и Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="6c394-387">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="6c394-388">Кроме того, добавлен параметр MinimumTlsVersion в выходные данные командлета Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="6c394-388">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="6c394-389">Добавлена проверка параметра -Size для командлетов Set-AzRedisCache и New-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="6c394-389">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="6c394-390">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6c394-390">Az.Resources</span></span>
- <span data-ttu-id="6c394-391">Обновлены командлеты политики для использования новой версии API 2019-06-01 с новым свойством EnforcementMode в назначении политики.</span><span class="sxs-lookup"><span data-stu-id="6c394-391">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="6c394-392">Обновлен пример справки по созданию определения политики</span><span class="sxs-lookup"><span data-stu-id="6c394-392">Updated create policy definition help example</span></span>
- <span data-ttu-id="6c394-393">Исправлена ошибка с параметром -ServicePrincipalName командлета Remove-AZADServicePrincipal с возвратом пустой ссылки, если имя субъекта службы не найдено.</span><span class="sxs-lookup"><span data-stu-id="6c394-393">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="6c394-394">Исправлена ошибка с New-AZADServicePrincipal с возвратом пустой ссылки, если у клиента нет подписки.</span><span class="sxs-lookup"><span data-stu-id="6c394-394">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="6c394-395">Изменен командлет New-AzAdServicePrincipal для добавления учетных данных только для связанного приложения.</span><span class="sxs-lookup"><span data-stu-id="6c394-395">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="6c394-396">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6c394-396">Az.Sql</span></span>
* <span data-ttu-id="6c394-397">Добавлена поддержка ReadReplicaCount для базы данных.</span><span class="sxs-lookup"><span data-stu-id="6c394-397">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="6c394-398">Исправлена ошибка с Set-AzSqlDatabase, если избыточность в пределах зоны не настроена.</span><span class="sxs-lookup"><span data-stu-id="6c394-398">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="6c394-399">Версия 3.0.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6c394-399">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="6c394-400">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="6c394-400">General</span></span>
* <span data-ttu-id="6c394-401">Выпущена версия Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="6c394-401">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6c394-402">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6c394-402">Az.Accounts</span></span>
* <span data-ttu-id="6c394-403">Добавлено сообщение об устаревании для псевдонима "Resolve-Error".</span><span class="sxs-lookup"><span data-stu-id="6c394-403">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="6c394-404">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="6c394-404">Az.Advisor</span></span>
* <span data-ttu-id="6c394-405">Добавлена новая категория Operational Excellence (Эффективность работы) в командлет Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="6c394-405">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6c394-406">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6c394-406">Az.Batch</span></span>
* <span data-ttu-id="6c394-407">`CoreQuota` в `BatchAccountContext` переименован в `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="6c394-407">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="6c394-408">Также появился новый `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="6c394-408">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="6c394-409">Это влияет на **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="6c394-409">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="6c394-410">Параметр **New-AzBatchTask** `-ResourceFile` теперь принимает коллекцию объектов `PSResourceFile`, которые можно создать с помощью нового командлета **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="6c394-410">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="6c394-411">Новый командлет **New-AzBatchResourceFile**, который помогает создавать объекты `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="6c394-411">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="6c394-412">Их можно передавать в **New-AzBatchTask** в параметре `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="6c394-412">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="6c394-413">Это позволяет поддерживать два новых типа файлов ресурсов, которые дополняют существующий метод `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="6c394-413">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="6c394-414">Файлы ресурсов на основе `AutoStorageContainerName` скачивают весь контейнер автоматического хранения в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="6c394-414">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="6c394-415">Файлы ресурсов на основе `StorageContainerUrl` скачивают указанный в URL-адресе контейнер в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="6c394-415">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="6c394-416">Удалено свойство `ApplicationPackages` в `PSApplication`, который возвращается из **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="6c394-416">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="6c394-417">Отдельные пакеты в приложении теперь можно извлечь с помощью **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="6c394-417">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="6c394-418">Например: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="6c394-418">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="6c394-419">`ApplicationId` переименован в `ApplicationName` для **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** и **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="6c394-419">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="6c394-420">Теперь `ApplicationId` является псевдонимом для `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="6c394-420">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="6c394-421">Добавлено новое свойство `PSWindowsUserConfiguration` в `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="6c394-421">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="6c394-422">`Version` переименован в `Name` для `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="6c394-422">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="6c394-423">`BlobSource` переименован в `HttpUrl` для `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="6c394-423">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="6c394-424">Удалено свойство `OSDisk` из `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="6c394-424">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="6c394-425">Удалена операция **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="6c394-425">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="6c394-426">Больше она не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6c394-426">This operation is no longer supported.</span></span>
* <span data-ttu-id="6c394-427">Удалено `TargetOSVersion` из `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="6c394-427">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="6c394-428">`CurrentOSVersion` переименован в `OSVersion` для `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="6c394-428">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="6c394-429">Удалено `DataEgressGiB` и `DataIngressGiB` из `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="6c394-429">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="6c394-430">Операция **Get-AzBatchNodeAgentSku** удалена и заменена на **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="6c394-430">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="6c394-431">**Get-AzBatchSupportedImage** возвращает те же данные, что и **Get-AzBatchNodeAgentSku**, но в более удобном формате.</span><span class="sxs-lookup"><span data-stu-id="6c394-431">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="6c394-432">Также возвращаются новые непроверенные образы.</span><span class="sxs-lookup"><span data-stu-id="6c394-432">New non-verified images are also now returned.</span></span> <span data-ttu-id="6c394-433">Включается и дополнительная информация о `Capabilities` и `BatchSupportEndOfLife` для каждого образа.</span><span class="sxs-lookup"><span data-stu-id="6c394-433">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="6c394-434">Добавлена возможность монтировать файловые системы на каждом узле пула с помощью нового параметра `MountConfiguration` в **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="6c394-434">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="6c394-435">Теперь поддерживаются правила безопасности сети, которые блокируют сетевой доступ к пулу по исходящему порту трафика.</span><span class="sxs-lookup"><span data-stu-id="6c394-435">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="6c394-436">Это выполняется с помощью свойства `SourcePortRanges` для `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="6c394-436">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="6c394-437">Что касается выполнения контейнеров, пакетная служба теперь поддерживает выполнение задачи в рабочей папке контейнера или рабочей папке задачи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="6c394-437">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="6c394-438">Выбор зависит от параметра `WorkingDirectory` в `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="6c394-438">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="6c394-439">Добавлена возможность указать коллекцию общедоступных IP-адресов для `PSNetworkConfiguration` с помощью нового свойства `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="6c394-439">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="6c394-440">Это гарантирует, что узлы в пуле будут иметь IP-адреса из списка, предоставленного пользователем.</span><span class="sxs-lookup"><span data-stu-id="6c394-440">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="6c394-441">Если значение не задано, по умолчанию для `WaitForSuccess` в `PSSTartTask` используется значение `$True` (ранее `$False`).</span><span class="sxs-lookup"><span data-stu-id="6c394-441">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="6c394-442">Если значение не задано, по умолчанию для `Scope` в `PSAutoUserSpecification` используется значение `Pool` (ранее `Task` для Windows или `Pool` для Linux).</span><span class="sxs-lookup"><span data-stu-id="6c394-442">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6c394-443">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6c394-443">Az.Cdn</span></span>
* <span data-ttu-id="6c394-444">Добавлены UrlRewriteAction и CacheKeyQueryStringAction в RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="6c394-444">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="6c394-445">Исправлено несколько ошибок, таких как отсутствующий входной параметр Selector в командлете New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="6c394-445">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6c394-446">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6c394-446">Az.Compute</span></span>
* <span data-ttu-id="6c394-447">Функция набора шифрования диска</span><span class="sxs-lookup"><span data-stu-id="6c394-447">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="6c394-448">Новые командлеты:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="6c394-448">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="6c394-449">Добавлен параметр ProximityPlacementGroupId в следующие командлеты: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="6c394-449">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="6c394-450">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="6c394-450">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="6c394-451">Параметры DiskEncryptionSetId и EncryptionType добавлены в следующие командлеты:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="6c394-451">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="6c394-452">Добавлен параметр PublicIPAddressVersion в New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="6c394-452">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="6c394-453">FileUris для расширения пользовательских скриптов теперь будет защищенным, а не общедоступным параметром</span><span class="sxs-lookup"><span data-stu-id="6c394-453">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="6c394-454">Добавлено ScaleInPolicy в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6c394-454">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="6c394-455">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="6c394-455">Breaking changes</span></span>
    - <span data-ttu-id="6c394-456">Параметр UploadSizeInBytes применяется теперь вместо DiskSizeGB для New-AzDiskConfig, если CreateOption имеет значение Upload</span><span class="sxs-lookup"><span data-stu-id="6c394-456">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="6c394-457">PublishingProfile.Source.ManagedImage.Id заменяется на StorageProfile.Source.Id в объекте GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="6c394-457">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6c394-458">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6c394-458">Az.DataFactory</span></span>
* <span data-ttu-id="6c394-459">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.3.0.</span><span class="sxs-lookup"><span data-stu-id="6c394-459">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6c394-460">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6c394-460">Az.DataLakeStore</span></span>
* <span data-ttu-id="6c394-461">Обновлен пакет SDK для ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), включает следующие исправления</span><span class="sxs-lookup"><span data-stu-id="6c394-461">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="6c394-462">Не создается исключение при невозможности десериализовать значение времени создания для записи в корзине или каталоге.</span><span class="sxs-lookup"><span data-stu-id="6c394-462">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="6c394-463">Предоставляется параметр для времени ожидания запроса в adlsclient</span><span class="sxs-lookup"><span data-stu-id="6c394-463">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="6c394-464">Исправлена передача исходного значения syncflag для восстановления badoffset</span><span class="sxs-lookup"><span data-stu-id="6c394-464">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="6c394-465">Исправлена операция EnumerateDirectory, чтобы она извлекала токен продолжения после проверки ответа</span><span class="sxs-lookup"><span data-stu-id="6c394-465">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="6c394-466">Исправлена ошибка объединения</span><span class="sxs-lookup"><span data-stu-id="6c394-466">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6c394-467">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6c394-467">Az.FrontDoor</span></span>
* <span data-ttu-id="6c394-468">Исправлены разные опечатки в разных частях модуля</span><span class="sxs-lookup"><span data-stu-id="6c394-468">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6c394-469">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6c394-469">Az.HDInsight</span></span>
* <span data-ttu-id="6c394-470">Исправлена ошибка, из-за которой клиент получал сообщение об ошибке 'Not a valid Base-64 string' (Не является допустимой строкой Base64) при выполнении Get-AzHDInsightCluster для получения кластера с хранилищем ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="6c394-470">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="6c394-471">Добавлен параметр с именем ApplicationId в три командлета Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig и New-AzHDInsightCluster, чтобы клиент мог предоставить идентификатор приложения субъекта-службы для доступа к Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="6c394-471">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="6c394-472">Для Microsoft.Azure.Management.HDInsight изменена версия с 2.1.0 на 5.1.0</span><span class="sxs-lookup"><span data-stu-id="6c394-472">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="6c394-473">Удалены пять командлетов:</span><span class="sxs-lookup"><span data-stu-id="6c394-473">Removed five cmdlets:</span></span>
    - <span data-ttu-id="6c394-474">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="6c394-474">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="6c394-475">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="6c394-475">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="6c394-476">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="6c394-476">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="6c394-477">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6c394-477">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="6c394-478">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6c394-478">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="6c394-479">Добавлены три командлета:</span><span class="sxs-lookup"><span data-stu-id="6c394-479">Added three cmdlets:</span></span>
    - <span data-ttu-id="6c394-480">Get-AzHDInsightMonitoring заменяет собой Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="6c394-480">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="6c394-481">Enable-AzHDInsightMonitoring заменяет собой Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="6c394-481">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="6c394-482">Disable-AzHDInsightMonitoring заменяет собой Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="6c394-482">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="6c394-483">Исправлен командлет Get-AzHDInsightProperties, чтобы он поддерживал получение сведений о возможностях из определенного расположения.</span><span class="sxs-lookup"><span data-stu-id="6c394-483">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="6c394-484">Удалены наборы параметров ("Spark1", "Spark2") из Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="6c394-484">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="6c394-485">Добавлены примеры в справочные документы по командлету Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="6c394-485">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="6c394-486">Изменен тип выходных данных для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="6c394-486">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="6c394-487">Для Get-AzHDInsightProperties тип выходных данных изменен с CapabilitiesResponse на AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="6c394-487">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="6c394-488">Для Remove-AzHDInsightCluster тип выходных данных изменен с ClusterGetResponse на bool.</span><span class="sxs-lookup"><span data-stu-id="6c394-488">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="6c394-489">Для Set-AzHDInsightGatewaySettings тип выходных данных изменен с HttpConnectivitySettings на GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="6c394-489">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="6c394-490">Добавлены несколько условий для проверки сценариев.</span><span class="sxs-lookup"><span data-stu-id="6c394-490">Added some scenario test cases.</span></span>
* <span data-ttu-id="6c394-491">Удалены несколько псевдонимов: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="6c394-491">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6c394-492">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6c394-492">Az.IotHub</span></span>
* <span data-ttu-id="6c394-493">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="6c394-493">Breaking changes:</span></span>
    - <span data-ttu-id="6c394-494">Командлет Add-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="6c394-494">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="6c394-495">Удален набор параметров __AllParameterSets для командлета Add-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="6c394-495">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="6c394-496">Командлет Get-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="6c394-496">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="6c394-497">Удален набор параметров __AllParameterSets для командлета Get-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="6c394-497">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="6c394-498">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties.</span><span class="sxs-lookup"><span data-stu-id="6c394-498">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="6c394-499">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties.</span><span class="sxs-lookup"><span data-stu-id="6c394-499">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="6c394-500">Командлет New-AzIotHubExportDevice больше не поддерживает псевдоним New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="6c394-500">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="6c394-501">Командлет New-AzIotHubImportDevice больше не поддерживает псевдоним New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="6c394-501">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="6c394-502">Командлет Remove-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="6c394-502">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="6c394-503">Удален набор параметров __AllParameterSets для командлета Remove-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="6c394-503">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="6c394-504">Командлет Set-AzIotHub теперь не поддерживает параметр OperationsMonitoringProperties и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="6c394-504">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="6c394-505">Удален набор параметров UpdateOperationsMonitoringProperties для командлета Set-AzIotHub.</span><span class="sxs-lookup"><span data-stu-id="6c394-505">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6c394-506">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6c394-506">Az.RecoveryServices</span></span>
* <span data-ttu-id="6c394-507">Azure Site Recovery поддерживает настройку сетевых ресурсов, например групп безопасности сети, общедоступных IP-адресов и внутренних подсистем балансировки нагрузки из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="6c394-507">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="6c394-508">Azure Site Recovery поддерживает запись на управляемый диск из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="6c394-508">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="6c394-509">Azure Site Recovery поддерживает сокращение NIC из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="6c394-509">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="6c394-510">Azure Site Recovery поддерживает ускорение сети NIC из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="6c394-510">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="6c394-511">Azure Site Recovery поддерживает автоматическое обновление агента из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="6c394-511">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="6c394-512">Azure Site Recovery поддерживает стандартный SSD-накопитель из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="6c394-512">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="6c394-513">Azure Site Recovery поддерживает двухпроходное шифрование диска Azure из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="6c394-513">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="6c394-514">Azure Site Recovery поддерживает новый добавленный диск из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="6c394-514">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="6c394-515">Добавлена функция SoftDelete для виртуальных машин и соответствующие тесты</span><span class="sxs-lookup"><span data-stu-id="6c394-515">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="6c394-516">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6c394-516">Az.Resources</span></span>
* <span data-ttu-id="6c394-517">Обновлена сборка зависимостей Microsoft.Extensions.Caching.Memory с версии 1.1.1 до 2.2</span><span class="sxs-lookup"><span data-stu-id="6c394-517">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6c394-518">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6c394-518">Az.Network</span></span>
* <span data-ttu-id="6c394-519">Изменены все командлеты для PrivateEndpointConnection, чтобы они поддерживали универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="6c394-519">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="6c394-520">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="6c394-520">Updated cmdlet:</span></span>
        - <span data-ttu-id="6c394-521">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="6c394-521">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6c394-522">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="6c394-522">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6c394-523">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="6c394-523">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6c394-524">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="6c394-524">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6c394-525">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6c394-525">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="6c394-526">Добавлен новый командлет для PrivateLinkResource, который поддерживает универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="6c394-526">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="6c394-527">Новый командлет</span><span class="sxs-lookup"><span data-stu-id="6c394-527">New cmdlet:</span></span>
        - <span data-ttu-id="6c394-528">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="6c394-528">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="6c394-529">Добавлены новые поля и параметр для протокола прокси версии 2.</span><span class="sxs-lookup"><span data-stu-id="6c394-529">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="6c394-530">Добавлено свойство EnableProxyProtocol в PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6c394-530">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="6c394-531">Добавлено свойство LinkIdentifier в PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6c394-531">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="6c394-532">Обновлен New-AzPrivateLinkService для поддержки нового необязательного параметра EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="6c394-532">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="6c394-533">Исправлено описание параметра в справочной документации по командлету New-AzApplicationGatewaySku.</span><span class="sxs-lookup"><span data-stu-id="6c394-533">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="6c394-534">Новые командлеты для поддержки политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="6c394-534">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="6c394-535">Добавлена поддержка дочерних ресурсов RouteTables для VirtualHub</span><span class="sxs-lookup"><span data-stu-id="6c394-535">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="6c394-536">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="6c394-536">New cmdlets added:</span></span>
        - <span data-ttu-id="6c394-537">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="6c394-537">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="6c394-538">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6c394-538">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="6c394-539">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6c394-539">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="6c394-540">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6c394-540">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="6c394-541">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="6c394-541">Set-AzVirtualHub</span></span>
* <span data-ttu-id="6c394-542">Добавлена поддержка новых свойств SKU для VirtualHub и VirtualWANType в VirtualWan</span><span class="sxs-lookup"><span data-stu-id="6c394-542">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="6c394-543">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="6c394-543">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="6c394-544">New-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="6c394-544">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="6c394-545">Update-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="6c394-545">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="6c394-546">New-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="6c394-546">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="6c394-547">Update-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="6c394-547">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="6c394-548">Добавлена поддержка свойства EnableInternetSecurity для HubVnetConnection, VpnConnection и ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="6c394-548">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="6c394-549">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="6c394-549">New cmdlets added:</span></span>
        - <span data-ttu-id="6c394-550">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="6c394-550">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="6c394-551">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="6c394-551">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="6c394-552">New-AzureRmVirtualHubVnetConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="6c394-552">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="6c394-553">New-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="6c394-553">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="6c394-554">Update-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="6c394-554">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="6c394-555">New-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="6c394-555">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="6c394-556">Set-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="6c394-556">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="6c394-557">Добавлена поддержка настройки политики верхнего уровня WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="6c394-557">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="6c394-558">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="6c394-558">New cmdlets added:</span></span>
        - <span data-ttu-id="6c394-559">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="6c394-559">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="6c394-560">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="6c394-560">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="6c394-561">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="6c394-561">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="6c394-562">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="6c394-562">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="6c394-563">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="6c394-563">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="6c394-564">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="6c394-564">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="6c394-565">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="6c394-565">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="6c394-566">New-AzApplicationGatewayFirewallPolicy: добавлены параметры PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="6c394-566">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="6c394-567">Добавлена поддержка оператора Geo-Match для CustomRule</span><span class="sxs-lookup"><span data-stu-id="6c394-567">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="6c394-568">Добавлен параметр GeoMatch в оператор для FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="6c394-568">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="6c394-569">Добавлена поддержка политики брандмауэра perListener и perSite</span><span class="sxs-lookup"><span data-stu-id="6c394-569">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="6c394-570">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="6c394-570">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="6c394-571">New-AzApplicationGatewayHttpListener: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="6c394-571">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="6c394-572">New-AzApplicationGatewayPathRuleConfig: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="6c394-572">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="6c394-573">Исправлен учет регистра для требуемой подсети с именем AzureBastionSubnet в PSBastion</span><span class="sxs-lookup"><span data-stu-id="6c394-573">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="6c394-574">Поддержка полного доменного имени назначения в правилах сети и преобразованного полного доменного имени в правилах NAT для брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="6c394-574">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="6c394-575">Добавлена поддержка ресурсов верхнего уровня RouteTables для IpGroup</span><span class="sxs-lookup"><span data-stu-id="6c394-575">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="6c394-576">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="6c394-576">New cmdlets added:</span></span>
        - <span data-ttu-id="6c394-577">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="6c394-577">New-AzIpGroup</span></span>
        - <span data-ttu-id="6c394-578">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="6c394-578">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="6c394-579">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="6c394-579">Get-AzIpGroup</span></span>
        - <span data-ttu-id="6c394-580">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="6c394-580">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6c394-581">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6c394-581">Az.ServiceFabric</span></span>
* <span data-ttu-id="6c394-582">Удален командлет Add-AzServiceFabricApplicationCertificate, так как соответствующий сценарий выполняется командлетом Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="6c394-582">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="6c394-583">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6c394-583">Az.Sql</span></span>
* <span data-ttu-id="6c394-584">Добавлена поддержка восстановления удаленных баз данных в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="6c394-584">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="6c394-585">Из кода удалены старые командлеты аудита.</span><span class="sxs-lookup"><span data-stu-id="6c394-585">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="6c394-586">Удалены нерекомендуемые псевдонимы:</span><span class="sxs-lookup"><span data-stu-id="6c394-586">Removed deprecated aliases:</span></span>
* <span data-ttu-id="6c394-587">Get-AzSqlDatabaseIndexRecommendations (вместо него используйте Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="6c394-587">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="6c394-588">Get-AzSqlDatabaseRestorePoints (вместо него используйте Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="6c394-588">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="6c394-589">Удален командлет Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6c394-589">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="6c394-590">Удалены псевдонимы для нерекомендуемых командлетов параметров оценки уязвимостей</span><span class="sxs-lookup"><span data-stu-id="6c394-590">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="6c394-591">Командлеты расширенного обнаружения угроз объявлены устаревшими</span><span class="sxs-lookup"><span data-stu-id="6c394-591">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="6c394-592">Добавлены командлеты для отключения и включения рекомендаций о конфиденциальности для столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="6c394-592">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6c394-593">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6c394-593">Az.Storage</span></span>
* <span data-ttu-id="6c394-594">Поддержка включения большой общей папки при создании или обновлении учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="6c394-594">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="6c394-595">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6c394-595">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="6c394-596">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6c394-596">Set-AzStorageAccount</span></span>
* <span data-ttu-id="6c394-597">При закрытии или получении маркера файла пропускается проверка того, является ли входной путь файлом или каталогом, чтобы избежать сбоев при получении объектов в состоянии DeletePending.</span><span class="sxs-lookup"><span data-stu-id="6c394-597">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="6c394-598">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="6c394-598">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="6c394-599">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="6c394-599">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="6c394-600">2.8.0 — октябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6c394-600">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="6c394-601">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="6c394-601">General</span></span>
* <span data-ttu-id="6c394-602">Выпуск Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="6c394-602">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6c394-603">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6c394-603">Az.Accounts</span></span>
* <span data-ttu-id="6c394-604">Обновление телеметрии и перезаписи URL-адресов для созданных модулей, исправление для модульных тестов Windows.</span><span class="sxs-lookup"><span data-stu-id="6c394-604">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6c394-605">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6c394-605">Az.ApiManagement</span></span>
* <span data-ttu-id="6c394-606">**Set-AzApiManagementApi** — в ApiVersionSet добавлена поддержка обновления API.</span><span class="sxs-lookup"><span data-stu-id="6c394-606">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="6c394-607">исправлена проблема https://github.com/Azure/azure-powershell/issues/10068.</span><span class="sxs-lookup"><span data-stu-id="6c394-607">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6c394-608">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6c394-608">Az.Automation</span></span>
* <span data-ttu-id="6c394-609">Исправлен командлет New-AzureAutomationSoftwareUpdateConfiguration для параметра перезагрузки Linux.</span><span class="sxs-lookup"><span data-stu-id="6c394-609">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="6c394-610">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6c394-610">Az.Batch</span></span>
* <span data-ttu-id="6c394-611">Командлет **Get-AzBatchNodeAgentSku** объявлен устаревшим и будет заменен на **Get-AzBatchSupportImage** в версии 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="6c394-611">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6c394-612">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6c394-612">Az.Compute</span></span>
* <span data-ttu-id="6c394-613">В командлеты New-AzVM и New-AzVmss добавлены параметры Priority, EvictionPolicy и MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="6c394-613">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="6c394-614">Исправлены предупреждающее сообщение для командлетов Add-AzVMAdditionalUnattendContent и Add-AzVMSshPublicKey и справочная документация по ним.</span><span class="sxs-lookup"><span data-stu-id="6c394-614">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="6c394-615">Для Set-AzVMDiskEncryptionExtension исправлено исключение -skipVmBackup для виртуальных машин Linux с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="6c394-615">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="6c394-616">Исправлена ошибка при изменении параметров шифрования в Set-AzVMDiskEncryptionExtension, реализован двухэтапный сценарий.</span><span class="sxs-lookup"><span data-stu-id="6c394-616">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6c394-617">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6c394-617">Az.DataFactory</span></span>
* <span data-ttu-id="6c394-618">Добавлены команды CRUD для потока данных Фабрики данных Azure версии 2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow и Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="6c394-618">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="6c394-619">Добавлены команды действий для сеанса отладки потока данных Фабрики данных Azure версии 2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand и Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="6c394-619">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="6c394-620">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.2.0.</span><span class="sxs-lookup"><span data-stu-id="6c394-620">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6c394-621">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6c394-621">Az.DataLakeStore</span></span>
* <span data-ttu-id="6c394-622">Проверка учетной записи исправлена так, чтобы учетные записи, содержащие знак "-", можно было передавать без домена.</span><span class="sxs-lookup"><span data-stu-id="6c394-622">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="6c394-623">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="6c394-623">Az.HealthcareApis</span></span>
* <span data-ttu-id="6c394-624">Версия PowerShell обновлена до 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="6c394-624">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="6c394-625">Версия пакета SDK обновлена до 1.0.2.</span><span class="sxs-lookup"><span data-stu-id="6c394-625">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="6c394-626">В тестах обновлены ссылки на новую версию пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="6c394-626">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="6c394-627">Вложенная выходная структура заменена на плоскую.</span><span class="sxs-lookup"><span data-stu-id="6c394-627">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6c394-628">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6c394-628">Az.IotHub</span></span>
* <span data-ttu-id="6c394-629">Добавлен новый источник маршрутизации DigitalTwinChangeEvents.</span><span class="sxs-lookup"><span data-stu-id="6c394-629">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="6c394-630">Исправлены незначительные ошибки: Get-AzIothub не возвращает subscriptionId.</span><span class="sxs-lookup"><span data-stu-id="6c394-630">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="6c394-631">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6c394-631">Az.Monitor</span></span>
* <span data-ttu-id="6c394-632">Добавлены новые получатели групп действий: -ItsmReceiver, -VoiceReceiver, -ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver.</span><span class="sxs-lookup"><span data-stu-id="6c394-632">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="6c394-633">Для получателей включите общую схему оповещений.</span><span class="sxs-lookup"><span data-stu-id="6c394-633">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="6c394-634">Это не касается получателей SMS, push-уведомлений приложения Azure, ITSM и голосовых сообщений.</span><span class="sxs-lookup"><span data-stu-id="6c394-634">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="6c394-635">Веб-перехватчики теперь поддерживают аутентификацию Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6c394-635">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6c394-636">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6c394-636">Az.Network</span></span>
* <span data-ttu-id="6c394-637">Добавлен новый командлет Get-AzAvailableServiceAlias, позволяющий получить псевдонимы для политик конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="6c394-637">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="6c394-638">В подключениях шлюза виртуальной сети появилась возможность добавлять селекторы трафика.</span><span class="sxs-lookup"><span data-stu-id="6c394-638">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="6c394-639">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="6c394-639">New cmdlets added:</span></span>
        - <span data-ttu-id="6c394-640">New-AzureRmTrafficSelectorPolicy.</span><span class="sxs-lookup"><span data-stu-id="6c394-640">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="6c394-641">В командлеты добавлены необязательные параметры -TrafficSelectorPolicies, -New-AzureRmVirtualNetworkGatewayConnection, -Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="6c394-641">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="6c394-642">В конфигурациях правил сетевой безопасности добавлена поддержка протоколов ESP и AH.</span><span class="sxs-lookup"><span data-stu-id="6c394-642">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="6c394-643">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="6c394-643">Updated cmdlets:</span></span>
        - <span data-ttu-id="6c394-644">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="6c394-644">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="6c394-645">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="6c394-645">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="6c394-646">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="6c394-646">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="6c394-647">Улучшена обработка исключений в командлетах Cortex.</span><span class="sxs-lookup"><span data-stu-id="6c394-647">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="6c394-648">Выпущены новые поколения и номера SKU VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="6c394-648">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="6c394-649">Представлены новые поколения VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="6c394-649">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="6c394-650">Представлены новые номера SKU VirtualNetworkGateways с высокой пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="6c394-650">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6c394-651">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6c394-651">Az.RedisCache</span></span>
* <span data-ttu-id="6c394-652">В справочную документацию по Set-AzRedisCache добавлены недостающие значения для параметра -Size.</span><span class="sxs-lookup"><span data-stu-id="6c394-652">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="6c394-653">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6c394-653">Az.Sql</span></span>
* <span data-ttu-id="6c394-654">Добавлена возможность назначать администратора Active Directory в Управляемом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="6c394-654">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6c394-655">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6c394-655">Az.Storage</span></span>
* <span data-ttu-id="6c394-656">Клиентская библиотека службы хранилища Azure обновлена до версии 11.1.0.</span><span class="sxs-lookup"><span data-stu-id="6c394-656">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="6c394-657">NextPageLink теперь позволяет получить список контейнеров с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="6c394-657">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="6c394-658">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6c394-658">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="6c394-659">NextPageLink теперь позволяет получить список учетных записей хранения из подписки.</span><span class="sxs-lookup"><span data-stu-id="6c394-659">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="6c394-660">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6c394-660">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="6c394-661">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="6c394-661">Az.StorageSync</span></span>
* <span data-ttu-id="6c394-662">Исправлена проблема 9810 с Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="6c394-662">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6c394-663">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6c394-663">Az.Websites</span></span>
* <span data-ttu-id="6c394-664">Обновление плана службы приложений с помощью Set-AzWebApp приводило к сбою приложения.</span><span class="sxs-lookup"><span data-stu-id="6c394-664">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="6c394-665">2.7.0 — сентябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6c394-665">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="6c394-666">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6c394-666">Az.ApiManagement</span></span>
* <span data-ttu-id="6c394-667">В справочной документации по командлету Set-AzApiManagementPolicy обновлено описание параметра -Format.</span><span class="sxs-lookup"><span data-stu-id="6c394-667">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="6c394-668">Из справочной документации удалены ссылки на нерекомендуемый командлет Update-AzApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="6c394-668">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="6c394-669">Вместо него следует использовать командлет Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="6c394-669">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6c394-670">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6c394-670">Az.Automation</span></span>
* <span data-ttu-id="6c394-671">В справочной документации по командлету Register-AzAutomationDscNode исправлена опечатка в примере.</span><span class="sxs-lookup"><span data-stu-id="6c394-671">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="6c394-672">Добавлено уточнение об ограничениях ОС для командлета Register-AzAutomationDSCNode.</span><span class="sxs-lookup"><span data-stu-id="6c394-672">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="6c394-673">Исправлено исключение пустой ссылки для параметра -Wait в командлете Start-AzAutomationRunbook.</span><span class="sxs-lookup"><span data-stu-id="6c394-673">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6c394-674">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6c394-674">Az.Compute</span></span>
* <span data-ttu-id="6c394-675">Добавлен параметр UploadSizeInBytes для командлета New-AzDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="6c394-675">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="6c394-676">Добавлен добавочный параметр для командлета New-AzSnapshotConfig.</span><span class="sxs-lookup"><span data-stu-id="6c394-676">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="6c394-677">Для виртуальной машины добавлены такие функции с низким приоритетом:</span><span class="sxs-lookup"><span data-stu-id="6c394-677">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="6c394-678">Для командлета New-AzVMConfig добавлены параметры MaxPrice, EvictionPolicy и Priority.</span><span class="sxs-lookup"><span data-stu-id="6c394-678">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="6c394-679">Для командлетов New-AzVmssConfig, Update-AzVM и Update-AzVmss добавлен параметр MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="6c394-679">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="6c394-680">Для командлета Get-AzAvailabilitySet устранена проблема со ссылкой на виртуальную машину, когда в нем перечисляются все группы доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="6c394-680">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="6c394-681">Исправлено исключение NULL для командлета Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="6c394-681">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="6c394-682">Исправлен метод поиска VHD для относительной конечной позиции.</span><span class="sxs-lookup"><span data-stu-id="6c394-682">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="6c394-683">Устранена проблема с UltraSSD для командлетов New-AzVM и Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="6c394-683">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6c394-684">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6c394-684">Az.DataFactory</span></span>
* <span data-ttu-id="6c394-685">Добавлены 3 новые команды для ADF версии 2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription и Get-AzDataFactoryV2TriggerSubscriptionStatus.</span><span class="sxs-lookup"><span data-stu-id="6c394-685">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="6c394-686">Пакет SDK ADF для .NET обновлен до версии 4.1.3.</span><span class="sxs-lookup"><span data-stu-id="6c394-686">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6c394-687">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6c394-687">Az.HDInsight</span></span>
* <span data-ttu-id="6c394-688">Укажите критические изменения.</span><span class="sxs-lookup"><span data-stu-id="6c394-688">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6c394-689">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6c394-689">Az.IotHub</span></span>
* <span data-ttu-id="6c394-690">Добавлена поддержка для вызова отработки отказа для IotHub в георегион аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="6c394-690">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="6c394-691">Добавлена поддержка для управления обогащением сообщений для IotHub.</span><span class="sxs-lookup"><span data-stu-id="6c394-691">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="6c394-692">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="6c394-692">New cmdlets are:</span></span>
    - <span data-ttu-id="6c394-693">Add-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="6c394-693">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="6c394-694">Get-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="6c394-694">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="6c394-695">Remove-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="6c394-695">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="6c394-696">Set-AzIotHubMessageEnrichment.</span><span class="sxs-lookup"><span data-stu-id="6c394-696">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6c394-697">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6c394-697">Az.Monitor</span></span>
* <span data-ttu-id="6c394-698">Указание на самую последнюю версию пакета SDK для монитора, т. е. 0.24.1-preview:</span><span class="sxs-lookup"><span data-stu-id="6c394-698">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="6c394-699">В командлеты метрик добавлены некритические изменения, т. е. перечисление единиц поддерживает несколько новых значений.</span><span class="sxs-lookup"><span data-stu-id="6c394-699">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="6c394-700">Эти командлеты доступны только для чтения, поэтому входные данные командлетов не будут изменены.</span><span class="sxs-lookup"><span data-stu-id="6c394-700">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="6c394-701">Актуальная версия API запросов **ActionGroups** — **2019-06-01**. До этого была версия **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="6c394-701">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="6c394-702">Тесты сценария обновлены в соответствии с этим изменением.</span><span class="sxs-lookup"><span data-stu-id="6c394-702">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="6c394-703">В конструкторы классов **EmailReceiver** и **WebhookReceiver** добавлен один новый обязательный аргумент — логическое значение с именем **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="6c394-703">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="6c394-704">Сейчас для него установлено значение **false**, чтобы скрыть это критическое изменение от командлетов.</span><span class="sxs-lookup"><span data-stu-id="6c394-704">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="6c394-705">**Примечание**. Это временное изменение, которое должно быть подтверждено командой оповещения.</span><span class="sxs-lookup"><span data-stu-id="6c394-705">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="6c394-706">Порядок аргументов для конструктора класса **Source** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="6c394-706">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="6c394-707">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="6c394-707">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="6c394-708">Порядок аргументов для конструктора класса **AlertingAction** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="6c394-708">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="6c394-709">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="6c394-709">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="6c394-710">Добавлена поддержка критериев динамического порога для оповещения метрики версии 2:</span><span class="sxs-lookup"><span data-stu-id="6c394-710">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="6c394-711">New-AzMetricAlertRuleV2Criteria: теперь также позволяет создавать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="6c394-711">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="6c394-712">Add-AzMetricAlertRuleV2: теперь также позволяет принимать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="6c394-712">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="6c394-713">Добавлены усовершенствования в командлетах запланированных правил запросов (SQR).</span><span class="sxs-lookup"><span data-stu-id="6c394-713">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="6c394-714">Командлеты будут принимать параметр Location в обоих форматах: расположение (например, eastus) или отображаемое имя расположения (например, "восточная часть США").</span><span class="sxs-lookup"><span data-stu-id="6c394-714">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="6c394-715">Параметр Enabled проиллюстрирован в файлах справки надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="6c394-715">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="6c394-716">Добавлены примеры для необязательного параметра ActionGroup.</span><span class="sxs-lookup"><span data-stu-id="6c394-716">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="6c394-717">Все файлы справки улучшены.</span><span class="sxs-lookup"><span data-stu-id="6c394-717">Overall improved help files</span></span>
* <span data-ttu-id="6c394-718">Исправлена ошибка в определении типа области для командлета Set-AzActionRule.</span><span class="sxs-lookup"><span data-stu-id="6c394-718">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6c394-719">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6c394-719">Az.Network</span></span>
* <span data-ttu-id="6c394-720">Исправлен неправильный пример в справочной документации по командлету New-AzApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="6c394-720">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="6c394-721">В справочную документацию по командлету Get-AzNetworkWatcherPacketCapture добавлено примечание, посвященное извлечению всех свойств для записи пакетов.</span><span class="sxs-lookup"><span data-stu-id="6c394-721">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="6c394-722">В справочной документации по командлету Test-AzNetworkWatcherIPFlow исправлен пример: теперь он правильно перечисляет сетевые карты.</span><span class="sxs-lookup"><span data-stu-id="6c394-722">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="6c394-723">Улучшен анализ облачных исключений для отображения дополнительных сведений (при их наличии).</span><span class="sxs-lookup"><span data-stu-id="6c394-723">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="6c394-724">Улучшен анализ облачных исключений для обработки дополнительного типа исключения SDK.</span><span class="sxs-lookup"><span data-stu-id="6c394-724">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="6c394-725">Исправлено неправильное сопоставление моделей правил безопасности.</span><span class="sxs-lookup"><span data-stu-id="6c394-725">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="6c394-726">Добавлены свойства сетевого интерфейса для компонента частного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="6c394-726">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="6c394-727">Для интерфейса PSNetworkInterface добавлено свойство PrivateEndpoint с типом PSResourceId.</span><span class="sxs-lookup"><span data-stu-id="6c394-727">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="6c394-728">В PSNetworkInterfaceIPConfiguration добавлено свойство PrivateLinkConnectionProperties с типом PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="6c394-728">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="6c394-729">Добавлен новый класс модели: PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="6c394-729">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="6c394-730">Добавлен новый тип ApplicationRuleProtocolType "mssql" для ресурса Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="6c394-730">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="6c394-731">Поддержка многоканального подключения в Виртуальной глобальной сети:</span><span class="sxs-lookup"><span data-stu-id="6c394-731">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="6c394-732">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="6c394-732">New cmdlets</span></span>
        - <span data-ttu-id="6c394-733">New-AzVpnSiteLink;</span><span class="sxs-lookup"><span data-stu-id="6c394-733">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="6c394-734">New-AzVpnSiteLinkConnection;</span><span class="sxs-lookup"><span data-stu-id="6c394-734">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="6c394-735">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="6c394-735">Updated cmdlet:</span></span>
        - <span data-ttu-id="6c394-736">New-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="6c394-736">New-VpnSite</span></span>
        - <span data-ttu-id="6c394-737">Update-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="6c394-737">Update-VpnSite</span></span>
        - <span data-ttu-id="6c394-738">New-VpnConnection;</span><span class="sxs-lookup"><span data-stu-id="6c394-738">New-VpnConnection</span></span>
        - <span data-ttu-id="6c394-739">Update-VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="6c394-739">Update-VpnConnection</span></span>
* <span data-ttu-id="6c394-740">Исправлены документы с некоторыми примерами PowerShell для использования командлетов AZ вместо командлетов AzureRM.</span><span class="sxs-lookup"><span data-stu-id="6c394-740">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6c394-741">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6c394-741">Az.RecoveryServices</span></span>
* <span data-ttu-id="6c394-742">Для объекта AzureVMpolicy добавлен новый атрибут — ProtectedItemsCount.</span><span class="sxs-lookup"><span data-stu-id="6c394-742">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="6c394-743">Добавлены тесты для политики виртуальной машины и восстановления исходной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="6c394-743">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="6c394-744">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6c394-744">Az.Resources</span></span>
* <span data-ttu-id="6c394-745">Исправлена ошибка, при которой не удавалось вызвать командлет New-AzRoleAssignment без параметра Scope.</span><span class="sxs-lookup"><span data-stu-id="6c394-745">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6c394-746">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6c394-746">Az.ServiceFabric</span></span>
* <span data-ttu-id="6c394-747">Исправлена опечатка в примере в справочной документации по командлету Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="6c394-747">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="6c394-748">Добавлены новые командлеты для управления приложениями и службами:</span><span class="sxs-lookup"><span data-stu-id="6c394-748">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="6c394-749">New-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="6c394-749">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="6c394-750">New-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="6c394-750">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="6c394-751">New-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="6c394-751">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="6c394-752">New-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="6c394-752">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="6c394-753">Update-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="6c394-753">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="6c394-754">Get-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="6c394-754">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="6c394-755">Get-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="6c394-755">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="6c394-756">Get-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="6c394-756">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="6c394-757">Get-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="6c394-757">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="6c394-758">Remove-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="6c394-758">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="6c394-759">Remove-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="6c394-759">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="6c394-760">Remove-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="6c394-760">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="6c394-761">Remove-AzServiceFabricServic.</span><span class="sxs-lookup"><span data-stu-id="6c394-761">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="6c394-762">Пакет SDK для Service Fabric обновлен до версии 1.2.0, в которой используется версия API 2019-03-01 поставщика ресурсов Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="6c394-762">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="6c394-763">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="6c394-763">Az.SignalR</span></span>
* <span data-ttu-id="6c394-764">Добавлены командлеты Update, Restart, CheckNameAvailability и GetUsage.</span><span class="sxs-lookup"><span data-stu-id="6c394-764">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="6c394-765">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6c394-765">Az.Sql</span></span>
* <span data-ttu-id="6c394-766">Обновлен пример в справочной документации по командлету Get-AzSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="6c394-766">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="6c394-767">Добавлен пример виртуального ядра для командлета создания эластичного пула (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="6c394-767">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="6c394-768">Удалена проверка свойства EmailAddresses и того, что свойство EmailAdmins правильное в случае, если свойство EmailAddresses пустое в командлетах Set-AzSqlServerAdvancedThreatProtectionPolicy и Set-AzSqlDatabaseAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="6c394-768">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="6c394-769">Теперь, если существует несколько параметров диагностики, включающих категорию аудита, параметры аудита сервера и базы данных удаляются.</span><span class="sxs-lookup"><span data-stu-id="6c394-769">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="6c394-770">Исправлена проверка адресов электронной почты в нескольких командлетах оценки уязвимостей SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting и Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="6c394-770">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6c394-771">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6c394-771">Az.Storage</span></span>
* <span data-ttu-id="6c394-772">Обновлен пример в справочной документации по командлету Get-AzStorageAccountKey.</span><span class="sxs-lookup"><span data-stu-id="6c394-772">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="6c394-773">Теперь при отправке и загрузке файла Azure в конечном файле сохраняются свойства SMB исходного файла (атрибуты файла, время создания файла, время последней записи файла).</span><span class="sxs-lookup"><span data-stu-id="6c394-773">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="6c394-774">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6c394-774">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="6c394-775">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6c394-775">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="6c394-776">Исправлена операция отправки блочного BLOB-объекта, в которой происходили сбои свойств и метаданных в контейнере с включенной ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="6c394-776">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="6c394-777">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6c394-777">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="6c394-778">Добавлена поддержка управления общими папками Azure в API плоскости управления с помощью таких командлетов:</span><span class="sxs-lookup"><span data-stu-id="6c394-778">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="6c394-779">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="6c394-779">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="6c394-780">Get-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="6c394-780">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="6c394-781">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="6c394-781">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="6c394-782">Remove-AzRmStorageShare.</span><span class="sxs-lookup"><span data-stu-id="6c394-782">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6c394-783">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6c394-783">Az.Websites</span></span>
* <span data-ttu-id="6c394-784">Устранена проблема, из-за которой теги webapp удалялись при переносе приложения в новый ASP.</span><span class="sxs-lookup"><span data-stu-id="6c394-784">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="6c394-785">Теперь командлет Publish-AzureWebapp работает в Linux и Windows.</span><span class="sxs-lookup"><span data-stu-id="6c394-785">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="6c394-786">Обновлен пример в справочной документации по командлету Get-AzWebAppPublishingProfile.</span><span class="sxs-lookup"><span data-stu-id="6c394-786">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="6c394-787">2.6.0 — август 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6c394-787">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="6c394-788">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="6c394-788">General</span></span>
* <span data-ttu-id="6c394-789">Исправлены опечатки в модулях.</span><span class="sxs-lookup"><span data-stu-id="6c394-789">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6c394-790">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6c394-790">Az.Accounts</span></span>
* <span data-ttu-id="6c394-791">Добавлена поддержка назначаемого пользователем удостоверения MSI при проверке подлинности в Функциях Azure (№ 9479).</span><span class="sxs-lookup"><span data-stu-id="6c394-791">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="6c394-792">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="6c394-792">Az.Aks</span></span>
* <span data-ttu-id="6c394-793">Устранена проблема с выходными данными для Get-AzAks.</span><span class="sxs-lookup"><span data-stu-id="6c394-793">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="6c394-794">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9847.</span><span class="sxs-lookup"><span data-stu-id="6c394-794">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6c394-795">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6c394-795">Az.ApiManagement</span></span>
* <span data-ttu-id="6c394-796">исправлена проблема https://github.com/Azure/azure-powershell/issues/9351.</span><span class="sxs-lookup"><span data-stu-id="6c394-796">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="6c394-797">Обновлена версия NuGet для .NET, которая не накладывает ограничений на productId, apiId, groupId и userId.</span><span class="sxs-lookup"><span data-stu-id="6c394-797">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="6c394-798">**Get-AzApiManagementProduct**. Добавлена поддержка запросов к продуктам с помощью API.</span><span class="sxs-lookup"><span data-stu-id="6c394-798">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="6c394-799">**New-AzApiManagementApiRevision**. Устранена проблема, из-за которой не задавался параметр ApiRevisionDescription при создании новой редакции API https://github.com/Azure/azure-powershell/issues/9752.</span><span class="sxs-lookup"><span data-stu-id="6c394-799">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="6c394-800">Исправлено написание имени модели c PsApiManagementOAuth2AuthrozationServer на PsApiManagementOAuth2AuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="6c394-800">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6c394-801">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6c394-801">Az.Batch</span></span>
* <span data-ttu-id="6c394-802">Исправлена опечатка в написании Windows со строчной буквы в справочных сообщениях и документации.</span><span class="sxs-lookup"><span data-stu-id="6c394-802">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6c394-803">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6c394-803">Az.Cdn</span></span>
* <span data-ttu-id="6c394-804">Исправлена опечатка во вспомогательном приложении модуля CDN.</span><span class="sxs-lookup"><span data-stu-id="6c394-804">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6c394-805">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6c394-805">Az.Compute</span></span>
* <span data-ttu-id="6c394-806">Добавлен параметр VmssId в новый командлет Add New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="6c394-806">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="6c394-807">Добавлены параметры TerminateScheduledEvents и TerminateScheduledEventNotBeforeTimeoutInMinutes в New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="6c394-807">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="6c394-808">Добавлено свойство HyperVGeneration в объект образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6c394-808">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="6c394-809">Добавлены компоненты Host и HostGroup.</span><span class="sxs-lookup"><span data-stu-id="6c394-809">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="6c394-810">Новые командлеты:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="6c394-810">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="6c394-811">Параметр HostId добавлен в New-AzVMConfig и New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="6c394-811">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="6c394-812">Исправлен пример в документации по Invoke-AzVMRunCommand, в котором теперь используется правильное имя параметра.</span><span class="sxs-lookup"><span data-stu-id="6c394-812">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="6c394-813">Исправлено описание VolumeType в справочной документации по Set-AzVMDiskEncryptionExtension и Set-AzVmssDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="6c394-813">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6c394-814">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6c394-814">Az.DataFactory</span></span>
* <span data-ttu-id="6c394-815">Исправлена опечатка в написании Windows со строчной буквы в документации по New-AzDataFactoryEncryptValue.</span><span class="sxs-lookup"><span data-stu-id="6c394-815">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="6c394-816">Пакет SDK ADF для .NET обновлен до версии 4.1.2.</span><span class="sxs-lookup"><span data-stu-id="6c394-816">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="6c394-817">Добавлены параметры DataProxyIntegrationRuntimeName, DataProxyStagingLinkedServiceName и DataProxyStagingPath в командлет Set-AzureRmDataFactoryV2IntegrationRuntime, что позволяет настраивать локальную среду выполнения интеграции в качестве прокси-сервера для Azure-SSIS Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="6c394-817">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="6c394-818">Обновлены PSTriggerRun для отображения активированных конвейеров, сообщений и свойств и PSActivityRun для отображения типа действия.</span><span class="sxs-lookup"><span data-stu-id="6c394-818">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6c394-819">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6c394-819">Az.DataLakeStore</span></span>
* <span data-ttu-id="6c394-820">Устранена проблема, при которой Get-DataLakeStoreDeletedItem переставал отвечать на запросы при возникновении ошибок или удаленных исключений.</span><span class="sxs-lookup"><span data-stu-id="6c394-820">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6c394-821">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6c394-821">Az.EventHub</span></span>
* <span data-ttu-id="6c394-822">Исправлена проблема № 9658: опечатка в написании параметра VirtualNteworkRule у Set-AzEventHubNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="6c394-822">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="6c394-823">Исправлена проблема № 9558: в Set-AzEventHubNamespace используется PATCH вместо PUT.</span><span class="sxs-lookup"><span data-stu-id="6c394-823">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="6c394-824">В командлет Set-AzEventHubNamespace добавлен параметр EnableKafka.</span><span class="sxs-lookup"><span data-stu-id="6c394-824">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="6c394-825">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="6c394-825">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="6c394-826">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="6c394-826">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="6c394-827">Исправлено написание Azure со строчной буквы.</span><span class="sxs-lookup"><span data-stu-id="6c394-827">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6c394-828">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6c394-828">Az.Monitor</span></span>
* <span data-ttu-id="6c394-829">Исправлены неправильные имена параметров в справочной документации.</span><span class="sxs-lookup"><span data-stu-id="6c394-829">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6c394-830">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6c394-830">Az.Network</span></span>
* <span data-ttu-id="6c394-831">Обновлен New-AzPrivateLinkServiceIpConfig.</span><span class="sxs-lookup"><span data-stu-id="6c394-831">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="6c394-832">Параметр PublicIpAddress объявлен нерекомендуемым, так как он не используется на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="6c394-832">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="6c394-833">Добавлен необязательный параметр Primary, указывающий, является ли текущая IP-конфигурация основной.</span><span class="sxs-lookup"><span data-stu-id="6c394-833">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="6c394-834">Улучшена обработка исключений из-за ошибок запроса от пакета SDK. Устранена проблема, при которой исключения пакета SDK не обрабатывались правильно, из-за чего не отображались основные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="6c394-834">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="6c394-835">Настроена логика проверки для префикса IPv6 IP-адреса для проверки правильности длины префикса IPv6.</span><span class="sxs-lookup"><span data-stu-id="6c394-835">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="6c394-836">Обновлен Get-AzVirtualNetworkSubnetConfig: добавлен набор параметров для получения по идентификатору ресурса подсети.</span><span class="sxs-lookup"><span data-stu-id="6c394-836">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="6c394-837">Обновлено описание параметра Location для AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="6c394-837">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6c394-838">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6c394-838">Az.OperationalInsights</span></span>
* <span data-ttu-id="6c394-839">Обновлена документация по New-AzOperationalInsightsLinuxSyslogDataSource.</span><span class="sxs-lookup"><span data-stu-id="6c394-839">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="6c394-840">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="6c394-840">Added example</span></span>
    - <span data-ttu-id="6c394-841">Обновлено описание параметра -Name.</span><span class="sxs-lookup"><span data-stu-id="6c394-841">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="6c394-842">Добавлен пример для New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="6c394-842">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="6c394-843">Изменено описание параметра -Name для New-AzOperationalInsightsWindowsEventDataSource.</span><span class="sxs-lookup"><span data-stu-id="6c394-843">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6c394-844">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6c394-844">Az.RecoveryServices</span></span>
* <span data-ttu-id="6c394-845">Обновлен Get-AzRecoveryServicesBackupJobDetail.md.</span><span class="sxs-lookup"><span data-stu-id="6c394-845">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="6c394-846">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6c394-846">Az.Resources</span></span>
* <span data-ttu-id="6c394-847">Добавлена поддержка новой версии API 2019-05-10 для Microsoft.Resource.</span><span class="sxs-lookup"><span data-stu-id="6c394-847">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="6c394-848">Добавлена поддержка copy.count = 0 для переменных, ресурсов и свойств.</span><span class="sxs-lookup"><span data-stu-id="6c394-848">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="6c394-849">Ресурсы, у которых condition = false или copy.count = 0, будут удаляться в полном режиме.</span><span class="sxs-lookup"><span data-stu-id="6c394-849">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="6c394-850">В справочную документацию добавлен пример назначения политики на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="6c394-850">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6c394-851">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6c394-851">Az.ServiceBus</span></span>
* <span data-ttu-id="6c394-852">Исправлена проблема № 9658: опечатка в написании параметра VirtualNetworkRule В Set-AzServiceBusNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="6c394-852">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="6c394-853">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="6c394-853">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="6c394-854">Добавлена новая команда Test-AzServiceBusNameAvailability для проверки доступности имени для очереди и раздела.</span><span class="sxs-lookup"><span data-stu-id="6c394-854">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="6c394-855">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6c394-855">Az.ServiceFabric</span></span>
* <span data-ttu-id="6c394-856">Устранены ошибки командлета для добавления типа узла:</span><span class="sxs-lookup"><span data-stu-id="6c394-856">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="6c394-857">ошибка NullReferenceException, возникавшая, если у группы ресурсов были другие VMSS, не связанные с кластером Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="6c394-857">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="6c394-858">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8681.</span><span class="sxs-lookup"><span data-stu-id="6c394-858">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="6c394-859">Исправлена ошибка, из-за которой командлет завершился сбоем, если virtualNetwork находилась не в той группе ресурсов, к которой относится кластер.</span><span class="sxs-lookup"><span data-stu-id="6c394-859">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="6c394-860">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8407.</span><span class="sxs-lookup"><span data-stu-id="6c394-860">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="6c394-861">Командлет Add-AzServiceFabricApplicationCertificate объявлен нерекомендуемым.</span><span class="sxs-lookup"><span data-stu-id="6c394-861">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="6c394-862">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6c394-862">Az.Sql</span></span>
* <span data-ttu-id="6c394-863">Обновление документации по старым командлетам аудита.</span><span class="sxs-lookup"><span data-stu-id="6c394-863">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6c394-864">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6c394-864">Az.Storage</span></span>
* <span data-ttu-id="6c394-865">Обновлена справка по Get/Close-AzStorageFileHandle: в примеры добавлены сценарии использования командлетов и обновлено описание параметров.</span><span class="sxs-lookup"><span data-stu-id="6c394-865">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="6c394-866">Добавлена поддержка StandardBlobTier в операции отправки BLOB-объекта и копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="6c394-866">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="6c394-867">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6c394-867">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="6c394-868">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6c394-868">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="6c394-869">Добавлена поддержка приоритета восстановления в операцию копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="6c394-869">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="6c394-870">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6c394-870">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6c394-871">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6c394-871">Az.Websites</span></span>
* <span data-ttu-id="6c394-872">Добавлены уточнение для параметра -AppSettings в Set-AzWebApp и Set-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="6c394-872">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="6c394-873">2.5.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6c394-873">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6c394-874">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6c394-874">Az.Accounts</span></span>
* <span data-ttu-id="6c394-875">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c394-875">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="6c394-876">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="6c394-876">Az.ApplicationInsights</span></span>
* <span data-ttu-id="6c394-877">Исправлена опечатка в примере в документации по Remove-AzApplicationInsightsApiKey.</span><span class="sxs-lookup"><span data-stu-id="6c394-877">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="6c394-878">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6c394-878">Az.Automation</span></span>
* <span data-ttu-id="6c394-879">Исправлена опечатка в строке ресурса.</span><span class="sxs-lookup"><span data-stu-id="6c394-879">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="6c394-880">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6c394-880">Az.CognitiveServices</span></span>
* <span data-ttu-id="6c394-881">Добавлена поддержка NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="6c394-881">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6c394-882">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6c394-882">Az.Compute</span></span>
* <span data-ttu-id="6c394-883">Добавлены недостающие свойства (ComputerName, OsName, OsVersion и HyperVGeneration) для объекта представления экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6c394-883">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="6c394-884">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6c394-884">Az.ContainerRegistry</span></span>
* <span data-ttu-id="6c394-885">Исправлена опечатка в Remove-AzContainerRegistryReplication для параметра репликации.</span><span class="sxs-lookup"><span data-stu-id="6c394-885">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="6c394-886">См. подробнее: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="6c394-886">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6c394-887">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6c394-887">Az.DataFactory</span></span>
* <span data-ttu-id="6c394-888">Пакет SDK для ADF .NET обновлен до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="6c394-888">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="6c394-889">Исправлена опечатка в документации по Get-AzDataFactoryV2PipelineRun.</span><span class="sxs-lookup"><span data-stu-id="6c394-889">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6c394-890">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6c394-890">Az.EventHub</span></span>
* <span data-ttu-id="6c394-891">Добавлен новый командлет для создания маркера SAS: New-AzEventHubAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="6c394-891">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="6c394-892">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="6c394-892">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6c394-893">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6c394-893">Az.KeyVault</span></span>
* <span data-ttu-id="6c394-894">Добавлена поддержка для настройки параметра KeySize в политиках сертификатов.</span><span class="sxs-lookup"><span data-stu-id="6c394-894">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6c394-895">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6c394-895">Az.LogicApp</span></span>
* <span data-ttu-id="6c394-896">Get-AzIntegrationAccountMap теперь надлежащим образом выводит все типы сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="6c394-896">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="6c394-897">Добавлен новый параметр MapType для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="6c394-897">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="6c394-898">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="6c394-898">Az.ManagedServices</span></span>
* <span data-ttu-id="6c394-899">Добавлена поддержка API версии 2019-06-01 (общедоступная).</span><span class="sxs-lookup"><span data-stu-id="6c394-899">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6c394-900">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6c394-900">Az.Network</span></span>
* <span data-ttu-id="6c394-901">Добавлена поддержка частной конечной точки и службы приватного канала.</span><span class="sxs-lookup"><span data-stu-id="6c394-901">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="6c394-902">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="6c394-902">New cmdlets</span></span>
        - <span data-ttu-id="6c394-903">Set-AzPrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="6c394-903">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="6c394-904">Set-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="6c394-904">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="6c394-905">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="6c394-905">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6c394-906">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="6c394-906">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6c394-907">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="6c394-907">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6c394-908">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="6c394-908">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6c394-909">Test-AzPrivateLinkServiceVisibility.</span><span class="sxs-lookup"><span data-stu-id="6c394-909">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="6c394-910">Get-AzAutoApprovedPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="6c394-910">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="6c394-911">Обновлены следующие команды для функции: Флаг PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies в подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="6c394-911">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="6c394-912">Обновлены командлеты New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig.</span><span class="sxs-lookup"><span data-stu-id="6c394-912">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="6c394-913">Добавлен необязательный параметр -PrivateEndpointNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к частной конечной точке в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="6c394-913">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="6c394-914">Добавлен необязательный параметр -PrivateLinkServiceNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к службе приватного канала в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="6c394-914">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="6c394-915">Параметр ServiceName командлета AzPrivateLinkService был переименован на Name с псевдонимом ServiceName для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="6c394-915">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="6c394-916">Включен протокол ICMP для настройки правил безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="6c394-916">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="6c394-917">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="6c394-917">Updated cmdlets</span></span>
        - <span data-ttu-id="6c394-918">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="6c394-918">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="6c394-919">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="6c394-919">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="6c394-920">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="6c394-920">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="6c394-921">Добавлен ConnectionProtocolType (Ikev1/Ikev2) в качестве настраиваемого параметра для командлета New-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="6c394-921">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="6c394-922">Добавлен PrivateIpAddressVersion в LoadBalancerFrontendIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="6c394-922">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="6c394-923">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="6c394-923">Updated cmdlet:</span></span>
        - <span data-ttu-id="6c394-924">New-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="6c394-924">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="6c394-925">Add-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="6c394-925">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="6c394-926">Set-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="6c394-926">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="6c394-927">Команда New-AzApplicationGatewayProbeConfig Шлюза приложений обновлена для поддержки настраиваемого порта в зонде.</span><span class="sxs-lookup"><span data-stu-id="6c394-927">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="6c394-928">Обновлен командлет New-AzApplicationGatewayProbeConfig: добавлен необязательный параметр Port, который используется при проверке внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="6c394-928">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="6c394-929">Этот параметр применяется к номерам SKU Standard_V2 и WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="6c394-929">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6c394-930">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6c394-930">Az.OperationalInsights</span></span>
* <span data-ttu-id="6c394-931">Обновленная версия по умолчанию для сохраненных операций поиска имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="6c394-931">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="6c394-932">Исправлены ошибки при обработке регулярных выражений со значениями NULL в журналах.</span><span class="sxs-lookup"><span data-stu-id="6c394-932">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6c394-933">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6c394-933">Az.RecoveryServices</span></span>
* <span data-ttu-id="6c394-934">Обновлен файл Get-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="6c394-934">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="6c394-935">Обновлен файл Get-AzRecoveryServicesBackupContainer.md.</span><span class="sxs-lookup"><span data-stu-id="6c394-935">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="6c394-936">Обновлен файл Get-AzRecoveryServicesVault.md.</span><span class="sxs-lookup"><span data-stu-id="6c394-936">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="6c394-937">Обновлен файл Wait-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="6c394-937">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="6c394-938">Обновлен файл Set-AzRecoveryServicesVaultContext.md.</span><span class="sxs-lookup"><span data-stu-id="6c394-938">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="6c394-939">Обновлен файл Get-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="6c394-939">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="6c394-940">Обновлен файл Get-AzRecoveryServicesBackupRecoveryPoint.md.</span><span class="sxs-lookup"><span data-stu-id="6c394-940">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="6c394-941">Обновлен файл Restore-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="6c394-941">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="6c394-942">Обновлен вызов службы для отмены регистрации контейнера в общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="6c394-942">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="6c394-943">Обновлен файл Set-AzRecoveryServicesAsrAlertSetting.md.</span><span class="sxs-lookup"><span data-stu-id="6c394-943">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="6c394-944">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6c394-944">Az.Resources</span></span>
- <span data-ttu-id="6c394-945">Удален отсутствующий командлет, который упоминается в документации по New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="6c394-945">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="6c394-946">Обновлены командлеты политик для использования новой версии API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="6c394-946">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6c394-947">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6c394-947">Az.ServiceBus</span></span>
* <span data-ttu-id="6c394-948">Добавлен новый командлет для создания маркера SAS: New-AzServiceBusAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="6c394-948">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="6c394-949">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="6c394-949">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="6c394-950">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6c394-950">Az.Sql</span></span>
* <span data-ttu-id="6c394-951">Исправлены отсутствующие примеры для командлета Set-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="6c394-951">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="6c394-952">Исправлены заданные повторяющиеся проверки для оценки наличия уязвимостей без указания адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="6c394-952">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="6c394-953">Исправлена незначительная опечатка в сообщении предупреждения.</span><span class="sxs-lookup"><span data-stu-id="6c394-953">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6c394-954">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6c394-954">Az.Storage</span></span>
* <span data-ttu-id="6c394-955">Обновлен пример в справочной документации для использования командлетом Get-AzStorageAccount правильного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="6c394-955">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="6c394-956">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="6c394-956">Az.StorageSync</span></span>
* <span data-ttu-id="6c394-957">Добавлен командлет Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="6c394-957">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="6c394-958">Исправлена проблема № 9551, связанная с TierFilesOlderThanDays.</span><span class="sxs-lookup"><span data-stu-id="6c394-958">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6c394-959">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6c394-959">Az.Websites</span></span>
* <span data-ttu-id="6c394-960">Исправлена ошибка, при которой некоторые свойства SiteConfig не возвращались Get-AzWebApp и Set-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="6c394-960">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="6c394-961">Добавлен новый параметр Location в Get-AzDeletedWebApp и Restore-AzDeletedWebApp.</span><span class="sxs-lookup"><span data-stu-id="6c394-961">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="6c394-962">Исправлена ошибка, которая возникала при клонировании слотов веб-приложений с помощью командлета New-AzWebApp-IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="6c394-962">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="6c394-963">2.4.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6c394-963">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6c394-964">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6c394-964">Az.Accounts</span></span>
* <span data-ttu-id="6c394-965">Добавлена поддержка командлетов профиля.</span><span class="sxs-lookup"><span data-stu-id="6c394-965">Add support for profile cmdlets</span></span>
* <span data-ttu-id="6c394-966">Добавлена поддержка сред и плоскостей данных в созданных командлетах.</span><span class="sxs-lookup"><span data-stu-id="6c394-966">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="6c394-967">Исправлена ошибка, когда в командлетах плоскости данных в Windows PowerShell в некоторых случаях использовалась неправильная конечная точка.</span><span class="sxs-lookup"><span data-stu-id="6c394-967">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="6c394-968">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="6c394-968">Az.Advisor</span></span>
* <span data-ttu-id="6c394-969">Выпущена общедоступная версия Az.Advisor.</span><span class="sxs-lookup"><span data-stu-id="6c394-969">GA release of Az.Advisor</span></span>
* <span data-ttu-id="6c394-970">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="6c394-970">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6c394-971">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6c394-971">Az.ApiManagement</span></span>
* <span data-ttu-id="6c394-972">исправлена проблема https://github.com/Azure/azure-powershell/issues/8671.</span><span class="sxs-lookup"><span data-stu-id="6c394-972">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="6c394-973">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="6c394-973">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="6c394-974">Добавлена поддержка запрашивания подписок по пользователю и продукту.</span><span class="sxs-lookup"><span data-stu-id="6c394-974">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="6c394-975">Добавлена поддержка создания запросов с использованием области "/", "/apis", "/apis/echo-api".</span><span class="sxs-lookup"><span data-stu-id="6c394-975">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="6c394-976">Исправлены проблемы https://github.com/Azure/azure-powershell/issues/9307 и https://github.com/Azure/azure-powershell/issues/8432.</span><span class="sxs-lookup"><span data-stu-id="6c394-976">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="6c394-977">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="6c394-977">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="6c394-978">Добавлена поддержка указания ApiVersion и ApiVersionSetId при импорте API-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="6c394-978">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6c394-979">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6c394-979">Az.Automation</span></span>
* <span data-ttu-id="6c394-980">Исправлена ошибка командлета Set-AzAutomationConnectionFieldValue при обработке строкового значения.</span><span class="sxs-lookup"><span data-stu-id="6c394-980">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6c394-981">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6c394-981">Az.Compute</span></span>
* <span data-ttu-id="6c394-982">В New AzImageConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="6c394-982">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6c394-983">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6c394-983">Az.DataFactory</span></span>
* <span data-ttu-id="6c394-984">Обновление выходных данных командлетов ADF, предназначенных для получения числа выполнений действий, конвейеров и триггеров, для поддержки канала Select-Object.</span><span class="sxs-lookup"><span data-stu-id="6c394-984">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6c394-985">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6c394-985">Az.EventGrid</span></span>
* <span data-ttu-id="6c394-986">Исправлена опечатка в документации по командлету New-AzEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="6c394-986">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6c394-987">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6c394-987">Az.IotHub</span></span>
* <span data-ttu-id="6c394-988">Добавлена поддержка повторного создания ключей политики авторизации.</span><span class="sxs-lookup"><span data-stu-id="6c394-988">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6c394-989">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6c394-989">Az.Network</span></span>
* <span data-ttu-id="6c394-990">К тегам общедоступного IP-адреса добавлен тег RoutingPreference.</span><span class="sxs-lookup"><span data-stu-id="6c394-990">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="6c394-991">Улучшены примеры для справочной документации по командлету Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="6c394-991">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6c394-992">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6c394-992">Az.PolicyInsights</span></span>
* <span data-ttu-id="6c394-993">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="6c394-993">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="6c394-994">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9446.</span><span class="sxs-lookup"><span data-stu-id="6c394-994">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6c394-995">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6c394-995">Az.OperationalInsights</span></span>
* <span data-ttu-id="6c394-996">Исправленная модель источника данных CustomLog возвращена в командлет Get-AzOperationalInsightsDataSource.</span><span class="sxs-lookup"><span data-stu-id="6c394-996">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6c394-997">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6c394-997">Az.RecoveryServices</span></span>
* <span data-ttu-id="6c394-998">Выпущено исправление для команды get-policy для виртуальных машин IaaS.</span><span class="sxs-lookup"><span data-stu-id="6c394-998">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="6c394-999">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6c394-999">Az.Resources</span></span>
    - <span data-ttu-id="6c394-1000">Исправлен текст справки по параметру Get-AzPolicyState -Top.</span><span class="sxs-lookup"><span data-stu-id="6c394-1000">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="6c394-1001">Добавлена поддержка разбиения по страницам на стороне клиента для Get-AzPolicyAlias.</span><span class="sxs-lookup"><span data-stu-id="6c394-1001">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="6c394-1002">Добавлены новые параметры для Set-AzPolicyAssignment, -PolicyParameters и -PolicyParametersObject.</span><span class="sxs-lookup"><span data-stu-id="6c394-1002">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="6c394-1003">Добавлен ряд обновлений документов и примеров для командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="6c394-1003">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6c394-1004">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6c394-1004">Az.ServiceBus</span></span>
* <span data-ttu-id="6c394-1005">Исправление ошибки № 4938: командлет New-AzureRmServiceBusQueue возвращает ответ BadRequest (Недопустимый запрос) при задании значения MaxSizeInMegabytes.</span><span class="sxs-lookup"><span data-stu-id="6c394-1005">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="6c394-1006">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6c394-1006">Az.Sql</span></span>
* <span data-ttu-id="6c394-1007">Из выпуска предварительной версии в выпуск общедоступной версии добавлены командлеты группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="6c394-1007">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="6c394-1008">Поддержка аудита Azure SQL Server и баз данных с помощью новых командлетов:</span><span class="sxs-lookup"><span data-stu-id="6c394-1008">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="6c394-1009">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="6c394-1009">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="6c394-1010">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="6c394-1010">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="6c394-1011">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="6c394-1011">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="6c394-1012">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="6c394-1012">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="6c394-1013">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="6c394-1013">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="6c394-1014">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="6c394-1014">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="6c394-1015">Из параметров оценки уязвимостей удалены ограничения, касающиеся электронной почты.</span><span class="sxs-lookup"><span data-stu-id="6c394-1015">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6c394-1016">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6c394-1016">Az.Storage</span></span>
* <span data-ttu-id="6c394-1017">Два параметра в указанном ниже командлете — -IndexDocument и -ErrorDocument404Path, — которые ранее были обязательными, стали необязательными:</span><span class="sxs-lookup"><span data-stu-id="6c394-1017">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="6c394-1018">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="6c394-1018">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="6c394-1019">Обновлена справка по командлету Get-AzStorageBlobContent: добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="6c394-1019">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="6c394-1020">При сбое выполнения командлета с ошибкой StorageException отображаются дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="6c394-1020">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="6c394-1021">Добавлена поддержка создания или обновления учетной записи хранения с использованием проверки подлинности AAD DS для службы "Файлы Azure".</span><span class="sxs-lookup"><span data-stu-id="6c394-1021">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="6c394-1022">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6c394-1022">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="6c394-1023">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6c394-1023">Set-AzStorageAccount</span></span>
* <span data-ttu-id="6c394-1024">Добавлена поддержка перечисления или закрытия дескрипторов файлов для общей папки, каталога файлов или файла:</span><span class="sxs-lookup"><span data-stu-id="6c394-1024">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="6c394-1025">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="6c394-1025">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="6c394-1026">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="6c394-1026">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="6c394-1027">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="6c394-1027">Az.StorageSync</span></span>
* <span data-ttu-id="6c394-1028">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="6c394-1028">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="6c394-1029">2.3.2 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6c394-1029">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6c394-1030">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6c394-1030">Az.Accounts</span></span>
* <span data-ttu-id="6c394-1031">Исправлена ошибка, связанная с использованием неправильного URL-адреса для вызовов функций.</span><span class="sxs-lookup"><span data-stu-id="6c394-1031">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="6c394-1032">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8983.</span><span class="sxs-lookup"><span data-stu-id="6c394-1032">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="6c394-1033">Устранена проблема с псевдонимами из AzureRM для командлетов Az.</span><span class="sxs-lookup"><span data-stu-id="6c394-1033">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="6c394-1034">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="6c394-1034">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="6c394-1035">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest.</span><span class="sxs-lookup"><span data-stu-id="6c394-1035">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6c394-1036">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6c394-1036">Az.Compute</span></span>
* <span data-ttu-id="6c394-1037">Простые наборы параметров New-AzVm и New-AzVmss теперь принимают параметр ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="6c394-1037">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="6c394-1038">Исправлена опечатка в справочной документации по New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="6c394-1038">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="6c394-1039">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="6c394-1039">Az.Dns</span></span>
* <span data-ttu-id="6c394-1040">Исправлена опечатка в справочных примерах по использованию Set-AzDnsZone.</span><span class="sxs-lookup"><span data-stu-id="6c394-1040">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6c394-1041">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6c394-1041">Az.EventGrid</span></span>
* <span data-ttu-id="6c394-1042">Обновлен для использования API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="6c394-1042">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="6c394-1043">Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="6c394-1043">New cmdlets:</span></span>
    - <span data-ttu-id="6c394-1044">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="6c394-1044">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="6c394-1045">Создает домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="6c394-1045">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="6c394-1046">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="6c394-1046">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="6c394-1047">Возвращает сведения о домене Сетки событий или список всех доменов Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="6c394-1047">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="6c394-1048">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="6c394-1048">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="6c394-1049">Удаляет домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="6c394-1049">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="6c394-1050">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="6c394-1050">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="6c394-1051">Повторно создает ключ общего доступа для домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="6c394-1051">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="6c394-1052">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="6c394-1052">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="6c394-1053">Возвращает ключи общего доступа, используемые для публикации событий в домене Сетки событий.</span><span class="sxs-lookup"><span data-stu-id="6c394-1053">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="6c394-1054">New-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="6c394-1054">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="6c394-1055">Создает раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="6c394-1055">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="6c394-1056">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="6c394-1056">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="6c394-1057">Возвращает сведения о разделе домена Сетки событий или список всех разделов определенного домена Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="6c394-1057">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="6c394-1058">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="6c394-1058">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="6c394-1059">Удаляет раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="6c394-1059">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="6c394-1060">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="6c394-1060">Updated cmdlets:</span></span>
    - <span data-ttu-id="6c394-1061">New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="6c394-1061">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="6c394-1062">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для нового домена Сетки событий и раздела домена Сетки событий и позволяющие создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="6c394-1062">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="6c394-1063">Добавляют новые обязательные параметры для указания имени нового домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="6c394-1063">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="6c394-1064">Добавляют новые наборы параметров для доменов и разделов домена и позволяют повторно использовать существующие параметры (например, EndPointType, SubjectBeginsWith и т. д.).</span><span class="sxs-lookup"><span data-stu-id="6c394-1064">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="6c394-1065">Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="6c394-1065">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="6c394-1066">срока действия подписки на событие;</span><span class="sxs-lookup"><span data-stu-id="6c394-1066">Event subscription expiration date,</span></span>
            - <span data-ttu-id="6c394-1067">параметров расширенной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="6c394-1067">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="6c394-1068">Добавляют новое перечисление для ServiceBusQueue в качестве места назначения.</span><span class="sxs-lookup"><span data-stu-id="6c394-1068">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="6c394-1069">Запрещают использование значение All в параметре -IncludedEventType и заменяют его следующим:</span><span class="sxs-lookup"><span data-stu-id="6c394-1069">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="6c394-1070">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="6c394-1070">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="6c394-1071">Добавляют новые необязательные параметры (Top, ODataQuery и NextLink) для поддержки разбиения на страницы и фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="6c394-1071">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="6c394-1072">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="6c394-1072">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="6c394-1073">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для домена Сетки событий и раздела домена Сетки событий и позволяющие удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="6c394-1073">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="6c394-1074">Добавляют новые обязательные параметры для указания имени домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="6c394-1074">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6c394-1075">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6c394-1075">Az.FrontDoor</span></span>
* <span data-ttu-id="6c394-1076">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="6c394-1076">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="6c394-1077">Добавляет поддержку преобразований и новое значение оператора автозавершения (RegEx).</span><span class="sxs-lookup"><span data-stu-id="6c394-1077">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="6c394-1078">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="6c394-1078">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="6c394-1079">Добавляет новые значения автозавершения.</span><span class="sxs-lookup"><span data-stu-id="6c394-1079">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6c394-1080">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6c394-1080">Az.Network</span></span>
* <span data-ttu-id="6c394-1081">Добавляет поддержку ресурса шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="6c394-1081">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="6c394-1082">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="6c394-1082">New cmdlets</span></span>
        - <span data-ttu-id="6c394-1083">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="6c394-1083">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="6c394-1084">Добавляет AvailablePrivateEndpointType.</span><span class="sxs-lookup"><span data-stu-id="6c394-1084">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="6c394-1085">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="6c394-1085">New cmdlets</span></span> 
        - <span data-ttu-id="6c394-1086">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="6c394-1086">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="6c394-1087">Добавляет PrivatePrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="6c394-1087">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="6c394-1088">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="6c394-1088">New cmdlets</span></span> 
        - <span data-ttu-id="6c394-1089">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6c394-1089">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="6c394-1090">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6c394-1090">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="6c394-1091">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6c394-1091">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="6c394-1092">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6c394-1092">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="6c394-1093">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6c394-1093">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="6c394-1094">Добавляет PrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="6c394-1094">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="6c394-1095">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="6c394-1095">New cmdlets</span></span>
        - <span data-ttu-id="6c394-1096">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6c394-1096">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="6c394-1097">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6c394-1097">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="6c394-1098">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6c394-1098">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="6c394-1099">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="6c394-1099">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="6c394-1100">Обновлены следующие команды для функции: флаг UseLocalAzureIpAddress для VPN-подключения.</span><span class="sxs-lookup"><span data-stu-id="6c394-1100">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="6c394-1101">Обновлен командлет New-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="6c394-1101">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="6c394-1102">Обновлен командлет Set-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="6c394-1102">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="6c394-1103">В пиринг ExpressRoute добавлено поле только для чтения PeeredConnections.</span><span class="sxs-lookup"><span data-stu-id="6c394-1103">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="6c394-1104">В ExpressRoute добавлено поле только для чтения GlobalReachEnabled.</span><span class="sxs-lookup"><span data-stu-id="6c394-1104">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="6c394-1105">Добавлен атрибут в рамках критического изменения, отменяющего статус устаревшего поля AllowGlobalReach в модели ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="6c394-1105">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="6c394-1106">Исправлена проблема, связанная с ошибкой 8756, при использовании TargetListenerID с командлетами AzApplicationGatewayRedirectConfiguration.</span><span class="sxs-lookup"><span data-stu-id="6c394-1106">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="6c394-1107">Исправлена ошибка в New-AzApplicationGatewayPathRuleConfig, не позволявшая задавать набор правил повторного создания.</span><span class="sxs-lookup"><span data-stu-id="6c394-1107">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="6c394-1108">Исправлено отображение VirtualNetworkTaps в NetworkInterfaceIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="6c394-1108">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="6c394-1109">Исправлены командлеты Cortex Get для отображения всех частей.</span><span class="sxs-lookup"><span data-stu-id="6c394-1109">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="6c394-1110">Исправлено создание ссылок VirtualHub для ExpressRouteGateways и VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="6c394-1110">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="6c394-1111">В AzureFirewall и NatGateway добавлена поддержка Зон доступности.</span><span class="sxs-lookup"><span data-stu-id="6c394-1111">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="6c394-1112">Добавлен командлет Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="6c394-1112">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="6c394-1113">Добавлена поддержка нескольких общедоступных IP-адресов для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="6c394-1113">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="6c394-1114">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="6c394-1114">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="6c394-1115">Добавлен параметр -PublicIpAddress, который принимает один или несколько объектов общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="6c394-1115">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="6c394-1116">Добавлен параметр -VirtualNetwork, который принимает объект виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="6c394-1116">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="6c394-1117">Добавлены методы AddPublicIpAddress и RemovePublicIpAddress для объекта брандмауэра. Они принимают объект общедоступного IP-адреса в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="6c394-1117">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="6c394-1118">Не рекомендуется использовать параметры -PublicIpName и -VirtualNetworkName.</span><span class="sxs-lookup"><span data-stu-id="6c394-1118">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="6c394-1119">Обновлены следующие команды для функции: В параметрах проверки подлинности AAD VPN-клиента задан ресурс шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="6c394-1119">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="6c394-1120">Обновлен командлет New-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="6c394-1120">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="6c394-1121">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="6c394-1121">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="6c394-1122">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр-переключатель RemoveAadAuthentication для удаления в шлюзе параметров проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="6c394-1122">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6c394-1123">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6c394-1123">Az.OperationalInsights</span></span>
* <span data-ttu-id="6c394-1124">Добавлена поддержка SKU **pergb2018** в команде New-AzureRmOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="6c394-1124">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="6c394-1125">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6c394-1125">Az.Resources</span></span>
* <span data-ttu-id="6c394-1126">Поддержка дополнительных вариантов экспорта шаблона.</span><span class="sxs-lookup"><span data-stu-id="6c394-1126">Support for additional Template Export options</span></span>
    - <span data-ttu-id="6c394-1127">В Export-AzResourceGroup добавлен параметр -SkipResourceNameParameterization.</span><span class="sxs-lookup"><span data-stu-id="6c394-1127">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="6c394-1128">В Export-AzResourceGroup добавлен параметр -SkipAllParameterization.</span><span class="sxs-lookup"><span data-stu-id="6c394-1128">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="6c394-1129">В Export-AzResourceGroup добавлен параметр -Resource для фильтрации экспортированных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6c394-1129">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6c394-1130">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6c394-1130">Az.ServiceFabric</span></span>
* <span data-ttu-id="6c394-1131">Исправлена ошибка, связанная с получением иногда неправильных отпечатков при добавлении сертификата ByExistingKeyVault.</span><span class="sxs-lookup"><span data-stu-id="6c394-1131">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="6c394-1132">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6c394-1132">Az.Sql</span></span>
* <span data-ttu-id="6c394-1133">Исправлен суффикс конечной точки хранилища службы "Расширенная защита от угроз Azure".</span><span class="sxs-lookup"><span data-stu-id="6c394-1133">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="6c394-1134">Исправлена ошибка, связанная с возможностью пакета "Расширенная защита данных" переопределять политику службы "Расширенная защита от угроз".</span><span class="sxs-lookup"><span data-stu-id="6c394-1134">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="6c394-1135">Новые командлеты для Management.Sql позволяют клиентам добавлять ключи TDE и задавать средство защиты TDE для управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="6c394-1135">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="6c394-1136">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6c394-1136">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="6c394-1137">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6c394-1137">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="6c394-1138">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6c394-1138">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="6c394-1139">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="6c394-1139">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="6c394-1140">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="6c394-1140">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6c394-1141">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6c394-1141">Az.Storage</span></span>
* <span data-ttu-id="6c394-1142">Поддержка класса Kind в FileStorage и значения Premium_ZRS в SkuName при создании учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="6c394-1142">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="6c394-1143">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6c394-1143">New-AzStorageAccount</span></span>
* <span data-ttu-id="6c394-1144">Уточнено описание командлета неизменности BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="6c394-1144">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="6c394-1145">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="6c394-1145">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6c394-1146">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6c394-1146">Az.Websites</span></span>
* <span data-ttu-id="6c394-1147">Оптимизирует Get-AzWebAppCertificate для фильтрации по группе ресурсов на сервере, а не в клиенте.</span><span class="sxs-lookup"><span data-stu-id="6c394-1147">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="6c394-1148">Добавляет параметр-переключатель - UseDisasterRecovery в Get AzWebAppSnapshot.</span><span class="sxs-lookup"><span data-stu-id="6c394-1148">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="6c394-1149">2.2.0 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6c394-1149">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="6c394-1150">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6c394-1150">Az.Cdn</span></span>
* <span data-ttu-id="6c394-1151">Обновлены командлеты для поддержки функции rulesEngine на основе API версии 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="6c394-1151">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6c394-1152">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6c394-1152">Az.Compute</span></span>
* <span data-ttu-id="6c394-1153">Добавлен параметр `NoWait`, который запускает операцию и немедленно возвращает значение еще до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="6c394-1153">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="6c394-1154">Обновлены командлеты:   Export-AzLogAnalyticRequestRateByInterval; Export-AzLogAnalyticThrottledRequest; Remove-AzVM; Remove-AzVMAccessExtension; Remove-AzVMAEMExtension; Remove-AzVMChefExtension; Remove-AzVMCustomScriptExtension; Remove-AzVMDiagnosticsExtension; Remove-AzVMDiskEncryptionExtension; Remove-AzVMDscExtension; Remove-AzVMSqlServerExtension; Restart-AzVM; Set-AzVM; Set-AzVMAccessExtension; Set-AzVMADDomainExtension; Set-AzVMAEMExtension; Set-AzVMBginfoExtension; Set-AzVMChefExtension; Set-AzVMCustomScriptExtension; Set-AzVMDiagnosticsExtension; Set-AzVMDscExtension; Set-AzVMExtension; Start-AzVM; Stop-AzVM; Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="6c394-1154">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6c394-1155">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6c394-1155">Az.EventHub</span></span>
* <span data-ttu-id="6c394-1156">Исправлена ошибка № 9231. Командлет Get-AzEventHubNamespace не возвращал теги.</span><span class="sxs-lookup"><span data-stu-id="6c394-1156">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="6c394-1157">Исправлена ошибка № 9230. Командлет Get-AzEventHubNamespace возвращал значение ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="6c394-1157">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6c394-1158">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6c394-1158">Az.Network</span></span>
* <span data-ttu-id="6c394-1159">Обновлены параметры ResourceId и InputObject для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="6c394-1159">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="6c394-1160">Добавлены псевдонимы для параметров ResourceId и InputObject.</span><span class="sxs-lookup"><span data-stu-id="6c394-1160">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6c394-1161">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6c394-1161">Az.PolicyInsights</span></span>
* <span data-ttu-id="6c394-1162">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyEvent.</span><span class="sxs-lookup"><span data-stu-id="6c394-1162">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6c394-1163">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6c394-1163">Az.RecoveryServices</span></span>
* <span data-ttu-id="6c394-1164">Минимальный срок хранения политики IaaSVM изменился с 1 до 7 дней.</span><span class="sxs-lookup"><span data-stu-id="6c394-1164">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6c394-1165">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6c394-1165">Az.ServiceBus</span></span>
* <span data-ttu-id="6c394-1166">Исправлена ошибка № 9182. Командлет Get-AzServiceBusNamespace возвращал ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="6c394-1166">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6c394-1167">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6c394-1167">Az.ServiceFabric</span></span>
* <span data-ttu-id="6c394-1168">Исправлена опечатка в сообщении об ошибке для командлета Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="6c394-1168">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="6c394-1169">Добавлен отсутствующий символ в командных строках Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="6c394-1169">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="6c394-1170">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6c394-1170">Az.Sql</span></span>
* <span data-ttu-id="6c394-1171">Для командлета New-AzureSqlInstance добавлен параметр DnsZonePartner, обеспечивающий поддержку AutoDr для Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="6c394-1171">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="6c394-1172">Командлет Get-AzSqlDatabaseSecureConnectionPolicy объявлен неподдерживаемым.</span><span class="sxs-lookup"><span data-stu-id="6c394-1172">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="6c394-1173">Командлеты обнаружения угроз переименованы в командлеты Расширенной защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="6c394-1173">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="6c394-1174">Параметры -StorageSizeInGB и -LicenseType командлета New-AzSqlInstance теперь необязательны.</span><span class="sxs-lookup"><span data-stu-id="6c394-1174">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6c394-1175">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6c394-1175">Az.Websites</span></span>
* <span data-ttu-id="6c394-1176">Исправлены проблемы, когда удалялись теги при использовании Set-AzWebApp и Set-AzWebAppSlot со свойством -WebApp.</span><span class="sxs-lookup"><span data-stu-id="6c394-1176">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="6c394-1177">2.1.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6c394-1177">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="6c394-1178">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6c394-1178">Az.ApiManagement</span></span>
* <span data-ttu-id="6c394-1179">Созданы командлеты для управления диагностикой в глобальной области и в области API.</span><span class="sxs-lookup"><span data-stu-id="6c394-1179">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="6c394-1180">**Get-AzApiManagementDiagnostic** — получение диагностики, заданной глобально или на уровне области API.</span><span class="sxs-lookup"><span data-stu-id="6c394-1180">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="6c394-1181">**New-AzApiManagementDiagnostic** — создание диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="6c394-1181">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="6c394-1182">**New-AzApiManagementHttpMessageDiagnostic** — создание параметра диагностики, для которого регистрируются заголовки и размер байтов тела.</span><span class="sxs-lookup"><span data-stu-id="6c394-1182">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="6c394-1183">**New-AzApiManagementPipelineDiagnosticSetting** — создание параметров диагностики для сообщений HTTP, поступающих в шлюз или исходящих из него.</span><span class="sxs-lookup"><span data-stu-id="6c394-1183">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="6c394-1184">**New-AzApiManagementSamplingSetting** — создание параметра выборки для запросов и ответов касательно диагностики.</span><span class="sxs-lookup"><span data-stu-id="6c394-1184">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="6c394-1185">**Remove-AzApiManagementDiagnostic** — удаление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="6c394-1185">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="6c394-1186">**Set-AzApiManagementDiagnostic** — обновление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="6c394-1186">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="6c394-1187">Созданы командлеты для управления кэшем в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="6c394-1187">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="6c394-1188">**Get-AzApiManagementCache** — получение сведений о кэше, указанном идентификатором, или обо всех кэшах.</span><span class="sxs-lookup"><span data-stu-id="6c394-1188">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="6c394-1189">**New-AzApiManagementCache** — создание кэша по умолчанию или кэша в определенном регионе Azure.</span><span class="sxs-lookup"><span data-stu-id="6c394-1189">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="6c394-1190">**Remove-AzApiManagementCache** — удаление кэша.</span><span class="sxs-lookup"><span data-stu-id="6c394-1190">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="6c394-1191">**Update-AzApiManagementCache** — обновление кэша.</span><span class="sxs-lookup"><span data-stu-id="6c394-1191">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="6c394-1192">Созданы командлеты для управления схемой API.</span><span class="sxs-lookup"><span data-stu-id="6c394-1192">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="6c394-1193">**New-AzApiManagementSchema** — создание схемы для API.</span><span class="sxs-lookup"><span data-stu-id="6c394-1193">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="6c394-1194">**Get-AzApiManagementSchema** — получение схем, настроенных в API.</span><span class="sxs-lookup"><span data-stu-id="6c394-1194">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="6c394-1195">**Remove-AzApiManagementSchema** — удаление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="6c394-1195">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="6c394-1196">**Set-AzApiManagementSchema** — обновление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="6c394-1196">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="6c394-1197">Создан командлет для создания токена пользователя.</span><span class="sxs-lookup"><span data-stu-id="6c394-1197">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="6c394-1198">**New-AzApiManagementUserToken** — создание токена пользователя, по умолчанию действительного в течение 8 часов. С помощью этого командлета можно создавать токен для пользователя GIT.</span><span class="sxs-lookup"><span data-stu-id="6c394-1198">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="6c394-1199">Создан командлет для получения состояния сети.</span><span class="sxs-lookup"><span data-stu-id="6c394-1199">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="6c394-1200">**Get-AzApiManagementNetworkStatus** — получение состояния подключения сети ресурсов, от которых зависит служба "Управление API".</span><span class="sxs-lookup"><span data-stu-id="6c394-1200">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="6c394-1201">Это полезно при развертывании службы ApiManagement в виртуальной сети и проверке того, не нарушена ли какая-либо из зависимостей.</span><span class="sxs-lookup"><span data-stu-id="6c394-1201">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="6c394-1202">Обновлен командлет **New-AzApiManagement** для управления службой ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="6c394-1202">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="6c394-1203">Добавлена поддержка нового SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="6c394-1203">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="6c394-1204">Добавлена поддержка для включения флага EnableClientCertificate в SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="6c394-1204">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="6c394-1205">Новый командлет **New-AzApiManagementSslSetting** позволяет настраивать параметр TLS/SSL для сервера (Backend) и внешнего интерфейса (Frontend).</span><span class="sxs-lookup"><span data-stu-id="6c394-1205">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="6c394-1206">Его также можно использовать для настройки Ciphers как 3DES, в ServerProtocols как Http2 для внешнего интерфейса (Frontend) службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="6c394-1206">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="6c394-1207">Добавлена поддержка настройки имени узла DeveloperPortal в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="6c394-1207">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="6c394-1208">Обновлен командлет **Get-AzApiManagementSsoToken** для извлечения объекта PsApiManagement в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="6c394-1208">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="6c394-1209">Обновлен командлет для отображения встроенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="6c394-1209">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="6c394-1210">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Код ошибки: ValidationError. Сообщение об ошибке: "Некоторые поля содержат неправильные значения". Сведения об ошибке: [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="6c394-1210">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="6c394-1211">Обновлен командлет **Export-AzApiManagementApi** для экспортирования программных интерфейсов в формате OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="6c394-1211">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="6c394-1212">Обновлен командлет **Import-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="6c394-1212">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="6c394-1213">Для импортирования API из спецификации документа OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="6c394-1213">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="6c394-1214">Для переопределения свойства PsApiManagementSchema, указанного в любом документе (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="6c394-1214">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="6c394-1215">Для переопределения свойства ServiceUrl, указанного в любом документе.</span><span class="sxs-lookup"><span data-stu-id="6c394-1215">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="6c394-1216">Обновлен командлет **Get-AzApiManagementPolicy** для возврата политики в формате, экранированном не для XML, с использованием rawxml.</span><span class="sxs-lookup"><span data-stu-id="6c394-1216">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="6c394-1217">Обновлен командлет **Set-AzApiManagementPolicy**. Он принимает политику в формате, экранированном не для XML, с использованием rawxml и в формате, экранированном для XML, с использованием XML.</span><span class="sxs-lookup"><span data-stu-id="6c394-1217">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="6c394-1218">Обновлен командлет **New-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="6c394-1218">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="6c394-1219">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="6c394-1219">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="6c394-1220">Для создания API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="6c394-1220">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="6c394-1221">Для клонирования API с использованием значений SourceApiId и SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="6c394-1221">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="6c394-1222">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="6c394-1222">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="6c394-1223">Обновлен командлет **Set-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="6c394-1223">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="6c394-1224">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="6c394-1224">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="6c394-1225">Для обновления API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="6c394-1225">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="6c394-1226">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="6c394-1226">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="6c394-1227">Обновлен командлет **New-AzApiManagementRevision**:</span><span class="sxs-lookup"><span data-stu-id="6c394-1227">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="6c394-1228">Для клонирования (копирования тегов, продуктов, операций и политик) существующей редакции с использованием SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="6c394-1228">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="6c394-1229">Новая редакция предполагает родительский идентификатор ApiId.</span><span class="sxs-lookup"><span data-stu-id="6c394-1229">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="6c394-1230">Для предоставления ApiRevisionDescription.</span><span class="sxs-lookup"><span data-stu-id="6c394-1230">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="6c394-1231">Для переопределения значения ServiceUrl при клонировании API.</span><span class="sxs-lookup"><span data-stu-id="6c394-1231">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="6c394-1232">Обновлен командлет **New-AzApiManagementIdentityProvider**:</span><span class="sxs-lookup"><span data-stu-id="6c394-1232">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="6c394-1233">Для настройки AAD или AADB2C с Authority.</span><span class="sxs-lookup"><span data-stu-id="6c394-1233">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="6c394-1234">Для установки политик SignupPolicy, SigninPolicy, ProfileEditingPolicy и PasswordResetPolicy.</span><span class="sxs-lookup"><span data-stu-id="6c394-1234">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="6c394-1235">Обновлен командлет **New-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="6c394-1235">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="6c394-1236">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="6c394-1236">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="6c394-1237">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="6c394-1237">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="6c394-1238">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="6c394-1238">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="6c394-1239">Обновлен командлет **Set-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="6c394-1239">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="6c394-1240">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="6c394-1240">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="6c394-1241">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="6c394-1241">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="6c394-1242">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="6c394-1242">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="6c394-1243">Следующие командлеты обновлены, чтобы принимать значение ResourceId в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="6c394-1243">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="6c394-1244">New-AzApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="6c394-1244">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="6c394-1245">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="6c394-1245">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="6c394-1246">Get-AzApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="6c394-1246">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="6c394-1247">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="6c394-1247">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="6c394-1248">Get-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="6c394-1248">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="6c394-1249">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="6c394-1249">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="6c394-1250">Get-AzApiManagementAuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="6c394-1250">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="6c394-1251">Get-AzApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="6c394-1251">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="6c394-1252">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="6c394-1252">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="6c394-1253">Get-AzApiManagementCertificate.</span><span class="sxs-lookup"><span data-stu-id="6c394-1253">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="6c394-1254">Remove-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="6c394-1254">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="6c394-1255">Remove-AzApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="6c394-1255">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6c394-1256">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6c394-1256">Az.Automation</span></span>
* <span data-ttu-id="6c394-1257">Обновлен командлет Get-AzAutomationJobOutputRecord для обработки значений в формате JSON и в виде текстовой записи.</span><span class="sxs-lookup"><span data-stu-id="6c394-1257">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="6c394-1258">исправлена проблема https://github.com/Azure/azure-powershell/issues/7977.</span><span class="sxs-lookup"><span data-stu-id="6c394-1258">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="6c394-1259">исправлена проблема https://github.com/Azure/azure-powershell/issues/8600.</span><span class="sxs-lookup"><span data-stu-id="6c394-1259">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="6c394-1260">Поведение командлета Start-AzAutomationDscCompilationJob изменено так, чтобы сразу же запустить задание, а не ждать его завершения.</span><span class="sxs-lookup"><span data-stu-id="6c394-1260">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="6c394-1261">исправлена проблема https://github.com/Azure/azure-powershell/issues/8347.</span><span class="sxs-lookup"><span data-stu-id="6c394-1261">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="6c394-1262">Исправлен командлет Get-AzAutomationDscNode, возвращающий все узлы при использовании -Name.</span><span class="sxs-lookup"><span data-stu-id="6c394-1262">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="6c394-1263">Теперь он возвращает только соответствующий узел.</span><span class="sxs-lookup"><span data-stu-id="6c394-1263">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6c394-1264">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6c394-1264">Az.Compute</span></span>
* <span data-ttu-id="6c394-1265">Добавлены параметры ProtectFromScaleIn и ProtectFromScaleSetAction для командлета Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="6c394-1265">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="6c394-1266">Командлет New-AzVM с простым набором параметров теперь по умолчанию использует доступное расположение, если регион "восточная часть США" не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6c394-1266">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6c394-1267">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6c394-1267">Az.DataLakeStore</span></span>
* <span data-ttu-id="6c394-1268">Обновлен пакет SDK ADLS для использования httpclient. В инфраструктуру Azure интегрирована проверка плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="6c394-1268">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6c394-1269">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6c394-1269">Az.Monitor</span></span>
* <span data-ttu-id="6c394-1270">Исправлены неправильные имена параметров в справочных примерах.</span><span class="sxs-lookup"><span data-stu-id="6c394-1270">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6c394-1271">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6c394-1271">Az.Network</span></span>
* <span data-ttu-id="6c394-1272">Добавлен флаг DisableBgpRoutePropagation для выходных данных действующей таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="6c394-1272">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="6c394-1273">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="6c394-1273">Updated cmdlet:</span></span>
        - <span data-ttu-id="6c394-1274">Get-AzEffectiveRouteTable.</span><span class="sxs-lookup"><span data-stu-id="6c394-1274">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="6c394-1275">Исправлен двойной дефис в документации New-AzApplicationGatewayTrustedRootCertificate.</span><span class="sxs-lookup"><span data-stu-id="6c394-1275">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="6c394-1276">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6c394-1276">Az.Resources</span></span>
* <span data-ttu-id="6c394-1277">Добавлен новый командлет Get-AzureRmDenyAssignment для получения запрещающих назначений.</span><span class="sxs-lookup"><span data-stu-id="6c394-1277">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="6c394-1278">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6c394-1278">Az.Sql</span></span>
* <span data-ttu-id="6c394-1279">Командлеты Расширенной защиты от угроз переименованы на командлеты Расширенной защиты данных, и оценка уязвимости включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6c394-1279">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="6c394-1280">2.0.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6c394-1280">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6c394-1281">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6c394-1281">Az.Accounts</span></span>
* <span data-ttu-id="6c394-1282">Обновлена библиотека аутентификации для устранения проблем с ADFS при использовании аутентификации на основе имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="6c394-1282">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6c394-1283">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6c394-1283">Az.CognitiveServices</span></span>
* <span data-ttu-id="6c394-1284">Отображается только заявление об отказе Bing для служб Поиска Bing.</span><span class="sxs-lookup"><span data-stu-id="6c394-1284">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="6c394-1285">Исправлена проблема с созданием учетной записи.</span><span class="sxs-lookup"><span data-stu-id="6c394-1285">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6c394-1286">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6c394-1286">Az.Compute</span></span>
* <span data-ttu-id="6c394-1287">Функция группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="6c394-1287">Proximity placement group feature.</span></span>
    - <span data-ttu-id="6c394-1288">Добавлены следующие новые командлеты:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="6c394-1288">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="6c394-1289">Новый параметр ProximityPlacementGroupId будет добавлен в следующие командлеты:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="6c394-1289">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="6c394-1290">В командлет New-AzGalleryImageVersion добавлен параметр StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="6c394-1290">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="6c394-1291">TargetRegion в командлете New-AzGalleryImageVersion может содержать StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="6c394-1291">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="6c394-1292">Параметр-переключатель SkipShutdown добавлен в командлеты Stop-AzVM и Stop-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="6c394-1292">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="6c394-1293">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="6c394-1293">Breaking changes</span></span>
    - <span data-ttu-id="6c394-1294">Командлет SET-AzVMBootDiagnostics изменен на Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="6c394-1294">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="6c394-1295">Командлет Export-AzLogAnalyticThrottledRequests изменен на Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="6c394-1295">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="6c394-1296">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="6c394-1296">Az.DeploymentManager</span></span>
* <span data-ttu-id="6c394-1297">Первая общедоступная версия командлетов диспетчера развертывания Azure</span><span class="sxs-lookup"><span data-stu-id="6c394-1297">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="6c394-1298">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="6c394-1298">Az.Dns</span></span>
* <span data-ttu-id="6c394-1299">Автоматическое делегирование DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="6c394-1299">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="6c394-1300">Командлет для создания зоны DNS принимает имя родительской зоны в качестве дополнительного необязательного параметра.</span><span class="sxs-lookup"><span data-stu-id="6c394-1300">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="6c394-1301">Он добавляет записи NS в родительской зоне для созданной дочерней зоны.</span><span class="sxs-lookup"><span data-stu-id="6c394-1301">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6c394-1302">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6c394-1302">Az.FrontDoor</span></span>
* <span data-ttu-id="6c394-1303">Первая общедоступная версия командлетов Azure FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="6c394-1303">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="6c394-1304">Переименованы командлеты WAF для включения Waf.</span><span class="sxs-lookup"><span data-stu-id="6c394-1304">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="6c394-1305">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6c394-1305">Az.HDInsight</span></span>
* <span data-ttu-id="6c394-1306">Удалены два командлета:</span><span class="sxs-lookup"><span data-stu-id="6c394-1306">Removed two cmdlets:</span></span>
    - <span data-ttu-id="6c394-1307">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6c394-1307">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="6c394-1308">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6c394-1308">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="6c394-1309">Добавлен новый командлет Set-AzHDInsightGatewayCredential для замены Grant-AzHDInsightHttpServicesAccess.</span><span class="sxs-lookup"><span data-stu-id="6c394-1309">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="6c394-1310">Обновлен командлет Get-AzHDInsightJobOutput для различения ролей читателя и оператора HDInsight:</span><span class="sxs-lookup"><span data-stu-id="6c394-1310">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="6c394-1311">Пользователям с ролью читателя не нужно указывать параметр DefaultStorageAccountKey явным образом, иначе возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="6c394-1311">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="6c394-1312">На пользователей с ролью оператора HDInsight это не повлияет.</span><span class="sxs-lookup"><span data-stu-id="6c394-1312">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6c394-1313">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6c394-1313">Az.Monitor</span></span>
* <span data-ttu-id="6c394-1314">Новые командлеты для API SQR (запланированное правило запросов)</span><span class="sxs-lookup"><span data-stu-id="6c394-1314">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="6c394-1315">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="6c394-1315">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="6c394-1316">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="6c394-1316">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="6c394-1317">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="6c394-1317">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="6c394-1318">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="6c394-1318">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="6c394-1319">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="6c394-1319">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="6c394-1320">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="6c394-1320">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="6c394-1321">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6c394-1321">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6c394-1322">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6c394-1322">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6c394-1323">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6c394-1323">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6c394-1324">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6c394-1324">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6c394-1325">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6c394-1325">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6c394-1326">См. подробнее об [API SQR](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules).</span><span class="sxs-lookup"><span data-stu-id="6c394-1326">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="6c394-1327">Обновлен файл Az.Monitor.md для включения командлетов для правила генерации оповещений на основе метрик GenV2(не классическая версия).</span><span class="sxs-lookup"><span data-stu-id="6c394-1327">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6c394-1328">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6c394-1328">Az.Network</span></span>
* <span data-ttu-id="6c394-1329">Добавлена поддержка для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="6c394-1329">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="6c394-1330">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="6c394-1330">New cmdlets</span></span>
        - <span data-ttu-id="6c394-1331">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6c394-1331">New-AzNatGateway</span></span>
        - <span data-ttu-id="6c394-1332">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6c394-1332">Get-AzNatGateway</span></span>
        - <span data-ttu-id="6c394-1333">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6c394-1333">Set-AzNatGateway</span></span>
        - <span data-ttu-id="6c394-1334">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6c394-1334">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="6c394-1335">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="6c394-1335">Updated cmdlets</span></span>
        - <span data-ttu-id="6c394-1336">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="6c394-1336">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="6c394-1337">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="6c394-1337">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="6c394-1338">Обновлены следующие команды для функции: Настройка и удаление пользовательских маршрутов через шлюз в Бруклине.</span><span class="sxs-lookup"><span data-stu-id="6c394-1338">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="6c394-1339">Обновлен командлет New-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="6c394-1339">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="6c394-1340">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="6c394-1340">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6c394-1341">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6c394-1341">Az.PolicyInsights</span></span>
* <span data-ttu-id="6c394-1342">Добавлена поддержка сведений об оценке политики запросов.</span><span class="sxs-lookup"><span data-stu-id="6c394-1342">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="6c394-1343">Добавлен параметр -Expand в командлет Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="6c394-1343">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="6c394-1344">Добавлена поддержка -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="6c394-1344">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6c394-1345">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6c394-1345">Az.RecoveryServices</span></span>
* <span data-ttu-id="6c394-1346">Добавлена поддержка перекрестной подписки на Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="6c394-1346">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="6c394-1347">Добавлена возможность отмечать предстоящие критически важные изменения для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="6c394-1347">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="6c394-1348">Исправлены план восстановления и план действий для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="6c394-1348">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="6c394-1349">Исправлено сетевое сопоставление обновления Azure Site Recovery (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="6c394-1349">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="6c394-1350">Исправлено направление защиты обновления Azure Site Recovery для управляемых дисков (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="6c394-1350">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="6c394-1351">Добавлены другие незначительные исправления.</span><span class="sxs-lookup"><span data-stu-id="6c394-1351">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="6c394-1352">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="6c394-1352">Az.Relay</span></span>
* <span data-ttu-id="6c394-1353">Исправлены опечатки в сообщениях для клиентов.</span><span class="sxs-lookup"><span data-stu-id="6c394-1353">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6c394-1354">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6c394-1354">Az.ServiceBus</span></span>
* <span data-ttu-id="6c394-1355">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="6c394-1355">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6c394-1356">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6c394-1356">Az.Storage</span></span>
* <span data-ttu-id="6c394-1357">Выполнено обновление клиентской библиотеки хранилища до версии 10.0.1 (пространство имен всех объектов из этого пакета SDK изменено с Microsoft.WindowsAzure.Storage. *на Microsoft.Azure.Storage*).</span><span class="sxs-lookup"><span data-stu-id="6c394-1357">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="6c394-1358">Выполнено обновление до Microsoft.Azure.Management.Storage версии 11.0.0 для включения поддержки нового API версии 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="6c394-1358">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="6c394-1359">Значение свойства Kind по умолчанию в учетной записи хранения изменено со Storage на StorageV2.</span><span class="sxs-lookup"><span data-stu-id="6c394-1359">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="6c394-1360">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6c394-1360">New-AzStorageAccount</span></span>
* <span data-ttu-id="6c394-1361">Изменено значение Sku.Name в выходных данных командлета учетной записи хранения в соответствии со значением Sku.Name во входных данных путем добавления _ (например, StandardLRS изменено на Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="6c394-1361">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="6c394-1362">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6c394-1362">New-AzStorageAccount</span></span>
    - <span data-ttu-id="6c394-1363">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6c394-1363">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="6c394-1364">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6c394-1364">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6c394-1365">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6c394-1365">Az.Websites</span></span>
* <span data-ttu-id="6c394-1366">Свойство Kind теперь будет задаваться объектам PSSite, возвращаемым командлетом Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="6c394-1366">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="6c394-1367">Get-AzWebApp\*Metrics и Get-AzAppServicePlanMetrics считаются нерекомендуемыми.</span><span class="sxs-lookup"><span data-stu-id="6c394-1367">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="6c394-1368">1.8.0 — апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6c394-1368">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6c394-1369">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="6c394-1369">Highlights since the last major release</span></span>
* <span data-ttu-id="6c394-1370">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="6c394-1370">General availability of `Az` module</span></span>
* <span data-ttu-id="6c394-1371">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="6c394-1371">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="6c394-1372">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="6c394-1372">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="6c394-1373">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="6c394-1373">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="6c394-1374">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="6c394-1374">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6c394-1375">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="6c394-1375">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="6c394-1376">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="6c394-1376">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6c394-1377">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6c394-1377">Az.Accounts</span></span>
* <span data-ttu-id="6c394-1378">Обновлен командлет Uninstall-AzureRm для правильного удаления модулей в Mac.</span><span class="sxs-lookup"><span data-stu-id="6c394-1378">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6c394-1379">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6c394-1379">Az.Batch</span></span>
* <span data-ttu-id="6c394-1380">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="6c394-1380">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6c394-1381">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6c394-1381">Az.Cdn</span></span>
* <span data-ttu-id="6c394-1382">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="6c394-1382">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6c394-1383">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6c394-1383">Az.CognitiveServices</span></span>
* <span data-ttu-id="6c394-1384">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="6c394-1384">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6c394-1385">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6c394-1385">Az.Compute</span></span>
* <span data-ttu-id="6c394-1386">Устранена проблема с установкой AEM, если в идентификаторах ресурсов дисков группа ресурсов указана в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="6c394-1386">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="6c394-1387">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="6c394-1387">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6c394-1388">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="6c394-1388">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6c394-1389">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6c394-1389">Az.DataFactory</span></span>
* <span data-ttu-id="6c394-1390">Добавлены свойства SsisProperties, если NodeCount не имеет значения NULL для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="6c394-1390">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6c394-1391">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6c394-1391">Az.DataLakeStore</span></span>
* <span data-ttu-id="6c394-1392">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="6c394-1392">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6c394-1393">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6c394-1393">Az.EventGrid</span></span>
* <span data-ttu-id="6c394-1394">Обновлен текст справки для конечной точки, указывающий, что необходимо создать ресурсы, прежде чем использовать командлеты для создания или обновления подписки на события.</span><span class="sxs-lookup"><span data-stu-id="6c394-1394">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6c394-1395">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6c394-1395">Az.EventHub</span></span>
* <span data-ttu-id="6c394-1396">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="6c394-1396">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="6c394-1397">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6c394-1397">Az.HDInsight</span></span>
* <span data-ttu-id="6c394-1398">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="6c394-1398">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6c394-1399">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6c394-1399">Az.IotHub</span></span>
* <span data-ttu-id="6c394-1400">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="6c394-1400">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6c394-1401">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6c394-1401">Az.KeyVault</span></span>
* <span data-ttu-id="6c394-1402">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="6c394-1402">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6c394-1403">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="6c394-1403">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="6c394-1404">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="6c394-1404">Az.MachineLearning</span></span>
* <span data-ttu-id="6c394-1405">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="6c394-1405">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="6c394-1406">Az.Media</span><span class="sxs-lookup"><span data-stu-id="6c394-1406">Az.Media</span></span>
* <span data-ttu-id="6c394-1407">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="6c394-1407">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6c394-1408">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6c394-1408">Az.Monitor</span></span>
  * <span data-ttu-id="6c394-1409">Добавлены новые командлеты для правила генерации оповещений на основе метрик GenV2 (не классических).</span><span class="sxs-lookup"><span data-stu-id="6c394-1409">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="6c394-1410">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="6c394-1410">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="6c394-1411">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="6c394-1411">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="6c394-1412">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="6c394-1412">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="6c394-1413">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="6c394-1413">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="6c394-1414">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="6c394-1414">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="6c394-1415">Обновлен пакет SDK Monitor до предварительной версии 0.22.0.</span><span class="sxs-lookup"><span data-stu-id="6c394-1415">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6c394-1416">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6c394-1416">Az.Network</span></span>
* <span data-ttu-id="6c394-1417">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="6c394-1417">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6c394-1418">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="6c394-1418">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="6c394-1419">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="6c394-1419">Az.NotificationHubs</span></span>
* <span data-ttu-id="6c394-1420">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="6c394-1420">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6c394-1421">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6c394-1421">Az.OperationalInsights</span></span>
* <span data-ttu-id="6c394-1422">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="6c394-1422">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="6c394-1423">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="6c394-1423">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="6c394-1424">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="6c394-1424">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6c394-1425">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6c394-1425">Az.RecoveryServices</span></span>
* <span data-ttu-id="6c394-1426">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="6c394-1426">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6c394-1427">Обновлен табличный формат для SQL на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="6c394-1427">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="6c394-1428">Добавлен альтернативный метод для получения расположения в Общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="6c394-1428">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="6c394-1429">Обновлено значение ScheduleRunDays в объекте SchedulePolicy в соответствии с часовым поясом.</span><span class="sxs-lookup"><span data-stu-id="6c394-1429">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6c394-1430">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6c394-1430">Az.RedisCache</span></span>
* <span data-ttu-id="6c394-1431">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="6c394-1431">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6c394-1432">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6c394-1432">Az.Resources</span></span>
* <span data-ttu-id="6c394-1433">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="6c394-1433">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="6c394-1434">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6c394-1434">Az.Sql</span></span>
* <span data-ttu-id="6c394-1435">Заменена зависимость от пакета SDK монитора на обычный код.</span><span class="sxs-lookup"><span data-stu-id="6c394-1435">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="6c394-1436">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="6c394-1436">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6c394-1437">Улучшен процесс классификации нескольких столбцов.</span><span class="sxs-lookup"><span data-stu-id="6c394-1437">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="6c394-1438">Добавлены свойства SKU (имя, семейство, производительность SKU) в отклике Get-AzSqlServerServiceObjective, а также по умолчанию задан табличный формат.</span><span class="sxs-lookup"><span data-stu-id="6c394-1438">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="6c394-1439">C помощью Get-AzSqlServerServiceObjective теперь можно получать список доступных целевых служб по расположению без необходимости заранее размещать сервер в регионе.</span><span class="sxs-lookup"><span data-stu-id="6c394-1439">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="6c394-1440">Поддерживается параметр часового пояса при создании Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="6c394-1440">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="6c394-1441">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="6c394-1441">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6c394-1442">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6c394-1442">Az.Websites</span></span>
* <span data-ttu-id="6c394-1443">Исправлены командлеты Set-AzWebApp и Set-AzWebAppSlot, которые теперь не удаляют теги при выполнении.</span><span class="sxs-lookup"><span data-stu-id="6c394-1443">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="6c394-1444">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="6c394-1444">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6c394-1445">Обновлен пакет SDK веб-узлов.</span><span class="sxs-lookup"><span data-stu-id="6c394-1445">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="6c394-1446">Удалено свойство AdminSiteName из PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="6c394-1446">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="6c394-1447">1.7.0 —апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6c394-1447">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6c394-1448">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="6c394-1448">Highlights since the last major release</span></span>
* <span data-ttu-id="6c394-1449">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="6c394-1449">General availability of `Az` module</span></span>
* <span data-ttu-id="6c394-1450">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="6c394-1450">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="6c394-1451">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="6c394-1451">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="6c394-1452">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="6c394-1452">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="6c394-1453">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="6c394-1453">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6c394-1454">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="6c394-1454">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="6c394-1455">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="6c394-1455">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6c394-1456">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6c394-1456">Az.Accounts</span></span>
* <span data-ttu-id="6c394-1457">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметр AzureAnalysisServicesEndpointResourceId.</span><span class="sxs-lookup"><span data-stu-id="6c394-1457">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6c394-1458">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6c394-1458">Az.AnalysisServices</span></span>
* <span data-ttu-id="6c394-1459">Использование ServiceClient в командлетах плоскости данных и удаление исходной логики проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="6c394-1459">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="6c394-1460">Add-AzureASAccount используется как оболочка для Connect-AzAccount во избежание критических изменений.</span><span class="sxs-lookup"><span data-stu-id="6c394-1460">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6c394-1461">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6c394-1461">Az.Automation</span></span>
* <span data-ttu-id="6c394-1462">Исправлена ошибка командлета New-AzAutomationSoftwareUpdateConfiguration, связанная с включением.</span><span class="sxs-lookup"><span data-stu-id="6c394-1462">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="6c394-1463">Теперь параметры IncludedKbNumber и IncludedPackageNameMask должны работать нормально.</span><span class="sxs-lookup"><span data-stu-id="6c394-1463">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="6c394-1464">Исправлена ошибка динамической группы управления обновлениями службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="6c394-1464">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6c394-1465">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6c394-1465">Az.Compute</span></span>
* <span data-ttu-id="6c394-1466">В командлеты New-AzDiskConfig и New-AzSnapshotConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="6c394-1466">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="6c394-1467">Теперь можно создавать виртуальные машину на основе образов из коллекции от других клиентов.</span><span class="sxs-lookup"><span data-stu-id="6c394-1467">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="6c394-1468">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6c394-1468">Az.ContainerInstance</span></span>
* <span data-ttu-id="6c394-1469">Исправлена проблема в параметре -Command командлета New-AzContainerGroup, из-за которой в конце добавлялся пустой аргумент.</span><span class="sxs-lookup"><span data-stu-id="6c394-1469">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6c394-1470">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6c394-1470">Az.DataFactory</span></span>
* <span data-ttu-id="6c394-1471">Пакет SDK для ADF .NET обновлен до версии 3.0.2.</span><span class="sxs-lookup"><span data-stu-id="6c394-1471">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="6c394-1472">Командлет Set-AzDataFactoryV2 обновлен с помощью дополнительных параметров для настроек, связанных с RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="6c394-1472">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6c394-1473">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6c394-1473">Az.Resources</span></span>
* <span data-ttu-id="6c394-1474">Улучшена обработка поставщиков Get-AzResource при предоставлении параметров -ResourceId или -ResourceGroupName, -Name и -ResourceType.</span><span class="sxs-lookup"><span data-stu-id="6c394-1474">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="6c394-1475">Улучшена обработка ошибок в командлетах Test-AzDeployment и Test-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="6c394-1475">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="6c394-1476">Теперь ошибки, возникающие за пределами проверки развертывания, обрабатываются и включаются в выходные данные команды.</span><span class="sxs-lookup"><span data-stu-id="6c394-1476">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="6c394-1477">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="6c394-1477">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="6c394-1478">Добавлен параметр-переключатель -IgnoreDynamicParameters, с помощью которого можно настроить командлеты развертывания так, чтобы они пропускали запросы в сценариях скриптов и заданий.</span><span class="sxs-lookup"><span data-stu-id="6c394-1478">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="6c394-1479">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="6c394-1479">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="6c394-1480">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6c394-1480">Az.Sql</span></span>
* <span data-ttu-id="6c394-1481">Поддержка классификации данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="6c394-1481">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6c394-1482">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6c394-1482">Az.Storage</span></span>
* <span data-ttu-id="6c394-1483">Подробные сообщения об ошибке передаются при создании контекста хранилища с помощью параметра -UseConnectedAccount, но без входа в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="6c394-1483">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="6c394-1484">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="6c394-1484">New-AzStorageContext</span></span>
* <span data-ttu-id="6c394-1485">Поддержка свойств службы управления BLOB-объектов в указанной учетной записи хранения с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="6c394-1485">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="6c394-1486">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="6c394-1486">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="6c394-1487">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="6c394-1487">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="6c394-1488">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6c394-1488">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="6c394-1489">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6c394-1489">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="6c394-1490">Поддержка параметра -AsJob в командлетах для отправки и скачивания больших двоичных объектов и файлов.</span><span class="sxs-lookup"><span data-stu-id="6c394-1490">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="6c394-1491">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6c394-1491">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="6c394-1492">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6c394-1492">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="6c394-1493">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6c394-1493">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="6c394-1494">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6c394-1494">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="6c394-1495">1.6.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6c394-1495">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6c394-1496">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="6c394-1496">Highlights since the last major release</span></span>
* <span data-ttu-id="6c394-1497">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="6c394-1497">General availability of `Az` module</span></span>
* <span data-ttu-id="6c394-1498">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="6c394-1498">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="6c394-1499">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="6c394-1499">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="6c394-1500">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="6c394-1500">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="6c394-1501">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="6c394-1501">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6c394-1502">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="6c394-1502">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="6c394-1503">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="6c394-1503">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6c394-1504">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6c394-1504">Az.Automation</span></span>
* <span data-ttu-id="6c394-1505">В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:</span><span class="sxs-lookup"><span data-stu-id="6c394-1505">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="6c394-1506">динамическое группирование;</span><span class="sxs-lookup"><span data-stu-id="6c394-1506">Dynamic grouping</span></span>
    * <span data-ttu-id="6c394-1507">скрипты предварительного или последующего выполнения;</span><span class="sxs-lookup"><span data-stu-id="6c394-1507">Pre-Post script</span></span>
    * <span data-ttu-id="6c394-1508">параметр перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="6c394-1508">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6c394-1509">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6c394-1509">Az.Compute</span></span>
* <span data-ttu-id="6c394-1510">Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.</span><span class="sxs-lookup"><span data-stu-id="6c394-1510">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="6c394-1511">Обновление клиентской библиотеки вычислений до версии 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="6c394-1511">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6c394-1512">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6c394-1512">Az.KeyVault</span></span>
* <span data-ttu-id="6c394-1513">Добавлена поддержка подстановочных знаков в командлетах KeyVault.</span><span class="sxs-lookup"><span data-stu-id="6c394-1513">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6c394-1514">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6c394-1514">Az.Network</span></span>
* <span data-ttu-id="6c394-1515">Добавлена поддержка анализа угроз для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="6c394-1515">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="6c394-1516">Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="6c394-1516">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6c394-1517">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6c394-1517">Az.RecoveryServices</span></span>
* <span data-ttu-id="6c394-1518">В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.</span><span class="sxs-lookup"><span data-stu-id="6c394-1518">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="6c394-1519">Добавлена поддержка канала для отмены регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="6c394-1519">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="6c394-1520">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6c394-1520">Az.Resources</span></span>
* <span data-ttu-id="6c394-1521">Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6c394-1521">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="6c394-1522">Обновлены учетные данные, используемые при общих вызовах к ARM.</span><span class="sxs-lookup"><span data-stu-id="6c394-1522">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="6c394-1523">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6c394-1523">Az.Sql</span></span>
* <span data-ttu-id="6c394-1524">Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="6c394-1524">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6c394-1525">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6c394-1525">Az.Storage</span></span>
* <span data-ttu-id="6c394-1526">Поддержка получения, настройки и удаления политики управления в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="6c394-1526">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="6c394-1527">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6c394-1527">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="6c394-1528">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6c394-1528">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="6c394-1529">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6c394-1529">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="6c394-1530">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="6c394-1530">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="6c394-1531">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="6c394-1531">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="6c394-1532">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="6c394-1532">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6c394-1533">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6c394-1533">Az.Websites</span></span>
* <span data-ttu-id="6c394-1534">Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="6c394-1534">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="6c394-1535">1.5.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6c394-1535">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6c394-1536">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6c394-1536">Az.Accounts</span></span>
* <span data-ttu-id="6c394-1537">Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.</span><span class="sxs-lookup"><span data-stu-id="6c394-1537">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="6c394-1538">Обновлены примеры для Connect AzAccount.</span><span class="sxs-lookup"><span data-stu-id="6c394-1538">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6c394-1539">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6c394-1539">Az.Automation</span></span>
* <span data-ttu-id="6c394-1540">Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="6c394-1540">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="6c394-1541">Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов.</span><span class="sxs-lookup"><span data-stu-id="6c394-1541">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="6c394-1542">Теперь он возвращает все узлы.</span><span class="sxs-lookup"><span data-stu-id="6c394-1542">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6c394-1543">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6c394-1543">Az.Cdn</span></span>
* <span data-ttu-id="6c394-1544">Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.</span><span class="sxs-lookup"><span data-stu-id="6c394-1544">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6c394-1545">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6c394-1545">Az.Compute</span></span>
* <span data-ttu-id="6c394-1546">Добавлена поддержка подстановочных знаков в командлетах Get.</span><span class="sxs-lookup"><span data-stu-id="6c394-1546">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6c394-1547">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6c394-1547">Az.DataFactory</span></span>
* <span data-ttu-id="6c394-1548">Обновлен пакет SDK для ADF .NET до версии 3.0.1.</span><span class="sxs-lookup"><span data-stu-id="6c394-1548">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6c394-1549">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6c394-1549">Az.LogicApp</span></span>
* <span data-ttu-id="6c394-1550">Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.</span><span class="sxs-lookup"><span data-stu-id="6c394-1550">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6c394-1551">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6c394-1551">Az.Network</span></span>
* <span data-ttu-id="6c394-1552">Добавлена поддержка подстановочных знаков в командлетах Network.</span><span class="sxs-lookup"><span data-stu-id="6c394-1552">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6c394-1553">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6c394-1553">Az.RecoveryServices</span></span>
* <span data-ttu-id="6c394-1554">Добавлена поддержка SQL Server на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="6c394-1554">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="6c394-1555">Обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="6c394-1555">SDK Update</span></span>
* <span data-ttu-id="6c394-1556">Удалена проверка VMappContainer в Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="6c394-1556">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="6c394-1557">Добавлены параметры Name и ServerName для Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="6c394-1557">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="6c394-1558">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6c394-1558">Az.Resources</span></span>
* <span data-ttu-id="6c394-1559">Добавлен параметр `-TemplateObject` в командлеты для развертывания.</span><span class="sxs-lookup"><span data-stu-id="6c394-1559">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="6c394-1560">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.</span><span class="sxs-lookup"><span data-stu-id="6c394-1560">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="6c394-1561">Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="6c394-1561">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="6c394-1562">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.</span><span class="sxs-lookup"><span data-stu-id="6c394-1562">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="6c394-1563">Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="6c394-1563">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="6c394-1564">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.</span><span class="sxs-lookup"><span data-stu-id="6c394-1564">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="6c394-1565">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6c394-1565">Az.Sql</span></span>
* <span data-ttu-id="6c394-1566">Обновление AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="6c394-1566">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="6c394-1567">Исправлено поведение для пограничного случая при создании параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="6c394-1567">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6c394-1568">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6c394-1568">Az.Storage</span></span>
* <span data-ttu-id="6c394-1569">Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="6c394-1569">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="6c394-1570">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6c394-1570">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="6c394-1571">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6c394-1571">Az.AnalysisServices</span></span>
* <span data-ttu-id="6c394-1572">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="6c394-1572">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6c394-1573">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6c394-1573">Az.Automation</span></span>
* <span data-ttu-id="6c394-1574">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="6c394-1574">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="6c394-1575">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="6c394-1575">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="6c394-1576">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="6c394-1576">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6c394-1577">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6c394-1577">Az.CognitiveServices</span></span>
* <span data-ttu-id="6c394-1578">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="6c394-1578">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6c394-1579">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6c394-1579">Az.Compute</span></span>
* <span data-ttu-id="6c394-1580">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="6c394-1580">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="6c394-1581">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="6c394-1581">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="6c394-1582">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="6c394-1582">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="6c394-1583">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="6c394-1583">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6c394-1584">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6c394-1584">Az.DataLakeStore</span></span>
* <span data-ttu-id="6c394-1585">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="6c394-1585">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6c394-1586">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6c394-1586">Az.EventHub</span></span>
* <span data-ttu-id="6c394-1587">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="6c394-1587">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="6c394-1588">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6c394-1588">Az.KeyVault</span></span>
* <span data-ttu-id="6c394-1589">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="6c394-1589">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6c394-1590">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6c394-1590">Az.LogicApp</span></span>
* <span data-ttu-id="6c394-1591">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="6c394-1591">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="6c394-1592">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="6c394-1592">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="6c394-1593">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="6c394-1593">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="6c394-1594">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="6c394-1594">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="6c394-1595">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="6c394-1595">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="6c394-1596">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="6c394-1596">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="6c394-1597">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="6c394-1597">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="6c394-1598">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="6c394-1598">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="6c394-1599">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="6c394-1599">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="6c394-1600">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="6c394-1600">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="6c394-1601">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="6c394-1601">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="6c394-1602">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="6c394-1602">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="6c394-1603">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="6c394-1603">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6c394-1604">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6c394-1604">Az.Monitor</span></span>
* <span data-ttu-id="6c394-1605">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="6c394-1605">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6c394-1606">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6c394-1606">Az.Network</span></span>
* <span data-ttu-id="6c394-1607">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="6c394-1607">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6c394-1608">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6c394-1608">Az.OperationalInsights</span></span>
* <span data-ttu-id="6c394-1609">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="6c394-1609">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="6c394-1610">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="6c394-1610">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="6c394-1611">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="6c394-1611">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="6c394-1612">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6c394-1612">Az.Resources</span></span>
* <span data-ttu-id="6c394-1613">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="6c394-1613">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="6c394-1614">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="6c394-1614">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="6c394-1615">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="6c394-1615">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="6c394-1616">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="6c394-1616">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="6c394-1617">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6c394-1617">Az.Sql</span></span>
* <span data-ttu-id="6c394-1618">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="6c394-1618">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="6c394-1619">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="6c394-1619">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6c394-1620">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6c394-1620">Az.Websites</span></span>
* <span data-ttu-id="6c394-1621">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="6c394-1621">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="6c394-1622">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6c394-1622">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6c394-1623">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6c394-1623">Az.Accounts</span></span>
* <span data-ttu-id="6c394-1624">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="6c394-1624">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6c394-1625">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6c394-1625">Az.AnalysisServices</span></span>
<span data-ttu-id="6c394-1626">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="6c394-1626">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6c394-1627">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6c394-1627">Az.Compute</span></span>
* <span data-ttu-id="6c394-1628">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="6c394-1628">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="6c394-1629">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="6c394-1629">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="6c394-1630">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="6c394-1630">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6c394-1631">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6c394-1631">Az.RecoveryServices</span></span>
<span data-ttu-id="6c394-1632">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="6c394-1632">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6c394-1633">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6c394-1633">Az.Resources</span></span>
* <span data-ttu-id="6c394-1634">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6c394-1634">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="6c394-1635">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="6c394-1635">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="6c394-1636">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="6c394-1636">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="6c394-1637">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="6c394-1637">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="6c394-1638">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6c394-1638">Az.Sql</span></span>
* <span data-ttu-id="6c394-1639">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="6c394-1639">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="6c394-1640">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="6c394-1640">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="6c394-1641">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="6c394-1641">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="6c394-1642">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6c394-1642">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6c394-1643">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6c394-1643">Az.Accounts</span></span>
* <span data-ttu-id="6c394-1644">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="6c394-1644">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6c394-1645">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6c394-1645">Az.AnalysisServices</span></span>
* <span data-ttu-id="6c394-1646">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="6c394-1646">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6c394-1647">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6c394-1647">Az.RecoveryServices</span></span>
* <span data-ttu-id="6c394-1648">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="6c394-1648">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="6c394-1649">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6c394-1649">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6c394-1650">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6c394-1650">Az.Accounts</span></span>
* <span data-ttu-id="6c394-1651">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="6c394-1651">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6c394-1652">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="6c394-1652">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6c394-1653">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="6c394-1653">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="6c394-1654">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="6c394-1654">Az.Aks</span></span>
* <span data-ttu-id="6c394-1655">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="6c394-1655">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6c394-1656">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6c394-1656">Az.Automation</span></span>
* <span data-ttu-id="6c394-1657">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="6c394-1657">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="6c394-1658">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="6c394-1658">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6c394-1659">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6c394-1659">Az.Cdn</span></span>
* <span data-ttu-id="6c394-1660">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="6c394-1660">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6c394-1661">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6c394-1661">Az.Compute</span></span>
* <span data-ttu-id="6c394-1662">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="6c394-1662">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="6c394-1663">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="6c394-1663">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="6c394-1664">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="6c394-1664">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="6c394-1665">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6c394-1665">Az.ContainerRegistry</span></span>
* <span data-ttu-id="6c394-1666">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="6c394-1666">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6c394-1667">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6c394-1667">Az.DataFactory</span></span>
* <span data-ttu-id="6c394-1668">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="6c394-1668">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6c394-1669">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6c394-1669">Az.DataLakeStore</span></span>
* <span data-ttu-id="6c394-1670">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="6c394-1670">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="6c394-1671">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="6c394-1671">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="6c394-1672">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="6c394-1672">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6c394-1673">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6c394-1673">Az.IotHub</span></span>
* <span data-ttu-id="6c394-1674">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="6c394-1674">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6c394-1675">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6c394-1675">Az.KeyVault</span></span>
* <span data-ttu-id="6c394-1676">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="6c394-1676">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6c394-1677">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6c394-1677">Az.Network</span></span>
* <span data-ttu-id="6c394-1678">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="6c394-1678">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="6c394-1679">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6c394-1679">Az.Resources</span></span>
* <span data-ttu-id="6c394-1680">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="6c394-1680">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="6c394-1681">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6c394-1681">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="6c394-1682">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="6c394-1682">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="6c394-1683">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="6c394-1683">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="6c394-1684">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="6c394-1684">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="6c394-1685">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="6c394-1685">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="6c394-1686">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="6c394-1686">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6c394-1687">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6c394-1687">Az.ServiceFabric</span></span>
* <span data-ttu-id="6c394-1688">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="6c394-1688">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="6c394-1689">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="6c394-1689">Fix some error messages.</span></span>
* <span data-ttu-id="6c394-1690">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="6c394-1690">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="6c394-1691">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="6c394-1691">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="6c394-1692">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="6c394-1692">Az.SignalR</span></span>
* <span data-ttu-id="6c394-1693">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="6c394-1693">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="6c394-1694">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6c394-1694">Az.Sql</span></span>
* <span data-ttu-id="6c394-1695">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="6c394-1695">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6c394-1696">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="6c394-1696">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="6c394-1697">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="6c394-1697">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="6c394-1698">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="6c394-1698">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6c394-1699">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6c394-1699">Az.Storage</span></span>
* <span data-ttu-id="6c394-1700">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="6c394-1700">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6c394-1701">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="6c394-1701">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="6c394-1702">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="6c394-1702">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="6c394-1703">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="6c394-1703">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="6c394-1704">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6c394-1704">Az.TrafficManager</span></span>
* <span data-ttu-id="6c394-1705">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="6c394-1705">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6c394-1706">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6c394-1706">Az.Websites</span></span>
* <span data-ttu-id="6c394-1707">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="6c394-1707">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6c394-1708">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="6c394-1708">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="6c394-1709">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="6c394-1709">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="6c394-1710">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6c394-1710">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6c394-1711">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6c394-1711">Az.Accounts</span></span>
* <span data-ttu-id="6c394-1712">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="6c394-1712">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6c394-1713">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6c394-1713">Az.Compute</span></span>
* <span data-ttu-id="6c394-1714">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="6c394-1714">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="6c394-1715">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="6c394-1715">Updated the description of ID in help files</span></span>
* <span data-ttu-id="6c394-1716">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="6c394-1716">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6c394-1717">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6c394-1717">Az.DataLakeStore</span></span>
* <span data-ttu-id="6c394-1718">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="6c394-1718">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="6c394-1719">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="6c394-1719">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6c394-1720">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6c394-1720">Az.EventGrid</span></span>
* <span data-ttu-id="6c394-1721">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="6c394-1721">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="6c394-1722">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="6c394-1722">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="6c394-1723">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="6c394-1723">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="6c394-1724">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="6c394-1724">Event Time-To-Live,</span></span>
        - <span data-ttu-id="6c394-1725">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="6c394-1725">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="6c394-1726">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="6c394-1726">Dead letter endpoint.</span></span>
    - <span data-ttu-id="6c394-1727">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="6c394-1727">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="6c394-1728">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="6c394-1728">Event Time-To-Live,</span></span>
        - <span data-ttu-id="6c394-1729">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="6c394-1729">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="6c394-1730">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="6c394-1730">Dead letter endpoint.</span></span>
* <span data-ttu-id="6c394-1731">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="6c394-1731">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="6c394-1732">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="6c394-1732">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6c394-1733">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6c394-1733">Az.IotHub</span></span>
* <span data-ttu-id="6c394-1734">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="6c394-1734">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6c394-1735">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6c394-1735">Az.LogicApp</span></span>
* <span data-ttu-id="6c394-1736">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="6c394-1736">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="6c394-1737">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6c394-1737">Az.Resources</span></span>
* <span data-ttu-id="6c394-1738">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="6c394-1738">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="6c394-1739">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="6c394-1739">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="6c394-1740">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="6c394-1740">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="6c394-1741">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="6c394-1741">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="6c394-1742">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="6c394-1742">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="6c394-1743">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="6c394-1743">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="6c394-1744">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="6c394-1744">Az.SignalR</span></span>
* <span data-ttu-id="6c394-1745">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="6c394-1745">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="6c394-1746">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6c394-1746">Az.Sql</span></span>
* <span data-ttu-id="6c394-1747">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="6c394-1747">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6c394-1748">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6c394-1748">Az.Storage</span></span>
* <span data-ttu-id="6c394-1749">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="6c394-1749">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="6c394-1750">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="6c394-1750">New-AzStorageContext</span></span>
* <span data-ttu-id="6c394-1751">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="6c394-1751">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="6c394-1752">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="6c394-1752">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6c394-1753">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6c394-1753">Az.Websites</span></span>
* <span data-ttu-id="6c394-1754">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="6c394-1754">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="6c394-1755">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="6c394-1755">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="6c394-1756">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="6c394-1756">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="6c394-1757">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="6c394-1757">General</span></span>

- <span data-ttu-id="6c394-1758">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="6c394-1758">General Availability of Az Module</span></span>
- <span data-ttu-id="6c394-1759">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="6c394-1759">Online help for each module</span></span>
- <span data-ttu-id="6c394-1760">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="6c394-1760">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="6c394-1761">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6c394-1761">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="6c394-1762">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6c394-1762">Az.Accounts</span></span>
- <span data-ttu-id="6c394-1763">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="6c394-1763">Changed from Az.Profile</span></span>
- <span data-ttu-id="6c394-1764">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="6c394-1764">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="6c394-1765">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6c394-1765">Az.ApiManagement</span></span>
- <span data-ttu-id="6c394-1766">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="6c394-1766">Fixes for #7002</span></span>
- <span data-ttu-id="6c394-1767">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6c394-1767">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="6c394-1768">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6c394-1768">Az.Batch</span></span>
- <span data-ttu-id="6c394-1769">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="6c394-1769">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="6c394-1770">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="6c394-1770">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="6c394-1771">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6c394-1771">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="6c394-1772">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="6c394-1772">Az.Billing</span></span>
- <span data-ttu-id="6c394-1773">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="6c394-1773">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="6c394-1774">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="6c394-1774">Az.CognitivServices</span></span>
- <span data-ttu-id="6c394-1775">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="6c394-1775">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="6c394-1776">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="6c394-1776">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="6c394-1777">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6c394-1777">Az.ContainerInstance</span></span>
- <span data-ttu-id="6c394-1778">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="6c394-1778">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="6c394-1779">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="6c394-1779">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="6c394-1780">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6c394-1780">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="6c394-1781">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6c394-1781">Az.DataLakeStore</span></span>
- <span data-ttu-id="6c394-1782">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6c394-1782">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="6c394-1783">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6c394-1783">Az.Monitor</span></span>
- <span data-ttu-id="6c394-1784">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6c394-1784">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="6c394-1785">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6c394-1785">Az.KeyVault</span></span>
- <span data-ttu-id="6c394-1786">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="6c394-1786">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="6c394-1787">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="6c394-1787">Az.MachineLearning</span></span>
- <span data-ttu-id="6c394-1788">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="6c394-1788">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="6c394-1789">Az.Media</span><span class="sxs-lookup"><span data-stu-id="6c394-1789">Az.Media</span></span>
- <span data-ttu-id="6c394-1790">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="6c394-1790">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="6c394-1791">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6c394-1791">Az.Network</span></span>
<span data-ttu-id="6c394-1792">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="6c394-1792">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="6c394-1793">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="6c394-1793">New cmdlets added:</span></span>
        - <span data-ttu-id="6c394-1794">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6c394-1794">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6c394-1795">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6c394-1795">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6c394-1796">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6c394-1796">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6c394-1797">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6c394-1797">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6c394-1798">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6c394-1798">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6c394-1799">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="6c394-1799">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="6c394-1800">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="6c394-1800">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="6c394-1801">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c394-1801">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="6c394-1802">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6c394-1802">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="6c394-1803">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6c394-1803">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="6c394-1804">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6c394-1804">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="6c394-1805">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6c394-1805">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="6c394-1806">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6c394-1806">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="6c394-1807">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6c394-1807">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="6c394-1808">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="6c394-1808">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="6c394-1809">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6c394-1809">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="6c394-1810">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6c394-1810">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="6c394-1811">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6c394-1811">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="6c394-1812">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6c394-1812">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="6c394-1813">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="6c394-1813">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="6c394-1814">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6c394-1814">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="6c394-1815">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6c394-1815">Az.OperationalInsights</span></span>
- <span data-ttu-id="6c394-1816">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6c394-1816">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="6c394-1817">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6c394-1817">Az.Profile</span></span>
- <span data-ttu-id="6c394-1818">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="6c394-1818">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="6c394-1819">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6c394-1819">Az.RecoveryServices</span></span>
- <span data-ttu-id="6c394-1820">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6c394-1820">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="6c394-1821">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6c394-1821">Az.Resources</span></span>
- <span data-ttu-id="6c394-1822">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6c394-1822">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="6c394-1823">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6c394-1823">Az.ServiceFabric</span></span>
- <span data-ttu-id="6c394-1824">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="6c394-1824">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="6c394-1825">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6c394-1825">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="6c394-1826">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="6c394-1826">Az.SIgnalR</span></span>
- <span data-ttu-id="6c394-1827">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="6c394-1827">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="6c394-1828">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6c394-1828">Az.Sql</span></span>
- <span data-ttu-id="6c394-1829">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="6c394-1829">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="6c394-1830">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="6c394-1830">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="6c394-1831">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6c394-1831">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="6c394-1832">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6c394-1832">Az.Storage</span></span>
- <span data-ttu-id="6c394-1833">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6c394-1833">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="6c394-1834">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6c394-1834">Az.Websites</span></span>
- <span data-ttu-id="6c394-1835">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6c394-1835">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="6c394-1836">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="6c394-1836">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="6c394-1837">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="6c394-1837">General</span></span>

* <span data-ttu-id="6c394-1838">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="6c394-1838">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="6c394-1839">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6c394-1839">Az.Compute</span></span>

* <span data-ttu-id="6c394-1840">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="6c394-1840">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="6c394-1841">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6c394-1841">Az.DataLakeStore</span></span>

* <span data-ttu-id="6c394-1842">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="6c394-1842">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="6c394-1843">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6c394-1843">Az.FrontDoor</span></span>

* <span data-ttu-id="6c394-1844">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="6c394-1844">Fixed some broken links</span></span>
    - <span data-ttu-id="6c394-1845">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="6c394-1845">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="6c394-1846">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="6c394-1846">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="6c394-1847">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6c394-1847">Az.RecoveryServices</span></span>

* <span data-ttu-id="6c394-1848">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="6c394-1848">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="6c394-1849">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="6c394-1849">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="6c394-1850">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6c394-1850">Az.Resources</span></span>

* <span data-ttu-id="6c394-1851">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="6c394-1851">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="6c394-1852">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="6c394-1852">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="6c394-1853">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6c394-1853">Az.Sql</span></span>

* <span data-ttu-id="6c394-1854">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="6c394-1854">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="6c394-1855">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="6c394-1855">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="6c394-1856">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="6c394-1856">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="6c394-1857">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6c394-1857">Az.Storage</span></span>

* <span data-ttu-id="6c394-1858">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6c394-1858">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="6c394-1859">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="6c394-1859">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="6c394-1860">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="6c394-1860">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="6c394-1861">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="6c394-1861">Support Static Website configuration</span></span>
    - <span data-ttu-id="6c394-1862">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="6c394-1862">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="6c394-1863">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="6c394-1863">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="6c394-1864">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6c394-1864">Az.Websites</span></span>

* <span data-ttu-id="6c394-1865">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6c394-1865">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="6c394-1866">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="6c394-1866">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="6c394-1867">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="6c394-1867">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="6c394-1868">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="6c394-1868">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="6c394-1869">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6c394-1869">Az.ApiManagement</span></span>
* <span data-ttu-id="6c394-1870">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="6c394-1870">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="6c394-1871">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6c394-1871">Az.Automation</span></span>
* <span data-ttu-id="6c394-1872">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="6c394-1872">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="6c394-1873">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="6c394-1873">Added Update Management cmdlets</span></span>
* <span data-ttu-id="6c394-1874">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="6c394-1874">Added Source Control cmdlets</span></span>
* <span data-ttu-id="6c394-1875">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="6c394-1875">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="6c394-1876">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="6c394-1876">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="6c394-1877">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6c394-1877">Az.Compute</span></span>
* <span data-ttu-id="6c394-1878">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="6c394-1878">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="6c394-1879">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="6c394-1879">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="6c394-1880">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6c394-1880">Az.ContainerInstance</span></span>
* <span data-ttu-id="6c394-1881">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="6c394-1881">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="6c394-1882">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="6c394-1882">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="6c394-1883">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="6c394-1883">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="6c394-1884">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6c394-1884">Az.Network</span></span>
* <span data-ttu-id="6c394-1885">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="6c394-1885">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="6c394-1886">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="6c394-1886">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="6c394-1887">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="6c394-1887">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="6c394-1888">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="6c394-1888">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="6c394-1889">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="6c394-1889">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="6c394-1890">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="6c394-1890">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="6c394-1891">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="6c394-1891">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="6c394-1892">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="6c394-1892">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="6c394-1893">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="6c394-1893">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="6c394-1894">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="6c394-1894">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="6c394-1895">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="6c394-1895">Az.Relay</span></span>
* <span data-ttu-id="6c394-1896">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="6c394-1896">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="6c394-1897">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6c394-1897">Az.Resources</span></span>
* <span data-ttu-id="6c394-1898">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="6c394-1898">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="6c394-1899">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="6c394-1899">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="6c394-1900">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="6c394-1900">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="6c394-1901">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6c394-1901">Az.ServiceFabric</span></span>
* <span data-ttu-id="6c394-1902">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="6c394-1902">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="6c394-1903">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6c394-1903">Az.Sql</span></span>
* <span data-ttu-id="6c394-1904">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="6c394-1904">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="6c394-1905">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="6c394-1905">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6c394-1906">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="6c394-1906">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6c394-1907">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="6c394-1907">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6c394-1908">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="6c394-1908">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6c394-1909">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="6c394-1909">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6c394-1910">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="6c394-1910">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6c394-1911">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="6c394-1911">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6c394-1912">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="6c394-1912">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="6c394-1913">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="6c394-1913">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="6c394-1914">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="6c394-1914">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="6c394-1915">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="6c394-1915">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="6c394-1916">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="6c394-1916">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="6c394-1917">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="6c394-1917">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="6c394-1918">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="6c394-1918">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="6c394-1919">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="6c394-1919">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="6c394-1920">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="6c394-1920">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="6c394-1921">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="6c394-1921">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="6c394-1922">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="6c394-1922">General</span></span>
* <span data-ttu-id="6c394-1923">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="6c394-1923">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="6c394-1924">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6c394-1924">Az.Profile</span></span>
* <span data-ttu-id="6c394-1925">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c394-1925">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="6c394-1926">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="6c394-1926">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="6c394-1927">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="6c394-1927">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="6c394-1928">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="6c394-1928">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="6c394-1929">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="6c394-1929">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="6c394-1930">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="6c394-1930">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="6c394-1931">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="6c394-1931">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="6c394-1932">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6c394-1932">Az.CognitiveServices</span></span>
* <span data-ttu-id="6c394-1933">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="6c394-1933">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6c394-1934">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6c394-1934">Az.Compute</span></span>
* <span data-ttu-id="6c394-1935">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="6c394-1935">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="6c394-1936">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="6c394-1936">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="6c394-1937">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="6c394-1937">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6c394-1938">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6c394-1938">Az.DataLakeStore</span></span>
* <span data-ttu-id="6c394-1939">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="6c394-1939">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="6c394-1940">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="6c394-1940">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="6c394-1941">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="6c394-1941">Az.Insights</span></span>
* <span data-ttu-id="6c394-1942">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="6c394-1942">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="6c394-1943">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="6c394-1943">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="6c394-1944">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="6c394-1944">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="6c394-1945">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="6c394-1945">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6c394-1946">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6c394-1946">Az.Network</span></span>
* <span data-ttu-id="6c394-1947">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="6c394-1947">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="6c394-1948">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="6c394-1948">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="6c394-1949">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="6c394-1949">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="6c394-1950">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="6c394-1950">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="6c394-1951">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="6c394-1951">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="6c394-1952">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="6c394-1952">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="6c394-1953">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="6c394-1953">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6c394-1954">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6c394-1954">Az.PolicyInsights</span></span>
* <span data-ttu-id="6c394-1955">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="6c394-1955">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="6c394-1956">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6c394-1956">Az.Resources</span></span>
* <span data-ttu-id="6c394-1957">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="6c394-1957">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="6c394-1958">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="6c394-1958">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6c394-1959">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6c394-1959">Az.ServiceBus</span></span>
* <span data-ttu-id="6c394-1960">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="6c394-1960">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6c394-1961">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6c394-1961">Az.ServiceFabric</span></span>
* <span data-ttu-id="6c394-1962">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="6c394-1962">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="6c394-1963">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="6c394-1963">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="6c394-1964">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="6c394-1964">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="6c394-1965">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="6c394-1965">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="6c394-1966">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="6c394-1966">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="6c394-1967">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="6c394-1967">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="6c394-1968">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6c394-1968">Az.Profile</span></span>
* <span data-ttu-id="6c394-1969">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="6c394-1969">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="6c394-1970">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c394-1970">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6c394-1971">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6c394-1971">Az.Compute</span></span>
* <span data-ttu-id="6c394-1972">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="6c394-1972">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="6c394-1973">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="6c394-1973">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6c394-1974">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6c394-1974">Az.DataLakeStore</span></span>
* <span data-ttu-id="6c394-1975">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="6c394-1975">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="6c394-1976">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6c394-1976">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="6c394-1977">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6c394-1977">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="6c394-1978">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6c394-1978">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="6c394-1979">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6c394-1979">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6c394-1980">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6c394-1980">Az.Network</span></span>
* <span data-ttu-id="6c394-1981">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="6c394-1981">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="6c394-1982">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="6c394-1982">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6c394-1983">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6c394-1983">Az.Resources</span></span>
* <span data-ttu-id="6c394-1984">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="6c394-1984">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="6c394-1985">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="6c394-1985">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="6c394-1986">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="6c394-1986">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="6c394-1987">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="6c394-1987">Azure.Storage</span></span>
* <span data-ttu-id="6c394-1988">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="6c394-1988">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="6c394-1989">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6c394-1989">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="6c394-1990">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="6c394-1990">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="6c394-1991">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="6c394-1991">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="6c394-1992">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="6c394-1992">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="6c394-1993">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6c394-1993">Az.CognitiveServices</span></span>
* <span data-ttu-id="6c394-1994">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="6c394-1994">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6c394-1995">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6c394-1995">Az.Compute</span></span>
* <span data-ttu-id="6c394-1996">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="6c394-1996">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="6c394-1997">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="6c394-1997">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="6c394-1998">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="6c394-1998">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="6c394-1999">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6c394-1999">Az.DataFactoryV2</span></span>
* <span data-ttu-id="6c394-2000">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="6c394-2000">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6c394-2001">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6c394-2001">Az.Network</span></span>
* <span data-ttu-id="6c394-2002">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="6c394-2002">Added NetworkProfile functionality.</span></span> <span data-ttu-id="6c394-2003">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="6c394-2003">new cmdlets added</span></span>
    - <span data-ttu-id="6c394-2004">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6c394-2004">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="6c394-2005">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6c394-2005">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="6c394-2006">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6c394-2006">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="6c394-2007">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6c394-2007">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="6c394-2008">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="6c394-2008">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="6c394-2009">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="6c394-2009">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="6c394-2010">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="6c394-2010">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="6c394-2011">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="6c394-2011">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="6c394-2012">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="6c394-2012">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6c394-2013">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6c394-2013">Az.RedisCache</span></span>
* <span data-ttu-id="6c394-2014">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="6c394-2014">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="6c394-2015">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="6c394-2015">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="6c394-2016">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6c394-2016">Az.Resources</span></span>
* <span data-ttu-id="6c394-2017">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6c394-2017">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="6c394-2018">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="6c394-2018">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="6c394-2019">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6c394-2019">Az.Sql</span></span>
* <span data-ttu-id="6c394-2020">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="6c394-2020">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6c394-2021">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6c394-2021">Az.Websites</span></span>
* <span data-ttu-id="6c394-2022">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="6c394-2022">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="6c394-2023">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="6c394-2023">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="6c394-2024">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="6c394-2024">0.2.0 - September 2018</span></span>
 <span data-ttu-id="6c394-2025">Начальный выпуск</span><span class="sxs-lookup"><span data-stu-id="6c394-2025">Initial Release</span></span>
