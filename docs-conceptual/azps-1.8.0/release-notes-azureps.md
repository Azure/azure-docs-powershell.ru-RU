---
title: Заметки о выпуске Azure PowerShell
description: Узнайте обо всех последних обновлениях модулей Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/30/2019
ms.openlocfilehash: 287e9e1f066d0768e7f572ca7f5f2ee2b78931d9
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "83386975"
---
## <a name="180---april-2019"></a><span data-ttu-id="4467d-103">1.8.0 — апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="4467d-103">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="4467d-104">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="4467d-104">Highlights since the last major release</span></span>
* <span data-ttu-id="4467d-105">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="4467d-105">General availability of `Az` module</span></span>
* <span data-ttu-id="4467d-106">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="4467d-106">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="4467d-107">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="4467d-107">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="4467d-108">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="4467d-108">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="4467d-109">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="4467d-109">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="4467d-110">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="4467d-110">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="4467d-111">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="4467d-111">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4467d-112">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4467d-112">Az.Accounts</span></span>
* <span data-ttu-id="4467d-113">Обновлен командлет Uninstall-AzureRm для правильного удаления модулей в Mac.</span><span class="sxs-lookup"><span data-stu-id="4467d-113">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="4467d-114">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4467d-114">Az.Batch</span></span>
* <span data-ttu-id="4467d-115">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="4467d-115">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4467d-116">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4467d-116">Az.Cdn</span></span>
* <span data-ttu-id="4467d-117">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="4467d-117">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4467d-118">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4467d-118">Az.CognitiveServices</span></span>
* <span data-ttu-id="4467d-119">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="4467d-119">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4467d-120">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4467d-120">Az.Compute</span></span>
* <span data-ttu-id="4467d-121">Устранена проблема с установкой AEM, если в идентификаторах ресурсов дисков группа ресурсов указана в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="4467d-121">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="4467d-122">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="4467d-122">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4467d-123">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="4467d-123">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4467d-124">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4467d-124">Az.DataFactory</span></span>
* <span data-ttu-id="4467d-125">Добавлены свойства SsisProperties, если NodeCount не имеет значения NULL для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="4467d-125">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4467d-126">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4467d-126">Az.DataLakeStore</span></span>
* <span data-ttu-id="4467d-127">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="4467d-127">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="4467d-128">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="4467d-128">Az.EventGrid</span></span>
* <span data-ttu-id="4467d-129">Обновлен текст справки для конечной точки, указывающий, что необходимо создать ресурсы, прежде чем использовать командлеты для создания или обновления подписки на события.</span><span class="sxs-lookup"><span data-stu-id="4467d-129">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4467d-130">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4467d-130">Az.EventHub</span></span>
* <span data-ttu-id="4467d-131">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="4467d-131">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="4467d-132">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4467d-132">Az.HDInsight</span></span>
* <span data-ttu-id="4467d-133">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="4467d-133">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4467d-134">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4467d-134">Az.IotHub</span></span>
* <span data-ttu-id="4467d-135">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="4467d-135">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4467d-136">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4467d-136">Az.KeyVault</span></span>
* <span data-ttu-id="4467d-137">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="4467d-137">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4467d-138">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="4467d-138">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="4467d-139">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="4467d-139">Az.MachineLearning</span></span>
* <span data-ttu-id="4467d-140">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="4467d-140">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="4467d-141">Az.Media</span><span class="sxs-lookup"><span data-stu-id="4467d-141">Az.Media</span></span>
* <span data-ttu-id="4467d-142">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="4467d-142">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4467d-143">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4467d-143">Az.Monitor</span></span>
  * <span data-ttu-id="4467d-144">Добавлены новые командлеты для правила генерации оповещений на основе метрик GenV2 (не классических).</span><span class="sxs-lookup"><span data-stu-id="4467d-144">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="4467d-145">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="4467d-145">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="4467d-146">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="4467d-146">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="4467d-147">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="4467d-147">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="4467d-148">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="4467d-148">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="4467d-149">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="4467d-149">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="4467d-150">Обновлен пакет SDK Monitor до предварительной версии 0.22.0.</span><span class="sxs-lookup"><span data-stu-id="4467d-150">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4467d-151">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4467d-151">Az.Network</span></span>
