---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsplanmetric
schema: 2.0.0
ms.openlocfilehash: 9a8ef074cf6e59d30217b55b956a4d5101708bcc
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076992"
---
# <span data-ttu-id="e20e6-101">Get-AzsPlanMetric</span><span class="sxs-lookup"><span data-stu-id="e20e6-101">Get-AzsPlanMetric</span></span>

## <span data-ttu-id="e20e6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e20e6-102">SYNOPSIS</span></span>
<span data-ttu-id="e20e6-103">Получение метрик указанного плана.</span><span class="sxs-lookup"><span data-stu-id="e20e6-103">Get the metrics of the specified plan.</span></span>

## <span data-ttu-id="e20e6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e20e6-104">SYNTAX</span></span>

```
Get-AzsPlanMetric -PlanName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e20e6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e20e6-105">DESCRIPTION</span></span>
<span data-ttu-id="e20e6-106">Получение метрик указанного плана.</span><span class="sxs-lookup"><span data-stu-id="e20e6-106">Get the metrics of the specified plan.</span></span>

## <span data-ttu-id="e20e6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e20e6-107">EXAMPLES</span></span>

### <span data-ttu-id="e20e6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e20e6-108">Example 1</span></span>
```powershell
PS C:\> Get-AzsPlanMetric -PlanName "testplan" -ResourceGroupName "testrg"

EndTime               MetricUnit StartTime            TimeGrain
-------               ---------- ---------            ---------
3/13/2020 12:06:16 AM Count      3/6/2020 12:00:00 AM P1D      
3/13/2020 12:06:16 AM Count      3/6/2020 12:00:00 AM P1D
```

<span data-ttu-id="e20e6-109">Получение метрик плана.</span><span class="sxs-lookup"><span data-stu-id="e20e6-109">Get a plan's metrics.</span></span>

## <span data-ttu-id="e20e6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e20e6-110">PARAMETERS</span></span>

### <span data-ttu-id="e20e6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e20e6-111">-DefaultProfile</span></span>
<span data-ttu-id="e20e6-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e20e6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e20e6-113">-PlanName</span><span class="sxs-lookup"><span data-stu-id="e20e6-113">-PlanName</span></span>
<span data-ttu-id="e20e6-114">Название плана.</span><span class="sxs-lookup"><span data-stu-id="e20e6-114">Name of the plan.</span></span>

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

### <span data-ttu-id="e20e6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e20e6-115">-ResourceGroupName</span></span>
<span data-ttu-id="e20e6-116">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="e20e6-116">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="e20e6-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e20e6-117">-SubscriptionId</span></span>
<span data-ttu-id="e20e6-118">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="e20e6-118">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e20e6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e20e6-119">CommonParameters</span></span>
<span data-ttu-id="e20e6-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e20e6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e20e6-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e20e6-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e20e6-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e20e6-122">INPUTS</span></span>

## <span data-ttu-id="e20e6-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e20e6-123">OUTPUTS</span></span>

### <span data-ttu-id="e20e6-124">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. Api20151101. IMetricList</span><span class="sxs-lookup"><span data-stu-id="e20e6-124">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMetricList</span></span>

<span data-ttu-id="e20e6-125">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="e20e6-125">ALIASES</span></span>

## <span data-ttu-id="e20e6-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="e20e6-126">NOTES</span></span>

## <span data-ttu-id="e20e6-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e20e6-127">RELATED LINKS</span></span>

