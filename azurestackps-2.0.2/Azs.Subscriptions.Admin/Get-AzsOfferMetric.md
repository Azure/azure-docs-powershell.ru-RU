---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsoffermetric
schema: 2.0.0
ms.openlocfilehash: 515cf3d9c26c9ca4ed59178e49854e23edfea84c
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076997"
---
# <span data-ttu-id="3882c-101">Get-AzsOfferMetric</span><span class="sxs-lookup"><span data-stu-id="3882c-101">Get-AzsOfferMetric</span></span>

## <span data-ttu-id="3882c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3882c-102">SYNOPSIS</span></span>
<span data-ttu-id="3882c-103">Получение метрик предложения.</span><span class="sxs-lookup"><span data-stu-id="3882c-103">Get the offer metrics.</span></span>

## <span data-ttu-id="3882c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3882c-104">SYNTAX</span></span>

```
Get-AzsOfferMetric -OfferName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3882c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3882c-105">DESCRIPTION</span></span>
<span data-ttu-id="3882c-106">Получение метрик предложения.</span><span class="sxs-lookup"><span data-stu-id="3882c-106">Get the offer metrics.</span></span>

## <span data-ttu-id="3882c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3882c-107">EXAMPLES</span></span>

### <span data-ttu-id="3882c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3882c-108">Example 1</span></span>
```powershell
PS C:\> Get-AzsOfferMetric -OfferName "testoffer" -ResourceGroupName "testrg"

EndTime               MetricUnit StartTime            TimeGrain
-------               ---------- ---------            ---------
3/13/2020 12:04:33 AM Count      3/6/2020 12:00:00 AM P1D      
3/13/2020 12:04:33 AM Count      3/6/2020 12:00:00 AM P1D
```

<span data-ttu-id="3882c-109">Получение метрик предложения.</span><span class="sxs-lookup"><span data-stu-id="3882c-109">Get the offer metrics.</span></span>

## <span data-ttu-id="3882c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3882c-110">PARAMETERS</span></span>

### <span data-ttu-id="3882c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3882c-111">-DefaultProfile</span></span>
<span data-ttu-id="3882c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3882c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3882c-113">-OfferName</span><span class="sxs-lookup"><span data-stu-id="3882c-113">-OfferName</span></span>
<span data-ttu-id="3882c-114">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="3882c-114">Name of an offer.</span></span>

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

### <span data-ttu-id="3882c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3882c-115">-ResourceGroupName</span></span>
<span data-ttu-id="3882c-116">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="3882c-116">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="3882c-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3882c-117">-SubscriptionId</span></span>
<span data-ttu-id="3882c-118">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="3882c-118">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3882c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3882c-119">CommonParameters</span></span>
<span data-ttu-id="3882c-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3882c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3882c-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3882c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3882c-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3882c-122">INPUTS</span></span>

## <span data-ttu-id="3882c-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3882c-123">OUTPUTS</span></span>

### <span data-ttu-id="3882c-124">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. Api20151101. IMetricList</span><span class="sxs-lookup"><span data-stu-id="3882c-124">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMetricList</span></span>

<span data-ttu-id="3882c-125">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="3882c-125">ALIASES</span></span>

## <span data-ttu-id="3882c-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="3882c-126">NOTES</span></span>

## <span data-ttu-id="3882c-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3882c-127">RELATED LINKS</span></span>