* <span data-ttu-id="4467d-152">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="4467d-152">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4467d-153">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="4467d-153">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="4467d-154">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="4467d-154">Az.NotificationHubs</span></span>
* <span data-ttu-id="4467d-155">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="4467d-155">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4467d-156">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4467d-156">Az.OperationalInsights</span></span>
* <span data-ttu-id="4467d-157">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="4467d-157">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="4467d-158">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="4467d-158">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="4467d-159">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="4467d-159">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4467d-160">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4467d-160">Az.RecoveryServices</span></span>
* <span data-ttu-id="4467d-161">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="4467d-161">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4467d-162">Обновлен табличный формат для SQL на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="4467d-162">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="4467d-163">Добавлен альтернативный метод для получения расположения в Общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="4467d-163">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="4467d-164">Обновлено значение ScheduleRunDays в объекте SchedulePolicy в соответствии с часовым поясом.</span><span class="sxs-lookup"><span data-stu-id="4467d-164">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="4467d-165">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="4467d-165">Az.RedisCache</span></span>
* <span data-ttu-id="4467d-166">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="4467d-166">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4467d-167">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4467d-167">Az.Resources</span></span>
* <span data-ttu-id="4467d-168">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="4467d-168">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="4467d-169">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4467d-169">Az.Sql</span></span>
* <span data-ttu-id="4467d-170">Заменена зависимость от пакета SDK монитора на обычный код.</span><span class="sxs-lookup"><span data-stu-id="4467d-170">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="4467d-171">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="4467d-171">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4467d-172">Улучшен процесс классификации нескольких столбцов.</span><span class="sxs-lookup"><span data-stu-id="4467d-172">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="4467d-173">Добавлены свойства SKU (имя, семейство, производительность SKU) в отклике Get-AzSqlServerServiceObjective, а также по умолчанию задан табличный формат.</span><span class="sxs-lookup"><span data-stu-id="4467d-173">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="4467d-174">C помощью Get-AzSqlServerServiceObjective теперь можно получать список доступных целевых служб по расположению без необходимости заранее размещать сервер в регионе.</span><span class="sxs-lookup"><span data-stu-id="4467d-174">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="4467d-175">Поддерживается параметр часового пояса при создании Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="4467d-175">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="4467d-176">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="4467d-176">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4467d-177">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4467d-177">Az.Websites</span></span>
* <span data-ttu-id="4467d-178">Исправлены командлеты Set-AzWebApp и Set-AzWebAppSlot, которые теперь не удаляют теги при выполнении.</span><span class="sxs-lookup"><span data-stu-id="4467d-178">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="4467d-179">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="4467d-179">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4467d-180">Обновлен пакет SDK веб-узлов.</span><span class="sxs-lookup"><span data-stu-id="4467d-180">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="4467d-181">Удалено свойство AdminSiteName из PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="4467d-181">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="4467d-182">1.7.0 —апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="4467d-182">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="4467d-183">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="4467d-183">Highlights since the last major release</span></span>
* <span data-ttu-id="4467d-184">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="4467d-184">General availability of `Az` module</span></span>
* <span data-ttu-id="4467d-185">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="4467d-185">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="4467d-186">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="4467d-186">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="4467d-187">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="4467d-187">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="4467d-188">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="4467d-188">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="4467d-189">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="4467d-189">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="4467d-190">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="4467d-190">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4467d-191">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4467d-191">Az.Accounts</span></span>
* <span data-ttu-id="4467d-192">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметр AzureAnalysisServicesEndpointResourceId.</span><span class="sxs-lookup"><span data-stu-id="4467d-192">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="4467d-193">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4467d-193">Az.AnalysisServices</span></span>
* <span data-ttu-id="4467d-194">Использование ServiceClient в командлетах плоскости данных и удаление исходной логики проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="4467d-194">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="4467d-195">Add-AzureASAccount используется как оболочка для Connect-AzAccount во избежание критических изменений.</span><span class="sxs-lookup"><span data-stu-id="4467d-195">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4467d-196">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4467d-196">Az.Automation</span></span>
* <span data-ttu-id="4467d-197">Исправлена ошибка командлета New-AzAutomationSoftwareUpdateConfiguration, связанная с включением.</span><span class="sxs-lookup"><span data-stu-id="4467d-197">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="4467d-198">Теперь параметры IncludedKbNumber и IncludedPackageNameMask должны работать нормально.</span><span class="sxs-lookup"><span data-stu-id="4467d-198">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="4467d-199">Исправлена ошибка динамической группы управления обновлениями службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="4467d-199">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4467d-200">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4467d-200">Az.Compute</span></span>
* <span data-ttu-id="4467d-201">В командлеты New-AzDiskConfig и New-AzSnapshotConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="4467d-201">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="4467d-202">Теперь можно создавать виртуальные машину на основе образов из коллекции от других клиентов.</span><span class="sxs-lookup"><span data-stu-id="4467d-202">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="4467d-203">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="4467d-203">Az.ContainerInstance</span></span>
* <span data-ttu-id="4467d-204">Исправлена проблема в параметре -Command командлета New-AzContainerGroup, из-за которой в конце добавлялся пустой аргумент.</span><span class="sxs-lookup"><span data-stu-id="4467d-204">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4467d-205">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4467d-205">Az.DataFactory</span></span>
* <span data-ttu-id="4467d-206">Пакет SDK для ADF .NET обновлен до версии 3.0.2.</span><span class="sxs-lookup"><span data-stu-id="4467d-206">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="4467d-207">Командлет Set-AzDataFactoryV2 обновлен с помощью дополнительных параметров для настроек, связанных с RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4467d-207">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4467d-208">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4467d-208">Az.Resources</span></span>
* <span data-ttu-id="4467d-209">Улучшена обработка поставщиков Get-AzResource при предоставлении параметров -ResourceId или -ResourceGroupName, -Name и -ResourceType.</span><span class="sxs-lookup"><span data-stu-id="4467d-209">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="4467d-210">Улучшена обработка ошибок в командлетах Test-AzDeployment и Test-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="4467d-210">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="4467d-211">Теперь ошибки, возникающие за пределами проверки развертывания, обрабатываются и включаются в выходные данные команды.</span><span class="sxs-lookup"><span data-stu-id="4467d-211">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="4467d-212">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="4467d-212">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="4467d-213">Добавлен параметр-переключатель -IgnoreDynamicParameters, с помощью которого можно настроить командлеты развертывания так, чтобы они пропускали запросы в сценариях скриптов и заданий.</span><span class="sxs-lookup"><span data-stu-id="4467d-213">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="4467d-214">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="4467d-214">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="4467d-215">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4467d-215">Az.Sql</span></span>
* <span data-ttu-id="4467d-216">Поддержка классификации данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="4467d-216">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4467d-217">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4467d-217">Az.Storage</span></span>
* <span data-ttu-id="4467d-218">Подробные сообщения об ошибке передаются при создании контекста хранилища с помощью параметра -UseConnectedAccount, но без входа в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="4467d-218">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="4467d-219">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="4467d-219">New-AzStorageContext</span></span>
* <span data-ttu-id="4467d-220">Поддержка свойств службы управления BLOB-объектов в указанной учетной записи хранения с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="4467d-220">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="4467d-221">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="4467d-221">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="4467d-222">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="4467d-222">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="4467d-223">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4467d-223">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="4467d-224">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4467d-224">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="4467d-225">Поддержка параметра -AsJob в командлетах для отправки и скачивания больших двоичных объектов и файлов.</span><span class="sxs-lookup"><span data-stu-id="4467d-225">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="4467d-226">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="4467d-226">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="4467d-227">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="4467d-227">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="4467d-228">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="4467d-228">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="4467d-229">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="4467d-229">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="4467d-230">1.6.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="4467d-230">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="4467d-231">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="4467d-231">Highlights since the last major release</span></span>
* <span data-ttu-id="4467d-232">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="4467d-232">General availability of `Az` module</span></span>
* <span data-ttu-id="4467d-233">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="4467d-233">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="4467d-234">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="4467d-234">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="4467d-235">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="4467d-235">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="4467d-236">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="4467d-236">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="4467d-237">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="4467d-237">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="4467d-238">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="4467d-238">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4467d-239">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4467d-239">Az.Automation</span></span>
* <span data-ttu-id="4467d-240">В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:</span><span class="sxs-lookup"><span data-stu-id="4467d-240">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="4467d-241">динамическое группирование;</span><span class="sxs-lookup"><span data-stu-id="4467d-241">Dynamic grouping</span></span>
    * <span data-ttu-id="4467d-242">скрипты предварительного или последующего выполнения;</span><span class="sxs-lookup"><span data-stu-id="4467d-242">Pre-Post script</span></span>
    * <span data-ttu-id="4467d-243">параметр перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="4467d-243">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4467d-244">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4467d-244">Az.Compute</span></span>
