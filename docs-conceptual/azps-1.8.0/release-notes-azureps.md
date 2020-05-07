---
title: Заметки о выпуске Azure PowerShell
description: Узнайте обо всех последних обновлениях модулей Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/30/2019
ms.openlocfilehash: 8a9a399f72ed9e3e9a3cbc09c8a4abaa91339c24
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/05/2020
ms.locfileid: "71319296"
---
## <a name="180---april-2019"></a><span data-ttu-id="024ee-103">1.8.0 — апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="024ee-103">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="024ee-104">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="024ee-104">Highlights since the last major release</span></span>
* <span data-ttu-id="024ee-105">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="024ee-105">General availability of `Az` module</span></span>
* <span data-ttu-id="024ee-106">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="024ee-106">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="024ee-107">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="024ee-107">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="024ee-108">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="024ee-108">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="024ee-109">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="024ee-109">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="024ee-110">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="024ee-110">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="024ee-111">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="024ee-111">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="024ee-112">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="024ee-112">Az.Accounts</span></span>
* <span data-ttu-id="024ee-113">Обновлен командлет Uninstall-AzureRm для правильного удаления модулей в Mac.</span><span class="sxs-lookup"><span data-stu-id="024ee-113">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="024ee-114">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="024ee-114">Az.Batch</span></span>
* <span data-ttu-id="024ee-115">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="024ee-115">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="024ee-116">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="024ee-116">Az.Cdn</span></span>
* <span data-ttu-id="024ee-117">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="024ee-117">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="024ee-118">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="024ee-118">Az.CognitiveServices</span></span>
* <span data-ttu-id="024ee-119">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="024ee-119">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="024ee-120">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="024ee-120">Az.Compute</span></span>
* <span data-ttu-id="024ee-121">Устранена проблема с установкой AEM, если в идентификаторах ресурсов дисков группа ресурсов указана в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="024ee-121">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="024ee-122">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="024ee-122">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="024ee-123">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="024ee-123">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="024ee-124">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="024ee-124">Az.DataFactory</span></span>
* <span data-ttu-id="024ee-125">Добавлены свойства SsisProperties, если NodeCount не имеет значения NULL для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="024ee-125">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="024ee-126">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="024ee-126">Az.DataLakeStore</span></span>
* <span data-ttu-id="024ee-127">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="024ee-127">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="024ee-128">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="024ee-128">Az.EventGrid</span></span>
* <span data-ttu-id="024ee-129">Обновлен текст справки для конечной точки, указывающий, что необходимо создать ресурсы, прежде чем использовать командлеты для создания или обновления подписки на события.</span><span class="sxs-lookup"><span data-stu-id="024ee-129">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="024ee-130">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="024ee-130">Az.EventHub</span></span>
* <span data-ttu-id="024ee-131">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="024ee-131">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="024ee-132">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="024ee-132">Az.HDInsight</span></span>
* <span data-ttu-id="024ee-133">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="024ee-133">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="024ee-134">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="024ee-134">Az.IotHub</span></span>
* <span data-ttu-id="024ee-135">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="024ee-135">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="024ee-136">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="024ee-136">Az.KeyVault</span></span>
* <span data-ttu-id="024ee-137">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="024ee-137">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="024ee-138">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="024ee-138">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="024ee-139">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="024ee-139">Az.MachineLearning</span></span>
* <span data-ttu-id="024ee-140">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="024ee-140">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="024ee-141">Az.Media</span><span class="sxs-lookup"><span data-stu-id="024ee-141">Az.Media</span></span>
* <span data-ttu-id="024ee-142">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="024ee-142">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="024ee-143">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="024ee-143">Az.Monitor</span></span>
  * <span data-ttu-id="024ee-144">Добавлены новые командлеты для правила генерации оповещений на основе метрик GenV2 (не классических).</span><span class="sxs-lookup"><span data-stu-id="024ee-144">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="024ee-145">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="024ee-145">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="024ee-146">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="024ee-146">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="024ee-147">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="024ee-147">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="024ee-148">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="024ee-148">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="024ee-149">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="024ee-149">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="024ee-150">Обновлен пакет SDK Monitor до предварительной версии 0.22.0.</span><span class="sxs-lookup"><span data-stu-id="024ee-150">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="024ee-151">Az.Network</span><span class="sxs-lookup"><span data-stu-id="024ee-151">Az.Network</span></span>
