---
Module Name: AzureRM.Insights
Module Guid: 698c387c-bd6b-41c6-82ce-721f1ef39548
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/AzureRM.Insights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/AzureRM.Insights.md
ms.openlocfilehash: d4f7819a3ddbf49f4a3c4ed56cd8273b1f2e1848
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93555048"
---
# <span data-ttu-id="4c120-101">Модуль AzureRM. Insights</span><span class="sxs-lookup"><span data-stu-id="4c120-101">AzureRM.Insights Module</span></span>
## <span data-ttu-id="4c120-102">Nописание</span><span class="sxs-lookup"><span data-stu-id="4c120-102">Description</span></span>
<span data-ttu-id="4c120-103">В этом разделе отображаются разделы справки по командлетам Azure Insights.</span><span class="sxs-lookup"><span data-stu-id="4c120-103">This topic displays help topics for the Azure Insights Cmdlets.</span></span>

## <span data-ttu-id="4c120-104">Командлеты AzureRM. Insights</span><span class="sxs-lookup"><span data-stu-id="4c120-104">AzureRM.Insights Cmdlets</span></span>
### [<span data-ttu-id="4c120-105">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="4c120-105">Add-AzureRmAutoscaleSetting</span></span>](Add-AzureRmAutoscaleSetting.md)
<span data-ttu-id="4c120-106">Создание параметра автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="4c120-106">Creates an Autoscale setting.</span></span>

### [<span data-ttu-id="4c120-107">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="4c120-107">Add-AzureRmLogAlertRule</span></span>](Add-AzureRmLogAlertRule.md)
<span data-ttu-id="4c120-108">Добавляет или заменяет правило оповещения в журнале.</span><span class="sxs-lookup"><span data-stu-id="4c120-108">Adds or replaces a log alert rule.</span></span>

### [<span data-ttu-id="4c120-109">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="4c120-109">Add-AzureRmLogProfile</span></span>](Add-AzureRmLogProfile.md)
<span data-ttu-id="4c120-110">Создание нового профиля журнала активности.</span><span class="sxs-lookup"><span data-stu-id="4c120-110">Creates a new activity log profile.</span></span> <span data-ttu-id="4c120-111">Этот профиль используется для архивации журнала активности в учетную запись хранения Azure или потоковой передачи в центр событий Azure в той же подписке.</span><span class="sxs-lookup"><span data-stu-id="4c120-111">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

- <span data-ttu-id="4c120-112">**Учетная** запись хранилища (учетная запись хранилища Premium не поддерживается) поддерживается только для стандартной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="4c120-112">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="4c120-113">Возможно, он либо имеет тип ARM, либо классический.</span><span class="sxs-lookup"><span data-stu-id="4c120-113">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="4c120-114">Если он зарегистрирован в учетной записи хранения, стоимость хранения журнала активности оплачивается по обычным стандартным тарифам на хранение.</span><span class="sxs-lookup"><span data-stu-id="4c120-114">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="4c120-115">На каждую подписку может быть одновременно задан только один профиль, но для экспорта журнала активности можно использовать только одну учетную запись хранения на подписку.</span><span class="sxs-lookup"><span data-stu-id="4c120-115">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 

- <span data-ttu-id="4c120-116">**Центр событий** — для экспорта журнала активности может использоваться только один центр событий на каждую подписку.</span><span class="sxs-lookup"><span data-stu-id="4c120-116">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="4c120-117">Если журнал активности является потоком для концентратора событий, применяются стандартные цены центра событий.</span><span class="sxs-lookup"><span data-stu-id="4c120-117">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> 

<span data-ttu-id="4c120-118">В журнале активности события могут относиться к региону или быть "глобальным".</span><span class="sxs-lookup"><span data-stu-id="4c120-118">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="4c120-119">Глобально, это означает, что эти события не зависят от региона и не зависят от региона, в большинстве событий — в эту категорию.</span><span class="sxs-lookup"><span data-stu-id="4c120-119">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="4c120-120">Если профиль журнала активности задан на портале, он неявно добавляет "Global" вместе с любым другим регионом, выбранным в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="4c120-120">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="4c120-121">При использовании командлета расположение как "Global" должно быть явно упомянуто отдельно от любого другого региона.</span><span class="sxs-lookup"><span data-stu-id="4c120-121">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 