* <span data-ttu-id="4467d-245">Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.</span><span class="sxs-lookup"><span data-stu-id="4467d-245">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="4467d-246">Обновление клиентской библиотеки вычислений до версии 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="4467d-246">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4467d-247">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4467d-247">Az.KeyVault</span></span>
* <span data-ttu-id="4467d-248">Добавлена поддержка подстановочных знаков в командлетах KeyVault.</span><span class="sxs-lookup"><span data-stu-id="4467d-248">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4467d-249">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4467d-249">Az.Network</span></span>
* <span data-ttu-id="4467d-250">Добавлена поддержка анализа угроз для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="4467d-250">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="4467d-251">Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="4467d-251">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4467d-252">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4467d-252">Az.RecoveryServices</span></span>
* <span data-ttu-id="4467d-253">В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.</span><span class="sxs-lookup"><span data-stu-id="4467d-253">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="4467d-254">Добавлена поддержка канала для отмены регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="4467d-254">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="4467d-255">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4467d-255">Az.Resources</span></span>
* <span data-ttu-id="4467d-256">Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="4467d-256">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="4467d-257">Обновлены учетные данные, используемые при общих вызовах к ARM.</span><span class="sxs-lookup"><span data-stu-id="4467d-257">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="4467d-258">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4467d-258">Az.Sql</span></span>
* <span data-ttu-id="4467d-259">Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="4467d-259">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4467d-260">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4467d-260">Az.Storage</span></span>
* <span data-ttu-id="4467d-261">Поддержка получения, настройки и удаления политики управления в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="4467d-261">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="4467d-262">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="4467d-262">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="4467d-263">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="4467d-263">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="4467d-264">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="4467d-264">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="4467d-265">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="4467d-265">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="4467d-266">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="4467d-266">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="4467d-267">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="4467d-267">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4467d-268">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4467d-268">Az.Websites</span></span>
* <span data-ttu-id="4467d-269">Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="4467d-269">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="4467d-270">1.5.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="4467d-270">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4467d-271">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4467d-271">Az.Accounts</span></span>
* <span data-ttu-id="4467d-272">Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.</span><span class="sxs-lookup"><span data-stu-id="4467d-272">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="4467d-273">Обновлены примеры для Connect AzAccount.</span><span class="sxs-lookup"><span data-stu-id="4467d-273">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4467d-274">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4467d-274">Az.Automation</span></span>
* <span data-ttu-id="4467d-275">Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="4467d-275">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="4467d-276">Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов.</span><span class="sxs-lookup"><span data-stu-id="4467d-276">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="4467d-277">Теперь он возвращает все узлы.</span><span class="sxs-lookup"><span data-stu-id="4467d-277">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4467d-278">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4467d-278">Az.Cdn</span></span>
* <span data-ttu-id="4467d-279">Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.</span><span class="sxs-lookup"><span data-stu-id="4467d-279">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4467d-280">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4467d-280">Az.Compute</span></span>
* <span data-ttu-id="4467d-281">Добавлена поддержка подстановочных знаков в командлетах Get.</span><span class="sxs-lookup"><span data-stu-id="4467d-281">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4467d-282">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4467d-282">Az.DataFactory</span></span>
* <span data-ttu-id="4467d-283">Обновлен пакет SDK для ADF .NET до версии 3.0.1.</span><span class="sxs-lookup"><span data-stu-id="4467d-283">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="4467d-284">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="4467d-284">Az.LogicApp</span></span>
* <span data-ttu-id="4467d-285">Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.</span><span class="sxs-lookup"><span data-stu-id="4467d-285">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4467d-286">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4467d-286">Az.Network</span></span>
* <span data-ttu-id="4467d-287">Добавлена поддержка подстановочных знаков в командлетах Network.</span><span class="sxs-lookup"><span data-stu-id="4467d-287">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4467d-288">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4467d-288">Az.RecoveryServices</span></span>
* <span data-ttu-id="4467d-289">Добавлена поддержка SQL Server на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="4467d-289">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="4467d-290">Обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="4467d-290">SDK Update</span></span>
* <span data-ttu-id="4467d-291">Удалена проверка VMappContainer в Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="4467d-291">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="4467d-292">Добавлены параметры Name и ServerName для Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="4467d-292">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="4467d-293">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4467d-293">Az.Resources</span></span>
* <span data-ttu-id="4467d-294">Добавлен параметр `-TemplateObject` в командлеты для развертывания.</span><span class="sxs-lookup"><span data-stu-id="4467d-294">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="4467d-295">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.</span><span class="sxs-lookup"><span data-stu-id="4467d-295">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="4467d-296">Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="4467d-296">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="4467d-297">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.</span><span class="sxs-lookup"><span data-stu-id="4467d-297">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="4467d-298">Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="4467d-298">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="4467d-299">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.</span><span class="sxs-lookup"><span data-stu-id="4467d-299">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="4467d-300">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4467d-300">Az.Sql</span></span>
* <span data-ttu-id="4467d-301">Обновление AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="4467d-301">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="4467d-302">Исправлено поведение для пограничного случая при создании параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="4467d-302">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4467d-303">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4467d-303">Az.Storage</span></span>
* <span data-ttu-id="4467d-304">Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="4467d-304">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="4467d-305">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="4467d-305">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="4467d-306">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4467d-306">Az.AnalysisServices</span></span>
* <span data-ttu-id="4467d-307">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="4467d-307">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4467d-308">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4467d-308">Az.Automation</span></span>
* <span data-ttu-id="4467d-309">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4467d-309">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="4467d-310">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4467d-310">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="4467d-311">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4467d-311">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4467d-312">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4467d-312">Az.CognitiveServices</span></span>
* <span data-ttu-id="4467d-313">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="4467d-313">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4467d-314">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4467d-314">Az.Compute</span></span>
* <span data-ttu-id="4467d-315">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="4467d-315">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="4467d-316">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="4467d-316">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="4467d-317">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="4467d-317">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="4467d-318">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="4467d-318">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4467d-319">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4467d-319">Az.DataLakeStore</span></span>
* <span data-ttu-id="4467d-320">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="4467d-320">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4467d-321">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4467d-321">Az.EventHub</span></span>
* <span data-ttu-id="4467d-322">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="4467d-322">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="4467d-323">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4467d-323">Az.KeyVault</span></span>
* <span data-ttu-id="4467d-324">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="4467d-324">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="4467d-325">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="4467d-325">Az.LogicApp</span></span>
* <span data-ttu-id="4467d-326">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="4467d-326">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="4467d-327">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="4467d-327">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="4467d-328">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="4467d-328">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="4467d-329">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="4467d-329">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="4467d-330">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="4467d-330">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="4467d-331">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="4467d-331">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="4467d-332">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="4467d-332">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="4467d-333">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="4467d-333">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="4467d-334">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="4467d-334">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="4467d-335">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="4467d-335">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="4467d-336">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="4467d-336">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="4467d-337">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4467d-337">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="4467d-338">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="4467d-338">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4467d-339">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4467d-339">Az.Monitor</span></span>
* <span data-ttu-id="4467d-340">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="4467d-340">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4467d-341">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4467d-341">Az.Network</span></span>
* <span data-ttu-id="4467d-342">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="4467d-342">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4467d-343">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4467d-343">Az.OperationalInsights</span></span>
* <span data-ttu-id="4467d-344">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="4467d-344">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="4467d-345">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="4467d-345">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="4467d-346">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="4467d-346">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="4467d-347">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4467d-347">Az.Resources</span></span>
* <span data-ttu-id="4467d-348">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="4467d-348">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="4467d-349">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="4467d-349">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="4467d-350">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="4467d-350">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="4467d-351">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="4467d-351">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="4467d-352">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4467d-352">Az.Sql</span></span>
* <span data-ttu-id="4467d-353">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="4467d-353">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="4467d-354">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="4467d-354">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4467d-355">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4467d-355">Az.Websites</span></span>
* <span data-ttu-id="4467d-356">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="4467d-356">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="4467d-357">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="4467d-357">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4467d-358">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4467d-358">Az.Accounts</span></span>
* <span data-ttu-id="4467d-359">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="4467d-359">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="4467d-360">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4467d-360">Az.AnalysisServices</span></span>
<span data-ttu-id="4467d-361">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="4467d-361">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4467d-362">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4467d-362">Az.Compute</span></span>
* <span data-ttu-id="4467d-363">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="4467d-363">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="4467d-364">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="4467d-364">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="4467d-365">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="4467d-365">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4467d-366">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4467d-366">Az.RecoveryServices</span></span>
<span data-ttu-id="4467d-367">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="4467d-367">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4467d-368">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4467d-368">Az.Resources</span></span>
* <span data-ttu-id="4467d-369">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4467d-369">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="4467d-370">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="4467d-370">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="4467d-371">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="4467d-371">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="4467d-372">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="4467d-372">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="4467d-373">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4467d-373">Az.Sql</span></span>
* <span data-ttu-id="4467d-374">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="4467d-374">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="4467d-375">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="4467d-375">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="4467d-376">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="4467d-376">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="4467d-377">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="4467d-377">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4467d-378">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4467d-378">Az.Accounts</span></span>
* <span data-ttu-id="4467d-379">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="4467d-379">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="4467d-380">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4467d-380">Az.AnalysisServices</span></span>
* <span data-ttu-id="4467d-381">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="4467d-381">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4467d-382">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4467d-382">Az.RecoveryServices</span></span>
* <span data-ttu-id="4467d-383">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="4467d-383">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="4467d-384">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="4467d-384">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4467d-385">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4467d-385">Az.Accounts</span></span>
* <span data-ttu-id="4467d-386">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="4467d-386">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="4467d-387">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="4467d-387">Update incorrect online help URLs</span></span>
* <span data-ttu-id="4467d-388">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="4467d-388">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="4467d-389">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="4467d-389">Az.Aks</span></span>
* <span data-ttu-id="4467d-390">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="4467d-390">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4467d-391">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4467d-391">Az.Automation</span></span>
* <span data-ttu-id="4467d-392">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="4467d-392">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="4467d-393">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="4467d-393">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4467d-394">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4467d-394">Az.Cdn</span></span>
* <span data-ttu-id="4467d-395">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="4467d-395">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4467d-396">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4467d-396">Az.Compute</span></span>
* <span data-ttu-id="4467d-397">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="4467d-397">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="4467d-398">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="4467d-398">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="4467d-399">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="4467d-399">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="4467d-400">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="4467d-400">Az.ContainerRegistry</span></span>
* <span data-ttu-id="4467d-401">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="4467d-401">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4467d-402">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4467d-402">Az.DataFactory</span></span>
* <span data-ttu-id="4467d-403">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="4467d-403">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4467d-404">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4467d-404">Az.DataLakeStore</span></span>
* <span data-ttu-id="4467d-405">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="4467d-405">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="4467d-406">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="4467d-406">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="4467d-407">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="4467d-407">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4467d-408">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4467d-408">Az.IotHub</span></span>
* <span data-ttu-id="4467d-409">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="4467d-409">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4467d-410">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4467d-410">Az.KeyVault</span></span>
* <span data-ttu-id="4467d-411">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="4467d-411">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4467d-412">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4467d-412">Az.Network</span></span>
* <span data-ttu-id="4467d-413">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="4467d-413">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="4467d-414">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4467d-414">Az.Resources</span></span>
* <span data-ttu-id="4467d-415">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="4467d-415">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="4467d-416">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4467d-416">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="4467d-417">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="4467d-417">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="4467d-418">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="4467d-418">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="4467d-419">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="4467d-419">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="4467d-420">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="4467d-420">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="4467d-421">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="4467d-421">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4467d-422">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4467d-422">Az.ServiceFabric</span></span>
* <span data-ttu-id="4467d-423">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="4467d-423">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="4467d-424">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="4467d-424">Fix some error messages.</span></span>
* <span data-ttu-id="4467d-425">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="4467d-425">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="4467d-426">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="4467d-426">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="4467d-427">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="4467d-427">Az.SignalR</span></span>
* <span data-ttu-id="4467d-428">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="4467d-428">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="4467d-429">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4467d-429">Az.Sql</span></span>
* <span data-ttu-id="4467d-430">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="4467d-430">Update incorrect online help URLs</span></span>
* <span data-ttu-id="4467d-431">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="4467d-431">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="4467d-432">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="4467d-432">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="4467d-433">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="4467d-433">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4467d-434">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4467d-434">Az.Storage</span></span>
* <span data-ttu-id="4467d-435">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="4467d-435">Update incorrect online help URLs</span></span>
* <span data-ttu-id="4467d-436">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="4467d-436">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="4467d-437">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="4467d-437">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="4467d-438">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="4467d-438">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="4467d-439">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="4467d-439">Az.TrafficManager</span></span>
* <span data-ttu-id="4467d-440">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="4467d-440">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4467d-441">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4467d-441">Az.Websites</span></span>
* <span data-ttu-id="4467d-442">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="4467d-442">Update incorrect online help URLs</span></span>
* <span data-ttu-id="4467d-443">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="4467d-443">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="4467d-444">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="4467d-444">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="4467d-445">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="4467d-445">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4467d-446">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4467d-446">Az.Accounts</span></span>
* <span data-ttu-id="4467d-447">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="4467d-447">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4467d-448">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4467d-448">Az.Compute</span></span>
* <span data-ttu-id="4467d-449">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="4467d-449">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="4467d-450">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="4467d-450">Updated the description of ID in help files</span></span>
* <span data-ttu-id="4467d-451">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="4467d-451">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4467d-452">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4467d-452">Az.DataLakeStore</span></span>
* <span data-ttu-id="4467d-453">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="4467d-453">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="4467d-454">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="4467d-454">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="4467d-455">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="4467d-455">Az.EventGrid</span></span>
* <span data-ttu-id="4467d-456">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="4467d-456">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="4467d-457">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="4467d-457">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="4467d-458">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="4467d-458">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="4467d-459">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="4467d-459">Event Time-To-Live,</span></span>
        - <span data-ttu-id="4467d-460">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="4467d-460">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="4467d-461">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="4467d-461">Dead letter endpoint.</span></span>
    - <span data-ttu-id="4467d-462">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="4467d-462">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="4467d-463">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="4467d-463">Event Time-To-Live,</span></span>
        - <span data-ttu-id="4467d-464">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="4467d-464">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="4467d-465">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="4467d-465">Dead letter endpoint.</span></span>