* <span data-ttu-id="024ee-152">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="024ee-152">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="024ee-153">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="024ee-153">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="024ee-154">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="024ee-154">Az.NotificationHubs</span></span>
* <span data-ttu-id="024ee-155">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="024ee-155">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="024ee-156">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="024ee-156">Az.OperationalInsights</span></span>
* <span data-ttu-id="024ee-157">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="024ee-157">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="024ee-158">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="024ee-158">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="024ee-159">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="024ee-159">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="024ee-160">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="024ee-160">Az.RecoveryServices</span></span>
* <span data-ttu-id="024ee-161">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="024ee-161">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="024ee-162">Обновлен табличный формат для SQL на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="024ee-162">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="024ee-163">Добавлен альтернативный метод для получения расположения в Общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="024ee-163">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="024ee-164">Обновлено значение ScheduleRunDays в объекте SchedulePolicy в соответствии с часовым поясом.</span><span class="sxs-lookup"><span data-stu-id="024ee-164">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="024ee-165">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="024ee-165">Az.RedisCache</span></span>
* <span data-ttu-id="024ee-166">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="024ee-166">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="024ee-167">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="024ee-167">Az.Resources</span></span>
* <span data-ttu-id="024ee-168">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="024ee-168">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="024ee-169">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="024ee-169">Az.Sql</span></span>
* <span data-ttu-id="024ee-170">Заменена зависимость от пакета SDK монитора на обычный код.</span><span class="sxs-lookup"><span data-stu-id="024ee-170">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="024ee-171">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="024ee-171">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="024ee-172">Улучшен процесс классификации нескольких столбцов.</span><span class="sxs-lookup"><span data-stu-id="024ee-172">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="024ee-173">Добавлены свойства SKU (имя, семейство, производительность SKU) в отклике Get-AzSqlServerServiceObjective, а также по умолчанию задан табличный формат.</span><span class="sxs-lookup"><span data-stu-id="024ee-173">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="024ee-174">C помощью Get-AzSqlServerServiceObjective теперь можно получать список доступных целевых служб по расположению без необходимости заранее размещать сервер в регионе.</span><span class="sxs-lookup"><span data-stu-id="024ee-174">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="024ee-175">Поддерживается параметр часового пояса при создании Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="024ee-175">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="024ee-176">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="024ee-176">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="024ee-177">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="024ee-177">Az.Websites</span></span>
* <span data-ttu-id="024ee-178">Исправлены командлеты Set-AzWebApp и Set-AzWebAppSlot, которые теперь не удаляют теги при выполнении.</span><span class="sxs-lookup"><span data-stu-id="024ee-178">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="024ee-179">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="024ee-179">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="024ee-180">Обновлен пакет SDK веб-узлов.</span><span class="sxs-lookup"><span data-stu-id="024ee-180">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="024ee-181">Удалено свойство AdminSiteName из PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="024ee-181">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="024ee-182">1.7.0 —апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="024ee-182">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="024ee-183">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="024ee-183">Highlights since the last major release</span></span>
* <span data-ttu-id="024ee-184">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="024ee-184">General availability of `Az` module</span></span>
* <span data-ttu-id="024ee-185">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="024ee-185">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="024ee-186">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="024ee-186">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="024ee-187">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="024ee-187">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="024ee-188">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="024ee-188">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="024ee-189">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="024ee-189">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="024ee-190">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="024ee-190">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="024ee-191">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="024ee-191">Az.Accounts</span></span>
* <span data-ttu-id="024ee-192">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметр AzureAnalysisServicesEndpointResourceId.</span><span class="sxs-lookup"><span data-stu-id="024ee-192">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="024ee-193">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="024ee-193">Az.AnalysisServices</span></span>
* <span data-ttu-id="024ee-194">Использование ServiceClient в командлетах плоскости данных и удаление исходной логики проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="024ee-194">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="024ee-195">Add-AzureASAccount используется как оболочка для Connect-AzAccount во избежание критических изменений.</span><span class="sxs-lookup"><span data-stu-id="024ee-195">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="024ee-196">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="024ee-196">Az.Automation</span></span>
* <span data-ttu-id="024ee-197">Исправлена ошибка командлета New-AzAutomationSoftwareUpdateConfiguration, связанная с включением.</span><span class="sxs-lookup"><span data-stu-id="024ee-197">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="024ee-198">Теперь параметры IncludedKbNumber и IncludedPackageNameMask должны работать нормально.</span><span class="sxs-lookup"><span data-stu-id="024ee-198">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="024ee-199">Исправлена ошибка динамической группы управления обновлениями службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="024ee-199">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="024ee-200">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="024ee-200">Az.Compute</span></span>
* <span data-ttu-id="024ee-201">В командлеты New-AzDiskConfig и New-AzSnapshotConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="024ee-201">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="024ee-202">Теперь можно создавать виртуальные машину на основе образов из коллекции от других клиентов.</span><span class="sxs-lookup"><span data-stu-id="024ee-202">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="024ee-203">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="024ee-203">Az.ContainerInstance</span></span>
* <span data-ttu-id="024ee-204">Исправлена проблема в параметре -Command командлета New-AzContainerGroup, из-за которой в конце добавлялся пустой аргумент.</span><span class="sxs-lookup"><span data-stu-id="024ee-204">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="024ee-205">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="024ee-205">Az.DataFactory</span></span>
* <span data-ttu-id="024ee-206">Пакет SDK для ADF .NET обновлен до версии 3.0.2.</span><span class="sxs-lookup"><span data-stu-id="024ee-206">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="024ee-207">Командлет Set-AzDataFactoryV2 обновлен с помощью дополнительных параметров для настроек, связанных с RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="024ee-207">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="024ee-208">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="024ee-208">Az.Resources</span></span>
* <span data-ttu-id="024ee-209">Улучшена обработка поставщиков Get-AzResource при предоставлении параметров -ResourceId или -ResourceGroupName, -Name и -ResourceType.</span><span class="sxs-lookup"><span data-stu-id="024ee-209">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="024ee-210">Улучшена обработка ошибок в командлетах Test-AzDeployment и Test-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="024ee-210">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="024ee-211">Теперь ошибки, возникающие за пределами проверки развертывания, обрабатываются и включаются в выходные данные команды.</span><span class="sxs-lookup"><span data-stu-id="024ee-211">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="024ee-212">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="024ee-212">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="024ee-213">Добавлен параметр-переключатель -IgnoreDynamicParameters, с помощью которого можно настроить командлеты развертывания так, чтобы они пропускали запросы в сценариях скриптов и заданий.</span><span class="sxs-lookup"><span data-stu-id="024ee-213">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="024ee-214">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="024ee-214">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="024ee-215">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="024ee-215">Az.Sql</span></span>
* <span data-ttu-id="024ee-216">Поддержка классификации данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="024ee-216">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="024ee-217">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="024ee-217">Az.Storage</span></span>
* <span data-ttu-id="024ee-218">Подробные сообщения об ошибке передаются при создании контекста хранилища с помощью параметра -UseConnectedAccount, но без входа в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="024ee-218">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="024ee-219">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="024ee-219">New-AzStorageContext</span></span>
* <span data-ttu-id="024ee-220">Поддержка свойств службы управления BLOB-объектов в указанной учетной записи хранения с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="024ee-220">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="024ee-221">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="024ee-221">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="024ee-222">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="024ee-222">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="024ee-223">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="024ee-223">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="024ee-224">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="024ee-224">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="024ee-225">Поддержка параметра -AsJob в командлетах для отправки и скачивания больших двоичных объектов и файлов.</span><span class="sxs-lookup"><span data-stu-id="024ee-225">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="024ee-226">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="024ee-226">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="024ee-227">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="024ee-227">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="024ee-228">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="024ee-228">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="024ee-229">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="024ee-229">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="024ee-230">1.6.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="024ee-230">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="024ee-231">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="024ee-231">Highlights since the last major release</span></span>
* <span data-ttu-id="024ee-232">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="024ee-232">General availability of `Az` module</span></span>
* <span data-ttu-id="024ee-233">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="024ee-233">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="024ee-234">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="024ee-234">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="024ee-235">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="024ee-235">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="024ee-236">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="024ee-236">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="024ee-237">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="024ee-237">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="024ee-238">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="024ee-238">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="024ee-239">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="024ee-239">Az.Automation</span></span>
* <span data-ttu-id="024ee-240">В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:</span><span class="sxs-lookup"><span data-stu-id="024ee-240">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="024ee-241">динамическое группирование;</span><span class="sxs-lookup"><span data-stu-id="024ee-241">Dynamic grouping</span></span>
    * <span data-ttu-id="024ee-242">скрипты предварительного или последующего выполнения;</span><span class="sxs-lookup"><span data-stu-id="024ee-242">Pre-Post script</span></span>
    * <span data-ttu-id="024ee-243">параметр перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="024ee-243">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="024ee-244">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="024ee-244">Az.Compute</span></span>
