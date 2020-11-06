---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/set-azurermdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
ms.openlocfilehash: 086ca93f7b975f6c9b7f4de806dac0c7c99012b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559055"
---
# <span data-ttu-id="55ff6-101">Set-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="55ff6-101">Set-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="55ff6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="55ff6-102">SYNOPSIS</span></span>
<span data-ttu-id="55ff6-103">Задает параметры журналов и метрик для ресурса.</span><span class="sxs-lookup"><span data-stu-id="55ff6-103">Sets the logs and metrics settings for the resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55ff6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="55ff6-104">SYNTAX</span></span>

```
Set-AzureRmDiagnosticSetting -ResourceId <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-EventHubAuthorizationRuleId <String>] [-Enabled <Boolean>]
 [-Categories <System.Collections.Generic.List`1[System.String]>]
 [-Timegrains <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="55ff6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="55ff6-105">DESCRIPTION</span></span>
<span data-ttu-id="55ff6-106">Командлет **Set-AzureRmDiagnosticSetting** включает или выключает каждый Временный промежуток и категорию журнала для определенного ресурса.</span><span class="sxs-lookup"><span data-stu-id="55ff6-106">The **Set-AzureRmDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>

<span data-ttu-id="55ff6-107">Журналы и метрики хранятся в указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="55ff6-107">The logs and metrics are stored in the specified storage account.</span></span>

<span data-ttu-id="55ff6-108">Этот командлет реализует шаблон ShouldProcess, т. е. может запросить подтверждение от пользователя, прежде чем действительно создать, изменить или удалить ресурс.</span><span class="sxs-lookup"><span data-stu-id="55ff6-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="55ff6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="55ff6-109">EXAMPLES</span></span>

### <span data-ttu-id="55ff6-110">Пример 1: включение всех метрик и журналов для ресурса</span><span class="sxs-lookup"><span data-stu-id="55ff6-110">Example 1: Enable all metrics and logs for a resource</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="55ff6-111">Эта команда включает все доступные метрики и журналы для Resource01.</span><span class="sxs-lookup"><span data-stu-id="55ff6-111">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="55ff6-112">Пример 2: Отключение всех метрик и журналов</span><span class="sxs-lookup"><span data-stu-id="55ff6-112">Example 2: Disable all metrics and logs</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="55ff6-113">Эта команда отключает все доступные метрики и журналы для Resource01 ресурсов.</span><span class="sxs-lookup"><span data-stu-id="55ff6-113">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="55ff6-114">Пример 3: включение нескольких категорий</span><span class="sxs-lookup"><span data-stu-id="55ff6-114">Example 3: Enable multiple categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2
StorageAccountId   : <storageAccountId>
StorageAccountName : <storageAccountName>
Metrics
Enabled   : True
Timegrain : PT1M
Enabled   : True
Timegrain : PT1H
Logs
Enabled  : True
Category : Category1
Enabled  : True
Category : Category2
Enabled  : True
Category : Category3
Enabled  : False
Category : Category4
```

<span data-ttu-id="55ff6-115">Эта команда включает Category1 и Category2.</span><span class="sxs-lookup"><span data-stu-id="55ff6-115">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="55ff6-116">Все timegrains и другие категории остаются прежними.</span><span class="sxs-lookup"><span data-stu-id="55ff6-116">All timegrains and other categories remain the same.</span></span>

### <span data-ttu-id="55ff6-117">Пример 4: включение многогранного интервала и нескольких категорий</span><span class="sxs-lookup"><span data-stu-id="55ff6-117">Example 4: Enable a time grain and multiple categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2 -Timegrains PT1M
```

<span data-ttu-id="55ff6-118">Эта команда включает только Category1, Category2 и зернистость времени PT1M.</span><span class="sxs-lookup"><span data-stu-id="55ff6-118">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="55ff6-119">Все остальные временные Гранки и категории не изменяются.</span><span class="sxs-lookup"><span data-stu-id="55ff6-119">All other time grains and categories are unchanged.</span></span>

## <span data-ttu-id="55ff6-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="55ff6-120">PARAMETERS</span></span>

### <span data-ttu-id="55ff6-121">-Категории</span><span class="sxs-lookup"><span data-stu-id="55ff6-121">-Categories</span></span>
<span data-ttu-id="55ff6-122">Указывает список категорий журналов для включения или отключения в соответствии со значением *Enabled*.</span><span class="sxs-lookup"><span data-stu-id="55ff6-122">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="55ff6-123">Если категория не указана, эта команда работает со всеми категориями.</span><span class="sxs-lookup"><span data-stu-id="55ff6-123">If you do not specify a category, this command operates on all categories.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55ff6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55ff6-124">-DefaultProfile</span></span>
<span data-ttu-id="55ff6-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="55ff6-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55ff6-126">-Включено</span><span class="sxs-lookup"><span data-stu-id="55ff6-126">-Enabled</span></span>
<span data-ttu-id="55ff6-127">Указывает, следует ли включить диагностику.</span><span class="sxs-lookup"><span data-stu-id="55ff6-127">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="55ff6-128">Укажите $True, чтобы включить диагностику, или $False, чтобы отключить диагностику.</span><span class="sxs-lookup"><span data-stu-id="55ff6-128">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55ff6-129">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="55ff6-129">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="55ff6-130">Правило центра событий i</span><span class="sxs-lookup"><span data-stu-id="55ff6-130">The event hub rule i</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55ff6-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55ff6-131">-ResourceId</span></span>
<span data-ttu-id="55ff6-132">Указывает идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="55ff6-132">Specifies the ID of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55ff6-133">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="55ff6-133">-RetentionEnabled</span></span>
<span data-ttu-id="55ff6-134">Указывает, включена ли хранение диагностических данных.</span><span class="sxs-lookup"><span data-stu-id="55ff6-134">Indicates whether retention of diagnostic information is enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55ff6-135">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="55ff6-135">-RetentionInDays</span></span>
<span data-ttu-id="55ff6-136">Указывает политику хранения в днях.</span><span class="sxs-lookup"><span data-stu-id="55ff6-136">Specifies the retention policy, in days.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55ff6-137">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="55ff6-137">-ServiceBusRuleId</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55ff6-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="55ff6-138">-StorageAccountId</span></span>
<span data-ttu-id="55ff6-139">Указывает идентификатор учетной записи хранения, в которой нужно сохранить данные.</span><span class="sxs-lookup"><span data-stu-id="55ff6-139">Specifies the ID of the Storage account in which to save the data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55ff6-140">-Timegrains</span><span class="sxs-lookup"><span data-stu-id="55ff6-140">-Timegrains</span></span>
<span data-ttu-id="55ff6-141">Задает временные зависимости для включения или отключения метрик в соответствии со значением *Enabled*.</span><span class="sxs-lookup"><span data-stu-id="55ff6-141">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="55ff6-142">Если вы не укажете промежуток времени, эта команда будет работать на всех доступных гранях времени.</span><span class="sxs-lookup"><span data-stu-id="55ff6-142">If you do not specify a time grain, this command operates on all available time grains.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55ff6-143">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="55ff6-143">-WorkspaceId</span></span>
<span data-ttu-id="55ff6-144">Идентификатор рабочей области.</span><span class="sxs-lookup"><span data-stu-id="55ff6-144">The Id of the workspace</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55ff6-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55ff6-145">CommonParameters</span></span>
<span data-ttu-id="55ff6-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="55ff6-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55ff6-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55ff6-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55ff6-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="55ff6-148">INPUTS</span></span>

### <span data-ttu-id="55ff6-149">Ничего</span><span class="sxs-lookup"><span data-stu-id="55ff6-149">None</span></span>
<span data-ttu-id="55ff6-150">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="55ff6-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="55ff6-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="55ff6-151">OUTPUTS</span></span>

### <span data-ttu-id="55ff6-152">Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="55ff6-152">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="55ff6-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="55ff6-153">NOTES</span></span>

## <span data-ttu-id="55ff6-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="55ff6-154">RELATED LINKS</span></span>

[<span data-ttu-id="55ff6-155">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="55ff6-155">Get-AzureRmDiagnosticSetting</span></span>](./Get-AzureRmDiagnosticSetting.md)