* <span data-ttu-id="4467d-466">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="4467d-466">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="4467d-467">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="4467d-467">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4467d-468">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4467d-468">Az.IotHub</span></span>
* <span data-ttu-id="4467d-469">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="4467d-469">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="4467d-470">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="4467d-470">Az.LogicApp</span></span>
* <span data-ttu-id="4467d-471">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="4467d-471">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="4467d-472">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4467d-472">Az.Resources</span></span>
* <span data-ttu-id="4467d-473">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="4467d-473">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="4467d-474">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="4467d-474">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="4467d-475">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="4467d-475">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="4467d-476">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="4467d-476">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="4467d-477">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="4467d-477">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="4467d-478">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="4467d-478">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="4467d-479">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="4467d-479">Az.SignalR</span></span>
* <span data-ttu-id="4467d-480">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="4467d-480">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="4467d-481">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4467d-481">Az.Sql</span></span>
* <span data-ttu-id="4467d-482">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="4467d-482">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4467d-483">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4467d-483">Az.Storage</span></span>
* <span data-ttu-id="4467d-484">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="4467d-484">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="4467d-485">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="4467d-485">New-AzStorageContext</span></span>
* <span data-ttu-id="4467d-486">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="4467d-486">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="4467d-487">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="4467d-487">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4467d-488">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4467d-488">Az.Websites</span></span>
* <span data-ttu-id="4467d-489">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="4467d-489">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="4467d-490">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="4467d-490">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="4467d-491">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="4467d-491">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="4467d-492">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="4467d-492">General</span></span>

