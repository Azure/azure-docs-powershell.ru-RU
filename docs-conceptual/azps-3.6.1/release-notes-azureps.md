---
title: Заметки о выпуске Azure PowerShell
description: Узнайте обо всех последних обновлениях модулей Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/09/2020
ms.openlocfilehash: 4c7ea19a225d63307ecf4a6fe5ebfa14ccd78d7e
ms.sourcegitcommit: f6fa6543be1e0f6330b1598f01528b2928cc426c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2020
ms.locfileid: "79036167"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="7af37-103">Заметки о выпуске Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="7af37-103">Azure PowerShell release notes</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="7af37-104">3.6.1 — март 2020 г.</span><span class="sxs-lookup"><span data-stu-id="7af37-104">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7af37-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7af37-105">Az.Accounts</span></span>
* <span data-ttu-id="7af37-106">Открытие страницы опроса Azure PowerShell в Send-Feedback [11020].</span><span class="sxs-lookup"><span data-stu-id="7af37-106">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="7af37-107">Отображение URL-адреса опроса Azure PowerShell в Resolve-Error [11021].</span><span class="sxs-lookup"><span data-stu-id="7af37-107">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="7af37-108">Добавлена версия Az в UserAgent.</span><span class="sxs-lookup"><span data-stu-id="7af37-108">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7af37-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7af37-109">Az.ApiManagement</span></span>
* <span data-ttu-id="7af37-110">Включена поддержка получения и настройки личного домена в конечной точке DeveloperPortal [11007].</span><span class="sxs-lookup"><span data-stu-id="7af37-110">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="7af37-111">Export-AzApiManagementApi: включена поддержка скачивания определения API в формате JSON [9987].</span><span class="sxs-lookup"><span data-stu-id="7af37-111">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="7af37-112">Import-AzApiManagementApi: включена поддержка импорта определения OpenApi 3.0 из документа JSON.</span><span class="sxs-lookup"><span data-stu-id="7af37-112">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="7af37-113">New-AzApiManagementIdentityProvider и Set-AzApiManagementIdentityProvider: включена поддержка настройки входа арендатора для поставщика AAD B2C [9784].</span><span class="sxs-lookup"><span data-stu-id="7af37-113">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7af37-114">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7af37-114">Az.DataLakeStore</span></span>
* <span data-ttu-id="7af37-115">Добавлена ссылка на System.Buffers явным образом в CSPROJ и PSD1.</span><span class="sxs-lookup"><span data-stu-id="7af37-115">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7af37-116">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7af37-116">Az.IotHub</span></span>
* <span data-ttu-id="7af37-117">Добавлена возможность управления устройствами в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="7af37-117">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="7af37-118">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="7af37-118">New Cmdlets are:</span></span>
    - <span data-ttu-id="7af37-119">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="7af37-119">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="7af37-120">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="7af37-120">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="7af37-121">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="7af37-121">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="7af37-122">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="7af37-122">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="7af37-123">Включена поддержка управления модулями в целевом устройстве Интернета вещей в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="7af37-123">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="7af37-124">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="7af37-124">New Cmdlets are:</span></span>
    - <span data-ttu-id="7af37-125">Add-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="7af37-125">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="7af37-126">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="7af37-126">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="7af37-127">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="7af37-127">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="7af37-128">Set-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="7af37-128">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="7af37-129">Добавлен командлет для получения строки подключения целевого устройства Интернета вещей в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="7af37-129">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="7af37-130">Добавлен командлет для получения строки подключения модуля на целевом устройстве Интернета вещей в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="7af37-130">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="7af37-131">Включена поддержка для получения или настройки родительского устройства для устройства Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="7af37-131">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="7af37-132">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="7af37-132">New Cmdlets are:</span></span>
    - <span data-ttu-id="7af37-133">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="7af37-133">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="7af37-134">Set-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="7af37-134">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="7af37-135">Включена поддержка управления связью "родители — потомки" устройства.</span><span class="sxs-lookup"><span data-stu-id="7af37-135">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7af37-136">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7af37-136">Az.Monitor</span></span>
* <span data-ttu-id="7af37-137">Исправлено выходное значение для Get-AzMetricDefinition [9714].</span><span class="sxs-lookup"><span data-stu-id="7af37-137">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7af37-138">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7af37-138">Az.Network</span></span>
* <span data-ttu-id="7af37-139">Обновлен пакет SDK для управления SQL.</span><span class="sxs-lookup"><span data-stu-id="7af37-139">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="7af37-140">Исправлена проблема с разницей в именовании в классе PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="7af37-140">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="7af37-141">Сопоставление ActionsRequired с ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="7af37-141">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="7af37-142">Добавление PublicNetworkAccess в команды New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="7af37-142">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="7af37-143">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7af37-143">Az.Resources</span></span>
* <span data-ttu-id="7af37-144">Исправлена ошибка пустой ссылки в Get-AzRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="7af37-144">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="7af37-145">Параметры -Force и -PassThru помечены необязательными в Remove-AzADGroup [10849].</span><span class="sxs-lookup"><span data-stu-id="7af37-145">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="7af37-146">Исправлена ошибка, из-за которой MailNickname не возвращается в Remove-AzADGroup [11167].</span><span class="sxs-lookup"><span data-stu-id="7af37-146">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="7af37-147">Исправлена ошибка, из-за которой операция канала Remove-AzADGroup не работает [11171].</span><span class="sxs-lookup"><span data-stu-id="7af37-147">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="7af37-148">Исправлена ошибка с пустой ссылкой в GetAzureRoleAssignmentCommand.</span><span class="sxs-lookup"><span data-stu-id="7af37-148">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="7af37-149">Добавлено критическое изменение атрибутов для будущих изменений командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="7af37-149">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="7af37-150">Обновлена команда Get-AzResourceGroup для выполнения фильтрации тегов группы ресурсов на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="7af37-150">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="7af37-151">Расширены командлеты Tag для включения поддержки параметра -ResourceId.</span><span class="sxs-lookup"><span data-stu-id="7af37-151">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="7af37-152">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="7af37-152">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="7af37-153">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="7af37-153">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="7af37-154">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="7af37-154">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="7af37-155">Добавлен новый командлет Tag.</span><span class="sxs-lookup"><span data-stu-id="7af37-155">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="7af37-156">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="7af37-156">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="7af37-157">Предоставляется ScopedDeployment из пакета SDK 3.3.0.</span><span class="sxs-lookup"><span data-stu-id="7af37-157">Brought ScopedDeployment from SDK 3.3.0</span></span> 

#### <a name="azsql"></a><span data-ttu-id="7af37-158">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7af37-158">Az.Sql</span></span>
* <span data-ttu-id="7af37-159">Добавление PublicNetworkAccess в команды New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="7af37-159">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="7af37-160">Включена поддержка конфигурации резервного копирования долгосрочного хранения для управляемых баз данных.</span><span class="sxs-lookup"><span data-stu-id="7af37-160">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="7af37-161">Получение или настройка политики LTR в управляемой базе данных.</span><span class="sxs-lookup"><span data-stu-id="7af37-161">Get/Set LTR policy on a managed database</span></span> 
    - <span data-ttu-id="7af37-162">Получение резервных копий LTR по управляемой базе данных, управляемому экземпляру или расположению.</span><span class="sxs-lookup"><span data-stu-id="7af37-162">Get LTR backup(s) by managed database, managed instance, or by location</span></span> 
    - <span data-ttu-id="7af37-163">Удаление резервной копии LTR.</span><span class="sxs-lookup"><span data-stu-id="7af37-163">Remove an LTR backup</span></span> 
    - <span data-ttu-id="7af37-164">Восстановление резервной копии LTR для создания новой управляемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="7af37-164">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="7af37-165">Добавление MinimalTlsVersion в New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="7af37-165">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="7af37-166">Добавление MinimalTlsVersion в New-AzSqlInstance и Set-AzSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="7af37-166">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="7af37-167">Обновлена версия пакета SDK для SQL для Az.Network.</span><span class="sxs-lookup"><span data-stu-id="7af37-167">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7af37-168">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7af37-168">Az.Storage</span></span>
* <span data-ttu-id="7af37-169">Включена поддержка AllowProtectedAppendWrite в ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="7af37-169">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="7af37-170">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="7af37-170">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="7af37-171">Добавлено предупреждение о критическом изменении для изменения типа AzureStorageTable в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="7af37-171">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="7af37-172">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="7af37-172">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="7af37-173">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="7af37-173">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7af37-174">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7af37-174">Az.Websites</span></span>
* <span data-ttu-id="7af37-175">Добавлен параметр Tag для New-AzAppServicePlan и Set-AzAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="7af37-175">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="7af37-176">Завершение выполнения командлета, если при добавлении личного домена на веб-сайт возникает исключение.</span><span class="sxs-lookup"><span data-stu-id="7af37-176">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="7af37-177">Включена поддержка выполнения операций для Служб приложений, которые находятся не в той же группе ресурсов, что и план службы приложений.</span><span class="sxs-lookup"><span data-stu-id="7af37-177">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="7af37-178">Применение ограничения доступа к WebApp/Function в разных группах ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7af37-178">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="7af37-179">Исправлена ошибка с указанием пользовательских имен узлов для WebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="7af37-179">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="7af37-180">3.5.0 — февраль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="7af37-180">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7af37-181">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="7af37-181">Highlights since the last major release</span></span>
* <span data-ttu-id="7af37-182">Обновлены данные телеметрии на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="7af37-182">Updated client side telemetry.</span></span>
* <span data-ttu-id="7af37-183">В Az.IotHub добавлены командлеты для управления устройствами.</span><span class="sxs-lookup"><span data-stu-id="7af37-183">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="7af37-184">В Az.SqlVirtualMachine добавлены командлеты для прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="7af37-184">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7af37-185">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7af37-185">Az.Accounts</span></span>
* <span data-ttu-id="7af37-186">В данные телеметрии на стороне клиента добавлены такие сведения, как идентификатор подписки, идентификатор арендатора и время выполнения.</span><span class="sxs-lookup"><span data-stu-id="7af37-186">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7af37-187">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7af37-187">Az.Automation</span></span>
* <span data-ttu-id="7af37-188">Исправлена опечатка в примере 1 в справочной документации по New-AzAutomationSoftwareUpdateConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7af37-188">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7af37-189">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7af37-189">Az.CognitiveServices</span></span>
* <span data-ttu-id="7af37-190">Обновлен пакет SDK до версии 7.0.</span><span class="sxs-lookup"><span data-stu-id="7af37-190">Updated SDK to 7.0</span></span>
* <span data-ttu-id="7af37-191">Улучшено сообщение об ошибке, которое появляется, если ответы сервера не содержат текст.</span><span class="sxs-lookup"><span data-stu-id="7af37-191">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7af37-192">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7af37-192">Az.Compute</span></span>
* <span data-ttu-id="7af37-193">Разрешено использовать пустое значение для ProximityPlacementGroupId во время обновления.</span><span class="sxs-lookup"><span data-stu-id="7af37-193">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7af37-194">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7af37-194">Az.FrontDoor</span></span>
* <span data-ttu-id="7af37-195">Добавлен командлет для получения определений управляемых правил, которые могут использоваться в WAF.</span><span class="sxs-lookup"><span data-stu-id="7af37-195">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7af37-196">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7af37-196">Az.IotHub</span></span>
* <span data-ttu-id="7af37-197">Добавлена возможность управления устройствами в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="7af37-197">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="7af37-198">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="7af37-198">New Cmdlets are:</span></span>
    - <span data-ttu-id="7af37-199">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="7af37-199">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="7af37-200">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="7af37-200">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="7af37-201">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="7af37-201">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="7af37-202">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="7af37-202">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7af37-203">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7af37-203">Az.KeyVault</span></span>
* <span data-ttu-id="7af37-204">Устранен дублирующийся текст для Add-AzKeyVaultKey.md.</span><span class="sxs-lookup"><span data-stu-id="7af37-204">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7af37-205">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7af37-205">Az.Monitor</span></span>
* <span data-ttu-id="7af37-206">Исправлено описание командлета Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="7af37-206">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="7af37-207">В команду New-AzMetricAlertRuleV2 добавлен новый параметр ActionGroupId.</span><span class="sxs-lookup"><span data-stu-id="7af37-207">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="7af37-208">Пользователь может предоставить ActionGroupId(string) или ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="7af37-208">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7af37-209">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7af37-209">Az.Network</span></span>
* <span data-ttu-id="7af37-210">Добавлен еще один параметр -EnableProxyProtocol для командлета New-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="7af37-210">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="7af37-211">Исправлен пример FilterData в Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="7af37-211">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="7af37-212">Добавлен пример Packet Capture для всех внутренних и внешних пакетов в Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="7af37-212">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="7af37-213">Добавлена поддерживаемая политика Брандмауэра Azure в брандмауэрах виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="7af37-213">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="7af37-214">Новые командлеты не добавлены.</span><span class="sxs-lookup"><span data-stu-id="7af37-214">No new cmdlets are added.</span></span> <span data-ttu-id="7af37-215">Снято ограничение политики брандмауэра в брандмауэрах виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="7af37-215">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7af37-216">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7af37-216">Az.RecoveryServices</span></span>
* <span data-ttu-id="7af37-217">Добавлена возможность восстановления в виде файлов для Баз данных SQL.</span><span class="sxs-lookup"><span data-stu-id="7af37-217">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7af37-218">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7af37-218">Az.Resources</span></span>
* <span data-ttu-id="7af37-219">Выполнен рефакторинг командлетов развертывания шаблона.</span><span class="sxs-lookup"><span data-stu-id="7af37-219">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="7af37-220">Добавлены новые командлеты для управления развертываниями в группе управления: \*-AzManagementGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="7af37-220">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="7af37-221">Добавлены новые командлеты для управления развертываниями в области арендатора: \*-AzTenantDeployment.</span><span class="sxs-lookup"><span data-stu-id="7af37-221">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="7af37-222">Выполнен рефакторинг командлетов \*-AzDeployment для работы в области подписки.</span><span class="sxs-lookup"><span data-stu-id="7af37-222">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="7af37-223">Созданы псевдонимы \*-AzSubscriptionDeployment для командлетов \*-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="7af37-223">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="7af37-224">Исправлен командлет Update-AzADApplication, когда параметр AvailableToOtherTenants не задан.</span><span class="sxs-lookup"><span data-stu-id="7af37-224">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="7af37-225">Удален набор параметров ApplicationObjectWithoutCredentialParameterSet, чтобы предотвратить возникновение AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="7af37-225">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="7af37-226">Повторно созданы файлы справки.</span><span class="sxs-lookup"><span data-stu-id="7af37-226">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="7af37-227">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7af37-227">Az.Sql</span></span>
* <span data-ttu-id="7af37-228">Добавлена возможность восстановления точки во времени между подписками в Управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="7af37-228">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="7af37-229">Добавлена возможность изменения существующего поколения оборудования Управляемого экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="7af37-229">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="7af37-230">Исправлены примеры справки Update-AzSqlServerVulnerabilityAssessmentSetting: выходные данные параметра и свойства — EmailAdmins.</span><span class="sxs-lookup"><span data-stu-id="7af37-230">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="7af37-231">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7af37-231">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="7af37-232">Добавлены командлеты для прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="7af37-232">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="7af37-233">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="7af37-233">Az.StorageSync</span></span>
* <span data-ttu-id="7af37-234">В командлете Invoke-AzStorageSyncCompatibilityCheck обновлены поддерживаемые наборы символов.</span><span class="sxs-lookup"><span data-stu-id="7af37-234">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="7af37-235">3.4.0 — февраль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="7af37-235">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7af37-236">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="7af37-236">Highlights since the last major release</span></span>
* <span data-ttu-id="7af37-237">Выпущена первоначальная версия 0.1.0 Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="7af37-237">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="7af37-238">Добавлена поддержка Az.Network ConnectionMonitor V2</span><span class="sxs-lookup"><span data-stu-id="7af37-238">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7af37-239">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7af37-239">Az.Accounts</span></span>
* <span data-ttu-id="7af37-240">Отключить автоматическое сохранение контекста, если AzureRmContext.json недоступен</span><span class="sxs-lookup"><span data-stu-id="7af37-240">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="7af37-241">Обновление ссылки на Azure Powershell Common до предварительной версии 1.3.5</span><span class="sxs-lookup"><span data-stu-id="7af37-241">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7af37-242">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7af37-242">Az.ApiManagement</span></span>
* <span data-ttu-id="7af37-243">**Get-AzApiManagementApiSchema** Исправлено получение схемы Open-API, связанной с API https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="7af37-243">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="7af37-244">**New-AzApiManagementProduct**\* и **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="7af37-244">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="7af37-245">Исправить документацию для https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="7af37-245">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="7af37-246">**Set-AzApiManagementApi** Добавлен пример, показывающий, как обновить ServiceUrl с помощью командлета</span><span class="sxs-lookup"><span data-stu-id="7af37-246">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7af37-247">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7af37-247">Az.Compute</span></span>
* <span data-ttu-id="7af37-248">Ограничение числа состояний виртуальных машин до 100, чтобы избежать регулирования при выполнении Get-AzVM-Status без имени виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7af37-248">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="7af37-249">Добавление обновления командлета -AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="7af37-249">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="7af37-250">Добавление параметров EncryptionType и DiskEncryptionSetId в следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="7af37-250">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="7af37-251">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="7af37-251">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="7af37-252">Добавление параметра ColocationStatus в командлет Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="7af37-252">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7af37-253">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7af37-253">Az.DataFactory</span></span>
* <span data-ttu-id="7af37-254">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.7.0.</span><span class="sxs-lookup"><span data-stu-id="7af37-254">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="7af37-255">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="7af37-255">Az.DeploymentManager</span></span>
* <span data-ttu-id="7af37-256">Добавляет операции LIST для ресурсов</span><span class="sxs-lookup"><span data-stu-id="7af37-256">Adds LIST operations for resources</span></span>
* <span data-ttu-id="7af37-257">Добавляет возможность выполнения операций на этапах Проверки работоспособности</span><span class="sxs-lookup"><span data-stu-id="7af37-257">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7af37-258">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7af37-258">Az.HDInsight</span></span>
* <span data-ttu-id="7af37-259">Исправление ошибки в документе New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="7af37-259">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7af37-260">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7af37-260">Az.KeyVault</span></span>
* <span data-ttu-id="7af37-261">Добавление Псевдонимов имени в атрибут VaultName, чтобы Remove-AzureKeyVault соответствовал New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="7af37-261">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7af37-262">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7af37-262">Az.Network</span></span>
* <span data-ttu-id="7af37-263">В Set-AzNetworkWatcherConfigFlowLog.md добавлен новый пример для демонстрации сценария отключения Аналитики трафика.</span><span class="sxs-lookup"><span data-stu-id="7af37-263">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="7af37-264">Добавление поддержки назначения IP-конфигурации для брандмауэра Azure — выделенная подсеть и общедоступный IP-адрес, которые брандмауэр будет использовать для управления трафиком</span><span class="sxs-lookup"><span data-stu-id="7af37-264">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="7af37-265">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="7af37-265">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="7af37-266">добавлен параметр — ManagementPublicIpAddress (необязательный), который принимает объект общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="7af37-266">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="7af37-267">Добавлен метод SetManagementIpConfiguration для объекта брандмауэра — в качестве входных данных требуется подсеть и общедоступный IP-адрес — имя подсети должно быть "AzureFirewallManagementSubnet"</span><span class="sxs-lookup"><span data-stu-id="7af37-267">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="7af37-268">Исправлены примеры Get-AzNetworkSecurityGroup для отображения примеров для группы безопасности сети (NSG) вместо сетевых интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="7af37-268">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="7af37-269">Исправлена опечатка в команде New-AzVpnSite, которая препятствовала завершению параметра идентификатором ресурса.</span><span class="sxs-lookup"><span data-stu-id="7af37-269">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="7af37-270">Добавлена поддержка конфигурации в наборе действий для правил подстановки URL-адресов в шлюзе приложения.</span><span class="sxs-lookup"><span data-stu-id="7af37-270">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="7af37-271">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="7af37-271">New cmdlets added:</span></span>
        - <span data-ttu-id="7af37-272">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="7af37-272">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="7af37-273">В следующие командлеты добавлен необязательный параметр — UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="7af37-273">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="7af37-274">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="7af37-274">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="7af37-275">Добавление поддержки для ресурсов NetworkWatcher ConnectionMonitor версии 2</span><span class="sxs-lookup"><span data-stu-id="7af37-275">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7af37-276">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7af37-276">Az.PolicyInsights</span></span>