* <span data-ttu-id="024ee-245">Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.</span><span class="sxs-lookup"><span data-stu-id="024ee-245">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="024ee-246">Обновление клиентской библиотеки вычислений до версии 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="024ee-246">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="024ee-247">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="024ee-247">Az.KeyVault</span></span>
* <span data-ttu-id="024ee-248">Добавлена поддержка подстановочных знаков в командлетах KeyVault.</span><span class="sxs-lookup"><span data-stu-id="024ee-248">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="024ee-249">Az.Network</span><span class="sxs-lookup"><span data-stu-id="024ee-249">Az.Network</span></span>
* <span data-ttu-id="024ee-250">Добавлена поддержка анализа угроз для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="024ee-250">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="024ee-251">Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="024ee-251">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="024ee-252">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="024ee-252">Az.RecoveryServices</span></span>
* <span data-ttu-id="024ee-253">В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.</span><span class="sxs-lookup"><span data-stu-id="024ee-253">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="024ee-254">Добавлена поддержка канала для отмены регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="024ee-254">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="024ee-255">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="024ee-255">Az.Resources</span></span>
* <span data-ttu-id="024ee-256">Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="024ee-256">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="024ee-257">Обновлены учетные данные, используемые при общих вызовах к ARM.</span><span class="sxs-lookup"><span data-stu-id="024ee-257">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="024ee-258">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="024ee-258">Az.Sql</span></span>
* <span data-ttu-id="024ee-259">Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="024ee-259">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="024ee-260">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="024ee-260">Az.Storage</span></span>
* <span data-ttu-id="024ee-261">Поддержка получения, настройки и удаления политики управления в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="024ee-261">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="024ee-262">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="024ee-262">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="024ee-263">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="024ee-263">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="024ee-264">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="024ee-264">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="024ee-265">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="024ee-265">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="024ee-266">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="024ee-266">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="024ee-267">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="024ee-267">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="024ee-268">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="024ee-268">Az.Websites</span></span>
* <span data-ttu-id="024ee-269">Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="024ee-269">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="024ee-270">1.5.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="024ee-270">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="024ee-271">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="024ee-271">Az.Accounts</span></span>
* <span data-ttu-id="024ee-272">Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.</span><span class="sxs-lookup"><span data-stu-id="024ee-272">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="024ee-273">Обновлены примеры для Connect AzAccount.</span><span class="sxs-lookup"><span data-stu-id="024ee-273">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="024ee-274">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="024ee-274">Az.Automation</span></span>
* <span data-ttu-id="024ee-275">Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="024ee-275">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="024ee-276">Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов.</span><span class="sxs-lookup"><span data-stu-id="024ee-276">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="024ee-277">Теперь он возвращает все узлы.</span><span class="sxs-lookup"><span data-stu-id="024ee-277">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="024ee-278">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="024ee-278">Az.Cdn</span></span>
* <span data-ttu-id="024ee-279">Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.</span><span class="sxs-lookup"><span data-stu-id="024ee-279">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="024ee-280">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="024ee-280">Az.Compute</span></span>
* <span data-ttu-id="024ee-281">Добавлена поддержка подстановочных знаков в командлетах Get.</span><span class="sxs-lookup"><span data-stu-id="024ee-281">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="024ee-282">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="024ee-282">Az.DataFactory</span></span>
* <span data-ttu-id="024ee-283">Обновлен пакет SDK для ADF .NET до версии 3.0.1.</span><span class="sxs-lookup"><span data-stu-id="024ee-283">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="024ee-284">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="024ee-284">Az.LogicApp</span></span>
* <span data-ttu-id="024ee-285">Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.</span><span class="sxs-lookup"><span data-stu-id="024ee-285">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="024ee-286">Az.Network</span><span class="sxs-lookup"><span data-stu-id="024ee-286">Az.Network</span></span>
* <span data-ttu-id="024ee-287">Добавлена поддержка подстановочных знаков в командлетах Network.</span><span class="sxs-lookup"><span data-stu-id="024ee-287">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="024ee-288">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="024ee-288">Az.RecoveryServices</span></span>
* <span data-ttu-id="024ee-289">Добавлена поддержка SQL Server на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="024ee-289">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="024ee-290">Обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="024ee-290">SDK Update</span></span>
* <span data-ttu-id="024ee-291">Удалена проверка VMappContainer в Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="024ee-291">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="024ee-292">Добавлены параметры Name и ServerName для Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="024ee-292">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="024ee-293">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="024ee-293">Az.Resources</span></span>
* <span data-ttu-id="024ee-294">Добавлен параметр `-TemplateObject` в командлеты для развертывания.</span><span class="sxs-lookup"><span data-stu-id="024ee-294">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="024ee-295">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.</span><span class="sxs-lookup"><span data-stu-id="024ee-295">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="024ee-296">Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="024ee-296">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="024ee-297">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.</span><span class="sxs-lookup"><span data-stu-id="024ee-297">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="024ee-298">Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="024ee-298">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="024ee-299">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.</span><span class="sxs-lookup"><span data-stu-id="024ee-299">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="024ee-300">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="024ee-300">Az.Sql</span></span>
* <span data-ttu-id="024ee-301">Обновление AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="024ee-301">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="024ee-302">Исправлено поведение для пограничного случая при создании параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="024ee-302">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="024ee-303">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="024ee-303">Az.Storage</span></span>
* <span data-ttu-id="024ee-304">Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="024ee-304">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="024ee-305">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="024ee-305">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="024ee-306">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="024ee-306">Az.AnalysisServices</span></span>
* <span data-ttu-id="024ee-307">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="024ee-307">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="024ee-308">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="024ee-308">Az.Automation</span></span>
* <span data-ttu-id="024ee-309">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="024ee-309">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="024ee-310">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="024ee-310">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="024ee-311">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="024ee-311">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="024ee-312">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="024ee-312">Az.CognitiveServices</span></span>
* <span data-ttu-id="024ee-313">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="024ee-313">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="024ee-314">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="024ee-314">Az.Compute</span></span>
* <span data-ttu-id="024ee-315">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="024ee-315">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="024ee-316">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="024ee-316">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="024ee-317">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="024ee-317">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="024ee-318">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="024ee-318">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="024ee-319">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="024ee-319">Az.DataLakeStore</span></span>
* <span data-ttu-id="024ee-320">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="024ee-320">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="024ee-321">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="024ee-321">Az.EventHub</span></span>
* <span data-ttu-id="024ee-322">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="024ee-322">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="024ee-323">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="024ee-323">Az.KeyVault</span></span>
* <span data-ttu-id="024ee-324">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="024ee-324">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="024ee-325">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="024ee-325">Az.LogicApp</span></span>
* <span data-ttu-id="024ee-326">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="024ee-326">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="024ee-327">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="024ee-327">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="024ee-328">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="024ee-328">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="024ee-329">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="024ee-329">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="024ee-330">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="024ee-330">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="024ee-331">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="024ee-331">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="024ee-332">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="024ee-332">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="024ee-333">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="024ee-333">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="024ee-334">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="024ee-334">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="024ee-335">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="024ee-335">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="024ee-336">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="024ee-336">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="024ee-337">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="024ee-337">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="024ee-338">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="024ee-338">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="024ee-339">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="024ee-339">Az.Monitor</span></span>
* <span data-ttu-id="024ee-340">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="024ee-340">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="024ee-341">Az.Network</span><span class="sxs-lookup"><span data-stu-id="024ee-341">Az.Network</span></span>
* <span data-ttu-id="024ee-342">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="024ee-342">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="024ee-343">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="024ee-343">Az.OperationalInsights</span></span>
* <span data-ttu-id="024ee-344">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="024ee-344">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="024ee-345">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="024ee-345">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="024ee-346">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="024ee-346">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="024ee-347">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="024ee-347">Az.Resources</span></span>
* <span data-ttu-id="024ee-348">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="024ee-348">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="024ee-349">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="024ee-349">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="024ee-350">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="024ee-350">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="024ee-351">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="024ee-351">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="024ee-352">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="024ee-352">Az.Sql</span></span>
* <span data-ttu-id="024ee-353">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="024ee-353">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="024ee-354">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="024ee-354">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="024ee-355">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="024ee-355">Az.Websites</span></span>
* <span data-ttu-id="024ee-356">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="024ee-356">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="024ee-357">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="024ee-357">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="024ee-358">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="024ee-358">Az.Accounts</span></span>
* <span data-ttu-id="024ee-359">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="024ee-359">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="024ee-360">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="024ee-360">Az.AnalysisServices</span></span>
<span data-ttu-id="024ee-361">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="024ee-361">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="024ee-362">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="024ee-362">Az.Compute</span></span>
* <span data-ttu-id="024ee-363">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="024ee-363">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="024ee-364">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="024ee-364">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="024ee-365">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="024ee-365">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="024ee-366">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="024ee-366">Az.RecoveryServices</span></span>
<span data-ttu-id="024ee-367">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="024ee-367">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="024ee-368">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="024ee-368">Az.Resources</span></span>
* <span data-ttu-id="024ee-369">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="024ee-369">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="024ee-370">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="024ee-370">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="024ee-371">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="024ee-371">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="024ee-372">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="024ee-372">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="024ee-373">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="024ee-373">Az.Sql</span></span>
* <span data-ttu-id="024ee-374">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="024ee-374">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="024ee-375">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="024ee-375">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="024ee-376">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="024ee-376">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="024ee-377">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="024ee-377">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="024ee-378">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="024ee-378">Az.Accounts</span></span>
* <span data-ttu-id="024ee-379">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="024ee-379">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="024ee-380">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="024ee-380">Az.AnalysisServices</span></span>
* <span data-ttu-id="024ee-381">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="024ee-381">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="024ee-382">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="024ee-382">Az.RecoveryServices</span></span>
* <span data-ttu-id="024ee-383">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="024ee-383">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="024ee-384">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="024ee-384">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="024ee-385">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="024ee-385">Az.Accounts</span></span>
* <span data-ttu-id="024ee-386">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="024ee-386">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="024ee-387">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="024ee-387">Update incorrect online help URLs</span></span>
* <span data-ttu-id="024ee-388">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="024ee-388">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="024ee-389">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="024ee-389">Az.Aks</span></span>
* <span data-ttu-id="024ee-390">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="024ee-390">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="024ee-391">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="024ee-391">Az.Automation</span></span>
* <span data-ttu-id="024ee-392">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="024ee-392">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="024ee-393">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="024ee-393">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="024ee-394">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="024ee-394">Az.Cdn</span></span>
* <span data-ttu-id="024ee-395">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="024ee-395">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="024ee-396">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="024ee-396">Az.Compute</span></span>
* <span data-ttu-id="024ee-397">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="024ee-397">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="024ee-398">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="024ee-398">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="024ee-399">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="024ee-399">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="024ee-400">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="024ee-400">Az.ContainerRegistry</span></span>
* <span data-ttu-id="024ee-401">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="024ee-401">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="024ee-402">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="024ee-402">Az.DataFactory</span></span>
* <span data-ttu-id="024ee-403">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="024ee-403">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="024ee-404">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="024ee-404">Az.DataLakeStore</span></span>
* <span data-ttu-id="024ee-405">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="024ee-405">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="024ee-406">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="024ee-406">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="024ee-407">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="024ee-407">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="024ee-408">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="024ee-408">Az.IotHub</span></span>
* <span data-ttu-id="024ee-409">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="024ee-409">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="024ee-410">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="024ee-410">Az.KeyVault</span></span>
* <span data-ttu-id="024ee-411">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="024ee-411">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="024ee-412">Az.Network</span><span class="sxs-lookup"><span data-stu-id="024ee-412">Az.Network</span></span>
* <span data-ttu-id="024ee-413">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="024ee-413">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="024ee-414">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="024ee-414">Az.Resources</span></span>
* <span data-ttu-id="024ee-415">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="024ee-415">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="024ee-416">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="024ee-416">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="024ee-417">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="024ee-417">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="024ee-418">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="024ee-418">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="024ee-419">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="024ee-419">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="024ee-420">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="024ee-420">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="024ee-421">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="024ee-421">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="024ee-422">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="024ee-422">Az.ServiceFabric</span></span>
* <span data-ttu-id="024ee-423">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="024ee-423">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="024ee-424">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="024ee-424">Fix some error messages.</span></span>
* <span data-ttu-id="024ee-425">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="024ee-425">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="024ee-426">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="024ee-426">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="024ee-427">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="024ee-427">Az.SignalR</span></span>
* <span data-ttu-id="024ee-428">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="024ee-428">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="024ee-429">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="024ee-429">Az.Sql</span></span>
* <span data-ttu-id="024ee-430">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="024ee-430">Update incorrect online help URLs</span></span>
* <span data-ttu-id="024ee-431">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="024ee-431">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="024ee-432">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="024ee-432">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="024ee-433">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="024ee-433">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="024ee-434">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="024ee-434">Az.Storage</span></span>
* <span data-ttu-id="024ee-435">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="024ee-435">Update incorrect online help URLs</span></span>
* <span data-ttu-id="024ee-436">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="024ee-436">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="024ee-437">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="024ee-437">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="024ee-438">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="024ee-438">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="024ee-439">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="024ee-439">Az.TrafficManager</span></span>
* <span data-ttu-id="024ee-440">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="024ee-440">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="024ee-441">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="024ee-441">Az.Websites</span></span>
* <span data-ttu-id="024ee-442">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="024ee-442">Update incorrect online help URLs</span></span>
* <span data-ttu-id="024ee-443">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="024ee-443">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="024ee-444">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="024ee-444">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="024ee-445">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="024ee-445">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="024ee-446">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="024ee-446">Az.Accounts</span></span>
* <span data-ttu-id="024ee-447">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="024ee-447">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="024ee-448">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="024ee-448">Az.Compute</span></span>
* <span data-ttu-id="024ee-449">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="024ee-449">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="024ee-450">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="024ee-450">Updated the description of ID in help files</span></span>
* <span data-ttu-id="024ee-451">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="024ee-451">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="024ee-452">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="024ee-452">Az.DataLakeStore</span></span>
* <span data-ttu-id="024ee-453">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="024ee-453">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="024ee-454">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="024ee-454">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="024ee-455">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="024ee-455">Az.EventGrid</span></span>
* <span data-ttu-id="024ee-456">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="024ee-456">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="024ee-457">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="024ee-457">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="024ee-458">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="024ee-458">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="024ee-459">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="024ee-459">Event Time-To-Live,</span></span>
        - <span data-ttu-id="024ee-460">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="024ee-460">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="024ee-461">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="024ee-461">Dead letter endpoint.</span></span>
    - <span data-ttu-id="024ee-462">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="024ee-462">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="024ee-463">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="024ee-463">Event Time-To-Live,</span></span>
        - <span data-ttu-id="024ee-464">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="024ee-464">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="024ee-465">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="024ee-465">Dead letter endpoint.</span></span>