<span data-ttu-id="4c120-122">**Примечание** . Если **вы не можете установить "Global" в указанных ниже областях, это приведет к тому, что журнал активности не будет экспортирован.**</span><span class="sxs-lookup"><span data-stu-id="4c120-122">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> 

### [<span data-ttu-id="4c120-123">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="4c120-123">Add-AzureRmMetricAlertRule</span></span>](Add-AzureRmMetricAlertRule.md)
<span data-ttu-id="4c120-124">Добавляет или обновляет правило оповещения на основе метрики.</span><span class="sxs-lookup"><span data-stu-id="4c120-124">Adds or updates a metric-based alert rule.</span></span>

### [<span data-ttu-id="4c120-125">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="4c120-125">Add-AzureRmWebtestAlertRule</span></span>](Add-AzureRmWebtestAlertRule.md)
<span data-ttu-id="4c120-126">Добавляет или обновляет правило оповещения для веб-теста.</span><span class="sxs-lookup"><span data-stu-id="4c120-126">Adds or updates a webtest alert rule.</span></span>

### [<span data-ttu-id="4c120-127">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4c120-127">Disable-AzureRmActivityLogAlert</span></span>](Disable-AzureRmActivityLogAlert.md)
<span data-ttu-id="4c120-128">Отключает оповещение журнала активности и задает его Теги.</span><span class="sxs-lookup"><span data-stu-id="4c120-128">Disables an activity log alert and sets its tags.</span></span>

### [<span data-ttu-id="4c120-129">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4c120-129">Enable-AzureRmActivityLogAlert</span></span>](Enable-AzureRmActivityLogAlert.md)
<span data-ttu-id="4c120-130">Включает предупреждение журнала активности и задает его Теги.</span><span class="sxs-lookup"><span data-stu-id="4c120-130">Enables an activity log alert and sets its Tags.</span></span>

### [<span data-ttu-id="4c120-131">Get-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="4c120-131">Get-AzureRmActionGroup</span></span>](Get-AzureRmActionGroup.md)
<span data-ttu-id="4c120-132">Получает группу действий.</span><span class="sxs-lookup"><span data-stu-id="4c120-132">Gets action group(s).</span></span>

### [<span data-ttu-id="4c120-133">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4c120-133">Get-AzureRmActivityLogAlert</span></span>](Get-AzureRmActivityLogAlert.md)
<span data-ttu-id="4c120-134">Получает один или несколько ресурсов для оповещения журнала активности.</span><span class="sxs-lookup"><span data-stu-id="4c120-134">Gets one or more activity log alert resources.</span></span>

### [<span data-ttu-id="4c120-135">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="4c120-135">Get-AzureRmAlertHistory</span></span>](Get-AzureRmAlertHistory.md)
<span data-ttu-id="4c120-136">Получает историю оповещений.</span><span class="sxs-lookup"><span data-stu-id="4c120-136">Gets the history of alerts.</span></span>

### [<span data-ttu-id="4c120-137">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="4c120-137">Get-AzureRmAlertRule</span></span>](Get-AzureRmAlertRule.md)
<span data-ttu-id="4c120-138">Возвращает правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="4c120-138">Gets alert rules.</span></span>

### [<span data-ttu-id="4c120-139">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="4c120-139">Get-AzureRmAutoscaleHistory</span></span>](Get-AzureRmAutoscaleHistory.md)
<span data-ttu-id="4c120-140">Получает журнал автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="4c120-140">Gets the Autoscale history.</span></span>

### [<span data-ttu-id="4c120-141">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="4c120-141">Get-AzureRmAutoscaleSetting</span></span>](Get-AzureRmAutoscaleSetting.md)
<span data-ttu-id="4c120-142">Получает параметры автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="4c120-142">Gets Autoscale settings.</span></span>