* <span data-ttu-id="7af37-277">Поддержка оценки соответствия до определения того, какой ресурс нужно исправить</span><span class="sxs-lookup"><span data-stu-id="7af37-277">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="7af37-278">Добавление параметра "—ResourceDiscoverMode" в Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="7af37-278">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="7af37-279">Добавление командлета Get-AzPolicyMetadata для получения ресурсов метаданных политики</span><span class="sxs-lookup"><span data-stu-id="7af37-279">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="7af37-280">Get-AzPolicyState и Get-AzPolicyStateSummary обновлены для API версии 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="7af37-280">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7af37-281">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7af37-281">Az.RecoveryServices</span></span>
* <span data-ttu-id="7af37-282">Поддержка Azure Site Recovery для удаления реплицированного диска.</span><span class="sxs-lookup"><span data-stu-id="7af37-282">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="7af37-283">В Azure Backup добавлена ​​поддержка добавления тегов при создании Хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="7af37-283">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7af37-284">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7af37-284">Az.Resources</span></span>
* <span data-ttu-id="7af37-285">Сделайте команду "Область" необязательной в командлетах \*—AzPolicyAssignment с настройкой по умолчанию для контекстной подписки</span><span class="sxs-lookup"><span data-stu-id="7af37-285">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="7af37-286">Добавление примеров создания ADServicePrincipal с паролем и ключом учетных данных</span><span class="sxs-lookup"><span data-stu-id="7af37-286">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="7af37-287">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7af37-287">Az.Sql</span></span>
<span data-ttu-id="7af37-288">Исправление командлета New-AzSqlDatabaseSecondary, чтобы проверить существование PartnerDatabaseName, а не DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="7af37-288">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7af37-289">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7af37-289">Az.Storage</span></span>
* <span data-ttu-id="7af37-290">Поддержка набора шифрования типа ключа таблиц и очередей в создании учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="7af37-290">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="7af37-291">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7af37-291">New-AzStorageAccount</span></span>
* <span data-ttu-id="7af37-292">Представление RequestId, если StorageException не имеет ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="7af37-292">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="7af37-293">Исправление примера 6 командлета Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="7af37-293">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7af37-294">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7af37-294">Az.Websites</span></span>
* <span data-ttu-id="7af37-295">Set-AzWebapp и Set-AzWebappSlot поддерживают свойства AlwaysOn, MinTls и FtpsState</span><span class="sxs-lookup"><span data-stu-id="7af37-295">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="7af37-296">Устранение проблемы, при которой параметр HttpsOnly с одновременным изменением AppservicePlan с помощью одной команды Set-AzWebApp сбрасывал значение HttpsOnly до значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="7af37-296">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="7af37-297">3.3.0 — январь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="7af37-297">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7af37-298">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7af37-298">Az.Accounts</span></span>
* <span data-ttu-id="7af37-299">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment: теперь они принимают параметры AzureAttestationServiceEndpointResourceId и AzureAttestationServiceEndpointSuffix.</span><span class="sxs-lookup"><span data-stu-id="7af37-299">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7af37-300">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7af37-300">Az.Cdn</span></span>
* <span data-ttu-id="7af37-301">Теперь в командлете New-AzCdnEndpoint отображаются сведения из сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="7af37-301">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7af37-302">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7af37-302">Az.Compute</span></span>
* <span data-ttu-id="7af37-303">Командлет Set-AzVMCustomScriptExtension исправлен для виртуальной машины с управляемым диском ОС без профиля ОС.</span><span class="sxs-lookup"><span data-stu-id="7af37-303">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="7af37-304">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7af37-304">Az.ContainerInstance</span></span>
* <span data-ttu-id="7af37-305">Исправлены имена параметров, используемые в примере командлета New-AzContainerGroup.</span><span class="sxs-lookup"><span data-stu-id="7af37-305">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="7af37-306">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="7af37-306">Az.DataBoxEdge</span></span>
* <span data-ttu-id="7af37-307">Добавлен командлет Get-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="7af37-307">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="7af37-308">получение контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="7af37-308">Get the Edge Storage Container</span></span>
* <span data-ttu-id="7af37-309">Добавлен командлет New-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="7af37-309">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="7af37-310">создание контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="7af37-310">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="7af37-311">Добавлен командлет Remove-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="7af37-311">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="7af37-312">удаление контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="7af37-312">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="7af37-313">Добавлен командлет Invoke-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="7af37-313">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="7af37-314">вызов действия для обновления данных в контейнере хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="7af37-314">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="7af37-315">Добавлен командлет Get-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="7af37-315">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="7af37-316">получение учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="7af37-316">Get the Edge Storage Account</span></span>
* <span data-ttu-id="7af37-317">Добавлен командлет New-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="7af37-317">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="7af37-318">создание учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="7af37-318">Create new Edge Storage Account</span></span>
* <span data-ttu-id="7af37-319">Добавлен командлет Remove-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="7af37-319">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="7af37-320">удаление учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="7af37-320">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="7af37-321">Вызов командлета Invoke-AzDataBoxEdgeShare:</span><span class="sxs-lookup"><span data-stu-id="7af37-321">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="7af37-322">вызов действия для обновления данных в общей папке.</span><span class="sxs-lookup"><span data-stu-id="7af37-322">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="7af37-323">Добавлен командлет Set-AzDataBoxEdgeStorageAccountCredential:</span><span class="sxs-lookup"><span data-stu-id="7af37-323">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="7af37-324">установка учетных данных для учетной записи хранилища Azure Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="7af37-324">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7af37-325">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7af37-325">Az.DataFactory</span></span>
* <span data-ttu-id="7af37-326">Добавлены свойства AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId и VersionStatus для командлета Get-AzDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="7af37-326">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="7af37-327">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.6.0.</span><span class="sxs-lookup"><span data-stu-id="7af37-327">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="7af37-328">Для командлета Set-AzureRmDataFactoryV2IntegrationRuntime добавлен параметр PublicIPs, позволяющий включить создание среды Azure-SSIS IR со статическими общедоступными IP-адресами.</span><span class="sxs-lookup"><span data-stu-id="7af37-328">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="7af37-329">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="7af37-329">Az.DevTestLabs</span></span>
* <span data-ttu-id="7af37-330">Удалена недействительная ссылка в файле Get-AzDtlAllowedVMSizesPolicy.md.</span><span class="sxs-lookup"><span data-stu-id="7af37-330">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7af37-331">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7af37-331">Az.EventHub</span></span>
* <span data-ttu-id="7af37-332">Устранена проблема № 10634: исправлена ссылка на пустой объект для удаления пространства имен концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="7af37-332">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7af37-333">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7af37-333">Az.HDInsight</span></span>
* <span data-ttu-id="7af37-334">Устранена ошибка в файле Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="7af37-334">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="7af37-335">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="7af37-335">Az.MachineLearning</span></span>
* <span data-ttu-id="7af37-336">Вычислительная среда Машинного обучения больше недоступна, поэтому удалены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="7af37-336">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="7af37-337">Get-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="7af37-337">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="7af37-338">Get-AzMlOpClusterKey;</span><span class="sxs-lookup"><span data-stu-id="7af37-338">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="7af37-339">New-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="7af37-339">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="7af37-340">Remove-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="7af37-340">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="7af37-341">Set-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="7af37-341">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="7af37-342">Test-AzMlOpClusterSystemServicesUpdateAvailability;</span><span class="sxs-lookup"><span data-stu-id="7af37-342">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="7af37-343">Update-AzMlOpClusterSystemService.</span><span class="sxs-lookup"><span data-stu-id="7af37-343">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7af37-344">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7af37-344">Az.Network</span></span>
* <span data-ttu-id="7af37-345">Обновлена зависимость Microsoft.Azure.Management.Sql от предварительной версии 1.36 до предварительной версии 1.37.</span><span class="sxs-lookup"><span data-stu-id="7af37-345">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7af37-346">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7af37-346">Az.RecoveryServices</span></span>
* <span data-ttu-id="7af37-347">Добавлена поддержка Azure Site Recovery для виртуальных машин с управляемым диском, зашифрованных при хранении с помощью управляемых клиентом ключей, при восстановлении из Azure в поставщике Azure.</span><span class="sxs-lookup"><span data-stu-id="7af37-347">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="7af37-348">Добавлена поддержка Azure Site Recovery для необязательного ввода идентификатора набора шифрования диска при включении защиты в рамках восстановления из VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="7af37-348">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="7af37-349">Добавлена поддержка Azure Site Recovery для необязательного ввода идентификатора набора шифрования диска на уровне диска при включении защиты в рамках восстановления из VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="7af37-349">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="7af37-350">Добавлена поддержка Azure Site Recovery для обновления элемента, защищенного репликацией, путем сопоставления набора шифрования диска при восстановлении из HyperV в Azure.</span><span class="sxs-lookup"><span data-stu-id="7af37-350">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7af37-351">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7af37-351">Az.Resources</span></span>
* <span data-ttu-id="7af37-352">Исправлена ошибка в справочном документе о командлете Remove-AzTag.</span><span class="sxs-lookup"><span data-stu-id="7af37-352">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="7af37-353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7af37-353">Az.Sql</span></span>
* <span data-ttu-id="7af37-354">Исправлена функция основных командлетов установки оценки уязвимостей: теперь она позволяет работать с базой данных master для базы данных Azure и ограничить ее в системных базах данных управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7af37-354">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="7af37-355">Устранена ошибка, возникающая при создании группы отработки отказа экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="7af37-355">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="7af37-356">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7af37-356">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="7af37-357">Добавлен новый допустимый тип лицензии: DR (аварийное восстановление).</span><span class="sxs-lookup"><span data-stu-id="7af37-357">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7af37-358">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7af37-358">Az.Storage</span></span>
* <span data-ttu-id="7af37-359">Добавлено предупреждающее сообщение о критическом изменении значения DefaultAction в следующем выпуске:</span><span class="sxs-lookup"><span data-stu-id="7af37-359">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="7af37-360">Update-AzStorageAccountNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="7af37-360">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="7af37-361">Включена поддержка получения времени последней синхронизации учетной записи хранения путем выполнения командлета Get-AzureRmStorageAccount с параметром -IncludeGeoReplicationStats:</span><span class="sxs-lookup"><span data-stu-id="7af37-361">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span> 
    - <span data-ttu-id="7af37-362">Get-AzureRmStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="7af37-362">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="7af37-363">3.2.0 — декабрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7af37-363">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="7af37-364">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="7af37-364">General</span></span>
* <span data-ttu-id="7af37-365">Обновление ссылок в .psd1 для использования относительного пути для всех модулей.</span><span class="sxs-lookup"><span data-stu-id="7af37-365">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7af37-366">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7af37-366">Az.Accounts</span></span>
* <span data-ttu-id="7af37-367">Установка правильного параметра UserAgent для телеметрии на стороне клиента для Az 4.0 (предварительная версия).</span><span class="sxs-lookup"><span data-stu-id="7af37-367">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="7af37-368">Отображение понятного пользователю сообщения об ошибке, если в Az 4.0 (предварительная версия) не указан контекст.</span><span class="sxs-lookup"><span data-stu-id="7af37-368">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7af37-369">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7af37-369">Az.Batch</span></span>
* <span data-ttu-id="7af37-370">Исправлена проблема [№ 10602](https://github.com/Azure/azure-powershell/issues/10602), из-за которой использование командлета **New-AzBatchPool** приводило к неправильной отправке VirtualMachineConfiguration.ContainerConfiguration или VirtualMachineConfiguration.DataDisks на сервер.</span><span class="sxs-lookup"><span data-stu-id="7af37-370">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7af37-371">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7af37-371">Az.DataFactory</span></span>
* <span data-ttu-id="7af37-372">Обновление пакета SDK Фабрики данных для .NET до версии 4.5.0.</span><span class="sxs-lookup"><span data-stu-id="7af37-372">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7af37-373">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7af37-373">Az.FrontDoor</span></span>
* <span data-ttu-id="7af37-374">Включена поддержка исключений управляемых правил WAF.</span><span class="sxs-lookup"><span data-stu-id="7af37-374">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="7af37-375">Добавление SocketAddr в список автозавершения.</span><span class="sxs-lookup"><span data-stu-id="7af37-375">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="7af37-376">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="7af37-376">Az.HealthcareApis</span></span>
* <span data-ttu-id="7af37-377">Обработка исключений.</span><span class="sxs-lookup"><span data-stu-id="7af37-377">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7af37-378">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7af37-378">Az.KeyVault</span></span>
* <span data-ttu-id="7af37-379">Исправлена ошибка при получении доступа к значению, которое может быть не задано.</span><span class="sxs-lookup"><span data-stu-id="7af37-379">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="7af37-380">Управление сертификатами шифрования на основе эллиптических кривых.</span><span class="sxs-lookup"><span data-stu-id="7af37-380">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="7af37-381">Включена возможность указания кривой для политик сертификатов.</span><span class="sxs-lookup"><span data-stu-id="7af37-381">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7af37-382">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7af37-382">Az.Monitor</span></span>
* <span data-ttu-id="7af37-383">Добавление необязательного аргумента в команду добавления параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="7af37-383">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="7af37-384">Существующий аргумент switch указывает на то, что экспорт в Log Analytics должен выполняться в фиксированную схему</span><span class="sxs-lookup"><span data-stu-id="7af37-384">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="7af37-385">(выделенный тип данных).</span><span class="sxs-lookup"><span data-stu-id="7af37-385">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7af37-386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7af37-386">Az.Network</span></span>
* <span data-ttu-id="7af37-387">В приложении AzureFirewall, NAT и сетевых правилах включена поддержка IpGroups.</span><span class="sxs-lookup"><span data-stu-id="7af37-387">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7af37-388">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7af37-388">Az.Resources</span></span>
* <span data-ttu-id="7af37-389">Устранена проблема, из-за которой при развертывании шаблона не удавалось считать его параметр, если имя параметра конфликтовало с именем встроенного параметра.</span><span class="sxs-lookup"><span data-stu-id="7af37-389">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="7af37-390">Обновлены командлеты политики для использования новой версии API 2019-09-01 с поддержкой группирования в определениях наборов политик.</span><span class="sxs-lookup"><span data-stu-id="7af37-390">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="7af37-391">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7af37-391">Az.Sql</span></span>
* <span data-ttu-id="7af37-392">Обновлена функция автоматического создания расширенного хранилища для службы оценки уязвимостей в учетной записи StorageV2.</span><span class="sxs-lookup"><span data-stu-id="7af37-392">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7af37-393">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7af37-393">Az.Storage</span></span>
* <span data-ttu-id="7af37-394">Включена поддержка создания маркера SAS на основе удостоверения контейнера и большого двоичного объекта с аутентификацией Oauth на основе контекста службы хранилища:</span><span class="sxs-lookup"><span data-stu-id="7af37-394">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="7af37-395">New-AzStorageContainerSASToken;</span><span class="sxs-lookup"><span data-stu-id="7af37-395">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="7af37-396">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="7af37-396">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="7af37-397">Отозвана поддержка ключей делегирования пользователя учетной записи хранения, а также всех маркеров SAS удостоверения:</span><span class="sxs-lookup"><span data-stu-id="7af37-397">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="7af37-398">Revoke-AzStorageAccountUserDelegationKeys.</span><span class="sxs-lookup"><span data-stu-id="7af37-398">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="7af37-399">Выполнено обновление до Microsoft.Azure.Management.Storage версии 14.2.0 для включения поддержки нового API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="7af37-399">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="7af37-400">Включена поддержка QuotaGiB (квота общего ресурса в ГиБ) для значений свыше 5120 в командлетах для работы с общими папками в плоскости управления и добавлен псевдоним Quota для параметра QuotaGiB.</span><span class="sxs-lookup"><span data-stu-id="7af37-400">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span> 
    - <span data-ttu-id="7af37-401">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="7af37-401">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="7af37-402">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="7af37-402">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="7af37-403">Добавлен псевдоним QuotaGiB для параметра Quota:</span><span class="sxs-lookup"><span data-stu-id="7af37-403">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="7af37-404">Set-AzStorageShareQuota.</span><span class="sxs-lookup"><span data-stu-id="7af37-404">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="7af37-405">Устранена проблема, из-за которой при использовании AzStorageContainerAcl могла очищаться хранимая политика доступа:</span><span class="sxs-lookup"><span data-stu-id="7af37-405">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="7af37-406">Set-AzStorageContainerAcl.</span><span class="sxs-lookup"><span data-stu-id="7af37-406">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="7af37-407">Версия 3.1.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7af37-407">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7af37-408">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="7af37-408">Highlights since the last major release</span></span>
* <span data-ttu-id="7af37-409">Выпуск Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="7af37-409">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="7af37-410">Выпуск Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="7af37-410">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7af37-411">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7af37-411">Az.Compute</span></span>
* <span data-ttu-id="7af37-412">Функция повторного применения виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="7af37-412">VM Reapply feature</span></span>
    - <span data-ttu-id="7af37-413">Добавлен параметр повторного применения в командлет Set-AzVM.</span><span class="sxs-lookup"><span data-stu-id="7af37-413">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="7af37-414">Функция AutomaticRepairs масштабируемого набора виртуальных машин:</span><span class="sxs-lookup"><span data-stu-id="7af37-414">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="7af37-415">Добавлены параметры EnableAutomaticRepair, AutomaticRepairGracePeriod и AutomaticRepairMaxInstanceRepairsPercent в следующие командлеты:   New-AzVmssConfig Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7af37-415">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="7af37-416">Включена поддержка образа из коллекции разных клиентов для New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="7af37-416">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="7af37-417">Добавлен фрагмент Spot в средство заполнения аргументов параметра Priority в командлетах New-AzVM, New-AzVMConfig и New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="7af37-417">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="7af37-418">Добавлены параметры DiskIOPSReadWrite и DiskMBpsReadWrite в командлет Add-AzVmssDataDisk.</span><span class="sxs-lookup"><span data-stu-id="7af37-418">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="7af37-419">Изменен параметр SourceImageId командлета New-AzGalleryImageVersion на необязательный.</span><span class="sxs-lookup"><span data-stu-id="7af37-419">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="7af37-420">Добавлены параметры OSDiskImage и DataDiskImage в командлет New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="7af37-420">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="7af37-421">Добавлен параметр HyperVGeneration в командлет New-AzGalleryImageDefinition.</span><span class="sxs-lookup"><span data-stu-id="7af37-421">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="7af37-422">Добавлены параметры SkipExtensionsOnOverprovisionedVMs в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="7af37-422">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="7af37-423">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="7af37-423">Az.DataBoxEdge</span></span>
* <span data-ttu-id="7af37-424">Добавлен командлет `Get-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="7af37-424">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="7af37-425">Получение заказа.</span><span class="sxs-lookup"><span data-stu-id="7af37-425">Get the Order</span></span>
* <span data-ttu-id="7af37-426">Добавлен командлет `New-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="7af37-426">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="7af37-427">Создание заказа.</span><span class="sxs-lookup"><span data-stu-id="7af37-427">Create new Order</span></span>
* <span data-ttu-id="7af37-428">Добавлен командлет `Remove-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="7af37-428">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="7af37-429">Удаление заказа.</span><span class="sxs-lookup"><span data-stu-id="7af37-429">Remove the Order</span></span>
* <span data-ttu-id="7af37-430">Изменен командлет `New-AzDataBoxEdgeShare`.</span><span class="sxs-lookup"><span data-stu-id="7af37-430">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="7af37-431">Создание локальной общей папки.</span><span class="sxs-lookup"><span data-stu-id="7af37-431">Now creates Local Share</span></span>
* <span data-ttu-id="7af37-432">Добавлен командлет `Set-AzDataBoxEdgeRole`.</span><span class="sxs-lookup"><span data-stu-id="7af37-432">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="7af37-433">Сопоставление IotRole с общей папкой.</span><span class="sxs-lookup"><span data-stu-id="7af37-433">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="7af37-434">Добавлен командлет `Invoke-AzDataBoxEdgeDevice`.</span><span class="sxs-lookup"><span data-stu-id="7af37-434">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="7af37-435">Вызов проверки обновлений, скачивание обновления, установка обновления на устройстве.</span><span class="sxs-lookup"><span data-stu-id="7af37-435">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="7af37-436">Добавлен командлет `Get-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="7af37-436">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="7af37-437">Получение сведений о триггерах.</span><span class="sxs-lookup"><span data-stu-id="7af37-437">Gets the information about Triggers</span></span>
* <span data-ttu-id="7af37-438">Добавлен командлет `New-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="7af37-438">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="7af37-439">Создание триггеров.</span><span class="sxs-lookup"><span data-stu-id="7af37-439">Create new Triggers</span></span>
* <span data-ttu-id="7af37-440">Добавлен командлет `Remove-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="7af37-440">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="7af37-441">Удаление триггеров.</span><span class="sxs-lookup"><span data-stu-id="7af37-441">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7af37-442">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7af37-442">Az.DataFactory</span></span>
* <span data-ttu-id="7af37-443">Обновление пакета SDK Фабрики данных для .NET до версии 4.4.0.</span><span class="sxs-lookup"><span data-stu-id="7af37-443">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="7af37-444">Добавлен параметр ExpressCustomSetup в командлет Set-AzureRmDataFactoryV2IntegrationRuntime для включения конфигураций установки и сторонних компонентов без использования настраиваемого скрипта установки.</span><span class="sxs-lookup"><span data-stu-id="7af37-444">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7af37-445">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7af37-445">Az.DataLakeStore</span></span>
* <span data-ttu-id="7af37-446">Обновлена документация по Get-AzDataLakeStoreDeletedItem и Restore-AzDataLakeStoreDeletedItem.</span><span class="sxs-lookup"><span data-stu-id="7af37-446">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7af37-447">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7af37-447">Az.EventHub</span></span>
* <span data-ttu-id="7af37-448">Исправлена проблема № 10301. Исправлен формат даты маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="7af37-448">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7af37-449">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7af37-449">Az.FrontDoor</span></span>
* <span data-ttu-id="7af37-450">Добавлен параметр MinimumTlsVersion в Enable-AzFrontDoorCustomDomainHttps и New-AzFrontDoorFrontendEndpointObject.</span><span class="sxs-lookup"><span data-stu-id="7af37-450">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="7af37-451">Добавлены параметры HealthProbeMethod и EnabledState в New-AzFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="7af37-451">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="7af37-452">Добавлен новый командлет для создания объекта BackendPoolsSettings для передачи при создании и обновлении Front Door.</span><span class="sxs-lookup"><span data-stu-id="7af37-452">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="7af37-453">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="7af37-453">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7af37-454">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7af37-454">Az.Network</span></span>
* <span data-ttu-id="7af37-455">Изменены примеры параметра FilterData Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="7af37-455">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="7af37-456">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="7af37-456">Az.PrivateDns</span></span>
* <span data-ttu-id="7af37-457">Пакет SDK PrivateDns для .NET обновлен до версии 1.0.0</span><span class="sxs-lookup"><span data-stu-id="7af37-457">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7af37-458">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7af37-458">Az.RecoveryServices</span></span>
* <span data-ttu-id="7af37-459">Включена поддержка Azure Site Recovery для выбора типа диска при включении защиты.</span><span class="sxs-lookup"><span data-stu-id="7af37-459">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="7af37-460">Внесено исправление Azure Site Recovery для изменения действия плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="7af37-460">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="7af37-461">Включена поддержка восстановления SQL Azure Backup для принятия баз данных файлового потока.</span><span class="sxs-lookup"><span data-stu-id="7af37-461">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7af37-462">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7af37-462">Az.RedisCache</span></span>
* <span data-ttu-id="7af37-463">Добавлен параметр MinimumTlsVersion в командлеты New-AzRedisCache и Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="7af37-463">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="7af37-464">Кроме того, добавлен параметр MinimumTlsVersion в выходные данные командлета Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="7af37-464">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="7af37-465">Добавлена проверка параметра -Size для командлетов Set-AzRedisCache и New-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="7af37-465">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="7af37-466">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7af37-466">Az.Resources</span></span>
- <span data-ttu-id="7af37-467">Обновлены командлеты политики для использования новой версии API 2019-06-01 с новым свойством EnforcementMode в назначении политики.</span><span class="sxs-lookup"><span data-stu-id="7af37-467">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="7af37-468">Обновлен пример справки по созданию определения политики</span><span class="sxs-lookup"><span data-stu-id="7af37-468">Updated create policy definition help example</span></span>
- <span data-ttu-id="7af37-469">Исправлена ошибка с параметром -ServicePrincipalName командлета Remove-AZADServicePrincipal с возвратом пустой ссылки, если имя субъекта службы не найдено.</span><span class="sxs-lookup"><span data-stu-id="7af37-469">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="7af37-470">Исправлена ошибка с New-AZADServicePrincipal с возвратом пустой ссылки, если у клиента нет подписки.</span><span class="sxs-lookup"><span data-stu-id="7af37-470">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="7af37-471">Изменен командлет New-AzAdServicePrincipal для добавления учетных данных только для связанного приложения.</span><span class="sxs-lookup"><span data-stu-id="7af37-471">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="7af37-472">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7af37-472">Az.Sql</span></span>
* <span data-ttu-id="7af37-473">Добавлена поддержка ReadReplicaCount для базы данных.</span><span class="sxs-lookup"><span data-stu-id="7af37-473">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="7af37-474">Исправлена ошибка с Set-AzSqlDatabase, если избыточность в пределах зоны не настроена.</span><span class="sxs-lookup"><span data-stu-id="7af37-474">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="7af37-475">Версия 3.0.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7af37-475">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="7af37-476">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="7af37-476">General</span></span>
* <span data-ttu-id="7af37-477">Выпущена версия Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="7af37-477">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7af37-478">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7af37-478">Az.Accounts</span></span>
* <span data-ttu-id="7af37-479">Добавлено сообщение об устаревании для псевдонима "Resolve-Error".</span><span class="sxs-lookup"><span data-stu-id="7af37-479">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="7af37-480">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="7af37-480">Az.Advisor</span></span>
* <span data-ttu-id="7af37-481">Добавлена новая категория Operational Excellence (Эффективность работы) в командлет Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="7af37-481">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7af37-482">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7af37-482">Az.Batch</span></span>
* <span data-ttu-id="7af37-483">`CoreQuota` в `BatchAccountContext` переименован в `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="7af37-483">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="7af37-484">Также появился новый `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="7af37-484">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="7af37-485">Это влияет на **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="7af37-485">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="7af37-486">Параметр **New-AzBatchTask** `-ResourceFile` теперь принимает коллекцию объектов `PSResourceFile`, которые можно создать с помощью нового командлета **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="7af37-486">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="7af37-487">Новый командлет **New-AzBatchResourceFile**, который помогает создавать объекты `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="7af37-487">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="7af37-488">Их можно передавать в **New-AzBatchTask** в параметре `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="7af37-488">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="7af37-489">Это позволяет поддерживать два новых типа файлов ресурсов, которые дополняют существующий метод `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="7af37-489">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="7af37-490">Файлы ресурсов на основе `AutoStorageContainerName` скачивают весь контейнер автоматического хранения в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="7af37-490">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="7af37-491">Файлы ресурсов на основе `StorageContainerUrl` скачивают указанный в URL-адресе контейнер в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="7af37-491">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="7af37-492">Удалено свойство `ApplicationPackages` в `PSApplication`, который возвращается из **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="7af37-492">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="7af37-493">Отдельные пакеты в приложении теперь можно извлечь с помощью **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="7af37-493">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="7af37-494">Например: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="7af37-494">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="7af37-495">`ApplicationId` переименован в `ApplicationName` для **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** и **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="7af37-495">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="7af37-496">Теперь `ApplicationId` является псевдонимом для `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="7af37-496">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="7af37-497">Добавлено новое свойство `PSWindowsUserConfiguration` в `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="7af37-497">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="7af37-498">`Version` переименован в `Name` для `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="7af37-498">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="7af37-499">`BlobSource` переименован в `HttpUrl` для `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="7af37-499">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="7af37-500">Удалено свойство `OSDisk` из `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="7af37-500">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="7af37-501">Удалена операция **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="7af37-501">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="7af37-502">Больше она не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7af37-502">This operation is no longer supported.</span></span>
* <span data-ttu-id="7af37-503">Удалено `TargetOSVersion` из `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="7af37-503">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="7af37-504">`CurrentOSVersion` переименован в `OSVersion` для `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="7af37-504">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="7af37-505">Удалено `DataEgressGiB` и `DataIngressGiB` из `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="7af37-505">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="7af37-506">Операция **Get-AzBatchNodeAgentSku** удалена и заменена на **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="7af37-506">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="7af37-507">**Get-AzBatchSupportedImage** возвращает те же данные, что и **Get-AzBatchNodeAgentSku**, но в более удобном формате.</span><span class="sxs-lookup"><span data-stu-id="7af37-507">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="7af37-508">Также возвращаются новые непроверенные образы.</span><span class="sxs-lookup"><span data-stu-id="7af37-508">New non-verified images are also now returned.</span></span> <span data-ttu-id="7af37-509">Включается и дополнительная информация о `Capabilities` и `BatchSupportEndOfLife` для каждого образа.</span><span class="sxs-lookup"><span data-stu-id="7af37-509">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="7af37-510">Добавлена возможность монтировать файловые системы на каждом узле пула с помощью нового параметра `MountConfiguration` в **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="7af37-510">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="7af37-511">Теперь поддерживаются правила безопасности сети, которые блокируют сетевой доступ к пулу по исходящему порту трафика.</span><span class="sxs-lookup"><span data-stu-id="7af37-511">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="7af37-512">Это выполняется с помощью свойства `SourcePortRanges` для `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="7af37-512">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="7af37-513">Что касается выполнения контейнеров, пакетная служба теперь поддерживает выполнение задачи в рабочей папке контейнера или рабочей папке задачи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="7af37-513">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="7af37-514">Выбор зависит от параметра `WorkingDirectory` в `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="7af37-514">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="7af37-515">Добавлена возможность указать коллекцию общедоступных IP-адресов для `PSNetworkConfiguration` с помощью нового свойства `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="7af37-515">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="7af37-516">Это гарантирует, что узлы в пуле будут иметь IP-адреса из списка, предоставленного пользователем.</span><span class="sxs-lookup"><span data-stu-id="7af37-516">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="7af37-517">Если значение не задано, по умолчанию для `WaitForSuccess` в `PSSTartTask` используется значение `$True` (ранее `$False`).</span><span class="sxs-lookup"><span data-stu-id="7af37-517">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="7af37-518">Если значение не задано, по умолчанию для `Scope` в `PSAutoUserSpecification` используется значение `Pool` (ранее `Task` для Windows или `Pool` для Linux).</span><span class="sxs-lookup"><span data-stu-id="7af37-518">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7af37-519">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7af37-519">Az.Cdn</span></span>
* <span data-ttu-id="7af37-520">Добавлены UrlRewriteAction и CacheKeyQueryStringAction в RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="7af37-520">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="7af37-521">Исправлено несколько ошибок, таких как отсутствующий входной параметр Selector в командлете New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="7af37-521">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7af37-522">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7af37-522">Az.Compute</span></span>
* <span data-ttu-id="7af37-523">Функция набора шифрования диска</span><span class="sxs-lookup"><span data-stu-id="7af37-523">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="7af37-524">Новые командлеты:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="7af37-524">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="7af37-525">Добавлен параметр ProximityPlacementGroupId в следующие командлеты: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="7af37-525">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="7af37-526">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="7af37-526">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="7af37-527">Параметры DiskEncryptionSetId и EncryptionType добавлены в следующие командлеты:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="7af37-527">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="7af37-528">Добавлен параметр PublicIPAddressVersion в New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="7af37-528">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="7af37-529">FileUris для расширения пользовательских скриптов теперь будет защищенным, а не общедоступным параметром</span><span class="sxs-lookup"><span data-stu-id="7af37-529">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="7af37-530">Добавлено ScaleInPolicy в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7af37-530">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="7af37-531">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="7af37-531">Breaking changes</span></span>
    - <span data-ttu-id="7af37-532">Параметр UploadSizeInBytes применяется теперь вместо DiskSizeGB для New-AzDiskConfig, если CreateOption имеет значение Upload</span><span class="sxs-lookup"><span data-stu-id="7af37-532">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="7af37-533">PublishingProfile.Source.ManagedImage.Id заменяется на StorageProfile.Source.Id в объекте GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="7af37-533">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7af37-534">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7af37-534">Az.DataFactory</span></span>
* <span data-ttu-id="7af37-535">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.3.0.</span><span class="sxs-lookup"><span data-stu-id="7af37-535">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7af37-536">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7af37-536">Az.DataLakeStore</span></span>
* <span data-ttu-id="7af37-537">Обновлен пакет SDK для ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), включает следующие исправления</span><span class="sxs-lookup"><span data-stu-id="7af37-537">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="7af37-538">Не создается исключение при невозможности десериализовать значение времени создания для записи в корзине или каталоге.</span><span class="sxs-lookup"><span data-stu-id="7af37-538">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="7af37-539">Предоставляется параметр для времени ожидания запроса в adlsclient</span><span class="sxs-lookup"><span data-stu-id="7af37-539">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="7af37-540">Исправлена передача исходного значения syncflag для восстановления badoffset</span><span class="sxs-lookup"><span data-stu-id="7af37-540">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="7af37-541">Исправлена операция EnumerateDirectory, чтобы она извлекала токен продолжения после проверки ответа</span><span class="sxs-lookup"><span data-stu-id="7af37-541">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="7af37-542">Исправлена ошибка объединения</span><span class="sxs-lookup"><span data-stu-id="7af37-542">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7af37-543">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7af37-543">Az.FrontDoor</span></span>
* <span data-ttu-id="7af37-544">Исправлены разные опечатки в разных частях модуля</span><span class="sxs-lookup"><span data-stu-id="7af37-544">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7af37-545">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7af37-545">Az.HDInsight</span></span>
* <span data-ttu-id="7af37-546">Исправлена ошибка, из-за которой клиент получал сообщение об ошибке 'Not a valid Base-64 string' (Не является допустимой строкой Base64) при выполнении Get-AzHDInsightCluster для получения кластера с хранилищем ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="7af37-546">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="7af37-547">Добавлен параметр с именем ApplicationId в три командлета Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig и New-AzHDInsightCluster, чтобы клиент мог предоставить идентификатор приложения субъекта-службы для доступа к Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="7af37-547">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="7af37-548">Для Microsoft.Azure.Management.HDInsight изменена версия с 2.1.0 на 5.1.0</span><span class="sxs-lookup"><span data-stu-id="7af37-548">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="7af37-549">Удалены пять командлетов:</span><span class="sxs-lookup"><span data-stu-id="7af37-549">Removed five cmdlets:</span></span>
    - <span data-ttu-id="7af37-550">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="7af37-550">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="7af37-551">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="7af37-551">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="7af37-552">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="7af37-552">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="7af37-553">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7af37-553">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="7af37-554">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7af37-554">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="7af37-555">Добавлены три командлета:</span><span class="sxs-lookup"><span data-stu-id="7af37-555">Added three cmdlets:</span></span>
    - <span data-ttu-id="7af37-556">Get-AzHDInsightMonitoring заменяет собой Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="7af37-556">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="7af37-557">Enable-AzHDInsightMonitoring заменяет собой Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="7af37-557">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="7af37-558">Disable-AzHDInsightMonitoring заменяет собой Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="7af37-558">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="7af37-559">Исправлен командлет Get-AzHDInsightProperties, чтобы он поддерживал получение сведений о возможностях из определенного расположения.</span><span class="sxs-lookup"><span data-stu-id="7af37-559">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="7af37-560">Удалены наборы параметров ("Spark1", "Spark2") из Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="7af37-560">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="7af37-561">Добавлены примеры в справочные документы по командлету Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="7af37-561">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="7af37-562">Изменен тип выходных данных для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="7af37-562">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="7af37-563">Для Get-AzHDInsightProperties тип выходных данных изменен с CapabilitiesResponse на AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="7af37-563">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="7af37-564">Для Remove-AzHDInsightCluster тип выходных данных изменен с ClusterGetResponse на bool.</span><span class="sxs-lookup"><span data-stu-id="7af37-564">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="7af37-565">Для Set-AzHDInsightGatewaySettings тип выходных данных изменен с HttpConnectivitySettings на GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="7af37-565">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="7af37-566">Добавлены несколько условий для проверки сценариев.</span><span class="sxs-lookup"><span data-stu-id="7af37-566">Added some scenario test cases.</span></span>