* <span data-ttu-id="024ee-466">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="024ee-466">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="024ee-467">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="024ee-467">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="024ee-468">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="024ee-468">Az.IotHub</span></span>
* <span data-ttu-id="024ee-469">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="024ee-469">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="024ee-470">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="024ee-470">Az.LogicApp</span></span>
* <span data-ttu-id="024ee-471">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="024ee-471">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="024ee-472">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="024ee-472">Az.Resources</span></span>
* <span data-ttu-id="024ee-473">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="024ee-473">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="024ee-474">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="024ee-474">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="024ee-475">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="024ee-475">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="024ee-476">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="024ee-476">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="024ee-477">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="024ee-477">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="024ee-478">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="024ee-478">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="024ee-479">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="024ee-479">Az.SignalR</span></span>
* <span data-ttu-id="024ee-480">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="024ee-480">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="024ee-481">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="024ee-481">Az.Sql</span></span>
* <span data-ttu-id="024ee-482">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="024ee-482">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="024ee-483">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="024ee-483">Az.Storage</span></span>
* <span data-ttu-id="024ee-484">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="024ee-484">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="024ee-485">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="024ee-485">New-AzStorageContext</span></span>
* <span data-ttu-id="024ee-486">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="024ee-486">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="024ee-487">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="024ee-487">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="024ee-488">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="024ee-488">Az.Websites</span></span>
* <span data-ttu-id="024ee-489">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="024ee-489">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="024ee-490">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="024ee-490">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="024ee-491">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="024ee-491">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="024ee-492">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="024ee-492">General</span></span>

