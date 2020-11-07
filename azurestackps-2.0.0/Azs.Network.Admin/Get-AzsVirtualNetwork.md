---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsvirtualnetwork
schema: 2.0.0
ms.openlocfilehash: 2f03d0599a7bfaf2b083b4a6c335b1de98b3fa73
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910492"
---
# <span data-ttu-id="8b061-101">Get-AzsVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8b061-101">Get-AzsVirtualNetwork</span></span>

## <span data-ttu-id="8b061-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8b061-102">SYNOPSIS</span></span>
<span data-ttu-id="8b061-103">Получение списка всех виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="8b061-103">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="8b061-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8b061-104">SYNTAX</span></span>

```
Get-AzsVirtualNetwork [-SubscriptionId <String[]>] [-Filter <String>] [-InlineCount <String>]
 [-OrderBy <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8b061-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b061-105">DESCRIPTION</span></span>
<span data-ttu-id="8b061-106">Получение списка всех виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="8b061-106">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="8b061-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8b061-107">EXAMPLES</span></span>

### <span data-ttu-id="8b061-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8b061-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsVirtualNetwork
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsvirtualnetwork
```

<span data-ttu-id="8b061-109">Возврат списка виртуальных сетей для метки стека Azure.</span><span class="sxs-lookup"><span data-stu-id="8b061-109">Return a list of virtual networks for the Azure Stack stamp.</span></span>

## <span data-ttu-id="8b061-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8b061-110">PARAMETERS</span></span>

### <span data-ttu-id="8b061-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b061-111">-DefaultProfile</span></span>
<span data-ttu-id="8b061-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8b061-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b061-113">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="8b061-113">-Filter</span></span>
<span data-ttu-id="8b061-114">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="8b061-114">OData filter parameter.</span></span>

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

### <span data-ttu-id="8b061-115">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="8b061-115">-InlineCount</span></span>
<span data-ttu-id="8b061-116">Параметр "подсчет в строке" OData.</span><span class="sxs-lookup"><span data-stu-id="8b061-116">OData inline count parameter.</span></span>

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

### <span data-ttu-id="8b061-117">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="8b061-117">-OrderBy</span></span>
<span data-ttu-id="8b061-118">Параметр orderBy OData.</span><span class="sxs-lookup"><span data-stu-id="8b061-118">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="8b061-119">-Skip</span><span class="sxs-lookup"><span data-stu-id="8b061-119">-Skip</span></span>
<span data-ttu-id="8b061-120">Параметр пропуска OData.</span><span class="sxs-lookup"><span data-stu-id="8b061-120">OData skip parameter.</span></span>

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

### <span data-ttu-id="8b061-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8b061-121">-SubscriptionId</span></span>
<span data-ttu-id="8b061-122">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8b061-122">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8b061-123">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="8b061-123">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8b061-124">-Top</span><span class="sxs-lookup"><span data-stu-id="8b061-124">-Top</span></span>
<span data-ttu-id="8b061-125">Параметр TOP для OData.</span><span class="sxs-lookup"><span data-stu-id="8b061-125">OData top parameter.</span></span>

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

### <span data-ttu-id="8b061-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b061-126">CommonParameters</span></span>
<span data-ttu-id="8b061-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8b061-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b061-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b061-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b061-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8b061-129">INPUTS</span></span>

## <span data-ttu-id="8b061-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b061-130">OUTPUTS</span></span>

### <span data-ttu-id="8b061-131">Microsoft. Azure. PowerShell. командлеты. NetworkAdmin. Models. Api20150615. IVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8b061-131">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IVirtualNetwork</span></span>



## <span data-ttu-id="8b061-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="8b061-132">NOTES</span></span>

## <span data-ttu-id="8b061-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8b061-133">RELATED LINKS</span></span>

