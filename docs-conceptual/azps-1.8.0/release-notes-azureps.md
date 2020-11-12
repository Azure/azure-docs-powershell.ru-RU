---
title: Заметки о выпуске Azure PowerShell
description: Узнайте обо всех последних обновлениях модулей Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/30/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 7d468fb760f9be23e8b8eea7f74adc1dd137e469
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2020
ms.locfileid: "93408332"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="86657-103">Заметки о выпуске Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="86657-103">Azure PowerShell release notes</span></span>
## <a name="180---april-2019"></a><span data-ttu-id="86657-104">1.8.0 — апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="86657-104">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="86657-105">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="86657-105">Highlights since the last major release</span></span>
* <span data-ttu-id="86657-106">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="86657-106">General availability of `Az` module</span></span>
* <span data-ttu-id="86657-107">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="86657-107">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="86657-108">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="86657-108">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="86657-109">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="86657-109">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="86657-110">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="86657-110">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="86657-111">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="86657-111">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="86657-112">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="86657-112">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="86657-113">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="86657-113">Az.Accounts</span></span>
* <span data-ttu-id="86657-114">Обновлен командлет Uninstall-AzureRm для правильного удаления модулей в Mac.</span><span class="sxs-lookup"><span data-stu-id="86657-114">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="86657-115">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="86657-115">Az.Batch</span></span>
* <span data-ttu-id="86657-116">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="86657-116">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="86657-117">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="86657-117">Az.Cdn</span></span>
* <span data-ttu-id="86657-118">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="86657-118">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="86657-119">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="86657-119">Az.CognitiveServices</span></span>
* <span data-ttu-id="86657-120">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="86657-120">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86657-121">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86657-121">Az.Compute</span></span>
* <span data-ttu-id="86657-122">Устранена проблема с установкой AEM, если в идентификаторах ресурсов дисков группа ресурсов указана в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="86657-122">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="86657-123">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="86657-123">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="86657-124">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="86657-124">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="86657-125">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="86657-125">Az.DataFactory</span></span>
* <span data-ttu-id="86657-126">Добавлены свойства SsisProperties, если NodeCount не имеет значения NULL для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="86657-126">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="86657-127">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="86657-127">Az.DataLakeStore</span></span>
* <span data-ttu-id="86657-128">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="86657-128">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="86657-129">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="86657-129">Az.EventGrid</span></span>
* <span data-ttu-id="86657-130">Обновлен текст справки для конечной точки, указывающий, что необходимо создать ресурсы, прежде чем использовать командлеты для создания или обновления подписки на события.</span><span class="sxs-lookup"><span data-stu-id="86657-130">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="86657-131">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="86657-131">Az.EventHub</span></span>
* <span data-ttu-id="86657-132">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="86657-132">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="86657-133">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="86657-133">Az.HDInsight</span></span>
* <span data-ttu-id="86657-134">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="86657-134">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="86657-135">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="86657-135">Az.IotHub</span></span>
* <span data-ttu-id="86657-136">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="86657-136">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="86657-137">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="86657-137">Az.KeyVault</span></span>
* <span data-ttu-id="86657-138">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="86657-138">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="86657-139">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="86657-139">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="86657-140">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="86657-140">Az.MachineLearning</span></span>
* <span data-ttu-id="86657-141">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="86657-141">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="86657-142">Az.Media</span><span class="sxs-lookup"><span data-stu-id="86657-142">Az.Media</span></span>
* <span data-ttu-id="86657-143">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="86657-143">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="86657-144">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="86657-144">Az.Monitor</span></span>
  * <span data-ttu-id="86657-145">Добавлены новые командлеты для правила генерации оповещений на основе метрик GenV2 (не классических).</span><span class="sxs-lookup"><span data-stu-id="86657-145">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="86657-146">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="86657-146">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="86657-147">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="86657-147">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="86657-148">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="86657-148">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="86657-149">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="86657-149">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="86657-150">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="86657-150">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="86657-151">Обновлен пакет SDK Monitor до предварительной версии 0.22.0.</span><span class="sxs-lookup"><span data-stu-id="86657-151">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="86657-152">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86657-152">Az.Network</span></span>