- <span data-ttu-id="024ee-493">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="024ee-493">General Availability of Az Module</span></span>
- <span data-ttu-id="024ee-494">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="024ee-494">Online help for each module</span></span>
- <span data-ttu-id="024ee-495">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="024ee-495">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="024ee-496">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="024ee-496">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="024ee-497">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="024ee-497">Az.Accounts</span></span>
- <span data-ttu-id="024ee-498">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="024ee-498">Changed from Az.Profile</span></span>
- <span data-ttu-id="024ee-499">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="024ee-499">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="024ee-500">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="024ee-500">Az.ApiManagement</span></span>
- <span data-ttu-id="024ee-501">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="024ee-501">Fixes for #7002</span></span>
- <span data-ttu-id="024ee-502">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="024ee-502">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="024ee-503">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="024ee-503">Az.Batch</span></span>
- <span data-ttu-id="024ee-504">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="024ee-504">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="024ee-505">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="024ee-505">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="024ee-506">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="024ee-506">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="024ee-507">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="024ee-507">Az.Billing</span></span>
- <span data-ttu-id="024ee-508">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="024ee-508">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="024ee-509">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="024ee-509">Az.CognitivServices</span></span>
- <span data-ttu-id="024ee-510">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="024ee-510">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="024ee-511">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="024ee-511">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="024ee-512">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="024ee-512">Az.ContainerInstance</span></span>
- <span data-ttu-id="024ee-513">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="024ee-513">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="024ee-514">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="024ee-514">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="024ee-515">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="024ee-515">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="024ee-516">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="024ee-516">Az.DataLakeStore</span></span>
- <span data-ttu-id="024ee-517">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="024ee-517">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="024ee-518">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="024ee-518">Az.Monitor</span></span>
- <span data-ttu-id="024ee-519">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="024ee-519">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="024ee-520">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="024ee-520">Az.KeyVault</span></span>
- <span data-ttu-id="024ee-521">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="024ee-521">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="024ee-522">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="024ee-522">Az.MachineLearning</span></span>
- <span data-ttu-id="024ee-523">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="024ee-523">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="024ee-524">Az.Media</span><span class="sxs-lookup"><span data-stu-id="024ee-524">Az.Media</span></span>
- <span data-ttu-id="024ee-525">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="024ee-525">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="024ee-526">Az.Network</span><span class="sxs-lookup"><span data-stu-id="024ee-526">Az.Network</span></span>
<span data-ttu-id="024ee-527">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="024ee-527">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="024ee-528">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="024ee-528">New cmdlets added:</span></span>
        - <span data-ttu-id="024ee-529">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="024ee-529">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="024ee-530">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="024ee-530">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="024ee-531">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="024ee-531">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="024ee-532">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="024ee-532">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="024ee-533">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="024ee-533">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="024ee-534">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="024ee-534">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="024ee-535">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="024ee-535">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="024ee-536">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="024ee-536">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="024ee-537">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="024ee-537">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="024ee-538">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="024ee-538">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="024ee-539">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="024ee-539">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="024ee-540">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="024ee-540">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="024ee-541">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="024ee-541">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="024ee-542">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="024ee-542">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="024ee-543">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="024ee-543">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="024ee-544">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="024ee-544">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="024ee-545">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="024ee-545">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="024ee-546">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="024ee-546">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="024ee-547">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="024ee-547">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="024ee-548">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="024ee-548">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="024ee-549">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="024ee-549">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="024ee-550">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="024ee-550">Az.OperationalInsights</span></span>
