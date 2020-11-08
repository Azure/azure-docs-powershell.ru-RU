---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsloadbalancer
schema: 2.0.0
ms.openlocfilehash: 1450a35252a3bd5e749a8ebdb60fda0e8ad35f88
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94077059"
---
# <span data-ttu-id="84109-101">Get-AzsLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="84109-101">Get-AzsLoadBalancer</span></span>

## <span data-ttu-id="84109-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="84109-102">SYNOPSIS</span></span>
<span data-ttu-id="84109-103">Получение списка всех подсистем балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="84109-103">Get a list of all load balancers.</span></span>

## <span data-ttu-id="84109-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="84109-104">SYNTAX</span></span>

```
Get-AzsLoadBalancer [-SubscriptionId <String[]>] [-Filter <String>] [-InlineCount <String>]
 [-OrderBy <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="84109-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="84109-105">DESCRIPTION</span></span>
<span data-ttu-id="84109-106">Получение списка всех подсистем балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="84109-106">Get a list of all load balancers.</span></span>

## <span data-ttu-id="84109-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="84109-107">EXAMPLES</span></span>

### <span data-ttu-id="84109-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="84109-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsLoadBalancer
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsloadbalancer
```



## <span data-ttu-id="84109-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="84109-109">PARAMETERS</span></span>

### <span data-ttu-id="84109-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84109-110">-DefaultProfile</span></span>
<span data-ttu-id="84109-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="84109-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84109-112">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="84109-112">-Filter</span></span>
<span data-ttu-id="84109-113">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="84109-113">OData filter parameter.</span></span>

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

### <span data-ttu-id="84109-114">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="84109-114">-InlineCount</span></span>
<span data-ttu-id="84109-115">Параметр "подсчет в строке" OData.</span><span class="sxs-lookup"><span data-stu-id="84109-115">OData inline count parameter.</span></span>

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

### <span data-ttu-id="84109-116">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="84109-116">-OrderBy</span></span>
<span data-ttu-id="84109-117">Параметр orderBy OData.</span><span class="sxs-lookup"><span data-stu-id="84109-117">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="84109-118">-Skip</span><span class="sxs-lookup"><span data-stu-id="84109-118">-Skip</span></span>
<span data-ttu-id="84109-119">Параметр пропуска OData.</span><span class="sxs-lookup"><span data-stu-id="84109-119">OData skip parameter.</span></span>

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

### <span data-ttu-id="84109-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="84109-120">-SubscriptionId</span></span>
<span data-ttu-id="84109-121">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="84109-121">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="84109-122">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="84109-122">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="84109-123">-Top</span><span class="sxs-lookup"><span data-stu-id="84109-123">-Top</span></span>
<span data-ttu-id="84109-124">Параметр TOP для OData.</span><span class="sxs-lookup"><span data-stu-id="84109-124">OData top parameter.</span></span>

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

### <span data-ttu-id="84109-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84109-125">CommonParameters</span></span>
<span data-ttu-id="84109-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="84109-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84109-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84109-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84109-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="84109-128">INPUTS</span></span>

## <span data-ttu-id="84109-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="84109-129">OUTPUTS</span></span>

### <span data-ttu-id="84109-130">Microsoft. Azure. PowerShell. командлеты. NetworkAdmin. Models. Api20150615. ILoadBalancer</span><span class="sxs-lookup"><span data-stu-id="84109-130">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.ILoadBalancer</span></span>



## <span data-ttu-id="84109-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="84109-131">NOTES</span></span>

## <span data-ttu-id="84109-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="84109-132">RELATED LINKS</span></span>