* <span data-ttu-id="86657-153">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="86657-153">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="86657-154">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="86657-154">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="86657-155">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="86657-155">Az.NotificationHubs</span></span>
* <span data-ttu-id="86657-156">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="86657-156">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="86657-157">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="86657-157">Az.OperationalInsights</span></span>
* <span data-ttu-id="86657-158">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="86657-158">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="86657-159">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="86657-159">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="86657-160">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="86657-160">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="86657-161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="86657-161">Az.RecoveryServices</span></span>
* <span data-ttu-id="86657-162">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="86657-162">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="86657-163">Обновлен табличный формат для SQL на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="86657-163">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="86657-164">Добавлен альтернативный метод для получения расположения в Общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="86657-164">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="86657-165">Обновлено значение ScheduleRunDays в объекте SchedulePolicy в соответствии с часовым поясом.</span><span class="sxs-lookup"><span data-stu-id="86657-165">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="86657-166">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="86657-166">Az.RedisCache</span></span>
* <span data-ttu-id="86657-167">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="86657-167">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="86657-168">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86657-168">Az.Resources</span></span>
* <span data-ttu-id="86657-169">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="86657-169">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="86657-170">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86657-170">Az.Sql</span></span>
* <span data-ttu-id="86657-171">Заменена зависимость от пакета SDK монитора на обычный код.</span><span class="sxs-lookup"><span data-stu-id="86657-171">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="86657-172">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="86657-172">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="86657-173">Улучшен процесс классификации нескольких столбцов.</span><span class="sxs-lookup"><span data-stu-id="86657-173">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="86657-174">Добавлены свойства SKU (имя, семейство, производительность SKU) в отклике Get-AzSqlServerServiceObjective, а также по умолчанию задан табличный формат.</span><span class="sxs-lookup"><span data-stu-id="86657-174">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="86657-175">C помощью Get-AzSqlServerServiceObjective теперь можно получать список доступных целевых служб по расположению без необходимости заранее размещать сервер в регионе.</span><span class="sxs-lookup"><span data-stu-id="86657-175">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="86657-176">Поддерживается параметр часового пояса при создании Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="86657-176">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="86657-177">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="86657-177">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="86657-178">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="86657-178">Az.Websites</span></span>
* <span data-ttu-id="86657-179">Исправлены командлеты Set-AzWebApp и Set-AzWebAppSlot, которые теперь не удаляют теги при выполнении.</span><span class="sxs-lookup"><span data-stu-id="86657-179">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="86657-180">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="86657-180">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="86657-181">Обновлен пакет SDK веб-узлов.</span><span class="sxs-lookup"><span data-stu-id="86657-181">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="86657-182">Удалено свойство AdminSiteName из PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="86657-182">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="86657-183">1.7.0 —апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="86657-183">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="86657-184">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="86657-184">Highlights since the last major release</span></span>
* <span data-ttu-id="86657-185">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="86657-185">General availability of `Az` module</span></span>
* <span data-ttu-id="86657-186">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="86657-186">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="86657-187">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="86657-187">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="86657-188">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="86657-188">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="86657-189">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="86657-189">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="86657-190">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="86657-190">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="86657-191">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="86657-191">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="86657-192">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="86657-192">Az.Accounts</span></span>
* <span data-ttu-id="86657-193">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметр AzureAnalysisServicesEndpointResourceId.</span><span class="sxs-lookup"><span data-stu-id="86657-193">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="86657-194">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="86657-194">Az.AnalysisServices</span></span>
* <span data-ttu-id="86657-195">Использование ServiceClient в командлетах плоскости данных и удаление исходной логики проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="86657-195">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="86657-196">Add-AzureASAccount используется как оболочка для Connect-AzAccount во избежание критических изменений.</span><span class="sxs-lookup"><span data-stu-id="86657-196">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="86657-197">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="86657-197">Az.Automation</span></span>
* <span data-ttu-id="86657-198">Исправлена ошибка командлета New-AzAutomationSoftwareUpdateConfiguration, связанная с включением.</span><span class="sxs-lookup"><span data-stu-id="86657-198">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="86657-199">Теперь параметры IncludedKbNumber и IncludedPackageNameMask должны работать нормально.</span><span class="sxs-lookup"><span data-stu-id="86657-199">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="86657-200">Исправлена ошибка динамической группы управления обновлениями службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="86657-200">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86657-201">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86657-201">Az.Compute</span></span>
* <span data-ttu-id="86657-202">В командлеты New-AzDiskConfig и New-AzSnapshotConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="86657-202">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="86657-203">Теперь можно создавать виртуальные машину на основе образов из коллекции от других клиентов.</span><span class="sxs-lookup"><span data-stu-id="86657-203">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="86657-204">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="86657-204">Az.ContainerInstance</span></span>
* <span data-ttu-id="86657-205">Исправлена проблема в параметре -Command командлета New-AzContainerGroup, из-за которой в конце добавлялся пустой аргумент.</span><span class="sxs-lookup"><span data-stu-id="86657-205">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="86657-206">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="86657-206">Az.DataFactory</span></span>
* <span data-ttu-id="86657-207">Пакет SDK для ADF .NET обновлен до версии 3.0.2.</span><span class="sxs-lookup"><span data-stu-id="86657-207">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="86657-208">Командлет Set-AzDataFactoryV2 обновлен с помощью дополнительных параметров для настроек, связанных с RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="86657-208">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="86657-209">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86657-209">Az.Resources</span></span>
* <span data-ttu-id="86657-210">Улучшена обработка поставщиков Get-AzResource при предоставлении параметров -ResourceId или -ResourceGroupName, -Name и -ResourceType.</span><span class="sxs-lookup"><span data-stu-id="86657-210">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="86657-211">Улучшена обработка ошибок в командлетах Test-AzDeployment и Test-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="86657-211">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="86657-212">Теперь ошибки, возникающие за пределами проверки развертывания, обрабатываются и включаются в выходные данные команды.</span><span class="sxs-lookup"><span data-stu-id="86657-212">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="86657-213">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="86657-213">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="86657-214">Добавлен параметр-переключатель -IgnoreDynamicParameters, с помощью которого можно настроить командлеты развертывания так, чтобы они пропускали запросы в сценариях скриптов и заданий.</span><span class="sxs-lookup"><span data-stu-id="86657-214">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="86657-215">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="86657-215">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="86657-216">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86657-216">Az.Sql</span></span>
* <span data-ttu-id="86657-217">Поддержка классификации данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="86657-217">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="86657-218">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="86657-218">Az.Storage</span></span>
* <span data-ttu-id="86657-219">Подробные сообщения об ошибке передаются при создании контекста хранилища с помощью параметра -UseConnectedAccount, но без входа в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="86657-219">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="86657-220">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="86657-220">New-AzStorageContext</span></span>
* <span data-ttu-id="86657-221">Поддержка свойств службы управления BLOB-объектов в указанной учетной записи хранения с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="86657-221">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="86657-222">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="86657-222">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="86657-223">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="86657-223">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="86657-224">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="86657-224">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="86657-225">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="86657-225">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="86657-226">Поддержка параметра -AsJob в командлетах для отправки и скачивания больших двоичных объектов и файлов.</span><span class="sxs-lookup"><span data-stu-id="86657-226">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="86657-227">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="86657-227">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="86657-228">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="86657-228">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="86657-229">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="86657-229">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="86657-230">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="86657-230">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="86657-231">1.6.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="86657-231">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="86657-232">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="86657-232">Highlights since the last major release</span></span>
* <span data-ttu-id="86657-233">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="86657-233">General availability of `Az` module</span></span>
* <span data-ttu-id="86657-234">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="86657-234">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="86657-235">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="86657-235">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="86657-236">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="86657-236">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="86657-237">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="86657-237">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="86657-238">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="86657-238">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="86657-239">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="86657-239">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="86657-240">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="86657-240">Az.Automation</span></span>
* <span data-ttu-id="86657-241">В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:</span><span class="sxs-lookup"><span data-stu-id="86657-241">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="86657-242">динамическое группирование;</span><span class="sxs-lookup"><span data-stu-id="86657-242">Dynamic grouping</span></span>
    * <span data-ttu-id="86657-243">скрипты предварительного или последующего выполнения;</span><span class="sxs-lookup"><span data-stu-id="86657-243">Pre-Post script</span></span>
    * <span data-ttu-id="86657-244">параметр перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="86657-244">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86657-245">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86657-245">Az.Compute</span></span>