### [<span data-ttu-id="4c120-143">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="4c120-143">Get-AzureRmDiagnosticSetting</span></span>](Get-AzureRmDiagnosticSetting.md)
<span data-ttu-id="4c120-144">Получает записанные в журнал временные Гранки и категории.</span><span class="sxs-lookup"><span data-stu-id="4c120-144">Gets the logged categories and time grains.</span></span>

### [<span data-ttu-id="4c120-145">Get-AzureRmLog</span><span class="sxs-lookup"><span data-stu-id="4c120-145">Get-AzureRmLog</span></span>](Get-AzureRmLog.md)
<span data-ttu-id="4c120-146">Возвращает журнал событий.</span><span class="sxs-lookup"><span data-stu-id="4c120-146">Gets a log of events.</span></span>

### [<span data-ttu-id="4c120-147">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="4c120-147">Get-AzureRmLogProfile</span></span>](Get-AzureRmLogProfile.md)
<span data-ttu-id="4c120-148">Получает профиль журнала.</span><span class="sxs-lookup"><span data-stu-id="4c120-148">Gets a log profile.</span></span>

### [<span data-ttu-id="4c120-149">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="4c120-149">Get-AzureRmMetric</span></span>](Get-AzureRmMetric.md)
<span data-ttu-id="4c120-150">Возвращает значения метрик ресурса.</span><span class="sxs-lookup"><span data-stu-id="4c120-150">Gets the metric values of a resource.</span></span>

### [<span data-ttu-id="4c120-151">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="4c120-151">Get-AzureRmMetricDefinition</span></span>](Get-AzureRmMetricDefinition.md)
<span data-ttu-id="4c120-152">Получение определений метрик.</span><span class="sxs-lookup"><span data-stu-id="4c120-152">Gets metric definitions.</span></span>

### [<span data-ttu-id="4c120-153">Get-AzureRmUsage</span><span class="sxs-lookup"><span data-stu-id="4c120-153">Get-AzureRmUsage</span></span>](Get-AzureRmUsage.md)
<span data-ttu-id="4c120-154">Получает метрики использования для ресурса.</span><span class="sxs-lookup"><span data-stu-id="4c120-154">Gets the usage metrics for a resource.</span></span>

### [<span data-ttu-id="4c120-155">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="4c120-155">New-AzureRmActionGroup</span></span>](New-AzureRmActionGroup.md)
<span data-ttu-id="4c120-156">Создает объект ссылки на ActionGroup в памяти.</span><span class="sxs-lookup"><span data-stu-id="4c120-156">Creates an ActionGroup reference object in memory.</span></span>

### [<span data-ttu-id="4c120-157">New-AzureRmActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="4c120-157">New-AzureRmActionGroupReceiver</span></span>](New-AzureRmActionGroupReceiver.md)
<span data-ttu-id="4c120-158">Создает нового приемника группы действий.</span><span class="sxs-lookup"><span data-stu-id="4c120-158">Creates an new action group receiver.</span></span>

### [<span data-ttu-id="4c120-159">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="4c120-159">New-AzureRmActivityLogAlertCondition</span></span>](New-AzureRmActivityLogAlertCondition.md)
<span data-ttu-id="4c120-160">Создает новый объект условия предупреждения журнала активности в памяти.</span><span class="sxs-lookup"><span data-stu-id="4c120-160">Creates an new activity log alert condition object in memory.</span></span>

### [<span data-ttu-id="4c120-161">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="4c120-161">New-AzureRmAlertRuleEmail</span></span>](New-AzureRmAlertRuleEmail.md)
<span data-ttu-id="4c120-162">Создание действия электронной почты для правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="4c120-162">Creates an email action for an alert rule.</span></span>

### [<span data-ttu-id="4c120-163">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="4c120-163">New-AzureRmAlertRuleWebhook</span></span>](New-AzureRmAlertRuleWebhook.md)
<span data-ttu-id="4c120-164">Создание веб-перехватчика правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="4c120-164">Creates an alert rule webhook.</span></span>