* <span data-ttu-id="7af37-567">Удалены несколько псевдонимов: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="7af37-567">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7af37-568">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7af37-568">Az.IotHub</span></span>
* <span data-ttu-id="7af37-569">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="7af37-569">Breaking changes:</span></span>
    - <span data-ttu-id="7af37-570">Командлет Add-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="7af37-570">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="7af37-571">Удален набор параметров __AllParameterSets для командлета Add-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="7af37-571">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="7af37-572">Командлет Get-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="7af37-572">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="7af37-573">Удален набор параметров __AllParameterSets для командлета Get-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="7af37-573">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="7af37-574">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties.</span><span class="sxs-lookup"><span data-stu-id="7af37-574">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="7af37-575">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties.</span><span class="sxs-lookup"><span data-stu-id="7af37-575">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="7af37-576">Командлет New-AzIotHubExportDevice больше не поддерживает псевдоним New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="7af37-576">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="7af37-577">Командлет New-AzIotHubImportDevice больше не поддерживает псевдоним New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="7af37-577">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="7af37-578">Командлет Remove-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="7af37-578">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="7af37-579">Удален набор параметров __AllParameterSets для командлета Remove-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="7af37-579">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="7af37-580">Командлет Set-AzIotHub теперь не поддерживает параметр OperationsMonitoringProperties и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="7af37-580">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="7af37-581">Удален набор параметров UpdateOperationsMonitoringProperties для командлета Set-AzIotHub.</span><span class="sxs-lookup"><span data-stu-id="7af37-581">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7af37-582">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7af37-582">Az.RecoveryServices</span></span>
* <span data-ttu-id="7af37-583">Azure Site Recovery поддерживает настройку сетевых ресурсов, например групп безопасности сети, общедоступных IP-адресов и внутренних подсистем балансировки нагрузки из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="7af37-583">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="7af37-584">Azure Site Recovery поддерживает запись на управляемый диск из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="7af37-584">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="7af37-585">Azure Site Recovery поддерживает сокращение NIC из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="7af37-585">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="7af37-586">Azure Site Recovery поддерживает ускорение сети NIC из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="7af37-586">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="7af37-587">Azure Site Recovery поддерживает автоматическое обновление агента из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="7af37-587">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="7af37-588">Azure Site Recovery поддерживает стандартный SSD-накопитель из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="7af37-588">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="7af37-589">Azure Site Recovery поддерживает двухпроходное шифрование диска Azure из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="7af37-589">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="7af37-590">Azure Site Recovery поддерживает новый добавленный диск из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="7af37-590">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="7af37-591">Добавлена функция SoftDelete для виртуальных машин и соответствующие тесты</span><span class="sxs-lookup"><span data-stu-id="7af37-591">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="7af37-592">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7af37-592">Az.Resources</span></span>
* <span data-ttu-id="7af37-593">Обновлена сборка зависимостей Microsoft.Extensions.Caching.Memory с версии 1.1.1 до 2.2</span><span class="sxs-lookup"><span data-stu-id="7af37-593">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7af37-594">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7af37-594">Az.Network</span></span>
* <span data-ttu-id="7af37-595">Изменены все командлеты для PrivateEndpointConnection, чтобы они поддерживали универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="7af37-595">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="7af37-596">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="7af37-596">Updated cmdlet:</span></span>
        - <span data-ttu-id="7af37-597">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="7af37-597">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7af37-598">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="7af37-598">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7af37-599">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="7af37-599">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7af37-600">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="7af37-600">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7af37-601">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7af37-601">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="7af37-602">Добавлен новый командлет для PrivateLinkResource, который поддерживает универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="7af37-602">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="7af37-603">Новый командлет</span><span class="sxs-lookup"><span data-stu-id="7af37-603">New cmdlet:</span></span>
        - <span data-ttu-id="7af37-604">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="7af37-604">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="7af37-605">Добавлены новые поля и параметр для протокола прокси версии 2.</span><span class="sxs-lookup"><span data-stu-id="7af37-605">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="7af37-606">Добавлено свойство EnableProxyProtocol в PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7af37-606">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="7af37-607">Добавлено свойство LinkIdentifier в PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7af37-607">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="7af37-608">Обновлен New-AzPrivateLinkService для поддержки нового необязательного параметра EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="7af37-608">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="7af37-609">Исправлено описание параметра в справочной документации по командлету New-AzApplicationGatewaySku.</span><span class="sxs-lookup"><span data-stu-id="7af37-609">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="7af37-610">Новые командлеты для поддержки политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="7af37-610">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="7af37-611">Добавлена поддержка дочерних ресурсов RouteTables для VirtualHub</span><span class="sxs-lookup"><span data-stu-id="7af37-611">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="7af37-612">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="7af37-612">New cmdlets added:</span></span>
        - <span data-ttu-id="7af37-613">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="7af37-613">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="7af37-614">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="7af37-614">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="7af37-615">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="7af37-615">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="7af37-616">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="7af37-616">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="7af37-617">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="7af37-617">Set-AzVirtualHub</span></span>
* <span data-ttu-id="7af37-618">Добавлена поддержка новых свойств SKU для VirtualHub и VirtualWANType в VirtualWan</span><span class="sxs-lookup"><span data-stu-id="7af37-618">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="7af37-619">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="7af37-619">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="7af37-620">New-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="7af37-620">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="7af37-621">Update-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="7af37-621">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="7af37-622">New-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="7af37-622">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="7af37-623">Update-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="7af37-623">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="7af37-624">Добавлена поддержка свойства EnableInternetSecurity для HubVnetConnection, VpnConnection и ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="7af37-624">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="7af37-625">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="7af37-625">New cmdlets added:</span></span>
        - <span data-ttu-id="7af37-626">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="7af37-626">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="7af37-627">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="7af37-627">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="7af37-628">New-AzureRmVirtualHubVnetConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="7af37-628">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="7af37-629">New-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="7af37-629">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="7af37-630">Update-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="7af37-630">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="7af37-631">New-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="7af37-631">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="7af37-632">Set-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="7af37-632">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="7af37-633">Добавлена поддержка настройки политики верхнего уровня WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="7af37-633">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="7af37-634">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="7af37-634">New cmdlets added:</span></span>
        - <span data-ttu-id="7af37-635">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="7af37-635">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="7af37-636">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="7af37-636">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="7af37-637">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="7af37-637">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="7af37-638">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="7af37-638">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="7af37-639">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="7af37-639">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="7af37-640">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="7af37-640">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="7af37-641">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="7af37-641">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="7af37-642">New-AzApplicationGatewayFirewallPolicy: добавлены параметры PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="7af37-642">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="7af37-643">Добавлена поддержка оператора Geo-Match для CustomRule</span><span class="sxs-lookup"><span data-stu-id="7af37-643">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="7af37-644">Добавлен параметр GeoMatch в оператор для FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="7af37-644">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="7af37-645">Добавлена поддержка политики брандмауэра perListener и perSite</span><span class="sxs-lookup"><span data-stu-id="7af37-645">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="7af37-646">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="7af37-646">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="7af37-647">New-AzApplicationGatewayHttpListener: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="7af37-647">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="7af37-648">New-AzApplicationGatewayPathRuleConfig: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="7af37-648">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="7af37-649">Исправлен учет регистра для требуемой подсети с именем AzureBastionSubnet в PSBastion</span><span class="sxs-lookup"><span data-stu-id="7af37-649">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="7af37-650">Поддержка полного доменного имени назначения в правилах сети и преобразованного полного доменного имени в правилах NAT для брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="7af37-650">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="7af37-651">Добавлена поддержка ресурсов верхнего уровня RouteTables для IpGroup</span><span class="sxs-lookup"><span data-stu-id="7af37-651">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="7af37-652">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="7af37-652">New cmdlets added:</span></span>
        - <span data-ttu-id="7af37-653">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="7af37-653">New-AzIpGroup</span></span>
        - <span data-ttu-id="7af37-654">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="7af37-654">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="7af37-655">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="7af37-655">Get-AzIpGroup</span></span>
        - <span data-ttu-id="7af37-656">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="7af37-656">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7af37-657">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7af37-657">Az.ServiceFabric</span></span>