* <span data-ttu-id="86657-246">Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.</span><span class="sxs-lookup"><span data-stu-id="86657-246">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="86657-247">Обновление клиентской библиотеки вычислений до версии 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="86657-247">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="86657-248">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="86657-248">Az.KeyVault</span></span>
* <span data-ttu-id="86657-249">Добавлена поддержка подстановочных знаков в командлетах KeyVault.</span><span class="sxs-lookup"><span data-stu-id="86657-249">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="86657-250">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86657-250">Az.Network</span></span>
* <span data-ttu-id="86657-251">Добавлена поддержка анализа угроз для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="86657-251">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="86657-252">Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="86657-252">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="86657-253">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="86657-253">Az.RecoveryServices</span></span>
* <span data-ttu-id="86657-254">В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.</span><span class="sxs-lookup"><span data-stu-id="86657-254">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="86657-255">Добавлена поддержка канала для отмены регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="86657-255">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="86657-256">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86657-256">Az.Resources</span></span>
* <span data-ttu-id="86657-257">Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="86657-257">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="86657-258">Обновлены учетные данные, используемые при общих вызовах к ARM.</span><span class="sxs-lookup"><span data-stu-id="86657-258">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="86657-259">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86657-259">Az.Sql</span></span>
* <span data-ttu-id="86657-260">Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="86657-260">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="86657-261">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="86657-261">Az.Storage</span></span>
* <span data-ttu-id="86657-262">Поддержка получения, настройки и удаления политики управления в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="86657-262">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="86657-263">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="86657-263">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="86657-264">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="86657-264">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="86657-265">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="86657-265">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="86657-266">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="86657-266">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="86657-267">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="86657-267">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="86657-268">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="86657-268">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="86657-269">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="86657-269">Az.Websites</span></span>
* <span data-ttu-id="86657-270">Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="86657-270">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="86657-271">1.5.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="86657-271">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="86657-272">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="86657-272">Az.Accounts</span></span>
* <span data-ttu-id="86657-273">Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.</span><span class="sxs-lookup"><span data-stu-id="86657-273">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="86657-274">Обновлены примеры для Connect AzAccount.</span><span class="sxs-lookup"><span data-stu-id="86657-274">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="86657-275">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="86657-275">Az.Automation</span></span>
* <span data-ttu-id="86657-276">Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="86657-276">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="86657-277">Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов.</span><span class="sxs-lookup"><span data-stu-id="86657-277">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="86657-278">Теперь он возвращает все узлы.</span><span class="sxs-lookup"><span data-stu-id="86657-278">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="86657-279">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="86657-279">Az.Cdn</span></span>
* <span data-ttu-id="86657-280">Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.</span><span class="sxs-lookup"><span data-stu-id="86657-280">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86657-281">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86657-281">Az.Compute</span></span>
* <span data-ttu-id="86657-282">Добавлена поддержка подстановочных знаков в командлетах Get.</span><span class="sxs-lookup"><span data-stu-id="86657-282">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="86657-283">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="86657-283">Az.DataFactory</span></span>
* <span data-ttu-id="86657-284">Обновлен пакет SDK для ADF .NET до версии 3.0.1.</span><span class="sxs-lookup"><span data-stu-id="86657-284">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="86657-285">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="86657-285">Az.LogicApp</span></span>
* <span data-ttu-id="86657-286">Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.</span><span class="sxs-lookup"><span data-stu-id="86657-286">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="86657-287">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86657-287">Az.Network</span></span>
* <span data-ttu-id="86657-288">Добавлена поддержка подстановочных знаков в командлетах Network.</span><span class="sxs-lookup"><span data-stu-id="86657-288">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="86657-289">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="86657-289">Az.RecoveryServices</span></span>
* <span data-ttu-id="86657-290">Добавлена поддержка SQL Server на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="86657-290">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="86657-291">Обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="86657-291">SDK Update</span></span>
* <span data-ttu-id="86657-292">Удалена проверка VMappContainer в Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="86657-292">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="86657-293">Добавлены параметры Name и ServerName для Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="86657-293">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="86657-294">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86657-294">Az.Resources</span></span>
* <span data-ttu-id="86657-295">Добавлен параметр `-TemplateObject` в командлеты для развертывания.</span><span class="sxs-lookup"><span data-stu-id="86657-295">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="86657-296">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.</span><span class="sxs-lookup"><span data-stu-id="86657-296">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="86657-297">Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="86657-297">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="86657-298">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.</span><span class="sxs-lookup"><span data-stu-id="86657-298">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="86657-299">Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="86657-299">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="86657-300">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.</span><span class="sxs-lookup"><span data-stu-id="86657-300">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="86657-301">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86657-301">Az.Sql</span></span>
* <span data-ttu-id="86657-302">Обновление AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="86657-302">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="86657-303">Исправлено поведение для пограничного случая при создании параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="86657-303">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="86657-304">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="86657-304">Az.Storage</span></span>
* <span data-ttu-id="86657-305">Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="86657-305">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="86657-306">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="86657-306">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="86657-307">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="86657-307">Az.AnalysisServices</span></span>
* <span data-ttu-id="86657-308">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="86657-308">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="86657-309">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="86657-309">Az.Automation</span></span>
* <span data-ttu-id="86657-310">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="86657-310">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="86657-311">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="86657-311">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="86657-312">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="86657-312">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="86657-313">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="86657-313">Az.CognitiveServices</span></span>
* <span data-ttu-id="86657-314">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="86657-314">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86657-315">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86657-315">Az.Compute</span></span>
* <span data-ttu-id="86657-316">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="86657-316">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="86657-317">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="86657-317">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="86657-318">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="86657-318">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="86657-319">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="86657-319">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="86657-320">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="86657-320">Az.DataLakeStore</span></span>
* <span data-ttu-id="86657-321">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="86657-321">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="86657-322">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="86657-322">Az.EventHub</span></span>
* <span data-ttu-id="86657-323">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="86657-323">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="86657-324">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="86657-324">Az.KeyVault</span></span>
* <span data-ttu-id="86657-325">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="86657-325">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="86657-326">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="86657-326">Az.LogicApp</span></span>
* <span data-ttu-id="86657-327">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="86657-327">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="86657-328">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="86657-328">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="86657-329">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="86657-329">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="86657-330">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="86657-330">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="86657-331">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="86657-331">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="86657-332">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="86657-332">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="86657-333">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="86657-333">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="86657-334">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="86657-334">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="86657-335">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="86657-335">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="86657-336">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="86657-336">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="86657-337">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="86657-337">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="86657-338">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="86657-338">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="86657-339">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="86657-339">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="86657-340">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="86657-340">Az.Monitor</span></span>
* <span data-ttu-id="86657-341">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="86657-341">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="86657-342">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86657-342">Az.Network</span></span>
* <span data-ttu-id="86657-343">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="86657-343">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="86657-344">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="86657-344">Az.OperationalInsights</span></span>
* <span data-ttu-id="86657-345">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="86657-345">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="86657-346">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="86657-346">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="86657-347">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="86657-347">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="86657-348">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86657-348">Az.Resources</span></span>
* <span data-ttu-id="86657-349">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="86657-349">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="86657-350">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="86657-350">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="86657-351">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="86657-351">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="86657-352">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="86657-352">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="86657-353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86657-353">Az.Sql</span></span>
* <span data-ttu-id="86657-354">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="86657-354">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="86657-355">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="86657-355">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="86657-356">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="86657-356">Az.Websites</span></span>
* <span data-ttu-id="86657-357">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="86657-357">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="86657-358">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="86657-358">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="86657-359">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="86657-359">Az.Accounts</span></span>
* <span data-ttu-id="86657-360">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="86657-360">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="86657-361">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="86657-361">Az.AnalysisServices</span></span>
<span data-ttu-id="86657-362">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="86657-362">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86657-363">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86657-363">Az.Compute</span></span>
* <span data-ttu-id="86657-364">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="86657-364">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="86657-365">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="86657-365">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="86657-366">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="86657-366">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="86657-367">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="86657-367">Az.RecoveryServices</span></span>
<span data-ttu-id="86657-368">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="86657-368">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="86657-369">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86657-369">Az.Resources</span></span>
* <span data-ttu-id="86657-370">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="86657-370">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="86657-371">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="86657-371">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="86657-372">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="86657-372">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="86657-373">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="86657-373">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="86657-374">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86657-374">Az.Sql</span></span>
* <span data-ttu-id="86657-375">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="86657-375">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="86657-376">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="86657-376">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="86657-377">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="86657-377">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="86657-378">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="86657-378">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="86657-379">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="86657-379">Az.Accounts</span></span>
* <span data-ttu-id="86657-380">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="86657-380">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="86657-381">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="86657-381">Az.AnalysisServices</span></span>
* <span data-ttu-id="86657-382">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="86657-382">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="86657-383">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="86657-383">Az.RecoveryServices</span></span>
* <span data-ttu-id="86657-384">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="86657-384">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="86657-385">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="86657-385">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="86657-386">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="86657-386">Az.Accounts</span></span>
* <span data-ttu-id="86657-387">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="86657-387">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="86657-388">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="86657-388">Update incorrect online help URLs</span></span>
* <span data-ttu-id="86657-389">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="86657-389">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="86657-390">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="86657-390">Az.Aks</span></span>
* <span data-ttu-id="86657-391">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="86657-391">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="86657-392">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="86657-392">Az.Automation</span></span>
* <span data-ttu-id="86657-393">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="86657-393">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="86657-394">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="86657-394">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="86657-395">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="86657-395">Az.Cdn</span></span>
* <span data-ttu-id="86657-396">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="86657-396">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86657-397">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86657-397">Az.Compute</span></span>
* <span data-ttu-id="86657-398">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="86657-398">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="86657-399">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="86657-399">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="86657-400">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="86657-400">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="86657-401">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="86657-401">Az.ContainerRegistry</span></span>
* <span data-ttu-id="86657-402">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="86657-402">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="86657-403">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="86657-403">Az.DataFactory</span></span>
* <span data-ttu-id="86657-404">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="86657-404">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="86657-405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="86657-405">Az.DataLakeStore</span></span>
* <span data-ttu-id="86657-406">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="86657-406">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="86657-407">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="86657-407">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="86657-408">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="86657-408">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="86657-409">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="86657-409">Az.IotHub</span></span>
* <span data-ttu-id="86657-410">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="86657-410">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="86657-411">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="86657-411">Az.KeyVault</span></span>
* <span data-ttu-id="86657-412">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="86657-412">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="86657-413">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86657-413">Az.Network</span></span>
* <span data-ttu-id="86657-414">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="86657-414">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="86657-415">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86657-415">Az.Resources</span></span>
* <span data-ttu-id="86657-416">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="86657-416">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="86657-417">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="86657-417">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="86657-418">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="86657-418">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="86657-419">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="86657-419">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="86657-420">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="86657-420">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="86657-421">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="86657-421">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="86657-422">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="86657-422">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="86657-423">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="86657-423">Az.ServiceFabric</span></span>
* <span data-ttu-id="86657-424">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="86657-424">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="86657-425">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="86657-425">Fix some error messages.</span></span>
* <span data-ttu-id="86657-426">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="86657-426">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="86657-427">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="86657-427">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="86657-428">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="86657-428">Az.SignalR</span></span>
* <span data-ttu-id="86657-429">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="86657-429">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="86657-430">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86657-430">Az.Sql</span></span>
* <span data-ttu-id="86657-431">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="86657-431">Update incorrect online help URLs</span></span>
* <span data-ttu-id="86657-432">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="86657-432">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="86657-433">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="86657-433">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="86657-434">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="86657-434">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="86657-435">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="86657-435">Az.Storage</span></span>
* <span data-ttu-id="86657-436">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="86657-436">Update incorrect online help URLs</span></span>
* <span data-ttu-id="86657-437">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="86657-437">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="86657-438">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="86657-438">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="86657-439">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="86657-439">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="86657-440">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="86657-440">Az.TrafficManager</span></span>
* <span data-ttu-id="86657-441">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="86657-441">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="86657-442">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="86657-442">Az.Websites</span></span>
* <span data-ttu-id="86657-443">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="86657-443">Update incorrect online help URLs</span></span>
* <span data-ttu-id="86657-444">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="86657-444">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="86657-445">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="86657-445">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="86657-446">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="86657-446">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="86657-447">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="86657-447">Az.Accounts</span></span>
* <span data-ttu-id="86657-448">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="86657-448">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86657-449">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86657-449">Az.Compute</span></span>
* <span data-ttu-id="86657-450">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="86657-450">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="86657-451">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="86657-451">Updated the description of ID in help files</span></span>
* <span data-ttu-id="86657-452">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="86657-452">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="86657-453">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="86657-453">Az.DataLakeStore</span></span>
* <span data-ttu-id="86657-454">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="86657-454">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="86657-455">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="86657-455">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="86657-456">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="86657-456">Az.EventGrid</span></span>
* <span data-ttu-id="86657-457">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="86657-457">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="86657-458">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="86657-458">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="86657-459">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="86657-459">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="86657-460">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="86657-460">Event Time-To-Live,</span></span>
        - <span data-ttu-id="86657-461">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="86657-461">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="86657-462">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="86657-462">Dead letter endpoint.</span></span>
    - <span data-ttu-id="86657-463">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="86657-463">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="86657-464">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="86657-464">Event Time-To-Live,</span></span>
        - <span data-ttu-id="86657-465">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="86657-465">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="86657-466">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="86657-466">Dead letter endpoint.</span></span>