### [<span data-ttu-id="4c120-165">New-AzureRmAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="4c120-165">New-AzureRmAutoscaleNotification</span></span>](New-AzureRmAutoscaleNotification.md)
<span data-ttu-id="4c120-166">Создает уведомление об автомасштабировании электронной почты.</span><span class="sxs-lookup"><span data-stu-id="4c120-166">Creates an Autoscale email notification.</span></span>

### [<span data-ttu-id="4c120-167">New-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="4c120-167">New-AzureRmAutoscaleProfile</span></span>](New-AzureRmAutoscaleProfile.md)
<span data-ttu-id="4c120-168">Создание профиля автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="4c120-168">Creates an Autoscale profile.</span></span>

### [<span data-ttu-id="4c120-169">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="4c120-169">New-AzureRmAutoscaleRule</span></span>](New-AzureRmAutoscaleRule.md)
<span data-ttu-id="4c120-170">Создает правило автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="4c120-170">Creates an Autoscale rule.</span></span>

### [<span data-ttu-id="4c120-171">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="4c120-171">New-AzureRmAutoscaleWebhook</span></span>](New-AzureRmAutoscaleWebhook.md)
<span data-ttu-id="4c120-172">Создание веб-перехватчика автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="4c120-172">Creates an Autoscale webhook.</span></span>

### [<span data-ttu-id="4c120-173">Remove-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="4c120-173">Remove-AzureRmActionGroup</span></span>](Remove-AzureRmActionGroup.md)
<span data-ttu-id="4c120-174">Удаление группы действий.</span><span class="sxs-lookup"><span data-stu-id="4c120-174">Removes an action group.</span></span>

### [<span data-ttu-id="4c120-175">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4c120-175">Remove-AzureRmActivityLogAlert</span></span>](Remove-AzureRmActivityLogAlert.md)
<span data-ttu-id="4c120-176">Удаляет оповещение журнала активности.</span><span class="sxs-lookup"><span data-stu-id="4c120-176">Removes an activity log alert.</span></span>

### [<span data-ttu-id="4c120-177">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="4c120-177">Remove-AzureRmAlertRule</span></span>](Remove-AzureRmAlertRule.md)
<span data-ttu-id="4c120-178">Удаление правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="4c120-178">Removes an alert rule.</span></span>

### [<span data-ttu-id="4c120-179">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="4c120-179">Remove-AzureRmAutoscaleSetting</span></span>](Remove-AzureRmAutoscaleSetting.md)
<span data-ttu-id="4c120-180">Удаление параметра автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="4c120-180">Removes an Autoscale setting.</span></span>

### [<span data-ttu-id="4c120-181">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="4c120-181">Remove-AzureRmLogProfile</span></span>](Remove-AzureRmLogProfile.md)
<span data-ttu-id="4c120-182">Удаление профиля журнала.</span><span class="sxs-lookup"><span data-stu-id="4c120-182">Removes a log profile.</span></span>

### [<span data-ttu-id="4c120-183">Set-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="4c120-183">Set-AzureRmActionGroup</span></span>](Set-AzureRmActionGroup.md)
<span data-ttu-id="4c120-184">Создает новую или обновляет существующую группу действий.</span><span class="sxs-lookup"><span data-stu-id="4c120-184">Creates a new or updates an existing action group.</span></span>

### [<span data-ttu-id="4c120-185">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4c120-185">Set-AzureRmActivityLogAlert</span></span>](Set-AzureRmActivityLogAlert.md)
<span data-ttu-id="4c120-186">Создание нового или установка существующего оповещения журнала активности.</span><span class="sxs-lookup"><span data-stu-id="4c120-186">Creates a new or sets an existing activity log alert.</span></span>

### [<span data-ttu-id="4c120-187">Set-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="4c120-187">Set-AzureRmDiagnosticSetting</span></span>](Set-AzureRmDiagnosticSetting.md)
<span data-ttu-id="4c120-188">Задает параметры журналов и метрик для ресурса.</span><span class="sxs-lookup"><span data-stu-id="4c120-188">Sets the logs and metrics settings for the resource.</span></span>