- <span data-ttu-id="024ee-551">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="024ee-551">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="024ee-552">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="024ee-552">Az.Profile</span></span>
- <span data-ttu-id="024ee-553">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="024ee-553">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="024ee-554">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="024ee-554">Az.RecoveryServices</span></span>
- <span data-ttu-id="024ee-555">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="024ee-555">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="024ee-556">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="024ee-556">Az.Resources</span></span>
- <span data-ttu-id="024ee-557">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="024ee-557">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="024ee-558">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="024ee-558">Az.ServiceFabric</span></span>
- <span data-ttu-id="024ee-559">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="024ee-559">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="024ee-560">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="024ee-560">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="024ee-561">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="024ee-561">Az.SIgnalR</span></span>
- <span data-ttu-id="024ee-562">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="024ee-562">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="024ee-563">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="024ee-563">Az.Sql</span></span>
- <span data-ttu-id="024ee-564">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="024ee-564">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="024ee-565">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="024ee-565">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="024ee-566">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="024ee-566">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="024ee-567">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="024ee-567">Az.Storage</span></span>
- <span data-ttu-id="024ee-568">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="024ee-568">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="024ee-569">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="024ee-569">Az.Websites</span></span>
- <span data-ttu-id="024ee-570">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="024ee-570">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="024ee-571">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="024ee-571">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="024ee-572">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="024ee-572">General</span></span>