* <span data-ttu-id="86657-467">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="86657-467">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="86657-468">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="86657-468">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="86657-469">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="86657-469">Az.IotHub</span></span>
* <span data-ttu-id="86657-470">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="86657-470">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="86657-471">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="86657-471">Az.LogicApp</span></span>
* <span data-ttu-id="86657-472">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="86657-472">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="86657-473">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86657-473">Az.Resources</span></span>
* <span data-ttu-id="86657-474">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="86657-474">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="86657-475">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="86657-475">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="86657-476">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="86657-476">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="86657-477">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="86657-477">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="86657-478">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="86657-478">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="86657-479">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="86657-479">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="86657-480">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="86657-480">Az.SignalR</span></span>
* <span data-ttu-id="86657-481">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="86657-481">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="86657-482">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86657-482">Az.Sql</span></span>
* <span data-ttu-id="86657-483">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="86657-483">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="86657-484">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="86657-484">Az.Storage</span></span>
* <span data-ttu-id="86657-485">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="86657-485">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="86657-486">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="86657-486">New-AzStorageContext</span></span>
* <span data-ttu-id="86657-487">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="86657-487">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="86657-488">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="86657-488">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="86657-489">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="86657-489">Az.Websites</span></span>
* <span data-ttu-id="86657-490">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="86657-490">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="86657-491">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="86657-491">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="86657-492">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="86657-492">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="86657-493">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="86657-493">General</span></span>