- <span data-ttu-id="4467d-493">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="4467d-493">General Availability of Az Module</span></span>
- <span data-ttu-id="4467d-494">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="4467d-494">Online help for each module</span></span>
- <span data-ttu-id="4467d-495">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="4467d-495">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="4467d-496">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="4467d-496">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="4467d-497">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4467d-497">Az.Accounts</span></span>
- <span data-ttu-id="4467d-498">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="4467d-498">Changed from Az.Profile</span></span>
- <span data-ttu-id="4467d-499">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="4467d-499">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="4467d-500">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4467d-500">Az.ApiManagement</span></span>
- <span data-ttu-id="4467d-501">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="4467d-501">Fixes for #7002</span></span>
- <span data-ttu-id="4467d-502">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="4467d-502">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="4467d-503">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4467d-503">Az.Batch</span></span>
- <span data-ttu-id="4467d-504">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="4467d-504">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="4467d-505">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="4467d-505">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="4467d-506">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="4467d-506">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="4467d-507">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="4467d-507">Az.Billing</span></span>
- <span data-ttu-id="4467d-508">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="4467d-508">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="4467d-509">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="4467d-509">Az.CognitivServices</span></span>
- <span data-ttu-id="4467d-510">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="4467d-510">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="4467d-511">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="4467d-511">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="4467d-512">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="4467d-512">Az.ContainerInstance</span></span>
- <span data-ttu-id="4467d-513">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="4467d-513">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="4467d-514">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="4467d-514">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="4467d-515">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="4467d-515">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="4467d-516">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4467d-516">Az.DataLakeStore</span></span>
- <span data-ttu-id="4467d-517">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="4467d-517">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="4467d-518">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4467d-518">Az.Monitor</span></span>
- <span data-ttu-id="4467d-519">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="4467d-519">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="4467d-520">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4467d-520">Az.KeyVault</span></span>
- <span data-ttu-id="4467d-521">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="4467d-521">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="4467d-522">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="4467d-522">Az.MachineLearning</span></span>
- <span data-ttu-id="4467d-523">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="4467d-523">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="4467d-524">Az.Media</span><span class="sxs-lookup"><span data-stu-id="4467d-524">Az.Media</span></span>
- <span data-ttu-id="4467d-525">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="4467d-525">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="4467d-526">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4467d-526">Az.Network</span></span>
<span data-ttu-id="4467d-527">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="4467d-527">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="4467d-528">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="4467d-528">New cmdlets added:</span></span>
        - <span data-ttu-id="4467d-529">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4467d-529">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4467d-530">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4467d-530">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4467d-531">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4467d-531">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4467d-532">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4467d-532">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4467d-533">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4467d-533">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4467d-534">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="4467d-534">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="4467d-535">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="4467d-535">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="4467d-536">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="4467d-536">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="4467d-537">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4467d-537">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="4467d-538">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4467d-538">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="4467d-539">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4467d-539">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="4467d-540">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4467d-540">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="4467d-541">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4467d-541">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="4467d-542">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4467d-542">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="4467d-543">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="4467d-543">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="4467d-544">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="4467d-544">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="4467d-545">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4467d-545">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="4467d-546">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4467d-546">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="4467d-547">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4467d-547">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="4467d-548">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="4467d-548">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="4467d-549">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="4467d-549">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="4467d-550">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4467d-550">Az.OperationalInsights</span></span>
