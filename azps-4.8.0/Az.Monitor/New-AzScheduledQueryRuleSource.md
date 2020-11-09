---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulesource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSource.md
ms.openlocfilehash: 931b1b39a61b1e2c879b8be1723c5ce9e90638a9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244419"
---
# <span data-ttu-id="40c64-101">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="40c64-101">New-AzScheduledQueryRuleSource</span></span>

## <span data-ttu-id="40c64-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="40c64-102">SYNOPSIS</span></span>
<span data-ttu-id="40c64-103">Создает объект типа Source (источник)</span><span class="sxs-lookup"><span data-stu-id="40c64-103">Creates an object of type Source</span></span>

## <span data-ttu-id="40c64-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="40c64-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSource -Query <String> [-AuthorizedResource <String[]>] -DataSourceId <String>
 [-QueryType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40c64-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="40c64-105">DESCRIPTION</span></span>
<span data-ttu-id="40c64-106">Создает объект типа Source.</span><span class="sxs-lookup"><span data-stu-id="40c64-106">Creates an object of type Source.</span></span>
<span data-ttu-id="40c64-107">Этот объект будет передан команде, которая создает правило оповещения журнала</span><span class="sxs-lookup"><span data-stu-id="40c64-107">This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="40c64-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="40c64-108">EXAMPLES</span></span>

### <span data-ttu-id="40c64-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="40c64-109">Example 1</span></span>
```powershell
PS C:\> $source = New-AzScheduledQueryRuleSource -Query "Heartbeat | summarize AggregatedValue = count() by bin(TimeGenerated, 5m)"
                  -DataSourceId "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace" 
                  -QueryType "ResultCount"
```

### <span data-ttu-id="40c64-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="40c64-110">Example 2</span></span>

<span data-ttu-id="40c64-111">Создает объект типа Source.</span><span class="sxs-lookup"><span data-stu-id="40c64-111">Creates an object of type Source.</span></span> <span data-ttu-id="40c64-112">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="40c64-112">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzScheduledQueryRuleSource -DataSourceId <String> -Query 'Heartbeat | summarize AggregatedValue = count() by bin(TimeGenerated, 5m)'
```

## <span data-ttu-id="40c64-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="40c64-113">PARAMETERS</span></span>

### <span data-ttu-id="40c64-114">-AuthorizedResource</span><span class="sxs-lookup"><span data-stu-id="40c64-114">-AuthorizedResource</span></span>
<span data-ttu-id="40c64-115">Список авторизованных ресурсов для этого оповещения</span><span class="sxs-lookup"><span data-stu-id="40c64-115">The list of authorized resources for this alert</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40c64-116">-DataSourceId</span><span class="sxs-lookup"><span data-stu-id="40c64-116">-DataSourceId</span></span>
<span data-ttu-id="40c64-117">Источник данных, на котором создано это оповещение</span><span class="sxs-lookup"><span data-stu-id="40c64-117">The data source on which this alert is created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40c64-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40c64-118">-DefaultProfile</span></span>
<span data-ttu-id="40c64-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="40c64-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40c64-120">-Query</span><span class="sxs-lookup"><span data-stu-id="40c64-120">-Query</span></span>
<span data-ttu-id="40c64-121">Запрос на оповещение</span><span class="sxs-lookup"><span data-stu-id="40c64-121">The alert query</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40c64-122">-QueryType</span><span class="sxs-lookup"><span data-stu-id="40c64-122">-QueryType</span></span>
<span data-ttu-id="40c64-123">Тип запроса: в настоящее время поддерживаются значения. ResultCount</span><span class="sxs-lookup"><span data-stu-id="40c64-123">Type of Query - currently supported values : ResultCount</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40c64-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40c64-124">CommonParameters</span></span>
<span data-ttu-id="40c64-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="40c64-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40c64-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40c64-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40c64-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="40c64-127">INPUTS</span></span>

### <span data-ttu-id="40c64-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="40c64-128">None</span></span>

## <span data-ttu-id="40c64-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="40c64-129">OUTPUTS</span></span>

### <span data-ttu-id="40c64-130">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="40c64-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span></span>

## <span data-ttu-id="40c64-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="40c64-131">NOTES</span></span>

## <span data-ttu-id="40c64-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="40c64-132">RELATED LINKS</span></span>