- <span data-ttu-id="86657-494">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="86657-494">General Availability of Az Module</span></span>
- <span data-ttu-id="86657-495">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="86657-495">Online help for each module</span></span>
- <span data-ttu-id="86657-496">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="86657-496">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="86657-497">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="86657-497">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="86657-498">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="86657-498">Az.Accounts</span></span>
- <span data-ttu-id="86657-499">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="86657-499">Changed from Az.Profile</span></span>
- <span data-ttu-id="86657-500">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="86657-500">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="86657-501">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="86657-501">Az.ApiManagement</span></span>
- <span data-ttu-id="86657-502">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="86657-502">Fixes for #7002</span></span>
- <span data-ttu-id="86657-503">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="86657-503">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="86657-504">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="86657-504">Az.Batch</span></span>
- <span data-ttu-id="86657-505">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="86657-505">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="86657-506">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="86657-506">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="86657-507">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="86657-507">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="86657-508">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="86657-508">Az.Billing</span></span>
- <span data-ttu-id="86657-509">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="86657-509">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="86657-510">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="86657-510">Az.CognitivServices</span></span>
- <span data-ttu-id="86657-511">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="86657-511">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="86657-512">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="86657-512">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="86657-513">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="86657-513">Az.ContainerInstance</span></span>
- <span data-ttu-id="86657-514">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="86657-514">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="86657-515">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="86657-515">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="86657-516">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="86657-516">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="86657-517">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="86657-517">Az.DataLakeStore</span></span>
- <span data-ttu-id="86657-518">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="86657-518">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="86657-519">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="86657-519">Az.Monitor</span></span>
- <span data-ttu-id="86657-520">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="86657-520">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="86657-521">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="86657-521">Az.KeyVault</span></span>
- <span data-ttu-id="86657-522">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="86657-522">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="86657-523">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="86657-523">Az.MachineLearning</span></span>
- <span data-ttu-id="86657-524">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="86657-524">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="86657-525">Az.Media</span><span class="sxs-lookup"><span data-stu-id="86657-525">Az.Media</span></span>
- <span data-ttu-id="86657-526">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="86657-526">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="86657-527">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86657-527">Az.Network</span></span>
<span data-ttu-id="86657-528">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="86657-528">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="86657-529">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="86657-529">New cmdlets added:</span></span>
        - <span data-ttu-id="86657-530">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="86657-530">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="86657-531">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="86657-531">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="86657-532">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="86657-532">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="86657-533">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="86657-533">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="86657-534">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="86657-534">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="86657-535">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="86657-535">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="86657-536">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="86657-536">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="86657-537">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="86657-537">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="86657-538">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="86657-538">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="86657-539">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="86657-539">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="86657-540">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="86657-540">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="86657-541">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="86657-541">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="86657-542">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="86657-542">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="86657-543">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="86657-543">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="86657-544">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="86657-544">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="86657-545">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="86657-545">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="86657-546">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="86657-546">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="86657-547">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="86657-547">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="86657-548">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="86657-548">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="86657-549">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="86657-549">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="86657-550">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="86657-550">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="86657-551">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="86657-551">Az.OperationalInsights</span></span>