- <span data-ttu-id="4467d-551">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="4467d-551">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="4467d-552">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="4467d-552">Az.Profile</span></span>
- <span data-ttu-id="4467d-553">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="4467d-553">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="4467d-554">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4467d-554">Az.RecoveryServices</span></span>
- <span data-ttu-id="4467d-555">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="4467d-555">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="4467d-556">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4467d-556">Az.Resources</span></span>
- <span data-ttu-id="4467d-557">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="4467d-557">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="4467d-558">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4467d-558">Az.ServiceFabric</span></span>
- <span data-ttu-id="4467d-559">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="4467d-559">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="4467d-560">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="4467d-560">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="4467d-561">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="4467d-561">Az.SIgnalR</span></span>
- <span data-ttu-id="4467d-562">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="4467d-562">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="4467d-563">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4467d-563">Az.Sql</span></span>
- <span data-ttu-id="4467d-564">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="4467d-564">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="4467d-565">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="4467d-565">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="4467d-566">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="4467d-566">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="4467d-567">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4467d-567">Az.Storage</span></span>
- <span data-ttu-id="4467d-568">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="4467d-568">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="4467d-569">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4467d-569">Az.Websites</span></span>
- <span data-ttu-id="4467d-570">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="4467d-570">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="4467d-571">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="4467d-571">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="4467d-572">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="4467d-572">General</span></span>

