---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulesource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSource.md
ms.openlocfilehash: 0fe5684805dfc3047abb39040d80eb8a388cf5a2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94064853"
---
# <span data-ttu-id="f1335-101">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="f1335-101">New-AzScheduledQueryRuleSource</span></span>

## <span data-ttu-id="f1335-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f1335-102">SYNOPSIS</span></span>
<span data-ttu-id="f1335-103">Создает объект типа Source (источник)</span><span class="sxs-lookup"><span data-stu-id="f1335-103">Creates an object of type Source</span></span>

## <span data-ttu-id="f1335-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f1335-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSource -Query <String> [-AuthorizedResource <String[]>] -DataSourceId <String>
 [-QueryType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1335-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1335-105">DESCRIPTION</span></span>
<span data-ttu-id="f1335-106">Создает объект типа Source.</span><span class="sxs-lookup"><span data-stu-id="f1335-106">Creates an object of type Source.</span></span>
<span data-ttu-id="f1335-107">Этот объект будет передан команде, которая создает правило оповещения журнала</span><span class="sxs-lookup"><span data-stu-id="f1335-107">This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="f1335-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f1335-108">EXAMPLES</span></span>

### <span data-ttu-id="f1335-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f1335-109">Example 1</span></span>
```powershell
PS C:\> $source = New-AzScheduledQueryRuleSource -Query "Heartbeat | summarize AggregatedValue = count() by bin(TimeGenerated, 5m)"
                  -DataSourceId "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace" 
                  -QueryType "ResultCount"
```

## <span data-ttu-id="f1335-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f1335-110">PARAMETERS</span></span>

### <span data-ttu-id="f1335-111">-AuthorizedResource</span><span class="sxs-lookup"><span data-stu-id="f1335-111">-AuthorizedResource</span></span>
<span data-ttu-id="f1335-112">Список авторизованных ресурсов для этого оповещения</span><span class="sxs-lookup"><span data-stu-id="f1335-112">The list of authorized resources for this alert</span></span>

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

### <span data-ttu-id="f1335-113">-DataSourceId</span><span class="sxs-lookup"><span data-stu-id="f1335-113">-DataSourceId</span></span>
<span data-ttu-id="f1335-114">Источник данных, на котором создано это оповещение</span><span class="sxs-lookup"><span data-stu-id="f1335-114">The data source on which this alert is created</span></span>

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

### <span data-ttu-id="f1335-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1335-115">-DefaultProfile</span></span>
<span data-ttu-id="f1335-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f1335-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1335-117">-Query</span><span class="sxs-lookup"><span data-stu-id="f1335-117">-Query</span></span>
<span data-ttu-id="f1335-118">Запрос на оповещение</span><span class="sxs-lookup"><span data-stu-id="f1335-118">The alert query</span></span>

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

### <span data-ttu-id="f1335-119">-QueryType</span><span class="sxs-lookup"><span data-stu-id="f1335-119">-QueryType</span></span>
<span data-ttu-id="f1335-120">Тип запроса: в настоящее время поддерживаются значения. ResultCount</span><span class="sxs-lookup"><span data-stu-id="f1335-120">Type of Query - currently supported values : ResultCount</span></span>

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

### <span data-ttu-id="f1335-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1335-121">CommonParameters</span></span>
<span data-ttu-id="f1335-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f1335-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1335-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1335-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1335-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f1335-124">INPUTS</span></span>

### <span data-ttu-id="f1335-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="f1335-125">None</span></span>

## <span data-ttu-id="f1335-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1335-126">OUTPUTS</span></span>

### <span data-ttu-id="f1335-127">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="f1335-127">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span></span>

## <span data-ttu-id="f1335-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="f1335-128">NOTES</span></span>

## <span data-ttu-id="f1335-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1335-129">RELATED LINKS</span></span>