- <span data-ttu-id="86657-552">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="86657-552">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="86657-553">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="86657-553">Az.Profile</span></span>
- <span data-ttu-id="86657-554">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="86657-554">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="86657-555">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="86657-555">Az.RecoveryServices</span></span>
- <span data-ttu-id="86657-556">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="86657-556">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="86657-557">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86657-557">Az.Resources</span></span>
- <span data-ttu-id="86657-558">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="86657-558">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="86657-559">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="86657-559">Az.ServiceFabric</span></span>
- <span data-ttu-id="86657-560">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="86657-560">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="86657-561">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="86657-561">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="86657-562">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="86657-562">Az.SIgnalR</span></span>
- <span data-ttu-id="86657-563">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="86657-563">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="86657-564">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86657-564">Az.Sql</span></span>
- <span data-ttu-id="86657-565">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="86657-565">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="86657-566">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="86657-566">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="86657-567">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="86657-567">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="86657-568">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="86657-568">Az.Storage</span></span>
- <span data-ttu-id="86657-569">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="86657-569">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="86657-570">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="86657-570">Az.Websites</span></span>
- <span data-ttu-id="86657-571">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="86657-571">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="86657-572">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="86657-572">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="86657-573">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="86657-573">General</span></span>

* <span data-ttu-id="86657-574">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="86657-574">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="86657-575">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86657-575">Az.Compute</span></span>