* <span data-ttu-id="024ee-573">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="024ee-573">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="024ee-574">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="024ee-574">Az.Compute</span></span>

* <span data-ttu-id="024ee-575">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="024ee-575">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="024ee-576">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="024ee-576">Az.DataLakeStore</span></span>

* <span data-ttu-id="024ee-577">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="024ee-577">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="024ee-578">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="024ee-578">Az.FrontDoor</span></span>

* <span data-ttu-id="024ee-579">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="024ee-579">Fixed some broken links</span></span>
    - <span data-ttu-id="024ee-580">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="024ee-580">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="024ee-581">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="024ee-581">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="024ee-582">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="024ee-582">Az.RecoveryServices</span></span>

* <span data-ttu-id="024ee-583">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="024ee-583">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="024ee-584">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="024ee-584">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="024ee-585">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="024ee-585">Az.Resources</span></span>

* <span data-ttu-id="024ee-586">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="024ee-586">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="024ee-587">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="024ee-587">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="024ee-588">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="024ee-588">Az.Sql</span></span>

* <span data-ttu-id="024ee-589">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="024ee-589">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="024ee-590">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="024ee-590">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="024ee-591">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="024ee-591">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="024ee-592">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="024ee-592">Az.Storage</span></span>

* <span data-ttu-id="024ee-593">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="024ee-593">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="024ee-594">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="024ee-594">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="024ee-595">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="024ee-595">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="024ee-596">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="024ee-596">Support Static Website configuration</span></span>
    - <span data-ttu-id="024ee-597">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="024ee-597">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="024ee-598">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="024ee-598">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="024ee-599">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="024ee-599">Az.Websites</span></span>