* <span data-ttu-id="7af37-658">Удален командлет Add-AzServiceFabricApplicationCertificate, так как соответствующий сценарий выполняется командлетом Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="7af37-658">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="7af37-659">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7af37-659">Az.Sql</span></span>
* <span data-ttu-id="7af37-660">Добавлена поддержка восстановления удаленных баз данных в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="7af37-660">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="7af37-661">Из кода удалены старые командлеты аудита.</span><span class="sxs-lookup"><span data-stu-id="7af37-661">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="7af37-662">Удалены нерекомендуемые псевдонимы:</span><span class="sxs-lookup"><span data-stu-id="7af37-662">Removed deprecated aliases:</span></span>
* <span data-ttu-id="7af37-663">Get-AzSqlDatabaseIndexRecommendations (вместо него используйте Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="7af37-663">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="7af37-664">Get-AzSqlDatabaseRestorePoints (вместо него используйте Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="7af37-664">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="7af37-665">Удален командлет Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7af37-665">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="7af37-666">Удалены псевдонимы для нерекомендуемых командлетов параметров оценки уязвимостей</span><span class="sxs-lookup"><span data-stu-id="7af37-666">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="7af37-667">Командлеты расширенного обнаружения угроз объявлены устаревшими</span><span class="sxs-lookup"><span data-stu-id="7af37-667">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="7af37-668">Добавлены командлеты для отключения и включения рекомендаций о конфиденциальности для столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="7af37-668">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7af37-669">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7af37-669">Az.Storage</span></span>
* <span data-ttu-id="7af37-670">Поддержка включения большой общей папки при создании или обновлении учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="7af37-670">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="7af37-671">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7af37-671">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="7af37-672">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7af37-672">Set-AzStorageAccount</span></span>
* <span data-ttu-id="7af37-673">При закрытии или получении маркера файла пропускается проверка того, является ли входной путь файлом или каталогом, чтобы избежать сбоев при получении объектов в состоянии DeletePending.</span><span class="sxs-lookup"><span data-stu-id="7af37-673">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="7af37-674">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="7af37-674">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="7af37-675">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="7af37-675">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="7af37-676">2.8.0 — октябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7af37-676">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="7af37-677">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="7af37-677">General</span></span>
* <span data-ttu-id="7af37-678">Выпуск Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="7af37-678">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7af37-679">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7af37-679">Az.Accounts</span></span>
* <span data-ttu-id="7af37-680">Обновление телеметрии и перезаписи URL-адресов для созданных модулей, исправление для модульных тестов Windows.</span><span class="sxs-lookup"><span data-stu-id="7af37-680">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7af37-681">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7af37-681">Az.ApiManagement</span></span>
* <span data-ttu-id="7af37-682">**Set-AzApiManagementApi** — в ApiVersionSet добавлена поддержка обновления API.</span><span class="sxs-lookup"><span data-stu-id="7af37-682">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="7af37-683">исправлена проблема https://github.com/Azure/azure-powershell/issues/10068.</span><span class="sxs-lookup"><span data-stu-id="7af37-683">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7af37-684">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7af37-684">Az.Automation</span></span>
* <span data-ttu-id="7af37-685">Исправлен командлет New-AzureAutomationSoftwareUpdateConfiguration для параметра перезагрузки Linux.</span><span class="sxs-lookup"><span data-stu-id="7af37-685">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="7af37-686">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7af37-686">Az.Batch</span></span>
* <span data-ttu-id="7af37-687">Командлет **Get-AzBatchNodeAgentSku** объявлен устаревшим и будет заменен на **Get-AzBatchSupportImage** в версии 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="7af37-687">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7af37-688">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7af37-688">Az.Compute</span></span>
* <span data-ttu-id="7af37-689">В командлеты New-AzVM и New-AzVmss добавлены параметры Priority, EvictionPolicy и MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="7af37-689">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="7af37-690">Исправлены предупреждающее сообщение для командлетов Add-AzVMAdditionalUnattendContent и Add-AzVMSshPublicKey и справочная документация по ним.</span><span class="sxs-lookup"><span data-stu-id="7af37-690">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="7af37-691">Для Set-AzVMDiskEncryptionExtension исправлено исключение -skipVmBackup для виртуальных машин Linux с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="7af37-691">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="7af37-692">Исправлена ошибка при изменении параметров шифрования в Set-AzVMDiskEncryptionExtension, реализован двухэтапный сценарий.</span><span class="sxs-lookup"><span data-stu-id="7af37-692">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7af37-693">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7af37-693">Az.DataFactory</span></span>
* <span data-ttu-id="7af37-694">Добавлены команды CRUD для потока данных Фабрики данных Azure версии 2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow и Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="7af37-694">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="7af37-695">Добавлены команды действий для сеанса отладки потока данных Фабрики данных Azure версии 2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand и Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="7af37-695">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="7af37-696">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.2.0.</span><span class="sxs-lookup"><span data-stu-id="7af37-696">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7af37-697">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7af37-697">Az.DataLakeStore</span></span>
* <span data-ttu-id="7af37-698">Проверка учетной записи исправлена так, чтобы учетные записи, содержащие знак "-", можно было передавать без домена.</span><span class="sxs-lookup"><span data-stu-id="7af37-698">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="7af37-699">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="7af37-699">Az.HealthcareApis</span></span>
* <span data-ttu-id="7af37-700">Версия PowerShell обновлена до 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="7af37-700">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="7af37-701">Версия пакета SDK обновлена до 1.0.2.</span><span class="sxs-lookup"><span data-stu-id="7af37-701">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="7af37-702">В тестах обновлены ссылки на новую версию пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="7af37-702">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="7af37-703">Вложенная выходная структура заменена на плоскую.</span><span class="sxs-lookup"><span data-stu-id="7af37-703">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7af37-704">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7af37-704">Az.IotHub</span></span>
* <span data-ttu-id="7af37-705">Добавлен новый источник маршрутизации DigitalTwinChangeEvents.</span><span class="sxs-lookup"><span data-stu-id="7af37-705">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="7af37-706">Исправлены незначительные ошибки: Get-AzIothub не возвращает subscriptionId.</span><span class="sxs-lookup"><span data-stu-id="7af37-706">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="7af37-707">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7af37-707">Az.Monitor</span></span>
* <span data-ttu-id="7af37-708">Добавлены новые получатели групп действий: -ItsmReceiver, -VoiceReceiver, -ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver.</span><span class="sxs-lookup"><span data-stu-id="7af37-708">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="7af37-709">Для получателей включите общую схему оповещений.</span><span class="sxs-lookup"><span data-stu-id="7af37-709">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="7af37-710">Это не касается получателей SMS, push-уведомлений приложения Azure, ITSM и голосовых сообщений.</span><span class="sxs-lookup"><span data-stu-id="7af37-710">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="7af37-711">Веб-перехватчики теперь поддерживают аутентификацию Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7af37-711">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7af37-712">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7af37-712">Az.Network</span></span>
* <span data-ttu-id="7af37-713">Добавлен новый командлет Get-AzAvailableServiceAlias, позволяющий получить псевдонимы для политик конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="7af37-713">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="7af37-714">В подключениях шлюза виртуальной сети появилась возможность добавлять селекторы трафика.</span><span class="sxs-lookup"><span data-stu-id="7af37-714">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="7af37-715">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="7af37-715">New cmdlets added:</span></span>
        - <span data-ttu-id="7af37-716">New-AzureRmTrafficSelectorPolicy.</span><span class="sxs-lookup"><span data-stu-id="7af37-716">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="7af37-717">В командлеты добавлены необязательные параметры -TrafficSelectorPolicies, -New-AzureRmVirtualNetworkGatewayConnection, -Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="7af37-717">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="7af37-718">В конфигурациях правил сетевой безопасности добавлена поддержка протоколов ESP и AH.</span><span class="sxs-lookup"><span data-stu-id="7af37-718">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="7af37-719">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="7af37-719">Updated cmdlets:</span></span>
        - <span data-ttu-id="7af37-720">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="7af37-720">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="7af37-721">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="7af37-721">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="7af37-722">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="7af37-722">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="7af37-723">Улучшена обработка исключений в командлетах Cortex.</span><span class="sxs-lookup"><span data-stu-id="7af37-723">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="7af37-724">Выпущены новые поколения и номера SKU VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="7af37-724">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="7af37-725">Представлены новые поколения VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="7af37-725">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="7af37-726">Представлены новые номера SKU VirtualNetworkGateways с высокой пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="7af37-726">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7af37-727">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7af37-727">Az.RedisCache</span></span>
* <span data-ttu-id="7af37-728">В справочную документацию по Set-AzRedisCache добавлены недостающие значения для параметра -Size.</span><span class="sxs-lookup"><span data-stu-id="7af37-728">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="7af37-729">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7af37-729">Az.Sql</span></span>
* <span data-ttu-id="7af37-730">Добавлена возможность назначать администратора Active Directory в Управляемом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="7af37-730">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7af37-731">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7af37-731">Az.Storage</span></span>
* <span data-ttu-id="7af37-732">Клиентская библиотека службы хранилища Azure обновлена до версии 11.1.0.</span><span class="sxs-lookup"><span data-stu-id="7af37-732">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="7af37-733">NextPageLink теперь позволяет получить список контейнеров с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="7af37-733">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="7af37-734">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7af37-734">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="7af37-735">NextPageLink теперь позволяет получить список учетных записей хранения из подписки.</span><span class="sxs-lookup"><span data-stu-id="7af37-735">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="7af37-736">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7af37-736">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="7af37-737">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="7af37-737">Az.StorageSync</span></span>
* <span data-ttu-id="7af37-738">Исправлена проблема 9810 с Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="7af37-738">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7af37-739">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7af37-739">Az.Websites</span></span>
* <span data-ttu-id="7af37-740">Обновление плана службы приложений с помощью Set-AzWebApp приводило к сбою приложения.</span><span class="sxs-lookup"><span data-stu-id="7af37-740">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="7af37-741">2.7.0 — сентябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7af37-741">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="7af37-742">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7af37-742">Az.ApiManagement</span></span>
* <span data-ttu-id="7af37-743">В справочной документации по командлету Set-AzApiManagementPolicy обновлено описание параметра -Format.</span><span class="sxs-lookup"><span data-stu-id="7af37-743">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="7af37-744">Из справочной документации удалены ссылки на нерекомендуемый командлет Update-AzApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="7af37-744">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="7af37-745">Вместо него следует использовать командлет Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="7af37-745">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7af37-746">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7af37-746">Az.Automation</span></span>
* <span data-ttu-id="7af37-747">В справочной документации по командлету Register-AzAutomationDscNode исправлена опечатка в примере.</span><span class="sxs-lookup"><span data-stu-id="7af37-747">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="7af37-748">Добавлено уточнение об ограничениях ОС для командлета Register-AzAutomationDSCNode.</span><span class="sxs-lookup"><span data-stu-id="7af37-748">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="7af37-749">Исправлено исключение пустой ссылки для параметра -Wait в командлете Start-AzAutomationRunbook.</span><span class="sxs-lookup"><span data-stu-id="7af37-749">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7af37-750">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7af37-750">Az.Compute</span></span>
* <span data-ttu-id="7af37-751">Добавлен параметр UploadSizeInBytes для командлета New-AzDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="7af37-751">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="7af37-752">Добавлен добавочный параметр для командлета New-AzSnapshotConfig.</span><span class="sxs-lookup"><span data-stu-id="7af37-752">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="7af37-753">Для виртуальной машины добавлены такие функции с низким приоритетом:</span><span class="sxs-lookup"><span data-stu-id="7af37-753">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="7af37-754">Для командлета New-AzVMConfig добавлены параметры MaxPrice, EvictionPolicy и Priority.</span><span class="sxs-lookup"><span data-stu-id="7af37-754">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="7af37-755">Для командлетов New-AzVmssConfig, Update-AzVM и Update-AzVmss добавлен параметр MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="7af37-755">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="7af37-756">Для командлета Get-AzAvailabilitySet устранена проблема со ссылкой на виртуальную машину, когда в нем перечисляются все группы доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="7af37-756">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="7af37-757">Исправлено исключение NULL для командлета Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="7af37-757">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="7af37-758">Исправлен метод поиска VHD для относительной конечной позиции.</span><span class="sxs-lookup"><span data-stu-id="7af37-758">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="7af37-759">Устранена проблема с UltraSSD для командлетов New-AzVM и Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="7af37-759">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7af37-760">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7af37-760">Az.DataFactory</span></span>
* <span data-ttu-id="7af37-761">Добавлены 3 новые команды для ADF версии 2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription и Get-AzDataFactoryV2TriggerSubscriptionStatus.</span><span class="sxs-lookup"><span data-stu-id="7af37-761">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="7af37-762">Пакет SDK ADF для .NET обновлен до версии 4.1.3.</span><span class="sxs-lookup"><span data-stu-id="7af37-762">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7af37-763">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7af37-763">Az.HDInsight</span></span>
* <span data-ttu-id="7af37-764">Укажите критические изменения.</span><span class="sxs-lookup"><span data-stu-id="7af37-764">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7af37-765">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7af37-765">Az.IotHub</span></span>
* <span data-ttu-id="7af37-766">Добавлена поддержка для вызова отработки отказа для IotHub в георегион аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="7af37-766">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="7af37-767">Добавлена поддержка для управления обогащением сообщений для IotHub.</span><span class="sxs-lookup"><span data-stu-id="7af37-767">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="7af37-768">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="7af37-768">New cmdlets are:</span></span>
    - <span data-ttu-id="7af37-769">Add-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="7af37-769">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="7af37-770">Get-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="7af37-770">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="7af37-771">Remove-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="7af37-771">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="7af37-772">Set-AzIotHubMessageEnrichment.</span><span class="sxs-lookup"><span data-stu-id="7af37-772">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7af37-773">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7af37-773">Az.Monitor</span></span>
* <span data-ttu-id="7af37-774">Указание на самую последнюю версию пакета SDK для монитора, т. е. 0.24.1-preview:</span><span class="sxs-lookup"><span data-stu-id="7af37-774">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="7af37-775">В командлеты метрик добавлены некритические изменения, т. е. перечисление единиц поддерживает несколько новых значений.</span><span class="sxs-lookup"><span data-stu-id="7af37-775">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="7af37-776">Эти командлеты доступны только для чтения, поэтому входные данные командлетов не будут изменены.</span><span class="sxs-lookup"><span data-stu-id="7af37-776">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="7af37-777">Актуальная версия API запросов **ActionGroups** — **2019-06-01**. До этого была версия **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="7af37-777">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="7af37-778">Тесты сценария обновлены в соответствии с этим изменением.</span><span class="sxs-lookup"><span data-stu-id="7af37-778">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="7af37-779">В конструкторы классов **EmailReceiver** и **WebhookReceiver** добавлен один новый обязательный аргумент — логическое значение с именем **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="7af37-779">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="7af37-780">Сейчас для него установлено значение **false**, чтобы скрыть это критическое изменение от командлетов.</span><span class="sxs-lookup"><span data-stu-id="7af37-780">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="7af37-781">**Примечание**. Это временное изменение, которое должно быть подтверждено командой оповещения.</span><span class="sxs-lookup"><span data-stu-id="7af37-781">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="7af37-782">Порядок аргументов для конструктора класса **Source** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="7af37-782">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="7af37-783">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="7af37-783">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="7af37-784">Порядок аргументов для конструктора класса **AlertingAction** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="7af37-784">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="7af37-785">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="7af37-785">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="7af37-786">Добавлена поддержка критериев динамического порога для оповещения метрики версии 2:</span><span class="sxs-lookup"><span data-stu-id="7af37-786">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="7af37-787">New-AzMetricAlertRuleV2Criteria: теперь также позволяет создавать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="7af37-787">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="7af37-788">Add-AzMetricAlertRuleV2: теперь также позволяет принимать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="7af37-788">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="7af37-789">Добавлены усовершенствования в командлетах запланированных правил запросов (SQR).</span><span class="sxs-lookup"><span data-stu-id="7af37-789">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="7af37-790">Командлеты будут принимать параметр Location в обоих форматах: расположение (например, eastus) или отображаемое имя расположения (например, "восточная часть США").</span><span class="sxs-lookup"><span data-stu-id="7af37-790">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="7af37-791">Параметр Enabled проиллюстрирован в файлах справки надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="7af37-791">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="7af37-792">Добавлены примеры для необязательного параметра ActionGroup.</span><span class="sxs-lookup"><span data-stu-id="7af37-792">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="7af37-793">Все файлы справки улучшены.</span><span class="sxs-lookup"><span data-stu-id="7af37-793">Overall improved help files</span></span>
* <span data-ttu-id="7af37-794">Исправлена ошибка в определении типа области для командлета Set-AzActionRule.</span><span class="sxs-lookup"><span data-stu-id="7af37-794">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7af37-795">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7af37-795">Az.Network</span></span>
* <span data-ttu-id="7af37-796">Исправлен неправильный пример в справочной документации по командлету New-AzApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="7af37-796">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="7af37-797">В справочную документацию по командлету Get-AzNetworkWatcherPacketCapture добавлено примечание, посвященное извлечению всех свойств для записи пакетов.</span><span class="sxs-lookup"><span data-stu-id="7af37-797">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="7af37-798">В справочной документации по командлету Test-AzNetworkWatcherIPFlow исправлен пример: теперь он правильно перечисляет сетевые карты.</span><span class="sxs-lookup"><span data-stu-id="7af37-798">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="7af37-799">Улучшен анализ облачных исключений для отображения дополнительных сведений (при их наличии).</span><span class="sxs-lookup"><span data-stu-id="7af37-799">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="7af37-800">Улучшен анализ облачных исключений для обработки дополнительного типа исключения SDK.</span><span class="sxs-lookup"><span data-stu-id="7af37-800">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="7af37-801">Исправлено неправильное сопоставление моделей правил безопасности.</span><span class="sxs-lookup"><span data-stu-id="7af37-801">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="7af37-802">Добавлены свойства сетевого интерфейса для компонента частного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="7af37-802">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="7af37-803">Для интерфейса PSNetworkInterface добавлено свойство PrivateEndpoint с типом PSResourceId.</span><span class="sxs-lookup"><span data-stu-id="7af37-803">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="7af37-804">В PSNetworkInterfaceIPConfiguration добавлено свойство PrivateLinkConnectionProperties с типом PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="7af37-804">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="7af37-805">Добавлен новый класс модели: PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="7af37-805">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="7af37-806">Добавлен новый тип ApplicationRuleProtocolType "mssql" для ресурса Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="7af37-806">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="7af37-807">Поддержка многоканального подключения в Виртуальной глобальной сети:</span><span class="sxs-lookup"><span data-stu-id="7af37-807">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="7af37-808">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="7af37-808">New cmdlets</span></span>
        - <span data-ttu-id="7af37-809">New-AzVpnSiteLink;</span><span class="sxs-lookup"><span data-stu-id="7af37-809">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="7af37-810">New-AzVpnSiteLinkConnection;</span><span class="sxs-lookup"><span data-stu-id="7af37-810">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="7af37-811">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="7af37-811">Updated cmdlet:</span></span>
        - <span data-ttu-id="7af37-812">New-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="7af37-812">New-VpnSite</span></span>
        - <span data-ttu-id="7af37-813">Update-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="7af37-813">Update-VpnSite</span></span>
        - <span data-ttu-id="7af37-814">New-VpnConnection;</span><span class="sxs-lookup"><span data-stu-id="7af37-814">New-VpnConnection</span></span>
        - <span data-ttu-id="7af37-815">Update-VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="7af37-815">Update-VpnConnection</span></span>
* <span data-ttu-id="7af37-816">Исправлены документы с некоторыми примерами PowerShell для использования командлетов AZ вместо командлетов AzureRM.</span><span class="sxs-lookup"><span data-stu-id="7af37-816">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7af37-817">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7af37-817">Az.RecoveryServices</span></span>
* <span data-ttu-id="7af37-818">Для объекта AzureVMpolicy добавлен новый атрибут — ProtectedItemsCount.</span><span class="sxs-lookup"><span data-stu-id="7af37-818">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="7af37-819">Добавлены тесты для политики виртуальной машины и восстановления исходной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="7af37-819">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="7af37-820">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7af37-820">Az.Resources</span></span>
* <span data-ttu-id="7af37-821">Исправлена ошибка, при которой не удавалось вызвать командлет New-AzRoleAssignment без параметра Scope.</span><span class="sxs-lookup"><span data-stu-id="7af37-821">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7af37-822">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7af37-822">Az.ServiceFabric</span></span>
* <span data-ttu-id="7af37-823">Исправлена опечатка в примере в справочной документации по командлету Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="7af37-823">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="7af37-824">Добавлены новые командлеты для управления приложениями и службами:</span><span class="sxs-lookup"><span data-stu-id="7af37-824">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="7af37-825">New-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="7af37-825">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="7af37-826">New-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="7af37-826">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="7af37-827">New-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="7af37-827">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="7af37-828">New-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="7af37-828">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="7af37-829">Update-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="7af37-829">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="7af37-830">Get-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="7af37-830">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="7af37-831">Get-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="7af37-831">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="7af37-832">Get-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="7af37-832">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="7af37-833">Get-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="7af37-833">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="7af37-834">Remove-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="7af37-834">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="7af37-835">Remove-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="7af37-835">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="7af37-836">Remove-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="7af37-836">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="7af37-837">Remove-AzServiceFabricServic.</span><span class="sxs-lookup"><span data-stu-id="7af37-837">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="7af37-838">Пакет SDK для Service Fabric обновлен до версии 1.2.0, в которой используется версия API 2019-03-01 поставщика ресурсов Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="7af37-838">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="7af37-839">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="7af37-839">Az.SignalR</span></span>
* <span data-ttu-id="7af37-840">Добавлены командлеты Update, Restart, CheckNameAvailability и GetUsage.</span><span class="sxs-lookup"><span data-stu-id="7af37-840">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="7af37-841">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7af37-841">Az.Sql</span></span>
* <span data-ttu-id="7af37-842">Обновлен пример в справочной документации по командлету Get-AzSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="7af37-842">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="7af37-843">Добавлен пример виртуального ядра для командлета создания эластичного пула (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="7af37-843">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="7af37-844">Удалена проверка свойства EmailAddresses и того, что свойство EmailAdmins правильное в случае, если свойство EmailAddresses пустое в командлетах Set-AzSqlServerAdvancedThreatProtectionPolicy и Set-AzSqlDatabaseAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="7af37-844">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="7af37-845">Теперь, если существует несколько параметров диагностики, включающих категорию аудита, параметры аудита сервера и базы данных удаляются.</span><span class="sxs-lookup"><span data-stu-id="7af37-845">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="7af37-846">Исправлена проверка адресов электронной почты в нескольких командлетах оценки уязвимостей SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting и Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="7af37-846">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7af37-847">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7af37-847">Az.Storage</span></span>
* <span data-ttu-id="7af37-848">Обновлен пример в справочной документации по командлету Get-AzStorageAccountKey.</span><span class="sxs-lookup"><span data-stu-id="7af37-848">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="7af37-849">Теперь при отправке и загрузке файла Azure в конечном файле сохраняются свойства SMB исходного файла (атрибуты файла, время создания файла, время последней записи файла).</span><span class="sxs-lookup"><span data-stu-id="7af37-849">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="7af37-850">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7af37-850">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="7af37-851">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7af37-851">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="7af37-852">Исправлена операция отправки блочного BLOB-объекта, в которой происходили сбои свойств и метаданных в контейнере с включенной ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="7af37-852">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="7af37-853">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7af37-853">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="7af37-854">Добавлена поддержка управления общими папками Azure в API плоскости управления с помощью таких командлетов:</span><span class="sxs-lookup"><span data-stu-id="7af37-854">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="7af37-855">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="7af37-855">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="7af37-856">Get-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="7af37-856">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="7af37-857">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="7af37-857">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="7af37-858">Remove-AzRmStorageShare.</span><span class="sxs-lookup"><span data-stu-id="7af37-858">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7af37-859">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7af37-859">Az.Websites</span></span>
* <span data-ttu-id="7af37-860">Устранена проблема, из-за которой теги webapp удалялись при переносе приложения в новый ASP.</span><span class="sxs-lookup"><span data-stu-id="7af37-860">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="7af37-861">Теперь командлет Publish-AzureWebapp работает в Linux и Windows.</span><span class="sxs-lookup"><span data-stu-id="7af37-861">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="7af37-862">Обновлен пример в справочной документации по командлету Get-AzWebAppPublishingProfile.</span><span class="sxs-lookup"><span data-stu-id="7af37-862">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="7af37-863">2.6.0 — август 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7af37-863">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="7af37-864">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="7af37-864">General</span></span>
* <span data-ttu-id="7af37-865">Исправлены опечатки в модулях.</span><span class="sxs-lookup"><span data-stu-id="7af37-865">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7af37-866">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7af37-866">Az.Accounts</span></span>
* <span data-ttu-id="7af37-867">Добавлена поддержка назначаемого пользователем удостоверения MSI при проверке подлинности в Функциях Azure (№ 9479).</span><span class="sxs-lookup"><span data-stu-id="7af37-867">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="7af37-868">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="7af37-868">Az.Aks</span></span>
* <span data-ttu-id="7af37-869">Устранена проблема с выходными данными для Get-AzAks.</span><span class="sxs-lookup"><span data-stu-id="7af37-869">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="7af37-870">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9847.</span><span class="sxs-lookup"><span data-stu-id="7af37-870">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7af37-871">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7af37-871">Az.ApiManagement</span></span>
* <span data-ttu-id="7af37-872">исправлена проблема https://github.com/Azure/azure-powershell/issues/9351.</span><span class="sxs-lookup"><span data-stu-id="7af37-872">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="7af37-873">Обновлена версия NuGet для .NET, которая не накладывает ограничений на productId, apiId, groupId и userId.</span><span class="sxs-lookup"><span data-stu-id="7af37-873">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="7af37-874">**Get-AzApiManagementProduct**. Добавлена поддержка запросов к продуктам с помощью API.</span><span class="sxs-lookup"><span data-stu-id="7af37-874">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="7af37-875">**New-AzApiManagementApiRevision**. Устранена проблема, из-за которой не задавался параметр ApiRevisionDescription при создании новой редакции API https://github.com/Azure/azure-powershell/issues/9752.</span><span class="sxs-lookup"><span data-stu-id="7af37-875">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="7af37-876">Исправлено написание имени модели c PsApiManagementOAuth2AuthrozationServer на PsApiManagementOAuth2AuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="7af37-876">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7af37-877">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7af37-877">Az.Batch</span></span>
* <span data-ttu-id="7af37-878">Исправлена опечатка в написании Windows со строчной буквы в справочных сообщениях и документации.</span><span class="sxs-lookup"><span data-stu-id="7af37-878">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7af37-879">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7af37-879">Az.Cdn</span></span>
* <span data-ttu-id="7af37-880">Исправлена опечатка во вспомогательном приложении модуля CDN.</span><span class="sxs-lookup"><span data-stu-id="7af37-880">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7af37-881">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7af37-881">Az.Compute</span></span>
* <span data-ttu-id="7af37-882">Добавлен параметр VmssId в новый командлет Add New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="7af37-882">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="7af37-883">Добавлены параметры TerminateScheduledEvents и TerminateScheduledEventNotBeforeTimeoutInMinutes в New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="7af37-883">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="7af37-884">Добавлено свойство HyperVGeneration в объект образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7af37-884">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="7af37-885">Добавлены компоненты Host и HostGroup.</span><span class="sxs-lookup"><span data-stu-id="7af37-885">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="7af37-886">Новые командлеты:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="7af37-886">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="7af37-887">Параметр HostId добавлен в New-AzVMConfig и New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="7af37-887">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="7af37-888">Исправлен пример в документации по Invoke-AzVMRunCommand, в котором теперь используется правильное имя параметра.</span><span class="sxs-lookup"><span data-stu-id="7af37-888">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="7af37-889">Исправлено описание VolumeType в справочной документации по Set-AzVMDiskEncryptionExtension и Set-AzVmssDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="7af37-889">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7af37-890">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7af37-890">Az.DataFactory</span></span>
* <span data-ttu-id="7af37-891">Исправлена опечатка в написании Windows со строчной буквы в документации по New-AzDataFactoryEncryptValue.</span><span class="sxs-lookup"><span data-stu-id="7af37-891">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="7af37-892">Пакет SDK ADF для .NET обновлен до версии 4.1.2.</span><span class="sxs-lookup"><span data-stu-id="7af37-892">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="7af37-893">Добавлены параметры DataProxyIntegrationRuntimeName, DataProxyStagingLinkedServiceName и DataProxyStagingPath в командлет Set-AzureRmDataFactoryV2IntegrationRuntime, что позволяет настраивать локальную среду выполнения интеграции в качестве прокси-сервера для Azure-SSIS Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="7af37-893">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="7af37-894">Обновлены PSTriggerRun для отображения активированных конвейеров, сообщений и свойств и PSActivityRun для отображения типа действия.</span><span class="sxs-lookup"><span data-stu-id="7af37-894">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7af37-895">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7af37-895">Az.DataLakeStore</span></span>
* <span data-ttu-id="7af37-896">Устранена проблема, при которой Get-DataLakeStoreDeletedItem переставал отвечать на запросы при возникновении ошибок или удаленных исключений.</span><span class="sxs-lookup"><span data-stu-id="7af37-896">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7af37-897">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7af37-897">Az.EventHub</span></span>
* <span data-ttu-id="7af37-898">Исправлена проблема № 9658: опечатка в написании параметра VirtualNteworkRule у Set-AzEventHubNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="7af37-898">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="7af37-899">Исправлена проблема № 9558: в Set-AzEventHubNamespace используется PATCH вместо PUT.</span><span class="sxs-lookup"><span data-stu-id="7af37-899">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="7af37-900">В командлет Set-AzEventHubNamespace добавлен параметр EnableKafka.</span><span class="sxs-lookup"><span data-stu-id="7af37-900">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="7af37-901">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="7af37-901">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="7af37-902">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="7af37-902">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="7af37-903">Исправлено написание Azure со строчной буквы.</span><span class="sxs-lookup"><span data-stu-id="7af37-903">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7af37-904">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7af37-904">Az.Monitor</span></span>
* <span data-ttu-id="7af37-905">Исправлены неправильные имена параметров в справочной документации.</span><span class="sxs-lookup"><span data-stu-id="7af37-905">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7af37-906">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7af37-906">Az.Network</span></span>
* <span data-ttu-id="7af37-907">Обновлен New-AzPrivateLinkServiceIpConfig.</span><span class="sxs-lookup"><span data-stu-id="7af37-907">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="7af37-908">Параметр PublicIpAddress объявлен нерекомендуемым, так как он не используется на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="7af37-908">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="7af37-909">Добавлен необязательный параметр Primary, указывающий, является ли текущая IP-конфигурация основной.</span><span class="sxs-lookup"><span data-stu-id="7af37-909">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="7af37-910">Улучшена обработка исключений из-за ошибок запроса от пакета SDK. Устранена проблема, при которой исключения пакета SDK не обрабатывались правильно, из-за чего не отображались основные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="7af37-910">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="7af37-911">Настроена логика проверки для префикса IPv6 IP-адреса для проверки правильности длины префикса IPv6.</span><span class="sxs-lookup"><span data-stu-id="7af37-911">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="7af37-912">Обновлен Get-AzVirtualNetworkSubnetConfig: добавлен набор параметров для получения по идентификатору ресурса подсети.</span><span class="sxs-lookup"><span data-stu-id="7af37-912">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="7af37-913">Обновлено описание параметра Location для AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="7af37-913">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7af37-914">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7af37-914">Az.OperationalInsights</span></span>
* <span data-ttu-id="7af37-915">Обновлена документация по New-AzOperationalInsightsLinuxSyslogDataSource.</span><span class="sxs-lookup"><span data-stu-id="7af37-915">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="7af37-916">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="7af37-916">Added example</span></span>
    - <span data-ttu-id="7af37-917">Обновлено описание параметра -Name.</span><span class="sxs-lookup"><span data-stu-id="7af37-917">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="7af37-918">Добавлен пример для New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="7af37-918">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="7af37-919">Изменено описание параметра -Name для New-AzOperationalInsightsWindowsEventDataSource.</span><span class="sxs-lookup"><span data-stu-id="7af37-919">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7af37-920">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7af37-920">Az.RecoveryServices</span></span>
* <span data-ttu-id="7af37-921">Обновлен Get-AzRecoveryServicesBackupJobDetail.md.</span><span class="sxs-lookup"><span data-stu-id="7af37-921">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="7af37-922">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7af37-922">Az.Resources</span></span>
* <span data-ttu-id="7af37-923">Добавлена поддержка новой версии API 2019-05-10 для Microsoft.Resource.</span><span class="sxs-lookup"><span data-stu-id="7af37-923">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="7af37-924">Добавлена поддержка copy.count = 0 для переменных, ресурсов и свойств.</span><span class="sxs-lookup"><span data-stu-id="7af37-924">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="7af37-925">Ресурсы, у которых condition = false или copy.count = 0, будут удаляться в полном режиме.</span><span class="sxs-lookup"><span data-stu-id="7af37-925">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="7af37-926">В справочную документацию добавлен пример назначения политики на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="7af37-926">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7af37-927">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7af37-927">Az.ServiceBus</span></span>
* <span data-ttu-id="7af37-928">Исправлена проблема № 9658: опечатка в написании параметра VirtualNetworkRule В Set-AzServiceBusNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="7af37-928">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="7af37-929">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="7af37-929">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="7af37-930">Добавлена новая команда Test-AzServiceBusNameAvailability для проверки доступности имени для очереди и раздела.</span><span class="sxs-lookup"><span data-stu-id="7af37-930">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="7af37-931">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7af37-931">Az.ServiceFabric</span></span>
* <span data-ttu-id="7af37-932">Устранены ошибки командлета для добавления типа узла:</span><span class="sxs-lookup"><span data-stu-id="7af37-932">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="7af37-933">ошибка NullReferenceException, возникавшая, если у группы ресурсов были другие VMSS, не связанные с кластером Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="7af37-933">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="7af37-934">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8681.</span><span class="sxs-lookup"><span data-stu-id="7af37-934">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="7af37-935">Исправлена ошибка, из-за которой командлет завершился сбоем, если virtualNetwork находилась не в той группе ресурсов, к которой относится кластер.</span><span class="sxs-lookup"><span data-stu-id="7af37-935">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="7af37-936">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8407.</span><span class="sxs-lookup"><span data-stu-id="7af37-936">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="7af37-937">Командлет Add-AzServiceFabricApplicationCertificate объявлен нерекомендуемым.</span><span class="sxs-lookup"><span data-stu-id="7af37-937">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="7af37-938">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7af37-938">Az.Sql</span></span>
* <span data-ttu-id="7af37-939">Обновление документации по старым командлетам аудита.</span><span class="sxs-lookup"><span data-stu-id="7af37-939">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7af37-940">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7af37-940">Az.Storage</span></span>
* <span data-ttu-id="7af37-941">Обновлена справка по Get/Close-AzStorageFileHandle: в примеры добавлены сценарии использования командлетов и обновлено описание параметров.</span><span class="sxs-lookup"><span data-stu-id="7af37-941">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="7af37-942">Добавлена поддержка StandardBlobTier в операции отправки BLOB-объекта и копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="7af37-942">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="7af37-943">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7af37-943">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="7af37-944">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="7af37-944">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="7af37-945">Добавлена поддержка приоритета восстановления в операцию копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="7af37-945">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="7af37-946">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="7af37-946">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7af37-947">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7af37-947">Az.Websites</span></span>
* <span data-ttu-id="7af37-948">Добавлены уточнение для параметра -AppSettings в Set-AzWebApp и Set-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="7af37-948">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="7af37-949">2.5.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7af37-949">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7af37-950">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7af37-950">Az.Accounts</span></span>
* <span data-ttu-id="7af37-951">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="7af37-951">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="7af37-952">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="7af37-952">Az.ApplicationInsights</span></span>
* <span data-ttu-id="7af37-953">Исправлена опечатка в примере в документации по Remove-AzApplicationInsightsApiKey.</span><span class="sxs-lookup"><span data-stu-id="7af37-953">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="7af37-954">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7af37-954">Az.Automation</span></span>
* <span data-ttu-id="7af37-955">Исправлена опечатка в строке ресурса.</span><span class="sxs-lookup"><span data-stu-id="7af37-955">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="7af37-956">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7af37-956">Az.CognitiveServices</span></span>
* <span data-ttu-id="7af37-957">Добавлена поддержка NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="7af37-957">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7af37-958">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7af37-958">Az.Compute</span></span>
* <span data-ttu-id="7af37-959">Добавлены недостающие свойства (ComputerName, OsName, OsVersion и HyperVGeneration) для объекта представления экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7af37-959">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="7af37-960">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7af37-960">Az.ContainerRegistry</span></span>
* <span data-ttu-id="7af37-961">Исправлена опечатка в Remove-AzContainerRegistryReplication для параметра репликации.</span><span class="sxs-lookup"><span data-stu-id="7af37-961">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="7af37-962">См. подробнее: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="7af37-962">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7af37-963">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7af37-963">Az.DataFactory</span></span>
* <span data-ttu-id="7af37-964">Пакет SDK для ADF .NET обновлен до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="7af37-964">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="7af37-965">Исправлена опечатка в документации по Get-AzDataFactoryV2PipelineRun.</span><span class="sxs-lookup"><span data-stu-id="7af37-965">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7af37-966">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7af37-966">Az.EventHub</span></span>
* <span data-ttu-id="7af37-967">Добавлен новый командлет для создания маркера SAS: New-AzEventHubAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="7af37-967">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="7af37-968">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="7af37-968">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7af37-969">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7af37-969">Az.KeyVault</span></span>
* <span data-ttu-id="7af37-970">Добавлена поддержка для настройки параметра KeySize в политиках сертификатов.</span><span class="sxs-lookup"><span data-stu-id="7af37-970">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7af37-971">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7af37-971">Az.LogicApp</span></span>
* <span data-ttu-id="7af37-972">Get-AzIntegrationAccountMap теперь надлежащим образом выводит все типы сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="7af37-972">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="7af37-973">Добавлен новый параметр MapType для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="7af37-973">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="7af37-974">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="7af37-974">Az.ManagedServices</span></span>
* <span data-ttu-id="7af37-975">Добавлена поддержка API версии 2019-06-01 (общедоступная).</span><span class="sxs-lookup"><span data-stu-id="7af37-975">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7af37-976">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7af37-976">Az.Network</span></span>
* <span data-ttu-id="7af37-977">Добавлена поддержка частной конечной точки и службы приватного канала.</span><span class="sxs-lookup"><span data-stu-id="7af37-977">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="7af37-978">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="7af37-978">New cmdlets</span></span>
        - <span data-ttu-id="7af37-979">Set-AzPrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="7af37-979">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="7af37-980">Set-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="7af37-980">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="7af37-981">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="7af37-981">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7af37-982">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="7af37-982">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7af37-983">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="7af37-983">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7af37-984">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="7af37-984">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7af37-985">Test-AzPrivateLinkServiceVisibility.</span><span class="sxs-lookup"><span data-stu-id="7af37-985">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="7af37-986">Get-AzAutoApprovedPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="7af37-986">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="7af37-987">Обновлены следующие команды для функции: Флаг PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies в подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="7af37-987">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="7af37-988">Обновлены командлеты New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig.</span><span class="sxs-lookup"><span data-stu-id="7af37-988">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="7af37-989">Добавлен необязательный параметр -PrivateEndpointNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к частной конечной точке в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="7af37-989">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="7af37-990">Добавлен необязательный параметр -PrivateLinkServiceNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к службе приватного канала в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="7af37-990">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="7af37-991">Параметр ServiceName командлета AzPrivateLinkService был переименован на Name с псевдонимом ServiceName для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="7af37-991">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="7af37-992">Включен протокол ICMP для настройки правил безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="7af37-992">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="7af37-993">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="7af37-993">Updated cmdlets</span></span>
        - <span data-ttu-id="7af37-994">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="7af37-994">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="7af37-995">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="7af37-995">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="7af37-996">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="7af37-996">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="7af37-997">Добавлен ConnectionProtocolType (Ikev1/Ikev2) в качестве настраиваемого параметра для командлета New-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="7af37-997">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="7af37-998">Добавлен PrivateIpAddressVersion в LoadBalancerFrontendIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7af37-998">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="7af37-999">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="7af37-999">Updated cmdlet:</span></span>
        - <span data-ttu-id="7af37-1000">New-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="7af37-1000">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="7af37-1001">Add-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="7af37-1001">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="7af37-1002">Set-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="7af37-1002">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="7af37-1003">Команда New-AzApplicationGatewayProbeConfig Шлюза приложений обновлена для поддержки настраиваемого порта в зонде.</span><span class="sxs-lookup"><span data-stu-id="7af37-1003">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="7af37-1004">Обновлен командлет New-AzApplicationGatewayProbeConfig: добавлен необязательный параметр Port, который используется при проверке внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="7af37-1004">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="7af37-1005">Этот параметр применяется к номерам SKU Standard_V2 и WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="7af37-1005">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7af37-1006">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7af37-1006">Az.OperationalInsights</span></span>
* <span data-ttu-id="7af37-1007">Обновленная версия по умолчанию для сохраненных операций поиска имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="7af37-1007">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="7af37-1008">Исправлены ошибки при обработке регулярных выражений со значениями NULL в журналах.</span><span class="sxs-lookup"><span data-stu-id="7af37-1008">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7af37-1009">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7af37-1009">Az.RecoveryServices</span></span>
* <span data-ttu-id="7af37-1010">Обновлен файл Get-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="7af37-1010">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="7af37-1011">Обновлен файл Get-AzRecoveryServicesBackupContainer.md.</span><span class="sxs-lookup"><span data-stu-id="7af37-1011">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="7af37-1012">Обновлен файл Get-AzRecoveryServicesVault.md.</span><span class="sxs-lookup"><span data-stu-id="7af37-1012">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="7af37-1013">Обновлен файл Wait-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="7af37-1013">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="7af37-1014">Обновлен файл Set-AzRecoveryServicesVaultContext.md.</span><span class="sxs-lookup"><span data-stu-id="7af37-1014">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="7af37-1015">Обновлен файл Get-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="7af37-1015">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="7af37-1016">Обновлен файл Get-AzRecoveryServicesBackupRecoveryPoint.md.</span><span class="sxs-lookup"><span data-stu-id="7af37-1016">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="7af37-1017">Обновлен файл Restore-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="7af37-1017">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="7af37-1018">Обновлен вызов службы для отмены регистрации контейнера в общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="7af37-1018">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="7af37-1019">Обновлен файл Set-AzRecoveryServicesAsrAlertSetting.md.</span><span class="sxs-lookup"><span data-stu-id="7af37-1019">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="7af37-1020">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7af37-1020">Az.Resources</span></span>
- <span data-ttu-id="7af37-1021">Удален отсутствующий командлет, который упоминается в документации по New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="7af37-1021">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="7af37-1022">Обновлены командлеты политик для использования новой версии API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="7af37-1022">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7af37-1023">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7af37-1023">Az.ServiceBus</span></span>
* <span data-ttu-id="7af37-1024">Добавлен новый командлет для создания маркера SAS: New-AzServiceBusAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="7af37-1024">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="7af37-1025">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="7af37-1025">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="7af37-1026">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7af37-1026">Az.Sql</span></span>
* <span data-ttu-id="7af37-1027">Исправлены отсутствующие примеры для командлета Set-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="7af37-1027">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="7af37-1028">Исправлены заданные повторяющиеся проверки для оценки наличия уязвимостей без указания адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="7af37-1028">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="7af37-1029">Исправлена незначительная опечатка в сообщении предупреждения.</span><span class="sxs-lookup"><span data-stu-id="7af37-1029">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7af37-1030">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7af37-1030">Az.Storage</span></span>
* <span data-ttu-id="7af37-1031">Обновлен пример в справочной документации для использования командлетом Get-AzStorageAccount правильного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="7af37-1031">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="7af37-1032">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="7af37-1032">Az.StorageSync</span></span>
* <span data-ttu-id="7af37-1033">Добавлен командлет Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="7af37-1033">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="7af37-1034">Исправлена проблема № 9551, связанная с TierFilesOlderThanDays.</span><span class="sxs-lookup"><span data-stu-id="7af37-1034">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7af37-1035">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7af37-1035">Az.Websites</span></span>
* <span data-ttu-id="7af37-1036">Исправлена ошибка, при которой некоторые свойства SiteConfig не возвращались Get-AzWebApp и Set-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="7af37-1036">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="7af37-1037">Добавлен новый параметр Location в Get-AzDeletedWebApp и Restore-AzDeletedWebApp.</span><span class="sxs-lookup"><span data-stu-id="7af37-1037">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="7af37-1038">Исправлена ошибка, которая возникала при клонировании слотов веб-приложений с помощью командлета New-AzWebApp-IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="7af37-1038">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="7af37-1039">2.4.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7af37-1039">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7af37-1040">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7af37-1040">Az.Accounts</span></span>
* <span data-ttu-id="7af37-1041">Добавлена поддержка командлетов профиля.</span><span class="sxs-lookup"><span data-stu-id="7af37-1041">Add support for profile cmdlets</span></span>
* <span data-ttu-id="7af37-1042">Добавлена поддержка сред и плоскостей данных в созданных командлетах.</span><span class="sxs-lookup"><span data-stu-id="7af37-1042">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="7af37-1043">Исправлена ошибка, когда в командлетах плоскости данных в Windows PowerShell в некоторых случаях использовалась неправильная конечная точка.</span><span class="sxs-lookup"><span data-stu-id="7af37-1043">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="7af37-1044">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="7af37-1044">Az.Advisor</span></span>
* <span data-ttu-id="7af37-1045">Выпущена общедоступная версия Az.Advisor.</span><span class="sxs-lookup"><span data-stu-id="7af37-1045">GA release of Az.Advisor</span></span>
* <span data-ttu-id="7af37-1046">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="7af37-1046">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7af37-1047">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7af37-1047">Az.ApiManagement</span></span>
* <span data-ttu-id="7af37-1048">исправлена проблема https://github.com/Azure/azure-powershell/issues/8671.</span><span class="sxs-lookup"><span data-stu-id="7af37-1048">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="7af37-1049">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="7af37-1049">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="7af37-1050">Добавлена поддержка запрашивания подписок по пользователю и продукту.</span><span class="sxs-lookup"><span data-stu-id="7af37-1050">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="7af37-1051">Добавлена поддержка создания запросов с использованием области "/", "/apis", "/apis/echo-api".</span><span class="sxs-lookup"><span data-stu-id="7af37-1051">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="7af37-1052">Исправлены проблемы https://github.com/Azure/azure-powershell/issues/9307 и https://github.com/Azure/azure-powershell/issues/8432.</span><span class="sxs-lookup"><span data-stu-id="7af37-1052">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="7af37-1053">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="7af37-1053">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="7af37-1054">Добавлена поддержка указания ApiVersion и ApiVersionSetId при импорте API-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="7af37-1054">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7af37-1055">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7af37-1055">Az.Automation</span></span>
* <span data-ttu-id="7af37-1056">Исправлена ошибка командлета Set-AzAutomationConnectionFieldValue при обработке строкового значения.</span><span class="sxs-lookup"><span data-stu-id="7af37-1056">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7af37-1057">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7af37-1057">Az.Compute</span></span>
* <span data-ttu-id="7af37-1058">В New AzImageConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="7af37-1058">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7af37-1059">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7af37-1059">Az.DataFactory</span></span>
* <span data-ttu-id="7af37-1060">Обновление выходных данных командлетов ADF, предназначенных для получения числа выполнений действий, конвейеров и триггеров, для поддержки канала Select-Object.</span><span class="sxs-lookup"><span data-stu-id="7af37-1060">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7af37-1061">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7af37-1061">Az.EventGrid</span></span>
* <span data-ttu-id="7af37-1062">Исправлена опечатка в документации по командлету New-AzEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="7af37-1062">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7af37-1063">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7af37-1063">Az.IotHub</span></span>
* <span data-ttu-id="7af37-1064">Добавлена поддержка повторного создания ключей политики авторизации.</span><span class="sxs-lookup"><span data-stu-id="7af37-1064">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7af37-1065">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7af37-1065">Az.Network</span></span>
* <span data-ttu-id="7af37-1066">К тегам общедоступного IP-адреса добавлен тег RoutingPreference.</span><span class="sxs-lookup"><span data-stu-id="7af37-1066">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="7af37-1067">Улучшены примеры для справочной документации по командлету Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="7af37-1067">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7af37-1068">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7af37-1068">Az.PolicyInsights</span></span>
* <span data-ttu-id="7af37-1069">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="7af37-1069">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="7af37-1070">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9446.</span><span class="sxs-lookup"><span data-stu-id="7af37-1070">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7af37-1071">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7af37-1071">Az.OperationalInsights</span></span>
* <span data-ttu-id="7af37-1072">Исправленная модель источника данных CustomLog возвращена в командлет Get-AzOperationalInsightsDataSource.</span><span class="sxs-lookup"><span data-stu-id="7af37-1072">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7af37-1073">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7af37-1073">Az.RecoveryServices</span></span>
* <span data-ttu-id="7af37-1074">Выпущено исправление для команды get-policy для виртуальных машин IaaS.</span><span class="sxs-lookup"><span data-stu-id="7af37-1074">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="7af37-1075">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7af37-1075">Az.Resources</span></span>
    - <span data-ttu-id="7af37-1076">Исправлен текст справки по параметру Get-AzPolicyState -Top.</span><span class="sxs-lookup"><span data-stu-id="7af37-1076">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="7af37-1077">Добавлена поддержка разбиения по страницам на стороне клиента для Get-AzPolicyAlias.</span><span class="sxs-lookup"><span data-stu-id="7af37-1077">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="7af37-1078">Добавлены новые параметры для Set-AzPolicyAssignment, -PolicyParameters и -PolicyParametersObject.</span><span class="sxs-lookup"><span data-stu-id="7af37-1078">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="7af37-1079">Добавлен ряд обновлений документов и примеров для командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="7af37-1079">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7af37-1080">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7af37-1080">Az.ServiceBus</span></span>
* <span data-ttu-id="7af37-1081">Исправление ошибки № 4938: командлет New-AzureRmServiceBusQueue возвращает ответ BadRequest (Недопустимый запрос) при задании значения MaxSizeInMegabytes.</span><span class="sxs-lookup"><span data-stu-id="7af37-1081">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="7af37-1082">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7af37-1082">Az.Sql</span></span>
* <span data-ttu-id="7af37-1083">Из выпуска предварительной версии в выпуск общедоступной версии добавлены командлеты группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7af37-1083">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="7af37-1084">Поддержка аудита Azure SQL Server и баз данных с помощью новых командлетов:</span><span class="sxs-lookup"><span data-stu-id="7af37-1084">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="7af37-1085">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="7af37-1085">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="7af37-1086">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="7af37-1086">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="7af37-1087">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="7af37-1087">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="7af37-1088">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="7af37-1088">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="7af37-1089">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="7af37-1089">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="7af37-1090">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="7af37-1090">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="7af37-1091">Из параметров оценки уязвимостей удалены ограничения, касающиеся электронной почты.</span><span class="sxs-lookup"><span data-stu-id="7af37-1091">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7af37-1092">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7af37-1092">Az.Storage</span></span>
* <span data-ttu-id="7af37-1093">Два параметра в указанном ниже командлете — -IndexDocument и -ErrorDocument404Path, — которые ранее были обязательными, стали необязательными:</span><span class="sxs-lookup"><span data-stu-id="7af37-1093">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="7af37-1094">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="7af37-1094">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="7af37-1095">Обновлена справка по командлету Get-AzStorageBlobContent: добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="7af37-1095">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="7af37-1096">При сбое выполнения командлета с ошибкой StorageException отображаются дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="7af37-1096">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="7af37-1097">Добавлена поддержка создания или обновления учетной записи хранения с использованием проверки подлинности AAD DS для службы "Файлы Azure".</span><span class="sxs-lookup"><span data-stu-id="7af37-1097">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="7af37-1098">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7af37-1098">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="7af37-1099">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7af37-1099">Set-AzStorageAccount</span></span>
* <span data-ttu-id="7af37-1100">Добавлена поддержка перечисления или закрытия дескрипторов файлов для общей папки, каталога файлов или файла:</span><span class="sxs-lookup"><span data-stu-id="7af37-1100">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="7af37-1101">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="7af37-1101">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="7af37-1102">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="7af37-1102">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="7af37-1103">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="7af37-1103">Az.StorageSync</span></span>
* <span data-ttu-id="7af37-1104">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="7af37-1104">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="7af37-1105">2.3.2 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7af37-1105">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7af37-1106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7af37-1106">Az.Accounts</span></span>
* <span data-ttu-id="7af37-1107">Исправлена ошибка, связанная с использованием неправильного URL-адреса для вызовов функций.</span><span class="sxs-lookup"><span data-stu-id="7af37-1107">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="7af37-1108">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8983.</span><span class="sxs-lookup"><span data-stu-id="7af37-1108">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="7af37-1109">Устранена проблема с псевдонимами из AzureRM для командлетов Az.</span><span class="sxs-lookup"><span data-stu-id="7af37-1109">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="7af37-1110">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="7af37-1110">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="7af37-1111">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest.</span><span class="sxs-lookup"><span data-stu-id="7af37-1111">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7af37-1112">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7af37-1112">Az.Compute</span></span>
* <span data-ttu-id="7af37-1113">Простые наборы параметров New-AzVm и New-AzVmss теперь принимают параметр ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="7af37-1113">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="7af37-1114">Исправлена опечатка в справочной документации по New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="7af37-1114">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="7af37-1115">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="7af37-1115">Az.Dns</span></span>
* <span data-ttu-id="7af37-1116">Исправлена опечатка в справочных примерах по использованию Set-AzDnsZone.</span><span class="sxs-lookup"><span data-stu-id="7af37-1116">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7af37-1117">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7af37-1117">Az.EventGrid</span></span>
* <span data-ttu-id="7af37-1118">Обновлен для использования API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="7af37-1118">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="7af37-1119">Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="7af37-1119">New cmdlets:</span></span>
    - <span data-ttu-id="7af37-1120">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="7af37-1120">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="7af37-1121">Создает домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="7af37-1121">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="7af37-1122">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="7af37-1122">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="7af37-1123">Возвращает сведения о домене Сетки событий или список всех доменов Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="7af37-1123">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="7af37-1124">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="7af37-1124">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="7af37-1125">Удаляет домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="7af37-1125">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="7af37-1126">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="7af37-1126">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="7af37-1127">Повторно создает ключ общего доступа для домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="7af37-1127">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="7af37-1128">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="7af37-1128">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="7af37-1129">Возвращает ключи общего доступа, используемые для публикации событий в домене Сетки событий.</span><span class="sxs-lookup"><span data-stu-id="7af37-1129">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="7af37-1130">New-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="7af37-1130">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="7af37-1131">Создает раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="7af37-1131">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="7af37-1132">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="7af37-1132">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="7af37-1133">Возвращает сведения о разделе домена Сетки событий или список всех разделов определенного домена Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="7af37-1133">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="7af37-1134">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="7af37-1134">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="7af37-1135">Удаляет раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="7af37-1135">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="7af37-1136">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="7af37-1136">Updated cmdlets:</span></span>
    - <span data-ttu-id="7af37-1137">New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="7af37-1137">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="7af37-1138">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для нового домена Сетки событий и раздела домена Сетки событий и позволяющие создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="7af37-1138">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="7af37-1139">Добавляют новые обязательные параметры для указания имени нового домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="7af37-1139">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="7af37-1140">Добавляют новые наборы параметров для доменов и разделов домена и позволяют повторно использовать существующие параметры (например, EndPointType, SubjectBeginsWith и т. д.).</span><span class="sxs-lookup"><span data-stu-id="7af37-1140">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="7af37-1141">Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="7af37-1141">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="7af37-1142">срока действия подписки на событие;</span><span class="sxs-lookup"><span data-stu-id="7af37-1142">Event subscription expiration date,</span></span>
            - <span data-ttu-id="7af37-1143">параметров расширенной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="7af37-1143">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="7af37-1144">Добавляют новое перечисление для ServiceBusQueue в качестве места назначения.</span><span class="sxs-lookup"><span data-stu-id="7af37-1144">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="7af37-1145">Запрещают использование значение All в параметре -IncludedEventType и заменяют его следующим:</span><span class="sxs-lookup"><span data-stu-id="7af37-1145">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="7af37-1146">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="7af37-1146">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="7af37-1147">Добавляют новые необязательные параметры (Top, ODataQuery и NextLink) для поддержки разбиения на страницы и фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="7af37-1147">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="7af37-1148">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="7af37-1148">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="7af37-1149">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для домена Сетки событий и раздела домена Сетки событий и позволяющие удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="7af37-1149">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="7af37-1150">Добавляют новые обязательные параметры для указания имени домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="7af37-1150">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7af37-1151">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7af37-1151">Az.FrontDoor</span></span>
* <span data-ttu-id="7af37-1152">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="7af37-1152">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="7af37-1153">Добавляет поддержку преобразований и новое значение оператора автозавершения (RegEx).</span><span class="sxs-lookup"><span data-stu-id="7af37-1153">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="7af37-1154">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="7af37-1154">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="7af37-1155">Добавляет новые значения автозавершения.</span><span class="sxs-lookup"><span data-stu-id="7af37-1155">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7af37-1156">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7af37-1156">Az.Network</span></span>
* <span data-ttu-id="7af37-1157">Добавляет поддержку ресурса шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="7af37-1157">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="7af37-1158">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="7af37-1158">New cmdlets</span></span>
        - <span data-ttu-id="7af37-1159">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="7af37-1159">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="7af37-1160">Добавляет AvailablePrivateEndpointType.</span><span class="sxs-lookup"><span data-stu-id="7af37-1160">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="7af37-1161">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="7af37-1161">New cmdlets</span></span> 
        - <span data-ttu-id="7af37-1162">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="7af37-1162">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="7af37-1163">Добавляет PrivatePrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="7af37-1163">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="7af37-1164">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="7af37-1164">New cmdlets</span></span> 
        - <span data-ttu-id="7af37-1165">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7af37-1165">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="7af37-1166">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7af37-1166">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="7af37-1167">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7af37-1167">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="7af37-1168">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7af37-1168">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="7af37-1169">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7af37-1169">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="7af37-1170">Добавляет PrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="7af37-1170">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="7af37-1171">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="7af37-1171">New cmdlets</span></span>
        - <span data-ttu-id="7af37-1172">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7af37-1172">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="7af37-1173">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7af37-1173">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="7af37-1174">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7af37-1174">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="7af37-1175">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="7af37-1175">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="7af37-1176">Обновлены следующие команды для функции: флаг UseLocalAzureIpAddress для VPN-подключения.</span><span class="sxs-lookup"><span data-stu-id="7af37-1176">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="7af37-1177">Обновлен командлет New-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="7af37-1177">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="7af37-1178">Обновлен командлет Set-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="7af37-1178">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="7af37-1179">В пиринг ExpressRoute добавлено поле только для чтения PeeredConnections.</span><span class="sxs-lookup"><span data-stu-id="7af37-1179">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="7af37-1180">В ExpressRoute добавлено поле только для чтения GlobalReachEnabled.</span><span class="sxs-lookup"><span data-stu-id="7af37-1180">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="7af37-1181">Добавлен атрибут в рамках критического изменения, отменяющего статус устаревшего поля AllowGlobalReach в модели ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="7af37-1181">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="7af37-1182">Исправлена проблема, связанная с ошибкой 8756, при использовании TargetListenerID с командлетами AzApplicationGatewayRedirectConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7af37-1182">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="7af37-1183">Исправлена ошибка в New-AzApplicationGatewayPathRuleConfig, не позволявшая задавать набор правил повторного создания.</span><span class="sxs-lookup"><span data-stu-id="7af37-1183">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="7af37-1184">Исправлено отображение VirtualNetworkTaps в NetworkInterfaceIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7af37-1184">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="7af37-1185">Исправлены командлеты Cortex Get для отображения всех частей.</span><span class="sxs-lookup"><span data-stu-id="7af37-1185">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="7af37-1186">Исправлено создание ссылок VirtualHub для ExpressRouteGateways и VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="7af37-1186">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="7af37-1187">В AzureFirewall и NatGateway добавлена поддержка Зон доступности.</span><span class="sxs-lookup"><span data-stu-id="7af37-1187">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="7af37-1188">Добавлен командлет Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="7af37-1188">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="7af37-1189">Добавлена поддержка нескольких общедоступных IP-адресов для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="7af37-1189">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="7af37-1190">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="7af37-1190">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="7af37-1191">Добавлен параметр -PublicIpAddress, который принимает один или несколько объектов общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="7af37-1191">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="7af37-1192">Добавлен параметр -VirtualNetwork, который принимает объект виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="7af37-1192">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="7af37-1193">Добавлены методы AddPublicIpAddress и RemovePublicIpAddress для объекта брандмауэра. Они принимают объект общедоступного IP-адреса в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="7af37-1193">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="7af37-1194">Не рекомендуется использовать параметры -PublicIpName и -VirtualNetworkName.</span><span class="sxs-lookup"><span data-stu-id="7af37-1194">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="7af37-1195">Обновлены следующие команды для функции: В параметрах проверки подлинности AAD VPN-клиента задан ресурс шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="7af37-1195">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="7af37-1196">Обновлен командлет New-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="7af37-1196">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="7af37-1197">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="7af37-1197">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="7af37-1198">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр-переключатель RemoveAadAuthentication для удаления в шлюзе параметров проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="7af37-1198">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7af37-1199">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7af37-1199">Az.OperationalInsights</span></span>
* <span data-ttu-id="7af37-1200">Добавлена поддержка SKU **pergb2018** в команде New-AzureRmOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="7af37-1200">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="7af37-1201">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7af37-1201">Az.Resources</span></span>
* <span data-ttu-id="7af37-1202">Поддержка дополнительных вариантов экспорта шаблона.</span><span class="sxs-lookup"><span data-stu-id="7af37-1202">Support for additional Template Export options</span></span>
    - <span data-ttu-id="7af37-1203">В Export-AzResourceGroup добавлен параметр -SkipResourceNameParameterization.</span><span class="sxs-lookup"><span data-stu-id="7af37-1203">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="7af37-1204">В Export-AzResourceGroup добавлен параметр -SkipAllParameterization.</span><span class="sxs-lookup"><span data-stu-id="7af37-1204">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="7af37-1205">В Export-AzResourceGroup добавлен параметр -Resource для фильтрации экспортированных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7af37-1205">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7af37-1206">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7af37-1206">Az.ServiceFabric</span></span>
* <span data-ttu-id="7af37-1207">Исправлена ошибка, связанная с получением иногда неправильных отпечатков при добавлении сертификата ByExistingKeyVault.</span><span class="sxs-lookup"><span data-stu-id="7af37-1207">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="7af37-1208">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7af37-1208">Az.Sql</span></span>
* <span data-ttu-id="7af37-1209">Исправлен суффикс конечной точки хранилища службы "Расширенная защита от угроз Azure".</span><span class="sxs-lookup"><span data-stu-id="7af37-1209">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="7af37-1210">Исправлена ошибка, связанная с возможностью пакета "Расширенная защита данных" переопределять политику службы "Расширенная защита от угроз".</span><span class="sxs-lookup"><span data-stu-id="7af37-1210">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="7af37-1211">Новые командлеты для Management.Sql позволяют клиентам добавлять ключи TDE и задавать средство защиты TDE для управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="7af37-1211">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="7af37-1212">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7af37-1212">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="7af37-1213">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7af37-1213">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="7af37-1214">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7af37-1214">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="7af37-1215">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="7af37-1215">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="7af37-1216">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="7af37-1216">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7af37-1217">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7af37-1217">Az.Storage</span></span>
* <span data-ttu-id="7af37-1218">Поддержка класса Kind в FileStorage и значения Premium_ZRS в SkuName при создании учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="7af37-1218">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="7af37-1219">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7af37-1219">New-AzStorageAccount</span></span>
* <span data-ttu-id="7af37-1220">Уточнено описание командлета неизменности BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="7af37-1220">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="7af37-1221">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="7af37-1221">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7af37-1222">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7af37-1222">Az.Websites</span></span>
* <span data-ttu-id="7af37-1223">Оптимизирует Get-AzWebAppCertificate для фильтрации по группе ресурсов на сервере, а не в клиенте.</span><span class="sxs-lookup"><span data-stu-id="7af37-1223">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="7af37-1224">Добавляет параметр-переключатель - UseDisasterRecovery в Get AzWebAppSnapshot.</span><span class="sxs-lookup"><span data-stu-id="7af37-1224">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="7af37-1225">2.2.0 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7af37-1225">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="7af37-1226">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7af37-1226">Az.Cdn</span></span>
* <span data-ttu-id="7af37-1227">Обновлены командлеты для поддержки функции rulesEngine на основе API версии 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="7af37-1227">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7af37-1228">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7af37-1228">Az.Compute</span></span>
* <span data-ttu-id="7af37-1229">Добавлен параметр `NoWait`, который запускает операцию и немедленно возвращает значение еще до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="7af37-1229">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="7af37-1230">Обновлены командлеты:   Export-AzLogAnalyticRequestRateByInterval; Export-AzLogAnalyticThrottledRequest; Remove-AzVM; Remove-AzVMAccessExtension; Remove-AzVMAEMExtension; Remove-AzVMChefExtension; Remove-AzVMCustomScriptExtension; Remove-AzVMDiagnosticsExtension; Remove-AzVMDiskEncryptionExtension; Remove-AzVMDscExtension; Remove-AzVMSqlServerExtension; Restart-AzVM; Set-AzVM; Set-AzVMAccessExtension; Set-AzVMADDomainExtension; Set-AzVMAEMExtension; Set-AzVMBginfoExtension; Set-AzVMChefExtension; Set-AzVMCustomScriptExtension; Set-AzVMDiagnosticsExtension; Set-AzVMDscExtension; Set-AzVMExtension; Start-AzVM; Stop-AzVM; Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="7af37-1230">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7af37-1231">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7af37-1231">Az.EventHub</span></span>
* <span data-ttu-id="7af37-1232">Исправлена ошибка № 9231. Командлет Get-AzEventHubNamespace не возвращал теги.</span><span class="sxs-lookup"><span data-stu-id="7af37-1232">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="7af37-1233">Исправлена ошибка № 9230. Командлет Get-AzEventHubNamespace возвращал значение ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="7af37-1233">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7af37-1234">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7af37-1234">Az.Network</span></span>
* <span data-ttu-id="7af37-1235">Обновлены параметры ResourceId и InputObject для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="7af37-1235">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="7af37-1236">Добавлены псевдонимы для параметров ResourceId и InputObject.</span><span class="sxs-lookup"><span data-stu-id="7af37-1236">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7af37-1237">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7af37-1237">Az.PolicyInsights</span></span>
* <span data-ttu-id="7af37-1238">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyEvent.</span><span class="sxs-lookup"><span data-stu-id="7af37-1238">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7af37-1239">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7af37-1239">Az.RecoveryServices</span></span>
* <span data-ttu-id="7af37-1240">Минимальный срок хранения политики IaaSVM изменился с 1 до 7 дней.</span><span class="sxs-lookup"><span data-stu-id="7af37-1240">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7af37-1241">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7af37-1241">Az.ServiceBus</span></span>
* <span data-ttu-id="7af37-1242">Исправлена ошибка № 9182. Командлет Get-AzServiceBusNamespace возвращал ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="7af37-1242">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7af37-1243">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7af37-1243">Az.ServiceFabric</span></span>
* <span data-ttu-id="7af37-1244">Исправлена опечатка в сообщении об ошибке для командлета Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="7af37-1244">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="7af37-1245">Добавлен отсутствующий символ в командных строках Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="7af37-1245">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="7af37-1246">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7af37-1246">Az.Sql</span></span>
* <span data-ttu-id="7af37-1247">Для командлета New-AzureSqlInstance добавлен параметр DnsZonePartner, обеспечивающий поддержку AutoDr для Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7af37-1247">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="7af37-1248">Командлет Get-AzSqlDatabaseSecureConnectionPolicy объявлен неподдерживаемым.</span><span class="sxs-lookup"><span data-stu-id="7af37-1248">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="7af37-1249">Командлеты обнаружения угроз переименованы в командлеты Расширенной защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="7af37-1249">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="7af37-1250">Параметры -StorageSizeInGB и -LicenseType командлета New-AzSqlInstance теперь необязательны.</span><span class="sxs-lookup"><span data-stu-id="7af37-1250">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7af37-1251">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7af37-1251">Az.Websites</span></span>
* <span data-ttu-id="7af37-1252">Исправлены проблемы, когда удалялись теги при использовании Set-AzWebApp и Set-AzWebAppSlot со свойством -WebApp.</span><span class="sxs-lookup"><span data-stu-id="7af37-1252">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="7af37-1253">2.1.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7af37-1253">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="7af37-1254">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7af37-1254">Az.ApiManagement</span></span>
* <span data-ttu-id="7af37-1255">Созданы командлеты для управления диагностикой в глобальной области и в области API.</span><span class="sxs-lookup"><span data-stu-id="7af37-1255">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="7af37-1256">**Get-AzApiManagementDiagnostic** — получение диагностики, заданной глобально или на уровне области API.</span><span class="sxs-lookup"><span data-stu-id="7af37-1256">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="7af37-1257">**New-AzApiManagementDiagnostic** — создание диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="7af37-1257">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="7af37-1258">**New-AzApiManagementHttpMessageDiagnostic** — создание параметра диагностики, для которого регистрируются заголовки и размер байтов тела.</span><span class="sxs-lookup"><span data-stu-id="7af37-1258">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="7af37-1259">**New-AzApiManagementPipelineDiagnosticSetting** — создание параметров диагностики для сообщений HTTP, поступающих в шлюз или исходящих из него.</span><span class="sxs-lookup"><span data-stu-id="7af37-1259">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="7af37-1260">**New-AzApiManagementSamplingSetting** — создание параметра выборки для запросов и ответов касательно диагностики.</span><span class="sxs-lookup"><span data-stu-id="7af37-1260">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="7af37-1261">**Remove-AzApiManagementDiagnostic** — удаление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="7af37-1261">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="7af37-1262">**Set-AzApiManagementDiagnostic** — обновление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="7af37-1262">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="7af37-1263">Созданы командлеты для управления кэшем в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="7af37-1263">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="7af37-1264">**Get-AzApiManagementCache** — получение сведений о кэше, указанном идентификатором, или обо всех кэшах.</span><span class="sxs-lookup"><span data-stu-id="7af37-1264">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="7af37-1265">**New-AzApiManagementCache** — создание кэша по умолчанию или кэша в определенном регионе Azure.</span><span class="sxs-lookup"><span data-stu-id="7af37-1265">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="7af37-1266">**Remove-AzApiManagementCache** — удаление кэша.</span><span class="sxs-lookup"><span data-stu-id="7af37-1266">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="7af37-1267">**Update-AzApiManagementCache** — обновление кэша.</span><span class="sxs-lookup"><span data-stu-id="7af37-1267">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="7af37-1268">Созданы командлеты для управления схемой API.</span><span class="sxs-lookup"><span data-stu-id="7af37-1268">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="7af37-1269">**New-AzApiManagementSchema** — создание схемы для API.</span><span class="sxs-lookup"><span data-stu-id="7af37-1269">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="7af37-1270">**Get-AzApiManagementSchema** — получение схем, настроенных в API.</span><span class="sxs-lookup"><span data-stu-id="7af37-1270">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="7af37-1271">**Remove-AzApiManagementSchema** — удаление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="7af37-1271">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="7af37-1272">**Set-AzApiManagementSchema** — обновление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="7af37-1272">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="7af37-1273">Создан командлет для создания токена пользователя.</span><span class="sxs-lookup"><span data-stu-id="7af37-1273">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="7af37-1274">**New-AzApiManagementUserToken** — создание токена пользователя, по умолчанию действительного в течение 8 часов. С помощью этого командлета можно создавать токен для пользователя GIT.</span><span class="sxs-lookup"><span data-stu-id="7af37-1274">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="7af37-1275">Создан командлет для получения состояния сети.</span><span class="sxs-lookup"><span data-stu-id="7af37-1275">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="7af37-1276">**Get-AzApiManagementNetworkStatus** — получение состояния подключения сети ресурсов, от которых зависит служба "Управление API".</span><span class="sxs-lookup"><span data-stu-id="7af37-1276">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="7af37-1277">Это полезно при развертывании службы ApiManagement в виртуальной сети и проверке того, не нарушена ли какая-либо из зависимостей.</span><span class="sxs-lookup"><span data-stu-id="7af37-1277">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="7af37-1278">Обновлен командлет **New-AzApiManagement** для управления службой ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="7af37-1278">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="7af37-1279">Добавлена поддержка нового SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="7af37-1279">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="7af37-1280">Добавлена поддержка для включения флага EnableClientCertificate в SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="7af37-1280">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="7af37-1281">Новый командлет **New-AzApiManagementSslSetting** позволяет настраивать параметр TLS/SSL для сервера (Backend) и внешнего интерфейса (Frontend).</span><span class="sxs-lookup"><span data-stu-id="7af37-1281">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="7af37-1282">Его также можно использовать для настройки Ciphers как 3DES, в ServerProtocols как Http2 для внешнего интерфейса (Frontend) службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="7af37-1282">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="7af37-1283">Добавлена поддержка настройки имени узла DeveloperPortal в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="7af37-1283">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="7af37-1284">Обновлен командлет **Get-AzApiManagementSsoToken** для извлечения объекта PsApiManagement в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="7af37-1284">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="7af37-1285">Обновлен командлет для отображения встроенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="7af37-1285">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="7af37-1286">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Код ошибки: ValidationError. Сообщение об ошибке: "Некоторые поля содержат неправильные значения". Сведения об ошибке: [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="7af37-1286">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="7af37-1287">Обновлен командлет **Export-AzApiManagementApi** для экспортирования программных интерфейсов в формате OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="7af37-1287">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="7af37-1288">Обновлен командлет **Import-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="7af37-1288">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="7af37-1289">Для импортирования API из спецификации документа OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="7af37-1289">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="7af37-1290">Для переопределения свойства PsApiManagementSchema, указанного в любом документе (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="7af37-1290">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="7af37-1291">Для переопределения свойства ServiceUrl, указанного в любом документе.</span><span class="sxs-lookup"><span data-stu-id="7af37-1291">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="7af37-1292">Обновлен командлет **Get-AzApiManagementPolicy** для возврата политики в формате, экранированном не для XML, с использованием rawxml.</span><span class="sxs-lookup"><span data-stu-id="7af37-1292">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="7af37-1293">Обновлен командлет **Set-AzApiManagementPolicy**. Он принимает политику в формате, экранированном не для XML, с использованием rawxml и в формате, экранированном для XML, с использованием XML.</span><span class="sxs-lookup"><span data-stu-id="7af37-1293">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="7af37-1294">Обновлен командлет **New-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="7af37-1294">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="7af37-1295">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="7af37-1295">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="7af37-1296">Для создания API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="7af37-1296">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="7af37-1297">Для клонирования API с использованием значений SourceApiId и SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="7af37-1297">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="7af37-1298">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="7af37-1298">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="7af37-1299">Обновлен командлет **Set-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="7af37-1299">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="7af37-1300">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="7af37-1300">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="7af37-1301">Для обновления API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="7af37-1301">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="7af37-1302">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="7af37-1302">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="7af37-1303">Обновлен командлет **New-AzApiManagementRevision**:</span><span class="sxs-lookup"><span data-stu-id="7af37-1303">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="7af37-1304">Для клонирования (копирования тегов, продуктов, операций и политик) существующей редакции с использованием SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="7af37-1304">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="7af37-1305">Новая редакция предполагает родительский идентификатор ApiId.</span><span class="sxs-lookup"><span data-stu-id="7af37-1305">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="7af37-1306">Для предоставления ApiRevisionDescription.</span><span class="sxs-lookup"><span data-stu-id="7af37-1306">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="7af37-1307">Для переопределения значения ServiceUrl при клонировании API.</span><span class="sxs-lookup"><span data-stu-id="7af37-1307">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="7af37-1308">Обновлен командлет **New-AzApiManagementIdentityProvider**:</span><span class="sxs-lookup"><span data-stu-id="7af37-1308">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="7af37-1309">Для настройки AAD или AADB2C с Authority.</span><span class="sxs-lookup"><span data-stu-id="7af37-1309">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="7af37-1310">Для установки политик SignupPolicy, SigninPolicy, ProfileEditingPolicy и PasswordResetPolicy.</span><span class="sxs-lookup"><span data-stu-id="7af37-1310">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="7af37-1311">Обновлен командлет **New-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="7af37-1311">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="7af37-1312">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="7af37-1312">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="7af37-1313">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="7af37-1313">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="7af37-1314">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="7af37-1314">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="7af37-1315">Обновлен командлет **Set-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="7af37-1315">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="7af37-1316">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="7af37-1316">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="7af37-1317">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="7af37-1317">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="7af37-1318">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="7af37-1318">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="7af37-1319">Следующие командлеты обновлены, чтобы принимать значение ResourceId в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="7af37-1319">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="7af37-1320">New-AzApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="7af37-1320">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="7af37-1321">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="7af37-1321">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="7af37-1322">Get-AzApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="7af37-1322">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="7af37-1323">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="7af37-1323">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="7af37-1324">Get-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="7af37-1324">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="7af37-1325">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="7af37-1325">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="7af37-1326">Get-AzApiManagementAuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="7af37-1326">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="7af37-1327">Get-AzApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="7af37-1327">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="7af37-1328">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="7af37-1328">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="7af37-1329">Get-AzApiManagementCertificate.</span><span class="sxs-lookup"><span data-stu-id="7af37-1329">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="7af37-1330">Remove-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="7af37-1330">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="7af37-1331">Remove-AzApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="7af37-1331">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7af37-1332">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7af37-1332">Az.Automation</span></span>
* <span data-ttu-id="7af37-1333">Обновлен командлет Get-AzAutomationJobOutputRecord для обработки значений в формате JSON и в виде текстовой записи.</span><span class="sxs-lookup"><span data-stu-id="7af37-1333">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="7af37-1334">исправлена проблема https://github.com/Azure/azure-powershell/issues/7977.</span><span class="sxs-lookup"><span data-stu-id="7af37-1334">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="7af37-1335">исправлена проблема https://github.com/Azure/azure-powershell/issues/8600.</span><span class="sxs-lookup"><span data-stu-id="7af37-1335">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="7af37-1336">Поведение командлета Start-AzAutomationDscCompilationJob изменено так, чтобы сразу же запустить задание, а не ждать его завершения.</span><span class="sxs-lookup"><span data-stu-id="7af37-1336">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="7af37-1337">исправлена проблема https://github.com/Azure/azure-powershell/issues/8347.</span><span class="sxs-lookup"><span data-stu-id="7af37-1337">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="7af37-1338">Исправлен командлет Get-AzAutomationDscNode, возвращающий все узлы при использовании -Name.</span><span class="sxs-lookup"><span data-stu-id="7af37-1338">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="7af37-1339">Теперь он возвращает только соответствующий узел.</span><span class="sxs-lookup"><span data-stu-id="7af37-1339">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7af37-1340">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7af37-1340">Az.Compute</span></span>
* <span data-ttu-id="7af37-1341">Добавлены параметры ProtectFromScaleIn и ProtectFromScaleSetAction для командлета Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="7af37-1341">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="7af37-1342">Командлет New-AzVM с простым набором параметров теперь по умолчанию использует доступное расположение, если регион "восточная часть США" не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7af37-1342">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7af37-1343">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7af37-1343">Az.DataLakeStore</span></span>
* <span data-ttu-id="7af37-1344">Обновлен пакет SDK ADLS для использования httpclient. В инфраструктуру Azure интегрирована проверка плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="7af37-1344">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7af37-1345">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7af37-1345">Az.Monitor</span></span>
* <span data-ttu-id="7af37-1346">Исправлены неправильные имена параметров в справочных примерах.</span><span class="sxs-lookup"><span data-stu-id="7af37-1346">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7af37-1347">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7af37-1347">Az.Network</span></span>
* <span data-ttu-id="7af37-1348">Добавлен флаг DisableBgpRoutePropagation для выходных данных действующей таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="7af37-1348">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="7af37-1349">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="7af37-1349">Updated cmdlet:</span></span>
        - <span data-ttu-id="7af37-1350">Get-AzEffectiveRouteTable.</span><span class="sxs-lookup"><span data-stu-id="7af37-1350">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="7af37-1351">Исправлен двойной дефис в документации New-AzApplicationGatewayTrustedRootCertificate.</span><span class="sxs-lookup"><span data-stu-id="7af37-1351">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="7af37-1352">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7af37-1352">Az.Resources</span></span>
* <span data-ttu-id="7af37-1353">Добавлен новый командлет Get-AzureRmDenyAssignment для получения запрещающих назначений.</span><span class="sxs-lookup"><span data-stu-id="7af37-1353">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="7af37-1354">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7af37-1354">Az.Sql</span></span>
* <span data-ttu-id="7af37-1355">Командлеты Расширенной защиты от угроз переименованы на командлеты Расширенной защиты данных, и оценка уязвимости включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7af37-1355">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="7af37-1356">2.0.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7af37-1356">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7af37-1357">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7af37-1357">Az.Accounts</span></span>
* <span data-ttu-id="7af37-1358">Обновлена библиотека аутентификации для устранения проблем с ADFS при использовании аутентификации на основе имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="7af37-1358">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7af37-1359">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7af37-1359">Az.CognitiveServices</span></span>
* <span data-ttu-id="7af37-1360">Отображается только заявление об отказе Bing для служб Поиска Bing.</span><span class="sxs-lookup"><span data-stu-id="7af37-1360">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="7af37-1361">Исправлена проблема с созданием учетной записи.</span><span class="sxs-lookup"><span data-stu-id="7af37-1361">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7af37-1362">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7af37-1362">Az.Compute</span></span>
* <span data-ttu-id="7af37-1363">Функция группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="7af37-1363">Proximity placement group feature.</span></span>
    - <span data-ttu-id="7af37-1364">Добавлены следующие новые командлеты:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="7af37-1364">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="7af37-1365">Новый параметр ProximityPlacementGroupId будет добавлен в следующие командлеты:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="7af37-1365">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="7af37-1366">В командлет New-AzGalleryImageVersion добавлен параметр StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="7af37-1366">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="7af37-1367">TargetRegion в командлете New-AzGalleryImageVersion может содержать StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="7af37-1367">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="7af37-1368">Параметр-переключатель SkipShutdown добавлен в командлеты Stop-AzVM и Stop-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="7af37-1368">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="7af37-1369">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="7af37-1369">Breaking changes</span></span>
    - <span data-ttu-id="7af37-1370">Командлет SET-AzVMBootDiagnostics изменен на Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="7af37-1370">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="7af37-1371">Командлет Export-AzLogAnalyticThrottledRequests изменен на Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="7af37-1371">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="7af37-1372">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="7af37-1372">Az.DeploymentManager</span></span>
* <span data-ttu-id="7af37-1373">Первая общедоступная версия командлетов диспетчера развертывания Azure</span><span class="sxs-lookup"><span data-stu-id="7af37-1373">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="7af37-1374">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="7af37-1374">Az.Dns</span></span>
* <span data-ttu-id="7af37-1375">Автоматическое делегирование DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="7af37-1375">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="7af37-1376">Командлет для создания зоны DNS принимает имя родительской зоны в качестве дополнительного необязательного параметра.</span><span class="sxs-lookup"><span data-stu-id="7af37-1376">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="7af37-1377">Он добавляет записи NS в родительской зоне для созданной дочерней зоны.</span><span class="sxs-lookup"><span data-stu-id="7af37-1377">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7af37-1378">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7af37-1378">Az.FrontDoor</span></span>
* <span data-ttu-id="7af37-1379">Первая общедоступная версия командлетов Azure FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="7af37-1379">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="7af37-1380">Переименованы командлеты WAF для включения Waf.</span><span class="sxs-lookup"><span data-stu-id="7af37-1380">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="7af37-1381">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7af37-1381">Az.HDInsight</span></span>
* <span data-ttu-id="7af37-1382">Удалены два командлета:</span><span class="sxs-lookup"><span data-stu-id="7af37-1382">Removed two cmdlets:</span></span>
    - <span data-ttu-id="7af37-1383">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7af37-1383">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="7af37-1384">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7af37-1384">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="7af37-1385">Добавлен новый командлет Set-AzHDInsightGatewayCredential для замены Grant-AzHDInsightHttpServicesAccess.</span><span class="sxs-lookup"><span data-stu-id="7af37-1385">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="7af37-1386">Обновлен командлет Get-AzHDInsightJobOutput для различения ролей читателя и оператора HDInsight:</span><span class="sxs-lookup"><span data-stu-id="7af37-1386">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="7af37-1387">Пользователям с ролью читателя не нужно указывать параметр DefaultStorageAccountKey явным образом, иначе возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="7af37-1387">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="7af37-1388">На пользователей с ролью оператора HDInsight это не повлияет.</span><span class="sxs-lookup"><span data-stu-id="7af37-1388">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7af37-1389">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7af37-1389">Az.Monitor</span></span>
* <span data-ttu-id="7af37-1390">Новые командлеты для API SQR (запланированное правило запросов)</span><span class="sxs-lookup"><span data-stu-id="7af37-1390">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="7af37-1391">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="7af37-1391">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="7af37-1392">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="7af37-1392">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="7af37-1393">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="7af37-1393">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="7af37-1394">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="7af37-1394">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="7af37-1395">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="7af37-1395">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="7af37-1396">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="7af37-1396">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="7af37-1397">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7af37-1397">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7af37-1398">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7af37-1398">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7af37-1399">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7af37-1399">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7af37-1400">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7af37-1400">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7af37-1401">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7af37-1401">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7af37-1402">См. подробнее об [API SQR](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules).</span><span class="sxs-lookup"><span data-stu-id="7af37-1402">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="7af37-1403">Обновлен файл Az.Monitor.md для включения командлетов для правила генерации оповещений на основе метрик GenV2(не классическая версия).</span><span class="sxs-lookup"><span data-stu-id="7af37-1403">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7af37-1404">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7af37-1404">Az.Network</span></span>
* <span data-ttu-id="7af37-1405">Добавлена поддержка для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="7af37-1405">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="7af37-1406">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="7af37-1406">New cmdlets</span></span>
        - <span data-ttu-id="7af37-1407">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7af37-1407">New-AzNatGateway</span></span>
        - <span data-ttu-id="7af37-1408">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7af37-1408">Get-AzNatGateway</span></span>
        - <span data-ttu-id="7af37-1409">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7af37-1409">Set-AzNatGateway</span></span>
        - <span data-ttu-id="7af37-1410">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7af37-1410">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="7af37-1411">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="7af37-1411">Updated cmdlets</span></span>
        - <span data-ttu-id="7af37-1412">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="7af37-1412">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="7af37-1413">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="7af37-1413">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="7af37-1414">Обновлены следующие команды для функции: Настройка и удаление пользовательских маршрутов через шлюз в Бруклине.</span><span class="sxs-lookup"><span data-stu-id="7af37-1414">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="7af37-1415">Обновлен командлет New-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="7af37-1415">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="7af37-1416">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="7af37-1416">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7af37-1417">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7af37-1417">Az.PolicyInsights</span></span>
* <span data-ttu-id="7af37-1418">Добавлена поддержка сведений об оценке политики запросов.</span><span class="sxs-lookup"><span data-stu-id="7af37-1418">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="7af37-1419">Добавлен параметр -Expand в командлет Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="7af37-1419">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="7af37-1420">Добавлена поддержка -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="7af37-1420">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7af37-1421">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7af37-1421">Az.RecoveryServices</span></span>
* <span data-ttu-id="7af37-1422">Добавлена поддержка перекрестной подписки на Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="7af37-1422">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="7af37-1423">Добавлена возможность отмечать предстоящие критически важные изменения для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="7af37-1423">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="7af37-1424">Исправлены план восстановления и план действий для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="7af37-1424">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="7af37-1425">Исправлено сетевое сопоставление обновления Azure Site Recovery (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="7af37-1425">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="7af37-1426">Исправлено направление защиты обновления Azure Site Recovery для управляемых дисков (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="7af37-1426">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="7af37-1427">Добавлены другие незначительные исправления.</span><span class="sxs-lookup"><span data-stu-id="7af37-1427">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="7af37-1428">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="7af37-1428">Az.Relay</span></span>
* <span data-ttu-id="7af37-1429">Исправлены опечатки в сообщениях для клиентов.</span><span class="sxs-lookup"><span data-stu-id="7af37-1429">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7af37-1430">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7af37-1430">Az.ServiceBus</span></span>
* <span data-ttu-id="7af37-1431">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="7af37-1431">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7af37-1432">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7af37-1432">Az.Storage</span></span>
* <span data-ttu-id="7af37-1433">Выполнено обновление клиентской библиотеки хранилища до версии 10.0.1 (пространство имен всех объектов из этого пакета SDK изменено с Microsoft.WindowsAzure.Storage. *на Microsoft.Azure.Storage*).</span><span class="sxs-lookup"><span data-stu-id="7af37-1433">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="7af37-1434">Выполнено обновление до Microsoft.Azure.Management.Storage версии 11.0.0 для включения поддержки нового API версии 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="7af37-1434">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="7af37-1435">Значение свойства Kind по умолчанию в учетной записи хранения изменено со Storage на StorageV2.</span><span class="sxs-lookup"><span data-stu-id="7af37-1435">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="7af37-1436">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7af37-1436">New-AzStorageAccount</span></span>
* <span data-ttu-id="7af37-1437">Изменено значение Sku.Name в выходных данных командлета учетной записи хранения в соответствии со значением Sku.Name во входных данных путем добавления _ (например, StandardLRS изменено на Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="7af37-1437">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="7af37-1438">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7af37-1438">New-AzStorageAccount</span></span>
    - <span data-ttu-id="7af37-1439">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7af37-1439">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="7af37-1440">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7af37-1440">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7af37-1441">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7af37-1441">Az.Websites</span></span>
* <span data-ttu-id="7af37-1442">Свойство Kind теперь будет задаваться объектам PSSite, возвращаемым командлетом Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="7af37-1442">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="7af37-1443">Get-AzWebApp\*Metrics и Get-AzAppServicePlanMetrics считаются нерекомендуемыми.</span><span class="sxs-lookup"><span data-stu-id="7af37-1443">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="7af37-1444">1.8.0 — апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7af37-1444">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7af37-1445">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="7af37-1445">Highlights since the last major release</span></span>
* <span data-ttu-id="7af37-1446">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="7af37-1446">General availability of `Az` module</span></span>
* <span data-ttu-id="7af37-1447">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="7af37-1447">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="7af37-1448">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="7af37-1448">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="7af37-1449">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="7af37-1449">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="7af37-1450">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="7af37-1450">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7af37-1451">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="7af37-1451">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="7af37-1452">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="7af37-1452">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7af37-1453">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7af37-1453">Az.Accounts</span></span>
* <span data-ttu-id="7af37-1454">Обновлен командлет Uninstall-AzureRm для правильного удаления модулей в Mac.</span><span class="sxs-lookup"><span data-stu-id="7af37-1454">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7af37-1455">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7af37-1455">Az.Batch</span></span>
* <span data-ttu-id="7af37-1456">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7af37-1456">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7af37-1457">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7af37-1457">Az.Cdn</span></span>
* <span data-ttu-id="7af37-1458">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7af37-1458">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7af37-1459">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7af37-1459">Az.CognitiveServices</span></span>
* <span data-ttu-id="7af37-1460">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7af37-1460">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7af37-1461">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7af37-1461">Az.Compute</span></span>
* <span data-ttu-id="7af37-1462">Устранена проблема с установкой AEM, если в идентификаторах ресурсов дисков группа ресурсов указана в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="7af37-1462">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="7af37-1463">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7af37-1463">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7af37-1464">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="7af37-1464">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7af37-1465">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7af37-1465">Az.DataFactory</span></span>
* <span data-ttu-id="7af37-1466">Добавлены свойства SsisProperties, если NodeCount не имеет значения NULL для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="7af37-1466">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7af37-1467">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7af37-1467">Az.DataLakeStore</span></span>
* <span data-ttu-id="7af37-1468">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7af37-1468">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7af37-1469">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7af37-1469">Az.EventGrid</span></span>
* <span data-ttu-id="7af37-1470">Обновлен текст справки для конечной точки, указывающий, что необходимо создать ресурсы, прежде чем использовать командлеты для создания или обновления подписки на события.</span><span class="sxs-lookup"><span data-stu-id="7af37-1470">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7af37-1471">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7af37-1471">Az.EventHub</span></span>
* <span data-ttu-id="7af37-1472">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="7af37-1472">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="7af37-1473">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7af37-1473">Az.HDInsight</span></span>
* <span data-ttu-id="7af37-1474">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7af37-1474">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7af37-1475">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7af37-1475">Az.IotHub</span></span>
* <span data-ttu-id="7af37-1476">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7af37-1476">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7af37-1477">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7af37-1477">Az.KeyVault</span></span>
* <span data-ttu-id="7af37-1478">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7af37-1478">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7af37-1479">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="7af37-1479">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="7af37-1480">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="7af37-1480">Az.MachineLearning</span></span>
* <span data-ttu-id="7af37-1481">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7af37-1481">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="7af37-1482">Az.Media</span><span class="sxs-lookup"><span data-stu-id="7af37-1482">Az.Media</span></span>
* <span data-ttu-id="7af37-1483">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7af37-1483">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7af37-1484">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7af37-1484">Az.Monitor</span></span>
  * <span data-ttu-id="7af37-1485">Добавлены новые командлеты для правила генерации оповещений на основе метрик GenV2 (не классических).</span><span class="sxs-lookup"><span data-stu-id="7af37-1485">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="7af37-1486">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="7af37-1486">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="7af37-1487">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="7af37-1487">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="7af37-1488">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7af37-1488">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="7af37-1489">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7af37-1489">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="7af37-1490">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7af37-1490">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="7af37-1491">Обновлен пакет SDK Monitor до предварительной версии 0.22.0.</span><span class="sxs-lookup"><span data-stu-id="7af37-1491">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7af37-1492">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7af37-1492">Az.Network</span></span>
* <span data-ttu-id="7af37-1493">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7af37-1493">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7af37-1494">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="7af37-1494">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="7af37-1495">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="7af37-1495">Az.NotificationHubs</span></span>
* <span data-ttu-id="7af37-1496">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7af37-1496">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7af37-1497">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7af37-1497">Az.OperationalInsights</span></span>
* <span data-ttu-id="7af37-1498">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7af37-1498">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="7af37-1499">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="7af37-1499">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="7af37-1500">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7af37-1500">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7af37-1501">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7af37-1501">Az.RecoveryServices</span></span>
* <span data-ttu-id="7af37-1502">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7af37-1502">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7af37-1503">Обновлен табличный формат для SQL на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="7af37-1503">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="7af37-1504">Добавлен альтернативный метод для получения расположения в Общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="7af37-1504">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="7af37-1505">Обновлено значение ScheduleRunDays в объекте SchedulePolicy в соответствии с часовым поясом.</span><span class="sxs-lookup"><span data-stu-id="7af37-1505">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7af37-1506">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7af37-1506">Az.RedisCache</span></span>
* <span data-ttu-id="7af37-1507">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7af37-1507">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7af37-1508">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7af37-1508">Az.Resources</span></span>
* <span data-ttu-id="7af37-1509">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="7af37-1509">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="7af37-1510">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7af37-1510">Az.Sql</span></span>
* <span data-ttu-id="7af37-1511">Заменена зависимость от пакета SDK монитора на обычный код.</span><span class="sxs-lookup"><span data-stu-id="7af37-1511">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="7af37-1512">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7af37-1512">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7af37-1513">Улучшен процесс классификации нескольких столбцов.</span><span class="sxs-lookup"><span data-stu-id="7af37-1513">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="7af37-1514">Добавлены свойства SKU (имя, семейство, производительность SKU) в отклике Get-AzSqlServerServiceObjective, а также по умолчанию задан табличный формат.</span><span class="sxs-lookup"><span data-stu-id="7af37-1514">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="7af37-1515">C помощью Get-AzSqlServerServiceObjective теперь можно получать список доступных целевых служб по расположению без необходимости заранее размещать сервер в регионе.</span><span class="sxs-lookup"><span data-stu-id="7af37-1515">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="7af37-1516">Поддерживается параметр часового пояса при создании Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7af37-1516">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="7af37-1517">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="7af37-1517">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7af37-1518">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7af37-1518">Az.Websites</span></span>
* <span data-ttu-id="7af37-1519">Исправлены командлеты Set-AzWebApp и Set-AzWebAppSlot, которые теперь не удаляют теги при выполнении.</span><span class="sxs-lookup"><span data-stu-id="7af37-1519">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="7af37-1520">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7af37-1520">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7af37-1521">Обновлен пакет SDK веб-узлов.</span><span class="sxs-lookup"><span data-stu-id="7af37-1521">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="7af37-1522">Удалено свойство AdminSiteName из PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="7af37-1522">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="7af37-1523">1.7.0 —апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7af37-1523">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7af37-1524">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="7af37-1524">Highlights since the last major release</span></span>
* <span data-ttu-id="7af37-1525">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="7af37-1525">General availability of `Az` module</span></span>
* <span data-ttu-id="7af37-1526">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="7af37-1526">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="7af37-1527">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="7af37-1527">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="7af37-1528">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="7af37-1528">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="7af37-1529">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="7af37-1529">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7af37-1530">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="7af37-1530">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="7af37-1531">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="7af37-1531">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7af37-1532">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7af37-1532">Az.Accounts</span></span>
* <span data-ttu-id="7af37-1533">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметр AzureAnalysisServicesEndpointResourceId.</span><span class="sxs-lookup"><span data-stu-id="7af37-1533">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7af37-1534">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7af37-1534">Az.AnalysisServices</span></span>
* <span data-ttu-id="7af37-1535">Использование ServiceClient в командлетах плоскости данных и удаление исходной логики проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="7af37-1535">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="7af37-1536">Add-AzureASAccount используется как оболочка для Connect-AzAccount во избежание критических изменений.</span><span class="sxs-lookup"><span data-stu-id="7af37-1536">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7af37-1537">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7af37-1537">Az.Automation</span></span>
* <span data-ttu-id="7af37-1538">Исправлена ошибка командлета New-AzAutomationSoftwareUpdateConfiguration, связанная с включением.</span><span class="sxs-lookup"><span data-stu-id="7af37-1538">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="7af37-1539">Теперь параметры IncludedKbNumber и IncludedPackageNameMask должны работать нормально.</span><span class="sxs-lookup"><span data-stu-id="7af37-1539">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="7af37-1540">Исправлена ошибка динамической группы управления обновлениями службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="7af37-1540">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7af37-1541">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7af37-1541">Az.Compute</span></span>
* <span data-ttu-id="7af37-1542">В командлеты New-AzDiskConfig и New-AzSnapshotConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="7af37-1542">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="7af37-1543">Теперь можно создавать виртуальные машину на основе образов из коллекции от других клиентов.</span><span class="sxs-lookup"><span data-stu-id="7af37-1543">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="7af37-1544">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7af37-1544">Az.ContainerInstance</span></span>
* <span data-ttu-id="7af37-1545">Исправлена проблема в параметре -Command командлета New-AzContainerGroup, из-за которой в конце добавлялся пустой аргумент.</span><span class="sxs-lookup"><span data-stu-id="7af37-1545">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7af37-1546">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7af37-1546">Az.DataFactory</span></span>
* <span data-ttu-id="7af37-1547">Пакет SDK для ADF .NET обновлен до версии 3.0.2.</span><span class="sxs-lookup"><span data-stu-id="7af37-1547">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="7af37-1548">Командлет Set-AzDataFactoryV2 обновлен с помощью дополнительных параметров для настроек, связанных с RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7af37-1548">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7af37-1549">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7af37-1549">Az.Resources</span></span>
* <span data-ttu-id="7af37-1550">Улучшена обработка поставщиков Get-AzResource при предоставлении параметров -ResourceId или -ResourceGroupName, -Name и -ResourceType.</span><span class="sxs-lookup"><span data-stu-id="7af37-1550">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="7af37-1551">Улучшена обработка ошибок в командлетах Test-AzDeployment и Test-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="7af37-1551">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="7af37-1552">Теперь ошибки, возникающие за пределами проверки развертывания, обрабатываются и включаются в выходные данные команды.</span><span class="sxs-lookup"><span data-stu-id="7af37-1552">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="7af37-1553">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="7af37-1553">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="7af37-1554">Добавлен параметр-переключатель -IgnoreDynamicParameters, с помощью которого можно настроить командлеты развертывания так, чтобы они пропускали запросы в сценариях скриптов и заданий.</span><span class="sxs-lookup"><span data-stu-id="7af37-1554">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="7af37-1555">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="7af37-1555">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="7af37-1556">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7af37-1556">Az.Sql</span></span>
* <span data-ttu-id="7af37-1557">Поддержка классификации данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="7af37-1557">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7af37-1558">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7af37-1558">Az.Storage</span></span>
* <span data-ttu-id="7af37-1559">Подробные сообщения об ошибке передаются при создании контекста хранилища с помощью параметра -UseConnectedAccount, но без входа в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="7af37-1559">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="7af37-1560">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="7af37-1560">New-AzStorageContext</span></span>
* <span data-ttu-id="7af37-1561">Поддержка свойств службы управления BLOB-объектов в указанной учетной записи хранения с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="7af37-1561">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="7af37-1562">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="7af37-1562">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="7af37-1563">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="7af37-1563">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="7af37-1564">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7af37-1564">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="7af37-1565">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7af37-1565">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="7af37-1566">Поддержка параметра -AsJob в командлетах для отправки и скачивания больших двоичных объектов и файлов.</span><span class="sxs-lookup"><span data-stu-id="7af37-1566">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="7af37-1567">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7af37-1567">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="7af37-1568">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7af37-1568">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="7af37-1569">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7af37-1569">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="7af37-1570">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7af37-1570">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="7af37-1571">1.6.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7af37-1571">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7af37-1572">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="7af37-1572">Highlights since the last major release</span></span>
* <span data-ttu-id="7af37-1573">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="7af37-1573">General availability of `Az` module</span></span>
* <span data-ttu-id="7af37-1574">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="7af37-1574">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="7af37-1575">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="7af37-1575">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="7af37-1576">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="7af37-1576">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="7af37-1577">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="7af37-1577">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7af37-1578">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="7af37-1578">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="7af37-1579">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="7af37-1579">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7af37-1580">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7af37-1580">Az.Automation</span></span>
* <span data-ttu-id="7af37-1581">В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:</span><span class="sxs-lookup"><span data-stu-id="7af37-1581">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="7af37-1582">динамическое группирование;</span><span class="sxs-lookup"><span data-stu-id="7af37-1582">Dynamic grouping</span></span>
    * <span data-ttu-id="7af37-1583">скрипты предварительного или последующего выполнения;</span><span class="sxs-lookup"><span data-stu-id="7af37-1583">Pre-Post script</span></span>
    * <span data-ttu-id="7af37-1584">параметр перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="7af37-1584">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7af37-1585">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7af37-1585">Az.Compute</span></span>
* <span data-ttu-id="7af37-1586">Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.</span><span class="sxs-lookup"><span data-stu-id="7af37-1586">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="7af37-1587">Обновление клиентской библиотеки вычислений до версии 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="7af37-1587">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7af37-1588">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7af37-1588">Az.KeyVault</span></span>
* <span data-ttu-id="7af37-1589">Добавлена поддержка подстановочных знаков в командлетах KeyVault.</span><span class="sxs-lookup"><span data-stu-id="7af37-1589">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7af37-1590">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7af37-1590">Az.Network</span></span>
* <span data-ttu-id="7af37-1591">Добавлена поддержка анализа угроз для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="7af37-1591">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="7af37-1592">Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="7af37-1592">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7af37-1593">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7af37-1593">Az.RecoveryServices</span></span>
* <span data-ttu-id="7af37-1594">В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.</span><span class="sxs-lookup"><span data-stu-id="7af37-1594">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="7af37-1595">Добавлена поддержка канала для отмены регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="7af37-1595">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="7af37-1596">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7af37-1596">Az.Resources</span></span>
* <span data-ttu-id="7af37-1597">Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7af37-1597">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="7af37-1598">Обновлены учетные данные, используемые при общих вызовах к ARM.</span><span class="sxs-lookup"><span data-stu-id="7af37-1598">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="7af37-1599">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7af37-1599">Az.Sql</span></span>
* <span data-ttu-id="7af37-1600">Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="7af37-1600">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7af37-1601">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7af37-1601">Az.Storage</span></span>
* <span data-ttu-id="7af37-1602">Поддержка получения, настройки и удаления политики управления в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="7af37-1602">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="7af37-1603">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7af37-1603">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="7af37-1604">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7af37-1604">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="7af37-1605">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7af37-1605">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="7af37-1606">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="7af37-1606">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="7af37-1607">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="7af37-1607">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="7af37-1608">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="7af37-1608">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7af37-1609">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7af37-1609">Az.Websites</span></span>
* <span data-ttu-id="7af37-1610">Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="7af37-1610">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="7af37-1611">1.5.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7af37-1611">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7af37-1612">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7af37-1612">Az.Accounts</span></span>
* <span data-ttu-id="7af37-1613">Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.</span><span class="sxs-lookup"><span data-stu-id="7af37-1613">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="7af37-1614">Обновлены примеры для Connect AzAccount.</span><span class="sxs-lookup"><span data-stu-id="7af37-1614">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7af37-1615">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7af37-1615">Az.Automation</span></span>
* <span data-ttu-id="7af37-1616">Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="7af37-1616">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="7af37-1617">Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов.</span><span class="sxs-lookup"><span data-stu-id="7af37-1617">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="7af37-1618">Теперь он возвращает все узлы.</span><span class="sxs-lookup"><span data-stu-id="7af37-1618">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7af37-1619">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7af37-1619">Az.Cdn</span></span>
* <span data-ttu-id="7af37-1620">Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.</span><span class="sxs-lookup"><span data-stu-id="7af37-1620">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7af37-1621">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7af37-1621">Az.Compute</span></span>
* <span data-ttu-id="7af37-1622">Добавлена поддержка подстановочных знаков в командлетах Get.</span><span class="sxs-lookup"><span data-stu-id="7af37-1622">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7af37-1623">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7af37-1623">Az.DataFactory</span></span>
* <span data-ttu-id="7af37-1624">Обновлен пакет SDK для ADF .NET до версии 3.0.1.</span><span class="sxs-lookup"><span data-stu-id="7af37-1624">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7af37-1625">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7af37-1625">Az.LogicApp</span></span>
* <span data-ttu-id="7af37-1626">Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.</span><span class="sxs-lookup"><span data-stu-id="7af37-1626">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7af37-1627">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7af37-1627">Az.Network</span></span>
* <span data-ttu-id="7af37-1628">Добавлена поддержка подстановочных знаков в командлетах Network.</span><span class="sxs-lookup"><span data-stu-id="7af37-1628">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7af37-1629">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7af37-1629">Az.RecoveryServices</span></span>
* <span data-ttu-id="7af37-1630">Добавлена поддержка SQL Server на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="7af37-1630">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="7af37-1631">Обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="7af37-1631">SDK Update</span></span>
* <span data-ttu-id="7af37-1632">Удалена проверка VMappContainer в Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="7af37-1632">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="7af37-1633">Добавлены параметры Name и ServerName для Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="7af37-1633">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="7af37-1634">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7af37-1634">Az.Resources</span></span>
* <span data-ttu-id="7af37-1635">Добавлен параметр `-TemplateObject` в командлеты для развертывания.</span><span class="sxs-lookup"><span data-stu-id="7af37-1635">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="7af37-1636">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.</span><span class="sxs-lookup"><span data-stu-id="7af37-1636">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="7af37-1637">Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="7af37-1637">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="7af37-1638">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.</span><span class="sxs-lookup"><span data-stu-id="7af37-1638">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="7af37-1639">Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="7af37-1639">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="7af37-1640">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.</span><span class="sxs-lookup"><span data-stu-id="7af37-1640">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="7af37-1641">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7af37-1641">Az.Sql</span></span>
* <span data-ttu-id="7af37-1642">Обновление AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="7af37-1642">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="7af37-1643">Исправлено поведение для пограничного случая при создании параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="7af37-1643">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7af37-1644">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7af37-1644">Az.Storage</span></span>
* <span data-ttu-id="7af37-1645">Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="7af37-1645">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="7af37-1646">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7af37-1646">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="7af37-1647">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7af37-1647">Az.AnalysisServices</span></span>
* <span data-ttu-id="7af37-1648">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="7af37-1648">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7af37-1649">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7af37-1649">Az.Automation</span></span>
* <span data-ttu-id="7af37-1650">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7af37-1650">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="7af37-1651">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7af37-1651">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="7af37-1652">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7af37-1652">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7af37-1653">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7af37-1653">Az.CognitiveServices</span></span>
* <span data-ttu-id="7af37-1654">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="7af37-1654">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7af37-1655">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7af37-1655">Az.Compute</span></span>
* <span data-ttu-id="7af37-1656">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="7af37-1656">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="7af37-1657">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="7af37-1657">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="7af37-1658">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="7af37-1658">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="7af37-1659">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7af37-1659">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7af37-1660">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7af37-1660">Az.DataLakeStore</span></span>
* <span data-ttu-id="7af37-1661">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="7af37-1661">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7af37-1662">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7af37-1662">Az.EventHub</span></span>
* <span data-ttu-id="7af37-1663">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="7af37-1663">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="7af37-1664">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7af37-1664">Az.KeyVault</span></span>
* <span data-ttu-id="7af37-1665">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="7af37-1665">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7af37-1666">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7af37-1666">Az.LogicApp</span></span>
* <span data-ttu-id="7af37-1667">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="7af37-1667">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="7af37-1668">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="7af37-1668">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="7af37-1669">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="7af37-1669">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="7af37-1670">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="7af37-1670">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="7af37-1671">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="7af37-1671">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="7af37-1672">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="7af37-1672">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="7af37-1673">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="7af37-1673">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="7af37-1674">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="7af37-1674">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="7af37-1675">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="7af37-1675">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="7af37-1676">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="7af37-1676">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="7af37-1677">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="7af37-1677">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="7af37-1678">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7af37-1678">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="7af37-1679">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="7af37-1679">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7af37-1680">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7af37-1680">Az.Monitor</span></span>
* <span data-ttu-id="7af37-1681">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="7af37-1681">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7af37-1682">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7af37-1682">Az.Network</span></span>
* <span data-ttu-id="7af37-1683">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="7af37-1683">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7af37-1684">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7af37-1684">Az.OperationalInsights</span></span>
* <span data-ttu-id="7af37-1685">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="7af37-1685">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="7af37-1686">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="7af37-1686">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="7af37-1687">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="7af37-1687">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="7af37-1688">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7af37-1688">Az.Resources</span></span>
* <span data-ttu-id="7af37-1689">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="7af37-1689">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="7af37-1690">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="7af37-1690">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="7af37-1691">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="7af37-1691">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="7af37-1692">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="7af37-1692">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="7af37-1693">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7af37-1693">Az.Sql</span></span>
* <span data-ttu-id="7af37-1694">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="7af37-1694">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="7af37-1695">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="7af37-1695">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7af37-1696">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7af37-1696">Az.Websites</span></span>
* <span data-ttu-id="7af37-1697">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="7af37-1697">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="7af37-1698">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7af37-1698">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7af37-1699">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7af37-1699">Az.Accounts</span></span>
* <span data-ttu-id="7af37-1700">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="7af37-1700">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7af37-1701">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7af37-1701">Az.AnalysisServices</span></span>
<span data-ttu-id="7af37-1702">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="7af37-1702">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7af37-1703">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7af37-1703">Az.Compute</span></span>
* <span data-ttu-id="7af37-1704">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="7af37-1704">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="7af37-1705">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="7af37-1705">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="7af37-1706">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="7af37-1706">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7af37-1707">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7af37-1707">Az.RecoveryServices</span></span>
<span data-ttu-id="7af37-1708">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="7af37-1708">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7af37-1709">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7af37-1709">Az.Resources</span></span>
* <span data-ttu-id="7af37-1710">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7af37-1710">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="7af37-1711">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="7af37-1711">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="7af37-1712">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="7af37-1712">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="7af37-1713">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="7af37-1713">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="7af37-1714">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7af37-1714">Az.Sql</span></span>
* <span data-ttu-id="7af37-1715">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="7af37-1715">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="7af37-1716">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="7af37-1716">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="7af37-1717">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="7af37-1717">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="7af37-1718">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7af37-1718">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7af37-1719">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7af37-1719">Az.Accounts</span></span>
* <span data-ttu-id="7af37-1720">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="7af37-1720">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7af37-1721">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7af37-1721">Az.AnalysisServices</span></span>
* <span data-ttu-id="7af37-1722">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="7af37-1722">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7af37-1723">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7af37-1723">Az.RecoveryServices</span></span>
* <span data-ttu-id="7af37-1724">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="7af37-1724">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="7af37-1725">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7af37-1725">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7af37-1726">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7af37-1726">Az.Accounts</span></span>
* <span data-ttu-id="7af37-1727">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="7af37-1727">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7af37-1728">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="7af37-1728">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7af37-1729">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="7af37-1729">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="7af37-1730">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="7af37-1730">Az.Aks</span></span>
* <span data-ttu-id="7af37-1731">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="7af37-1731">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7af37-1732">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7af37-1732">Az.Automation</span></span>
* <span data-ttu-id="7af37-1733">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="7af37-1733">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="7af37-1734">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="7af37-1734">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7af37-1735">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7af37-1735">Az.Cdn</span></span>
* <span data-ttu-id="7af37-1736">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="7af37-1736">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7af37-1737">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7af37-1737">Az.Compute</span></span>
* <span data-ttu-id="7af37-1738">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="7af37-1738">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="7af37-1739">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="7af37-1739">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="7af37-1740">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="7af37-1740">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="7af37-1741">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7af37-1741">Az.ContainerRegistry</span></span>
* <span data-ttu-id="7af37-1742">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="7af37-1742">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7af37-1743">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7af37-1743">Az.DataFactory</span></span>
* <span data-ttu-id="7af37-1744">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="7af37-1744">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7af37-1745">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7af37-1745">Az.DataLakeStore</span></span>
* <span data-ttu-id="7af37-1746">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="7af37-1746">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="7af37-1747">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="7af37-1747">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="7af37-1748">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="7af37-1748">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7af37-1749">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7af37-1749">Az.IotHub</span></span>
* <span data-ttu-id="7af37-1750">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="7af37-1750">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7af37-1751">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7af37-1751">Az.KeyVault</span></span>
* <span data-ttu-id="7af37-1752">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="7af37-1752">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7af37-1753">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7af37-1753">Az.Network</span></span>
* <span data-ttu-id="7af37-1754">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="7af37-1754">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="7af37-1755">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7af37-1755">Az.Resources</span></span>
* <span data-ttu-id="7af37-1756">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="7af37-1756">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="7af37-1757">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7af37-1757">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="7af37-1758">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="7af37-1758">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="7af37-1759">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="7af37-1759">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="7af37-1760">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="7af37-1760">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="7af37-1761">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="7af37-1761">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="7af37-1762">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="7af37-1762">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7af37-1763">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7af37-1763">Az.ServiceFabric</span></span>
* <span data-ttu-id="7af37-1764">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="7af37-1764">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="7af37-1765">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="7af37-1765">Fix some error messages.</span></span>
* <span data-ttu-id="7af37-1766">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="7af37-1766">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="7af37-1767">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="7af37-1767">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="7af37-1768">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="7af37-1768">Az.SignalR</span></span>
* <span data-ttu-id="7af37-1769">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="7af37-1769">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="7af37-1770">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7af37-1770">Az.Sql</span></span>
* <span data-ttu-id="7af37-1771">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="7af37-1771">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7af37-1772">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="7af37-1772">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="7af37-1773">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="7af37-1773">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="7af37-1774">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="7af37-1774">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7af37-1775">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7af37-1775">Az.Storage</span></span>
* <span data-ttu-id="7af37-1776">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="7af37-1776">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7af37-1777">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="7af37-1777">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="7af37-1778">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="7af37-1778">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="7af37-1779">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="7af37-1779">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="7af37-1780">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="7af37-1780">Az.TrafficManager</span></span>
* <span data-ttu-id="7af37-1781">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="7af37-1781">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7af37-1782">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7af37-1782">Az.Websites</span></span>
* <span data-ttu-id="7af37-1783">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="7af37-1783">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7af37-1784">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="7af37-1784">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="7af37-1785">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="7af37-1785">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="7af37-1786">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7af37-1786">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7af37-1787">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7af37-1787">Az.Accounts</span></span>
* <span data-ttu-id="7af37-1788">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="7af37-1788">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7af37-1789">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7af37-1789">Az.Compute</span></span>
* <span data-ttu-id="7af37-1790">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="7af37-1790">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="7af37-1791">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="7af37-1791">Updated the description of ID in help files</span></span>
* <span data-ttu-id="7af37-1792">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="7af37-1792">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7af37-1793">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7af37-1793">Az.DataLakeStore</span></span>
* <span data-ttu-id="7af37-1794">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="7af37-1794">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="7af37-1795">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="7af37-1795">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7af37-1796">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7af37-1796">Az.EventGrid</span></span>
* <span data-ttu-id="7af37-1797">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="7af37-1797">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="7af37-1798">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="7af37-1798">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="7af37-1799">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="7af37-1799">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="7af37-1800">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="7af37-1800">Event Time-To-Live,</span></span>
        - <span data-ttu-id="7af37-1801">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="7af37-1801">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="7af37-1802">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="7af37-1802">Dead letter endpoint.</span></span>
    - <span data-ttu-id="7af37-1803">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="7af37-1803">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="7af37-1804">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="7af37-1804">Event Time-To-Live,</span></span>
        - <span data-ttu-id="7af37-1805">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="7af37-1805">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="7af37-1806">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="7af37-1806">Dead letter endpoint.</span></span>
* <span data-ttu-id="7af37-1807">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="7af37-1807">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="7af37-1808">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="7af37-1808">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7af37-1809">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7af37-1809">Az.IotHub</span></span>
* <span data-ttu-id="7af37-1810">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="7af37-1810">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7af37-1811">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7af37-1811">Az.LogicApp</span></span>
* <span data-ttu-id="7af37-1812">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="7af37-1812">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="7af37-1813">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7af37-1813">Az.Resources</span></span>
* <span data-ttu-id="7af37-1814">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="7af37-1814">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="7af37-1815">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="7af37-1815">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="7af37-1816">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="7af37-1816">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="7af37-1817">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="7af37-1817">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="7af37-1818">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="7af37-1818">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="7af37-1819">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="7af37-1819">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="7af37-1820">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="7af37-1820">Az.SignalR</span></span>
* <span data-ttu-id="7af37-1821">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="7af37-1821">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="7af37-1822">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7af37-1822">Az.Sql</span></span>
* <span data-ttu-id="7af37-1823">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="7af37-1823">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7af37-1824">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7af37-1824">Az.Storage</span></span>
* <span data-ttu-id="7af37-1825">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="7af37-1825">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="7af37-1826">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="7af37-1826">New-AzStorageContext</span></span>
* <span data-ttu-id="7af37-1827">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="7af37-1827">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="7af37-1828">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="7af37-1828">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7af37-1829">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7af37-1829">Az.Websites</span></span>
* <span data-ttu-id="7af37-1830">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="7af37-1830">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="7af37-1831">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="7af37-1831">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="7af37-1832">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="7af37-1832">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="7af37-1833">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="7af37-1833">General</span></span>

- <span data-ttu-id="7af37-1834">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="7af37-1834">General Availability of Az Module</span></span>
- <span data-ttu-id="7af37-1835">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="7af37-1835">Online help for each module</span></span>
- <span data-ttu-id="7af37-1836">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="7af37-1836">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="7af37-1837">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7af37-1837">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="7af37-1838">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7af37-1838">Az.Accounts</span></span>
- <span data-ttu-id="7af37-1839">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="7af37-1839">Changed from Az.Profile</span></span>
- <span data-ttu-id="7af37-1840">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="7af37-1840">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="7af37-1841">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7af37-1841">Az.ApiManagement</span></span>
- <span data-ttu-id="7af37-1842">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="7af37-1842">Fixes for #7002</span></span>
- <span data-ttu-id="7af37-1843">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7af37-1843">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="7af37-1844">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7af37-1844">Az.Batch</span></span>
- <span data-ttu-id="7af37-1845">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="7af37-1845">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="7af37-1846">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="7af37-1846">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="7af37-1847">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7af37-1847">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="7af37-1848">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="7af37-1848">Az.Billing</span></span>
- <span data-ttu-id="7af37-1849">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="7af37-1849">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="7af37-1850">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="7af37-1850">Az.CognitivServices</span></span>
- <span data-ttu-id="7af37-1851">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="7af37-1851">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="7af37-1852">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="7af37-1852">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="7af37-1853">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7af37-1853">Az.ContainerInstance</span></span>
- <span data-ttu-id="7af37-1854">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="7af37-1854">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="7af37-1855">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="7af37-1855">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="7af37-1856">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7af37-1856">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="7af37-1857">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7af37-1857">Az.DataLakeStore</span></span>
- <span data-ttu-id="7af37-1858">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7af37-1858">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="7af37-1859">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7af37-1859">Az.Monitor</span></span>
- <span data-ttu-id="7af37-1860">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7af37-1860">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="7af37-1861">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7af37-1861">Az.KeyVault</span></span>
- <span data-ttu-id="7af37-1862">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="7af37-1862">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="7af37-1863">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="7af37-1863">Az.MachineLearning</span></span>
- <span data-ttu-id="7af37-1864">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="7af37-1864">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="7af37-1865">Az.Media</span><span class="sxs-lookup"><span data-stu-id="7af37-1865">Az.Media</span></span>
- <span data-ttu-id="7af37-1866">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="7af37-1866">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="7af37-1867">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7af37-1867">Az.Network</span></span>
<span data-ttu-id="7af37-1868">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="7af37-1868">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="7af37-1869">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="7af37-1869">New cmdlets added:</span></span>
        - <span data-ttu-id="7af37-1870">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7af37-1870">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7af37-1871">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7af37-1871">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7af37-1872">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7af37-1872">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7af37-1873">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7af37-1873">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7af37-1874">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7af37-1874">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7af37-1875">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="7af37-1875">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="7af37-1876">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="7af37-1876">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="7af37-1877">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="7af37-1877">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="7af37-1878">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7af37-1878">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="7af37-1879">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7af37-1879">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="7af37-1880">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7af37-1880">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="7af37-1881">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7af37-1881">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="7af37-1882">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7af37-1882">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="7af37-1883">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7af37-1883">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="7af37-1884">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="7af37-1884">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="7af37-1885">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7af37-1885">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="7af37-1886">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7af37-1886">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="7af37-1887">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7af37-1887">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="7af37-1888">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7af37-1888">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="7af37-1889">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="7af37-1889">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="7af37-1890">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7af37-1890">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="7af37-1891">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7af37-1891">Az.OperationalInsights</span></span>
- <span data-ttu-id="7af37-1892">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7af37-1892">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="7af37-1893">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7af37-1893">Az.Profile</span></span>
- <span data-ttu-id="7af37-1894">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="7af37-1894">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="7af37-1895">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7af37-1895">Az.RecoveryServices</span></span>
- <span data-ttu-id="7af37-1896">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7af37-1896">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="7af37-1897">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7af37-1897">Az.Resources</span></span>
- <span data-ttu-id="7af37-1898">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7af37-1898">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="7af37-1899">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7af37-1899">Az.ServiceFabric</span></span>
- <span data-ttu-id="7af37-1900">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="7af37-1900">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="7af37-1901">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7af37-1901">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="7af37-1902">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="7af37-1902">Az.SIgnalR</span></span>
- <span data-ttu-id="7af37-1903">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="7af37-1903">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="7af37-1904">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7af37-1904">Az.Sql</span></span>
- <span data-ttu-id="7af37-1905">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="7af37-1905">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="7af37-1906">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="7af37-1906">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="7af37-1907">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7af37-1907">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="7af37-1908">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7af37-1908">Az.Storage</span></span>
- <span data-ttu-id="7af37-1909">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7af37-1909">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="7af37-1910">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7af37-1910">Az.Websites</span></span>
- <span data-ttu-id="7af37-1911">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7af37-1911">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="7af37-1912">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="7af37-1912">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="7af37-1913">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="7af37-1913">General</span></span>

* <span data-ttu-id="7af37-1914">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="7af37-1914">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="7af37-1915">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7af37-1915">Az.Compute</span></span>

* <span data-ttu-id="7af37-1916">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="7af37-1916">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="7af37-1917">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7af37-1917">Az.DataLakeStore</span></span>

* <span data-ttu-id="7af37-1918">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="7af37-1918">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="7af37-1919">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7af37-1919">Az.FrontDoor</span></span>

* <span data-ttu-id="7af37-1920">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="7af37-1920">Fixed some broken links</span></span>
    - <span data-ttu-id="7af37-1921">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="7af37-1921">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="7af37-1922">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="7af37-1922">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="7af37-1923">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7af37-1923">Az.RecoveryServices</span></span>

* <span data-ttu-id="7af37-1924">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="7af37-1924">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="7af37-1925">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="7af37-1925">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="7af37-1926">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7af37-1926">Az.Resources</span></span>

* <span data-ttu-id="7af37-1927">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="7af37-1927">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="7af37-1928">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="7af37-1928">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="7af37-1929">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7af37-1929">Az.Sql</span></span>

* <span data-ttu-id="7af37-1930">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="7af37-1930">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="7af37-1931">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="7af37-1931">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="7af37-1932">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="7af37-1932">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="7af37-1933">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7af37-1933">Az.Storage</span></span>

* <span data-ttu-id="7af37-1934">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7af37-1934">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="7af37-1935">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="7af37-1935">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="7af37-1936">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="7af37-1936">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="7af37-1937">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="7af37-1937">Support Static Website configuration</span></span>
    - <span data-ttu-id="7af37-1938">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="7af37-1938">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="7af37-1939">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="7af37-1939">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="7af37-1940">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7af37-1940">Az.Websites</span></span>

* <span data-ttu-id="7af37-1941">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7af37-1941">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="7af37-1942">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="7af37-1942">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="7af37-1943">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7af37-1943">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="7af37-1944">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="7af37-1944">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="7af37-1945">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7af37-1945">Az.ApiManagement</span></span>
* <span data-ttu-id="7af37-1946">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="7af37-1946">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="7af37-1947">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7af37-1947">Az.Automation</span></span>
* <span data-ttu-id="7af37-1948">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="7af37-1948">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="7af37-1949">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="7af37-1949">Added Update Management cmdlets</span></span>
* <span data-ttu-id="7af37-1950">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="7af37-1950">Added Source Control cmdlets</span></span>
* <span data-ttu-id="7af37-1951">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="7af37-1951">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="7af37-1952">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="7af37-1952">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="7af37-1953">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7af37-1953">Az.Compute</span></span>
* <span data-ttu-id="7af37-1954">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="7af37-1954">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="7af37-1955">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="7af37-1955">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="7af37-1956">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7af37-1956">Az.ContainerInstance</span></span>
* <span data-ttu-id="7af37-1957">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="7af37-1957">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="7af37-1958">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="7af37-1958">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="7af37-1959">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="7af37-1959">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="7af37-1960">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7af37-1960">Az.Network</span></span>
* <span data-ttu-id="7af37-1961">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="7af37-1961">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="7af37-1962">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="7af37-1962">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="7af37-1963">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="7af37-1963">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="7af37-1964">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="7af37-1964">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="7af37-1965">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="7af37-1965">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="7af37-1966">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="7af37-1966">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="7af37-1967">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="7af37-1967">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="7af37-1968">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="7af37-1968">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="7af37-1969">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="7af37-1969">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="7af37-1970">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="7af37-1970">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="7af37-1971">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="7af37-1971">Az.Relay</span></span>
* <span data-ttu-id="7af37-1972">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="7af37-1972">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="7af37-1973">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7af37-1973">Az.Resources</span></span>
* <span data-ttu-id="7af37-1974">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="7af37-1974">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="7af37-1975">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="7af37-1975">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="7af37-1976">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="7af37-1976">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="7af37-1977">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7af37-1977">Az.ServiceFabric</span></span>
* <span data-ttu-id="7af37-1978">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="7af37-1978">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="7af37-1979">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7af37-1979">Az.Sql</span></span>
* <span data-ttu-id="7af37-1980">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="7af37-1980">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="7af37-1981">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="7af37-1981">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7af37-1982">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="7af37-1982">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7af37-1983">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="7af37-1983">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7af37-1984">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="7af37-1984">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7af37-1985">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="7af37-1985">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="7af37-1986">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="7af37-1986">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="7af37-1987">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="7af37-1987">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="7af37-1988">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="7af37-1988">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="7af37-1989">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="7af37-1989">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="7af37-1990">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="7af37-1990">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="7af37-1991">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="7af37-1991">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="7af37-1992">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="7af37-1992">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="7af37-1993">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="7af37-1993">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="7af37-1994">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="7af37-1994">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="7af37-1995">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="7af37-1995">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="7af37-1996">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="7af37-1996">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="7af37-1997">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="7af37-1997">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="7af37-1998">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="7af37-1998">General</span></span>
* <span data-ttu-id="7af37-1999">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="7af37-1999">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="7af37-2000">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7af37-2000">Az.Profile</span></span>
* <span data-ttu-id="7af37-2001">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="7af37-2001">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="7af37-2002">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="7af37-2002">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="7af37-2003">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="7af37-2003">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="7af37-2004">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="7af37-2004">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="7af37-2005">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="7af37-2005">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="7af37-2006">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="7af37-2006">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="7af37-2007">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="7af37-2007">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="7af37-2008">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7af37-2008">Az.CognitiveServices</span></span>
* <span data-ttu-id="7af37-2009">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="7af37-2009">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7af37-2010">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7af37-2010">Az.Compute</span></span>
* <span data-ttu-id="7af37-2011">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="7af37-2011">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="7af37-2012">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="7af37-2012">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="7af37-2013">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="7af37-2013">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7af37-2014">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7af37-2014">Az.DataLakeStore</span></span>
* <span data-ttu-id="7af37-2015">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="7af37-2015">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="7af37-2016">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="7af37-2016">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="7af37-2017">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="7af37-2017">Az.Insights</span></span>
* <span data-ttu-id="7af37-2018">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="7af37-2018">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="7af37-2019">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="7af37-2019">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="7af37-2020">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="7af37-2020">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="7af37-2021">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="7af37-2021">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7af37-2022">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7af37-2022">Az.Network</span></span>
* <span data-ttu-id="7af37-2023">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="7af37-2023">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="7af37-2024">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="7af37-2024">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="7af37-2025">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="7af37-2025">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="7af37-2026">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="7af37-2026">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="7af37-2027">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="7af37-2027">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="7af37-2028">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="7af37-2028">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="7af37-2029">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="7af37-2029">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7af37-2030">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7af37-2030">Az.PolicyInsights</span></span>
* <span data-ttu-id="7af37-2031">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="7af37-2031">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="7af37-2032">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7af37-2032">Az.Resources</span></span>
* <span data-ttu-id="7af37-2033">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="7af37-2033">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="7af37-2034">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="7af37-2034">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7af37-2035">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7af37-2035">Az.ServiceBus</span></span>
* <span data-ttu-id="7af37-2036">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="7af37-2036">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7af37-2037">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7af37-2037">Az.ServiceFabric</span></span>
* <span data-ttu-id="7af37-2038">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="7af37-2038">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="7af37-2039">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="7af37-2039">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="7af37-2040">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="7af37-2040">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="7af37-2041">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="7af37-2041">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="7af37-2042">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="7af37-2042">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="7af37-2043">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="7af37-2043">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="7af37-2044">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7af37-2044">Az.Profile</span></span>
* <span data-ttu-id="7af37-2045">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="7af37-2045">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="7af37-2046">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="7af37-2046">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7af37-2047">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7af37-2047">Az.Compute</span></span>
* <span data-ttu-id="7af37-2048">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="7af37-2048">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="7af37-2049">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="7af37-2049">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7af37-2050">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7af37-2050">Az.DataLakeStore</span></span>
* <span data-ttu-id="7af37-2051">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="7af37-2051">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="7af37-2052">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7af37-2052">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="7af37-2053">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7af37-2053">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="7af37-2054">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7af37-2054">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="7af37-2055">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7af37-2055">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7af37-2056">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7af37-2056">Az.Network</span></span>
* <span data-ttu-id="7af37-2057">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="7af37-2057">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="7af37-2058">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="7af37-2058">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7af37-2059">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7af37-2059">Az.Resources</span></span>
* <span data-ttu-id="7af37-2060">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="7af37-2060">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="7af37-2061">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="7af37-2061">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="7af37-2062">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="7af37-2062">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="7af37-2063">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="7af37-2063">Azure.Storage</span></span>
* <span data-ttu-id="7af37-2064">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="7af37-2064">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="7af37-2065">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="7af37-2065">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="7af37-2066">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="7af37-2066">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="7af37-2067">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="7af37-2067">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="7af37-2068">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="7af37-2068">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="7af37-2069">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7af37-2069">Az.CognitiveServices</span></span>
* <span data-ttu-id="7af37-2070">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="7af37-2070">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7af37-2071">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7af37-2071">Az.Compute</span></span>
* <span data-ttu-id="7af37-2072">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="7af37-2072">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="7af37-2073">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="7af37-2073">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="7af37-2074">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="7af37-2074">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="7af37-2075">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="7af37-2075">Az.DataFactoryV2</span></span>
* <span data-ttu-id="7af37-2076">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="7af37-2076">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7af37-2077">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7af37-2077">Az.Network</span></span>
* <span data-ttu-id="7af37-2078">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="7af37-2078">Added NetworkProfile functionality.</span></span> <span data-ttu-id="7af37-2079">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="7af37-2079">new cmdlets added</span></span>
    - <span data-ttu-id="7af37-2080">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7af37-2080">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="7af37-2081">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7af37-2081">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="7af37-2082">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7af37-2082">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="7af37-2083">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7af37-2083">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="7af37-2084">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="7af37-2084">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="7af37-2085">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="7af37-2085">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="7af37-2086">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="7af37-2086">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="7af37-2087">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="7af37-2087">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="7af37-2088">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="7af37-2088">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7af37-2089">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7af37-2089">Az.RedisCache</span></span>
* <span data-ttu-id="7af37-2090">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="7af37-2090">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="7af37-2091">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="7af37-2091">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="7af37-2092">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7af37-2092">Az.Resources</span></span>
* <span data-ttu-id="7af37-2093">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7af37-2093">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="7af37-2094">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="7af37-2094">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="7af37-2095">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7af37-2095">Az.Sql</span></span>
* <span data-ttu-id="7af37-2096">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="7af37-2096">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7af37-2097">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7af37-2097">Az.Websites</span></span>
* <span data-ttu-id="7af37-2098">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="7af37-2098">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="7af37-2099">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="7af37-2099">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="7af37-2100">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="7af37-2100">0.2.0 - September 2018</span></span>
 <span data-ttu-id="7af37-2101">Начальный выпуск</span><span class="sxs-lookup"><span data-stu-id="7af37-2101">Initial Release</span></span>