* <span data-ttu-id="86657-576">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="86657-576">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="86657-577">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="86657-577">Az.DataLakeStore</span></span>

* <span data-ttu-id="86657-578">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="86657-578">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="86657-579">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="86657-579">Az.FrontDoor</span></span>

* <span data-ttu-id="86657-580">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="86657-580">Fixed some broken links</span></span>
    - <span data-ttu-id="86657-581">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="86657-581">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="86657-582">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="86657-582">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="86657-583">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="86657-583">Az.RecoveryServices</span></span>

* <span data-ttu-id="86657-584">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="86657-584">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="86657-585">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="86657-585">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="86657-586">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86657-586">Az.Resources</span></span>

* <span data-ttu-id="86657-587">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="86657-587">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="86657-588">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="86657-588">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="86657-589">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86657-589">Az.Sql</span></span>

* <span data-ttu-id="86657-590">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="86657-590">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="86657-591">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="86657-591">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="86657-592">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="86657-592">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="86657-593">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="86657-593">Az.Storage</span></span>

* <span data-ttu-id="86657-594">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="86657-594">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="86657-595">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="86657-595">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="86657-596">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="86657-596">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="86657-597">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="86657-597">Support Static Website configuration</span></span>
    - <span data-ttu-id="86657-598">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="86657-598">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="86657-599">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="86657-599">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="86657-600">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="86657-600">Az.Websites</span></span>