* <span data-ttu-id="024ee-600">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="024ee-600">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="024ee-601">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="024ee-601">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="024ee-602">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="024ee-602">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="024ee-603">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="024ee-603">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="024ee-604">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="024ee-604">Az.ApiManagement</span></span>
* <span data-ttu-id="024ee-605">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="024ee-605">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="024ee-606">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="024ee-606">Az.Automation</span></span>
* <span data-ttu-id="024ee-607">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="024ee-607">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="024ee-608">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="024ee-608">Added Update Management cmdlets</span></span>
* <span data-ttu-id="024ee-609">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="024ee-609">Added Source Control cmdlets</span></span>
* <span data-ttu-id="024ee-610">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="024ee-610">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="024ee-611">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="024ee-611">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="024ee-612">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="024ee-612">Az.Compute</span></span>
* <span data-ttu-id="024ee-613">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="024ee-613">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="024ee-614">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="024ee-614">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="024ee-615">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="024ee-615">Az.ContainerInstance</span></span>
* <span data-ttu-id="024ee-616">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="024ee-616">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="024ee-617">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="024ee-617">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="024ee-618">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="024ee-618">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="024ee-619">Az.Network</span><span class="sxs-lookup"><span data-stu-id="024ee-619">Az.Network</span></span>
* <span data-ttu-id="024ee-620">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="024ee-620">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="024ee-621">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="024ee-621">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="024ee-622">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="024ee-622">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="024ee-623">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="024ee-623">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="024ee-624">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="024ee-624">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="024ee-625">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="024ee-625">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="024ee-626">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="024ee-626">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="024ee-627">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="024ee-627">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="024ee-628">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="024ee-628">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="024ee-629">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="024ee-629">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="024ee-630">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="024ee-630">Az.Relay</span></span>
* <span data-ttu-id="024ee-631">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="024ee-631">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="024ee-632">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="024ee-632">Az.Resources</span></span>
* <span data-ttu-id="024ee-633">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="024ee-633">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="024ee-634">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="024ee-634">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="024ee-635">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="024ee-635">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="024ee-636">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="024ee-636">Az.ServiceFabric</span></span>
* <span data-ttu-id="024ee-637">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="024ee-637">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="024ee-638">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="024ee-638">Az.Sql</span></span>
* <span data-ttu-id="024ee-639">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="024ee-639">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="024ee-640">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="024ee-640">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="024ee-641">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="024ee-641">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="024ee-642">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="024ee-642">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="024ee-643">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="024ee-643">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="024ee-644">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="024ee-644">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="024ee-645">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="024ee-645">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="024ee-646">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="024ee-646">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="024ee-647">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="024ee-647">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="024ee-648">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="024ee-648">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="024ee-649">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="024ee-649">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="024ee-650">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="024ee-650">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="024ee-651">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="024ee-651">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="024ee-652">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="024ee-652">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="024ee-653">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="024ee-653">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="024ee-654">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="024ee-654">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="024ee-655">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="024ee-655">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="024ee-656">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="024ee-656">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="024ee-657">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="024ee-657">General</span></span>
* <span data-ttu-id="024ee-658">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="024ee-658">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="024ee-659">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="024ee-659">Az.Profile</span></span>
* <span data-ttu-id="024ee-660">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="024ee-660">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="024ee-661">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="024ee-661">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="024ee-662">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="024ee-662">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="024ee-663">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="024ee-663">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="024ee-664">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="024ee-664">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="024ee-665">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="024ee-665">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="024ee-666">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="024ee-666">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="024ee-667">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="024ee-667">Az.CognitiveServices</span></span>
* <span data-ttu-id="024ee-668">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="024ee-668">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="024ee-669">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="024ee-669">Az.Compute</span></span>
* <span data-ttu-id="024ee-670">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="024ee-670">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="024ee-671">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="024ee-671">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="024ee-672">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="024ee-672">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="024ee-673">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="024ee-673">Az.DataLakeStore</span></span>
* <span data-ttu-id="024ee-674">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="024ee-674">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="024ee-675">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="024ee-675">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="024ee-676">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="024ee-676">Az.Insights</span></span>
* <span data-ttu-id="024ee-677">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="024ee-677">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="024ee-678">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="024ee-678">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="024ee-679">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="024ee-679">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="024ee-680">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="024ee-680">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="024ee-681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="024ee-681">Az.Network</span></span>
* <span data-ttu-id="024ee-682">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="024ee-682">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="024ee-683">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="024ee-683">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="024ee-684">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="024ee-684">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="024ee-685">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="024ee-685">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="024ee-686">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="024ee-686">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="024ee-687">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="024ee-687">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="024ee-688">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="024ee-688">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="024ee-689">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="024ee-689">Az.PolicyInsights</span></span>
* <span data-ttu-id="024ee-690">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="024ee-690">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="024ee-691">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="024ee-691">Az.Resources</span></span>
* <span data-ttu-id="024ee-692">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="024ee-692">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="024ee-693">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="024ee-693">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="024ee-694">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="024ee-694">Az.ServiceBus</span></span>
* <span data-ttu-id="024ee-695">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="024ee-695">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="024ee-696">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="024ee-696">Az.ServiceFabric</span></span>
* <span data-ttu-id="024ee-697">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="024ee-697">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="024ee-698">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="024ee-698">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="024ee-699">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="024ee-699">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="024ee-700">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="024ee-700">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="024ee-701">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="024ee-701">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="024ee-702">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="024ee-702">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="024ee-703">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="024ee-703">Az.Profile</span></span>
* <span data-ttu-id="024ee-704">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="024ee-704">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="024ee-705">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="024ee-705">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="024ee-706">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="024ee-706">Az.Compute</span></span>
* <span data-ttu-id="024ee-707">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="024ee-707">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="024ee-708">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="024ee-708">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="024ee-709">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="024ee-709">Az.DataLakeStore</span></span>
* <span data-ttu-id="024ee-710">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="024ee-710">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="024ee-711">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="024ee-711">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="024ee-712">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="024ee-712">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="024ee-713">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="024ee-713">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="024ee-714">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="024ee-714">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="024ee-715">Az.Network</span><span class="sxs-lookup"><span data-stu-id="024ee-715">Az.Network</span></span>
* <span data-ttu-id="024ee-716">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="024ee-716">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="024ee-717">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="024ee-717">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="024ee-718">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="024ee-718">Az.Resources</span></span>
* <span data-ttu-id="024ee-719">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="024ee-719">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="024ee-720">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="024ee-720">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="024ee-721">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="024ee-721">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="024ee-722">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="024ee-722">Azure.Storage</span></span>
* <span data-ttu-id="024ee-723">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="024ee-723">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="024ee-724">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="024ee-724">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="024ee-725">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="024ee-725">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="024ee-726">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="024ee-726">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="024ee-727">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="024ee-727">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="024ee-728">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="024ee-728">Az.CognitiveServices</span></span>
* <span data-ttu-id="024ee-729">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="024ee-729">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="024ee-730">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="024ee-730">Az.Compute</span></span>
* <span data-ttu-id="024ee-731">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="024ee-731">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="024ee-732">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="024ee-732">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="024ee-733">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="024ee-733">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="024ee-734">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="024ee-734">Az.DataFactoryV2</span></span>
* <span data-ttu-id="024ee-735">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="024ee-735">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="024ee-736">Az.Network</span><span class="sxs-lookup"><span data-stu-id="024ee-736">Az.Network</span></span>
* <span data-ttu-id="024ee-737">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="024ee-737">Added NetworkProfile functionality.</span></span> <span data-ttu-id="024ee-738">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="024ee-738">new cmdlets added</span></span>
    - <span data-ttu-id="024ee-739">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="024ee-739">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="024ee-740">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="024ee-740">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="024ee-741">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="024ee-741">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="024ee-742">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="024ee-742">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="024ee-743">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="024ee-743">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="024ee-744">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="024ee-744">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="024ee-745">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="024ee-745">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="024ee-746">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="024ee-746">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="024ee-747">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="024ee-747">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="024ee-748">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="024ee-748">Az.RedisCache</span></span>
* <span data-ttu-id="024ee-749">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="024ee-749">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="024ee-750">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="024ee-750">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="024ee-751">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="024ee-751">Az.Resources</span></span>
* <span data-ttu-id="024ee-752">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="024ee-752">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="024ee-753">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="024ee-753">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="024ee-754">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="024ee-754">Az.Sql</span></span>
* <span data-ttu-id="024ee-755">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="024ee-755">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="024ee-756">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="024ee-756">Az.Websites</span></span>
* <span data-ttu-id="024ee-757">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="024ee-757">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="024ee-758">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="024ee-758">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="024ee-759">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="024ee-759">0.2.0 - September 2018</span></span>
 <span data-ttu-id="024ee-760">Начальный выпуск</span><span class="sxs-lookup"><span data-stu-id="024ee-760">Initial Release</span></span>