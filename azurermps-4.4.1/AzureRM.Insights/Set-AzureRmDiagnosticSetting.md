---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
ms.openlocfilehash: 36e523fbb224b77df205b8c7e7d736af0faa2962
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733367"
---
# <span data-ttu-id="25720-101">Set-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="25720-101">Set-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="25720-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="25720-102">SYNOPSIS</span></span>
<span data-ttu-id="25720-103">Задает параметры журналов и метрик для ресурса.</span><span class="sxs-lookup"><span data-stu-id="25720-103">Sets the logs and metrics settings for the resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25720-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="25720-104">SYNTAX</span></span>

```
Set-AzureRmDiagnosticSetting -ResourceId <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-EventHubAuthorizationRuleId <String>] [-Enabled <Boolean>]
 [-Categories <System.Collections.Generic.List`1[System.String]>]
 [-Timegrains <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="25720-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="25720-105">DESCRIPTION</span></span>
<span data-ttu-id="25720-106">Командлет **Set-AzureRmDiagnosticSetting** включает или выключает каждый Временный промежуток и категорию журнала для определенного ресурса.</span><span class="sxs-lookup"><span data-stu-id="25720-106">The **Set-AzureRmDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>

<span data-ttu-id="25720-107">Журналы и метрики хранятся в указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="25720-107">The logs and metrics are stored in the specified storage account.</span></span>

## <span data-ttu-id="25720-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="25720-108">EXAMPLES</span></span>

### <span data-ttu-id="25720-109">Пример 1: включение всех метрик и журналов для ресурса</span><span class="sxs-lookup"><span data-stu-id="25720-109">Example 1: Enable all metrics and logs for a resource</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="25720-110">Эта команда включает все доступные метрики и журналы для Resource01.</span><span class="sxs-lookup"><span data-stu-id="25720-110">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="25720-111">Пример 2: Отключение всех метрик и журналов</span><span class="sxs-lookup"><span data-stu-id="25720-111">Example 2: Disable all metrics and logs</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="25720-112">Эта команда отключает все доступные метрики и журналы для Resource01 ресурсов.</span><span class="sxs-lookup"><span data-stu-id="25720-112">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="25720-113">Пример 3: включение нескольких категорий</span><span class="sxs-lookup"><span data-stu-id="25720-113">Example 3: Enable multiple categories</span></span>
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

<span data-ttu-id="25720-114">Эта команда включает Category1 и Category2.</span><span class="sxs-lookup"><span data-stu-id="25720-114">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="25720-115">Все timegrains и другие категории остаются прежними.</span><span class="sxs-lookup"><span data-stu-id="25720-115">All timegrains and other categories remain the same.</span></span>

### <span data-ttu-id="25720-116">Пример 4: включение многогранного интервала и нескольких категорий</span><span class="sxs-lookup"><span data-stu-id="25720-116">Example 4: Enable a time grain and multiple categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2 -Timegrains PT1M
```

<span data-ttu-id="25720-117">Эта команда включает только Category1, Category2 и зернистость времени PT1M.</span><span class="sxs-lookup"><span data-stu-id="25720-117">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="25720-118">Все остальные временные Гранки и категории не изменяются.</span><span class="sxs-lookup"><span data-stu-id="25720-118">All other time grains and categories are unchanged.</span></span>

## <span data-ttu-id="25720-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="25720-119">PARAMETERS</span></span>

### <span data-ttu-id="25720-120">-Категории</span><span class="sxs-lookup"><span data-stu-id="25720-120">-Categories</span></span>
<span data-ttu-id="25720-121">Указывает список категорий журналов для включения или отключения в соответствии со значением *Enabled*.</span><span class="sxs-lookup"><span data-stu-id="25720-121">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="25720-122">Если категория не указана, эта команда работает со всеми категориями.</span><span class="sxs-lookup"><span data-stu-id="25720-122">If you do not specify a category, this command operates on all categories.</span></span>

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

### <span data-ttu-id="25720-123">-Включено</span><span class="sxs-lookup"><span data-stu-id="25720-123">-Enabled</span></span>
<span data-ttu-id="25720-124">Указывает, следует ли включить диагностику.</span><span class="sxs-lookup"><span data-stu-id="25720-124">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="25720-125">Укажите $True, чтобы включить диагностику, или $False, чтобы отключить диагностику.</span><span class="sxs-lookup"><span data-stu-id="25720-125">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25720-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25720-126">-ResourceId</span></span>
<span data-ttu-id="25720-127">Указывает идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="25720-127">Specifies the ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25720-128">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="25720-128">-RetentionEnabled</span></span>
<span data-ttu-id="25720-129">Указывает, включена ли хранение диагностических данных.</span><span class="sxs-lookup"><span data-stu-id="25720-129">Indicates whether retention of diagnostic information is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25720-130">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="25720-130">-RetentionInDays</span></span>
<span data-ttu-id="25720-131">Указывает политику хранения в днях.</span><span class="sxs-lookup"><span data-stu-id="25720-131">Specifies the retention policy, in days.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25720-132">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="25720-132">-ServiceBusRuleId</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25720-133">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="25720-133">-StorageAccountId</span></span>
<span data-ttu-id="25720-134">Указывает идентификатор учетной записи хранения, в которой нужно сохранить данные.</span><span class="sxs-lookup"><span data-stu-id="25720-134">Specifies the ID of the Storage account in which to save the data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25720-135">-Timegrains</span><span class="sxs-lookup"><span data-stu-id="25720-135">-Timegrains</span></span>
<span data-ttu-id="25720-136">Задает временные зависимости для включения или отключения метрик в соответствии со значением *Enabled*.</span><span class="sxs-lookup"><span data-stu-id="25720-136">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="25720-137">Если вы не укажете промежуток времени, эта команда будет работать на всех доступных гранях времени.</span><span class="sxs-lookup"><span data-stu-id="25720-137">If you do not specify a time grain, this command operates on all available time grains.</span></span>

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

### <span data-ttu-id="25720-138">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="25720-138">-WorkspaceId</span></span>
<span data-ttu-id="25720-139">Идентификатор рабочей области.</span><span class="sxs-lookup"><span data-stu-id="25720-139">The Id of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25720-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25720-140">-DefaultProfile</span></span>
<span data-ttu-id="25720-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="25720-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25720-142">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="25720-142">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="25720-143">Идентификатор правила центра событий</span><span class="sxs-lookup"><span data-stu-id="25720-143">The event hub rule id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25720-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25720-144">CommonParameters</span></span>
<span data-ttu-id="25720-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="25720-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25720-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25720-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25720-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="25720-147">INPUTS</span></span>

## <span data-ttu-id="25720-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="25720-148">OUTPUTS</span></span>

### <span data-ttu-id="25720-149">Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="25720-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="25720-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="25720-150">NOTES</span></span>

## <span data-ttu-id="25720-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="25720-151">RELATED LINKS</span></span>

[<span data-ttu-id="25720-152">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="25720-152">Get-AzureRmDiagnosticSetting</span></span>](./Get-AzureRmDiagnosticSetting.md)