* <span data-ttu-id="86657-601">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="86657-601">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="86657-602">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="86657-602">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="86657-603">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="86657-603">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="86657-604">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="86657-604">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="86657-605">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="86657-605">Az.ApiManagement</span></span>
* <span data-ttu-id="86657-606">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="86657-606">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="86657-607">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="86657-607">Az.Automation</span></span>
* <span data-ttu-id="86657-608">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="86657-608">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="86657-609">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="86657-609">Added Update Management cmdlets</span></span>
* <span data-ttu-id="86657-610">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="86657-610">Added Source Control cmdlets</span></span>
* <span data-ttu-id="86657-611">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="86657-611">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="86657-612">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="86657-612">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="86657-613">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86657-613">Az.Compute</span></span>
* <span data-ttu-id="86657-614">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="86657-614">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="86657-615">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="86657-615">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="86657-616">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="86657-616">Az.ContainerInstance</span></span>
* <span data-ttu-id="86657-617">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="86657-617">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="86657-618">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="86657-618">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="86657-619">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="86657-619">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="86657-620">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86657-620">Az.Network</span></span>
* <span data-ttu-id="86657-621">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="86657-621">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="86657-622">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="86657-622">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="86657-623">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="86657-623">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="86657-624">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="86657-624">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="86657-625">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="86657-625">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="86657-626">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="86657-626">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="86657-627">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="86657-627">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="86657-628">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="86657-628">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="86657-629">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="86657-629">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="86657-630">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="86657-630">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="86657-631">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="86657-631">Az.Relay</span></span>
* <span data-ttu-id="86657-632">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="86657-632">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="86657-633">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86657-633">Az.Resources</span></span>
* <span data-ttu-id="86657-634">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="86657-634">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="86657-635">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="86657-635">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="86657-636">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="86657-636">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="86657-637">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="86657-637">Az.ServiceFabric</span></span>
* <span data-ttu-id="86657-638">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="86657-638">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="86657-639">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86657-639">Az.Sql</span></span>
* <span data-ttu-id="86657-640">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="86657-640">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="86657-641">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="86657-641">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="86657-642">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="86657-642">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="86657-643">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="86657-643">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="86657-644">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="86657-644">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="86657-645">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="86657-645">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="86657-646">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="86657-646">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="86657-647">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="86657-647">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="86657-648">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="86657-648">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="86657-649">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="86657-649">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="86657-650">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="86657-650">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="86657-651">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="86657-651">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="86657-652">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="86657-652">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="86657-653">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="86657-653">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="86657-654">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="86657-654">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="86657-655">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="86657-655">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="86657-656">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="86657-656">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="86657-657">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="86657-657">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="86657-658">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="86657-658">General</span></span>
* <span data-ttu-id="86657-659">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="86657-659">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="86657-660">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="86657-660">Az.Profile</span></span>
* <span data-ttu-id="86657-661">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="86657-661">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="86657-662">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="86657-662">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="86657-663">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="86657-663">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="86657-664">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="86657-664">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="86657-665">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="86657-665">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="86657-666">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="86657-666">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="86657-667">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="86657-667">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="86657-668">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="86657-668">Az.CognitiveServices</span></span>
* <span data-ttu-id="86657-669">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="86657-669">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86657-670">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86657-670">Az.Compute</span></span>
* <span data-ttu-id="86657-671">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="86657-671">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="86657-672">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="86657-672">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="86657-673">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="86657-673">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="86657-674">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="86657-674">Az.DataLakeStore</span></span>
* <span data-ttu-id="86657-675">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="86657-675">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="86657-676">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="86657-676">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="86657-677">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="86657-677">Az.Insights</span></span>
* <span data-ttu-id="86657-678">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="86657-678">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="86657-679">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="86657-679">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="86657-680">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="86657-680">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="86657-681">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="86657-681">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="86657-682">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86657-682">Az.Network</span></span>
* <span data-ttu-id="86657-683">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="86657-683">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="86657-684">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="86657-684">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="86657-685">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="86657-685">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="86657-686">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="86657-686">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="86657-687">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="86657-687">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="86657-688">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="86657-688">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="86657-689">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="86657-689">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="86657-690">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="86657-690">Az.PolicyInsights</span></span>
* <span data-ttu-id="86657-691">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="86657-691">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="86657-692">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86657-692">Az.Resources</span></span>
* <span data-ttu-id="86657-693">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="86657-693">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="86657-694">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="86657-694">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="86657-695">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="86657-695">Az.ServiceBus</span></span>
* <span data-ttu-id="86657-696">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="86657-696">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="86657-697">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="86657-697">Az.ServiceFabric</span></span>
* <span data-ttu-id="86657-698">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="86657-698">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="86657-699">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="86657-699">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="86657-700">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="86657-700">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="86657-701">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="86657-701">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="86657-702">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="86657-702">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="86657-703">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="86657-703">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="86657-704">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="86657-704">Az.Profile</span></span>
* <span data-ttu-id="86657-705">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="86657-705">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="86657-706">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="86657-706">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86657-707">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86657-707">Az.Compute</span></span>
* <span data-ttu-id="86657-708">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="86657-708">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="86657-709">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="86657-709">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="86657-710">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="86657-710">Az.DataLakeStore</span></span>
* <span data-ttu-id="86657-711">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="86657-711">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="86657-712">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="86657-712">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="86657-713">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="86657-713">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="86657-714">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="86657-714">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="86657-715">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="86657-715">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="86657-716">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86657-716">Az.Network</span></span>
* <span data-ttu-id="86657-717">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="86657-717">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="86657-718">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="86657-718">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="86657-719">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86657-719">Az.Resources</span></span>
* <span data-ttu-id="86657-720">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="86657-720">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="86657-721">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="86657-721">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="86657-722">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="86657-722">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="86657-723">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="86657-723">Azure.Storage</span></span>
* <span data-ttu-id="86657-724">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="86657-724">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="86657-725">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="86657-725">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="86657-726">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="86657-726">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="86657-727">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="86657-727">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="86657-728">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="86657-728">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="86657-729">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="86657-729">Az.CognitiveServices</span></span>
* <span data-ttu-id="86657-730">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="86657-730">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86657-731">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86657-731">Az.Compute</span></span>
* <span data-ttu-id="86657-732">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="86657-732">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="86657-733">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="86657-733">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="86657-734">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="86657-734">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="86657-735">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="86657-735">Az.DataFactoryV2</span></span>
* <span data-ttu-id="86657-736">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="86657-736">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="86657-737">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86657-737">Az.Network</span></span>
* <span data-ttu-id="86657-738">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="86657-738">Added NetworkProfile functionality.</span></span> <span data-ttu-id="86657-739">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="86657-739">new cmdlets added</span></span>
    - <span data-ttu-id="86657-740">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="86657-740">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="86657-741">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="86657-741">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="86657-742">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="86657-742">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="86657-743">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="86657-743">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="86657-744">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="86657-744">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="86657-745">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="86657-745">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="86657-746">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="86657-746">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="86657-747">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="86657-747">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="86657-748">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="86657-748">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="86657-749">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="86657-749">Az.RedisCache</span></span>
* <span data-ttu-id="86657-750">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="86657-750">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="86657-751">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="86657-751">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="86657-752">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86657-752">Az.Resources</span></span>
* <span data-ttu-id="86657-753">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="86657-753">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="86657-754">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="86657-754">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="86657-755">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86657-755">Az.Sql</span></span>
* <span data-ttu-id="86657-756">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="86657-756">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="86657-757">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="86657-757">Az.Websites</span></span>
* <span data-ttu-id="86657-758">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="86657-758">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="86657-759">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="86657-759">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="86657-760">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="86657-760">0.2.0 - September 2018</span></span>
 <span data-ttu-id="86657-761">Начальный выпуск</span><span class="sxs-lookup"><span data-stu-id="86657-761">Initial Release</span></span>