* <span data-ttu-id="4467d-573">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="4467d-573">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="4467d-574">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4467d-574">Az.Compute</span></span>

* <span data-ttu-id="4467d-575">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="4467d-575">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="4467d-576">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4467d-576">Az.DataLakeStore</span></span>

* <span data-ttu-id="4467d-577">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="4467d-577">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="4467d-578">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4467d-578">Az.FrontDoor</span></span>

* <span data-ttu-id="4467d-579">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="4467d-579">Fixed some broken links</span></span>
    - <span data-ttu-id="4467d-580">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="4467d-580">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="4467d-581">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="4467d-581">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="4467d-582">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4467d-582">Az.RecoveryServices</span></span>

* <span data-ttu-id="4467d-583">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="4467d-583">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="4467d-584">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="4467d-584">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="4467d-585">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4467d-585">Az.Resources</span></span>

* <span data-ttu-id="4467d-586">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="4467d-586">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="4467d-587">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="4467d-587">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="4467d-588">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4467d-588">Az.Sql</span></span>

* <span data-ttu-id="4467d-589">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="4467d-589">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="4467d-590">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="4467d-590">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="4467d-591">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="4467d-591">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="4467d-592">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4467d-592">Az.Storage</span></span>

* <span data-ttu-id="4467d-593">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4467d-593">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="4467d-594">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="4467d-594">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="4467d-595">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="4467d-595">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="4467d-596">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="4467d-596">Support Static Website configuration</span></span>
    - <span data-ttu-id="4467d-597">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="4467d-597">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="4467d-598">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="4467d-598">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="4467d-599">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4467d-599">Az.Websites</span></span>

* <span data-ttu-id="4467d-600">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4467d-600">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="4467d-601">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="4467d-601">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="4467d-602">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4467d-602">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="4467d-603">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="4467d-603">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="4467d-604">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4467d-604">Az.ApiManagement</span></span>
* <span data-ttu-id="4467d-605">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="4467d-605">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="4467d-606">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4467d-606">Az.Automation</span></span>
* <span data-ttu-id="4467d-607">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="4467d-607">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="4467d-608">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="4467d-608">Added Update Management cmdlets</span></span>
* <span data-ttu-id="4467d-609">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="4467d-609">Added Source Control cmdlets</span></span>
* <span data-ttu-id="4467d-610">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="4467d-610">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="4467d-611">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="4467d-611">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="4467d-612">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4467d-612">Az.Compute</span></span>
* <span data-ttu-id="4467d-613">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="4467d-613">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="4467d-614">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="4467d-614">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="4467d-615">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="4467d-615">Az.ContainerInstance</span></span>
* <span data-ttu-id="4467d-616">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="4467d-616">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="4467d-617">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="4467d-617">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="4467d-618">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="4467d-618">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="4467d-619">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4467d-619">Az.Network</span></span>
* <span data-ttu-id="4467d-620">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="4467d-620">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="4467d-621">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="4467d-621">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="4467d-622">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="4467d-622">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="4467d-623">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="4467d-623">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="4467d-624">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="4467d-624">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="4467d-625">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="4467d-625">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="4467d-626">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="4467d-626">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="4467d-627">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="4467d-627">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="4467d-628">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="4467d-628">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="4467d-629">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="4467d-629">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="4467d-630">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="4467d-630">Az.Relay</span></span>
* <span data-ttu-id="4467d-631">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="4467d-631">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="4467d-632">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4467d-632">Az.Resources</span></span>
* <span data-ttu-id="4467d-633">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="4467d-633">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="4467d-634">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="4467d-634">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="4467d-635">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="4467d-635">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="4467d-636">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4467d-636">Az.ServiceFabric</span></span>
* <span data-ttu-id="4467d-637">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="4467d-637">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="4467d-638">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4467d-638">Az.Sql</span></span>
* <span data-ttu-id="4467d-639">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4467d-639">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="4467d-640">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="4467d-640">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="4467d-641">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="4467d-641">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="4467d-642">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="4467d-642">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="4467d-643">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="4467d-643">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="4467d-644">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="4467d-644">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="4467d-645">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="4467d-645">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="4467d-646">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="4467d-646">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="4467d-647">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="4467d-647">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="4467d-648">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="4467d-648">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="4467d-649">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="4467d-649">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="4467d-650">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="4467d-650">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="4467d-651">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="4467d-651">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="4467d-652">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="4467d-652">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="4467d-653">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="4467d-653">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="4467d-654">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="4467d-654">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="4467d-655">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="4467d-655">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="4467d-656">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="4467d-656">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="4467d-657">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="4467d-657">General</span></span>
* <span data-ttu-id="4467d-658">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="4467d-658">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="4467d-659">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="4467d-659">Az.Profile</span></span>
* <span data-ttu-id="4467d-660">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="4467d-660">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="4467d-661">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="4467d-661">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="4467d-662">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="4467d-662">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="4467d-663">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="4467d-663">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="4467d-664">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="4467d-664">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="4467d-665">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="4467d-665">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="4467d-666">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="4467d-666">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="4467d-667">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4467d-667">Az.CognitiveServices</span></span>
* <span data-ttu-id="4467d-668">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="4467d-668">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4467d-669">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4467d-669">Az.Compute</span></span>
* <span data-ttu-id="4467d-670">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="4467d-670">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="4467d-671">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="4467d-671">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="4467d-672">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="4467d-672">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4467d-673">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4467d-673">Az.DataLakeStore</span></span>
* <span data-ttu-id="4467d-674">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="4467d-674">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="4467d-675">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="4467d-675">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="4467d-676">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="4467d-676">Az.Insights</span></span>
* <span data-ttu-id="4467d-677">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="4467d-677">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="4467d-678">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="4467d-678">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="4467d-679">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="4467d-679">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="4467d-680">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="4467d-680">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4467d-681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4467d-681">Az.Network</span></span>
* <span data-ttu-id="4467d-682">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="4467d-682">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="4467d-683">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="4467d-683">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="4467d-684">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="4467d-684">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="4467d-685">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="4467d-685">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="4467d-686">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="4467d-686">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="4467d-687">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="4467d-687">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="4467d-688">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="4467d-688">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4467d-689">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4467d-689">Az.PolicyInsights</span></span>
* <span data-ttu-id="4467d-690">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="4467d-690">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="4467d-691">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4467d-691">Az.Resources</span></span>
* <span data-ttu-id="4467d-692">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="4467d-692">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="4467d-693">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="4467d-693">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="4467d-694">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4467d-694">Az.ServiceBus</span></span>
* <span data-ttu-id="4467d-695">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="4467d-695">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4467d-696">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4467d-696">Az.ServiceFabric</span></span>
* <span data-ttu-id="4467d-697">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="4467d-697">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="4467d-698">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="4467d-698">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="4467d-699">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="4467d-699">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="4467d-700">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="4467d-700">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="4467d-701">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="4467d-701">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="4467d-702">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="4467d-702">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="4467d-703">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="4467d-703">Az.Profile</span></span>
* <span data-ttu-id="4467d-704">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="4467d-704">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="4467d-705">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="4467d-705">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4467d-706">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4467d-706">Az.Compute</span></span>
* <span data-ttu-id="4467d-707">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="4467d-707">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="4467d-708">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="4467d-708">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4467d-709">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4467d-709">Az.DataLakeStore</span></span>
* <span data-ttu-id="4467d-710">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="4467d-710">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="4467d-711">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4467d-711">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="4467d-712">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4467d-712">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="4467d-713">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4467d-713">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="4467d-714">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4467d-714">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4467d-715">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4467d-715">Az.Network</span></span>
* <span data-ttu-id="4467d-716">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="4467d-716">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="4467d-717">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="4467d-717">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4467d-718">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4467d-718">Az.Resources</span></span>
* <span data-ttu-id="4467d-719">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="4467d-719">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="4467d-720">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="4467d-720">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="4467d-721">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="4467d-721">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="4467d-722">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="4467d-722">Azure.Storage</span></span>
* <span data-ttu-id="4467d-723">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="4467d-723">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="4467d-724">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="4467d-724">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="4467d-725">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="4467d-725">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="4467d-726">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="4467d-726">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="4467d-727">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="4467d-727">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="4467d-728">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4467d-728">Az.CognitiveServices</span></span>
* <span data-ttu-id="4467d-729">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="4467d-729">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4467d-730">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4467d-730">Az.Compute</span></span>
* <span data-ttu-id="4467d-731">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="4467d-731">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="4467d-732">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="4467d-732">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="4467d-733">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="4467d-733">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="4467d-734">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="4467d-734">Az.DataFactoryV2</span></span>
* <span data-ttu-id="4467d-735">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="4467d-735">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4467d-736">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4467d-736">Az.Network</span></span>
* <span data-ttu-id="4467d-737">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="4467d-737">Added NetworkProfile functionality.</span></span> <span data-ttu-id="4467d-738">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="4467d-738">new cmdlets added</span></span>
    - <span data-ttu-id="4467d-739">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4467d-739">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="4467d-740">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4467d-740">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="4467d-741">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4467d-741">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="4467d-742">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4467d-742">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="4467d-743">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="4467d-743">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="4467d-744">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="4467d-744">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="4467d-745">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="4467d-745">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="4467d-746">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="4467d-746">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="4467d-747">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="4467d-747">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="4467d-748">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="4467d-748">Az.RedisCache</span></span>
* <span data-ttu-id="4467d-749">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="4467d-749">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="4467d-750">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="4467d-750">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="4467d-751">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4467d-751">Az.Resources</span></span>
* <span data-ttu-id="4467d-752">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4467d-752">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="4467d-753">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="4467d-753">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="4467d-754">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4467d-754">Az.Sql</span></span>
* <span data-ttu-id="4467d-755">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="4467d-755">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4467d-756">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4467d-756">Az.Websites</span></span>
* <span data-ttu-id="4467d-757">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="4467d-757">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="4467d-758">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="4467d-758">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="4467d-759">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="4467d-759">0.2.0 - September 2018</span></span>
 <span data-ttu-id="4467d-760">Начальный выпуск</span><span class="sxs-lookup"><span data-stu-id="4467d-760">Initial Release</span></span>
